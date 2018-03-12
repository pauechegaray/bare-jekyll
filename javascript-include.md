---
layout: page
title: JS Include

# scripts will be inserted from
# assets/js{{ page dir without extension }}/SCRIPT_FILE_NAME
scripts:
  - script.js
---

<div id="js">

## Including js in a specific page

If we want to include specific script(s) in a page, we can do the following.

For example, we create a ***javascript-include.md*** at the root of our jekyll site.

We then configure front matter to load scripts :

{% highlight yaml %}
---
...
# page front matter
# scripts will be inserted from
# assets/js{{ page.dir }}/SCRIPT_FILE_NAME
scripts:
 - script.js
---
{% endhighlight %}

As we use `permalink: pretty`, our page will be reached at ***root/javascript-include/index.html***, where `page.dir` is ***/javascript-include***.

Our script(s) will be stored in ***/assets/js{{ page.dir }}/***. If we have multiple scripts, they will be loaded in the same order they appear in our front matter.

**Note :** All scripts will loaded in the footer, just before the closing <code></body></code> element.

</div>
