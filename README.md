Description
There are modules for getting OS metrics on systems running the Linux kernel. 

Basic stats for major subsystems are provided (Processor/CPU, Memory).

Example Usage
print number of processes running:

from linux_metrics import cpu_stat

print cpu_stat.procs_running()
print CPU utilization every 5 secs:

>>> from linux_metrics import cpu_stat
>>>
>>> while True:
...     cpu_pcts = cpu_stat.cpu_percents(5)
...     print 'cpu utilization: %.2f%%' % (100 - cpu_pcts['idle'])
...
cpu utilization: 0.70%
cpu utilization: 0.50%
cpu utilization: 24.80%
cpu utilization: 20.89%
cpu utilization: 40.04%