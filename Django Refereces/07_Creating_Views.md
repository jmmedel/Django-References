Django - Creating Views
Advertisements
 Previous Page Next Page  
A view function, or “view” for short, is simply a Python function that takes a web request and returns a web response. This response can be the HTML contents of a Web page, or a redirect, or a 404 error, or an XML document, or an image, etc. Example: You use view to create web pages, note that you need to associate a view to a URL to see it as a web page.

In Django, views have to be created in the app views.py file.

Simple View
We will create a simple view in myapp to say "welcome to my app!"

See the following view −

from django.http import HttpResponse

def hello(request):
   text = """<h1>welcome to my app !</h1>"""
   return HttpResponse(text)
In this view, we use HttpResponse to render the HTML (as you have probably noticed we have the HTML hard coded in the view). To see this view as a page we just need to map it to a URL (this will be discussed in an upcoming chapter).

We used HttpResponse to render the HTML in the view before. This is not the best way to render pages. Django supports the MVT pattern so to make the precedent view, Django - MVT like, we will need −

A template: myapp/templates/hello.html

And now our view will look like −

from django.shortcuts import render

def hello(request):
   return render(request, "myapp/template/hello.html", {})
Views can also accept parameters −

from django.http import HttpResponse

def hello(request, number):
   text = "<h1>welcome to my app number %s!</h1>"% number
   return HttpResponse(text)
When linked to a URL, the page will display the number passed as a parameter. Note that the parameters will be passed via the URL (discussed in the next chapter).