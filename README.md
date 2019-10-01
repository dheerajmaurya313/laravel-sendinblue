# Sendinblue for Laravel

[![Latest Version on Packagist](https://img.shields.io/packagist/v/damcclean/laravel-sendinblue.svg?style=flat-square)](https://packagist.org/packages/damcclean/laravel-sendinblue)
[![Build Status](https://img.shields.io/travis/damcclean/laravel-sendinblue/master.svg?style=flat-square)](https://travis-ci.org/damcclean/laravel-sendinblue)
[![Total Downloads](https://img.shields.io/packagist/dt/damcclean/laravel-sendinblue.svg?style=flat-square)](https://packagist.org/packages/damcclean/laravel-sendinblue)

This package provides an easy wrapper around the Sendinblue API for Laravel 5 applications. Behind the scenes of this package, we use the [official Sendinblue SDK](https://github.com/sendinblue/APIv3-php-library/tree/master/docs/Api) for PHP.

This package is **not a mail driver**, just a manager for contacts and other Sendinblue things. Think of it like the Sendinblue version of [Spatie's Newsletter](https://github.com/spatie/laravel-newsletter) package. This package is in no way affiliated with Sendinblue.

Here are some of the available methods:

```php
...
use Sendinblue;
...

// Create a contact, with just an email
Sendinblue::createContact('bob@example.com');

// Create a contact, with more information
Sendinblue::createContact('billy@example.com', [
    'FNAME' => 'Billy',
    'LNAME' => 'Smith'
]);

// Delete a contact
Sendinblue::deleteContact('jen@example.com');

// Create a folder
Sendinblue::createFolder('Personal');

// Create a list
// First param is the name, second is the id of the folder
Sendinblue::createList('Blog Mailing List', 7);
```

## Installation

You can install the package via composer:

```bash
composer require damcclean/laravel-sendinblue
```

Then you can publish the configuration file:

```bash
php artisan vendor:publish --provider="Damcclean\Sendinblue\SendinblueServiceProvider"
```

## Usage

After you've installed the package and published the config file, you'll need to add your Sendinblue API Key to your `.env` file:

```bash
SENDINBLUE_APIKEY=...
```

Then you can simply use the Sendinblue stuff, like this:

``` php
use Sendinblue;

Sendinblue::createContact('bob@example.com');
```

### Testing

``` bash
vendor/bin/phpunit
```

### Changelog

Please see [CHANGELOG](CHANGELOG.md) for more information what has changed recently.

## Contributing

Please see [CONTRIBUTING](CONTRIBUTING.md) for details.

### Security

If you discover any security related issues, please email duncan@mcclean.co.uk instead of using the issue tracker.

## Credits

- [Duncan McClean](https://github.com/damcclean)
- [All Contributors](../../contributors)

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.
लारवेल के लिए सेंडिनब्लू
Packagist बिल्ड स्थिति कुल डाउनलोड पर नवीनतम संस्करण

यह पैकेज Laravel 5 अनुप्रयोगों के लिए Sendinblue API के आसपास एक आसान आवरण प्रदान करता है। इस पैकेज के दृश्यों के पीछे, हम PHP के लिए आधिकारिक Sendinblue SDK का उपयोग करते हैं।

यह पैकेज एक मेल ड्राइवर नहीं है, बस संपर्कों और अन्य Sendinblue चीजों के लिए एक प्रबंधक है। इसे Spatie के न्यूज़लैटर पैकेज के Sendinblue संस्करण की तरह समझें। यह पैकेज किसी भी तरह से Sendinblue से संबद्ध नहीं है।

यहाँ उपलब्ध तरीकों में से कुछ हैं:

...
Sendinblue का उपयोग करें;
...

// एक ईमेल बनाएं, सिर्फ एक ईमेल के साथ
Sendinblue :: createContact ('bob@example.com ');

// अधिक जानकारी के साथ, एक संपर्क बनाएँ
Sendinblue :: createContact ('billy@example.com ', [
    'FNAME' => 'बिली',
    'LNAME' => 'स्मिथ'
]);

// एक संपर्क हटाएं
Sendinblue :: deleteContact ('jen@example.com ');

// एक फ़ोल्डर बनाएँ
Sendinblue :: createFolder ('व्यक्तिगत');

// एक सूची बनाएं
// पहला परम नाम है, दूसरा फ़ोल्डर की आईडी है
Sendinblue :: createList ('ब्लॉग मेलिंग सूची', 7);
स्थापना
आप संगीतकार के माध्यम से पैकेज स्थापित कर सकते हैं:

कंपोजर को डैमेलियन / लार्वेल-सेंडिनब्लू की आवश्यकता होती है
फिर आप कॉन्फ़िगरेशन फ़ाइल प्रकाशित कर सकते हैं:

php कारीगर विक्रेता: प्रकाशित --provider = "डैमक्लेन \ Sendinblue \ SendinblueServiceProvider"
प्रयोग
पैकेज स्थापित करने और कॉन्फिगर फ़ाइल प्रकाशित करने के बाद, आपको अपनी Sendinblue API कुंजी को अपने .env फ़ाइल में जोड़ना होगा:

SENDINBLUE_APIKEY = ...
तो आप बस Sendinblue सामान का उपयोग कर सकते हैं, जैसे:

Sendinblue का उपयोग करें;

Sendinblue :: createContact ('bob@example.com ');
परीक्षण
विक्रेता / बिन / phpunit
बदलाव का
कृपया अधिक जानकारी के लिए CHANGELOG देखें जो हाल ही में बदल गया है।

योगदान
कृपया विवरण के लिए अनुबंध देखें।

सुरक्षा
यदि आपको सुरक्षा संबंधी कोई समस्या है, तो कृपया मुद्दे ट्रैकर का उपयोग करने के बजाय duncan@mcclean.co.uk पर ईमेल करें।

क्रेडिट
डंकन मैक्लेन
सभी योगदानकर्ता
लाइसेंस
MIT लाइसेंस (MIT)। अधिक जानकारी के लिए कृपया लाइसेंस फ़ाइल देखें।
