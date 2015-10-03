![goodshare.js logo github](http://goodshare.ru/assets/images/goodshare-logo-github.jpg)

> Внимание! Документацию, примеры использования и рекомендации по установке на **русском языке**&nbsp;— вы можете найти на [официальном сайте](http://goodshare.ru/).

# goodshare.js

Useful jQuery plugin that will help your website visitors share a link on social networks and microblogs. Easy to install and configuring on any of your website!

### Features
Simple install, can work through СDN, extensive documentation, developer support, **SEO friendly**, many options for customization of appearance, **clean code without scripts tracking user activity** on the page, **high speed**.

#### Changes

At ver. ``3.0`` we added [share counters](https://github.com/enjoyiacm/goodshare.js#counters) for most popular social networks and reorganize code.

At ver. ``3.1.7`` we added an external function ``getCount()`` that updates counter from any place of your script. This can be useful if you create share buttons when the DOM is fully loaded. [Small demo can be found on JSFiddle](https://jsfiddle.net/730xnkzr/#run).

### Demo
If you're looking for a simple basic demo, it's [here](http://goodshare.ru/examples.html).

## Install

Download [goodshare.js](https://github.com/enjoyiacm/goodshare.js/archive/master.zip) from GitHub. Place plugin file to your project folder: ``./path/to/your/project/folder/js/goodshare.min.js``.

Add to your project template (or something else):

```javascript
<!-- jQuery 1.11.2 minify version from Google CDN JS -->
<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.3/jquery.min.js"></script>

<!-- goodshare.js minify version -->
<script src="../path/to/your/project/folder/js/goodshare.min.js"></script>
```
If you want place plugin via fast CDN (special thanks to [jsDelivr](http://www.jsdelivr.com) project and [this issue](https://github.com/enjoyiacm/goodshare.js/issues/2)), use this:

```javascript
<!-- Latest 3.1.x goodshare.js minify version from jsDelivr CDN -->
<script src="https://cdn.jsdelivr.net/jquery.goodshare.js/3.1.7/goodshare.min.js"></script>
```

For more speed and profit, use «all in one» solution from [jsDelivr](http://www.jsdelivr.com) CDN:

```javascript
<!-- jQuery 1.11.3 minify version and latest 3.1.x goodshare.js minify version from jsDelivr CDN -->
<script src="https://cdn.jsdelivr.net/g/jquery@1.11.3,jquery.goodshare.js@3.1.7"></script>
```

## List of supported social networks and microblogs

* `vk` [Вконтакте](http://vk.com)
* `fb` [Facebook](http://facebook.com)
* `ok` [Одноклассники](http://ok.ru)
* `mr` [Мой Мир@Mail.Ru](http://my.mail.ru)
* `gp` [Google Plus](http://plus.google.com)
* `li` [LinkedIn](http://linkedin.com)
* `tw` [Twitter](http://twitter.com)
* `lj` [LiveJournal](http://livejournal.com)
* `tm` [tumblr](http://tumblr.com)
* `bl` [Blogger](http://blogger.com)
* `pt` [Pinterest](http://pinterest.com)
* `di` [Digg](http://digg.com)
* `en` [Evernote](http://evernote.com)
* `rd` [Reddit](http://reddit.com)
* `su` [StumbleUpon](http://www.stumbleupon.com)
* `po` [Pocket](https://getpocket.com)
* `sb` [Surfingbird](http://surfingbird.ru)
* `bf` [Buffer](http://buffer.com)
* `ra` [Readability](http://www.readability.com)

If you don't see your social network, please [let us know](https://github.com/enjoyiacm/goodshare.js#developer) and we'll try to add it!

## Description

Plugin works with any HTML tags: `<a>` or `<div>` or `<button>` or other. So you can choose any and add required attributes: class `goodshare` and `data-type`. For example:

```html
<!-- Create button with share to Twitter -->
<button class="goodshare" data-type="tw">Share this to Twitter</button>

<!-- Create link with share to Facebook -->
<a href="#" class="goodshare" data-type="fb">Share this to Facebook</a>

<!-- Create div container with share to LinkedIn -->
<div class="goodshare" data-type="li">Share this to LinkedIn</div>

<!-- Create icon from Fontello.com with share to Google+ -->
<i class="goodshare icon-google-plus" data-type="gp"></i>
```

### List of attributes

You can change these attributes as needed for your project:
<table>
<thead>
<tr>
<th>Attribute</th>
<th>Description (default: value)</th>
</tr>
</thead>
<tbody>
<tr>
<td>data-type</td>
<td>[required] Type (name) of social network (default: "vk")</td>
</tr>
<tr>
<td>data-url</td>
<td>(optional) Current page URL (default: browser adress field)</td>
</tr>
<tr>
<td>data-title</td>
<td>(optional) Current page title (default: head title)</td>
</tr>
<tr>
<td>data-text</td>
<td>(optional) Current page description text (default: meta property="og:description")</td>
</tr>
<tr>
<td>data-image</td>
<td>(optional) Current page image URL (default: meta property="og:image")</td>
</tr>
</tbody>
</table>

### Note for `<a>` links

We use `event.preventDefault()` for event "click". So don't be afraid to use links like this:
```html
<a href="#">My link</a>
```
## Counters

To display counter, just add ``data-counter`` attribute to HTML element that will contain numbers. For example:

```html
<!-- Create link with share to Facebook and counter -->
<a href="#" class="goodshare" data-type="fb">
  Share this to Facebook
  <span data-counter="fb"></span>
</a>
```

**Note:** You may put this attribute to any element, even that hasn't class ``goodshare``. For example:

```html
<!-- Create link with share to Facebook -->
<a href="#" class="goodshare" data-type="fb">Share this to Facebook</a>
...
...
<!-- Create external Facebook share counter -->
<div>
  <div>All Facebook shares:</div>
  <div data-counter="fb"></div>
</div>
```

Value of ``data-counter`` attribute, see in this list of supported social networks and microblogs:

* `vk` [Вконтакте](http://vk.com)
* `fb` [Facebook](http://facebook.com)
* `ok` [Одноклассники](http://ok.ru)
* `mr` [Мой Мир@Mail.Ru](http://my.mail.ru)
* `gp` [Google Plus](http://plus.google.ru)
* `li` [LinkedIn](http://linkedin.com)
* `tw` [Twitter](http://twitter.com)
* `tm` [tumblr](http://tumblr.com)
* `pt` [Pinterest](http://pinterest.com)
* `rd` [Reddit](http://reddit.com)
* `su` [StumbleUpon](http://www.stumbleupon.com)
* `po` [Pocket](https://getpocket.com)
* `sb` [Surfingbird](http://surfingbird.ru)
* `bf` [Buffer](http://buffer.com)

**Note:** ``StumbleUpon`` and ``Pocket`` counters use [Yahoo Query Language](https://developer.yahoo.com/yql) (YQL). It may impose some restrictions on use, associated with limit queries to Yahoo (we try to find another solution for this, if you know — [write issue to us](https://github.com/enjoyiacm/goodshare.js/issues/new)).

**Note:** ``Surfingbird`` counter use [Any Origin](http://anyorigin.com/). It may impose some restrictions on use requests to their server (we try to find another solution for this, if you know — [write issue to us](https://github.com/enjoyiacm/goodshare.js/issues/new)).

## Usage example

This example shows one of decoration options with all supported social networks.

![goodshare.js usage example github](http://goodshare.ru/assets/images/goodshare-usage-example-github-ver2.jpg)

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <title>My page with goodshare.js</title>
    <style>
	  html, body {font-family: Arial, Helvetica, sans-serif; font-size: 16px; line-height: 24px; text-align: center;}
      a {color: #ffffff; display: inline-block; width: 150px; padding: 10px; margin: 2px auto; cursor: pointer;}
      a[data-type="vk"] {background: #45668e;}
      a[data-type="fb"] {background: #3b5998;}
      a[data-type="ok"] {background: #ed812b;}
      a[data-type="mr"] {background: #168de2;}
      a[data-type="gp"] {background: #dd4b39;}
      a[data-type="li"] {background: #0976b4;}
      a[data-type="tw"] {background: #55acee;}
      a[data-type="lj"] {background: #004359;}
      a[data-type="tm"] {background: #35465c;}
      a[data-type="bl"] {background: #f57d00;}
      a[data-type="pt"] {background: #cc2127;}
      a[data-type="di"] {background: #000000;}
      a[data-type="en"] {background: #7ac142;}
      a[data-type="rd"] {background: #5f99cf;}
      a[data-type="su"] {background: #eb4924;}
      a[data-type="po"] {background: #d3505a;}
      a[data-type="sb"] {background: #26B1F6;}
      a[data-type="bf"] {background: #323b43;}
      a[data-type="ra"] {background: #990000;}
    </style>
  </head>
  <body>
    <h1>My page with goodshare.js</h1>
    <p>Useful jQuery plugin that will help your website visitors share a link on social networks and microblogs.<br />
    Easy to install and configuring on any of your website!</p>
    <div>
      <a href="#" class="goodshare" data-type="vk">Вконтакте <span data-counter="vk"></span></a> 
      <a href="#" class="goodshare" data-type="fb">Facebook <span data-counter="fb"></span></a> 
      <a href="#" class="goodshare" data-type="ok">Одноклассники <span data-counter="ok"></span></a> 
      <a href="#" class="goodshare" data-type="mr">Мой Мир@Mail.Ru <span data-counter="mr"></span></a> 
      <a href="#" class="goodshare" data-type="gp">Google Plus <span data-counter="gp"></span></a> 
      <a href="#" class="goodshare" data-type="li">LinkedIn <span data-counter="li"></span></a> 
      <a href="#" class="goodshare" data-type="tw">Twitter <span data-counter="tw"></span></a> 
      <a href="#" class="goodshare" data-type="lj">LiveJournal</a> 
      <a href="#" class="goodshare" data-type="tm">tumblr <span data-counter="tm"></span></a> 
      <a href="#" class="goodshare" data-type="bl">Blogger</a> 
      <a href="#" class="goodshare" data-type="pt">Pinterest <span data-counter="pt"></span></a> 
      <a href="#" class="goodshare" data-type="di">Digg</a> 
      <a href="#" class="goodshare" data-type="en">Evernote</a> 
      <a href="#" class="goodshare" data-type="rd">Reddit <span data-counter="rd"></span></a>
      <a href="#" class="goodshare" data-type="su">StumbleUpon <span data-counter="su"></span></a>
      <a href="#" class="goodshare" data-type="po">Pocket <span data-counter="po"></span></a>
      <a href="#" class="goodshare" data-type="sb">Surfingbird <span data-counter="sb"></span></a>
      <a href="#" class="goodshare" data-type="bf">Buffer <span data-counter="bf"></span></a>
      <a href="#" class="goodshare" data-type="ra">Readability</a>
    </div>
    <p>See goodshare.js on GitHub: <a href="https://github.com/enjoyiacm/goodshare.js" target="_blank">https://github.com/enjoyiacm/goodshare.js</a></p>.
    <!-- jQuery 1.11.3 minify version and latest 3.1.x goodshare.js minify version from jsDelivr CDN -->
    <script src="https://cdn.jsdelivr.net/g/jquery@1.11.3,jquery.goodshare.js@3.1.7"></script>
  </body>
</html>
```

## Developer

Development and maintenance of `goodshare.js` project engaged in [Interactive agency «Central marketing»](http://centralmarketing.ru). If you want to write a «thank you» or ask us about something, [use this e-mail](mailto:support@goodshare.ru).

## Your help

If you want help, we will be glad reviews about `goodshare.js` on personal blogs (including Twitter), online media or specialized IT-portals. Thank you!

## License

[The MIT License (MIT)](https://github.com/enjoyiacm/goodshare.js/blob/master/LICENSE)
