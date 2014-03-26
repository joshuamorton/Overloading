#On Code Golf and Function Decorators
###Or: Implementing Method Overloading in Python

(Full disclosure, I'm writing this at 3 AM, pardon any errors)

To start, a brief overview of function decorators, since this will delve heavily into them:

    def decorator(function):
        #create a closure 
        def newFunc(): #note that newFunc still has access to the function variable
            print "stuff before"
            function()
            print "stuff after"
        return newFunc

    @decorator
    def ello():
        print "hello world"

    ello() #->

    #stuff before
    #hello world
    #stuff after

