# nicehatjimmy

Based on the work of https://github.com/davidphilipbarr/nicehatharry#. I have just updated the GPIO pins to suit my needs. 

A small 'hat' that sits ontop of the nice!nano to support a nice!view.

In your zmk-config repo, in  `config/west.yml`  file:

In  `manifest.remotes`

```
    - name: rpk
      url-base: https://github.com/rpkeeb
```

And then in  `manifest.projects`:

```
    - name: nicehatjimmy
      remote: rpk
      revision: main
````

And then in  `build.yaml`:

```
    - board: nice_nano
      shield: 'your_keyboard' nicehatjimmy nice_view
```

And finally, place the  `nicehatjimmy`  in place of the nice_view_adapter from the nice_view instructions.
