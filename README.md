JVMimeTypes - JV Mime Types
================
Create By: Jaime Marcelo Valasek

Use this module to validate the file upload using mime-types or extensions.

Futures video lessons can be developed and published on the website or Youtube channel http://www.zf2.com.br/tutoriais http://www.youtube.com/zf2tutoriais

Installation
-----
Download this module into your vendor folder.

After done the above steps, open the file `config/application.config.php`. And add the module with the name `JVMimeTypes`.


Using the JVMimeTypes
-----
Instantiating the class module JVMimeTypes
```php
$serviceMimeTypes = new MimeTypes($this->getServiceLocator()->get('servicemanager'));
```

```php
/*
 * Listing the mime types with extensions as an index - custom
 * Passing false as the second parameter returns the numerical indices
 */
exit(print_r($serviceMimeTypes->getMimeTypeCustom(array('ext-audio-min'))));

// result
Array
(
    [mp3] => video/x-mpeg
    [wma] => audio/x-ms-wma
)

/* 
 * Listing extensions custom audio
 */
exit(print_r($serviceMimeTypes->getExtCustom(array('ext-audio-min'))));

// result
Array
(
    [0] => mp3
    [1] => wma
)
```
All methods available
-----

 - Methods to bring standard file extensions
`getExtImage();`
`getExtAudio();`
`getExtVideo();`
`getExtApplication();`
`getExtText();`
`getExtFiles();`

 - Methods patterns to bring the mime types of files
`getMimeTypeImage()`
`getMimeTypeAudio()`
`getMimeTypeVideo()`
`getMimeTypeApplication()`
`getMimeTypeText()`
`getMimeTypeFiles()`

 - Methods custom - create your own profiles mime types accessing the file `config/module.config.php` just follow the examples are there and call the custom method, for example:
`getExtCustom(array('ext-audio-min'));`
`getMimeTypeCustom(array('ext-audio-min'));`
 

