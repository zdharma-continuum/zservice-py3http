# py3http

This Zsh service-plugin will serve given directory (plugin's directory by default) using Python's 3 HTTP server.

## [Zinit](https://github.com/zdharma-continuum/zinit)

A service-plugin needs a plugin manager that supports loading single plugin instance per all active Zsh sessions, in
background. Zinit supports this, just add:

```
zinit ice service'py3http'
zinit light zdharma-continuum/zservice-py3http
```

to `~/.zshrc`.

## Explanation of Zsh-spawned services

First Zsh instance that will gain a lock will spawn the service. Other Zsh instances will wait. When you close the
initial Zsh session, another Zsh will gain lock and resume the service.
