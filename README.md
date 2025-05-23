# StressTest

### A simple C++ application to stress test your server's **CPU** and **RAM** capacity.

---

## 🛠 What It Does

This lightweight C++ tool performs a 10-minute stress test on both CPU and RAM to help you evaluate server hardware performance and thermal limits. It:

- Detects total available RAM (Linux only)
- Allocates ~95% of system memory
- Launches maximum number of CPU threads
- Performs heavy floating-point operations
- Logs the process to `stress_log.txt`

---

## 📦 Features

- Multi-threaded CPU load generation
- Dynamic RAM consumption based on physical memory
- Compatible with **Linux**
- Clean runtime logging

---

## 🔧 Usage

### 🧱 Requirements
- g++ compiler
- Linux-based system

### ⚙️ Compile & Run
```bash
g++ -std=c++11 stress.cpp -o stress -pthread
./stress


📁 Output Sample

  ==== CPU & RAM Stress Test ====
  Start Time: Fri May 23 14:59:21 2025
  System RAM: 16384 MB
  RAM Allocated: 15552 MB
  Logical Threads: 8
  Test Duration: 600 seconds
  Starting stress...
  
  ...
  
  Stress test completed successfully.
  End Time: Fri May 23 15:09:21 2025
  Total Elapsed Time: 600 seconds
  
  Test by: Amin
  ===============================



⚠️ Limitations
	•	Only supports Linux for RAM detection
	•	No live CPU/RAM usage graph or metrics
	•	Not suitable for use on production machines

