# Livewire-Maps

Basic Google Maps-implementation for Laravel-Livewire currently supporting:
- Map-Markers ([view docs](./docs/MapMarkers.md))
- Map-Move-Listeners ([view docs](./docs/MapMoveListener.md))

## Installation

You can install the package via composer:

```bash
composer require esadewater/livewire-maps
```

You can publish the assets with:

```bash
php artisan vendor:publish --tag="livewire-maps-assets"
```

Alternatively you can include the JavaScript resources in your app.js:

```javascript
const {init} = require("../../vendor/esadewater/livewire-maps/resources/js/LiveWireMaps");
init();
```

You can publish the config file with:

```bash
php artisan vendor:publish --tag="livewire-maps-config"
```

Optionally, you can publish the views using

```bash
php artisan vendor:publish --tag="livewire-maps-views"
```

## Usage

Get an API-key for the Google Maps Platform from [here](https://console.cloud.google.com/google/maps-apis/start) and add it to your .env-file:

```dotenv
GOOGLE_MAPS_API_KEY=YOUR_KEY_GOES_HERE
```

Add the following directive right after @livewireScripts:

```php
@livewireMapsScripts
```

Then you are ready to start with a basic map with a center point and a zoom:

```php
<livewire:map-view center-lat="52.004021" center-lng="7.710472" zoom="3" style="100vh" />
```

## Testing

```bash
composer test
```

## Credits

- [Erik Sadewater](https://github.com/esadewater)

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.
