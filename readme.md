# kava-patches

these are the patches applied to the forks of various dependencies of the [Kava blockchain](https://github.com/Kava-Labs/kava).

they are given as git patches that may be applied to future upstream releases.

to create a patch, use `git format-patch`:
```sh
# patch of just the current head commit:
git format-patch HEAD^

# patch of all commits between two refs:
git format-patch v1.2.x..release/v1.2.x-kava

# patches for n commits before ref:
git format-path -<n> my-git-ref
```

to apply a patch, checkout the desired base branch then:
```sh
git apply <path-to-patch-file>
git commit -a
```

for patches that will result in conflicts:
```sh
git am --3way <path-to-patch-file>
```
