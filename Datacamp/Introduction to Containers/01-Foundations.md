# Introduction to Containers


Physical machines have limitations when performing multiple tasks, they are expensive, maintenance can be a hassle , and scaling is inflexible. Virtual machines (VMs) address these limitations. A VM is a simulated computer system running *inside* another physical computer. Each VM has its own independent operating system and applications, completely isolated from other VMs on the same host.

- Maximize hardware usage by running multiple VMs on a single host, leading to cost efficiencies and sustainable resource use.
- Upgrade hardware resources for a VM without purchasing new physical hardware, provided the host has sufficient capacity.
- VMs on the same host are fully isolated, preventing threats from spreading between them and enhancing security and stability.
- Seamlessly run different operating systems on the same host machine.

>[!NOTE]
>Virtualization is the process of creating a virtual version of a computing resource. Full virtualization is the most advanced level, where an entire computer system is virtualized, resulting in a VM. Other levels of virtualization involve specific components, not an entire VM.

Beyond virtualizing an entire computer, virtualization can also occur at the component level. OS-level virtualization, also known as containerization, virtualizes the operating system itself. It does not virtualize the underlying hardware or the OS kernel. Instead, it creates isolated user spaces(called containers) that interact with the host's non-virtualized OS kernel. The OS kernel allocates hardware resources to these user spaces as needed.

> [!NOTE]
> **Definition of Containerization:**
The process of packaging an application and all its necessary dependencies into a container, which is an isolated environment managed by the OS kernel.

Multiple applications can run reliably on a single host OS without each needing its own dedicated OS. Each application in its container has its own environment, preventing dependency conflicts. Containers do not interfere with other processes on the same host. A crash in one container won't affect others. Containers are highly portable. Because they bundle all dependencies, they behave identically when moved and run on different host machines. Containers don't need to load an entire operating system, leading to rapid startup times. This is crucial for high availability and quick scaling.

---