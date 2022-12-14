<h1 align="center">Minishell</h1>

---

<p align="center">
	<img src="https://cdn.intra.42.fr/users/ariahi.jpg" height=75>
	<h3 align="center">
	<a href="https://www.linkedin.com">ariahi</a>
</p>
<p align="center">
	<img src="https://cdn.intra.42.fr/users/rel-maza.jpg" height=75>
	<h3 align="center">
	<a href="https://www.linkedin.com/in/rida-el-mazary/">rel-maza</a>
</p>

From your comments, you seem to be confused about exactly what a shell is. The kernel is responsible for managing the system. It's the part that actually loads and runs programs, accesses files, allocates memory, etc. But the kernel has no user interface; you can only communicate with it by using another program as an intermediary.

A shell is a program that prints a prompt, reads a line of input from you, and then interprets it as one or more commands to manipulate files or run other programs. Before the invention of the GUI, the shell was the primary user interface of an OS. On MS-DOS, the shell was called command.com and people wouldn't usually change it. On Unix, however, there have long been multiple shells that users could pick from.

They can be divided into 3 types. The Bourne-compatible shells use the syntax derived from the original Bourne shell. C shells use the syntax from the original C shell. Then there are nontraditional shells that invent their own syntax, or borrow one from some programming language, and are generally much less popular than the first two types.

A built-in command is simply a command that the shell carries out itself, instead of interpreting it as a request to load and run some other program. This has two main effects. First, it's usually faster, because loading and running a program takes time. Of course, the longer the command takes to run, the less significant the load time is compared to the overall run time (because the load time is fairly constant).

Secondly, a built-in command can affect the internal state of the shell. That's why commands like cd must be built-in, because an external program can't change the current directory of the shell. Other commands, like echo, might be built-in for efficiency, but there's no intrinsic reason they can't be external commands.

Which commands are built-in depends on the shell that you're using. You'll have to consult its documentation for a list (e.g., bash's built-in commands are listed in Chapter 4 of its manual). The type command can tell you if a command is built-in (if your shell is POSIX-compatible), because POSIX requires that type be a built-in. If which is not a built-in in your shell, then it probably won't know about your shell's built-ins, but will just look for external programs.
