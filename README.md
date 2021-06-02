# R-Flow

R-Flow is a software product that uses R / Python to analyze data in a workflow. 
R-Flow can automatically perform R / Python analysis by selecting only the R / Python function Task icon without RScript  / Python Script creation. It also defines and reuses all steps from data entry to output into a single workflow and provides a readily available model for statistics, machine learning and optimization. R-Flow provides a visualization function of the results of the Analytics Model as an Analytic Report. 

R-Flow offers Personal and Enterprise versions. 

1. Personal: Installed/run on a personal PC.

   Requirements 

   Windows 7 Over (64 bit)

   R 3.6 Over

   Python 3.6 Over

2. Enterprise: Install the R-Flow server module on Linux and use it by connecting to the Linux server from the client (Windows). The server module is provided as a Docker image. 

   Requirements

   Linux (Centos, Ubuntu)

   Docker 



Enterprise R-Flow Installation Guide (It is recommended to install with the root account during installation.)

​	**Download Docker Image**

​		docker push hwasumok/r-flow:latest

​	**Docker Run**

​		docker run -it \
​              --hostname r-flow \
​              --name r-flow \
​              -p 9081:8080 -p 6311:6311 -p 3307:3306 \
​              --privileged \
​              -e container=docker \
​              -v /sys/fs/cgroup:/sys/fs/cgroup:ro \
​              hwasumok/r-flow:latest \
​              bash

​	**Docker attacch**

​		docker attach r-flow

​	**Docker r-flow exec.**	

​		/root/r.flow.folder/r.flow.sh

​	**Download R-Flow Client and Install.** **(\* Assume that the server address is 10.10.10.10. )**

​		Access http://10.10.10.10/r.flow.ui/pub/publish.html in a web browser.  

​		Click the Install button to download and install the R-Flow client program. 

​	**R-Flow server connection **

​		Run the installed R-Flow. When running for the first time, a window for entering the R-Flow server address appears.

​		Enter the server address as follows http://10.10.10.10/r.flow.ui/pub and click the OK button.

​		When the Login window appears, the system account ID and password are as follows. 

​		admin/sysadmin

