![](gdb.png)
^ (default GDB – no extra tools, no context window, very basic)

# 🛠️ What is GDB?

GDB is the standard GNU debugger used by Linux developers to debug compiled applications — but for exploit developers, it’s an essential tool to reverse and break things!

---

## 🧪 Try It Yourself

```bash
$ gdb -q /bin/ls
(gdb) start
```

This opens `/bin/ls` in GDB and begins execution right before `main()`.

---

## 🕹️ What’s a Debugger, Really?

A **debugger** is like a **time machine** for programs:
You can pause, inspect, step through, or even change execution on the fly.

For exploit developers, it’s invaluable for:

- Analyzing control flow  
- Watching memory in real time  
- Testing and refining payloads  

---

## 💣 Why GDB Matters for Exploit Devs

While developers use GDB to fix bugs, **exploit devs use it to *find* them.**

You’ll:

- Inspect registers and stack at crash points
- Set breakpoints to trap execution at the right time
- Craft and debug shellcode or ROP chains step by step

---

# 💉 GEF – GDB Enhanced Features

![](gef.png)
^ (GEF loaded – colorful, structured UI, context-aware)

While vanilla GDB works, it’s… minimal.

That’s where **[GEF (GDB Enhanced Features)](https://github.com/hugsy/gef)** comes in. It provides:
- A better UI with a clear context window
- Syntax highlighting and register coloring
- Built-in commands for heap analysis, format string exploits, syscall tracing, and more

---

## 🚀 Installing GEF

Installation is super simple:

```bash
bash -c "$(curl -fsSL https://gef.blah.cat/sh)"
```

This script safely adds the plugin to your `~/.gdbinit` so GEF loads automatically whenever you start GDB.

---

## 🧭 Final Tip

💡 **Always use GDB with GEF for binary exploitation**. It speeds up learning and makes debugging binaries 10x more intuitive.

If you're feeling fancy later, you can also explore:
- [Pwndbg](https://github.com/pwndbg/pwndbg) – another GDB plugin with exploit dev features

---

!!! tip
	🧠 Mastering GDB is one of the best investments you can make as an exploit developer.