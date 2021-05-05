## Explanation

In the `QueueTest` implementation we only got 2 threads which both act as consumer and producer, with both first adding data then removing. Since they both act as consumer and producer, when a thread calls `notify` to wake up another thread, the other thread is never incorrect, since they both act as consumers and producers. In the `ProdCons` scenario, it could wake up the wrong thread.

## Results

```bash
====================================================== results
no errors detected

====================================================== statistics
elapsed time:       00:00:00
states:             new=1655,visited=1789,backtracked=3444,end=62
search:             maxDepth=150,constraints=0
choice generators:  thread=1654 (signal=15,lock=190,sharedRef=980,threadApi=2,reschedule=467), data=0
heap:               new=2756,released=7242,maxLive=377,gcCycles=3442
instructions:       58548
max memory:         123MB
loaded code:        classes=65,methods=1489

====================================================== search finished: 5/5/21 10:37 AM
```
