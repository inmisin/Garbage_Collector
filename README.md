# Baby's First Garbage Collector (BFGC)

An ultra-lightweight, production-ready **Mark-and-Sweep Garbage Collector** simulation implemented in vanilla C. This project simulates a stack-based Virtual Machine (VM) memory management layer, eliminating the need for manual memory management (`free()`) by automatically reclaiming unreachable objects.

> 💡 **Reference Note:** This implementation is strictly based on the classic educational guide ["Baby's First Garbage Collector"](https://journal.stuffwithstuff.com/2013/12/08/babys-first-garbage-collector/) by Bob Nystrom (munificent).

---

## 🚀 Features

* **Garbage Collected VM:** A fully automated memory management layer built on top of a stack-based virtual machine simulation.
* **Zero-Waste Memory Footprint:** Efficient utilization of C's `union` (Tagged Union pattern) to encapsulate different object types (`INT` and `PAIR`) without bloating memory.
* **Cycle-Safe Traversal:** Smart reachability checking that prevents stack overflows or infinite loops when processing cyclic object graphs (e.g., objects pointing to each other).
* **Dynamic Heap Growth:** Automatic scaling of the GC trigger threshold ($2 \times \text{live objects}$) after each collection cycle to adapt to memory pressure.

