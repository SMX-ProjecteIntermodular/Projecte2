# Guia 3. Markdown per treballar amb repositoris

Markdown és el llenguatge que s'utilitza per donar format al text amb fitxers que tenen l'extensió `.md`. GitHub i Visual Studio Code el mostren amb format quan obres, per exemple, el fitxer `README.md`.

Markdown és un llenguatge de marcatge lleuger, creat al 2004 per John Gruber amb l'objectiu de crear un llenguatge que fos fàcil de llegir i escriure i al mateix temps poder ser convertit en HTML, evitant la complexitat de l'HTML. Markdown és molt utilitzat per a documentació, blogs i fòrums, i és compatible amb moltes plataformes, com ara GitHub, Reddit i Stack Overflow. A més, és compatible amb molts editors de text i IDEs, com Visual Studio Code, Atom i Sublime Text.

En aquesta guia explicarem les principals característiques de Markdown i com utilitzar-les per crear documentació clara i ben estructurada per als vostres projectes.

## Títols i seccions

Els títols es creen amb el símbol `#`. Com més símbols, més petit és el nivell del títol:

```markdown
# Títol principal
## Secció
### Subsecció
```

Fes servir un sol `#` per al títol principal del document i mantén l'ordre dels nivells. No passis directament de `##` a `####` sense una raó clara.

## Paràgrafs i salts de línia

Escriu un paràgraf en una o diverses línies. Per començar un paràgraf nou, deixa una línia buida:

```markdown
Aquest és el primer paràgraf.

Aquest és el segon paràgraf.
```

Per forçar un salt de línia dins del mateix paràgraf, acaba la línia amb dos espais o fes servir `<br>` quan sigui necessari. Normalment, separar els paràgrafs és més llegible.

## Èmfasi i text de codi

```markdown
**negreta**
*itàlica*
***negreta i itàlica***
~~text ratllat~~
`git status`
```

Fes servir la negreta per destacar informació important i les cometes invertides per a ordres, noms de fitxer, carpetes o fragments curts de codi.

## Llistes

### Llista no ordenada

```markdown
- Primer element
- Segon element
  - Subelement
```

També es pot escriure amb `*` o `+`, però és millor mantenir el mateix estil dins del document.

### Llista ordenada

```markdown
1. Instal·la Git.
2. Clona el repositori.
3. Obre la carpeta amb Visual Studio Code.
```

### Llista de tasques

GitHub converteix aquesta sintaxi en caselles que es poden marcar:

```markdown
- [x] Crear el repositori
- [ ] Afegir el README
- [ ] Fer el primer commit
```

## Enllaços

Un enllaç té un text visible i una adreça:

```markdown
[Documentació de Git](https://git-scm.com/doc)
```

Per enllaçar un fitxer del mateix repositori, fes servir una ruta relativa:

```markdown
[Consulta la guia de comandes](guies/02-comandes-git.md)
```

Una ruta relativa parteix de la carpeta on es troba el fitxer actual. Comprova les majúscules, minúscules i extensions: `guies/02-comandes-git.md` no és el mateix que `Guies/02-comandes-git.md` en tots els sistemes.

També pots crear un enllaç a una secció del mateix document amb l'àncora que genera GitHub:

```markdown
[Ves a la secció de llistes](#llistes)
```

## Imatges

La sintaxi d'una imatge és semblant a la d'un enllaç, però comença amb `!`:

```markdown
![Captura de la pàgina principal](media/captura-readme.png)
```

El text entre claudàtors és el text alternatiu. Ha de descriure la imatge perquè el contingut sigui més accessible i també es pugui entendre si la imatge no es carrega.

Evita pujar imatges innecessàriament grans, en aquests casos és millor utilitzar una imatge més petita o un enllaç a la imatge externa a [Flickr](https://www.flickr.com/), [Unsplash](https://unsplash.com/) o [Pexels](https://www.pexels.com/), per exemple. Desa-les en una carpeta com `media/` i utilitza una ruta relativa quan la imatge formi part del repositori.

## Codi

### Codi dins d'una frase

Per a una ordre o un nom curt, fes servir una sola cometa invertida:

```markdown
Executa `git status` abans de fer un commit.
```

### Bloc de codi

Per mostrar diverses línies, utilitza tres accents greus i indica el llenguatge quan sigui possible:

````markdown
```bash
git status
git add README.md
git commit -m "Actualitza el README"
```
````

Altres identificadors habituals són `text`, `markdown`, `html`, `javascript` i `python`.

## Cites

El símbol `>` crea una cita:

```markdown
> Una bona documentació explica què fa el projecte i com començar-hi.
```

Les cites són útils per reproduir una indicació o destacar una informació, però no cal utilitzar-les per a tot el text.

## Separadors

Una línia amb tres guions crea un separador horitzontal:

```markdown
---
```

Utilitza'l només per separar parts que realment necessiten una divisió visual. Per a la majoria de documents, els títols ja són suficients.

## Taules

Les taules permeten comparar informació en files i columnes:

```markdown
| Ordre | Funció |
|---|---|
| `git status` | Mostra l'estat del repositori |
| `git diff` | Mostra els canvis |
| `git push` | Publica els commits |
```

La primera fila conté els encapçalaments i la segona, amb guions, separa els encapçalaments del contingut. No posis paràgrafs llargs dins d'una taula: costa llegir-los, especialment en pantalles petites.

## Caràcters especials

Alguns caràcters tenen un significat especial en Markdown. Si vols mostrar-los com a text, posa una barra inversa davant:

```markdown
\*Això no es mostrarà en cursiva\*
\# Això no és un títol
```

Els caràcters més habituals que es poden escapar són `\`, `` ` ``, `*`, `_`, `{}`, `[]`, `()`, `#`, `+`, `-`, `.`, `!` i `|`.

## README d'un repositori

Un `README.md` sol ser la primera pàgina que consulta una persona quan entra al repositori. Com a mínim, hauria d'incloure:

- El nom del projecte.
- Una descripció breu del seu objectiu.
- Els requisits o programes necessaris.
- Les instruccions per instal·lar-lo o començar-hi.
- Exemples d'ús, si són útils.
- Enllaços a documentació relacionada.
- L'autoria o la llicència, si el projecte ho requereix.

Comença amb una descripció clara i ordena la informació de la més necessària a la més específica.

## Previsualitzar i revisar

Abans de fer `commit` i `push`:

1. Desa el fitxer `.md`.
2. Obre la previsualització amb **Open Preview** o amb `Ctrl+Shift+V`.
3. Comprova que els títols tenen una jerarquia coherent.
4. Clica tots els enllaços i revisa les rutes relatives.
5. Comprova que les imatges es carreguen i tenen text alternatiu.
6. Revisa les llistes, les taules i els blocs de codi.
7. Llegeix el text per detectar errors d'ortografia i informació sensible.
8. Consulta els canvis amb `git diff` abans de preparar el commit.

## Errors habituals

- Oblidar una línia buida entre blocs de text o llistes.
- Escriure una ruta incorrecta en un enllaç o una imatge.
- No tancar les cometes invertides o els delimitadors d'un bloc de codi.
- Utilitzar un títol només perquè el text quedi més gran.
- Afegir una imatge sense text alternatiu.
- Posar secrets, contrasenyes o tokens en un exemple publicat.
- Fer servir HTML complex quan Markdown ja resol la necessitat.

## Editor específics per Markdown

Tot i que tots els editors de codi i IDE permeten escriure fitxers Markdown (Visual Studio Code, Atom, Sublime Text, etc.), també existeixen editors específics per a Markdown, com [Typora](https://typora.io/), [Mark Text](https://marktext.app/), [Obsidian](https://obsidian.md/) o [SoloMD](https://solomd.app/). Aquests editors ofereixen una previsualització en temps real i altres funcionalitats que poden ser útils per a la creació de documentació.

Si heu de treballar amb Markdown i no disposeu d'un editor específic, podeu utilitzar un editor en línia com [Dillinger](https://dillinger.io/) o [StackEdit](https://stackedit.io/). Aquests editors permeten escriure i previsualitzar Markdown directament al navegador, sense necessitat d'instal·lar cap programari addicional.

> 💡 Google Docs inclou Markdown en els formats permesos per exportar un document.
