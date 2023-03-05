# Watching nvidia-smi

One of the most common things as a datascientist we do is watching nvidia-smi , to look at our GPU utilization, memory etc.



Simply running nvidia-smi will give the GPU and memory utilization at a particular time only.



In order to run it across a period of time, so you don't want to repeat yourself you can use the command:

```
nvidia-smi -l 1
watch -n0.1 nvidia-smi
```



Another command to check utilization, which was recommended by Jeremy Howard is:



```
nvidia-smi dmon
```
