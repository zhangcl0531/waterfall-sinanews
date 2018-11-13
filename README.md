# waterfall-sinanews


[预览链接](http://js.jirengu.com/pocufudipu)

## 懒加载原理
当访问一个页面的时候，先把img元素或是其他元素的背景图片路径替换成同一张图片的路径（这样就只需请求一次），只有当图片出现在浏览器的可视区域内时，才设置图片正真的路径，让图片显示出来。这就是图片懒加载。

## 瀑布流原理
1.要求要进行布置的元素等宽，然后计算元素的宽度与浏览器宽度之比，得到需要布置的列数；   
2.创建一个数组，长度为列数，里面的值为已布置元素的总高度（最开始为0）；  
3.然后将未布置的元素依次布置到高度最小的那一列；  
4.重复上述操作，直至图片摆放完毕   
5.当窗体宽度发生改变时，重新调整元素排列   


## 实现原理
1.获取数据  
     1.1 获取page = 1 的 12条，page++ (此时page =2)  
     1.2 当页面滚动，load出现在屏幕时，再获取page  的12条  
2.把数据拼装成dom 放到页面   
3.使用瀑布流去摆放 dom 位置   
