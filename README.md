# test

## Project setup

``` 
npm install
```

### Compiles and hot-reloads for development

``` 
npm run serve
```

### Compiles and minifies for production

``` 
npm run build
```

### Lints and fixes files

``` 
npm run lint
```

### sass
& 取到父选择器

.funky {
  font: {
    family: fantasy;
    size: 30em;
    weight: bold;
  }
}

$ 变量声明
1.数字，1, 2, 13, 10px
2.字符串，有引号字符串与无引号字符串，"foo", 'bar', baz
3.颜色，blue, #04a3f9, rgba(255,0,0,0.5)
4.布尔型，true, false
5.空值，null
6.数组 (list)，用空格或逗号作分隔符
7.maps, 相当于 JavaScript 的 object，(key1: value1, key2: value2)

#{} 插值语句
通过 #{} 插值语句可以在选择器或属性名中使用变量
p.#{$name} {
  #{$attr}-color: blue;
}

!default 给一个未通过 !default 声明赋值的变量赋值，此时，如果变量已经被赋值，不会再被重新赋值，但是如果变量还没有被赋值，则会被赋予新的值
$content: "First content";
$content: "Second content?" !default;
$content为"First content"

@import 导入 SCSS 或 Sass 文件

@media screen and (max-width: 300px){}

@extend继承样式

@if 当 @if 的表达式返回值不是 false 或者 null 时，条件成立，输出 {} 内的代码
p {
  @if $type == ocean {
    color: blue;
  }  @else if $type == monster {
    color: green;
  } @else {
    color: black;
  }
}

@for $i from 1 through 3 {
  .item-#{$i} { width: 2em * $i; }
}
当使用 through 时，条件范围包含 <start> 与 <end> 的值，而使用 to 时条件范围只包含 <start> 的值不包含 <end> 的值

@each
@each $var in <list> {}

混合指令 @mixin 可以用 =
@include 可以用 +

函数指令 @function grid-width($n) {
  @return $n * $grid-width + ($n - 1) * $gutter-width;
}