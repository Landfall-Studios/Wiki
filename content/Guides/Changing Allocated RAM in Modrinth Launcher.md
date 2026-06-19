---
dg-publish: true
---
## Overview

Minecraft modpacks often need more RAM than what is allocated by default. If you're experiencing lag, stuttering, or "out of memory" crashes, increasing your RAM allocation can help significantly. For playing a modpack such as Landfall, we generally recommend allocating at least 8GB.

---

## Option 1: Change Allocation Globally (Recommended)

Instead of adjusting RAM for each modpack individually, you can change the default memory allocation globally in the Modrinth App’s main settings.

This means all modpacks—current and future—will inherit this setting automatically, so you don’t need to tweak it every time you install a new pack. It’s a set-and-forget approach that ensures consistent performance across the board. You can always override it for individual instances later if needed.

1. **Navigate to Modrinth Settings**    
- On the left sidebar, click your installed modpack and locate the button with the gear icon.
	![[modrinth-ram-3.png]]
2. **"Default instance options"**
	**a.** Select the "Default instance options" tab
	**b.** Input your desired memory in "Memory allocated". (ex. 8000 MB)
	![[modrinth-ram-4.png]]
3. **Restart Minecraft**
   - You will need to restart Minecraft for the changes to take effect.



## Option 2: Change Allocation Per-Instance

1. **Navigate to the Modpack or Instance Settings**    
- On the left sidebar, click your installed modpack and locate the button with the gear icon.
	![[modrinth-ram-1.png]]
2. **"Java and Memory"**
	**a.** Select the "Java and Memory" tab
	**b.** Check the box labeled "Custom memory allocation"
	**c.** Input your desired memory. (ex. 8000 MB)
	![[modrinth-ram-2.png]]
3. **Restart Minecraft**
   - You will need to restart Minecraft for the changes to take effect.

---

## 📝 Note on Memory Units

For the sake of simplicity in this guide, we will approximate 1 GB of memory as 1000 MB.

Technically, memory (RAM) uses base-2 units, where:
- **1 GB = 1024 MB**,
- **1 MB = 1024 KB**, etc.
However, most modern tools and games often round or mix units when displaying memory sizes, especially when setting RAM limits.

Since the goal here is clarity and easy math, we’ll treat **1 GB ≈ 1000 MB**. If you're doing technical troubleshooting or nearing limits (e.g. maxing out your RAM), it's best to use base-2 values for accuracy.