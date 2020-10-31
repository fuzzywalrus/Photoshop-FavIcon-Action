# Favicon Creator Action for the Obsessive

FavIcons today are plentiful, ranging a variety of sizes, however wrangling them all in is a pain. This project includes a simple Photoshop action, sketch file with predefined exports, and macOS Automator script that creates 14 favicon sizes based on the current standards. 

I highly recommend (albeit dated) [favicon cheat sheet](https://github.com/audreyr/favicon-cheat-sheet) and [Apple's Configuring Web Applications](https://developer.apple.com/library/content/documentation/AppleApplications/Reference/SafariWebContent/ConfiguringWebApplications/ConfiguringWebApplications.html) and [The Web App Manifest](https://developers.google.com/web/fundamentals/web-app-manifest/) for more information.

# Photoshop Favicon Creator for the Obsessive.

## Installing the action

In Photoshop (under actions), click the menu and locate "Load Action," this will bring up the OS dialog box. Locate the Favicon Creator.

## Using the action

The default image must be square and above 228 x 228 pixels (I recommend personally recommend using higher than this). Click play, and the action will create 13 icon sizes in PNG.


# Sketch Export for the Obsessive

Open the sketch, and replace the content with your content. 

## Using the export
 The predefined exports will appear in the export panel.  


#### Optional but recommended: Optimization

Unoptimized PNGs from Photoshop tend to be quite large. I highly recommend for macOS users the free application [ImageOptim](https://imageoptim.com/mac) for lossless PNG compression. It's brainlessly easy. Drag and drop all the newly created PNGs to shave off valuable KBs off images without any quality hit.

For the more obsessive, macOS users, [ImageAlpha](https://pngmini.com/) (works in tandem with ImageOptim) allows users to use indexed color profiles even further to reduce file sizes. [PNGquant](https://pngquant.org/) works natively from Photoshop, and [TinyPNG](https://tinypng.com/) provides free service usable from your web browser. Lastly, [ImageSquash](https://www.realmacsoftware.com/squash/) by RealMac offers a commercial alternative. See [favicon cheat sheet](https://github.com/audreyr/favicon-cheat-sheet) for CLI utilities.


## Required HTML


To use these icons, you will want to include in the `<head></head>` of your HTML file the appropriate linking.


```html
<!-- generics -->
<link rel="icon" href="/path/to/favicon-32.png" sizes="32x32">
<link rel="icon" href="/path/to/favicon-128.png" sizes="128x128">
<link rel="icon" href="/path/to/favicon-192.png" sizes="192x192">

<!-- Android -->
<link rel="shortcut icon" href="/path/to/favicon-196.png" sizes="196x196">

<!-- iOS -->
<link rel="apple-touch-icon" href="/path/to/favicon-152.png" sizes="152x152">
<link rel="apple-touch-icon" href="/path/to/favicon-167.png" sizes="167x167">
<link rel="apple-touch-icon" href="/path/to/favicon-180.png" sizes="180x180">
```

## Included Icons


Size | Name | Purpose
---- | ---- | -------
32x32  | favicon-32.png | Certain old but not too old Chrome versions mishandle ico
120x120 | favicon-120.png | iPhone retina touch icon (Change for iOS 7: up from 114x114) - deprecated
128x128 | favicon-128.png | Chrome Web Store icon
128x128 | smalltile.png  | Small Windows 8 Star Screen Icon
152x152 | favicon-152.png | iPad touch icon (Change for iOS 7: up from 144x144)
167x167 | favicon-167.png | iPad Retina touch icon (change for iOS 10: up from 152x152)**
180x180 | favicon-180.png | iPhone 6 plus
192x192 | favicon-192.png | Google Developer Web App Manifest Recommendation for Chrome
196x196 | favicon-196.png | Chrome for Android home screen icon
270x270 | mediumtile.png |  Medium Windows 8 Start Screen Icon *
558x270 | widetile.png  |  Wide Windows 8 Start Screen Icon *
558x558 | largetile.png  |  Large Windows 8 Start Screen Icon *


Deprecated 

Size | Name | Purpose
---- | ---- | -------
57x57  | favicon-57.png | Standard iOS home screen (iPod Touch, iPhone first generation to 3G) - deprecated *
76x76  | favicon-76.png | iPad home screen icon - deprecated *
96x96  | favicon-96.png | GoogleTV icon - deprecated *
114x114 | favicon-114.png | iOS7 Retina - deprecated *
144x144 | favicon-144.png | IE10 Metro tile for pinned sites - iPad pre-iOS 10 - deprecated *
195x195 | favicon-195.png | Opera Speed Dial icon (Not working in Opera 15 and later) - deprecated *
228x228 | favicon-228.png | Opera Coast icon - depreicated *

* *Denotes not included in this action
* **Denotes not included in this action but planned in the future. iOS will fallback to the 152x152

## Further notes

For IE 10 and older browsers, you will still need to create a favicon.ico if you elect to include a favicon.ico, currently, Safari will default to the favicon.ico over the PNG. I highly recommend the following [How to Create Retina-Caliber Favicons](https://daringfireball.net/2013/01/retina_favicons) to preserve retina icons for Safari.

Google also has declarations in a manifest.json file, [Web App Manifest](https://developers.google.com/web/fundamentals/web-app-manifest/).

### Don't forget OpenGraph images & Twitter Card images

Favicons are only part of the preview game for your website, be sure to include Twitter Card and Facebook OpenGraph data for much more social media-friendly sharing of your website/web app. Apple's Messages, Slack, and other popular communication applications use these for Rich Media Previews. For both Twitter:card and OG tags to work, they both require more than just the images. Image requirements are linked below.

[Facebook Best Practices for Images practices](https://developers.facebook.com/docs/sharing/best-practices#images)

[Twitter Summary Card with Large Image](https://dev.twitter.com/cards/types/summary-large-image)

[How to add iMessage Rich Video Previews to your website](https://www.emergeinteractive.com/insights/detail/rich-video-previews-in-ios-macos-messages)
