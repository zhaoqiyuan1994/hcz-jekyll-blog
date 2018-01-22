---
layout: post
title: Example content for posts  
categories: others
---
<h1>Dynamic Photo Wall</p>

<p>What will you do if you want to create a dynamic photo wall in your website?
The way i choose is using js and html "<A>" tag to implement a dynamic photo wall and when you click on the photo, it will jump to the webpage you linked</p>

<p>Firstly you need to think what kind of data structure you use, in this case i choose array, because there are few element. if you want use that to process a database you need to consider another efficient structure, such as hash map</p>
<h2>Js Code</h2>

<pre><code>tell application "Foo"
    beep
end tell
</code></pre>

<p>This is an <a href="#">example link</a>.</p>

<p>I start my morning with a cup of coffee and
<a href="http://www.nytimes.com/">The New York Times</a>.</p>

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
