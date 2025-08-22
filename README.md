# assistant-ia-pipelines

Ce repertoire contient les pipeline utilisés sur assistant-ia (anciennement albert-conversation).

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
