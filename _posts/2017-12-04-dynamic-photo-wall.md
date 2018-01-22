---
layout: post
title: Example content for posts  
categories: JavaScript
---
<h1>Dynamic Photo Wall</p>

<p>What will you do if you want to create a dynamic photo wall in your website?
The way i choose is using js and html "<A>" tag to implement a dynamic photo wall and when you click on the photo, it will jump to the webpage you linked</p>

<p>Firstly you need to think what kind of data structure you use, in this case i choose array, because there are few element. if you want use that to process a database you need to consider another efficient structure, such as hash map</p>
<h2>Js Code</h2>

<pre><code><script type="text/javascript">
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
</code></pre>

<h3>HTML code</h3>
<p>if you want when ever you click your picture, the webpage will jump to a current page,you need to do that</p>
<pre><code>
<a href=#target url target="view_window">
   <img id="photo" here is your java script>
</a>
</code></pre>


### Code snippet

{% highlight python %}
if __name__ =='__main__':
    img_thread = threading.Thread(target=downloadWallpaper)
    img_thread.start()
    st = '\rDownloading Image'
    current = 1
    while img_thread.is_alive():
        sys.stdout.write(st+'.'*((current)%5))
        current=current+1
        time.sleep(0.3)
    img_thread.join()
    print('\nImage of the day downloaded.')
{% endhighlight %}
