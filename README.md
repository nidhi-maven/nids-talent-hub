Bootstrap Scrollspy Directive for Angular.js
===========================

This is a replacement for Bootstrap Scrollspy in Angular.js because if you drop in default Bootstrap Scrollspy, it may act up due to refresh/render timing. Also I don't see anything available on the internet as of today as a good replacement. I wrote mine really quick and it is somewhat of a "hack" still. But it works for general use cases.

## Known Limitations

- I only coded for "vertical" scrolling.
- The default spying parent is basically $window. I just don't have a need for spying on a DIV scrolling.
- There is a small hack to do a $watch on $rootScope for DOM change. This allows any controllers to trigger refresh of the spy directive.
 
## Usage

See [Bootstrap Scrollspy Documentation] (http://getbootstrap.com/javascript/#scrollspy) for more information

Put this in the `<body>`:

```javascript
<body data-target='#yourUlElement' scroll-spy=''>
```

Then make sure to add the `id` into `href` attribute of the `nav` item like below:

```javascript
<ul id='yourUlElement'>
  <li>
    <a href="#yourSectionId">
      Chinese
    </a>
  </li>
</ul>
```

The `data-target` must be a unique element so it's safe to use `id` instead of `class`.

And that's it.
