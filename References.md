# Reading materials

## Selection of Operating System Papers

见 [教学计划](Schedule.md)

## UNIX

* [Youtube Unix intro](https://www.youtube.com/watch?v=tc4ROCJYbm0)
* [The UNIX Time-Sharing System](http://citeseer.ist.psu.edu/10962.html), [Dennis M. Ritchie](http://cm.bell-labs.com/who/dmr/) and [Ken L.Thompson](http://cm.bell-labs.com/who/dmr/),. Bell System Technical Journal 57, number 6, part 2 (July-August 1978) pages 1905-1930. ([local copy](https://pdos.csail.mit.edu/6.828/2018/readings/ritchie78unix.pdf)) You read this paper in 6.033.
* [The Evolution of the Unix Time-sharing System](http://www.read.seas.harvard.edu/~kohler/class/aosref/ritchie84evolution.pdf), Dennis M. Ritchie, 1979.
* The C programming language (second edition) by Kernighan and Ritchie. Prentice Hall, Inc., 1988. ISBN 0-13-110362-8, 1998.

## x86 Emulation
* [QEMU](http://www.qemu.org/) - A fast and popular x86 platform and CPU emulator.
    * User manual(http://wiki.qemu.org/Qemu-doc.html)
* [Bochs](http://bochs.sourceforge.net/) - A more mature, but quirkier and much slower x86 emulator. Bochs is generally a more faithful emulator of real hardware than QEMU.
    * [User manual](http://bochs.sourceforge.net/doc/docbook/user/index.html)
    * [Debugger reference](http://bochs.sourceforge.net/doc/docbook/user/internal-debugger.html)

## x86 Assembly Language
* [PC Assembly Language](http://www.drpaulcarter.com/pcasm/), Paul A. Carter, November 2003. [(local copy)](https://pdos.csail.mit.edu/6.828/2018/readings/pcasm-book.pdf)
* Intel 80386 Programmer's Reference Manual, 1987 (HTML). (local copy - PDF) (local copy - HTML)
* Much shorter than the full current Intel Architecture manuals below, but describes all processor features used in 6.828.
* IA-32 Intel Architecture Software Developer's Manuals, Intel, 2007. Local copies:
    * Volume I: Basic Architecture
    * Volume 2A: Instruction Set Reference, A-M
    * Volume 2B: Instruction Set Reference, N-Z
    * Volume 3A: System Programming Guide, Part 1
    * Volume 3B: System Programming Guide, Part 2
* Multiprocessor references:
    * MP specification
    * IO APIC
* AMD64 Architecture Programmer's Manual.
Covers both the "classic" 32-bit x86 architecture and the new 64-bit extensions supported by the latest AMD and Intel processors.
* Writing inline assembly language with GCC:
    * Brennan's Guide to Inline Assembly, Brennan "Mr. Wacko" Underwood
    * Inline assembly for x86 in Linux, Bharata B. Rao, IBM
    * GCC-Inline-Assembly-HOWTO, Sandeep.S
* Loading x86 executables in the ELF format:
    * Tool Interface Standard (TIS) Executable and Linking Format (ELF).
The definitive standard for the ELF format.
    * Wikipedia page has a short description.

## PC Hardware Programming
* General PC architecture information
    * Phil Storrs PC Hardware book, Phil Storrs, December 1998.
    * Bochs technical hardware specifications directory.
* General BIOS and PC bootstrap
    * BIOS Services and Software Interrupts, Roger Morgan, 1997.
    * "El Torito" Bootable CD-ROM Format Specification, Phoenix/IBM, January 1995.
* VGA display - kern/console.c
    * VESA BIOS Extension (VBE) 3.0, Video Electronics Standards Association, September 1998. (local copy)
    * VGADOC, Finn Thøgersen, 2000. (local copy - text) (local copy - ZIP)
    * Free VGA Project, J.D. Neal, 1998.
* Keyboard and Mouse - kern/console.c
    * Adam Chapweske's resources.
* 8253/8254 Programmable Interval Timer (PIT) - inc/timerreg.h
    * 82C54 CHMOS Programmable Interval Timer, Intel, October 1994. (local copy)
    * Data Solutions 8253/8254 Tutorial, Data Solutions.
* 8259/8259A Programmable Interrupt Controller (PIC) - kern/picirq.*
    * 8259A Programmable Interrupt Controller, Intel, December 1988.
* Real-Time Clock (RTC) - kern/kclock.*
    * Phil Storrs PC Hardware book, Phil Storrs, December 1998. In particular:
        * Understanding the CMOS
        * A list of what is in the CMOS
    * CMOS Memory Map, Padgett Peterson, May 1996.
    * M48T86 PC Real-Time Clock, ST Microelectronics, April 2004. (local copy)
* 16550 UART Serial Port - kern/console.c
    * PC16550D Universal Asynchronous Receiver/Transmitter with FIFOs, National Semiconductor, 1995.
    * Technical Data on 16550, Byterunner Technologies.
    * Interfacing the Serial / RS232 Port, Craig Peacock, August 2001.
* IEEE 1284 Parallel Port - kern/console.c
    * Parallel Port Central, Jan Axelson.
    * Parallel Port Background, Warp Nine Engineering.
    * IEEE 1284 - Updating the PC Parallel Port, National Instruments.
    * Interfacing the Standard Parallel Port, Craig Peacock, August 2001.
* IDE hard drive controller - fs/ide.c
    * AT Attachment with Packet Interface - 6 (working draft), ANSI, December 2001.
    * Programming Interface for Bus Master IDE Controller, Brad Hosler, Intel, May 1994.
    * The Guide to ATA/ATAPI documentation, Constantine Sapuntzakis, January 2002.
* Sound cards (not supported in 6.828 kernel, but you're welcome to do it as a challenge problem!)
    * Sound Blaster Series Hardware Programming Guide, Creative Technology, 1996.
    * 8237A High Performance Programmable DMA Controller, Intel, September 1993.
    * Sound Blaster 16 Programming Document, Ethan Brodsky, June 1997.
    * Sound Programming, Inverse Reality.
* E100 Network Interface Card
    * Intel 8255x 10/100 Mbps Ethernet Controller Family Open Source Software Developer Manual
    * 82559ER Fast Ethernet PCI Controller Datasheet
* E1000 Network Interface Card
    * PCI/PCI-X Family of Gigabit Ethernet Controllers Software Developer's Manual