These snippets are based of the ones of Gilles Castel *[blogpost in which he described it](https://castel.dev/post/lecture-notes-1/)*.

## Vim configuration

This config will work for a lazy neovim.
```lua
return {
        "SirVer/ultisnips",
        keys = {
            {"<tab>", vim.cmd.UltiSnipsExpandTrigger},
            {"<C-u>", vim.cmd.UltiSnipsEdit},
            {"<C-n>", vim.cmd.UltiSnipsJumpForwardTrigger,
            {"<C-b>", vim.cmd.UltiSnipsJumpBackwardTrigger},
        }
    }
}
```

