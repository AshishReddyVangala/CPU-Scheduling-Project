CPU Scheduling Simulator

Project Overview:
This project is a C++ CPU scheduling simulator developed as part of the CS30200 OPERATING SYSTEMS course at Purdue University, Spring 2024. 
The simulator models the execution of both real-time and interactive processes, handling various resource requests such as CPU time, disk reads, and terminal (TTY) accesses. 
The goal of the simulator is to prioritize real-time processes to meet their deadlines, implement preemptive scheduling, and provide a detailed summary report showcasing key metrics from the simulation.

Features:
Process Management: The simulator manages both real-time and interactive processes, each with distinct scheduling needs.
Resource Handling: Processes can request multiple resources such as CPU, Disk, and TTY, which are handled according to their types and scheduling requirements.
Preemptive Scheduling: Real-time processes are prioritized to ensure deadlines are met, with a preemptive approach taken when necessary.
Simulation Metrics: The simulator provides a detailed summary report at the end of the simulation, including metrics like CPU utilization, disk access statistics, and the number of processes that completed or missed deadlines.

How It Works:
Input Handling: The simulator reads process information and resource requests from a predefined input format. The input includes process types (REAL-TIME or INTERACTIVE), arrival times, deadlines for real-time processes, and resource requests.
Process Execution: The simulator selects processes based on their arrival times and types, with real-time processes taking priority. It processes each resource request, updating the simulation time accordingly.
Requeueing: Processes with multiple resource requests are requeued with updated arrival times, ensuring they are scheduled correctly in subsequent simulation cycles.
Summary Report: After all processes have been executed, the simulator prints a summary report detailing:
Number of real-time and interactive processes completed.
Percentage of real-time processes that missed their deadlines.
Total number of disk accesses and average disk access duration.
CPU and disk utilization percentages.
File Structure

main.cpp: The main C++ source file containing the CPU scheduling simulator.
input.txt (optional): An input file containing the list of processes and their resource requests. The format should match the expected input structure used by the simulator.
Input Format:
The input file should list processes and their resource requests in the following format:
Process Type: Either REAL-TIME or INTERACTIVE, followed by the process's arrival time.
Deadline (for real-time processes): The deadline time for completing the process.
Resource Requests: List of resources requested by the process, along with the time needed for each resource.

Example:
REAL-TIME 100
DEADLINE 200
CPU 50
DISK 30
INTERACTIVE 150
CPU 100

How to Run
Set Up: Ensure you have a C++ compiler installed on your system.
Compile the source code using a C++ compiler:
g++ main.cpp -o cpusim
Run the compiled simulator:
./cpusim < input.txt
The simulator will output the process execution details and print a summary report at the end of the simulation.

Summary Report:
The summary report includes the following metrics:
Number of real-time processes completed.
Percentage of real-time processes that missed their deadlines.
Number of interactive processes completed.
Total number of disk accesses.
Average disk access duration.
Total simulation time elapsed.
CPU and disk utilization percentages.
