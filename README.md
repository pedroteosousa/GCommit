![GCommit](GCommitLogo.png)


# GCommit - Group Commit

GCommit is a git-plugin that eases how to commit when you need to sign for
more than one person -- pair and mob programming reality.

Instead of having to set manually the other developers names, you can define
once and reference at any commit-time.

## Installation
For installation you have to run the next command:

```
$ sudo make install

GCommit has been installed successfully
```

## Uninstall
For Uninstallation you have to run the next command:

```
$ sudo make uninstall
```


## How to use

GCommit reads a file that defines your teammates signatures, so first create
a `.gitteam` file in your project's root directory, that follows the following
structure:

```plain
JD="João Daniel <jotaf.daniel@gmail.com>"
JOD="John Doe <jon.doe@example.com>"
JAD="Jane Doe <jane.doe@example.com>"
```

> note: there's no empty line at the end

Once you have `.gitteam` in your repository, you can commit something using:

```bash
git gcommit JAD JD
```

This will generate a initial commit message like this:

```plain


Signed-off-by: Jane Doe <jane.doe@example.com>
Signed-off-by: João Daniel <jotaf.daniel@gmail.com>
```

To pass other ```git commit``` command line arguments to GCommit we would have to do the following :

```bash
git gcommit JAD JD --amend
```
where ```--ammend``` is an argument for ```git commit``` 

To add all the members of your team to the commit, you can use the following command

```bash
git gcommit --all
```

To remove particular members from a commit 

```bash
git gcommit --except JAD
```

This command would remove ```JAD``` and adds all others to the commit list.


## Contributing

Please refer to [CONTRIBUTING.md][1]


## Contributors

Many thanks to all contributors!

| | | | | |
|-|-|-|-|-|
|<p align="center"><img style="border-radius: 100px" width="100px" src="https://avatars3.githubusercontent.com/u/5549736?s=200&v=4"  alt="Mairielli" /><br />[Mairieli][mairieli] Wessel</p>|<p align="center"><img style="border-radius: 100px" width="100px" src="https://avatars2.githubusercontent.com/u/7605307?s=200&v=4"  alt="Emmanuel Arias"/><br />[Emmanuel][eamanu] Arias</p>|<p align="center"><img style="border-radius: 100px" width="100px" src="https://avatars2.githubusercontent.com/u/12171804?s=100&v=4" alt="Gurkirpal Singh" width="100px"/><br />[Gurkirpal][gpalsingh] Singh </p>|<p align="center"><img style="border-radius: 100px" width="100px" src="https://avatars2.githubusercontent.com/u/3865119?s=200&v=4"  alt="Eloy"/><br />[Eloy][ehx]</p>|<p align="center"><img style="border-radius: 100px" width="100px" src="https://avatars0.githubusercontent.com/u/3801092?s=200&v=4"  alt="Thathiane"/><br />[Thathiane][thatiane] Rosa</p>|
|<p align="center"><img style="border-radius: 100px" width="100px" src="https://avatars3.githubusercontent.com/u/8609211?s=200&v=4"  alt="Vinay Hedge"/><br />[Vinay][hegde5] Hegde</p>|<p align="center"><img style="border-radius: 100px" width="100px" src="https://avatars3.githubusercontent.com/u/17693231?s=200&v=4" alt="Andre Moukarzel"/><br />[Andre][Detril] Moukarzel</p>|<p align="center"><img style="border-radius: 100px" width="100px" src="https://avatars3.githubusercontent.com/u/27254325?s=200&v=4" alt="Caio Andrade"/><br />[Caio][CaioA] Andrade</p>|<p align="center"><img style="border-radius: 100px" width="100px" src="https://avatars2.githubusercontent.com/u/7110169?s=200&v=4"  alt="Pedro Pereira"/><br />[Pedro][pedro823] Pereira </p>|<p align="center"><img style="border-radius: 100px" width="100px" src="https://avatars1.githubusercontent.com/u/20888363?s=200&v=4" alt="Jay Welborn"/><br />[Jay][JayWelborn] Welborn </p>|
|<p align="center"><img style="border-radius: 100px" width="100px" src="https://avatars1.githubusercontent.com/u/39068024?s=460&v=4" alt="Leandro Rodrigues" width="100px"/><br />[Leandro][Leandrigues] Rodrigues</p>|<p align="center"><img style="border-radius: 100px" width="100px" src="https://avatars1.githubusercontent.com/u/30770796?s=460&v=4"  alt="ParthPratim" width="100px"/><br />[Parth][ParthPratim] Pratim </p>|<p align="center"><img style="border-radius: 100px" width="100px" src="https://avatars1.githubusercontent.com/u/5351077?s=460&v=4"  alt="JorossBarredo" width="100px"/><br />[Joross][iamjoross] Joross </p>| |



## License



This project is licensed under the [MIT License][2]



[1]: https://github.com/jooaodanieel/GCommit/blob/master/CONTRIBUTING.md
[2]: https://opensource.org/licenses/MIT


[mairieli]: https://github.com/mairieli
[eamanu]: https://github.com/eamanu
[gpalsingh]: https://github.com/gpalsingh
[ehx]: https://github.com/ehx
[thatiane]: https://github.com/thatiane
[hegde5]: https://github.com/hegde5
[Detril]: https://github.com/Detril
[CaioA]: https://github.com/CanTulio
[pedro823]: https://github.com/pedro823
[JayWelborn]:https://github.com/JayWelborn
[Leandrigues]:https://github.com/Leandrigues
[ParthPratim]:https://github.com/ParthPratim
[iamjoross]:https://github.com/iamjoross

