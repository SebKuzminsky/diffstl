This is a tool to visually diff STL files.  It integrates with git,
and is easy to run on the command line.

It uses stl_cmd to compute the diffs and fstl to view them.

stl_cmd is available in Debian, and here: <https://github.com/AllwineDesigns/stl_cmd.git>

fstl is available in Debian, and here: <https://www.mattkeeter.com/projects/fstl/>, <https://github.com/fstl-app/fstl>


# Running by hand

`diffstl a.stl b.stl`


# Integrating with git

1.  In `~/.gitconfig` (global) or `.git/config` (per repo), add these lines:
```
    [diff "diffstl"]
        command=diffstl
```

2.  In `.gitattributes` in your repo, add this line:
```
    *.stl diff=diffstl
```

3. Run `git diff` like normal, e.g. `git diff a.stl` or `git diff v1.0..v1.1 -- a.stl`.
