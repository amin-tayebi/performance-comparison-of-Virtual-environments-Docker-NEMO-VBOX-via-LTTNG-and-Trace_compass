# performance comparison of Virtual environments (Docker, NEMO , VBOX) with LTTNG and Trace compass tool (2019)
#httpserver has been written with Java. In 2018 we evaluated a dockerized web-application to compare the results with another virtual environmens (Vbox-NEMO).
#NEMO is a java virtual network emulator based on JVM (has been proposed by prof Luca VELTRI) which its source codes and description exists freely HERE https://netsec.unipr.it/project/nemo.

# STEPS

1-run the httpserver codes (which has been uploaded in java copy) on ECLIPS and export it as a jar file (Httpserver9090.jar).

Note1: We put some computations (e.g. calculating random integers) to increase CPU loads on the httpserver.
Note2: the name of the image should be exactly:

A-as Httpserver9090.jar
B-also in the program mentiond folder (jar) unless it doesn't work

2-buiding related container. 
3-now the httpserver is built and run on top of Docker.
4-by using lttng+tracecompass you are able to compare CPU and memory(RAM) on your PC in this scenario.
5-then you have to run httpserver on top of Vbox and again using lttng+tracecompass write the results.
6-run httpserver on top of NEMO and write the results. 
7-we also compare the cpu and memory for Linux Mint.

In case of memory usage:
vbox :400 mb
Docker 30 mb
Nemo 20mb

In case of CPU usage:
vbox 97%
Docker 16%
Nemo 38%

you can see that memory  in NEMO is better than: Docker and Vbox
in CPU scenario NEMO is better than: Vbox and Linux mint

In another words

# CPU performance 
Virtual Box CPU usage analyze shows 230% out of 800% with the same Hardware and scenario

NEMO CPU usage analyze shows 38% out of 800% with the same Hardware and scenario

DOCKER CPU usage analyze shows 16.5% out of 800% with the same Hardware and scenario

# Memory performance 
Virtual Box memory usage analyze shows 394.8 MB with the same Hardware and scenario

Nemo memory usage analyze shows 19.3 MB with the same Hardware and scenario

DOCKER memory usage analyze shows 27.5 MB with the same Hardware and scenario
