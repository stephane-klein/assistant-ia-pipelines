## Workspace de l'environnement de production

Le dossier [`./pipelines/`](./pipelines/) contient les [Open WebUI Pipelines functions](https://docs.openwebui.com/pipelines/) qui sont déployés sur l'instance <https://albert.numerique.gouv.fr>.

## Upload de Pipelines

Vous pouvez utiliser le scripts suivant pour uploader une pipeline function, par exemple [`./pipeline_nos_administrations.py`](./pipelines/pipeline_nos_administrations.py) vers l'instance de <https://albert.numerique.gouv.fr/> :

```sh
$ ./scripts/upload-pipelines-function.py pipelines/pipeline_nos_administrations.py
{"status":true,"detail":"Pipeline uploaded successfully to ./pipelines/pipeline_nos_administrations.py"}
```
