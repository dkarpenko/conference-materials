## Event
* Date: 2015.09.28
* Location: Minsk, Belarus
* Website: [jetconf.by](http://jetconf.by/)

## Program
* [Java byte code in practice by Rafael Winterhalter](#java-byte-code-in-practice-by-rafael-winterhalter)
* [An introduction to JVM performance by Rafael Winterhalter](#an-introduction-to-jvm-performance-by-rafael-winterhalter)
* [Scala performance for those who doubt by Roman Grebennikov](#scala-performance-for-those-who-doubt-by-roman-grebennikov)
* [Atomics, CAS, and Nonblocking Algorithms by Alexey Fyodorov]("#atomics-cas-and-nonblocking-algorithms-by-alexey-fyodorov)
* [Domain-specific Hotspot Optimization with Scalan by Alexander Slesarenko](#domain-specific-hotspot-optimization-with-scalan-by-alexander-slesarenko)
* [Do we need Unsafe in Java? by Andrei Pangin](#do-we-need-unsafe-in-java-by-andrei-pangin)
* [How "final" is final? by Volker Simonis](#how-final-is-final-by-volker-simonis)


### Java byte code in practice by Rafael Winterhalter
#### Brief
```
At first glance, Java byte code can appear to be some low level magic that is both hard to understand and effectively irrelevant to application developers. However, neither is true. With only little practice, Java byte code becomes easy to read and can give true insights into the functioning of a Java program. In this talk, we will cast light on compiled Java code and its interplay with the Java virtual machine. In the process, we will look into the evolution of byte code over the recent major releases with features such as dynamic method invocation which is the basis to Java 8 lambda expressions. Finally, we will learn about tools for the run time generation of Java classes and how these tools are used to build modern frameworks and libraries. Among those tools, I present [Byte Buddy](http://bytebuddy.net/), an open source tool of my own efforts and an attempt to considerably simplify run time code generation in Java.
```
#### Materials
* [Slides](http://www.slideshare.net/RafaelWinterhalter/java-byte-code-in-practice)
* [2015.05.20 Screencast from vJUG](https://youtu.be/5cNyrkjJ5KY?t=5m4s)
* [2014.09.09-11 Understanding Java byte code](https://vimeo.com/105869193)

### An introduction to JVM performance by Rafael Winterhalter
#### Brief
```
Writing software for a virtual machine allows developers to forget about machine code assembly, interrupts and processor caches. This makes Java a convenient language, but all too many developers see the JVM as a black box and are often unsure of how to optimize their code for performance. This unfortunately adds credence to the myth that Java is always outperformed by native languages. In this talk we'll take a peek at the inner workings of the HotSpot Virtual Machine, its Just-In-Time Compiler and the interplay with a computer's hardware. From this, we will understand the more common optimizations that a virtual machine applies to be better equipped to improve and to reason about a Java program's performance, and how to correctly measure runtime!
```
#### Materials
* [Slides](http://www.slideshare.net/RafaelWinterhalter/an-introduction-to-jvm-performance)
* 

### Scala performance for those who doubt by Roman Grebennikov
#### Brief
```
Scala language has a lot of nifty features like pattern matching, recursion, collections with lambdas and other things from functional programming world. And all these features are combined together in a way that makes programming happier. 
But all these dreams about FP magic can be easily destroyed by the fact, that "when I rewrote all my spaghetti Java code to a Scala one-liner, why did it become three times slower?". Brutal reality hints us that all these modern high-level abstractions may hide monsters inside and a comfort you get by using them has it's own price. And if you develop something more complex than a simple CRUD application and it's even slightly connected with performance, you must clearly understand how do all these "monads" behave. 
This talk will tell you about magic performed by scala compiler, will show you a couple of horror stories about scala performance with explanations and solutions:
JMH and how to use it with Scala.
What happens when you hit 'compile' button.
Pattern-matching, tail recursion and collections under the hood.
How HotSpot optimises your code.
Parental advisory: 18+, explicit x86_64 assembly inside.
```
#### Materials
* [Slides/ Javapoint 2015/ Scala performance под капотом](http://www.slideshare.net/Shutty/scala-performance)
* [Video/ Scala User Group Voronezh/ Scala performance для сомневающихся](https://www.youtube.com/watch?v=vRdgK07exM4)
 
### Atomics, CAS, and Nonblocking Algorithms by Alexey Fyodorov
#### Brief
```
This updated talk will dive you into disadvantages of locking, CAS operations, Java atomic variable classes and a couple of nonblocking algorithms: nonblocking stack and nonblocking queue. We will also talk about ABA problem. The talk is based on JCIP (§15) and TAoMP (§§ 5, 7, 10, 11). It will be interesting for Java programmers who have heard about CAS and lock-free, but who have no experience in writing non-blocking code.
```
#### Materials
* [Slides/ JEEConf 2015/ Atomics, CAS and Nonblocking algorithms](http://www.slideshare.net/23derevo/fyodorov-atomics)
* [Video/ JEEConf 2015/ Atomics, CAS and Nonblocking algorithms](https://www.youtube.com/watch?v=htbPckvO2zQ)

### Domain-specific Hotspot Optimization with Scalan by Alexander Slesarenko
#### Brief
```
While high-level abstractions greatly simplify program development, they ultimately need to be eliminated to produce high-performance code. 
I will present Scalan, a framework which enables compilation of high-level object-oriented-functional code in Scala into high-performance low-level code. 
Using simple examples we will look at compilation pipeline of Scalan in action. We start from DSL embedding, then discuss transformation and specialization techniques based on staged evaluation, then generation of efficient imperative code using Lightweight Modular Staging framework and finally performance evaluation and speedups.
```
#### Materials
* [Video/ ICFP 2015](https://www.youtube.com/watch?v=eZ2gDvjOujA)
* [ACM DL/ Scalan: a framework for domain-specific hotspot optimization](http://dl.acm.org/citation.cfm?id=2814203)
* [scalan](https://github.com/scalan/scalan)

### Do we need Unsafe in Java? by Andrei Pangin
#### Brief
```
Java platform is highly appreciated for its security features: type safety, bounds checking, access control, automatic memory management, etc. The Virtual Machine provides a managed environment to guard applications from typical run-time problems. Today, however, more and more developers opt to break the barrier and escape from JVM sandbox. There is hardly a Senior Java developer who has never heard of sun.misc.Unsafe. Though it has always been a private API intended for JDK internal use only, the popularity of Unsafe has grown too fast, and now it is used in many open-source projects. OK.RU is not an exception: its software also heavily relies on Unsafe APIs. 
During this session we'll try to understand what is so attractive about Unsafe. Why do people keep using it regardless the warnings of removal from future JDK releases? Are there any safe alternatives to private API or is it absolutely vital? We will review the typical cases when Java developers prefer to go unsafe and discuss major benefits and the drawbacks of it. The report will be supported by the real examples from OK.RU experience.
```
#### Materials
* 

### How "final" is final? by Volker Simonis
#### Brief 
```
Altough the concept of "final" fields is quite simple, its implementation in Java can lead to surprising effects. First of all, the Java VM and Java language have a slightly different understanding of "final". Second (and unfortunately) declaring a field as final doesn't mean that the VM or the programmer can really rely on its immutability. 
This talk will show the differnt aspects of "finality" and their impact on the Java compiler and the Java VM. It will demonstrate how finality can be circumvented in Java with the help of reflection or sun.misc.Unsafe. And finally it will discuss the impacts this has on the optimzations done by the JIT compiler.
```
#### Materials


## Speakers
### Alexander Slesarenko
#### Bio
```
Alexander is a principal engineer at Huawei Research Center in Moscow. He is leading the Scalan project - a framework for creating high-performance DSLs in Scala. He also worked in the IT industry as software architect for several years.
```
#### Links
* [pat.keldysh.ru/~slesarenko/](http://pat.keldysh.ru/~slesarenko/)


### Rafael Winterhalter
#### Bio
```
Rafael works as a software engineer in Oslo, Norway. He is a proponent of static typing and a JVM enthusiast with particular interests in code instrumentation, concurrency and functional programming. Rafael blogs about software development, regularly presents at conferences and was pronounced a Java One Rock Star. When coding outside of his work place, he contributes to a wide range of open source projects and often works on Byte Buddy, a library for simple runtime code generation for the Java virtual machine.
```
#### Links
* [twitter/rafaelcodes](https://twitter.com/rafaelcodes)
* [github/raphw](https://github.com/raphw)
* [rafael.codes](http://rafael.codes/)
* [lanyrd.com/rafaelwth](http://lanyrd.com/profile/rafaelwth/)

### Roman Grebennikov
#### Bio
```
Co-founder and distributed systems developer in Sociohub, activist of Voronezh Scala User Group. Went a long professional way from a graphics designer and C++ HFT developer to a Scala fanboy.
```
#### Links
* [twitter/public_void_grv](https://twitter.com/public_void_grv)
* [github/romangrebennikov](https://github.com/romangrebennikov)

### Alexey Fyodorov
#### Bio
```
Java developer for 8+ years. Worked for Oracle for 3 years (JCK Team, Java Platform group). Leader of the St. Petersburg Java User Group, and CodeFreeze community, organizer of Russian Java conferences JPoint and Joker. Interested in Java runtime, multithreaded programming, Java compatibility and software engineering trade-offs. Since 2015 Technology Evangelist at Odnoklassniki.
```
#### Links
* [twitter/23derevo](https://twitter.com/23derevo)
* [about.me/alexey.fyodorov](https://about.me/alexey.fyodorov)


### Andrei Pangin
#### Bio
```
Andrei is a lead software engineer at Mail.Ru Group. In efforts to build a fast and reliable platform for OK.RU social network he squeezes every cycle out of the Java server performance. Andrei's past experience at Sun Microsystems helps him to investigate Java Virtual Machine bugs and even to patch OpenJDK. He knows no limits in hacking Java and playing with undocumented APIs. These experiments are reflected in Andrei's presentations on Java internals. They’ve also inspired the project “one-nio” - the open-source framework for developing high-loaded servers in Java.
```
#### Links

### Volker Simonis
#### Bio
```
Volker works for SAP in the SAP JVM Technology group. OpenJDK contributor from the very beginning and helped SAP and the SAP JVM team engage in the OpenJDK project. Project lead of the OpenJDK PowerPC/AIX porting project, a JDK8 committer and JDK9 reviewer.
```
#### Links
* [Volker Simonis](http://www.progdoc.de/)
* [How to Contribute to the OpenJDK](http://www.progdoc.de/papers/EclipseCon2011/EclipseCon2011.html)
* [Video/ 2014.10.20-21/ Heart Surgery: HotSpot Debugging at the OS Level](https://www.youtube.com/watch?v=JZpEskA_89U)
* [Video/ Jeeconf 2015/ Packed Objects, Object Layout & Value Types — a Survey ](https://www.youtube.com/watch?v=JZpEskA_89U)