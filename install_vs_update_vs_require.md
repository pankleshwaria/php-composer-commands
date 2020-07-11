# composer install vs update vs require

## composer install
composer install will not update anything; it will just install all the dependencies as specified in the composer.lock file

In detail composer install will:

- Check if composer.lock file exists (if not, run composer-update and create it)
- Read composer.lock file
- Install the packages specified in the composer.lock file

## composer update
composer update will update your depencencies as they are specified in composer.json

For example, if you require this package as a dependency:

"twig/twig": "0.9.*",
and you have actually installed the 0.9.1 version of the package, running composer update will cause an upgrade of this package (for example to 0.9.2, if it's already been released)

In detail composer update will:

- Read composer.json
- Remove installed packages that are no more required in composer.json
- Check the availability of the latest versions of your required packages
- Install the latest versions of your packages
- Update composer.lock to store the installed packages version

## composer require
composer require will add depencency to your composer.json file, then it will install the dependencies and update the composer.lock file

In detail composer require will:

- Add required depencency in your composer.json file
- Check the availability of the latest versions of your required packages (package specified in require)
- Install the latest versions of your packages
- Update composer.lock to store the installed packages version

## When to install, when to update and when to require

composer update is mostly used in the 'development phase', to upgrade our project packages according to what we have specified in the composer.json file.

composer install is primarily used in the 'deploying phase' to install our application on a production server or on a testing environment, using the same dependencies stored in the composer.lock file created by composer update.

composer require is used when you need to add new dependencies to your project. You need to commit your composer.lock file along with composer.json so that when composer install is runned in 'deployment phase' the new dependencies are downloaded.

## Contributing and Licence
This repo is only for educational purpose. Feel free to do clone, modify and share this repository.
If you find an error or have questions, feel free to write in comments or raise an issue. If you want to contribute, feel free to hand in a 
pull-request.
