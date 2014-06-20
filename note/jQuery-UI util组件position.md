
##jQuery UI util组件 position解析
---
jquery.ui.position组件是一个独立的util组件不依赖任何其他组件，可以独立存在。
它为我们提供了相对另一个元素定位一个元素的能力，
举个栗子： 我们需要一个div相对浏览器居中position组件一个方法搞定: <a href="#" target="_blank">示例</a>

    $('.mydiv').position({
        'at': 'center',
        'my': 'center',
        'of': window
    });
**at,my** 属性为position组件提供目标元素和相对元素的位置信息，有三个可选值**'left center right'**， **of**
属性提供一个相对元素, 可选值有: **Selector or Element or jQuery or <a href="#">Event</a>**, **event**是个特殊的选项，
后面会专门提到。

进价1：PM突然来了一个需求输入框输入数字同时需要在输入框上边悬浮一个框 so easy。

    $('.mydiv').position({
        'at': 'left top',
        'my': 'left bottom',
        'of': 'input'
    });
    
进价2：PM又来了XXX我们有个需求，想让鼠标在某个区域移动的时候跟随鼠标显示一个层。PM真烦 不过还好position知心朋友
so easy 

    $('.div1').mousemove(function (event) {
        $('.div2').position({
            'my': 'left bottom',
            'of': event
        });
    });
    
是不是so easy。**at,my,of**三个参数已经可以满足工作中得大多数需求了。position还有另外三个参数**collision,using,within**

    
    

    
