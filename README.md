<h1 align="center"> Table Reservation - Wordpress Plugin </h1> <br>
<p align="center">
  <a href="http://true-emotions.studio/">
    <img alt="Table Reservation" title="Table Reservation" src="http://true-emotions.studio/wp-content/uploads/2018/01/icon-256x256.jpg" width="250">
  </a>
</p>

<p align="center">
  The Revolution in Table Reservation.
</p>

<p align="center">
  <a href="http://true-emotions.studio/">
    <img alt="True Emotions Studio" title="We are" src="http://true-emotions.studio/wp-content/uploads/2018/01/logo2.jpg" width="105">
  </a>
  
  <a href="https://join.slack.com/t/table-reservation/shared_invite/enQtMzAxMjUwMjk5ODYwLTFkYWEzYjBhODAwNmY3NTcyY2M4NWYxZmMzNTAwMWZhYmZhZWM3Nzc4NThkYzU1NDkzMjk0ZWRmYzY2ODcyYmI">
    <img alt="Chat" title="Chat" src="http://true-emotions.studio/wp-content/uploads/2018/01/slack-e1516318903115.png" width="150">
  </a>

  <a href="https://trello.com/b/BdGT06ts">
    <img alt="Road map" title="Road map" src="http://true-emotions.studio/wp-content/uploads/2018/01/logo-blue-lg-300x95.png" width="150">
  </a>
</p>

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
## Table of Contents


- [Demo](http://true-emotions.studio/sample-page/)
- [Introduction](#introduction)
- [Features](#features)
- [Feedback](#feedback)
- [Contributors](#contributors)
- [Build Process](#build-process)
- [Sponsors](#sponsors-)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## Introduction

This plugin allows users quickly book a table in your cafe or make a restaurant reservation. Undoubtedly, its simplicity and beauty will increase the attendance of your place. Built with Vue and Wordpress is the most feature-rich WP Table Reservation Plugin that is 100% free.

<p align="center">
  <img src = "http://true-emotions.studio/wp-content/uploads/2018/01/screenshot-1.gif" width=1000>
</p>

## Features

A few of the things you can do with Table Reservation:

* Selectable tables for reservations
* THERE ARE NO COLLISIONS, i.e. one table can't be reserved by different people simultaneously.
* Comfortably add, edit, delete or reject reservations from Wordpress dashboard
* Email notifications about reservation (both for admin and guest)
* Customisable colors, date/time format and all notification mails about reservation
* Each field of reservation form is easily translatable into the required language
* Well-thought-out mobile usability in the field
* WPBakery(Visual Composer) compatible

<p align="center">
  <img src = "http://true-emotions.studio/wp-content/uploads/2018/01/banner-1544x500.gif" width=1000>
</p>

## Feedback

Feel free to [file an issue](https://github.com/vanadiuz/table-reservation/issues/new). Feature requests are always welcome.

If there's anything you'd like to chat about, please feel free to join our [Slack chat](https://join.slack.com/t/table-reservation/shared_invite/enQtMzAxMjUwMjk5ODYwLTFkYWEzYjBhODAwNmY3NTcyY2M4NWYxZmMzNTAwMWZhYmZhZWM3Nzc4NThkYzU1NDkzMjk0ZWRmYzY2ODcyYmI)!

## Contributors

This project follows the [all-contributors](https://github.com/kentcdodds/all-contributors) specification and is brought to you by these [awesome contributors](./CONTRIBUTORS.md).

## Build Process

- Clone or download the repo
- Put it in wp-content/plugins/ (preferably on a locally deployed server with wordpress)
- Go to table-reservation/tremtr (here is front-end web app on Vue js)
- `npm install` to install dependencies 
- `npm run dev` to start develope app
- Activate plugin inside WordPress and [create a new table](http://data.true-emotions.studio/plugins/trem-table-reservation/table-reservation.mp4 "Video!")
- Now you can modify the Vue Js code and immediately watch how it will work in Wordpress

**Build Production Version of Plugin**
- `npm run build` to build front-end part of plugin
- Copy JS files from ./tremtr/dist/static/js to ./assets/js
- Open table-reservation.php in plagin's root and commit 
```php
  wp_register_script( 'tremtr-app', 'http://localhost:8080/app.js' , '', '', true );
```
- In the same place uncommit and rename next lines 
```php
            // wp_register_script('tremtr-manifest', TREMTR_PLUGIN_URL . '/assets/js/manifest.6a98d09897ee4023cfac.js', array(), '1.0.0', 'screen, all');
            // wp_register_script('tremtr-vendor', TREMTR_PLUGIN_URL . '/assets/js/vendor.27bdc60e48dd445d7732.js', array(), '1.0.0', 'screen, all');
            // wp_register_script('tremtr-app', TREMTR_PLUGIN_URL . '/assets/js/app.5ba64ddd460771627e94.js', array(), '1.0.0', 'screen, all');
```

## Sponsors

Support this project by becoming a sponsor. Your logo will show up here with a link to your website. [Become a sponsor](http://true-emotions.studio/contact-us/)

## License

GPLv2 or later
