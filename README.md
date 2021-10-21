# performance comparison of Virtualization environments (Docker, NEMO, VBOX) with LTTNG and Trace compass tool (2019)
#httpserver has been written with Java. In 2018 I evaluated a dockerized web-application (more descriptions is in Project section) in order to compare the results with another virtual environmens (Vbox-NEMO).
#NEMO is a java virtual network emulator (has been proposed by prof Luca VELTRI) which its codes exist in github.

# STEPS

1-run the httpserver codes (which has been uploaded in java copy) on ECLIPS and export it as a jar file (Httpserver9090.jar).

Note1: I put some computatins (e.g. calculating random integers) to increase CPU loads on the httpserver.
Note2: the name of the image should be exactly

A-as Httpserver9090.jar
B- also in the program mentiond folder (jar) unless it doesn't work

2-buid the container. 
3-now the httpserver is built and run on top of Docker.
4-by using lttng+tracecompass you are able to compare CPU and memory(RAM) on your PC in this scenario.
5-then you have to run httpserver on top of Vbox and again using lttng+tracecompass write the results.
6-run httpserver on top of NEMO and write the results. 
7-we also compare the cpu and memory for Linux Mint.

in case of memory usage:
vbox :400 mb
Docker 30 mb
Nemo 20mb

in case of CPU usage:
vbox 97%
Docker 16%
Nemo 38%

you can see that memory  in NEMO is better than: Docker and Vbox
in CPU scenario NEMO is better than: Vbox and Linux mint
