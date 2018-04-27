## Short Answer Questions

Add your answers inline, below, with your pull request.

1. List all of the main states a process may be in at any point in time on a
   standard Unix system. Briefly explain what each of these states mean.
  * **Running:** The process is active, receiving system resources, and serving its requests.
  * **Suspended:** The process is waiting to be allocated resources to run.
  * **Stopped:** The process has been halted, and lets the parent know that it has been terminated.
  * **Zombie:** The process has been terminated, but not reaped by it's parent (or cannot be reaped because its parent is already dead, leaving it stuck in a zombie state).

2. What is a Zombie Process? How does it get created? How does it get destroyed?
  * A zombie process occurs when a process informs it's parent that it is exiting, in the time between the process informing the parent, and the parent cleaning up the process, it is a zombie process. A process can get stuck in this state if the parent died before releasing any child processes.

3. Describe the job of the Scheduler in the OS in general.
  * The scheduler makes sure that processes receive processing time, which can be accomplished in a variety of ways, some more efficient than others.

4. Describe the benefits of the MLFQ over a plain Round-Robin scheduler.
  * In a simple RR scheduler, a process can issue an I/O just before a time slice ends and dominate CPU time, whereas a better-implemented MLFQ will reduce the priority of a process after it's used up its time allotment.