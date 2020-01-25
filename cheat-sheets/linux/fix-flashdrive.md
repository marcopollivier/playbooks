# USB devices showing a read only

## When you attach your USB key to your laptop:

**1) So that you won't type your password all the time**
```sh
$ run sudo su
```
**2) To see where your USB stick is mounted**
```sh
$ run df -Th
```
**3) Unmount your USB stick
Run dosfsck on the device you saw from your previous command**
```sh
dosfsck /dev/sdc1
```
**4) Remove and attach again your USB stick**

Problem should be solved now.
Now, for your HDD, please follow the answer to this question. It is about an external HDD but it is the same thing for your case.

