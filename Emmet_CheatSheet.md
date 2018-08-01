
## Child: >
nav>ul>li
```html
<nav>
    <ul>
        <li></li>
    </ul>
</nav>
```

## Sibling: +
div+p+bq
```html
<div></div>
<p></p>
<blockquote></blockquote>
```

## Climb-up: ^
div+div>p>span+em^bq
```html
<div></div>
<div>
    <p><span></span><em></em></p>
    <blockquote></blockquote>
</div>
div+div>p>span+em^^bq
<div></div>
<div>
    <p><span></span><em></em></p>
</div>
<blockquote></blockquote>
```

## Grouping: ()
div>(header>ul>li*2>a)+footer>p
```html
<div>
    <header>
        <ul>
            <li><a href=""></a></li>
            <li><a href=""></a></li>
        </ul>
    </header>
    <footer>
        <p></p>
    </footer>
</div>
```

(div>dl>(dt+dd)*3)+footer>p
```html
<div>
    <dl>
        <dt></dt>
        <dd></dd>
        <dt></dt>
        <dd></dd>
        <dt></dt>
        <dd></dd>
    </dl>
</div>
<footer>
    <p></p>
</footer>
```

## Multiplication: *
ul>li*5
```html
<ul>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
</ul>
```

## Item numbering: $

ul>li.item$*5
```html
<ul>
    <li class="item1"></li>
    <li class="item2"></li>
    <li class="item3"></li>
    <li class="item4"></li>
    <li class="item5"></li>
</ul>
```

h$[title=item$]{Header $}*3
```html
<h1 title="item1">Header 1</h1>
<h2 title="item2">Header 2</h2>
<h3 title="item3">Header 3</h3>
ul>li.item$$$*5
<ul>
    <li class="item001"></li>
    <li class="item002"></li>
    <li class="item003"></li>
    <li class="item004"></li>
    <li class="item005"></li>
</ul>
```

ul>li.item$@-*5
```html
<ul>
    <li class="item5"></li>
    <li class="item4"></li>
    <li class="item3"></li>
    <li class="item2"></li>
    <li class="item1"></li>
</ul>
```
ul>li.item$@3*5
```html
<ul>
    <li class="item3"></li>
    <li class="item4"></li>
    <li class="item5"></li>
    <li class="item6"></li>
    <li class="item7"></li>
</ul>
```

## ID and CLASS attributes

#header
```html
<div id="header"></div>
```

.title
```html
<div class="title"></div>
```

form#search.wide
```html
<form id="search" class="wide"></form>
```

p.class1.class2.class3
```html
<p class="class1 class2 class3"></p>
```
## Custom attributes

p[title="Hello world"]
```html
<p title="Hello world"></p>
```

td[rowspan=2 colspan=3 title]
```html
<td rowspan="2" colspan="3" title=""></td>
```

[a='value1' b="value2"]
```html
<div a="value1" b="value2"></div>
```
## Text: {}

a{Click me}
```html
<a href="">Click me</a>
```

p>{Click }+a{here}+{ to continue}
```html
<p>Click <a href="">here</a> to continue</p>
```

## Implicit tag names
.class
```html
<div class="class"></div>
```

em>.class
```html
<em><span class="class"></span></em>
```

ul>.class
```html
<ul>
    <li class="class"></li>
</ul>
```

table>.row>.col
```html
<table>
    <tr class="row">
        <td class="col"></td>
    </tr>
</table>
```

# HTML
All unknown abbreviations will be transformed to tag, e.g. foo → <foo></foo>.

#### !
Alias of html:5
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <title>Document</title>
</head>
<body>
    
</body>
</html>
```
#### a
```html
<a href=""></a>
```
#### a:link
```html
<a href="http://"></a>
```
#### a:mail
```html
<a href="mailto:"></a>
```
#### abbr
```html
<abbr title=""></abbr>
```
#### acronym, acr
```html
<acronym title=""></acronym>
```
#### base
```html
<base href="" />
```
#### basefont
```html
<basefont />
```
#### br
```html
<br />
```
#### frame
```html
```html
<frame />
```

#### hr
```html
<hr />
```

#### bdo
```html
<bdo dir=""></bdo>
```

#### bdo:r
```html
<bdo dir="rtl"></bdo>
```

#### bdo:l
```html
<bdo dir="ltr"></bdo>
#### col
```html
<col />
```
#### link
```html
<link rel="stylesheet" href="" />
```
#### link:css
```html
<link rel="stylesheet" href="style.css" />
```
#### link:print
```html
<link rel="stylesheet" href="print.css" media="print" />
```
#### link:favicon
```html
<link rel="shortcut icon" type="image/x-icon" href="favicon.ico" />
```
#### link:touch
```html
<link rel="apple-touch-icon" href="favicon.png" />
```
#### link:rss
```html
<link rel="alternate" type="application/rss+xml" title="RSS" href="rss.xml" />
```
#### link:atom
```html
<link rel="alternate" type="application/atom+xml" title="Atom" href="atom.xml" />
```
#### link:import, link:im
```html
<link rel="import" href="component.html" />
```
#### meta
```html
<meta />
```
#### meta:utf
```html
<meta http-equiv="Content-Type" content="text/html;charset=UTF-8" />
```
#### meta:win
```html
<meta http-equiv="Content-Type" content="text/html;charset=windows-1251" />
```
#### meta:vp
```html
<meta name="viewport" content="width=device-width, user-scalable=no, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0" />
```
#### meta:compat
```html
<meta http-equiv="X-UA-Compatible" content="IE=7" />
```
#### style
```html
<style></style>
```
#### script
```html
<script></script>
```
#### script:src
```html
<script src=""></script>
```
#### img
```html
<img src="" alt="" />
```
#### img:srcset, img:s
```html
<img srcset="" src="" alt="" />
```
#### img:sizes, img:z
```html
<img sizes="" srcset="" src="" alt="" />
```
#### picture
```html
<picture></picture>
```
#### source, src
```html
<source />
```
#### source:src, src:sc
```html
<source src="" type="" />
```
#### source:srcset, src:s
```html
<source srcset="" />
```
#### source:media, src:m
```html
<source media="(min-width: )" srcset="" />
```
#### source:type, src:t
```html
<source srcset="" type="image/" />
```
#### source:sizes, src:z
```html
<source sizes="" srcset="" />
```
#### source:media:type, src:mt
```html
<source media="(min-width: )" srcset="" type="image/" />
```
#### source:media:sizes, src:mz
```html
<source media="(min-width: )" sizes="" srcset="" />
```
#### source:sizes:type, src:zt
```html
<source sizes="" srcset="" type="image/" />
```
#### iframe
```html
<iframe src="" frameborder="0"></iframe>
```
#### embed
```html
<embed src="" type="" />
```
#### object
```html
<object data="" type=""></object>
```
#### param
```html
<param name="" value="" />
```
#### map
```html
<map name=""></map>
```
#### area
```html
<area shape="" coords="" href="" alt="" />
```
#### area:d
```html
<area shape="default" href="" alt="" />
```
#### area:c
```html
<area shape="circle" coords="" href="" alt="" />
```
#### area:r
```html
<area shape="rect" coords="" href="" alt="" />
```
#### area:p
```html
<area shape="poly" coords="" href="" alt="" />
```
#### form
```html
<form action=""></form>
```
#### form:get
```html
<form action="" method="get"></form>
```
#### form:post
```html
<form action="" method="post"></form>
```
#### label
```html
<label for=""></label>
```
#### input
```html
<input type="text" />
```
#### inp
```html
<input type="text" name="" id="" />
```
#### input:hidden, input:h
Alias of input[type=hidden name]
```html
<input type="hidden" name="" />
```
#### input:text, input:t
Alias of inp
```html
<input type="text" name="" id="" />
```
#### input:search
Alias of inp[type=search]
```html
<input type="search" name="" id="" />
```
#### input:email
Alias of inp[type=email]
```html
<input type="email" name="" id="" />
```
#### input:url
Alias of inp[type=url]
```html
<input type="url" name="" id="" />
```
#### input:password, input:p
Alias of inp[type=password]
```html
<input type="password" name="" id="" />
```
#### input:datetime
Alias of inp[type=datetime]
```html
<input type="datetime" name="" id="" />
```
#### input:date
Alias of inp[type=date]
```html
<input type="date" name="" id="" />
```
#### input:datetime-local
Alias of inp[type=datetime-local]
```html
<input type="datetime-local" name="" id="" />
```
#### input:month
Alias of inp[type=month]
```html
<input type="month" name="" id="" />
```

#### input:week
Alias of inp[type=week]
```html
<input type="week" name="" id="" />
```
#### input:time
Alias of inp[type=time]
```html
<input type="time" name="" id="" />
```
#### input:tel
Alias of inp[type=tel]
```html
<input type="tel" name="" id="" />
```
#### input:number
Alias of inp[type=number]
```html
<input type="number" name="" id="" />
```
#### input:color
Alias of inp[type=color]
```html
<input type="color" name="" id="" />
```
#### input:checkbox, input:c
Alias of inp[type=checkbox]
```html
<input type="checkbox" name="" id="" />
```
#### input:radio, input:r
Alias of inp[type=radio]
```html
<input type="radio" name="" id="" />
```
#### input:range
Alias of inp[type=range]
```html
<input type="range" name="" id="" />
```
#### input:file, input:f
Alias of inp[type=file]
```html
<input type="file" name="" id="" />
```
#### input:submit, input:s
```html
<input type="submit" value="" />
```
#### input:image, input:i
```html
<input type="image" src="" alt="" />
```
#### input:button, input:b
```html
<input type="button" value="" />
```
#### isindex
```html
<isindex />
#### input:reset
Alias of input:button[type=reset]
```html
<input type="reset" value="" />
```
#### select
```html
<select name="" id=""></select>
```
#### select:disabled, select:d
Alias of select[disabled.]
```html
<select name="" id="" disabled="disabled"></select>
```
#### option, opt
```html
<option value=""></option>
```
#### textarea
```html
<textarea name="" id="" cols="30" rows="10"></textarea>
```
#### marquee
```html
<marquee behavior="" direction=""></marquee>
```
#### menu:context, menu:c
Alias of menu[type=context]>
```html
<menu type="context"></menu>
```
#### menu:toolbar, menu:t
Alias of menu[type=toolbar]>
```html
<menu type="toolbar"></menu>
```
#### video
```html
<video src=""></video>
```
#### audio
```html
<audio src=""></audio>
```
#### html:xml
```html
<html xmlns="http://www.w3.org/1999/xhtml"></html>
```
#### keygen
```html
<keygen />
```
#### command
```html
<command />
```
#### button:submit, button:s, btn:s
Alias of button[type=submit]
```html
<button type="submit"></button>
```
#### button:reset, button:r, btn:r
Alias of button[type=reset]
```html
<button type="reset"></button>
```
#### button:disabled, button:d, btn:d
Alias of button[disabled.]
```html
<button disabled="disabled"></button>
```
#### fieldset:disabled, fieldset:d, fset:d, fst:d
Alias of fieldset[disabled.]
```html
<fieldset disabled="disabled"></fieldset>
```
#### bq
Alias of blockquote
```html
<blockquote></blockquote>
```
#### fig
Alias of figure
```html
<figure></figure>
```
#### figc
Alias of figcaption
```html
<figcaption></figcaption>
```
#### pic
Alias of picture
```html
<picture></picture>
```
#### ifr
Alias of iframe
```html
<iframe src="" frameborder="0"></iframe>
```
#### emb
Alias of embed
```html
<embed src="" type="" />
```
#### obj
Alias of object
```html
<object data="" type=""></object>
```
#### cap
Alias of caption
```html
<caption></caption>
```
#### colg
Alias of colgroup
```html
<colgroup></colgroup>
```
#### fst, fset
Alias of fieldset
```html
<fieldset></fieldset>
```
#### btn
Alias of button
```html
<button></button>
```
#### optg
Alias of optgroup
```html
<optgroup></optgroup>
```
#### tarea
Alias of textarea
```html
<textarea name="" id="" cols="30" rows="10"></textarea>
```
#### leg
Alias of legend
```html
<legend></legend>
```
#### sect
Alias of section
```html
<section></section>
```
#### art
Alias of article
```html
<article></article>
```
#### hdr
Alias of header
```html
<header></header>
```
#### ftr
Alias of footer
```html
<footer></footer>
```
#### adr
Alias of address
```html
<address></address>
```
#### dlg
Alias of dialog
```html
<dialog></dialog>
```
#### str
Alias of strong
```html
<strong></strong>
```
#### prog
Alias of progress
```html
<progress></progress>
```
#### mn
Alias of main
```html
<main></main>
```
#### tem
Alias of template
```html
<template></template>
```
#### datag
Alias of datagrid
```html
<datagrid></datagrid>
```
#### datal
Alias of datalist
```html
<datalist></datalist>
```
#### kg
Alias of keygen
```html
<keygen />
```
#### out
```html
<output></output>
```
#### det
```html
<details></details>
```
#### cmd
Alias of command
```html
<command />
```
#### doc
Alias of html>(head>meta[charset=${charset}]+title{${1:Document}})+body
```html
<html>
<head>
    <meta charset="UTF-8" />
    <title>Document</title>
</head>
<body>
    
</body>
</html>
```
#### doc4
Alias of html>(head>meta[http-equiv="Content-Type" content="text/html;charset=${charset}"]+title{${1:Document}})+body
```html
<html>
<head>
    <meta http-equiv="Content-Type" content="text/html;charset=UTF-8" />
    <title>Document</title>
</head>
<body>
    
</body>
</html>
```
#### ri:dpr, ri:d
Alias of img:s
```html
<img srcset="" src="" alt="" />
```
#### ri:viewport, ri:v
Alias of img:z
```html
<img sizes="" srcset="" src="" alt="" />
```
#### ri:art, ri:a
Alias of pic>src:m+img
```html
<picture>
    <source media="(min-width: )" srcset="" />
    <img src="" alt="" />
</picture>
```
#### ri:type, ri:t
Alias of pic>src:t+img
```html
<picture>
    <source srcset="" type="image/" />
    <img src="" alt="" />
</picture>
```
#### html:4t
Alias of !!!4t+doc4[lang=${lang}]
```html
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
<html lang="en">
<head>
    <meta http-equiv="Content-Type" content="text/html;charset=UTF-8" />
    <title>Document</title>
</head>
<body>
    
</body>
</html>
```
#### html:4s
Alias of !!!4s+doc4[lang=${lang}]
```html
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">
<html lang="en">
<head>
    <meta http-equiv="Content-Type" content="text/html;charset=UTF-8" />
    <title>Document</title>
</head>
<body>
    
</body>
</html>
```
#### html:xt
Alias of !!!xt+doc4[xmlns=http://www.w3.org/1999/xhtml xml:lang=${lang}]
```html
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en">
<head>
    <meta http-equiv="Content-Type" content="text/html;charset=UTF-8" />
    <title>Document</title>
</head>
<body>
    
</body>
</html>
```
#### html:xs
Alias of !!!xs+doc4[xmlns=http://www.w3.org/1999/xhtml xml:lang=${lang}]
```html
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en">
<head>
    <meta http-equiv="Content-Type" content="text/html;charset=UTF-8" />
    <title>Document</title>
</head>
<body>
    
</body>
</html>
```
#### html:xxs
Alias of !!!xxs+doc4[xmlns=http://www.w3.org/1999/xhtml xml:lang=${lang}]
```html
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.1//EN" "http://www.w3.org/TR/xhtml11/DTD/xhtml11.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en">
<head>
    <meta http-equiv="Content-Type" content="text/html;charset=UTF-8" />
    <title>Document</title>
</head>
<body>
    
</body>
</html>
```
#### html:5
Alias of !!!+doc[lang=${lang}]
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <title>Document</title>
</head>
<body>
    
</body>
</html>
```
#### ol+
Alias of ol>li
```html
<ol>
    <li></li>
</ol>
```
#### ul+
Alias of ul>li
```html
<ul>
    <li></li>
</ul>
```
#### dl+
Alias of dl>dt+dd
```html
<dl>
    <dt></dt>
    <dd></dd>
</dl>
```
#### map+
Alias of map>area
```html
<map name="">
    <area shape="" coords="" href="" alt="" />
</map>
```
#### table+
Alias of table>tr>td
```html
<table>
    <tr>
        <td></td>
    </tr>
</table>
```
#### colgroup+, colg+
Alias of colgroup>col
```html
<colgroup>
    <col />
</colgroup>
```
#### tr+
Alias of tr>td
```html
<tr>
    <td></td>
</tr>
```
#### select+
Alias of select>option
```html
<select name="" id="">
    <option value=""></option>
</select>
```
#### optgroup+, optg+
Alias of optgroup>option
```html
<optgroup>
    <option value=""></option>
</optgroup>
```
#### pic+
Alias of picture>source:srcset+img
```html
<picture>
    <source srcset="" />
    <img src="" alt="" />
</picture>
```
#### !!!
```html
<!DOCTYPE html>
```
#### !!!4t
```html
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
```
#### !!!4s
```html
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">
```
#### !!!xt
```html
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
```
#### !!!xs
```html
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
```
#### !!!xxs
```html
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.1//EN" "http://www.w3.org/TR/xhtml11/DTD/xhtml11.dtd">
```
#### c
```html
<!-- ${child} -->
```
#### cc:ie6
```html
<!--[if lte IE 6]>
    ${child}
<![endif]-->
```
#### cc:ie
```html
<!--[if IE]>
    ${child}
<![endif]-->
```
#### cc:noie
```html
<!--[if !IE]><!-->
    ${child}
<!--<![endif]-->
```

