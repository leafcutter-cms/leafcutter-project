# Including libraries

To include libraries just for one page, you can add them to the page's meta comment, like so:

```html
<!--@meta
theme_packages:
  - library/jquery
-->
```

This page, for example, includes a directive telling Leafcutter to load jQuery UI. If you check dev tools you should see it being loaded.

<!--@meta
theme_packages:
  - library/jquery-ui
-->
