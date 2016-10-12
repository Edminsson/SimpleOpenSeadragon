# The most simple page using openseadragon and openseadragonFiltering

OpenseadragonFiltering is listed as a plugin http://openseadragon.github.io/#plugins

I don't know how to best install openseadragonFiltering. Trying to access the master branch in the bower file directly does not seem to work. I installed the file manually. 

I had to set crossOriginPolicy to anonymous to avoid the following error

    Uncaught SecurityError: Failed to execute 'getImageData' on 'CanvasRenderingContext2D': The canvas has been tainted by cross-origin data.

Openseadragon did not set crossorigin property in the img element but the error is still a cross site error.

The same thing happened when I loaded an Image into a canvas and try to apply a filter programmatically.
I solved it the same way by setting crossOrigin to anonymous directly on the Image-object.

Then I decided to apply my own filter to openseadragon the same way that openseadragonFiltering does.
So I added a handler to the openseadragon event tile-drawing and changed the canvas myself. This code is in
the ownFilter page.



### To install
- install bower
- use http-server
- browse to index.html, canvasIndex.html and ownfilter.html.
