Download Link: https://assignmentchef.com/product/solved-assignment-2-cpu-scheduling-simulation-csc-139-operating-system-principles-objectives
<br>
This programming project is to simulate a few CPU scheduling policies discussed in the class. You will write a C program to implement a simulator with different scheduling algorithms. The simulator selects a task to run from ready queue based on the scheduling algorithm. Since the project intends to simulate a CPU scheduler, so it does not require any actual process creation or execution. When a task is scheduled, the simulator will simply print out what task is selected to run at a time. It outputs the way similar to Gantt chart style.

<h1>1          Description</h1>

The selected scheduling algorithms to implement in this project are 1) First Come First Serve (FCFS), 2) Round Robin (RR), and 3) Shortest Remaining Time First (SRTF). The detailed algorithms are already described in class slides and textbook Chapter 5.

2.1     Task Information

The task information will be read from an input file. The format is pid arrivaltime bursttime

All of fields are integer type where pid is a unique numeric process ID

arrivaltime is the time when the task arrives in the unit of milliseconds bursttime the is the CPU time requested by a task, in the unit of milliseconds

The time unit for arrivaltime, bursttime and interval is millisecond.

2.2      Command-line Usage and Examples

Usage: proj2 inputfile [FCFS|RR|SRTF] [timequantum]

where inputfile is the file name with task information. FCFS, RR, and SRTF are names of scheduling algorithms. The time quantum only applies to RR. FCFS is nonpreemptive, while RR and SRTF are all preemptive. The last argument is needed only for RR. (See following table for more examples)

<table width="0">

 <tbody>

  <tr>

   <td width="205">Examples</td>

   <td width="394">Description</td>

  </tr>

  <tr>

   <td width="205">proj2 input.1 FCFS</td>

   <td width="394">FCFS scheduling with the data file “input.1”</td>

  </tr>

  <tr>

   <td width="205">proj2 input.1 RR 2</td>

   <td width="394">Simulate RR scheduling with time quantum 2 milliseconds (4th parameter is required even for quantum 1 millisecond) with the data file “input.1”</td>

  </tr>

  <tr>

   <td width="205">proj2 input.1 SRTF</td>

   <td width="394">Simulate SRTF scheduling with the data file “input.1”</td>

  </tr>

 </tbody>

</table>

2.3      Sample Inputs and Outputs

Sample input files and expected outputs are shown in Appendix. You can use it to verify your results.

<h1>2          Requirements</h1>

The project requires to simulate FCFS, RR, and SRTF scheduling for given tasks and to compute the average waiting time, response time, turnaround time and overall CPU usage. You can find their definitions in textbook.

<ol>

 <li>Implement scheduling algorithm for FCFS, RR, and SRTF. The program should schedule tasks and print progress of task every unit time (millisecond) as shown in sample outputs.</li>

 <li>Print statistical information. As soon as all tasks are completed, the program should compute and print 1) average waiting time, 2) average response time, 3) average turnaround time and 4) overall CPU usage.</li>

</ol>

Note: if you use static array to implement ready queue structure, you can assume the maximum queue length is 20.

<h1>3          Suggested Methodology</h1>

<ol>

 <li>Implement one scheduling algorithm at each step</li>

 <li>You can use circular linked list as a queue structure</li>

 <li>You can use a data structure similar to PCB for each task, though it will be much simpler</li>

</ol>

<h1>4          Deliverables</h1>

Make sure your code can be compiled and work on Athena server correctly. Upload to Canvas the following: • All source codes/files that you have added/modified and the demonstrative results.

<ul>

 <li>A README.TXT file that briefly describes each file, how to compile the file(s), and how to run the file.</li>

 <li>These files should be placed in a directory called &lt;ECS username&gt;-asgmt2.</li>

 <li>Use tar command to place all the files in a single file called &lt;ECS username&gt;-asgmt2.tar.</li>

</ul>

Assuming you are in the directory &lt;ECS username&gt;-asgmt2 do the following:

<ul>

 <li>Goto the parent directory: cd ..</li>

 <li>tar the files:</li>

</ul>

tar -cvf &lt;ECS username&gt;-asgmt2.tar ./&lt;ECS username&gt;-asgmt2

<ul>

 <li>Verify the files have been placed in a tar file:</li>

</ul>

tar -tvf &lt;ECS username&gt;-asgmt2.tar

<ul>

 <li>Compress the files using gzip: gzip &lt;ECS username&gt;-asgmt2.tar</li>

 <li>Verify that the gzipped file exists: ls &lt;ECS username&gt;-asgmt2.tar.gz</li>

</ul>