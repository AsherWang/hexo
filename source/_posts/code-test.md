---
title: code-test
---
``` javascript
    console.log('233');
    hexo.extend.tag.register('fancybox', function(args){
    var original = args.shift(),
        thumbnail = '';

    if (args.length && rUrl.test(args[0])){
        thumbnail = args.shift();
    }

    var title = args.join(' ');

    return '<a class="fancybox" href="' + original + '" title="' + title + '">' +
        '<img src="' + (thumbnail || original) + '" alt="' + title + '">'
        '</a>' +
        (title ? '<span class="caption">' + title + '</span>' : '');
    });
```