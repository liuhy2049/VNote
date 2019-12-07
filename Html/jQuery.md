# 1. jQuery
## 1.1. 如何实现通过select的text来选中对应的option
     $("#id option:contains('text')").attr("selected", true);

## 1.2. jQuery 父级,祖先,兄弟,等选择性操作

    jQuery.parent(expr) 找父亲节点，可以传入expr进行过滤，比如$("span").parent()或者$("span").parent(".class") 
    jQuery.parents(expr),类似于jQuery.parents(expr),但是是查找所有祖先元素，不限于父元素 
    jQuery.children(expr).返回所有子节点，这个方法只会返回直接的孩子节点，不会返回所有的子孙节点 
    jQuery.contents(),返回下面的所有内容，包括节点和文本。这个方法和children()的区别就在于，包括空白文本，也会被作为一个 
    jQuery对象返回，children()则只会返回节点 
    jQuery.prev()，返回上一个兄弟节点，不是所有的兄弟节点 
    jQuery.prevAll()，返回所有之前的兄弟节点 
    jQuery.next(),返回下一个兄弟节点，不是所有的兄弟节点 
    jQuery.nextAll()，返回所有之后的兄弟节点 
    jQuery.siblings(),返回兄弟姐妹节点，不分前后 
    jQuery.find(expr),跟jQuery.filter(expr)完全不一样。jQuery.filter()是从初始的jQuery对象集合中筛选出一部分，而jQuery.find()的返回结果，不会有初始集合中的内容，比如$("p"),find("span"),是从元素开始找,等同于$("p span")

## 1.3. jQuery on()绑定动态元素出现的问题
    如果可能，尝试将事件侦听器绑定到最精确的元素，以避免无用的事件处理。
    也就是说，如果向ID A的现有元素添加B类元素，则不使用
        $（document.body）.on（'单击'，'#a.b'，函数（）{
    而是使用
        $（'#a'）.on（'单击'，'.b'，函数（）{ # jQuery
