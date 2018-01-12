# Photoshop Favicon Creator Action for the Obsessive

FavIcons today are plentiful, ranging a variety of sizes, however wrangling them all in is a pain. This is a simple Photoshop action that creates 13 favicon sizes based on the current standards. I highly recommend [favicon cheat sheet](https://github.com/audreyr/favicon-cheat-sheet) and [Apple's Configuring Web Applications](https://developer.apple.com/library/content/documentation/AppleApplications/Reference/SafariWebContent/ConfiguringWebApplications/ConfiguringWebApplications.html)  for more information

## Installing the action

In Photoshop (under actions), click the menu and locate "Load Action", this will bring up the OS dialog box. Locate the Favicon Creator.

## Using the action

The default image must be square and above 228 x 228 pixels (I recommend personally recommend using higher than this). Click play and the action will create 13 icon sizes in PNG.

#### Optional but recommended: Optimization

Unoptimized PNGs from Photoshop tend to be quite large. I highly recommend for macOS users the free application [ImageOptim](https://imageoptim.com/mac) for lossless PNG compression. It's brainlessly easy. Drag and drop all the newly created PNGs to shave off valuable KBs off images without any quality hit.

For the more obsessive, macOS users, [ImageAlpha](https://pngmini.com/) (works in tandem with ImageOptim) allows users to use indexed color profiles to even further reduce file sizes. [PNGquant](https://pngquant.org/) works natively from Photoshop and [TinyPNG](https://tinypng.com/) provides free service usable from your web browser. See [favicon cheat sheet](https://github.com/audreyr/favicon-cheat-sheet) for CLI utilities.


## Required HTML


To use these icons, will want to include in the `<head></head>` of your html file the appropriate linking


```html
<!-- generics -->
<link rel="icon" href="/path/to/favicon-32.png" sizes="32x32">
<link rel="icon" href="/path/to/favicon-57.png" sizes="57x57">
<link rel="icon" href="/path/to/favicon-76.png" sizes="76x76">
<link rel="icon" href="/path/to/favicon-96.png" sizes="96x96">
<link rel="icon" href="/path/to/favicon-128.png" sizes="128x128">
<link rel="icon" href="/path/to/favicon-228.png" sizes="228x228">
<!-- Android -->
<link rel="shortcut icon" href="/path/to/favicon-196.png" sizes="196x196">
<!-- iOS -->
<link rel="apple-touch-icon" href="/path/to/favicon-120.png" sizes="120x120">
<link rel="apple-touch-icon"  href="path/to/favicon-152.png" sizes="152x152">
<link rel="apple-touch-icon" href="path/to/favicon-180.png" sizes="180x180">
<!-- windows -->
<meta name="msapplication-TileColor" content="#FFFFFF">
<meta name="msapplication-TileImage" content="/path/to/favicon-144.png">
```

## Included Icons


Size | Name | Purpose
---- | ---- | -------
32x32  | favicon-32.png  | Certain old but not too old Chrome versions mishandle ico
57x57 | favicon-57.png | Standard iOS home screen (iPod Touch, iPhone first generation to 3G)
76x76 | favicon-76.png | iPad home screen icon
96x96 | favicon-96.png | GoogleTV icon
120x120 | favicon-120.png | iPhone retina touch icon (Change for iOS 7: up from 114x114)
128x128 | favicon-128.png | Chrome Web Store icon
128x128 |	smalltile.png | Small Windows 8 Star Screen Icon
144x144 | favicon-144.png | IE10 Metro tile for pinned site
152x152 | favicon-152.png | iPad touch icon (Change for iOS 7: up from 144x144)
167x167 | favicon-167.png | iPad Retina touch icon (change for iOS 10: up from 152x152)**
180x180 | favicon-180.png | iPhone 6 plus
195x195 | favicon-195.png | Opera Speed Dial icon (Not working in Opera 15 and later)
196x196 | favicon-196.png | Chrome for Android home screen icon
228x228 | favicon-228.png | Opera Coast icon
270x270 |	mediumtile.png |	Medium Windows 8 Start Screen Icon *
558x270 |	widetile.png |	Wide Windows 8 Start Screen Icon *
558x558 |	largetile.png |	Large Windows 8 Start Screen Icon *
* *Denotes not included in this action
* **Denotes not included in this action but planned in the future. iOS will fallback to the 152x152

## Further notes

For IE 10 and older browsers you will still need to create a favicon.ico. If you elect to include a favicon.ico, currently safari will defaul to the favicon.ico over the PNG. I highly recommend following [How to Create Retina-Caliber Favicons](https://daringfireball.net/2013/01/retina_favicons) to preserve retina icons for Safari.


### Don't forget OpenGraph images & Twitter Card images

Favicons are only part of the preview game for your website, be sure to include Twitter Card and FaceBook OpenGraph data for much more social media friendly sharing of your website/webapp. For both Twitter:card and og tags to work, they both require more than just the images. Image requirements are linked below.

[FaceBook Best Practices for Images practices](https://developers.facebook.com/docs/sharing/best-practices#images)

[Twitter Summary Card with Large Image](https://dev.twitter.com/cards/types/summary-large-image)
