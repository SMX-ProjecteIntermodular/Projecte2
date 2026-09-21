# Activitat 1. El primer repositori: GitHub i Visual Studio Code

**Durada:** 4 hores, en 2 sessions de 2 hores  
**Modalitat:** pràctica guiada individual  
**Prerequisits:** cap

## Situació

Començarem preparant les eines que farem servir durant el projecte. Crearàs un compte de GitHub, instal·laràs Git i connectaràs un repositori remot amb una carpeta local oberta amb Visual Studio Code.

## Objectius

- Crear un compte de GitHub i configurar-lo de manera segura.
- Instal·lar Git i Visual Studio Code.
- Configurar el nom i el correu de Git.
- Crear un repositori a GitHub.
- Clonar-lo i obrir-lo amb Visual Studio Code.
- Fer i sincronitzar el primer commit.

## Tasques

### 1. Crear el compte de GitHub

1. Accedeix a [GitHub](https://github.com/) i crea un compte amb el correu indicat pel centre.
2. Tria un nom d'usuari professional i fàcil de recordar.
3. Verifica el correu i activa l'autenticació en dos passos si és possible.
4. Completa només la informació pública necessària.
5. No comparteixis mai la contrasenya.

### 2. Preparar les eines

Instal·la Git i Visual Studio Code seguint la [guia d'iniciació](guias/01-iniciacio-git-github-vscode.md). Obre el terminal integrat de Visual Studio Code i comprova les versions:

```bash
git --version
code --version
```

Configura la identitat de Git, substituint les dades per les teves:

```bash
git config --global user.name "Nom Cognom"
git config --global user.email "correu@exemple.cat"
```

Comprova la configuració:

```bash
git config --global --list
```

### 3. Crear i clonar un repositori

1. A GitHub, crea un repositori anomenat `perfil-git-nom-cognom`.
2. Afegeix una descripció curta.
3. Marca l'opció per crear un `README.md`.
4. Mantén-lo privat mentre fas les primeres proves, si el professorat ho indica.
5. Copia l'URL HTTPS del repositori.
6. A Visual Studio Code, obre la paleta d'ordres amb `Ctrl+Shift+P` i tria **Git: Clone**.
7. Enganxa l'URL, escull una carpeta de treball i obre el repositori clonat.

### 4. Fer el primer canvi

Edita el `README.md` i afegeix:

- El teu nom o àlies acadèmic.
- El cicle formatiu que curses.
- Una frase sobre què vols aprendre.

Desa el fitxer i, des de l'apartat **Control de codi font** de Visual Studio Code:

1. Revisa el canvi.
2. Escriu el missatge `Afegeix presentacio inicial`.
3. Fes **Commit**.
4. Fes **Sync Changes** o **Push**.
5. Actualitza GitHub i comprova que el canvi hi apareix.

## Evidències

Lliura:

- L'enllaç al repositori.
- Una captura on es vegi el repositori obert a Visual Studio Code.
- Una captura de GitHub amb el primer canvi publicat.
- Una frase explicant què diferencia Git de GitHub.

## Comprovació ràpida

Abans de donar l'activitat per acabada, respon:

- Puc trobar el meu repositori local a l'ordinador?
- El repositori local està connectat amb el remot?
- Puc veure el meu commit a GitHub?
- He publicat alguna dada que no hauria de ser pública?

## Criteris d'èxit

- El compte funciona i té un nom d'usuari professional.
- Git i Visual Studio Code estan instal·lats.
- El repositori local i el remot estan connectats.
- El primer canvi es pot veure a GitHub.
- El commit descriu el canvi realitzat.
