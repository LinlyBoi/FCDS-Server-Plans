# MEMORY MANAGEMENT 
## IN LINUX
---
## Idle Page Tracking
Ensuring are that no resources are wasted

---
## How are pages represented?
The pages are represented as a bitmap
- Array of 8 byte integers 
- Each bit $\rightarrow$ Page

---
## How are pages marked IDLE?
- Set bit correspondent to page on bitmap
- Only for user memory pages
- Kernel level pages are never marked IDLE
---
## Implementation Details
1. Kernel internally keeps track of accesses to memory pages
2. Unreferenced pages are reclaimed
Sometimes Kernel explicitly marks pages as accessed
---
## Explicit Mark
1. User space process executing a system call
2. Page used for storing file system buffers is read or written
3. Page accessed by a device driver using `get_user_pages()`
---
## Dirty Pages
- Old pages that haven't been written to
- Cleared out when virtual memory is full
- Written to disk/swap
---
# Memory Hot (Un) Plugging
Adjusting memory at runtime

---
## Plugging In
1. Add memory to Linux
2. Onlining Memory Blocks %%unHide memory from pager%%
---
## UnPlugging Memory
1. Offlining Memory Blocks %%Hide memory from pager%%
2. Remove ALL free pages
---
## Monitoring System Memory
![[Pasted image 20230403210727.png]]
#### Observing Memory Blocks
```shell
cat /sys/device/system/memory/memoryXXX/state
```
Where `XXX` is the number of the memory block
---
# NUMA
#### Non Uniform Memory Access
---
### Memory Policies
Determine which node the kernel chooses to allocate memory to in a system

---
## Policy Scopes
1. System Default
2. Task/Process
3. VMA %%(Virtual Memory Area)%%
%%ggeg git gud%%
---
# Virtual Memory
When RAM just isn't enough
---
#### Linux uses a 64-bit virtual memory scheme
- Basically infinite address space
- Each process gets their own address space
---
### Address Spaces Segments
- Stack
- Code
- Data
- Heap
---
### Stack and Heap
- Storing variables
- Dynamically allocated memory
---

### Code and Data
- Instructions and data of program
---
## Memory Allocation
 1. Buddy System
 2. Slab System
---
## Buddy System
- Fixed Size blocks of power 2
- Allocated/Free (V/I)
- Adjacent Free blocks combined
---
## Slab System
- Used for Kernel Objects
- Each Cache has its "free list"
%%- Network Buffers, File system caches%%
---
