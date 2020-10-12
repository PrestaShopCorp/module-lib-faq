# PrestaShop module library for FAQ

This library allows module to retrieve FAQ (Frequently Asked Questions) from PrestaShop APIs.

## Installation

```
composer require prestashop/module-lib-faq
```

## Usage

* Common case

    The simplest way to use this library is:

    ```php
    use PrestaShop\ModuleLibFaq\Faq;

    // [...]

    $faq = new Faq('your module key', _PS_VERSION, 'the current iso code');
    $faqContent = $faq->getFaq();
    ```

* With additional code to run in case of error

    ```php
    use PrestaShop\ModuleLibFaq\Faq;

    // [...]

    $faq = new Faq('your module key', _PS_VERSION, 'the current iso code');
    $faq->setErrorCallable(function(\Exception $e) { /* send to logger */ });
    $faqContent = $faq->getFaq();
    ```

