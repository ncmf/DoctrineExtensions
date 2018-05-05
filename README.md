# DoctrineExtensions
Быстрая установка и настройка gedmo/doctrine-extensions со всеми плюшками

## Установка

* `composer require ncmf/doctrine-extensions:dev-master`
* `composer dump-autoload --optimize`
* Прописать в config.yml

        imports:
            ... 
            - { resource: "@NCMFDoctrineExtensionsBundle/Resources/config/config.yml" }
* Register bundle in kernel: app/AppKernel.php

        ...
        class AppKernel extends Kernel
        {
            ...
            public function registerBundles()
            {
                $bundles = [
                    ...
                    new \NCMF\DoctrineExtensionsBundle\NCMFDoctrineExtensionsBundle(),
                ];
* `php bin/console cache:clear`