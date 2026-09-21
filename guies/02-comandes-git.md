# Guia 2. Treballant en el repositori amb Git

A la Guia 1 hem vist com crear un compte a GitHub i com crear un primer repositori i com clonar aquest repositori a l'ordinador. En aquesta guia veurem com treballar amb Git per a gestionar els canvis i sincronitzar-los amb el repositori remot de GitHub.

## Edició en local i control de versions

Un cop teniu el fitxer `README.md` al vostre ordinador, podeu començar a editar-lo, així mateix afegirem nous fitxers: de text, imatges, etc. Recordeu que Git funciona com una "màquina del temps". Per desar un canvi oficialment, hem de passar per dues etapes:

### El cicle de treball (Add i Commit)

Els canvis que feu als fitxers no es guarden automàticament al vostre historial de versions, sinó que hi ha dues etapes: el staging o "zona de preparació" (Add) i el repositori.

El staging és com una llista de coses que voleu incloure en la propera "foto" del vostre projecte. Allà podem anar afegint els arxius que s'han modificat o creat de nous. Té l'avantatge que podem anar afegint conforme anem treballant, i després fer un sol commit amb tots els canvis.

El commit és l'acció de "fer una foto" del projecte en aquell moment. Aquí és on posem una etiqueta descriptiva per recordar què hem fet. Els diferents commits formen l'historial del projecte i s'identifiquen amb un codi únic (hash).

```plain
           ┌────────────────────┐
           │  Working Directory │
           │ (fitxers editats)  │
           └─────────┬──────────┘
                     │  git add
                     ▼
           ┌────────────────────┐
           │    Staging Area    │
           │ (fitxers preparats)│
           └─────────┬──────────┘
                     │ git commit
                     ▼
           ┌────────────────────┐
           │     Repository     │   
           │ (historial segur)  │ 
           └─────────┬──────────┘
                     │ git checkout
                     ▼
           ┌────────────────────┐
           │  Working Directory │
           └────────────────────┘
```

A més, la sincronització amb el repositori remot (GitHub) es fa amb les comandes `git push` (per pujar canvis) i `git pull` (per baixar canvis).

### Add i Commit per per terminal

1. Afegir els canvis a la zona de preparació (Staging Area):  
   Això indica a Git quins fitxers volem incloure en la següent "foto".  

   ```Bash  
   git add nom_del_fitxer.md  
   # O per afegir-ho tot:  
   git add .
   ```

2. Confirmar els canvis (Commit):  
   Aquí posem una etiqueta al nostre canvi. Sigues descriptiu\!  

    ```Bash  
    git commit -m "Afegit apartat d'instal·lació a la guia"
    ```

### Add i Commit per VS Code

El primer caldrà fer, és definir l'usuari de Git (un nom i un correu) que serveix per identificar els nostres commits. Com que a l'ordinador de l'escola no tenim permisos per definir la configuració global, ho per cada repositori:

Obriu la terminal integrada a VS Code (Ctrl + ñ) i executeu:

```Bash
git config user.name "El teu Nom"
git config user.email elteumail
```

Veureu que a la barra lateral esquerra hi ha una icona amb tres cercles i línies (Control de Codi Font o Ctrl + Shift + G).

A mesura que modifiqueu els fitxers .md, aquests apareixeran a la llista de "Canvis" (Changes).

![VS Code Git](img/VCodeGit.png)

- **Afegir els canvis (Add / Staging):**

    Al costat del nom del fitxer que heu editat, apareixerà una icona d'un més (+).

    Si premeu el +, el fitxer passarà a la secció "Canvis preparats" (Staged Changes). Això equival a fer un git add.

    ![VS Code Add](img/VCodeAdded.png)

- **Confirmar els canvis (Commit):**

    A la part superior del panell veureu un quadre de text que diu "Missatge". Escriviu què heu fet (ex: Afegit apartat VS Code).

    Premeu el botó blau que diu "Confirmar" (Commit). Ara el canvi ja està guardat al vostre historial local.

    ![VS Code commit dialog showing blue Commit button in the source control panel, with a commit message field above it and staged changes listed below](img/VCodeCommit.png)
