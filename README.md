# 🔍 Word Frequency Analysis using Parallel Computing

## 📌 Overview

This project analyzes the performance of different computing approaches to find the **Top 10 most frequent words** in a large dataset.

It compares three approaches:

* Naïve (Sequential)
* Multiprocessing (using fork)
* Multithreading (using pthreads)

The goal is to evaluate execution time and performance improvements using parallel computing.

---

## ⚙️ Technologies Used

* Language: C
* OS: Linux (Ubuntu VM)
* Concepts:

  * Multiprocessing (fork, shared memory)
  * Multithreading (pthread, mutex)
  * Parallel Computing
  * Performance Analysis

---

## 🧠 Approaches

### 1️⃣ Naïve Approach

* Sequential execution
* No parallelism
* Slowest performance

### 2️⃣ Multiprocessing

* Uses multiple child processes
* Shared memory with `mmap`
* Best performance improvement

### 3️⃣ Multithreading

* Uses threads (`pthread`)
* Synchronization with mutex
* Faster than naïve but limited by locking

---

## 📊 Results Summary

* Naïve: Slowest ⛔
* Multiprocessing: Fastest 🚀
* Multithreading: Good but limited ⚖️

From the report:

* Best performance achieved with **8 processes**
* Multithreading improved but affected by mutex overhead

---

## 📁 Dataset

Dataset used:

* enwik8 (large text dataset)

---

## 📄 Report

Full report available in:

```
/report/os-project-report.pdf
```

---

## 🚀 How to Run

### Compile:

```bash
gcc naive.c -o naive
gcc multiprocessing.c -o multi_proc
gcc multithreading.c -o multi_thread -lpthread
```

### Run:

```bash
./naive
./multi_proc
./multi_thread
```

---

## 👩‍💻 Author

Sara Shrouf
Computer Engineering Student
