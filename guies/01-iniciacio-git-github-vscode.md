# Guia 1. Iniciació a Git, GitHub i Visual Studio Code

## Conceptes essencials

- **Git:** sistema que registra versions dels fitxers en local.
- **GitHub:** servei remot on podem allotjar i compartir repositoris Git.
- **Repositori local:** còpia de treball que hi ha al nostre ordinador.
- **Repositori remot:** còpia allotjada a GitHub.
- **Commit:** punt de l'historial que descriu un conjunt de canvis.
- **Push:** envia commits locals al repositori remot.
- **Pull:** descarrega canvis del repositori remot.

## Instal·lació

1. Instal·la Git des de [git-scm.com](https://git-scm.com/downloads).
2. Instal·la Visual Studio Code des de [code.visualstudio.com](https://code.visualstudio.com/).
3. Reinicia Visual Studio Code si ja estava obert.
4. Obre **Terminal > New Terminal**.
5. Comprova les instal·lacions:

```bash
git --version
code --version
```

## Configuració inicial

Executa una sola vegada:

```bash
git config --global user.name "Nom Cognom"
git config --global user.email "correu@exemple.cat"
```

Consulta la configuració:

```bash
git config --global --list
git config user.name
git config user.email
```

El correu de Git hauria de coincidir amb un correu verificat a GitHub si vols que GitHub associï els commits al teu compte.

## Crear i clonar un repositori

Per crear un repositori remot, entra a GitHub, prem **New repository**, escriu el nom i confirma. Per descarregar-lo a l'ordinador:

```bash
git clone https://github.com/USUARI/REPOSITORI.git
cd REPOSITORI
code .
```

També es pot fer amb **Git: Clone** des de la paleta d'ordres de Visual Studio Code.

## Autenticació

Quan GitHub demani identificació per HTTPS, segueix el flux del navegador o utilitza el mètode que indiqui el centre. Una contrasenya normal pot no funcionar com a contrasenya de Git. No copiïs tokens en fitxers ni els comparteixis.

## Flux de treball recomanat

```text
Editar -> git status -> git diff -> git add -> git commit -> git push
```

Des de Visual Studio Code, l'apartat **Control de codi font** ofereix botons equivalents, però és important entendre què fa cada pas.

## Problemes habituals

- **`git` no es reconeix:** tanca i torna a obrir el terminal o revisa la instal·lació.
- **No apareix el canvi:** desa el fitxer i executa `git status`.
- **No es pot fer `push`:** comprova l'autenticació i que el remot sigui correcte amb `git remote -v`.
- **El commit no apareix al compte:** revisa el correu configurat i el correu verificat a GitHub.
