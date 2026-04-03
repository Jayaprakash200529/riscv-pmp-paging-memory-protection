🔐 RISC-V Hybrid Memory Protection (PMP + Paging)

A hardware-based memory protection system combining Physical Memory Protection (PMP) and Paging-based Virtual Memory for secure and efficient address translation in RISC-V systems.

---

📌 Overview

Modern processors require strong memory isolation for secure execution.
This project proposes a Hybrid PMP + Paging Architecture to provide:

- 🔒 Secure memory access control
- ⚡ Fast address translation using Mini-TLB
- 🧠 Hardware-level protection enforcement
- 🛡️ Support for confidential computing

---

🏗️ System Architecture

The system integrates:

- MMU (Memory Management Unit)
- PMP Unit (Access Control)
- Paging Unit (Virtual Memory)
- Mini-TLB (Translation Cache)

🔄 Flow:

CPU Request
   ↓
Virtual Address Translation (MMU)
   ↓
PMP Permission Check
   ↓
Physical Memory Access

---

⚙️ Modules

🔹 MMU (mmu.v)

- Virtual → Physical address translation
- Page table lookup
- Mini-TLB implementation

🔹 PMP Unit (pmp_unit.v)

- Region-based access control
- Mode-based permission validation

🔹 Top Module (riscv_mem_subsystem_top.v)

- Integrates MMU + PMP
- Generates final physical address and fault signal

🔹 Testbench

- Validates:
  - Address translation
  - PMP violations
  - Fault handling

---

🧪 Simulation Results

✔ Successful address translation
✔ PMP violation detection
✔ Fault handling for unauthorized access
✔ No undefined (X/Z) signals after reset

---

🛠️ Tools Used

- Verilog HDL
- Xilinx Vivado
- Behavioral Simulation
- RTL Design & Verification

---

📊 FPGA Implementation

- Efficient LUT usage
- Optimized Flip-Flop utilization
- Scalable architecture

---

💡 Key Features

- Hybrid protection mechanism
- Reduced latency using Mini-TLB
- Hardware-based security enforcement
- Suitable for secure embedded systems

---

🚀 Applications

- Secure processors
- Confidential computing
- Embedded systems security
- IoT device protection

---

📚 References

- RISC-V Privileged Architecture Specification
- Hennessy & Patterson – Computer Architecture
- Xilinx Vivado Design Suite Documentation

---

👨‍💻 Author

K. Jayaprakash
K. Sai Sreeja
J. Manoj
M. Jyothish
Electronics and Communication Engineering
VEMU Institute of Technology

---

⭐ Future Work

- Sv39 full implementation
- Multi-level page tables
- Advanced TLB replacement (LRU)
- Pipeline optimization

---

🙌 Acknowledgment

Guided by:
Ms. C.H. Rajeswari, M.Tech
Assistant Professor – ECE

---

📌 Status

✔ Completed
✔ Simulated
✔ Verified

---

⭐ If you found this useful, give a star!
