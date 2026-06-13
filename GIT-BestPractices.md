# GIT: Best Practices

## git-commit

### Uso de la opcion `--amend`

```bash
# modifica la estructura del ultimo commit sobre la rama actual
git commit --amend
```
* Solamente se puede modificar el ultimo commit mediante este método
* Evitar modificar commit's que ya fueron publicados en el repositorio remoto (solamente para uso local)
