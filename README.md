```markdown
# 🚀 Contained: A Lightweight Container Runner

Welcome to **Contained**, a minimalist container runtime designed for running isolated processes with ease.

## 🌟 Features

- **Namespace Isolation**: Runs processes in a separate user and PID namespace.
- **Resource Limiting**: Configurable memory, CPU, and I/O limits.
- **Capability Dropping**: Reduces process capabilities to enhance security.
- **Syscall Filtering**: Restricts the syscalls available to the containerized process.

## 🛠 Usage

You can use **Contained** to run `/bin/sh` in the `/misc/img` directory as root with the following command:

```bash
sudo ./contained -m ~/misc/busybox-img/ -u 0 -c /bin/sh
```

### Example Session

```bash
$ sudo ./contained -m ~/misc/busybox-img/ -u 0 -c /bin/sh
=> validating Linux version...4.7.10.201610222037-1-grsec on x86_64.
=> setting cgroups...memory...cpu...pids...blkio...done.
=> setting rlimit...done.
=> remounting everything with MS_PRIVATE...remounted.
=> making a temp directory and a bind mount there...done.
=> pivoting root...done.
=> unmounting /oldroot.oQ5jOY...done.
=> trying a user namespace...writing /proc/32627/uid_map...writing /proc/32627/gid_map...done.
=> switching to uid 0 / gid 0...done.
=> dropping capabilities...bounding...inheritable...done.
=> filtering syscalls...done.
/ # whoami
root
/ # hostname
05fe5c-three-of-pentacles
/ # exit
=> cleaning cgroups...done.
```

## 🐳 Requirements

- **Linux Kernel**: Version 4.7 or later.
- **Cgroups**: Enabled and configured.
- **Root Privileges**: Required for setting namespaces and resource limits.

## 📜 License

This project is licensed under the MIT License.

---

Made with ❤️ by [Your Name]
```

## 🔗 Resources

- [Linux Namespaces](https://man7.org/linux/man-pages/man7/namespaces.7.html)
- [Control Groups (cgroups)](https://man7.org/linux/man-pages/man7/cgroups.7.html)

## 🤝 Contributing

Contributions are welcome! Please open an issue or submit a pull request on GitHub.

---

Feel free to customize further as per your needs! 🚀
