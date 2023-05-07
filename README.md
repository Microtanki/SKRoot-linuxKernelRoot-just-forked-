# SKRoot - SuperKernelRoot - Linux Kernel Level Perfectly Hidden ROOT Demo
New generation SKRoot, challenge the whole network root detection means, with the mask completely different ideas, get rid of the weakness of the mask is detected, the perfect hidden root function, the whole process does not need to pause SELinux, to achieve the real SELinux 0% touch, universal, pass all the kernel, no kernel source code, direct patch kernel, compatible with Android APP direct JNI call, stable, smooth, no flashback.
## Function List：
#### 1. Displays its own permission information
#### 2. Get ROOT access
#### 3. Execute the ROOT command
#### 4. Execute native kernel commands
#### 5. Install and deploy su
#### 6. inject su into the specified process
#### 7. Uninstall and clean su completely

## Function Remarks:
The only way for APP application to get ROOT permission is to get ROOT secret key, this key is a 48-bit random string, safe and reliable, if you feel the length is not enough, you can modify the source code to expand the length.

Among them, [inject su to the specified process] only supports to authorize su to the 64-bit APP, the old 32-bit APP is no longer supported, because almost all APPs on the market are 64-bit, such as MT File Manager, Root Explorer File Manager, etc.

## Use process:
#### 1. By dragging and dropping the kernel file set find_proc_pid_status can directly get the entry address of the function proc_pid_status, IDA jump to the address and press F5, the naked eye can get the offset value of cred or seccomp in the task_struct structure (seccomp is a non-essential item).
#### 2. By dragging and dropping the kernel file set find_avc_denied can get the entrance address of the relevant function, IDA jump to the address and press F5, the naked eye jump can get avc_denied entrance location.
#### 3. By dragging and dropping the kernel file set find_do_execve can directly get the entry location of the function do_execve.
#### 4. Start patching the kernel by dragging and dropping the kernel file to patch_kernel_root and entering the above information value, and the ROOT key will be automatically generated until the patch is completed.
#### 5. Start PermissionManager, enter the ROOT key value, and start enjoying the comfortable ROOT environment.

There are many ways to get these 4 values from the kernel file without source code, there are at least 4 of them, in fact, you can search them directly with IDA~, here for your convenience, we made three "script tools" with their source code.

 
## Effect:
#### experiment hundreds of machines, all stable operation (such as Redmi K20\K30\K40\K50\K60, Xiaomi 8\9\10\11\12\13, Xiaomi Tablet 5, Red Devil 5\6\7, Lenovo, Samsung, One Plus, ROG2\3, etc.)
#### over all mainstream APP ROOT detection on the market, such as agriculture XX, delivery X12XX3, etc...
#### No need to pay attention to Google GKI
#### Let all the ROOT detection means return to dust, may the world usher in a better ROOT era!

![image](https://github.com/abcz316/linuxKernelRoot/blob/master/ScreenCap/1.png)
![image](https://github.com/abcz316/linuxKernelRoot/blob/master/ScreenCap/2.png)
![image](https://github.com/abcz316/linuxKernelRoot/blob/master/ScreenCap/3.png)
![image](https://github.com/abcz316/linuxKernelRoot/blob/master/ScreenCap/4.png)
