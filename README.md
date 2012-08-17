# thumber

__Creates image thumbnails from PDF files.__

_Thumber_ generates thumbnails from your PDFs. You can call it using a single tag in your template.

### Example usage:

```
{exp:thumber:create src="/uploads/documents/yourfile.pdf" page='1' extension='jpg' height='250' class='awesome' title='Click to download' link='yes'}
```

### Parameters:
 - `src`: The source PDF ___[Required]___
 - `width`: The width of the generated thumbnail
 - `height`: The height of the generated thumbnail
 - `page`: The page of the PDF used to generate the thumbnail ___[Default: 1]___
 - `extension`: The file type of the generated thumbnail ___[Default: png]___
 - `link`: Wrap the thumbnail in a link to the PDF ___[Default: no]___
 - `crop`: Where `width` and `height` are both specified, crop to preserve aspect ratio ___[Default: yes]___

Any other parameters will be added to the `img` tag in the the generated html snippet - so if you want to add an `id` or `class`, just add them as parameters.

### Requirements:
 - This plugin requires [ImageMagick](http://www.imagemagick.org/) and [Ghostscript](http://www.ghostscript.com/) to be installed
 - You should create a directory for your cached thumbnails to live. The default directory is specified as `/images/thumber`. _Thumber_ should have permissions to write to this directory

### Todos:
 - Improve caching (e.g. add an expiry time to cached images)
 - Add more parameters, e.g. `max_width`, `max_height`
 - Allow for tag pairs as well as single tags