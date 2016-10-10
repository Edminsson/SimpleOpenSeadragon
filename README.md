# The most simple page using openseadragon and openseadragonFiltering

I don't know how to best install openseadragonFiltering. Trying to access the master branch in the bower file directly does not seem to work. I installed the file manually. 

I had to set crossOriginPolicy to anonymous to avoid the following error

    Uncaught SecurityError: Failed to execute 'getImageData' on 'CanvasRenderingContext2D': The canvas has been tainted by cross-origin data.

Openseadragon did not set crossorigin property in the img element but the error is still a cross site error.
Could it be because the server returns a CrossControlAllowOrigin header? 



### To install
- install bower
- use http-server
