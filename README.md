# Memory-management-interfaces-C
My own implementation of malloc() and free().

##### This was a university assignment I had to complete with a team member.

## Usage and Setup for the program:
  1. Clone this repository on your `Ubuntu ` running device
  2. Open your teminal.
  3. Navigate to the root directory where all the files are downloaded
  4. Execute the command `make all`
  5. It might show you a bunch of warnings, etc. As long as there is no error run the command `./myalloc`
  
## Algorithms Used:
  - Initially a contigious chunk of dynamic memory is assigned to demonstrate the working of the various methods and interfaces.
  - Memory (free and occupied) is managed by maintaining two separate linked lists with the address of the memory available/used.
  - Splitting/Coalescing is used to make sure fragmentation is avoided.
  - Any request for memory less than `8 bytes` is allocated all 8 bytes - Only one source of internal fragmentation
  - size of free/used memory is stored in the 8 bytes above each memory pointer in the corresponding linked lists.
  - ### Allocation Algorithms supported:
      - `FIRST_FIT` : finds the first address in memory chunk which can fit the requested allocation size.
      - `BEST_FIT ` : finds the smallest possible memory hole that can accomadate the requested size (traverses whole list of Free memory).
      - `WORST_FIT` : finds the largest possible memory hole that can accomodate the requested size (again, traverses through the whole Free memory list).
  - Also supports the compaction function to make sure free memory is optimized.
  
## Other supported functionalities:
  - Can print the layout of memory chunk being managed.
  - Can print memory statistics to console if needed.
  


