## Instructions

## Contribute
File a Pull Request with your changes. When your changes are considered good to go, a preview is built on the [wiki](https://github.com/UnofficialCrusaderPatch/UnofficialCrusaderPatch-wiki/wiki) of this repository.

When that also looks good, the changes are published upstream to [the real wiki](https://github.com/UnofficialCrusaderPatch/UnofficialCrusaderPatch/wiki).

### What to contribute
- Game information: size of map, information about AI parameters, which sound file maps to which voice line, etc.
- Articles about UCP3 and the GUI: tutorials, wiki documentation on usage of the software.
- Content contributions: documentation of the currently shipped UCP3 features.

## Developers

### Pushing changes to the actual wiki:
```shell
git clone https://github.com/UnofficialCrusaderPatch/UnofficialCrusaderPatch-wiki
git clone https://github.com/UnofficialCrusaderPatch/UnofficialCrusaderPatch.wiki

cd UnofficialCrusaderPatch.wiki
git pull ../UnofficialCrusaderPatch-wiki
git push
```

### Pulling changes from the actual wiki:
```shell
git clone https://github.com/UnofficialCrusaderPatch/UnofficialCrusaderPatch-wiki
git clone https://github.com/UnofficialCrusaderPatch/UnofficialCrusaderPatch.wiki

cd UnofficialCrusaderPatch-wiki
git pull ../UnofficialCrusaderPatch.wiki
git push
```

## Editing Notes

GitHub's Wiki does not allow sub pages, so we fake this by providing custom sidebars that apply to all files of the same folder and to all files in nested folders, unless another `_Sidebar.md` is defined in them.

To create them, it is important to understand that GitHub also does not support relative paths in page links. However, such folder paths will be used to structure the wiki source. Links to other pages need to refer to the actual file name. **This also means that filenames need to be unique, even if nested, since all are pulled into the same space.** In turn, the links in sidebars will not work in a normal markdown preview. Always validate them in the actual wiki.
