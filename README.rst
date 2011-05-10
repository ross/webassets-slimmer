There's not much to it, just import webassets_slimmer to allow it to add its
filters. and then add js_slimmer or css_slimmer to your filters list.

    import webassets_slimmer

    register('js_all', Bundle('js/jquery.min.js', 'js/log.js', 'js/app.js',
        filters=['js_slimmer'], output=join('js', 'js_all.js')))
    register('css_all', Bundle('css/grid.css', 'css/screen.css',
        filters=['css_slimmer'], output=join('css', 'css_all.css')))
