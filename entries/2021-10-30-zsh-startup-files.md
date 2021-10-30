# ZSH Startup Files

There are 5 startup files that ZSH read commands from:

```
$HOME/.zshenv
$HOME/.zprofile
$HOME/.zshrc
$HOME/.zlogin
$HOME/.zlogout
```

And they are executed in the order provided above.

- `.zshenv`;
  - DOs: setup `$PATH`, store important environment variables;
  - DON'Ts: commands that produce output or assume that shell is attached to the TTY;
- `.zshrc` is the place to store all of the information;
  - DOs: aliases, functions, options, key bindings etc;
  - DON'Ts: probably secrets or env (this allows easy `.zshrc` sharing on Github for example);
- `.zlogin`/`.zlogout` executed only in login shells on login and exit `.zprofile` same as `.zlogin`, but executed before `.zshrc`;
  - DOs: commands only for login shells. Do not change the environment at all here;
  - DON'Ts: aliases, options, env;
- 

## Sources

- [Startup Files][startupfiles].

[startupfiles]: https://zsh.sourceforge.io/Intro/intro_3.html
