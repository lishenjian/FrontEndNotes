#页面头排版问题
##无序列表
页面头中通常会使用链表作为页面头的导航，因此考虑把 li 元素水平排列：
   ```
   <!DOCTYPE>
    <html>
        <head>
            <meta charset="utf-8">
            <style>
                ul{
                    background-color:#ccc;
                    height:100px;
                }
                .displaySty li{
                    display:inline-block;
                }
                .floatSty li{
                    float:left;
                    padding-right:30px;
                }
            </style>
        </head>
        <body>
            <ul class="displaySty">
                <li><a href="#">链接一</a></li>
                <li><a href="#">链接二</a></li>
                <li><a href="#">链接三</a></li>
            </ul>
            <ul class="floatSty">
                <li><a href="#">链接一</a></li>
                <li><a href="#">链接二</a></li>
                <li><a href="#">链接三</a></li>
            </ul>
        </body>
    </html>
    ```
    1. 用浮动
       用浮动使li脱离原来的文档流，向 left 或 right浮动使li水平排布（原来的列表前的图标会保留，需要用list-style:none; 去除）；
    2. display样式
       inline-block 把li 变为内联元素，li之间没有换行，因此会水平排列，但是列表前的图标会自动消失；