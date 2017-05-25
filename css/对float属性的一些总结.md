### 对float属性的一些总结。

前提：大的div盒子内包含两个div盒子或者是span行内元素。父的div的className为parent，子div盒子分别为div-1、div-2，当子元素为span行内元素为span-1、span-2。

* 当**div-1**的float属性为left时，
	* **parent盒子**发生高度坍塌，此时高度为不浮动元素的高度。
  * **div-1盒子**的表现形式像脱离文件流，直到触碰到float的元素。
  * **div-2盒子**的表现形式就当div-1盒子不存在时显示，但是文字部分的表现形式会对float盒子形成文字环绕。


* 当**div-1**的float属性为left时，div-2的float的属性为left时，
	* **parent盒子**发生高度坍塌，此时高度为0
  * **div-1盒子、div-2盒子**的表现形式像脱离文件流，直到触碰到float的元素。

* 当**div-1**的float属性不为left时，**div-2**的float的属性为left时，情况与上述所说的情况一相似。
  * **parent盒子**发生高度坍塌，此时高度为不浮动元素的高度。
  * **div-1盒子**与正常的div盒子显示一致。
  * **div-2盒子**的表现形式像脱离文件流，直到触碰到float的元素。
* 当**span-1**的float属性为left时，**span-2**的float的属性不为left时，情况与上述所说的情况一相似。
* 当**span-1**的float属性为left时，**span-2**的float的属性为left时，情况与上述所说的情况二相似。
* 当**span-1**的float属性不为left时，**span-2**的float的属性为left时，情况与上述所说的情况一相似。
  * **parent盒子**发生高度坍塌，此时高度为不浮动元素的高度。
  * **span-1** 因为是行内元素，所以跟span-2排列在同一行，但是**span-2**是浮动元素，所以浮动到左边，因此**span-2**的排在**span-1**前面
  * **span-2**的表现形式像脱离文件流，直到触碰到float的元素。

demo:https://lixinz.github.io/bing_basic_summary/css/float.html