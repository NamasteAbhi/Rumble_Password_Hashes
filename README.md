# Rumble Password Hash Generator (JavaScript)

This repository contains a JavaScript code snippet that mimics the password hashing mechanism used by [Rumble](https://rumble.com/). The implementation allows you to generate password hashes with specific salts, similar to how Rumble does during user authentication.

## Features

- Uses a custom MD5 hashing implementation (`MD5Ex`).
- Supports iterative hash stretching to enhance security.
- Generates password hashes that follow the same logic used on the Rumble website.

## Usage

```
// Sample salts and password
const salts = ['CzqdrIEq', '25kpbuhq0', 'i3OoGUE0']; // These Salt Comes From Response https://rumble.com/service.php?name=user.get_salts&included_js_libs=main,web_services,events,error,facebook_events,htmx.org,navigation-state,darkmode,ui,featured-pills,notify,playlist-menu,modal-base,ui_header,main-menu-item-hover,search-bar,premium-popup,event_handler,ui_overlay,md5,validate,facebook,google,apple,login_form&included_css_libs=ui_overlay,form,service.user,global
const password = '12345678';
console.log('password_hashes:', EncryptPassword(password,salts).join(','));
```
