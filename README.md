# MP1_SE4367.001_EJB180000_Evan_Branco
MP1 Project Repository

Eva Branco, EJB180000
For class SE 4367.001

I apologize if the repository is less concise and messier than u would perfer, I'm only just now learn EGit, and I appear to have broken some of my dependencies during the process. Notheless! Errors that did not make in into the code available in this reposity.

The project was large and complicated, and it may be helpful to you to include a review of what files were editied, and what my results were.

Section 1: 
Deliverables: DominatorFinder.java

This was the most difficult section of the project for me, as I was completely caught off guard. DominatorFinder.java, as given, runs, and seems to perform its analysis correctly. My file contains several large comment strings, where, in an attempt to gather extra points, I communicated my current level of understanding and present several options as to why I was having such trouble. 

Section 2:
Deliverables: TestSootCallGraph.java, Part2.txt

Section 2 was quite simple, since it required only an understanding of Call Grpahing methods, which was described in great detail in the given spark paper. I slightly modified the given Test class to determine the runtime in nanoseconds, but made no other changes. Most of the points from this section will come from Part2.txt, my analysis of the data and my explination of the two algorihm's pros and cons.

Section 3:
Deliverables: Part3_A.png, Part3_B.png, TestSootLoggingHeap.java

Section 3 was split into two different exercises, the first of which only required me to follow the given directions. I included my execution of Example.java in Part3_A.png, though it is certainly not needed.

The second activiy, however, required much more effort and thought. I spend many hours reading soot documentation and aquired code that works. I was eventually able to locate a path to aquire of the nessesary data for the Log calls, but the isWrite boolean. I was unable to find a clean and consise call selection like with the rest, and I ultimately decieded that my best option was to simply parse jimmple manually. This is an unacceptable solution, as it likely will not fucntion with jimple statements whos formatting is unlike the statements aquired from HelloThread.java. If there are jimple statements that do not conform to the exact formatting I saw, the program would fail. Another pet peeve was the naming of the Thread groups and threads themselves. No matter how often I ran the program, I was never able to ses one of the threads named main. In addition, instead of Thread[Thread-0,5,main], my thread groups appeared as Thread[Thread-#,5,Soot ThreadGroup]. My output never perfectly matched those of the example, but I'm hoping thats just the nature of threads. Difficult to predict and hard to organize.

The Part3_B.png is a png of my output in eclipse, but the same output is also coppied below:

Thread Thread-7 wrote static field <HelloThread: int x>
Thread Thread-8 wrote static field <HelloThread: int x>
Thread Thread-8 wrote instance field <HelloThread$TestThread: int y> of object Thread[Thread-8,5,Soot Threadgroup]
Thread Thread-8 read instance field <HelloThread$TestThread: int y> of object Thread[Thread-8,5,Soot Threadgroup]
Thread Thread-7 read instance field <HelloThread$TestThread: int y> of object Thread[Thread-7,5,Soot Threadgroup]
Thread Thread-7 read static field <HelloThread: int x>
Thread Thread-7 read static field <java.lang.System: java.io.PrintStream out>
