# Guia 3. Incidències i seguretat

## Abans de publicar

Revisa que els arxius no tinguin errors o avisos de format, a l'editor Visual Code són els avisos que apareixen en la part inferior de la pantalla. D'aquesta manera, evitaràs haver de fer commits simplement per corregir errors de format.

Recordeu que el commit necessita un text clar i concís, que expliqui què s'ha fet. Evita missatges com "canvis" o "actualització", ja que no aporten informació útil. Un bon exemple seria: "Afegit fitxer README.md amb la documentació del projecte".

## Diagnosi ordenada

Quan una operació falla:

1. Llegeix el missatge d'error complet.
2. Executa `git status`.
3. Comprova la carpeta actual amb `pwd` o revisa la ruta de Visual Studio Code.
4. Comprova el remot amb `git remote -v`.
5. Revisa que el fitxer estigui desat.
6. Demana ajuda compartint l'error, però ocultant tokens i dades privades.

## Errors freqüents

### `not a git repository`

El terminal no és dins d'un repositori. Obre la carpeta correcta o executa:

```bash
cd ruta/de/la/carpeta
```

### `nothing to commit`

No hi ha canvis nous, o el fitxer no s'ha desat. Comprova `git status` i desa des de Visual Studio Code.

### Conflicte o canvi remot pendent

No eliminis fitxers ni facis ordres destructives. Executa `git pull`, llegeix les marques de conflicte i demana suport si no entens quina versió conservar.

### `rejected` en fer `push`

El remot pot tenir canvis que encara no tens. Executa `git pull` i revisa el resultat abans de tornar a fer `push`.

## Comunicació d'una incidència

Per demanar ajuda, indica:

- Què intentaves fer.
- Quina comanda o botó has utilitzat.
- El missatge d'error exacte.
- El resultat de `git status`.
- Què has provat després.

No enviïs mai contrasenyes, tokens ni claus privades.
