#Aspose Cloud for Symfony

This bundle allows you to work with Aspose Cloud SDK in your Symfony applications quickly and easily. 


Installation
----------------------------------

Add the following lines to your composer.json file:

<pre>
// composer.json
{
    // ...
    require: {
        // ..        
        "aspose/cloud-bundle": "dev-master"

    }
}
</pre>


Now, you can install the new dependencies by running Composer's update command from the directory where your composer.json file is located.

<pre>
    composer update
</pre>


Update your AppKernel.php file, and register the new bundle:

<pre>
// app/AppKernel.php
public function registerBundles()
{
    // ...
     new Aspose\Bundle\CloudBundle\AsposeCloudBundle(),
    // ...
);
}
</pre>

Usage
----------------------------------

The Bundle is called as a standard service.

<pre>
$this->get('asposeapp');
</pre>

This will return you object of Product class and you can access properties and methods of class.
