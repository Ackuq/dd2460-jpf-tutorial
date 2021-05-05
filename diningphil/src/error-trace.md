
## Error Trace of Dining Philosophers







| Thread name and id   | main      | thread-1  |  thread-2  |   thread-3  |   thread-4  | thread-5  |
| ------------- |---------------| ------| ------| ------| ------|
| 0             | create forks and creates first Philosopher | $1600 |
| 1-12          | create remaining Philosophers  |   $12 |
| 13            |       |   pickup left fork |||||
| 14            |       |   pickup right fork |||||
| 15            |       |    |pickup left fork||||
| 16            |       |   |pickup right fork||||
| 17            |       |    ||pickup left fork|||
| 18            |       |    ||pickup right fork|||
| 19            |       |   pickup left fork |||||
| 20            |       |   pickup left fork |||||
| 21            |       |   pickup left fork |||||
| 22            |       |   pickup left fork |||||
| 23            |       |   pickup left fork |||||
| 24            |       |   pickup left fork |||||
| 25            |       |   pickup left fork |||||









##Full error trace
```
JavaPathfinder core system v8.0 - (C) 2005-2014 United States Government. All rights reserved.


====================================================== system under test
DiningPhil.main()

====================================================== search started: 5/5/21 8:42 AM

====================================================== error 1
gov.nasa.jpf.vm.NotDeadlockedProperty
deadlock encountered:
  thread DiningPhil$Philosopher:{id:1,name:Thread-1,status:BLOCKED,priority:5,isDaemon:false,lockCount:0,suspendCount:0}
  thread DiningPhil$Philosopher:{id:2,name:Thread-2,status:BLOCKED,priority:5,isDaemon:false,lockCount:0,suspendCount:0}
  thread DiningPhil$Philosopher:{id:3,name:Thread-3,status:BLOCKED,priority:5,isDaemon:false,lockCount:0,suspendCount:0}
  thread DiningPhil$Philosopher:{id:4,name:Thread-4,status:BLOCKED,priority:5,isDaemon:false,lockCount:0,suspendCount:0}
  thread DiningPhil$Philosopher:{id:5,name:Thread-5,status:BLOCKED,priority:5,isDaemon:false,lockCount:0,suspendCount:0}


====================================================== trace #1
------------------------------------------------------ transition #0 thread: 0
gov.nasa.jpf.vm.choice.ThreadChoiceFromSet {id:"ROOT" ,1/1,isCascaded:false}
      [3157 insn w/o sources]
  DiningPhil.java:50             : Fork[] forks = new Fork[N];
  DiningPhil.java:51             : for (int i = 0; i < N; i++) {
  DiningPhil.java:52             : forks[i] = new Fork();
  DiningPhil.java:23             : static class Fork {
      [1 insn w/o sources]
  DiningPhil.java:23             : static class Fork {
  DiningPhil.java:52             : forks[i] = new Fork();
  DiningPhil.java:51             : for (int i = 0; i < N; i++) {
  DiningPhil.java:52             : forks[i] = new Fork();
  DiningPhil.java:23             : static class Fork {
      [1 insn w/o sources]
  DiningPhil.java:23             : static class Fork {
  DiningPhil.java:52             : forks[i] = new Fork();
  DiningPhil.java:51             : for (int i = 0; i < N; i++) {
  DiningPhil.java:52             : forks[i] = new Fork();
  DiningPhil.java:23             : static class Fork {
      [1 insn w/o sources]
  DiningPhil.java:23             : static class Fork {
  DiningPhil.java:52             : forks[i] = new Fork();
  DiningPhil.java:51             : for (int i = 0; i < N; i++) {
  DiningPhil.java:52             : forks[i] = new Fork();
  DiningPhil.java:23             : static class Fork {
      [1 insn w/o sources]
  DiningPhil.java:23             : static class Fork {
  DiningPhil.java:52             : forks[i] = new Fork();
  DiningPhil.java:51             : for (int i = 0; i < N; i++) {
  DiningPhil.java:52             : forks[i] = new Fork();
  DiningPhil.java:23             : static class Fork {
      [1 insn w/o sources]
  DiningPhil.java:23             : static class Fork {
  DiningPhil.java:52             : forks[i] = new Fork();
  DiningPhil.java:51             : for (int i = 0; i < N; i++) {
  DiningPhil.java:55             : new Philosopher(forks[i], forks[(i + 1) % N]);
  DiningPhil.java:31             : public Philosopher(Fork left, Fork right) {
      [145 insn w/o sources]
  DiningPhil.java:32             : this.left = left;
  DiningPhil.java:33             : this.right = right;
  DiningPhil.java:34             : start();
      [1 insn w/o sources]
------------------------------------------------------ transition #1 thread: 0
gov.nasa.jpf.vm.choice.ThreadChoiceFromSet {id:"START" ,1/2,isCascaded:false}
      [2 insn w/o sources]
  DiningPhil.java:35             : }
  DiningPhil.java:55             : new Philosopher(forks[i], forks[(i + 1) % N]);
  DiningPhil.java:54             : for (int i = 0; i < N; i++) {
  DiningPhil.java:55             : new Philosopher(forks[i], forks[(i + 1) % N]);
  DiningPhil.java:31             : public Philosopher(Fork left, Fork right) {
      [27 insn w/o sources]
------------------------------------------------------ transition #2 thread: 0
gov.nasa.jpf.vm.choice.ThreadChoiceFromSet {id:"LOCK" ,1/2,isCascaded:false}
      [119 insn w/o sources]
  DiningPhil.java:32             : this.left = left;
  DiningPhil.java:33             : this.right = right;
------------------------------------------------------ transition #3 thread: 0
gov.nasa.jpf.vm.choice.ThreadChoiceFromSet {id:"EXPOSE" ,1/2,isCascaded:false}
  DiningPhil.java:33             : this.right = right;
  DiningPhil.java:34             : start();
      [1 insn w/o sources]
------------------------------------------------------ transition #4 thread: 0
gov.nasa.jpf.vm.choice.ThreadChoiceFromSet {id:"START" ,1/3,isCascaded:false}
      [2 insn w/o sources]
  DiningPhil.java:35             : }
  DiningPhil.java:55             : new Philosopher(forks[i], forks[(i + 1) % N]);
  DiningPhil.java:54             : for (int i = 0; i < N; i++) {
  DiningPhil.java:55             : new Philosopher(forks[i], forks[(i + 1) % N]);
  DiningPhil.java:31             : public Philosopher(Fork left, Fork right) {
      [27 insn w/o sources]
------------------------------------------------------ transition #5 thread: 0
gov.nasa.jpf.vm.choice.ThreadChoiceFromSet {id:"LOCK" ,1/3,isCascaded:false}
      [119 insn w/o sources]
  DiningPhil.java:32             : this.left = left;
  DiningPhil.java:33             : this.right = right;
------------------------------------------------------ transition #6 thread: 0
gov.nasa.jpf.vm.choice.ThreadChoiceFromSet {id:"EXPOSE" ,1/3,isCascaded:false}
  DiningPhil.java:33             : this.right = right;
  DiningPhil.java:34             : start();
      [1 insn w/o sources]
------------------------------------------------------ transition #7 thread: 0
gov.nasa.jpf.vm.choice.ThreadChoiceFromSet {id:"START" ,1/4,isCascaded:false}
      [2 insn w/o sources]
  DiningPhil.java:35             : }
  DiningPhil.java:55             : new Philosopher(forks[i], forks[(i + 1) % N]);
  DiningPhil.java:54             : for (int i = 0; i < N; i++) {
  DiningPhil.java:55             : new Philosopher(forks[i], forks[(i + 1) % N]);
  DiningPhil.java:31             : public Philosopher(Fork left, Fork right) {
      [27 insn w/o sources]
------------------------------------------------------ transition #8 thread: 0
gov.nasa.jpf.vm.choice.ThreadChoiceFromSet {id:"LOCK" ,1/4,isCascaded:false}
      [119 insn w/o sources]
  DiningPhil.java:32             : this.left = left;
  DiningPhil.java:33             : this.right = right;
------------------------------------------------------ transition #9 thread: 0
gov.nasa.jpf.vm.choice.ThreadChoiceFromSet {id:"EXPOSE" ,1/4,isCascaded:false}
  DiningPhil.java:33             : this.right = right;
  DiningPhil.java:34             : start();
      [1 insn w/o sources]
------------------------------------------------------ transition #10 thread: 0
gov.nasa.jpf.vm.choice.ThreadChoiceFromSet {id:"START" ,1/5,isCascaded:false}
      [2 insn w/o sources]
  DiningPhil.java:35             : }
  DiningPhil.java:55             : new Philosopher(forks[i], forks[(i + 1) % N]);
  DiningPhil.java:54             : for (int i = 0; i < N; i++) {
  DiningPhil.java:55             : new Philosopher(forks[i], forks[(i + 1) % N]);
  DiningPhil.java:31             : public Philosopher(Fork left, Fork right) {
      [27 insn w/o sources]
------------------------------------------------------ transition #11 thread: 0
gov.nasa.jpf.vm.choice.ThreadChoiceFromSet {id:"LOCK" ,1/5,isCascaded:false}
      [119 insn w/o sources]
  DiningPhil.java:32             : this.left = left;
  DiningPhil.java:33             : this.right = right;
  DiningPhil.java:34             : start();
      [1 insn w/o sources]
------------------------------------------------------ transition #12 thread: 0
gov.nasa.jpf.vm.choice.ThreadChoiceFromSet {id:"START" ,1/6,isCascaded:false}
      [2 insn w/o sources]
  DiningPhil.java:35             : }
  DiningPhil.java:55             : new Philosopher(forks[i], forks[(i + 1) % N]);
  DiningPhil.java:54             : for (int i = 0; i < N; i++) {
  DiningPhil.java:57             : }
  DiningPhil.java:3              : // Copyright (C) 2006 United States Government as represented by the
------------------------------------------------------ transition #13 thread: 1
gov.nasa.jpf.vm.choice.ThreadChoiceFromSet {id:"TERMINATE" ,1/5,isCascaded:false}
      [1 insn w/o sources]
  DiningPhil.java:1              :
  DiningPhil.java:39             : synchronized (left) {
------------------------------------------------------ transition #14 thread: 1
gov.nasa.jpf.vm.choice.ThreadChoiceFromSet {id:"LOCK" ,1/5,isCascaded:false}
  DiningPhil.java:39             : synchronized (left) {
  DiningPhil.java:40             : synchronized (right) {
------------------------------------------------------ transition #15 thread: 2
gov.nasa.jpf.vm.choice.ThreadChoiceFromSet {id:"LOCK" ,2/5,isCascaded:false}
      [1 insn w/o sources]
  DiningPhil.java:1              :
  DiningPhil.java:39             : synchronized (left) {
------------------------------------------------------ transition #16 thread: 2
gov.nasa.jpf.vm.choice.ThreadChoiceFromSet {id:"LOCK" ,2/5,isCascaded:false}
  DiningPhil.java:39             : synchronized (left) {
  DiningPhil.java:40             : synchronized (right) {
------------------------------------------------------ transition #17 thread: 3
gov.nasa.jpf.vm.choice.ThreadChoiceFromSet {id:"LOCK" ,2/4,isCascaded:false}
      [1 insn w/o sources]
  DiningPhil.java:1              :
  DiningPhil.java:39             : synchronized (left) {
------------------------------------------------------ transition #18 thread: 3
gov.nasa.jpf.vm.choice.ThreadChoiceFromSet {id:"LOCK" ,2/4,isCascaded:false}
  DiningPhil.java:39             : synchronized (left) {
  DiningPhil.java:40             : synchronized (right) {
------------------------------------------------------ transition #19 thread: 4
gov.nasa.jpf.vm.choice.ThreadChoiceFromSet {id:"LOCK" ,2/3,isCascaded:false}
      [1 insn w/o sources]
  DiningPhil.java:1              :
  DiningPhil.java:39             : synchronized (left) {
------------------------------------------------------ transition #20 thread: 4
gov.nasa.jpf.vm.choice.ThreadChoiceFromSet {id:"LOCK" ,2/3,isCascaded:false}
  DiningPhil.java:39             : synchronized (left) {
  DiningPhil.java:40             : synchronized (right) {
------------------------------------------------------ transition #21 thread: 5
gov.nasa.jpf.vm.choice.ThreadChoiceFromSet {id:"LOCK" ,2/2,isCascaded:false}
      [1 insn w/o sources]
  DiningPhil.java:1              :
  DiningPhil.java:39             : synchronized (left) {
------------------------------------------------------ transition #22 thread: 5
gov.nasa.jpf.vm.choice.ThreadChoiceFromSet {id:"LOCK" ,2/2,isCascaded:false}
  DiningPhil.java:39             : synchronized (left) {
  DiningPhil.java:40             : synchronized (right) {

====================================================== snapshot #1
thread DiningPhil$Philosopher:{id:1,name:Thread-1,status:BLOCKED,priority:5,isDaemon:false,lockCount:0,suspendCount:0}
  owned locks:DiningPhil$Fork@162
  blocked on: DiningPhil$Fork@163
  call stack:
	at DiningPhil$Philosopher.run(DiningPhil.java:40)

thread DiningPhil$Philosopher:{id:2,name:Thread-2,status:BLOCKED,priority:5,isDaemon:false,lockCount:0,suspendCount:0}
  owned locks:DiningPhil$Fork@163
  blocked on: DiningPhil$Fork@164
  call stack:
	at DiningPhil$Philosopher.run(DiningPhil.java:40)

thread DiningPhil$Philosopher:{id:3,name:Thread-3,status:BLOCKED,priority:5,isDaemon:false,lockCount:0,suspendCount:0}
  owned locks:DiningPhil$Fork@164
  blocked on: DiningPhil$Fork@165
  call stack:
	at DiningPhil$Philosopher.run(DiningPhil.java:40)

thread DiningPhil$Philosopher:{id:4,name:Thread-4,status:BLOCKED,priority:5,isDaemon:false,lockCount:0,suspendCount:0}
  owned locks:DiningPhil$Fork@165
  blocked on: DiningPhil$Fork@166
  call stack:
	at DiningPhil$Philosopher.run(DiningPhil.java:40)

thread DiningPhil$Philosopher:{id:5,name:Thread-5,status:BLOCKED,priority:5,isDaemon:false,lockCount:0,suspendCount:0}
  owned locks:DiningPhil$Fork@166
  blocked on: DiningPhil$Fork@162
  call stack:
	at DiningPhil$Philosopher.run(DiningPhil.java:40)


====================================================== results
error #1: gov.nasa.jpf.vm.NotDeadlockedProperty "deadlock encountered:   thread DiningPhil$Philosop..."

====================================================== statistics
elapsed time:       00:00:00
states:             new=2535,visited=5671,backtracked=8183,end=29
search:             maxDepth=29,constraints=0
choice generators:  thread=2534 (signal=0,lock=1608,sharedRef=3,threadApi=5,reschedule=918), data=0
heap:               new=404,released=19609,maxLive=387,gcCycles=8206
instructions:       55524
max memory:         240MB
loaded code:        classes=64,methods=1478

====================================================== search finished: 5/5/21 8:42 AM
```