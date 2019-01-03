![](https://user-images.githubusercontent.com/43666255/50647950-37e9b280-0f7a-11e9-90b6-f1baa3b0128e.png)

ALE is a modern asynchronous linter for Vim/Neovim (Neovim). ale-sensible provides a works-out-of-the-box experience:

![ALE vs ALE SENSIBLE](https://user-images.githubusercontent.com/43666255/50647394-bba29f80-0f78-11e9-83be-1cd33c75ca32.png)

- **No stuttery gutter taking space and shaking up your code**
- **No nervous linting in the current line while editing**
- **No delayed linting; linting happens right after 0ms in Normal mode or 0ms after you left Insert mode** 
- **No more broken colortheme, ale-sensible matches every colortheme**
- **Does not bloat your config, it's just one line and makes ALE turn-key-ready, you can still adjust ALE further**

With ALE's default config the gutter jumps in and out when switching buffers between linted and non-linted files. If you prefer a toned-down, minimalistic Neovim this gutter feels out of place. It's jumpy and stuttery, pushing all your code in and out, especially if you are coding on a remote server and worse: There aren't any colorthemes which theme the gutter. So it's always grey and doesn't match your chosen colorscheme. To fix all these issues just place...

```
Plug 'desmap/ale-sensible'
```
in your Neovim config before the ALE plugin. So you should end up with...
```
Plug 'desmap/ale-sensible'
Plug 'w0rp/ale'
...
```
Install all linters you want to use locally or globally (don't mix) and ALE will find them. To set fixers, e.g. first Prettier, then Standard, add `let g:ale_fixers = ['prettier', 'standard']` to your config. To execute all fixers, run `:ALEFix` in Neovim.

Find further config options for ALE in Neovim with `:help ale`
