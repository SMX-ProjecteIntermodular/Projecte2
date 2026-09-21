# Guia 2. Comandes bàsiques de Git

Executa les ordres des de la carpeta del repositori. Pots fer la mateixa operació des de la interfície de Visual Studio Code.

| Ordre | Funció |
|---|---|
| `git status` | Mostra l'estat dels fitxers i la branca actual |
| `git diff` | Mostra canvis encara no preparats |
| `git add fitxer` | Prepara un fitxer per al proper commit |
| `git add .` | Prepara tots els canvis de la carpeta actual; usa'l amb atenció |
| `git commit -m "Missatge"` | Desa un punt de l'historial |
| `git log --oneline` | Mostra l'historial resumit |
| `git show` | Mostra el contingut d'un commit |
| `git remote -v` | Mostra els repositoris remots configurats |
| `git push` | Publica commits locals al remot |
| `git pull` | Descarrega i integra canvis del remot |

## El cicle de tres zones

```text
Working tree       ->      Staging area       ->      Repository
fitxers editats            git add                   git commit
```

`git status` indica en quina zona es troba cada canvi. Un fitxer no forma part del commit fins que s'ha preparat amb `git add`.

## Exemple complet

```bash
git status
# edita un fitxer
git diff
git add README.md
git status
git commit -m "Actualitza documentacio"
git log --oneline -3
git push
```

## Desfer o corregir amb prudència

Si només vols treure un fitxer de la zona de preparació, sense perdre el contingut:

```bash
git restore --staged README.md
```

Si vols descartar canvis locals d'un fitxer, atura't i comprova abans què perdràs. Aquesta ordre elimina canvis no commitats:

```bash
git restore README.md
```

Durant les primeres pràctiques, demana ajuda abans d'utilitzar ordres que eliminin fitxers o reescriguin l'historial.

## Bons missatges de commit

Un bon missatge explica què ha canviat:

- `Afegeix estructura del perfil`
- `Completa instruccions de xarxa`
- `Corregeix enllaç a la documentació`

Evita missatges com `canvis`, `prova` o `coses`, perquè no ajuden a entendre l'historial.
