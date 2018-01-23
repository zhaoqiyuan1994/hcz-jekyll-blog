---
layout: post
title: Dynamic photo Wall  
categories: JavaScript
---
Dynamic Photo Wall
There is my photo wall [view][Photolink] it
What will you do if you want to create a dynamic photo wall in your website?
The way i choose is using js and html <A> tag to implement a dynamic photo wall and when you click on the photo, it will jump to the webpage you linked

You need to think what kind of data structure you use, in this case i choose array, because there are few element. if you want use that to process a database you need to consider another efficient structure, such as hash map.
Here is my full code [click][fullcode] to see full code
[fullcode]:   https://github.com/zhaoqiyuan1994/PhotoWall.github.io
[Photolink]:     http://panda1994.com/PhotoWall.github.io/

### JS code snippet

{% highlight java %}
	var photos = ['img/1.png','img/2.png','img/3.png'];
	var count = 0; //count the num of picture
	var flag; //return the action id
	function callback() //this method is main method to change the picture
	{ 
 		document.getElementById("photo").src = photos[count];
 		count++;
 	if (count == photos.length)
  		count = 0; 
	} 
	function change() //start
	{
 		flag = setInterval(callback,2000); 
	}
	function off() //if your mouse stay on the current picture it will stop
	{
 		clearInterval(flag);
	}
	function on() //when you move your mouse, keep changing the picture
	{
 		flag = setInterval(callback,2000); 
	}
	function leftMove() //move to left picture
	{
	 	document.getElementById("photo").src = photos[count];
 		count++;
 		if (count == photos.length)
  			count = 0;
	}
	function rightMove() //move to right picture
	{
 	count--;
 	document.getElementById("photo").src = photos[count];
 	if (count <= 0)
  		count = photos.length - 1;
	}
	</script>
{% endhighlight %}
