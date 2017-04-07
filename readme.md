# mt-theme


## Installation

```
composer require intmedia/mt-theme
```

Optional:

```
composer require frontpack/less
composer require frontpack/composer-assets-plugin
```

## Components

``` less
@import 'assets/typro/typro/base/base';
@import 'assets/typro/typro/mixins/fonts';
@import 'assets/intmedia/mt-theme/components/page';
@import 'assets/intmedia/mt-theme/components/header';
@import 'assets/intmedia/mt-theme/components/footer';
@import 'assets/intmedia/mt-theme/components/content';
@import 'assets/intmedia/mt-theme/components/logo';
@import 'assets/intmedia/mt-theme/components/navigation';
@import 'assets/intmedia/mt-theme/components/button';
@import 'assets/intmedia/mt-theme/components/text';
@import 'assets/intmedia/mt-theme/components/video';
```

### layout/page

``` html
<div class="wrapper">
...
</div>
```

* `@mt-page-max-width: 70em;`
* `@mt-page-border-radius: 3px;`


### header

``` html
<div class="header">
	<div class="header__inner">
		<div class="header__block">
			<!-- logo -->
			<!-- navigation -->
		</div>
	</div>
</div>
```

* `@mt-header-background: #f8f8f8;`
* `@mt-header-border-bottom: 1px solid #eee;`
* `@mt-header-max-width: @mt-page-max-width;`


### content

``` html
<div class="content">
	<div class="content__inner">
		<div class="content__block">
			<!-- content -->
		</div>
	</div>
</div>
```

* `@mt-content-max-width: @mt-page-max-width;`
* `@mt-content-background: transparent;`


### footer

``` html
<div class="footer">
	<div class="footer__inner">
		<div class="footer__block">
			&copy; footer
		</div>
	</div>
</div>
```

* `@mt-footer-max-width: @mt-page-max-width;`
* `@mt-footer-background: transparent;`
* `@mt-footer-border-top: 1px solid #e8e8e8;`
* `@mt-footer-color: gray;`
* `@mt-footer-margin-top: 1em;`


### logo

``` html
<div class="logo">
	<div class="logo__inner">
		<a href="#" rel="home" class="logo__name">Site Name</a>
		<span class="logo__motto">Site motto</span>
	</div>
</div>
```

* `@mt-logo-name-color: #000;`
* `@mt-logo-name-font-size: 150%;`
* `@mt-logo-motto-color: gray;`

* `.logo--on-left`
* `.logo--inlined`
* `.logo--centered`


### navigation

``` html
<div class="navigation">
	<div class="navigation__inner">
		<a href="#" class="navigation__item navigation__item--active">Homepage</a>
		<a href="#" class="navigation__item">Články</a>
		<a href="#" class="navigation__item">O webu</a>
	</div>
</div>
```

* `@mt-navigation-item-color: #000;`
* `@mt-navigation-item-border-radius: @mt-page-border-radius;`
* `@mt-navigation-active-item-color: #000;`
* `@mt-navigation-active-item-background: #fff;`
* `@mt-navigation-active-item-border-color: #ddd;`

* `.navigation--centered`
* `.navigation--on-right`


### button

``` html
<a href="#" class="button">Koupit</a>
```

* `@mt-button-border-radius: @mt-page-border-radius;`
* `@mt-button-color: #fff;`
* `@mt-button-background-color: #0d79a7;`
* `@mt-button-border-color: @mt-button-background-color;`
* `@mt-button-inline-color: darken(@mt-button-background-color, 10%);`
* `@mt-button-inline-background-color: transparent;`

* `.button--bordered`


### text

``` html
<div class="text">
	<div class="text__image">
		<img src="photo.img" alt="">
	</div>
	<h1 class="text__header">Lorem ipsum dolor sit</h1>
	<p class="text__perex">Lorem ipsum dolo rsit</p>
	<div class="text__content">
		<p>Lorem ipsum</p>
	</div>
</div>
```

* `@mt-text-max-width: 54em;`
* `@mt-text-perex-color: #666;`


### video

``` html
<div class="video">
	<div class="video__container">
		<a href="http://youtube.com/..." class="video__placeholder">
			<span class="video__description">Lorem ipsum dolor sit amete</span>
			<div class="video__image">
				<img src="thumbnail.jpg" alt="">
			</div>
		</a>
	</div>
</div>

<div class="video">
	<div class="video__container">
		<iframe width="560" height="315" src="https://www.youtube.com/embed/kiRdxavlrCk" frameborder="0" allowfullscreen></iframe>
	</div>
</div>
```

V této podobě se zobrazí na celou šířku

* `.video--w640` - omezí velikost videa/placeholderu na `640px`
* `.video--centered` - vystředí video na střed; v kombinaci s `.video--w640` omezí velikost kontejneru
