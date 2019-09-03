There is a writeup for this vulnerability at https://www.anquanke.com/post/id/166819 (in Chinese).
This is a local priviledge escalation exploit for a kernel bpf bug.
affected version: 4.20-rc1, 4.20-rc2, 4.20-rc3, 4.20-rc4

```bash
user@syzkaller:~$ ./exp
rop_payload_initialized
uid=0(root) gid=0(root) groups=0(root) context=system_u:system_r:kernel_t:s0
# uname -a
Linux syzkaller 4.20.0-rc3 #1 SMP Thu Nov 22 15:12:38 CST 2018 x86_64 GNU/Linux
#
```

references:
https://www.mail-archive.com/netdev@vger.kernel.org/msg256073.html
https://www.mail-archive.com/netdev@vger.kernel.org/msg256054.html
