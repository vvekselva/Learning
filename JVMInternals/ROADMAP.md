# JVM Internals Roadmap

## 1. Java Execution Model
Learn JDK vs JRE vs JVM, `javac`, `.java -> .class`, JVM startup, bytecode, interpreter and JIT.

Commands:
```bash
javac HelloJVM.java
java HelloJVM
javap -c HelloJVM
javap -v HelloJVM
```

Links:
- https://docs.oracle.com/en/java/javase/21/vm/
- https://docs.oracle.com/javase/specs/jvms/se21/html/jvms-2.html
- https://docs.oracle.com/en/java/javase/21/docs/specs/man/javap.html

## 2. JVM Bytecode & Class File
- https://docs.oracle.com/javase/specs/jvms/se21/html/jvms-3.html
- https://docs.oracle.com/javase/specs/jvms/se21/html/jvms-4.html
- https://docs.oracle.com/javase/specs/jvms/se21/html/jvms-6.html

## 3. Class Loading
- https://docs.oracle.com/javase/specs/jvms/se21/html/jvms-5.html
- https://docs.oracle.com/en/java/javase/21/docs/api/java.base/java/lang/ClassLoader.html

Command:
```bash
java -Xlog:class+load=info HelloJVM
```

## 4. JVM Runtime Data Areas
- https://docs.oracle.com/javase/specs/jvms/se21/html/jvms-2.html#jvms-2.5
- https://docs.oracle.com/en/java/javase/21/vm/native-memory-tracking.html

## 5. Objects & Memory
- https://github.com/openjdk/jol
- https://shipilev.net/jvm/anatomy-quarks/
- https://github.com/openjdk/jdk/tree/master/src/hotspot

## 6. Garbage Collection
- https://docs.oracle.com/en/java/javase/21/gctuning/
- https://docs.oracle.com/en/java/javase/21/gctuning/garbage-first-garbage-collector.html
- https://docs.oracle.com/en/java/javase/21/gctuning/z-garbage-collector.html
- https://wiki.openjdk.org/display/shenandoah/Main

Command:
```bash
java -Xlog:gc* YourProgram
```

## 7. Interpreter & JIT
- https://shipilev.net/jvm/anatomy-quarks/
- https://github.com/openjdk/jdk/tree/master/src/hotspot
- https://www.oreilly.com/library/view/java-performance-2nd/9781492056102/
- https://www.oreilly.com/library/view/optimizing-java/9781492025781/

Commands:
```bash
java -XX:+PrintCompilation YourProgram
java -Xlog:compiler*=debug YourProgram
```

## 8. Java Memory Model & Concurrency
- https://docs.oracle.com/javase/specs/jls/se21/html/jls-17.html
- https://openjdk.org/jeps/444
- https://docs.oracle.com/en/java/javase/21/docs/api/java.base/java/util/concurrent/package-summary.html

## 9. Diagnostics & Performance
- https://docs.oracle.com/en/java/javase/21/docs/specs/man/jcmd.html
- https://docs.oracle.com/en/java/javase/21/docs/specs/man/jstack.html
- https://docs.oracle.com/en/java/javase/21/docs/specs/man/jmap.html
- https://docs.oracle.com/en/java/javase/21/docs/specs/man/jstat.html
- https://docs.oracle.com/en/java/javase/21/jfapi/
- https://github.com/openjdk/jmc

## 10. HotSpot Internals
- https://github.com/openjdk/jdk
- https://github.com/openjdk/jdk/tree/master/src/hotspot
- https://openjdk.org/
- https://openjdk.org/jeps/0

## Core Learning Cycle
READ → WRITE SMALL PROGRAM → RUN JVM TOOL → OBSERVE → EXPLAIN → COMMIT
