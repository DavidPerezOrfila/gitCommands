# Comandos más comunes de GIT

> ### - Reconstruye el proyecto al estado anterior del repositorio en el último commit

>```
> git checkout --.
>```

> ### - Modificar el nombre de una **rama**

>```
> git branch -m master nombreDeLaRama
>```

> ### - Modificar globalmente la configuración de git para cambiar el nombre a la **rama** principal por defecto

>```
> git config --global init.defaultBrach nombreDeLaRama
>```

> ### - Listar las configuraciones globales

>```
> git config --global --list
>```

> ### - Listar las configuraciones globales (_modo edición_)

>```
> git config --global -e
>```

> ### - Quitar un fichero del stage después de añadirlo

>```
> git reset nombreDelFichero
>```

> ### - Añadir modificaciones al stage y realizar commit en un mismo comando

>```
> git commit -am "mensaje"
>```

> ### - Listar el log con los commits realizados

>```
> git log
>```

> ### - Crear un fichero **_.gitkeep_** dentro de una carpeta vacía para forzar a GIT a añadirla al stage

![gitkeep](https://github.com/DavidPerezOrfila/gitCommands/blob/master/img/gitkeep.png)

> ### - Crear un **alias** global "**_s_**" para realizar un `git status` en su forma corta

>```
> git config --global alias.s "status --short"
>```

> ### - Crear un **alias** global "**_lg_**" para visualizar un log personalizado

>```
> git config --global alias.lg "log --graph --abbrev-commit --decorate --format=format:'%C(bold blue)%h%C(reset) - %C(bold green)(%ar)%C(reset) %C(white)%s%C(reset) %C(dim white)- %an%C(reset)%C(bold yellow)%d%C(reset)' --all"
>```

> ### - Ver diferencias de código en ficheros modificados

>```
> git diff
>```

> ### - Ver diferencias de código en ficheros modificados ya añadidos al **stage**

>```
> git diff --staged
>```

> ### - Modificar mensaje de un commit
>```
> git commit --amend -m "mensaje a modificar"
>```

> ### - Restaura el stage al estado anterior del último commit
> ```
> git reset --soft 49f2315
> o
> git reset --soft HEAD^
> ```

> ### - Restaurar git a un punto anterior sin modificar los nuevos datos añadidos con posterioridad
> ```
> git reset --mix 49f2315
> o
> git reset --mix HEAD^3
> ```

> ### - Restaurar git a un punto anterior quitando los nuevos datos añadidos con posterioridad
> ```
> git reset --hard 49f2315
> o
> git reset --hard HEAD^3
> ```

> ### - Restaurar git a un punto anterior histórico con **_reflog_**
> ```
> git reflog
> ```
> ### - Renombrar nombre fichero con **GIT**
> ```
> git mv destruir-mundo.md salvar-mundo.md
> ```
![salvar-mundo](https://github.com/DavidPerezOrfila/gitCommands/blob/master/img/salvar-mundo.png)

> ### - Eliminar un fichero con **GIT**
> #### (no lo elimina del stage)
> ```
> git rm salvar-mundo.md
> ```
![salvar-mundoGITrm](https://github.com/DavidPerezOrfila/gitCommands/blob/master/img/salvar-mundoGITrm.png?)