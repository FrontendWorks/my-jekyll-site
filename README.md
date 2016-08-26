# Codonomics Web-Site

## TODOs

* Minify and Combine CSS
* Minify and Combine JS
* Enable GZip compression
* Explore Asset pipelines for Jekyll using (jekyll-assets or anything else)
* Explore using http://fontello.com/ instead of fontawesome or other font files, to reduce footprint and increase page speed
* Leverage Browser cacheing
* Remove Unused CSS Rules


## Performance Improvements

The following things are done to improve the performance of the site
* Improve Website Load Times Using Progressive JPEGs. Use `-interlace` option in ImageMagic's `convert` command for this.
* Compress images for faster page loading. You can run the following command in mac's commandline to reduce the image size (ImageMagic should be imstalled before this.) 
`convert -strip -interlace Plane -gaussian-blur 0.5 -quality 25 -fuzz 40% banner.jpg banner5.jpg`

## References for further reading
* [Efficient Image Resizing With ImageMagick](https://www.smashingmagazine.com/2015/06/efficient-image-resizing-with-imagemagick/)
* [How does progressive JPEG work?](http://pooyak.com/p/progjpeg/)
* [Use ImageMagick to create optimised and progressive JPGs](https://coderwall.com/p/ryzmaa/use-imagemagick-to-create-optimised-and-progressive-jpgs)
* [YUIBlogDevelopmentImage Optimization, Part 4: Progressive JPEG...Hot or Not?
Image Optimization, Part 4: Progressive JPEG...Hot or Not?](http://yuiblog.com/blog/2008/12/05/imageopt-4/)