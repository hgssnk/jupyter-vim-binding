# jupyter-vim-binding

## jupytertheme installation

``` bash
# install themes
pip install jupyterthemes
# setting theme
jt -t gruvboxd
```

add to css

```css:~/.jupyter/custom/custom.css
/* Jupyter cell is in normal mode when code mirror */
.edit_mode .cell.selected .CodeMirror-focused.cm-fat-cursor {
background-color: #000000 !important;
}
/* Jupyter cell is in insert mode when code mirror */
.edit_mode .cell.selected .CodeMirror-focused:not(.cm-fat-cursor) {
background-color: #000000 !important;
}
/* images background-color */
div.output_subarea {
  background-color: #DACCA7;
}
```

## vim installation

```bash
# Create required directory in case (optional)
mkdir -p $(jupyter --data-dir)/nbextensions
# Clone the repository
cd $(jupyter --data-dir)/nbextensions
git clone https://github.com/lambdalisue/jupyter-vim-binding vim_binding
# Activate the extension
jupyter nbextension enable vim_binding/vim_binding
```
