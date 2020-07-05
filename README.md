## php-composer-commands
A list of basic PHP composer commands that you will end up using the most.

# Composer
Composer is the dependency management tool in PHP. It It allows you to declare the librarie that your project depends on and it will manage (install/update) them for you.

# System Requirments
- Composer only works with PHP 5.3.2 and above to run.
- You need Composer installed. (To check if the composer is installed open CMD/Terminal run command composer).
- To start using composer in your project you need a composer.json file. This file describes the dependencies of your project and contains other metadata.
- Composer is multi-platform and will runs equally with on Windows, Linux, and MacOs.

# Composer commands

```
composer init
```
Creates a composer.json file in the current directory.

```
composer install
```
To install the dependencies defined in the composer.json file you run the install command. 
When you run the install command two things happen:
- It installs all the dependencies specified in composer.json file.
- It creates composer.lock file. composer.lock file contains info about all the packages that were installed and their exact version.

```
composer update
```
Updates all the dependencies of your project to their latest versions.
This is equivalent to deleting the composer.lock file and running install again.

```
composer update vendor/package1 vendor/package2
```
This will update only the packages that are specified and not all.

```
composer require "vendor/package:3.*"
```
Adds a new package to your composer.json file.

```
composer remove vendor/package
```
Remove the package from composer.json file.
After removing the requirements, the modified requirements will be uninstalled.

```
composer show
```
Shows the list of all the available packages.

```
composer search monolog
```
Search package with name monoloag.
Usually, this will search for packagist.org for the package mentioned.

```
composer show monoloag/*
```
To filter the list you can also pass wildcards.

## Contributing and Licence
This repo is only for educational purpose. Feel free to do clone, modify and share this repository.
If you find an error or have questions, feel free to write in comments or raise an issue. If you want to contribute, feel free to hand in a 
pull-request.
