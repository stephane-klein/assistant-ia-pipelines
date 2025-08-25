# Workspace de l'environnement de développement

Le dossier [`./pipelines/`](./pipelines/) contient les [Open WebUI Pipelines functions](https://docs.openwebui.com/pipelines/) qui sont déployés sur l'instance <https://albert-dev.beta.numerique.gouv.fr/>.

## Upload de Pipelines

Vous pouvez utiliser le scripts suivant pour uploader une pipeline function, par exemple [`./pipelines/hello_world.py`](./pipelines/hello_world.py) vers l'instance de <https://albert-dev.beta.numerique.gouv.fr/> :

```sh
$ ./scripts/upload-pipelines-function.py pipelines/hello_world.py
{"status":true,"detail":"Pipeline uploaded successfully to ./pipelines/hello_world.py"}
```
