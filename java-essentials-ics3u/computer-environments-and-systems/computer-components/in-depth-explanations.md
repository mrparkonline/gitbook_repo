# In-depth Explanations

{% embed url="https://www.youtube.com/watch?v=BL4DCEp7blY" %}
How to Build a PC by LTT
{% endembed %}

## Order of Components to Choose & Important Considerations

A very good website to help you organize your build a website called: [**pcpartpicker**](https://ca.pcpartpicker.com/).

### 1. CPU Choice

I personally like to choose CPU first because it helps us narrow down choices for our build.

**The CPU choice determines:**

* **Motherboard Choice:** The socket family of the CPU will determine the type of the motherboard you buy.
* **RAM Choice:** Most modern CPUs will state their preferred RAM configurations on their specification sheet.
* **CPU Cooler Choice:** CPUs that are intended to be overclocked or just generally stronger won't come with a CPU cooler; therefore, you are expected to buy a standalone cooler.
* **GPU Choice:** Depending on the CPU chosen, the processor may not have a GPU built-in. CPUs without GPUs in them will have no output to display (monitor), so your system will need a dedicated graphics card. CPUs that have integrated GPU are called either Accelerated Processing Unit APU.

{% hint style="info" %}
The speed of CPU is determined by Hertz (Hz) most often to referred as "clock speed". The faster the speed; the faster the processing speed of the CPU.

More cores the CPU has, the CPU will be able to handle more process/applications at the same time.

A CPU Cache is often mentioned when differentiating processors because a larger cache memory helps the CPU store more important data within its own short term memory for faster processing.
{% endhint %}

### 2. Choose a Case

Choosing a case will determine the outer aesthetics of your build, but it will importantly determine the limits of what you can install as well.

**The case ...**

* will state what [_**form factors**_](#user-content-fn-1)[^1] of the motherboards it can support, so it determines your motherboard sizing.
* will have a cooler height limits, so you can only use certain air-based CPU coolers.
* will have radiator dimension limits, so you can only use certain [AIO CPU coolers](#user-content-fn-2)[^2]**.**
* will state a length limit for GPU cards, so you must get one that fits your case.
* will state how many SATA based drives you can fit in your case. This determines your long term storage options for your case.
* will state the form factor of the [**PSU**](#user-content-fn-3)[^3] that it can support; this narrows down your PSU choice as well.

### 3. Motherboard

By now you have chosen a CPU and the case. The CPU chosen will determine your the socket type the motherboard must have. The case will determine the form factor (ATX, mATX, or ITX) of your motherboard.

**Your motherboard  ...**

* will state the best memory (RAM) configurations by stating the type of RAM it supports (speed limit, the RAM generation, and channeling).
* will state the number of PCI connectors for extra component installations (graphics card, network card, and etc)
* will state the number and the type of hard drive interfaces as well

### 4. RAM

Both the CPU and the motherboard will state their preferred RAM configurations. By following what is stated from the two components, you should be able to buy a proper RAM for your system.

{% hint style="info" %}
The speed of the RAM (Hz) will determine how fast your RAM can communicate with your CPU for its processes.

The size of the RAM (GB) will determine the number of processes that can be stored for your PC.
{% endhint %}

### 5. Hard Drive

At this point, it is crucial to think about all the apps you intend to use on your machine and research  the amount of hard drive storage your PC requires.

{% hint style="info" %}
**3 Common Types of Hard Drives**

1. **NVME SSD** --> these are currently the fastest commercial drives, these often install directly onto the motherboard
2. **SATA SSD** --> these are often cheaper than NVME drives, but they will require SATA cables to install to the motherboard and it will have to be mounted to the case
3. **SATA Hard Disk Drive** --> these drives are the cheapest out of the three and often can store a lot more data than the other two; however, it sacrifices speed for greater data storage
{% endhint %}

### 6. CPU Cooler & Thermal Paste

We have installed 90% of the necessary components of the computer. If your CPU did not come with a CPU cooler, you would want to apply thermal paste (little pea amount) onto your CPU and install a CPU cooler.

### 7. GPU

If you did not choose a APU, then you will also need a dedicated GPU (a graphics card). Best way to choose a GPU is to first narrow down the size limitations of the case and then consider the applications that you need to run on your PC.

### 8. PSU

A PSU is something that is installed at the end and all of the required connectors will be connected to the motherboard, hard drives, and GPU if needed. All the components from section 1 to 7 will have their "wattage requirements" or TDP[^4]. At this point, you should be choosing a PSU with enough wattage to power your PC.

I personally recommend that you choose a PSU that has at least 100 wattage of wriggle room so that your PC can function still when it randomly uses little more power than intended. Having more wattage than the calculated maximum also allow us to upgrade our PC in the future.

{% hint style="info" %}
**Modularity:**

To make your life easier, it is often better to get a PSU where you can control which wires to be installed.&#x20;

This can range from:

* non-modular (all possible cables are attached (nonremovable) on the PSU)
* semi-modular (only the necessary cables are attached)
* fully-modular (all cables are detached)
{% endhint %}

[^1]: technical word for sizes for components

[^2]: "AiO" stands for "All in One", which means that you'll get a complete package, consisting of radiator, fan, pump, tubes and cooling unit, which reliably cools your CPU.

[^3]: Power Supply Unit

[^4]: Thermal Design Power, or TDP, is a term commonly associated with CPUs and GPUs. TDP represents the maximum amount of heat that a component can generate under a given workload
