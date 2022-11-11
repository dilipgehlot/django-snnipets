# django-snnipets
Some helpful code snippets...

1. Decorator  to for custom autherization.


from django.http import HttpResponse

def module_allowed(module_name):
    def decorator(func):
           def wrap(request,*args,**kwargs):
                if Condtion:  Here Condtion check for the autherization                         
                        return func(request,*args,**kwargs)  
                else:   
                        Handle the request by redirecting or django's permissio denied exeption 
                        return HttpResponse("⚠ You are not authorized to view this page !")
        return wrap
    return decorator



Add decorator on funtions

from ...py import module_allowed

@module_allowed('Reports')
def some_function(request):
    .....
 
 
 
 

