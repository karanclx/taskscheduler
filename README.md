# promanage task scheduler

a java-based task scheduling system that optimizes project selection to maximize revenue under deadline constraints.

---

## overview

promanage solutions handles multiple client projects each week. since only one project can be completed per day (maximum 5 per week), selecting the right projects is critical.

this system:
- stores project data in postgresql
- uses a greedy algorithm (job sequencing with deadlines)
- generates an optimal weekly schedule
- supports rolling weekly planning

---

## core idea

each project has:
- deadline (in working days)
- revenue (profit if completed on time)

the system:
1. sorts projects by revenue (highest first)
2. assigns each project to the latest available day before its deadline
3. maximizes total revenue

---

## tech stack

- java (core java, jdbc)
- postgresql
- intellij idea

---

## features

- add new projects
- view all projects
- generate optimal weekly schedule
- project lifecycle tracking:
  - pending
  - completed
  - expired
- rolling weekly update:
  - deadlines reduced
  - expired projects handled

---

## algorithm

greedy scheduling (job sequencing with deadlines)

time complexity: o(n log n)
