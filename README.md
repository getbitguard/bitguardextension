# Bitguard Browser Extention

Bitguard Browser Extention is a free extension that blocks ads and malicious domains known to spread malware, disables tracking. We have included a few extensive filters that offer decent protection against annoying, flashy ads, YouTube commercials, and more. Unlike other adblockers we do not have a whitelist for websites, advertisers or ad networks to show you unwanted ads. Blocking ads will speed up your website load speed, decrease CPU and memory usage.

The extension allows you to switch back on ads for your favorite websites in case you know there are no intrusive and/or misleading advertising there.

## Features

- Remove all ads
- Block malware and tracking
- Improve browser performance
- No "acceptable" ads or whitelisted websites/ad networks

## Why another AdBlocker though?

Bitguard was created with the sole purpose to block ALL ads. Many adblockers are affiliated with ad networks bypassing ads for a fee. We couldn't find an adblocker blocking everything, so we just decided to make our own, filtering every ad without exceptions.

Also Bitguard Extention integrates link to "Bitguard Scan" our security risk score product.

## Contribution

**Found an issue?**

Post in the Issue section of this repository or contact us on our [website](https://www.getbitguard.com/support)

**Translation**

Help us translate the extension to your language [here](https://www.getbitguard.com/support)

## Contact us

You can drop us a line at hello@getbitguard.com.

## License

Free. Bitguard browser extention is an open source project licensed under GPL v3. The first version was forked from AdGuard v 3.5.31 on 24 December 2020 inheriting the GPL v3 license for open source.

**Changes made to the source code**

- Fully re-design to improved user experience and simplified design.
- Modified the default performance.
- Access to "Bitguard Scan" in one click.
- Translation corrections.


<a id="dev"></a>
## Development

<a id="dev-requirements"></a>
### Requirements

- [nodejs](https://nodejs.org/en/download/)
- [yarn](https://yarnpkg.com/en/docs/install/)

Install local dependencies by running:
```
  yarn install
```

<a id="dev-build"></a>
### How to build

**How to run tests**
```
  yarn test
```

**Building the dev version**

Run the following command:
```
  yarn dev
```

This will create a build directory with unpacked extensions for all browsers:
```
  build/dev/chrome
  build/dev/firefox
  build/dev/edge
```

**Building the beta and release versions**

Before building the release version, you should manually download necessary resources: filters and public suffix list.

```
  yarn resources
```

```
  CREDENTIALS_PASSWORD=<password> yarn beta
  CREDENTIALS_PASSWORD=<password> yarn release
```
You will need to put certificate.pem and mozilla_credentials.json files to the `./private` directory. This build will create unpacked extensions and then pack them (crx for Chrome, xpi for Firefox).


<a id="dev-linter"></a>
### Linter
Despite our code my not currently comply with new style configuration,
please, setup `eslint` in your editor to follow up with it `.eslintrc`

<a id="dev-localizations"></a>
### Update localizations

To download and append localizations run:
```
  yarn locales-download
```

To upload new phrases to crowdin you need the file with phrases `./Extension/_locales/en/messages.json`. Then run:
```
  yarn locales-upload
```
## Minimum supported browser versions
| Browser                 	| Version 	|
|-------------------------	|:-------:	|
| Chromium Based Browsers 	|    55   	|
| Firefox                 	|    52   	|
| Opera                   	|    42   	|
| Edge                    	|    15.14942/39.14942   	|
