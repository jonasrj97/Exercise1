# Reasons for concurrency and parallelism


To complete this exercise you will have to use git. Create one or several commits that adds answers to the following questions and push it to a repository to complete the task. Remember to also submit your answers to Blackboard

When answering the questions, remember to use all the resources at your disposal. Asking the internet isn't a form of "cheating", it's a way of learning.

 ### What is concurrency? What is parallelism? What's the difference?
 > *Concurrency is when multiple tasks can be started, run or excecuted at the same time. But there is not progress on more than one task at a time, although several tasks can be somewhere between started and finished. Parallelism is when several tasks are progressing at the same time. This is typically the case when a computer has more than one CPUs. So the difference is that parallelism is when progress is done on more than one task at the time, while concurrency cannot.*
 
 ### Why have machines become increasingly multicore in the past decade?
 > *Computers with multiple cores can excecute complex tasks/programs much faster than singecored computers. New technology developed the past decade has made the physical size of the cores smaller and cheaper, as well as better pipelining and architectures. One major reason it that the clock speed has reached a limit, so to increase run time more cores need to be implemented.*
 
 ### What kinds of problems motivates the need for concurrent execution?
 (Or phrased differently: What problems do concurrency help in solving?)
 > *Concurrency is efficient when mulitple users are on a website, when a user is requiring several commands the computer can excecute several tasks in the background, and when tasks or substasks need to be excecuted remotely for instance on different servers.*
 
 ### Does creating concurrent programs make the programmer's life easier? Harder? Maybe both?
 (Come back to this after you have worked on part 4 of this exercise)
 > *Creating concurrent programs is much more intricate than sequential ones, but after mastering it is could be easier. Concurrent programming is important for many reasons, and is a necessity in modern programming. So when working with advanced programming in new technology, concurrency is vital.*
 
 ### What are the differences between processes, threads, green threads, and coroutines?
 > *Processes have their own memory space, which means that they do not share memory directly. Threads do not have their own memory locations, so multiple threads can work on the same memory locations. This implies that one thread can affect other threads when running. Processes can be associated as a virtual computer, and threads as virtual cores. Green threads are run by other mechanisms than the OS, for instance by program scripts. Coroutines are similar to threads, but they do not use parallelism, but they use concurrency. Coroutines may be controlled by other instances than the OS.*
 
 ### Which one of these do `pthread_create()` (C/POSIX), `threading.Thread()` (Python), `go` (Go) create?
 > *Green threads.*
 
 ### How does pythons Global Interpreter Lock (GIL) influence the way a python Thread behaves?
 > *GIl is manipulating the execution of threads so that only one native thread can execute at a clock cycle.*
 
 ### With this in mind: What is the workaround for the GIL (Hint: it's another module)?
 > *When using GIL, the parallelism of the program could be worsened considerably, especially when containing numerous threads.*
 
 ### What does `func GOMAXPROCS(n int) int` change? 
 > *It sets the number of CPUs that can execute simultaneously, and returns the prevoius setting (an integer).*
