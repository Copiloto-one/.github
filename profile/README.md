Copiloto
========

Carga de trabajo:
-----------------
Kanban: https://github.com/orgs/Copiloto-one/projects/1/views/1


#Desarrollo

El modelo propuesto para realizar cambios en el codigo esta basado en el flujo `feature-branching`. En este flujo cada ticket en la tabla o `issue` tiene por lo menos un pull-request vinculado para poder considerar el ticket como trabajado. El flujo funciona de la siguiente manera:

Para dar un ejemplo, tomemos el siguiente ticket: https://github.com/Copiloto-one/DBO/issues/3. El flujo `git` para empezar a trabajar en el ticket implica lo siguiente:

1) Actualizo el `branch` `main` y creo un nuevo `branch` que linkea al ticket en el nombre.
```
  git checkout main
  git pull origin main
  git branch -b issue-#3
```

Ahora el `HEAD` del repositorio `.git` local apunta a la nueva rama `issue-#3` y es aqui donde vamos a realizar los cambios que se necesitan para el completar el ticket, o parte de el. Una vez tengamos los cambios necesarios pasamos a consolidar los cambios con un `commit`:

2) Agrego los cambios al `branch` y hago `commit` en la rama
```
  git add -A
  git commit -m '#3 Agregando documentacion sobre feature-branching'
```

La rama puede incluir la cantidad de `commits` que sea necesario. El destino final de la nueva rama `issue-#3` es generar un `pull-request`, el cual una vez aprobado y `merged` con la rama `main` da el ticket como finalizado. Para crear un `pull-request` a partir de la nueva rama solo necesitamos empujar la nueva rama al repositorio remoto:

```
  git push origin issue-#3
```

La nueva rama ya esta en github y podemos crear un nuevo `pull-request` a traves del link que github comparte en la respuesta al `push` o podemos hacerlo en la interfaz web haciendo click en `pull-requests` y creando un nuevo pull-request a partir de la nueva rama que acabamos de empujar a github. Mas detalle en: https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request

Guias Github:
------------
Para mas detalles sobre como interactuar con github a traves de `commits` y `pull-requests` referirse a:
https://docs.github.com/en/issues/tracking-your-work-with-issues/linking-a-pull-request-to-an-issue

Guia de Github generales: https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-branches

