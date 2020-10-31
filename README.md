# gazebo_on_kubernetes
Running Gazebo on kubernetes cluster

## The Work is still in progress 

For trying the deployment you should have a working kubernetes cluster and kubectl installed.

```bash
    # First clone the repository
    git clone https://github.com/kapilPython/gazebo_on_kubernetes.git
    # then run
    kubectl create -f gazebo_on_kubernetes
```
Note:- *gzweb is unable to communicate with the gazebo server on startup but if you go inside the pod and run gzweb again on a different port it works fine*

To try and run gzweb inside container again

```bash
    kubectl exec -it gazebo-client bash
    npm start # this will start gzweb on port 8080 which can be accesed with a web browser.
```

***
*Inspiration*

[icclab/ros_on_kubernetes](https://github.com/icclab/ros_on_kubernetes)

[Article](https://blog.zhaw.ch/icclab/challenges-with-running-ros-on-kubernetes/) This blog talks about challenges for running ros on kubernetes cluster and the same challenges remain for gzserver and gzclient/gzweb communication.
