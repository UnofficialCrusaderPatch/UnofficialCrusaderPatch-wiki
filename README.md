## Instructions

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