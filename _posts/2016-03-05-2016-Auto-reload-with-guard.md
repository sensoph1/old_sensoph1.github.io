---
layout: post
title:  "Live reload a page using Guard!"
date:   2016-03-05 15:45:50
categories: jekyll
---

So I am working on redoing this sites css using sassy css (scss) and in doing so i needed a way to have it auto update easier than just stopping the server and restarted. In my research i discovered a gem called guard. 

below are the gems you will need at a minimum 
{% highlight ruby %}
gem 'jekyll'
gem 'guard'
gem 'guard-jekyll-plus'
gem 'guard-livereload'
{% endhighlight %}

{% highlight ruby %}

$ bundle install
$ jekyll build

{% endhighlight %}

if you get any errors after building you might be missing a gem, add it to the gemfile and retry the bundle.

now you will need to run the following command to generate a guard file

{% highlight ruby %}
bundle exec guard init

{% endhighlight %}


once that is complete i added the following to the Guardfile

{% highlight ruby %}
guard 'jekyll-plus', :serve => true do
  watch /.*/
  ignore /^_site/
end

guard 'livereload' do
  watch /.*/
end
{% endhighlight %}

the final step i used was to add the extension to chrome using the following link.

http://livereload.com/extensions/

to run i used the following command 

{% highlight ruby %}
bundle exec guard 

{% endhighlight %}

and it began watching the current directory and in another terminal i ran this command:

{% highlight ruby %}
jekyll serve --watch

{% endhighlight %}

seems to be working nicely when i save a document, then tab over and refresh.