| command                                                 | action                                     |
| :------------------------------------------------------ | :----------------------------------------- |
| `nvm install 'lts/*' --reinstall-packages-from=current` | reinstall all global packages from current |

### Default Global Packages From File While Installing

If you have a list of default packages you want installed every time you install a new version, we support that too -- just add the package names, one per line, to the file `$NVM_DIR/default-packages`. You can add anything npm would accept as a package argument on the command line.

# $NVM_DIR/default-packages

rimraf
object-inspect@1.0.2
stevemao/left-pad
