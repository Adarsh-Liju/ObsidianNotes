![[UE20CS351_Unit2_Slides.pdf]]
## Virtualization Software Techniques

## **Trap and Emulate**

### Basic Idea
1. Trap to **hypervisor** when the **VM** tries to execute an **instruction** that could change the **state of the system** 
2. **Emulate** execution of this instruction in **Hypervisor**
3. This will not impact the **hardware** of the system and provides **isolation**

## Why **trap and emulate**

1. There are two modes of CPU operations
	1. User Mode (Ring 3)
	2. Privilaged Mode (Ring 0)
2. An attempt to execute system instructions in user mode creates a **trap** also called **general protection fault (gpf)**
3. For example , access to **system state** triggers a **trap**

## Solution

1. Run the VM in (User Mode)Ring 3 and the Hypervisor in (Privilaged Mode) Ring 0. 
2. Anytime the VM tries to execute a system instruction or tries to execute a system state , traps to VMM(hypervisor)
3. The VMM then emulates it , then goes back to normal state

## Issues/Problems

1. Performance Overhead - traping costs are very high
2. Not all architectures support it
3. Some X86 instructions which change hardware state run in privilaged and non - privilaged states

## **Binary Translation**

1. It is one specific approach to implementing **full virtualization** that does not require **hardware virtualization** features
2. It involves the hypervisor examining the **virtual guest code** for **"unsafe or sensitive"** but **unprivilaged instructions** and translating these to **"safe"** or **privilaged equivalents** and then executing the **translated code**
3. It supports **x86**

## **Xen**
![[Xen.png]]
- Paravirtualization Hypervisor
- VM's called **domain
	- Dom0 - **Domain0**
		- Special Domain, essentially the **host OS** 
		- Handles all **I/O**
	- Xen Hypervisor
		- All Functions other than I/O
		- Trap and Emulate
		- Binary Translation
		- Sensitive instructions

### **KVM** Architecture
- Extends **Linux Kernel** Architecture to add hypervisor functionality
	- **Leverage** Linux Code
	- Each **VM** appears as a Linux Process

# Virtualization - **Memory** and **I/O**

## Page Walking

1. Software page walker is a OS handler that 