# 📝 MY_WORK: Student Information, Development Log, Reflection & Answers

> This is the **only file** your instructor reads to grade Parts 3 and 4 (documentation and video). Everything you write here must be **in your own words**.

---

## 🛑 STOP: Read This Before You Do Anything Else

> ### 1️⃣ Read the whole `README.md` first
> The `README.md` in this repository contains the full instructions: how this assignment continues Assignment 1, the Chapter 5 recap, class descriptions, feature specifications, question prompts and the video script. **If you skip it, you will lose marks.**
>
> ### 2️⃣ Understand the full code before answering any question
> Open `SchedulerSimulationSync.java` and read it **from top to bottom**. You must be able to explain what `SharedStats`, `ReadyQueue`, `CpuWorker`, `RaceWindow.pause()`, `ReentrantLock` and `Semaphore` do **before** you write a single answer in Parts B and C. **Run the original starter first** (it is intentionally broken) and **save its output**: you need it for Question 1 of Part C.
>
> ### 3️⃣ Use only the code of this repository
> Work **only** on `SchedulerSimulationSync.java` from this repository. Do **not** copy or paste code from your previous assignments.
>
> ### 4️⃣ Commit many times, not once
> A single commit, or all commits made in the last hour, costs you **-0.5 mark**. See the [Commit Rules](#-commit-rules-mandatory) below.

**How to use this file:**
1. Fill in your **Student Information** (below) right now.
2. Follow the steps in the **Work Roadmap** in order.
3. Update the **Development Log** *every time* you work on the assignment, not at the end.
4. Do not delete any section header. Replace the `[...]` placeholders with your own text.

---

## 👤 Student Information

> ⚠️ **WARNING:** Fill this in first. Your name and ID must match the student ID you set in `SchedulerSimulationSync.java` (line 304) and the one you say in your video.

| Field | Your Answer |
|-------|-------------|
| **Full Name** | [Rena hassan mohammed Kariri] |
| **Student ID** | [446052320] |
| **University Email** | [446052320]@std.psau.edu.sa |
| **GitHub Username** | [Rena-446] |
| **Repository Link** | [https://github.com/Rena-446/OS-Assignment3-Rena-Kariri] |
 
---

## 🎥 Video Link

**Video Link**: [https://drive.google.com/file/d/14ZFX1IU5o2IM-_4k5qPZwzT0DE3b69Gw/view?usp=drivesdk]

> ⚠️ **WARNING:** The video must be **publicly accessible** ("Anyone with the link can view") on **Google Drive**, **YouTube (Unlisted or Public)** or any other cloud file-sharing system. A private, restricted or broken link counts as a **missing video (-1 mark)**.
>
> 💡 **TIP:** Open the link in a **private/incognito window** before you submit. If it asks you to log in or request access, it is not public.
>
> 📌 **NOTE:** The link goes in **this file only** (`MY_WORK.md`), **not** in `README.md`. Name your video file `StudentID_Assignment3_Demo.mp4`. It must last **2 to 3 minutes**.

---

## 🗺️ Work Roadmap (follow in this order)

| Step | What to do | Where | Marks |
|:----:|------------|-------|:-----:|
| 0 | Read `README.md`, read the full code, **run the original starter and save its output** (it fails on purpose) | Your IDE | – |
| 1 | Fork, rename, keep the repo **PUBLIC**, set your student ID (line 304), **commit** | GitHub + code | Part 1 (1) |
| 2 | Feature 1: Mutex lock on the ready queue, **commit** | Code | Part 2 (0.25) |
| 3 | Feature 2: Mutex lock(s) on the shared statistics, **commit** | Code | Part 2 (0.25) |
| 4 | Feature 3: Counting semaphore instead of busy waiting, **commit** | Code | Part 2 (0.5) |
| 5 | Development Log (5+ entries, different dates) | This file, Part A | Part 3 (0.5) |
| 6 | Reflection (4 questions) | This file, Part B | Part 3 (0.5) |
| 7 | Technical Answers (4 questions) | This file, Part C | Part 3 (0.5) |
| 8 | Record the video, upload it, paste the link above | Video + this file | Part 4 (1.5) |
| 9 | Final check, then submit the repo link on Blackboard | Blackboard | – |

> 💡 **TIP:** Tick each step off as you go. Do not leave the log, the reflection or the video for the last day.

---

## 🔁 Commit Rules (MANDATORY)

> ### ⚠️ MANY COMMITS ARE REQUIRED. A single bulk commit is penalized (-0.5 mark).

**Minimum: 4 meaningful commits. Aim for 7 or more.**

| # | Commit | Example message |
|:-:|--------|-----------------|
| 1 | Student ID set | `Set my student ID: 441234567` |
| 2 | Feature 1: Ready queue lock | `Feature 1: Protected the ready queue with a ReentrantLock` |
| 3 | Feature 2: Statistics locks | `Feature 2: Added locks to the shared statistics counters` |
| 4 | Feature 3: Semaphore | `Feature 3: Replaced busy waiting with a counting semaphore` |
| 5 | Development log entries | `Docs: Added development log entries 1-3` |
| 6 | Reflection and answers | `Docs: Completed reflection and technical answers` |
| 7 | Video link | `Docs: Added demo video link` |

**Rules:**
- ✅ **One commit per feature.** Do not put all three features in one commit.
- ✅ **Commit after each work session**, and after each part of this file.
- ✅ **Spread your commits over different dates.** Not all in one day.
- ❌ **Do not make all commits in the last hour** before the deadline (November 14, 2026).
- ❌ **No vague messages** like `done`, `update` or `final version`.

> 💡 **TIP:** Your commit history is checked and you **show it in your video** (at least 4 commits visible). Your development log dates should match your commit dates.
>
> 💡 **TIP:** **Use VS Code** (see *Recommended Development Environment* in `README.md` for the full setup). Sign in to GitHub in VS Code, then commit from the Source Control panel (Ctrl+Shift+G) → stage → write a message → Commit → Sync/Push. You can edit and commit this file the same way. **Pushing** matters: commits that are not pushed to GitHub are invisible to the instructor.

---

# Part A: Development Log (0.5 mark)

> ⚠️ **WARNING:** Minimum **5 entries**, spread over **different dates**. Five entries written on the same day, or written all at once at the end, will lose marks and look like a copy. Entry dates should be **between the start of the assignment and the deadline (November 14, 2026)**.
>
> 💡 **TIP:** Write an entry at the **end of each work session**, while you still remember what happened. It takes 5 minutes.
>
> 💡 **TIP:** Be specific. "Worked on the code" is a weak entry. "Added a `ReentrantLock queueLock` to `ReadyQueue` and wrapped the body of `poll()` in `lock()` / `try` / `finally { unlock() }`" is a strong one.
>
> 📌 **NOTE:** Each entry needs: date and time, what you did, details, challenges, solution, and time spent. Real challenges are fine (and expected). Do not invent fake ones.

## Example Entry (do not copy it, write your own)

### Entry 1 - [November 2, 2026, 4:30 PM]
**What I did**: Forked the repository, set my student ID, and ran the original starter

**Details**:
- Forked the starter repository and renamed it
- Changed student ID on line 304 to my actual ID (441234567)
- Ran the original program: 4 CPUs started, three of them picked `P1`, then `IllegalThreadStateException` and the watchdog stopped the program
- Saved the output in a text file for Question 1
- Committed and pushed: `Set my student ID: 441234567`

**Challenges**: I did not understand why the same process was picked by three CPUs

**Solution**: Read `ReadyQueue.poll()` again and found the `RaceWindow.pause()` between reading the head and removing it

**Time spent**: 45 minutes

---

## Your Development Log

### Entry 1 - [Nov 7,2026 Time: 8pm]
**What I did**: Set My Student ID

**Details**:
• Updated the student ID in the Java source code.
• Used my actual student ID as the random number generator seed.

**Challenges**:
Located the correct place to update the student ID
**Solution**:
Updated the assigned variable and checked the value.
**Time spent**:
10 minutes
---

### Entry 2 - [Nov 8 Time: 8pm]
**What I did**: Run the original code before making any changes.

**Details**:
• Compiled and executed the original Java program.
• Observed the initial CPU scheduling behavior and program output.
• Checked the original implementation before starting the required features.
**Challenges**:
Understanding the original program structure and its execution.
**Solution**:
Reviewed the output and examined the existing code.
**Time spent**:
10 minutes
---

### Entry 3 - [Nov 10 Time: 4am]
**What I did**: implement feature 1

**Details**:
• Added a ReentrantLock named queueLock.
• Protected the add(), poll(), processOf(), and snapshot() methods.
• Used try-finally to ensure the lock is always released.
**Challenges**:
Preventing multiple CPU threads from accessing shared queue data simultaneously.
**Solution**:
Used a lock to protect critical sections.
**Time spent**:
30 minutes
---

### Entry 4 - [Nov 11 Time: 6pm]
**What I did**: implement Feature 2

**Details**:
• Added a ReentrantLock named statsLock.
• Protected shared statistics from concurrent access.
• Updated the methods for completed processes, context switches, and total service time.
• Used try-finally to release the lock safely.
**Challenges**:
Avoiding race conditions when multiple threads update shared statistics.
**Solution**:
Protected shared variables using a synchronization lock.
**Time spent**:
20 minutes
---

### Entry 5 - [Nov 12 Time: 2pm]
**What I did**: implement feature 3

**Details**:
• Added a counting semaphore to track available processes.
• Used acquire() when a CPU requests a process.
• Used release() when a process is added to the ready queue.
• Replaced the busy-waiting behavior with blocking synchronization.
• Added a wake-up mechanism to allow CPUs to terminate when all processes are completed.
• Tested the program and checked the verification results.
**Challenges**:
Preventing unnecessary CPU polling and ensuring that CPU threads terminate correctly.
**Solution**:
Used semaphore synchronization and a wake-up mechanism to coordinate CPU threads.
**Time spent**:
2 hours
---

### Entry 6 - [Optional - Date and Time]
**What I did**:

**Details**:

**Challenges**:

**Solution**:

**Time spent**:

---

## Development Log Summary

> 💡 **TIP:** Fill this in **last**, after all entries are written.

**Total time spent on assignment**: [X hours]

**Most challenging part**:

**Most interesting learning**:

**What I would do differently next time**:

---

# Part B: Reflection (0.5 mark)

> 🛑 **STOP:** Do **not** start this part until you have read the `README.md`, read the **entire** `SchedulerSimulationSync.java`, run it, and finished the three features.
>
> ⚠️ **WARNING:** Each answer must be **5 to 7 sentences**, in **your own words**. Copied or AI-generated answers without understanding get **0 marks for the whole assignment**. You may be asked to explain them in person.
>
> 💡 **TIP:** Mention concrete things you actually did: a method you wrote, an error you hit, a line of output you saw. Generic answers score low.
>
> 💡 **TIP:** Draft your answer in a few bullet points first, then turn them into sentences.

## Question 1: What did you learn about synchronization?

> 💡 **TIP:** Talk about race conditions (read-modify-write), critical sections, mutual exclusion with `ReentrantLock` and `try/finally`, the role of a counting semaphore, and what surprised you when the starter failed.

**Your Answer:** *(5-7 sentences)*

[I learned that synchronization is important when multiple threads work at the same time. Without it, race conditions can happen when threads access the same data. I used ReentrantLock to protect the shared queue and prevent conflicts. I also learned that try and finally make sure the lock is released safely. Finally, I learned that semaphores help control access to available processes.]

## Question 2: What was the most challenging part of this assignment?

> 💡 **TIP:** Pick **one** specific challenge (understanding why the starter failed, choosing the lock granularity, the initial value of the semaphore, the shutdown of the CPUs, Git, the video) and say *why* it was hard.

**Your Answer:** *(5-7 sentences)*

[The most challenging part was Feature 3. I had difficulty understanding how to use semaphores to control the CPU threads. Sometimes, the CPUs kept waiting even after all processes were finished. I solved this by using a wake-up mechanism to notify the CPUs when all processes were completed. After testing the program, all shared values were correct.]

## Question 3: How did you overcome the challenges you faced?

> 💡 **TIP:** Describe your method: reading the slides and the documentation, adding `System.out.println` to debug, running the program many times, re-reading the README, testing after each small change, asking for help.

**Your Answer:** *(5-7 sentences)*

[I overcame the challenges by reading the slides and README carefully. I used System.out.println() to understand what was happening in the program. I tested the code many times after each change. When I faced errors, I checked the code and tried to understand the problem. This helped me fix the errors and complete the assignment.]

## Question 4: Where can synchronization concepts be applied in real-world applications?

> 💡 **TIP:** Use real applications you know (banking and money transfers, ticket or seat booking, a shared counter on a website, a print queue, a database) and connect each one to what you built here (shared data, critical section, lock or semaphore).

**Your Answer:** *(5-7 sentences)*

[Synchronization is important in many real-world applications. For example, in banking, it prevents problems when two people transfer money at the same time. In ticket booking systems, it prevents two people from booking the same seat. It is also useful in databases when many users access the same data. These examples show why synchronization is important.]

### Optional: What would you like to learn more about?

[I would like to learn more about multithreading and synchronization. I want to understand how locks and semaphores work in bigger applications. I am also interested in learning how to solve race conditions. I think these topics will help me become better at programming.]

### Optional: How confident do you feel about synchronization concepts now?

[I feel more confident about synchronization now. I understand how locks and semaphores help protect shared data. I also learned how to prevent race conditions. At first, the concepts were difficult, but practicing helped me understand them better.]

### Optional: Feedback on the assignment

[The assignment was helpful because I learned by writing and testing code. Some parts were difficult, especially Feature 3. I liked that I could see the results after running the program. I suggest adding more examples to explain synchronization concepts. Overall, it was a good learning experience.]

---

# Part C: Technical Answers (0.5 mark)

> 🛑 **STOP:** You cannot answer these questions without understanding the code. Re-read `SchedulerSimulationSync.java` and **run it** first. Your answers must reference **your own code and your own output** (your student ID makes your output and your expected values unique).
>
> ⚠️ **WARNING:** Each answer must be **3 to 5 sentences**, with specific examples from your code or output. Use correct terms: race condition, critical section, mutual exclusion, mutex lock, semaphore, busy waiting, deadlock, producer, consumer.
>
> 💡 **TIP:** Keep the output of the **original starter** and the output of your **final version** in text files or screenshots, so you can copy real snippets for Question 1.

## Question 1: Race Condition in Your Own Output

**Question**: Run the **original starter** (before any fix) and paste the **verification block** of that run. Which value was wrong (expected vs observed)? Explain **step by step**, with two named threads/CPUs, how **one lost update** happens on one of the shared variables (read, `RaceWindow.pause()`, write). Why can the same bug happen on a real machine even without `RaceWindow`, and why is it hard to detect?

> ⚠️ **WARNING:** The snippet must come from **your own run** (with your student ID), not from a classmate or from this README.
>
> 💡 **TIP:** Use a small timeline: *CPU-1 reads `contextSwitchCount` = 12 → CPU-2 reads 12 → CPU-1 writes 13 → CPU-2 writes 13 → one increment is lost.* If your starter run crashed before printing numbers, run it several times (or paste the exception and the watchdog message and explain it).

**Your Answer:** *(3-5 sentences)*

[In the original program, I noticed that the verification results did not match the expected values. The context switches, completed processes, and total service time had incorrect results. The program also showed busy-waiting polls instead of zero. This happened because multiple CPUs accessed shared data at the same time without proper synchronization. One CPU could update a value while another CPU was reading or changing it, causing a race condition and lost updates.]

Verification block of the **original starter**:
```
[Paste the verification block (or the exception/watchdog message) of the starter here]
```

Verification block of **my final version**:
```
[Paste the verification block of your final version here (all lines ✔)]
```

**Explanation of the timeline:**
[CPU-1 reads the shared counter value 12. Before CPU-1 updates it, CPU-2 also reads the same value 12. CPU-1 adds 1 and writes 13. Then CPU-2 also adds 1 and writes 13. The expected value is 14, but the actual value is 13 because one update was lost.]

## Question 2: Critical Sections and Lock Granularity

**Question**: List the **critical sections** you protected (variables and methods) and the lock(s) you used. **Lock granularity:** did you use **one lock** for the three statistics or **one lock per variable**? Why, and what is the trade-off? Why is the **ready queue** protected by a **different** lock than the statistics? Explain how your solution provides **mutual exclusion**, and discuss **progress** and **bounded waiting** (a default `ReentrantLock` is not fair: what does that imply?).

> 💡 **TIP:** The three counters are independent: does updating `contextSwitchCount` need to block an update of `totalServiceTime`? Also think about what could go wrong (deadlock, or long waiting) if the queue lock and the statistics lock were the **same** lock and a thread held it while doing something slow.

**Your Answer:** *(3-5 sentences)*

[I used a ReentrantLock called queueLock to protect the shared list and map in the ReadyQueue class. I used this lock in add(), poll(), processOf(), and snapshot() to prevent multiple CPUs from changing shared data at the same time. The lock provides mutual exclusion, and I used try/finally to make sure the lock is always released. This helps the program work correctly, but ReentrantLock is not fair by default, so bounded waiting is not guaranteed. I also used a semaphore to control when CPUs can access available processes in the queue.]

| Critical section (variable / method) | Lock used | Why it needs protection |
|---|---|---|
| [e.g., `ReadyQueue.poll()`] | [lock name] | [reason] |
| [...] | [...] | [...] |

## Question 3: Busy Waiting vs Semaphore

**Question**: Describe the **busy waiting** of the starter and its cost (give the `Busy-waiting polls` number from your **starter** run). What does the **value of your semaphore** represent? What is its **initial value** and why? What is its value right after the `numProcesses` initial `add()` calls? Why does the last CPU call `release(totalCPUs)` at the end, and what would happen if it did not?

> 💡 **TIP:** Think about what a CPU does when the queue is empty in the starter, and what a CPU does in your final version (is it running, ready or blocked?). Also check what happens to a CPU blocked in `acquire()` when no process will ever be added again.

**Your Answer:** *(3-5 sentences)*

[In the starter code, CPUs kept checking the ready queue repeatedly to see if a process was available. This caused busy waiting and wasted CPU time. In my original run, the busy-waiting polls were [242]. I used a counting semaphore with an initial value of 0 because there were no available processes at the beginning. After adding all processes, its value becomes equal to the number of processes, and the last CPU releases the semaphore to wake up waiting CPUs so they can terminate instead of waiting forever.]

## Question 4: Classical Problems and Deadlock

**Question**: The CPUs and the ready queue look like a classical synchronization problem of Chapter 5. **Name it**, and say who plays the **producer** and the **consumer** roles (careful: here the CPUs also re-enqueue processes). If the ready queue were **bounded** (capacity `K`), name the **three semaphores** you would need and their **initial values**. Describe a **deadlock scenario** that appears if a thread acquired the **mutex before** waiting on the semaphore (or if two locks were acquired in different orders), and say **which of the four necessary conditions** you would break to prevent it.

> 💡 **TIP:** Recall the bounded-buffer solution of the slides (`empty`, `full`, `mutex`) and the order of `wait()` calls in the producer and the consumer. For the deadlock, think about a producer that holds the mutex while waiting for a free slot that only a consumer (who needs the mutex) can create.

**Your Answer:** *(3-5 sentences)*

**Classical problem and roles**:
[The ready queue works like a bounded buffer with a limited capacity. The producer adds new processes to the queue, and the CPU workers act as consumers because they take processes from it. The CPUs can also add unfinished processes back to the queue. This means the queue needs synchronization to prevent problems when multiple threads access it at the same time.]

**Semaphores for a bounded queue (name and initial value)**:
[use three semaphores: empty, full, and mutex. The initial value of empty is K because the queue has K empty slots. The initial value of full is 0 because the queue is empty at the beginning. The initial value of mutex is 1 to allow only one thread to access the queue at a time.]

**Deadlock scenario and prevention**:
[A deadlock can happen if a CPU takes the mutex lock before waiting for a process. If the queue is empty, the CPU keeps the lock while waiting. Another CPU cannot add a new process because the first CPU is holding the lock. To prevent this, the thread should wait on the semaphore before acquiring the mutex. Also, all threads should acquire locks in the same order.

four conditions are mutual exclusion, hold and wait, no preemption, and circular wait. We can prevent deadlock by breaking at least one of these condition]

## Summary

**Key concepts I understood through these questions:**
1.I understood how synchronization prevents race conditions when multiple CPUs access shared data.
2.I learned how to use ReentrantLock and semaphores to protect the ready queue.
3.I understood the difference between busy waiting and semaphore waiting, and how deadlocks can happen.

**Concepts I need to study more:**
1.I need to practice more with semaphores and understand how wait() and signal() work.
2.I need to understand deadlock conditions better and how to prevent them in different situations.

---

# ✅ Final Checklist (complete before submitting)

> ⚠️ **WARNING:** Go through every line. Blackboard does not accept submissions after the deadline, which is **November 14, 2026**.

**Repository**
- [x ] Repository is **PUBLIC** (Settings → Danger Zone → Visibility)
- [x ] Repository is renamed to `OS-Assignment3-YourFirstName-YourLastName`
- [x ] GitHub account uses the university email (`@std.psau.edu.sa`)

**Code**
- [x ] Student ID is set in `SchedulerSimulationSync.java` (line 304)
- [x ] My code is based **only** on the starter of this repository (nothing copied from previous assignments)
- [x ] Code compiles and runs with no errors, and terminates by itself (no `⛔ WATCHDOG`)
- [ x] Feature 1 (ready queue lock), Feature 2 (statistics locks) and Feature 3 (semaphore, no busy waiting) all work
- [x ] **The four verification lines are ✔ in 5 consecutive runs**
- [ x] Every lock is released in a `finally` block
- [x ] `RaceWindow`, `Config`, the verification block and the watchdog are **unchanged**
- [x ] Each feature has clear comments

**Commits**
- [x ] **At least 4 meaningful commits, ideally 7 or more**
- [ x] **One commit per feature**
- [ x] Commits are spread over **different dates** (not all in the last hour)
- [ x] Everything is **pushed** to GitHub

**This file (`MY_WORK.md`)**
- [ x] Full name and student ID filled in at the top
- [ x] Development log has **5+ entries** on different dates
- [ x] Reflection: 4 questions, 5-7 sentences each
- [x ] Technical answers: 4 questions, 3-5 sentences each, with examples from **your** output (starter output **and** final output pasted in Question 1)
- [x ] No `[...]` placeholders left
- [x ] No section headers deleted

**Video**
- [x ] 2-3 minutes long, named `StudentID_Assignment3_Demo.mp4`
- [ x] Shows your name, ID, repository, 3 features (and your lock granularity choice), IDE execution with the verification block, one synchronization concept, and commit history
- [x ] Link is **public** (tested in an incognito window) and pasted in the **Video Link** section above

**Blackboard**
- [x ] Submit **only** the link to your public GitHub repository

> 🎯 **Good luck!** Start early, commit regularly, and make sure you can explain every line you submit.
