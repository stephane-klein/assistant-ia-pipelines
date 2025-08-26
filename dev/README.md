# Workspace de l'environnement de développement

Le dossier [`./pipelines/`](./pipelines/) contient les [Open WebUI Pipelines functions](https://docs.openwebui.com/pipelines/) qui sont déployés sur l'instance <https://albert-dev.beta.numerique.gouv.fr/>.

## Upload de Pipelines

Vous pouvez utiliser le scripts suivant pour uploader une pipeline function, par exemple [`./pipelines/hello_world.py`](./pipelines/hello_world.py) vers l'instance de <https://albert-dev.beta.numerique.gouv.fr/> :

```sh
$ ./scripts/upload-pipelines-function.py pipelines/hello_world.py
{"status":true,"detail":"Pipeline uploaded successfully to ./pipelines/hello_world.py"}
```

Il est aussi possible d'uploader la configuration des variables Valves :

```
$ ./scripts/upload-pipelines-function-valves.py pipelines/hello_world_valves.json
```

Attention, les fichiers *valves.json peuvent contenir des informations sensibles et ne doivent pas être committés en clair dans le repository.
Pour cela, des fichiers `*_valves.json.skel`, sans secret, sont intégrés au repository.  
Pour les utiliser, vous pouvez copier leur contenu, exemple :

```sh
$ cp pipelines/pipeline_service_public_valves.json.skel pipelines/pipeline_service_public_valves.json
```

et ensuite set le ou les secrets dans `pipelines/pipeline_service_public_valves.json` et pour finir, exécuter :

```sh
$ ./scripts/upload-pipelines-function-valves.py pipelines/pipeline_service_public_valves.json
```
