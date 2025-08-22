# assistant-ia-pipelines

Ce repository contient les pipeline utilisés sur assistant-ia (anciennement albert-conversation).

## Configuration du workspace

Ce projet est compatible sour Linux et MacOS. Je ne l'ai personnellement testé uniquement sous Linux [Fedora](https://notes.sklein.xyz/Fedora/).

Prérequis:

- Installer Mise: https://mise.jdx.dev/installing-mise.html

```sh
$ mise install
$ git config core.hooksPath git-hooks
$ gitleaks --version
gitleaks version 8.25.1
```

## Instances de prod et dev

Pour le moment il existe deux instances de *Assistant IA* :

- https://albert.numerique.gouv.fr/ géré dans le dossier [`./prod/`](./prod/)
- https://albert-dev.beta.numerique.gouv.fr/ géré dans le dossier [`./dev/`](./dev/)

Je vous invite à explorer le dossier de l'instance de votre choix.


## Contributions

Ce projet utilise [Gitleaks](https://notes.sklein.xyz/Gitleaks/) pour éviter de publier par erreur des secrets.

Pour plus d'informations, je vous invite à consulter cette note : https://notes.sklein.xyz/2025-05-07_2353/

Voici quelques commandes utiles.

Tester si votre dossier contient des secrets en dehors du fichiers `.secret` :

```
$ gitleaks dir -v

    ○
    │╲
    │ ○
    ○ ░
    ░    gitleaks

4:37PM INF scanned ~101712 bytes (101.71 KB) in 18.3ms
4:37PM INF no leaks found
```
