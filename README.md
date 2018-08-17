# jupyter-notebook-diff

Use nbdime! :raised_hands:

This setup worked for me and I use a separate env to keep my other envs clean.

## First time setup

```
conda env create --file environment-nbdime.yml
```

```
source activate nbdime
nbdime config-git --enable --global
```

edit ~/.gitconfig and change diff to webdiff as follows:
```
[diff "jupyternotebook"]
command = git-nbdiffdriver webdiff 
```

`git diff *.ipynb`

## Usage

```
source activate nbdime; git diff *.ipynb
```

# other ways to use nbdime
- https://nbdime.readthedocs.io/en/stable/vcs.html#git-integration

# nbdime resources
- https://github.com/jupyter/nbdime
- https://test-nbdime.readthedocs.io/en/latest/

# other ideas (not nbdime...)
- http://timstaley.co.uk/posts/making-git-and-jupyter-notebooks-play-nice/
Not fond of these methods, I've tried them and no... 
I often clean all outputs and save a clean notebook. The manual save doesn't kill me, it's the diffs hence nbdime is a win for me

