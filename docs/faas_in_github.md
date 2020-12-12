# GitHub Actions as FaaS 

FaaS is a fancy term in the world of cloud computing. FaaS stands for *Function as a Service*. This is the next generation of SaaS, which stands for *Software as a Service*. While in SaaS one has to specify the infrastructure that is required for funning a Software and then a cloud provider will go an find a suitable spot for running that software in the form of a virtual machine. Software developers needed to understand a lot about how a piece of code has to be connected to the Internet and how data is handled. To be honest these functions is pretty standard for most platforms based on JavaScript, Python, PHP, Perl, R or any of the other programming language. Basically the part of making something available on the Internet is pretty repetetive. One of the many challenges in this scenario is that in an SaaS environment our business logic hangs around and waits for potential requests - even if there are very few incoming requests and our software is idle most of the time. 

FaaS now goes a step further and abstracts the infrastructure and strips the standard parts of a software away from our functions. So software developers can focus more thoroughly on the actual business logic that makes their code special. That means that we don't really bother of how software connects to the internet and how data arrives at our function. Instead with FaaS the cloud provider handles the standard processes and just passes the data into our code, without us having to know much of the nitty gritty details of HTTP, REST, gPRC, graphQL or even SOAP. We can think of FaaS as a way to simplify our software by committing to standards for connecting our business logic to the internet.

At the core a *function* in FaaS is a sequence of commands that will be executed everytime this is needed. Normally we declare what our funciton can handle. Based on this declaration, the cloud service decides when it has to run our function. In the meantime our function is not present. If there is something for our function to do, our cloud provider will get our function going. This solves the problem if our software is not doing much most of the time.

## GitHub Actions

GitHub Actions is a feature of GitHub repositories. It allows repository owners to define functions that run automatically if something happens in our repositories.

We can think of GitHub actions as a special form of FaaS. 
