---

title: Pink老师 HTML CSS 学习笔记（第十三季）
date: 2021-02-16 21:59:38
categories:
- [前端]
- [HTML]
- [CSS]
tags:
- HTML
- CSS
- Pink
---

![](https://img-blog.csdnimg.cn/20210116002056446.jpg)

<!--more-->

> 本学习笔记是个人对Pink老师课程的总结归纳，转载请注明出处！ 

# Pink老师 HTML CSS 学习笔记（第十二季）

> 原创思维导图，开源地址：https://github.com/JERRY-Z-J-R/JERRY-Mind

![](https://img-blog.csdnimg.cn/20210217011404416.png)

# 案例：

![](https://img-blog.csdnimg.cn/20210217015342801.gif)

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>CSS3 属性选择器</title>
    <style>
        /* 属性选择器使用方法 */
        /* 选择的是：  既是button 又有 disabled 这个属性的元素 */
        /* 属性选择器的权重是 10 */
        /* 1.直接写属性 */

        button[disabled] {
            cursor: default;
        }

        button {
            cursor: pointer;
        }

        /* 2. 属性等于值 */

        input[type="search"] {
            color: pink;
        }

        /* 3. 以某个值开头的 属性值 */

        div[class^="icon"] {
            color: red;
        }

        /* 4. 以某个值结尾的 */

        div[class$="icon"] {
            color: green;
        }

        /* 5. 可以在任意位置的 */

        div[class*="icon"] {
            color: blue;
        }
    </style>
</head>

<body>
    <!-- disabled 是禁用我们的按钮 -->
    <button>按钮</button>
    <button>按钮</button>
    <button disabled="disabled">按钮</button>
    <button disabled="disabled">按钮</button>

    <input type="text" name="" id="" value="文本框">
    <input type="text" name="" id="" value="文本框">
    <input type="text" name="" id="" value="文本框">
    <input type="search" name="" id="" value="搜索框">
    <input type="search" name="" id="" value="搜索框">
    <input type="search" name="" id="" value="搜索框">
    <div class="icon1">图标1</div>
    <div class="icon2">图标2</div>
    <div class="icon3">图标3</div>
    <div class="iicon3">图标4</div>
    <div class="absicon">图标5</div>
</body>

</html>
```

---

![](https://img-blog.csdnimg.cn/20210217015608669.png)

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>CSS3 结构伪类选择器</title>
    <style>
        ul li:first-child {
            background-color: pink;
        }

        ul li:last-child {
            background-color: deeppink;
        }

        /* nth-child(n)  我们要第几个，n就是几  比如我们选第8个， 我们直接写 8就可以了 */

        ul li:nth-child(8) {
            background-color: lightpink;
        }
    </style>
</head>

<body>
    <ul>
        <li>1</li>
        <li>2</li>
        <li>3</li>
        <li>4</li>
        <li>5</li>
        <li>6</li>
        <li>7</li>
        <li>8</li>
        <li>9</li>
        <li>10</li>
    </ul>
</body>

</html>
```

---

![](https://img-blog.csdnimg.cn/20210217015745606.png)

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>nth-child</title>
    <style>
        /* n 可是关键词  even 是偶数  odd 是奇数 */
        /* ul li:nth-child(even) {
            background-color: pink;
        }
        
        ul li:nth-child(odd) {
            background-color: hotpink;
        } */
        /* n 是公式  但是 n 从0开始计算 */
        /* ul li:nth-child(n) {
            background-color: pink;
        } */
        /* 2n 偶数  类似于 even */
        /* ul li:nth-child(2n) {
            background-color: pink;
        } */
        /* 2n + 1  类似于 odd */
        /* ul li:nth-child(2n+1) {
            background-color: skyblue;
        } */
        /* 5n  选择第  0  5  10  15 ... */
        /* ul li:nth-child(5n) {
            background-color: pink;
        } */
        /* n+5 就是从第5个开始往后面选择 包含第5个 */
        /* ul li:nth-child(n+5) {
            background-color: pink;
        } */
        /* -n + 5 就是选择前面5个  */

        ul li:nth-child(-n+5) {
            background-color: pink;
        }
    </style>
</head>

<body>
    <ul>
        <li>1</li>
        <li>2</li>
        <li>3</li>
        <li>4</li>
        <li>5</li>
        <li>6</li>
        <li>7</li>
        <li>8</li>
        <li>9</li>
        <li>10</li>
    </ul>
</body>
```

---

![](https://img-blog.csdnimg.cn/20210217015921561.png)

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>nth-of-type</title>
    <style>
        /* div :nth-child(1) {
            background-color: pink;
        }
        
        div :nth-child(2) {
            background-color: purple;
        } */
        /* div span:nth-child(1) {  这个选不到
            background-color: pink;
        } */

        div span:nth-child(2) {
            background-color: pink;
        }

        /* 总结： :nth-child(n)  选择 父元素里面的 第 n个孩子， 它不管里面的孩子是否同一种类型 */
        /* of-type 选择指定类型的元素 */

        div span:first-of-type {
            background-color: purple;
        }

        div span:last-of-type {
            background-color: skyblue;
        }

        div span:nth-of-type(2) {
            background-color: red;
        }
    </style>
</head>

<body>
    <div>
        <p>我是一个屁</p>
        <span>我是span</span>
        <span>我是span</span>
        <span>我是span</span>
    </div>
    <!-- ul 里面我们只允许放li  所以 nth-child 和 nth-of-type 就一样了 -->
    <ul>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
    </ul>
</body>

</html>
```

---

![](https://img-blog.csdnimg.cn/2021021702475540.png)

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>CSS3 伪元素选择器</title>
    <style>
        div {
            width: 300px;
            height: 300px;
            border: 1px solid #000;
        }

        div::before {
            content: "我";
            display: inline-block;
            width: 100px;
            height: 100px;
            background-color: pink;
        }

        div::after {
            content: "小猪佩奇";
            display: inline-block;
            width: 100px;
            height: 100px;
            background-color: pink;
        }
    </style>
</head>

<body>
    <div>是</div>
</body>

</html>
```

---

![](https://img-blog.csdnimg.cn/20210217020056941.png)

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>伪元素选择器案例</title>
    <style>
        @font-face {
            font-family: 'icomoon';
            src: url('fonts/icomoon.eot?cv013x');
            src: url('fonts/icomoon.eot?cv013x#iefix') format('embedded-opentype'), url('fonts/icomoon.ttf?cv013x') format('truetype'), url('fonts/icomoon.woff?cv013x') format('woff'), url('fonts/icomoon.svg?cv013x#icomoon') format('svg');
            font-weight: normal;
            font-style: normal;
        }

        span {
            font-family: 'icomoon';
            position: absolute;
            top: 10px;
            right: 10px;
        }

        div,
        p {
            position: relative;
            width: 249px;
            height: 35px;
            border: 1px solid red;
        }

        /* p::after {
            content: '';
            position: absolute;
            top: 10px;
            right: 10px;
            font-family: 'icomoon';
        } */

        p::after {
            content: '\ea50';
            position: absolute;
            top: 10px;
            right: 10px;
            font-family: 'icomoon';
        }
    </style>
</head>

<body>
    <div>
        <span></span>
    </div>

    <p></p>
</body>

</html>
```

---

![](https://img-blog.csdnimg.cn/20210217020158108.png)

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>2D 转换之位移 translate</title>
    <style>
        /* 移动盒子的位置： 定位   盒子的外边距  2d转换移动 */

        div {
            width: 200px;
            height: 200px;
            background-color: pink;
            /* x就是x轴上移动位置 y 就是y轴上移动位置 中间用逗号分隔*/
            /* transform: translate(x, y); */
            /* transform: translate(100px, 100px); */
            /* 1. 我们如果只移动x坐标 */
            /* transform: translate(100px, 0); */
            /* transform: translateX(100px); */
            /* 2. 我们如果只移动y坐标 */
            /* transform: translate(0, 100px); */
            /* transform: translateY(100px); */
        }

        div:first-child {
            transform: translate(30px, 30px);
        }

        div:last-child {
            background-color: purple;
        }
    </style>
</head>

<body>
    <div></div>
    <div></div>
</body>

</html>
```

---

![](https://img-blog.csdnimg.cn/20210217020306705.png)

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>让盒子实现水平居中和垂直居中</title>
    <style>
        div {
            position: relative;
            width: 500px;
            height: 500px;
            background-color: pink;
            /* 1. 我们tranlate里面的参数是可以用 % */
            /* 2. 如果里面的参数是 % 移动的距离是 盒子自身的宽度或者高度来对比的 */
            /* 这里的 50% 就是 50px 因为盒子的宽度是 100px */
            /* transform: translateX(50%); */
        }

        p {
            position: absolute;
            top: 50%;
            left: 50%;
            width: 200px;
            height: 200px;
            background-color: purple;
            /* margin-top: -100px;
            margin-left: -100px; */
            /* translate(-50%, -50%)  盒子往上走自己高度的一半   */
            transform: translate(-50%, -50%);
        }

        span {
            /* translate 对于行内元素是无效的 */
            transform: translate(300px, 300px);
        }
    </style>
</head>

<body>
    <div>
        <p></p>
    </div>
    <span>123</span>
</body>

</html>
```

---

![](https://img-blog.csdnimg.cn/2021021702042026.gif)

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>2D 转换之旋转 rotate</title>
    <style>
        img {
            width: 150px;
            /* 顺时针旋转45度 */
            /* transform: rotate(45deg); */
            border-radius: 50%;
            border: 5px solid pink;
            /* 过渡写到本身上，谁做动画给谁加 */
            transition: all 0.3s;
        }

        img:hover {
            transform: rotate(360deg);
        }
    </style>
</head>

<body>
    <img src="media/pic.jpg" alt="">
</body>

</html>
```

---

![](https://img-blog.csdnimg.cn/20210217020528635.gif)

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>CSS3 书写三角</title>
    <style>
        div {
            position: relative;
            width: 249px;
            height: 35px;
            border: 1px solid #000;
        }

        div::after {
            content: "";
            position: absolute;
            top: 8px;
            right: 15px;
            width: 10px;
            height: 10px;
            border-right: 1px solid #000;
            border-bottom: 1px solid #000;
            transform: rotate(45deg);
            transition: all 0.2s;
        }

        /* 鼠标经过div  里面的三角旋转 */

        div:hover::after {
            transform: rotate(225deg);
        }
    </style>
</head>

<body>
    <div></div>
</body>

</html>
```

---

![](https://img-blog.csdnimg.cn/20210217021053713.gif)

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>设置元素转换中心点</title>
    <style>
        div {
            width: 200px;
            height: 200px;
            background-color: pink;
            margin: 100px auto;
            transition: all 1s;
            /* 1.可以跟方位名词 */
            /* transform-origin: left bottom; */
            /* 2. 默认的是 50%  50%  等价于 center  center */
            /* 3. 可以是px 像素 */
            transform-origin: 50px 50px;
        }

        div:hover {
            transform: rotate(360deg);
        }
    </style>
</head>

<body>
    <div></div>
</body>

</html>
```

---

![](https://img-blog.csdnimg.cn/20210217021248617.gif)

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>旋转中心点案例</title>
    <style>
        div {
            overflow: hidden;
            width: 200px;
            height: 200px;
            border: 1px solid pink;
            margin: 10px;
            float: left;
        }

        div::before {
            content: "黑马";
            display: block;
            width: 100%;
            height: 100%;
            background-color: hotpink;
            transform: rotate(180deg);
            transform-origin: left bottom;
            transition: all 0.4s;
        }

        /* 鼠标经过div 里面的before 复原 */

        div:hover::before {
            transform: rotate(0deg);
        }
    </style>
</head>

<body>
    <div></div>
    <div></div>
    <div></div>
</body>

</html>
```

---

![](https://img-blog.csdnimg.cn/20210217021352979.gif)

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>2D转换之缩放scale</title>
    <style>
        div {
            width: 200px;
            height: 200px;
            background-color: pink;
            margin: 100px auto;
            /* transform-origin: left bottom; */
        }

        div:hover {
            /* 1. 里面写的数字不跟单位 就是倍数的意思 1 就是1倍  2就是 2倍 */
            /* transform: scale(x, y); */
            /* transform: scale(2, 2); */
            /* 2. 修改了宽度为原来的2倍  高度 不变 */
            /* transform: scale(2, 1); */
            /* 3. 等比例缩放 同时修改宽度和高度，我们有简单的写法  以下是 宽度修改了2倍，高度默认和第一个参数一样*/
            /* transform: scale(2); */
            /* 4. 我们可以进行缩小  小于1 就是缩放 */
            /* transform: scale(0.5, 0.5); */
            /* transform: scale(0.5); */
            /* 5. scale 的优势之处： 不会影响其他的盒子 而且可以设置缩放的中心点*/
            /* width: 300px;
            height: 300px; */
            transform: scale(2);
        }
    </style>
</head>

<body>
    <div></div>
    123123
</body>

</html>
```

---

![](https://img-blog.csdnimg.cn/2021021702150355.gif)

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>图片放大案例</title>
    <style>
        div {
            overflow: hidden;
            float: left;
            margin: 10px;
        }

        div img {
            transition: all .4s;
        }

        div img:hover {
            transform: scale(1.1);
        }
    </style>
</head>

<body>
    <div>
        <a href="#"><img src="media/scale.jpg" alt=""></a>
    </div>
    <div>
        <a href="#"><img src="media/scale.jpg" alt=""></a>
    </div>
    <div>
        <a href="#"><img src="media/scale.jpg" alt=""></a>
    </div>
</body>

</html>
```

---

![](https://img-blog.csdnimg.cn/20210217021618941.gif)

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>分页按钮案例</title>
    <style>
        li {
            float: left;
            width: 30px;
            height: 30px;
            border: 1px solid pink;
            margin: 10px;
            text-align: center;
            line-height: 30px;
            list-style: none;
            border-radius: 50%;
            cursor: pointer;
            transition: all .4s;
        }

        li:hover {
            transform: scale(1.2);
        }
    </style>
</head>

<body>
    <ul>
        <li>1</li>
        <li>2</li>
        <li>3</li>
        <li>4</li>
        <li>5</li>
        <li>6</li>
        <li>7</li>
    </ul>
</body>

</html>
```

---

![](https://img-blog.csdnimg.cn/20210217021717404.gif)

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>2D转换综合写法顺序</title>
    <style>
        div {
            width: 200px;
            height: 200px;
            background-color: pink;
            transition: all .5s;
        }

        div:hover {
            /* transform: rotate(180deg) translate(150px, 50px); */
            /* 我们同时有位移和其他属性，我们需要把位移放到最前面 */
            transform: translate(150px, 50px) rotate(180deg) scale(1.2);
        }
    </style>
</head>

<body>
    <div></div>
</body>

</html>
```

---

![](https://img-blog.csdnimg.cn/20210217021827408.gif)

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>CSS3动画基本使用</title>
    <style>
        /* 我们想页面一打开，一个盒子就从左边走到右边 */
        /* 1. 定义动画 */

        @keyframes move {

            /* 开始状态 */
            0% {
                transform: translateX(0px);
            }

            /* 结束状态 */
            100% {
                transform: translateX(1000px);
            }
        }

        div {
            width: 200px;
            height: 200px;
            background-color: pink;
            /* 2. 调用动画 */
            /* 动画名称 */
            animation-name: move;
            /* 持续时间 */
            animation-duration: 2s;
        }
    </style>
</head>

<body>
    <div></div>
</body>

</html>
```

---

![](https://img-blog.csdnimg.cn/20210217022020704.gif)

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>动画序列</title>
    <style>
        /* from to 等价于  0% 和  100% */
        /* @keyframes move {
            from {
                transform: translate(0, 0);
            }
            to {
                transform: translate(1000px, 0);
            }
        } */
        /* 动画序列 */
        /* 1. 可以做多个状态的变化 keyframe 关键帧 */
        /* 2. 里面的百分比要是整数 */
        /* 3. 里面的百分比就是 总的时间（我们这个案例10s）的划分 25% * 10  =  2.5s */

        @keyframes move {
            0% {
                transform: translate(0, 0);
            }

            25% {
                transform: translate(1000px, 0)
            }

            50% {
                transform: translate(1000px, 500px);
            }

            75% {
                transform: translate(0, 500px);
            }

            100% {
                transform: translate(0, 0);
            }
        }

        div {
            width: 100px;
            height: 100px;
            background-color: pink;
            animation-name: move;
            animation-duration: 10s;
        }
    </style>
</head>

<body>
    <div>

    </div>
</body>

</html>
```

---

![](https://img-blog.csdnimg.cn/2021021702213542.png)

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>动画属性</title>
    <style>
        @keyframes move {
            0% {
                transform: translate(0, 0);
            }

            100% {
                transform: translate(1000px, 0);
            }
        }

        div {
            width: 100px;
            height: 100px;
            background-color: pink;
            /* 动画名称 */
            animation-name: move;
            /* 持续时间 */
            /* animation-duration: 2s; */
            /* 运动曲线 */
            /* animation-timing-function: ease; */
            /* 何时开始 */
            animation-delay: 1s;
            /* 重复次数  iteration 重复的 conut 次数  infinite  无限 */
            /* animation-iteration-count: infinite; */
            /* 是否反方向播放 默认的是 normal  如果想要反方向 就写 alternate */
            /* animation-direction: alternate; */
            /* 动画结束后的状态 默认的是 backwards  回到起始状态 我们可以让他停留在结束状态 forwards */
            /* animation-fill-mode: forwards; */
            /* animation: name duration timing-function delay iteration-count direction fill-mode; */
            /* animation: move 2s linear 0s 1 alternate forwards; */
            /* 前面2个属性 name  duration 一定要写 */
            /* animation: move 2s linear  alternate forwards; */
        }

        div:hover {
            /* 鼠标经过div 让这个div 停止动画，鼠标离开就继续动画 */
            animation-play-state: paused;
        }
    </style>
</head>

<body>
    <div>

    </div>
</body>

</html>
```

---

![](https://img-blog.csdnimg.cn/20210217022445531.gif)

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>大数据热点图</title>
    <style>
        body {
            background-color: #333;
        }

        .map {
            position: relative;
            width: 747px;
            height: 616px;
            background: url(media/map.png) no-repeat;
            margin: 0 auto;
        }

        .city {
            position: absolute;
            top: 227px;
            right: 193px;
            color: #fff;
        }

        .tb {
            top: 500px;
            right: 80px;
        }

        .dotted {
            width: 8px;
            height: 8px;
            background-color: #09f;
            border-radius: 50%;
        }

        .city div[class^="pulse"] {
            /* 保证我们小波纹在父盒子里面水平垂直居中 放大之后就会中心向四周发散 */
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 8px;
            height: 8px;
            box-shadow: 0 0 12px #009dfd;
            border-radius: 50%;
            animation: pulse 1.2s linear infinite;
        }

        .city div.pulse2 {
            animation-delay: 0.4s;
        }

        .city div.pulse3 {
            animation-delay: 0.8s;
        }

        @keyframes pulse {
            0% {}

            70% {
                /* transform: scale(5);  我们不要用scale 因为他会让 阴影变大*/
                width: 40px;
                height: 40px;
                opacity: 1;
            }

            100% {
                width: 70px;
                height: 70px;
                opacity: 0;
            }
        }
    </style>
</head>

<body>
    <div class="map">
        <div class="city">
            <div class="dotted"></div>
            <div class="pulse1"></div>
            <div class="pulse2"></div>
            <div class="pulse3"></div>
        </div>
        <div class="city tb">
            <div class="dotted"></div>
            <div class="pulse1"></div>
            <div class="pulse2"></div>
            <div class="pulse3"></div>
        </div>
    </div>
</body>

</html>
```

---

![](https://img-blog.csdnimg.cn/20210217022628523.gif)

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>速度曲线步长</title>
    <style>
        div {
            overflow: hidden;
            font-size: 20px;
            width: 0;
            height: 30px;
            background-color: pink;
            /* 让我们的文字强制一行内显示 */
            white-space: nowrap;
            /* steps 就是分几步来完成我们的动画 有了steps 就不要在写 ease 或者linear 了 */
            animation: w 4s steps(10) forwards;
        }

        @keyframes w {
            0% {
                width: 0;
            }

            100% {
                width: 200px;
            }
        }
    </style>
</head>

<body>
    <div>世纪佳缘我在这里等你</div>
</body>

</html>
```

---

![](https://img-blog.csdnimg.cn/20210217022748739.gif)

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>奔跑的熊大案例</title>
    <style>
        body {
            background-color: #ccc;
        }

        div {
            position: absolute;
            width: 200px;
            height: 100px;
            background: url(media/bear.png) no-repeat;
            /* 我们元素可以添加多个动画， 用逗号分隔 */
            animation: bear .4s steps(8) infinite, move 3s forwards;
        }

        @keyframes bear {
            0% {
                background-position: 0 0;
            }

            100% {
                background-position: -1600px 0;
            }
        }

        @keyframes move {
            0% {
                left: 0;
            }

            100% {
                left: 50%;
                /* margin-left: -100px; */
                transform: translateX(-50%);
            }
        }
    </style>
</head>

<body>
    <div></div>
</body>

</html>
```

---

![](https://img-blog.csdnimg.cn/20210217022851426.png)

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>3D移动translate3d</title>
    <style>
        body {
            /* 透视写到被观察元素的父盒子上面 */
            perspective: 200px;
        }

        div {
            width: 200px;
            height: 200px;
            background-color: pink;
            /* transform: translateX(100px);
            transform: translateY(100px); */
            /* transform: translateX(100px) translateY(100px) translateZ(100px); */
            /* 1. translateZ 沿着Z轴移动 */
            /* 2. translateZ 后面的单位我们一般跟px */
            /* 3. translateZ(100px) 向外移动100px （向我们的眼睛来移动的） */
            /* 4. 3D移动有简写的方法 */
            /* transform: translate3d(x,y,z); */
            /* transform: translate3d(100px, 100px, 100px); */
            /* 5. xyz是不能省略的，如果没有就写0 */
            transform: translate3d(400px, 100px, 100px);
        }
    </style>
</head>

<body>
    <div></div>
</body>

</html>
```

---

![](https://img-blog.csdnimg.cn/20210217022935906.png)

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>translateZ</title>
    <style>
        body {
            perspective: 500px;
        }

        div {
            width: 200px;
            height: 200px;
            background-color: pink;
            margin: 100px auto;
            transform: translateZ(0);
        }
    </style>
</head>

<body>
    <div></div>
    <div></div>
    <div></div>
</body>

</html>
```

---

![](https://img-blog.csdnimg.cn/20210217023103697.gif)

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>rotateX</title>
    <style>
        body {
            perspective: 300px;
        }

        img {
            display: block;
            margin: 100px auto;
            transition: all 1s;
        }

        img:hover {
            transform: rotateX(45deg);
        }
    </style>
</head>

<body>
    <img src="media/pig.jpg" alt="">
</body>

</html>
```

---

![](https://img-blog.csdnimg.cn/20210217023224657.gif)

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>rotateY</title>
    <style>
        body {
            perspective: 500px;
        }

        img {
            display: block;
            margin: 100px auto;
            transition: all 1s;
        }

        img:hover {
            transform: rotateY(45deg);
        }
    </style>
</head>

<body>
    <img src="media/pig.jpg" alt="">
</body>

</html>
```

---

![](https://img-blog.csdnimg.cn/20210217023338360.gif)

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>rotateZ</title>
    <style>
        body {
            perspective: 500px;
        }

        img {
            display: block;
            margin: 100px auto;
            transition: all 1s;
        }

        img:hover {
            /* transform: rotateZ(180deg); */
            /* transform: rotate3d(x,y,z,deg); */
            /* transform: rotate3d(1, 0, 0, 45deg); */
            /* transform: rotate3d(0, 1, 0, 45deg); */
            transform: rotate3d(1, 1, 0, 45deg);
        }
    </style>
</head>

<body>
    <img src="media/pig.jpg" alt="">
</body>

</html>
```

---

![](https://img-blog.csdnimg.cn/20210217023437371.gif)

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>3D呈现transform-style</title>
    <style>
        body {
            perspective: 500px;
        }

        .box {
            position: relative;
            width: 200px;
            height: 200px;
            margin: 100px auto;
            transition: all 2s;
            /* 让子元素保持3d立体空间环境 */
            transform-style: preserve-3d;
        }

        .box:hover {
            transform: rotateY(60deg);
        }

        .box div {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: pink;
        }

        .box div:last-child {
            background-color: purple;
            transform: rotateX(60deg);
        }
    </style>
</head>

<body>
    <div class="box">
        <div></div>
        <div></div>
    </div>
</body>

</html>
```

---

![](https://img-blog.csdnimg.cn/20210217023558144.gif)

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>两面翻转的盒子</title>
    <style>
        body {
            perspective: 400px;
        }

        .box {
            position: relative;
            width: 300px;
            height: 300px;
            margin: 100px auto;
            transition: all .4s;
            /* 让背面的紫色盒子保留立体空间 给父级添加的 */
            transform-style: preserve-3d;
        }

        .box:hover {
            transform: rotateY(180deg);
        }

        .front,
        .back {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            border-radius: 50%;
            font-size: 30px;
            color: #fff;
            text-align: center;
            line-height: 300px;
        }

        .front {
            background-color: pink;
            z-index: 1;
        }

        .back {
            background-color: purple;
            /* 像手机一样 背靠背 旋转 */
            transform: rotateY(180deg);
        }
    </style>
</head>

<body>
    <div class="box">
        <div class="front">黑马程序员</div>
        <div class="back">pink老师这里等你</div>
    </div>
</body>

</html>
```

---

![](https://img-blog.csdnimg.cn/20210217023709823.gif)

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>3D导航栏案例</title>
    <style>
        * {
            margin: 0;
            padding: 0;
        }

        ul {
            margin: 100px;
        }

        ul li {
            float: left;
            margin: 0 5px;
            width: 120px;
            height: 35px;
            list-style: none;
            /* 一会我们需要给box 旋转 也需要透视 干脆给li加 里面的子盒子都有透视效果 */
            perspective: 500px;
        }

        .box {
            position: relative;
            width: 100%;
            height: 100%;
            transform-style: preserve-3d;
            transition: all .4s;
        }

        .box:hover {
            transform: rotateX(90deg);
        }

        .front,
        .bottom {
            position: absolute;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
        }

        .front {
            background-color: pink;
            z-index: 1;
            transform: translateZ(17.5px);
        }

        .bottom {
            background-color: purple;
            /* 这个x轴一定是负值 */
            /* 我们如果有移动 或者其他样式，必须先写我们的移动 */
            transform: translateY(17.5px) rotateX(-90deg);
        }
    </style>
</head>

<body>
    <ul>
        <li>
            <div class="box">
                <div class="front">黑马程序员</div>
                <div class="bottom">pink老师等你</div>
            </div>
        </li>
        <li>
            <div class="box">
                <div class="front">黑马程序员</div>
                <div class="bottom">pink老师等你</div>
            </div>
        </li>
        <li>
            <div class="box">
                <div class="front">黑马程序员</div>
                <div class="bottom">pink老师等你</div>
            </div>
        </li>
        <li>
            <div class="box">
                <div class="front">黑马程序员</div>
                <div class="bottom">pink老师等你</div>
            </div>
        </li>
        <li>
            <div class="box">
                <div class="front">黑马程序员</div>
                <div class="bottom">pink老师等你</div>
            </div>
        </li>
        <li>
            <div class="box">
                <div class="front">黑马程序员</div>
                <div class="bottom">pink老师等你</div>
            </div>
        </li>
    </ul>
</body>

</html>
```

---

![](https://img-blog.csdnimg.cn/20210217024600678.gif)

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>综合案例旋转木马</title>
    <style>
        body {
            perspective: 1000px;
        }

        section {
            position: relative;
            width: 300px;
            height: 200px;
            margin: 150px auto;
            transform-style: preserve-3d;
            /* 添加动画效果 */
            animation: rotate 10s linear infinite;
            background: url(media/pig.jpg) no-repeat;
        }

        section:hover {
            /* 鼠标放入section 停止动画 */
            animation-play-state: paused;
        }

        @keyframes rotate {
            0% {
                transform: rotateY(0);
            }

            100% {
                transform: rotateY(360deg);
            }
        }

        section div {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url(media/dog.jpg) no-repeat;
        }

        section div:nth-child(1) {
            transform: rotateY(0) translateZ(300px);
        }

        section div:nth-child(2) {
            /* 先旋转好了再 移动距离 */
            transform: rotateY(60deg) translateZ(300px);
        }

        section div:nth-child(3) {
            /* 先旋转好了再 移动距离 */
            transform: rotateY(120deg) translateZ(300px);
        }

        section div:nth-child(4) {
            /* 先旋转好了再 移动距离 */
            transform: rotateY(180deg) translateZ(300px);
        }

        section div:nth-child(5) {
            /* 先旋转好了再 移动距离 */
            transform: rotateY(240deg) translateZ(300px);
        }

        section div:nth-child(6) {
            /* 先旋转好了再 移动距离 */
            transform: rotateY(300deg) translateZ(300px);
        }
    </style>
</head>

<body>
    <section>
        <div></div>
        <div></div>
        <div></div>
        <div></div>
        <div></div>
        <div></div>
    </section>
</body>

</html>
```

---

![](https://img-blog.csdnimg.cn/20210217023948571.png)

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>vscode</title>
    <style>
        div {
            color: red;
            font-size: 12px;
            line-height: 1.5;
        }
    </style>
</head>

<body>
    <div>12</div>
    <div>12</div>
    <div>12</div>
    <div>12</div>
    <div>abc</div>
    <div>abc</div>
    <div>abqwec</div>
    <div>12</div>
    <div>
        <div></div>
        <div></div>
    </div>
    <div name="" id="" cols="30" rows="10"></div>
</body>

</html>
```

---


> **与我交流 >_^**
>
> **QQ：** 1846334075
>
> **WeChat：** zhoujirui54
>
> **个人网站：** <http://jerry-z-j-r.github.io>	
>
> **CSDN：** <https://blog.csdn.net/D_si_God>
>
> **Cnblogs：** <https://www.cnblogs.com/JERRY-Z-J-R/>
>
> **GitHub：** <https://github.com/JERRY-Z-J-R>
>
> **Gitee：** <https://gitee.com/JERRY-Z-J-R>
>
> **bilibili：** <https://space.bilibili.com/505277890>
>
> **微博：** <https://weibo.com/JERRY2454>
>
> **知乎：** <https://www.zhihu.com/people/JERRY-Z-J-R>