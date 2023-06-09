# MicroSymfony 🎶

MicroSymfony is a template to initialize an application to use Symfony as a microframework.

It can be used to create a POC or prototyping something without having to take care
of the design, while having something still enjoyable (and fit to be seen).

Even it is minimalist, we don't want to sacrifice quality.
There are some tests (100% coverage) and CS checks: php-cs-fixer + PHPStan. 

It's not really intented to be used in production, use a your onw risks.
Well at least you should remove the classless framework to use a modern CSS framework.


## Demo 🌈

Because a live demo is always better than all explanations. Here is it:

* Live demo at [https://microsymfony.ovh](https://microsymfony.ovh)


## Todo 🖋 


## To try/test 💡

* try dropin minimal: https://github.com/dohliam/dropin-minimal-css


## Requirements ⚙

* [PHP 8.1](https://www.php.net/releases/8.1/en.php)
* The [Symfony CLI](https://symfony.com/download)
* The [Xdebug](https://xdebug.org/) PHP extension if you want to run the code coverage report


## Stack 🔗

* [Symfony 6.3](https://symfony.com)
* [Twig 3](https://twig.symfony.com)
* [Stimulus 3.2](https://stimulus.hotwired.dev/)
* [PHPUnit 9.5](https://phpunit.de)
* The classless [BareCSS](http://barecss.com) CSS framework 


## Barecss forks 🎨

* https://github.com/zonradkuse


## What does it ship? 🚀

* A [demo with some JavaScript and Stimulus using the new Sf 6.3 asset mapper component](https://github.com/strangebuzz/MicroSymfony/blob/main/templates/stimulus.html.twig) 
* A [default error page extending the base layout](https://github.com/strangebuzz/symfony-micro/blob/main/templates/bundles/TwigBundle/Exception/error.html.twig)


## What it doesn't ship? ❌

* The debug toolbar
* Doctrine


## Installation & first run 🚀

    composer install

Start the web server:

    make start

Or with [Castor](https://github.com/jolicode/castor):

    castor symfony:start


Then open [https://127.0.0.1:8000](https://127.0.0.1:8000)

The port can change if `8000` is already used.


## Tests ✅

Run tests with:

    vendor/bin/simple-phpunit

Using composer:

    composer app-test

Using the Makefile:

    make test

Using the [Castor](https://github.com/jolicode/castor):

    castor test:all

Make your choice! ✅ 


## Code coverage ♻️

The code coverage is at 100% and is analysed with a simple script 
(thanks [Ocramius](https://ocramius.github.io/blog/automated-code-coverage-check-for-github-pull-requests-with-travis/)).

For instance, in the following build, the code coverage analysis fails because the
code coverage is 95.35% is the below the wanted threshold of 100%.

    https://github.com/strangebuzz/MicroSymfony/actions/runs/5220428064/jobs/9423476258

The default threshold is 100%, you can change it in the [GitHub actions file](.github/workflows/symfony.yml). 


## Dev-tools ✨
 
* php-cs-fixer with the [Symfony ruleset and PHP strict types](https://github.com/strangebuzz/MicroSymfony/blob/main/.php-cs-fixer.dist.php)
* PHPStan at [maximum level](https://github.com/strangebuzz/MicroSymfony/blob/main/phpstan.neon)
* [Castor task runner](https://github.com/strangebuzz/MicroSymfony/blob/main/castor.php)
* A simple [Makefile](https://github.com/strangebuzz/MicroSymfony/blob/main/Makefile)


## References 📚

* https://developer.mozilla.org/en-US/docs/Web/HTML/Element/script/type/importmap
* https://symfony.com/blog/new-in-symfony-6-3-assetmapper-component
* https://github.com/rails/importmap-rails#expected-errors-from-using-the-es-module-shim
* https://dohliam.github.io/dropin-minimal-css/?bare#text
