# mosaic
(forked from [codebox](https://github.com/codebox/mosaic))
In contrast to the original code, you don't need a large set of images. You can use a small set of images which will be color corrected to fit the target image. 

This utility can be used to generate [photo-mosaic](http://en.wikipedia.org/wiki/Photographic_mosaic) images, to use it you must have Python installed, along with the [Pillow](http://pillow.readthedocs.org/en/latest/) imaging library.

Run the utility from the command line, as follows:

<pre>python mosaic.py &lt;image&gt; &lt;tiles directory&gt;
</pre>

*   The `image` argument should contain the path to the image for which you want to build the mosaic
*   The `tiles directory` argument should contain the path to the directory containing the tile images (the directory will be searched recursively, so it doesn't matter if some of the images are contained in sub-directories)

For example:

<pre>python mosaic.py game_of_thrones_poster.jpg /home/admin/images/screenshots
</pre>

The images below show an example of how the mosaic tiles are matched to the details of the original image:

![Mosaic Image](http://codebox.org.uk/graphics/mosaic/mosaic_small.jpg)  
<span class="smallText">Original</span>

[![Mosaic Image Detail](http://codebox.org.uk/graphics/mosaic/mosaic_detail.jpg)](http://codebox.org.uk/graphics/mosaic/mosaic_large.jpg)  
<span class="smallText">Mosaic Detail (click through for [full mosaic](http://codebox.org.uk/graphics/mosaic/mosaic_large.jpg) ~15MB)</span>

Producing large, highly detailed mosaics can take some time - you should experiment with the various [configuration parameters](https://github.com/codebox/mosaic/blob/master/mosaic.py#L6) explained in the source code to find the right balance between image quality and render time.
