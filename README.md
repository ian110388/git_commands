# git_commands

> Editar la configuración global con editor de texto.

```
git config --global -e
a: Para editar archivo
esc: para dejar de editar
:wq: Guardar cambios y salir
```

> Configuración global: Permite configurar git para que siempre inicie un repositorio con la rama main.

```
git config --global init.defaultbranch main
```

> Quita archivos del stage.

```
git reset file
```

> Recontruye el proyecto a como estaba antes

```
git checkout --.
```

> Renombrar branch.

```
git branch -m master main
```

> Muestra archivos modificados con un icono o simbolo.

```
git status --short
```

---

# Alias

> Status.

```
git config --global alias.s "status --short"
```

> Log.

```
git config --global alias.lg "log --graph --abbrev-commit --decorate 
--format=format:'%C(bold blue)%h%C(reset) - %C(bold green)(%ar)%C(reset) 
%C(white)%s%C(reset) %C(dim white)- %an%C(reset)%C(bold yellow)%d%C(reset)' --all"
```

---

> Muestra las diferencias del código anterior y el actual: Working Directory

```
git diff
```

> Muestra las diferencias del código anterior y el actual: Stage

```
git diff --staged
```

> Permite corregir el mensaje del último commit

```
git commit --amend -m "nuevo mensaje"
```

> Permite combinar los cambios nuevos con un commit anterior

```
git reset --soft HEAD^ 
```

> Regresar a un punto del códdigo anterior manteniendo cambios , pero saca del stage los cambios realizados

```
git reset --mixed hash del commit
```

> Regresa o resetea el código a un punto anterior pero a diferencia del --mixed este comando si destruye los cambios posteriores al reset

```
git reset --hard hash del commit
```

> Nos muestra un historial de todos los movimientos de nuestro repositorio en orden cronológico.

```
git reflog
```

> Unir dos ramas. Para realizar un merge se debe de estar posicionado en la rama en la cuál se quire integrar los cambios realizados en la rama secundaria.

```
git merge rama-villanos
```

> Elimina la (rama secundaria) que ya fué incluida en la rama main

```
git branch -d rama-villanos -> NORMAL
git branch -d rama-villanos -F -> FORZADO
```

> Comando para crear una nueva rama y al mismo tiempo cambiarme a ella

```
git checkout -b rama-villanos
```

> Crear Tags

```
git tag super-release
```

> Eliminar Tags

```
git tag -d super-release
```

> Crear un tag con versionamiento y comentarios

```
git tag -a v0.1.0 hash -m "versión alpha de la app"
```

> Mostrar información del tag creado

```
git show v0.1.0
```

> Agregar elementos al stash con un comentario para poderlo identificar

```
git stash save "nombre para identificar"
```

> Otros comandos del stash

```
git stash
git stash list
git stash pop
git stash apply stash{0}
git stash drop stash{0}
git stash show stash{0}
git stash list --stat
```

> Configuración global para realizar el pull con Fast Forward

```
git config --global pull.ff only
```
