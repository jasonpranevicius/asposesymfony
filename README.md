#Aspose Cloud for Symfony

This bundle allows you to work with [Aspose Cloud SDK](https://cloud.aspose.com/) in your Symfony applications 


Installation
----------------------------------

Add the following lines to your composer.json file:

```json
// composer.json
{
    require: {
        "aspose/cloud-bundle": "dev-master"
    }
}
```

Install the new dependencies by running `composer update` from the directory where your composer.json file is located.

Update your `AppKernel.php` by registering the new bundle:

```php
// app/AppKernel.php
public function registerBundles()
{
    // ...
     new Aspose\Bundle\CloudBundle\AsposeCloudBundle(),
    // ...
);
}
```

Add you Aspose API key to your config

```yml
// app/config/config.yml

aspose_cloud:
    url: http://api.aspose.com/v1.1
    app:
        sid: yoursidhere
        key: yourkeyhere
        outputLocation: "%kernel.cache_dir%/aspose_cloud/" # let the API save files in the cache directory by default
```


Usage
----------------------------------

To configure the initial credentials in the static fields of the `AsposeApp`, first get it from the container

```
// Bundle/Controller/DemoController.php
$app = $this->get('aspose.app');

$wordConverter = $this->get('aspose.wordsconverter');
$wordConverter->setFilename($absolutePath)
              ->convert();

```
