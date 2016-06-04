# Projects

> Welcome to Wind River® Helix™ App Cloud. Now you can create, modify, and debug applications running on real hardware—in the cloud. Wind River® Helix™ App Cloud is the central place for managing your devices and projects.

> Now you can create, modify, and debug applications running on real hardware—in the cloud. Wind River® Helix™ App Cloud is the central place for managing your devices and projects.

[Wind River® Helix App Cloud](https://app.cloud.windriver.com/#/home)

## Sign Up for Free

1. Go to [https://app.cloud.windriver.com/user/register](https://app.cloud.windriver.com/user/register)
2. If already registered [https://app.cloud.windriver.com/](https://app.cloud.windriver.com/)

## Getting Started

> Getting Started. Use the New Device button in the navigation bar at the top of the page to create or register your device.

> Create a new device. Create a new device by choosing from a pre-defined list of Software Developer Kits (SDKs). New SDKs have been recently added:
> - Wind River Rocket for Intel Galileo Gen 2
> - Wind River Rocket for Simulator
> - Pulsar Linux for Minnowboard Max

> Register an existing device. Register a device that was previously created in App Cloud. The device Registration ID is dispayed in the device details pane once created.

## Video Tutorials

> These video tutorials introduce key concepts and demonstrate step-by-step processes to help you make the most of App Cloud.

- Rocket SDK Getting Started
- Rocket SDK Debugger Workflow
- Deploying Pulsar Linux to the Hardware
- Creating and Debugging a Pulsar C Application
- Creating and Debugging a Pulsar Javascript Application
- Building gzip on Pulsar - an Open Source Autoconf Project
- Building lua on Pulsar - an Open Source Makefile Project

## Wind River Rocket Intel x86 Simulator "VirtualDevice"

1. Close any Project running and terminate any Device simulation
2. Select "New Device" from upper right corner
3. From "Add a new device to App Cloud" popup window select "Create a new device from the supported SDK list"

### Device Setup

#### Add a new device to App Cloud

__Select a SDK__ Register an existing device or create a new device from a pre-defined list of Software Developer Kits (SDKs), select "Wind River Rocket for Intel x86 Simulator" then click "Next"

__Enter a Device Name__ Choose "VirtualDevice" then select "Create Device"

#### Virtual Device Start

In summary

```sh
    VirtualDevice
     Wind River Rocket for Intel x86 Simulator 1.0.0.1
     Offline Device
    Description
     A Rocket OS distribution for QEMU x86 Quark
    Documentation
     [Getting started with Rocket on QEMU x86]()
    Registration ID
    Unique ID
```

Now select

 - __Start Device Simulation__, to start your Virtual Device
 - __Terminate Device Simulation__, to stop your Virtual Device

Before moving on, __start Device Simulation__

### Application Development

#### Wind River Rocket Intel x86 Simulator "VirtualDevice", Applications Projects, Templates

> Application Projects. 
> > This is the central place to manage your projects. Click on the button below to create your first project.

Create 2 different projects by selecting "Create New Project":

1. First called "MyDiningPhilosophers" based on "Dining Philosophers" Project Template
2. Second called "MyHelloWorld" based on "Empty C Project"

#### Wind River Rocket Intel x86 Simulator "VirtualDevice", Applications Projects, MyHelloWorld

Open "MyHelloWorld" by selecting "Open" green button, "Loading your Workspace" message will appear shortly in a new web browser tab and then Could9 Workspace will be initialized.

##### __MyHelloWorld - Cloud9 Workspace__ Console "outdir/zephyr.elf - Running"

1. Go to MyHelloWorld Could9 Workspace web browser tab
2. Select "Run Project" if it is not running
3. Go to console "outdir/zephyr.elf - Running"

Full View

```sh
make 
Using /users/xe1gyq/MyHelloWorld/zephyr/arch/x86/configs/basic_minuteia_defconfig as base
Merging /users/xe1gyq/MyHelloWorld/zephyr/kernel/configs/micro.config
Merging prj_x86.conf
*
* Restart config...
*
*
* Zephyr Kernel/x86 Configuration
*
Kernel Type
  1. Nano Kernel (NANOKERNEL) (NEW)
> 2. Micro Kernel (MICROKERNEL)
choice[1-2]: *
* General Kernel Options
*
System tick frequency (in ticks/second) (SYS_CLOCK_TICKS_PER_SEC) [100] (NEW) 
System clock's h/w timer frequency (SYS_CLOCK_HW_CYCLES_PER_SEC) [25000000] 25000000
Initialize stack areas (INIT_STACKS) [N/y/?] (NEW) 
Execute in place (XIP) [N/y/?] (NEW) 
Enable ring buffers (RING_BUFFER) [N/y/?] (NEW) 
Enable event logger (EVENT_LOGGER) [N/y/?] (NEW) 
Enable profiler features (KERNEL_PROFILER) [N/y/?] (NEW) 
*
* Security Options
*
Customized security (CUSTOM_SECURITY) [N/y/?] (NEW) 
Compiler stack canaries (STACK_CANARIES) [N/y/?] (NEW) 
*
* Nanokernel Options
*
Boot banner (BOOT_BANNER) [N/y/?] (NEW) 
Interrupt latency metrics [EXPERIMENTAL] (INT_LATENCY_BENCHMARK) [N/y/?] (NEW) 
Background task stack size (in bytes) (MAIN_STACK_SIZE) [1024] (NEW) 
ISR and initialization stack size (in bytes) (ISR_STACK_SIZE) [2048] (NEW) 
Task and fiber custom data (THREAD_CUSTOM_DATA) [N/y/?] (NEW) 
Enable timeouts on nanokernel objects (NANO_TIMEOUTS) [N/y/?] (NEW) 
Enable nanokernel timers (NANO_TIMERS) [N/y/?] (NEW) 
*
* Microkernel Options
*
Microkernel server fiber (_k_server) stack size (MICROKERNEL_SERVER_STACK_SIZE) [1024] (NEW) 
Priority of the kernel service fiber (MICROKERNEL_SERVER_PRIORITY) [0] (NEW) 
Maximum priority for priority inheritance algorithm (PRIORITY_CEILING) [0] (NEW) 
Microkernel server command stack size (in packets) (COMMAND_STACK_SIZE) [64] (NEW) 
Number of command packets (NUM_COMMAND_PACKETS) [16] (NEW) 
Number of timer packets (NUM_TIMER_PACKETS) [10] (NEW) 
Number of task priorities (NUM_TASK_PRIORITIES) [16] (NEW) 
Workload monitoring [EXPERIMENTAL] (WORKLOAD_MONITOR) [N/y/?] (NEW) 
Number of task IRQ objects (MAX_NUM_TASK_IRQS) [0] (NEW) 
*
* Timer API Options
*
Task time slicing (TIMESLICING) [Y/n/?] (NEW) 
  Time slice size (in ticks) (TIMESLICE_SIZE) [0] (NEW) 
  Time slicing task priority threshold (TIMESLICE_PRIORITY) [0] (NEW) 
Task monitoring [EXPERIMENTAL] (TASK_MONITOR) [N/y/?] (NEW) 
Kernel object monitoring [EXPERIMENTAL] (OBJECT_MONITOR) [N/y/?] (NEW) 
Task and fiber monitoring [EXPERIMENTAL] (THREAD_MONITOR) [N/y/?] (NEW) 
Advanced power management (ADVANCED_POWER_MANAGEMENT) [N/y/?] (NEW) 
*
* X86 Platform Configuration options
*
Amount of RAM given to the kernel (in kb) (RAM_SIZE) [192] (NEW) 
Platform Selection
  1. Galileo Gen2 (PLATFORM_GALILEO) (NEW)
  2. IA32 with PCI (PLATFORM_IA32_PCI) (NEW)
> 3. IA32 (PLATFORM_IA32)
choice[1-3]: Intel Processor
  1. Atom (CPU_ATOM) (NEW)
> 2. Minute IA (CPU_MINUTEIA)
choice[1-2]: Enable cache flushing mechanism (CACHE_FLUSHING) [Y/?] (NEW) y
*
* Platform Capabilities
*
Advanced Idle Supported (ADVANCED_IDLE_SUPPORTED) [N/y/?] (NEW) 
EOI Handler Supported (EOI_HANDLER_SUPPORTED) [Y/?] (NEW) y
Unaligned Write Unsupported (UNALIGNED_WRITE_UNSUPPORTED) [N/y/?] (NEW) 
Lock Instruction Unsupported (LOCK_INSTRUCTION_UNSUPPORTED) [N/y/?] (NEW) 
Number of dynamic int stubs (NUM_DYNAMIC_STUBS) [0] (NEW) 
Disable PIC (PIC_DISABLE) [Y/n/?] y
*
* Processor Capabilities
*
Support IA32 legacy IO ports (IA32_LEGACY_IO_PORTS) [Y/n/?] y
Detect cache line size at runtime (CACHE_LINE_SIZE_DETECT) [Y/n/?] (NEW) 
Detect support of CLFLUSH instruction at runtime (CLFLUSH_DETECT) [Y/n/?] (NEW) 
*
* Floating Point Options
*
Floating point instructions (FLOAT) [N/y/?] (NEW) 
*
* x86 Core Options
*
No Asynchronous Interrupts (NO_ISRS) [N/y/?] (NEW) 
Enable nested interrupts (NO_NESTED_INTERRUPTS) [N/y/?] (NEW) 
*
* Memory Layout Options
*
Number of IDT vectors (IDT_NUM_VECTORS) [256] (NEW) 
Number of spare GDT entries (NUM_GDT_SPARE_ENTRIES) [0] (NEW) 
Physical load address (PHYS_LOAD_ADDR) [0x00100000] (NEW) 
Reboot implementation
> 1. Use the RST_CNT register (REBOOT_RST_CNT) (NEW)
choice[1]: 1
*
* Device Drivers
*
Simple UART driver (UART_SIMPLE) [N/y/?] (NEW) 
*
* Console drivers
*
Console drivers (CONSOLE) [Y/n] y
  Enable console input handler (CONSOLE_HANDLER) [Y/?] (NEW) y
  Use UART for console (UART_CONSOLE) [Y/n/?] y
    UART Console Index (UART_CONSOLE_INDEX) [0] (NEW) 
    UART Console Baud Rate (UART_CONSOLE_BAUDRATE) [115200] (NEW) 
  Use RAM console (RAM_CONSOLE) [N/y/?] (NEW) 
  Inter-processor Interrupt console sender (IPI_CONSOLE_SENDER) [N/y/?] (NEW) 
  Inter-processor interrupt console receiver (IPI_CONSOLE_RECEIVER) [N/y/?] (NEW) 
*
* Serial Drivers
*
Serial Drivers (SERIAL) [Y/n/?] y
  *
  * Serial Port Options
  *
  Serial interrupt level (SERIAL_INTERRUPT_LEVEL) [Y/n/?] (NEW) 
  Serial interrupt low (SERIAL_INTERRUPT_LOW) [N/y/?] (NEW) 
  Interrupt driven UART support (UART_INTERRUPT_DRIVEN) [Y/?] (NEW) y
  NS16550 serial driver (NS16550) [Y/n/?] y
  K20 serial driver (K20_UART) [N/y/?] (NEW) 
  Stellaris serial driver (STELLARIS_UART) [N/y/?] (NEW) 
*
* Interrupt Controllers
*
LOAPIC (LOAPIC) [Y/?] y
  LOAPIC Debug (LOAPIC_DEBUG) [N/y/?] (NEW) 
  Local APIC Base Address (LOAPIC_BASE_ADDRESS) [0xFEE00000] (NEW) 
  IO-APIC (IOAPIC) [Y/?] (NEW) y
    IO-APIC Debugging (IOAPIC_DEBUG) [N/y/?] (NEW) 
    IO-APIC Base Address (IOAPIC_BASE_ADDRESS) [0xFEC00000] (NEW) 
    Number of Redirection Table Entries available (IOAPIC_NUM_RTES) [24] (NEW) 
*
* Timer Drivers
*
HPET timer (HPET_TIMER) [Y/n/?] y
  HPET timer legacy emulation mode (HPET_TIMER_LEGACY_EMULATION) [Y/n/?] y
  Enable HPET debug output (HPET_TIMER_DEBUG) [N/y/?] (NEW) 
  HPET Base Address (HPET_TIMER_BASE_ADDRESS) [0xFED00000] (NEW) 
  HPET Timer IRQ (HPET_TIMER_IRQ) [2] 2
  HPET Timer IRQ Priority (HPET_TIMER_IRQ_PRIORITY) [4] (NEW) 
  HPET Interrupt Trigger Condition
  > 1. Falling Edge (HPET_TIMER_FALLING_EDGE) (NEW)
    2. Rising Edge (HPET_TIMER_RISING_EDGE)
    3. Level High (HPET_TIMER_LEVEL_HIGH) (NEW)
    4. Level Low (HPET_TIMER_LEVEL_LOW)
  choice[1-4]: LOAPIC timer (LOAPIC_TIMER) [N/y/?] (NEW) 
API to disable system clock (SYSTEM_CLOCK_DISABLE) [Y/?] (NEW) y
*
* Random Generation Configuration
*
Custom random generator (RANDOM_GENERATOR) [N/y/?] (NEW) 
  Non-random number generator (TEST_RANDOM_GENERATOR) [N/y/?] (NEW) 
*
* PCI Settings
*
Enable PCI (PCI) [N/y/?] (NEW) 
*
* GPIO Drivers
*
GPIO Drivers (GPIO) [N/y/?] (NEW) 
Shared interrupt driver (SHARED_IRQ) [N/y/?] (NEW) 
Shared interrupt instance 1 (SHARED_IRQ_1) [N/y/?] (NEW) 
*
* SPI hardware bus support
*
SPI hardware bus support (SPI) [N/y/?] (NEW) 
*
* I2C Drivers
*
I2C Drivers (I2C) [N/y/?] (NEW) 
*
* PWM (Pulse Width Modulation) Drivers
*
PWM (Pulse Width Modulation) Drivers (PWM) [N/y/?] (NEW) 
*
* Enable platform pinmux driver
*
Enable platform pinmux driver (PINMUX) [N/y] (NEW) 
*
* ADC drivers
*
ADC drivers (ADC) [N/y/?] (NEW) 
*
* Cryptography
*
*
* Compile and Link Features
*
The kernel binary name (KERNEL_BIN_NAME) [zephyr] (NEW) 
Custom linker scripts provided (HAVE_CUSTOM_LINKER_SCRIPT) [N/y/?] (NEW) 
Cross-compiler tool prefix (CROSS_COMPILE) [] (NEW) 
Task-aware debugging with GDB (GDB_INFO) [N/y/?] (NEW) 
Allow linking with --whole-archive (LINK_WHOLE_ARCHIVE) [N/y/?] (NEW) 
Custom compiler options (COMPILER_OPT) [-O0 -g] -O0 -g
Cross-compiler variant name (TOOLCHAIN_VARIANT) [] (NEW) 
C Library
> 1. Build minimal c library (MINIMAL_LIBC) (NEW)
  2. Build with newlib c library (NEWLIB_LIBC) (NEW)
choice[1-2]: Build additional libc functions [EXPERIMENTAL] (MINIMAL_LIBC_EXTENDED) [N/y/?] (NEW) 
*
* Debugging Options
*
Build kernel with debugging enabled (DEBUG) [N/y/?] (NEW) 
Send printk() to console (PRINTK) [Y/n/?] (NEW) 
Send stdout to console (STDOUT_CONSOLE) [Y/n/?] y
Send stdout at the earliest stage possible (EARLY_CONSOLE) [N/y/?] (NEW) 
Enable __ASSERT() macro (ASSERT) [N/y/?] (NEW) 
Enable system debugging information (DEBUG_INFO) [Y/?] (NEW) y
Enable GDB Server [EXPERIMENTAL] (GDB_SERVER) [Y/n/?] y
  Maximum number of GDB Server Software breakpoints (GDB_SERVER_MAX_SW_BP) [100] (NEW) 
  Enable GDB interrupt mode (GDB_SERVER_INTERRUPT_DRIVEN) [Y/n/?] (NEW) 
  Enable the bootloader mode (GDB_SERVER_BOOTLOADER) [N/y/?] (NEW) 
*
* Safe memory access
*
Enable safe memory access (MEM_SAFE) [Y/?] (NEW) y
  Safe memory access implementation
  > 1. Software validation of memory access within memory regions (MEM_SAFE_CHECK_BOUNDARIES) (NEW)
  choice[1]: 1
Number of safe memory access regions that can be added at runtime (MEM_SAFE_NUM_EXTRA_REGIONS) [0] (NEW) 
Boot using Linux kexec() system call (BOOTLOADER_KEXEC) [N/y/?] (NEW) 
Generic boot loader support (BOOTLOADER_UNKNOWN) [Y/?] (NEW) y
*
* System Monitoring Options
*
Enable performance metrics [EXPERIMENTAL] (PERFORMANCE_METRICS) [N/y/?] (NEW) 
Reboot functionalities (REBOOT) [Y/?] (NEW) y
#
# configuration written to .config
#
make[1]: Entering directory '/users/xe1gyq/MyHelloWorld/zephyr'
make[2]: Entering directory '/users/xe1gyq/MyHelloWorld/outdir'
  GEN     ./Makefile
scripts/kconfig/conf --silentoldconfig Kconfig
  Using /users/xe1gyq/MyHelloWorld/zephyr as source for kernel
  GEN     ./Makefile
  CHK     include/generated/version.h
  UPD     include/generated/version.h
  HOSTCC  scripts/gen_idt/gen_idt.o
  HOSTLD  scripts/gen_idt/gen_idt
  CHK     misc/generated/configs.c
  UPD     misc/generated/configs.c
  CHK     include/generated/offsets.h
  UPD     include/generated/offsets.h
  CHK     misc/generated/sysgen/prj.mdef
  UPD     misc/generated/sysgen/prj.mdef
  LD      lib/libc/minimal/source/stdlib/built-in.o
  CC      lib/libc/minimal/source/stdout/fprintf.o
  CC      lib/libc/minimal/source/stdout/prf.o
  CC      lib/libc/minimal/source/stdout/sprintf.o
  CC      lib/libc/minimal/source/stdout/stdout_console.o
  LD      lib/libc/minimal/source/stdout/built-in.o
  CC      lib/libc/minimal/source/string/string.o
  LD      lib/libc/minimal/source/string/built-in.o
  LD      lib/libc/minimal/source/built-in.o
  LD      lib/libc/minimal/built-in.o
  LD      lib/libc/built-in.o
  LD      lib/built-in.o
  CC      arch/x86/core/gdt.o
  CC      arch/x86/core/thread.o
  CC      arch/x86/core/fatal.o
  AS      arch/x86/core/cpuhalt.o
  AS      arch/x86/core/excstub.o
  AS      arch/x86/core/swap.o
  AS      arch/x86/core/intboiexit.o
  AS      arch/x86/core/msr.o
  CC      arch/x86/core/excconnect.o
  CC      arch/x86/core/inthndlset.o
  CC      arch/x86/core/sys_fatal_error_handler.o
  AS      arch/x86/core/crt0.o
  AS      arch/x86/core/driver_static_irq_stubs.o
  CC      arch/x86/core/atomic_nolock.o
  AS      arch/x86/core/atomic.o
  AS      arch/x86/core/cache_s.o
  CC      arch/x86/core/cache.o
  CC      arch/x86/core/intconnect.o
  AS      arch/x86/core/intstub.o
  CC      arch/x86/core/strtask.o
  CC      arch/x86/core/x86_reboot.o
  CC      arch/x86/core/debug/debug_frames.o
  LD      arch/x86/core/debug/built-in.o
  LD      arch/x86/core/built-in.o
  CC      arch/x86/debug/gdb_arch.o
  LD      arch/x86/debug/built-in.o
  CC      arch/x86/platforms/ia32/ia32_config.o
  CC      arch/x86/platforms/ia32/ia32.o
  LD      arch/x86/platforms/ia32/built-in.o
  LD      arch/x86/built-in.o
  LD      arch/built-in.o
  CC      kernel/microkernel/k_task.o
  CC      kernel/microkernel/k_idle.o
  CC      kernel/microkernel/k_init.o
  CC      kernel/microkernel/k_command_packet.o
  CC      kernel/microkernel/k_move_data.o
  CC      kernel/microkernel/k_ticker.o
  CC      kernel/microkernel/k_memory_map.o
  CC      kernel/microkernel/k_memory_pool.o
  CC      kernel/microkernel/k_irq.o
  CC      kernel/microkernel/k_nop.o
  CC      kernel/microkernel/k_offload.o
  CC      kernel/microkernel/k_event.o
  CC      kernel/microkernel/k_mailbox.o
  CC      kernel/microkernel/k_mutex.o
  CC      kernel/microkernel/k_fifo.o
  CC      kernel/microkernel/k_semaphore.o
  CC      kernel/microkernel/k_timer.o
  CC      kernel/microkernel/k_pipe_buffer.o
  CC      kernel/microkernel/k_pipe.o
  CC      kernel/microkernel/k_pipe_get.o
  CC      kernel/microkernel/k_pipe_put.o
  CC      kernel/microkernel/k_pipe_util.o
  CC      kernel/microkernel/k_pipe_xfer.o
  CC      kernel/microkernel/k_server.o
  LD      kernel/microkernel/built-in.o
  CC      kernel/nanokernel/nano_fiber.o
  CC      kernel/nanokernel/nano_lifo.o
  CC      kernel/nanokernel/nano_fifo.o
  CC      kernel/nanokernel/nano_stack.o
  CC      kernel/nanokernel/nano_sys_clock.o
  CC      kernel/nanokernel/nano_context.o
  CC      kernel/nanokernel/nano_init.o
  CC      kernel/nanokernel/nano_sema.o
  CC      misc/generated/configs.o
  CC      misc/generated/sysgen/kernel_main.o
  LD      misc/generated/sysgen/built-in.o
  LD      misc/generated/built-in.o
  LD      misc/built-in.o
  CC      debug/gdb_server.o
  LD      debug/built-in.o
  CC      ../src/../src/main.o
  LD      ../src/built-in.o
  CC      drivers/console/uart_console.o
  LD      drivers/console/built-in.o
  CC      drivers/interrupt_controller/i8259.o
  CC      drivers/interrupt_controller/system_apic.o
  CC      drivers/interrupt_controller/loapic_intr.o
  CC      drivers/interrupt_controller/ioapic_intr.o
  LD      drivers/interrupt_controller/built-in.o
  LD      drivers/random/built-in.o
  CC      drivers/serial/serial.o
  CC      drivers/serial/ns16550.o
  LD      drivers/serial/built-in.o
  CC      drivers/timer/hpet.o
  CC      drivers/timer/sys_clock_init.o
  LD      drivers/timer/built-in.o
  LD      drivers/built-in.o
  LINK    zephyr
  LD      zephyr.elf
  GEN     .version
  SIDT    zephyr.elf
  BIN     zephyr.bin
  SYSMAP  System.map
make[2]: Leaving directory '/users/xe1gyq/MyHelloWorld/outdir'
make[1]: Leaving directory '/users/xe1gyq/MyHelloWorld/zephyr'
Loading /users/xe1gyq/MyHelloWorld//outdir/zephyr.elf on target...  done
Starting application...  done
Application is now running
```

Short View

```sh
    make
    * Zephyr Kernel/x86 Configuration
    * General Kernel Options
    * Security Options
    * Nanokernel Options
    * Microkernel Options
    * Timer API Options
    * X86 Platform Configuration options
    * Platform Capabilities
    * Processor Capabilities
    * Floating Point Options
    * x86 Core Options
    * Memory Layout Options
    * Device Drivers
    * Console drivers
    * Serial Drivers
    * Interrupt Controllers
    * Timer Drivers
    * Random Generation Configuration
    * PCI Settings
    * GPIO Drivers
    * SPI hardware bus support
    * I2C Drivers
    * PWM (Pulse Width Modulation) Drivers
    * Enable platform pinmux driver
    * ADC drivers
    * Cryptography
    * Compile and Link Features
    * Debugging Options
    * Safe memory access
    * System Monitoring Options
    # configuration written to .config
    Using /users/xe1gyq/MyHelloWorld/zephyr as source for kernel
      SYSMAP  System.map
    make[2]: Leaving directory '/users/xe1gyq/MyHelloWorld/outdir'
    make[1]: Leaving directory '/users/xe1gyq/MyHelloWorld/zephyr'
    Loading /users/xe1gyq/MyHelloWorld//outdir/zephyr.elf on target...  done
    Starting application...  done
    Application is now running
```

##### __MyHelloWorld - Cloud9 Workspace__ Console "bash - xe1gyq@helix-app-cloud:~/MyHelloWorld$"

1. Go to MyHelloWorld Could9 Workspace web browser tab
2. Select "Run Project" if it is not running
3. Clic on "+" under Console Area and Select "New Terminal"
3. Under terminal "bash - xe1gyq@helix-app-cloud:~/MyHelloWorld" and type the following commands

```sh
    xe1gyq@helix-app-cloud:~/MyHelloWorld$ pwd
    /users/xe1gyq/MyHelloWorld
    xe1gyq@helix-app-cloud:~/MyHelloWorld$ ls ..
    CProject   MyDiningPhilosophers  dining-philosophers-sample-app  lost+found
    MyDevices  MyHelloWorld          home                            mthread.d
    xe1gyq@helix-app-cloud:~/MyHelloWorld$ 
```

###### Make Menuconfig

```sh
xe1gyq@helix-app-cloud:~/MyHelloWorld$ make menuconfig
make[1]: Entering directory '/users/xe1gyq/MyHelloWorld/zephyr'
make[2]: Entering directory '/users/xe1gyq/MyHelloWorld/outdir'
  GEN     ./Makefile
  HOSTCC  scripts/kconfig/mconf.o
  HOSTCC  scripts/kconfig/lxdialog/checklist.o
  HOSTCC  scripts/kconfig/lxdialog/util.o
  HOSTCC  scripts/kconfig/lxdialog/inputbox.o
  HOSTCC  scripts/kconfig/lxdialog/textbox.o
  HOSTCC  scripts/kconfig/lxdialog/yesno.o
  HOSTCC  scripts/kconfig/lxdialog/menubox.o
  HOSTLD  scripts/kconfig/mconf
scripts/kconfig/mconf Kconfig


*** End of the configuration.
*** Execute 'make' to start the build or try 'make help'.

make[2]: Leaving directory '/users/xe1gyq/MyHelloWorld/outdir'
make[1]: Leaving directory '/users/xe1gyq/MyHelloWorld/zephyr'
xe1gyq@helix-app-cloud:~/MyHelloWorld$ 
```

###### Make

```sh
xe1gyq@helix-app-cloud:~/MyHelloWorld$ make
make[1]: Entering directory '/users/xe1gyq/MyHelloWorld/zephyr'
make[2]: Entering directory '/users/xe1gyq/MyHelloWorld/outdir'
  Using /users/xe1gyq/MyHelloWorld/zephyr as source for kernel
  GEN     ./Makefile
  CHK     include/generated/version.h
  CHK     misc/generated/configs.c
  CHK     include/generated/offsets.h
  CHK     misc/generated/sysgen/prj.mdef
make[2]: Leaving directory '/users/xe1gyq/MyHelloWorld/outdir'
make[1]: Leaving directory '/users/xe1gyq/MyHelloWorld/zephyr'
xe1gyq@helix-app-cloud:~/MyHelloWorld$ 
```

###### Upper Directories

```sh
xe1gyq@helix-app-cloud:~/MyHelloWorld$ ls
Makefile  MyDevices  outdir  prj.mdef  prj_x86.conf  src  zephyr
xe1gyq@helix-app-cloud:~/MyHelloWorld$ ls src/
Makefile  built-in.o  main.c  main.o
xe1gyq@helix-app-cloud:~/MyHelloWorld$ ls zephyr/
Kbuild   Kconfig.zephyr  Makefile.inc  arch           debug    include  lib   net     scripts
Kconfig  Makefile        README.txt    buildDefaults  drivers  kernel   misc  schema  zephyr-env.sh
xe1gyq@helix-app-cloud:~/MyHelloWorld$ ls outdir/
Makefile    drivers             irq_int_vector_map.o  misc         zephyr      zephyr.lst
System.map  final-linker.cmd    kernel                scripts      zephyr.bin  zephyr.map
arch        include             lib                   source       zephyr.elf  zephyr.strip
debug       int_vector_alloc.o  linker.cmd            staticIdt.o  zephyr.lnk
```

#### Wind River Rocket Intel x86 Simulator "VirtualDevice", Applications Projects, MyDiningPhilosophers

```sh
xe1gyq@helix-app-cloud:~/MyHelloWorld$ cd ../MyDiningPhilosophers/
xe1gyq@helix-app-cloud:~/MyDiningPhilosophers$ make
make[1]: Entering directory '/users/xe1gyq/MyHelloWorld/zephyr'
make[2]: Entering directory '/users/xe1gyq/MyDiningPhilosophers/outdir'
  Using /users/xe1gyq/MyHelloWorld/zephyr as source for kernel
  GEN     ./Makefile
  CHK     include/generated/version.h
  CHK     misc/generated/configs.c
  CHK     include/generated/offsets.h
  CHK     misc/generated/sysgen/prj.mdef
make[2]: Leaving directory '/users/xe1gyq/MyDiningPhilosophers/outdir'
make[1]: Leaving directory '/users/xe1gyq/MyHelloWorld/zephyr'
xe1gyq@helix-app-cloud:~/MyDiningPhilosophers$ 
```

#### Wind River Rocket Intel x86 Simulator "VirtualDevice", Applications Projects, Github

You can import existing projects from Github, let's import philosophers example

```sh
    xe1gyq@helix-app-cloud:~$ git clone https://github.com/wind-river-rocket/dining-philosophers-sample-app.git
```

- [Wind River Rocket Sample Applications Github](https://github.com/wind-river-rocket)

## Wind River Rocket Galileo 2 "Galileo2Device"

1. Close any Project running and terminate any Device simulation
2. Select "New Device" from upper right corner
3. From "Add a new device to App Cloud" popup window select "Create a new device from the supported SDK list"

### Device Setup

#### Add a new device to App Cloud

__Select the SDK__ Register an existing device or create a new device from a pre-defined list of Software Developer Kits (SDKs), select "Wind River Rocket for Intel Galileo Gen 2" then click "Next"

__Enter a Device Name__ Choose "Galileo2Device" then select "Create Device"

#### Galileo 2 Device Start

In summary we need to:

- Deploy Wind River Rocket for Intel Galileo Gen2 on Galileo2Device
- Connect Device Virtual Gateway

Check Galileo2Device Summary

```sh
    Galileo2Device
     Wind River Rocket for Intel Galileo Gen2 1.0.0.1
     Offline Gateway
     Offline Device
    Description
     Designed for makers, students, educators, and DIY electronics enthusiasts, the Intel® Galileo Gen 2 board is an Arduino certified development and prototyping board based on Intel® ..
    Documentation
     [Hide deployment instructions]()
     [Getting started with Rocket on Galileo Gen 2]()
    Registration ID
    Unique ID
```

__Follow the instructions below to deploy Wind River Rocket for Intel Galileo Gen2 on Galileo2Device__

Click on "Generate and Download Device Image" and follow onscreen steps:

    Use a Galileo Gen 2 SD card to boot the Rocket OS as follows:
    1. To download the OS, click Generate & Download Device Image.
    2. Format a 1 GB or larger SD card as a FAT32 file system.
    3. Use any zip utility to extract the OS image to the SD Card.
    4. If you have not already done so, power off your board.
    5. Insert the SD card and power on the board.

__Device Virtual Gateway not connected__

Follow onscreen steps:

    You have to run a Virtual Gateway application on your desktop to use this device.
    The Virtual Gateway is specific to a device; you must download and run a different Virtual Gateway for each different device.

    To run the Virtual Gateway you must:
    - Download it for your device by clicking on the Download button
    - Unzip the archive on your host, and double click on the launch script Galileo2Device-virtual-gateway.sh
    - When prompted, enter the serial port connected to your device

When running "Galileo2Device-virtual-gateway.sh" this is the log seen:

```sh
    xe1gyq@jessie:~/Downloads/IntelGalileoGateway/Galileo2Device-virtual-gateway$ sh Galileo2Device-virtual-gateway.sh 
    
    Helix App Cloud Virtual Gateway for device Galileo2Device on server https://app.cloud.windriver.com
    Version: 0.2
    
    Provide the name of the serial port your device is connected to:
    Serial port: /dev/ttyUSB0
    Connecting serial port with serial parameters (from the SDK): 115200-8-N-1-N
    
    Configure a SOCKS v5 proxy to access App Cloud server (y/n, default is n): n
    
    Starting the Virtual Gateway for Galileo2Device.
    Connecting to Helix App Cloud server...
    Connection with Helix App Cloud server has been established
    Received connection request for serial port "/dev/ttyUSB0"
    Successfully opened serial port "/dev/ttyUSB0"
```

Check again Galileo2Device Summary

```sh
    Galileo2Device
     Wind River Rocket for Intel Galileo Gen2 1.0.0.1
     Online Gateway
     Online Device
```

### Application Development

#### Wind River Rocket Galileo 2 "Galileo2Device", Applications Projects, Templates

> Application Projects. This is the central place to manage your projects. Click on the button below to create your first project.

Create a project by selecting "Create New Project". you will find several templates:

- Analog Red/Write (ADC/PWM)
- Digital Read/write (GPIO)
- Dining Philosophers
- Empty C Project
- Grove-LCD
- HTTP Server using LWIP Project

Choose "Grove-LCD" template and name it "MyGrove-LCD"

Open "MyGrove-LCD" by selecting "Open" green button, "Loading your Workspace" message will appear shortly in a new web browser tab and then Could9 Workspace will be initialized

##### __MyGrove-LCD Cloud9 Workspace__ Console "outdir/zephyr.elf - Running"

1. Go to MyGrove-LCD Could9 Workspace web browser tab
2. Select "Run Project" if it is not running
3. Go to console "outdir/zephyr.elf - Running"

```sh
    make
    make
    make[1]: Entering directory '/users/xe1gyq/MyGrove-LCD/zephyr'
    make[2]: Entering directory '/users/xe1gyq/MyGrove-LCD/outdir'
      Using /users/xe1gyq/MyGrove-LCD/zephyr as source for kernel
      GEN     ./Makefile
      CHK     include/generated/version.h
      CHK     misc/generated/configs.c
      CHK     include/generated/offsets.h
      CHK     misc/generated/sysgen/prj.mdef
    make[2]: Leaving directory '/users/xe1gyq/MyGrove-LCD/outdir'
    make[1]: Leaving directory '/users/xe1gyq/MyGrove-LCD/zephyr'
    Loading /users/xe1gyq/MyGrove-LCD//outdir/zephyr.elf on target...  done
    Starting application...  done
    Application is now running
    Pin 0 configured
    Pin 1 configured
    Pin 2 configured
    Pin 3 configured
    Pin 4 configured
    Pin 5 configured
    Pin 6 configured
    Pin 7 configured
    Pin 8 configured
    Pin 9 configured
    Pin 10 configured
    Pin 11 configured
    Pin 12 configured
    Pin 13 configured
    Pin 14 configured
    Pin 15 configured
    Pin 16 configured
    Pin 17 configured
    Pin 18 configured
    Pin 19 configured
    Initialize LCD ... done
    Button on D3 = 0
```

##### __MyGrove-LCD Cloud9 Workspace__ Console "bash - helix app cloud"

1. Go to MyGrove-LCD Could9 Workspace web browser tab
2. Select "Run Project" if it is not running
3. Clic on "+" under Console Area and Select "New Terminal"
3. Under terminal "bash - xe1gyq@helix-app-cloud:~/MyGrove-LCD" and type the following commands

```sh
    xe1gyq@helix-app-cloud:~/MyGrove-LCD$ ls
    Makefile  MyDevices  README.txt  prj.mdef  prj_x86.conf  src  zephyr
    xe1gyq@helix-app-cloud:~/MyGrove-LCD$ make menuconfig
```

## Wind River Pulsar Intel x86 Simulator "VirtualDevice"

If you have a Minnowboard MAX the work with Wind River Pulsar