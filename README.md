# ev_01
Este repositorio demuestra el uso de control de versiones con Git, trabajo colaborativo y automatización básica siguiendo el modelo GitFlow.
- feat: agrega fecha al README
- fix: corrige formato de fecha
  
Se utiliza el siguiente esquema:
- feature/fecha-1
- feature/fecha-2
- hotfix/fix-fecha

Se sigue el modelo GitFlow:
- Las ramas feature se crean desde develop
- Las feature se integran a develop mediante Pull Request
- Las ramas hotfix se crean desde main
- Los hotfix se integran a main mediante Pull Request

Se utiliza Pull Request para integrar cambios:
- Cada feature requiere un PR hacia develop
- Cada hotfix requiere un PR hacia main
- Antes del merge se revisan los cambios
- Se valida que el código funcione correctamente
