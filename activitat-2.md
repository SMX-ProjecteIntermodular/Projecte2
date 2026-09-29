# Activitat 2. Documentar i versionar: Markdown i Git local

## Presentació de l'activitat

La documentació tècnica: guies de instal·lació, de configuració, procediments de manteniment, etc. són un recurs molt valuós pels equips de treball i departaments de IT de les organitzacions. La seva qualitat i claredat és fonamental per a la productivitat i la seguretat de les operacions.

Un problema habitual és que la documentació es quedi obsoleta i no reflecteixi l'estat real del sistema. Per això, és important versionar-la i mantenir un historial de canvis. Així, qualsevol persona que consulti la documentació podrà veure quan s'ha actualitzat per última vegada i quins canvis s'han fet.

El versionat tot i que inicialment es va dissenyar per a programari, és una eina molt útil per a qualsevol tipus de documentació. En aquesta activitat aprendràs a escriure documentació tècnica amb Markdown i a versionar-la amb Git en local abans de sincronitzar-la amb GitHub.

### Durada de l'activitat

- 4 hores (dues sessions de 2 hores).

### Objectius de l'activitat

- Editar un document en format Markdown amb Visual Studio Code.
- Entendre l'estat d'un repositori local.
- Practicar `status`, `add`, `commit`, `log` i `diff`.
- Fer commits petits i descriptius.
- Recuperar informació de l'historial sense perdre feina.

### Competències treballades

m) Organitzar i desenvolupar el treball assignat mantenint unes relacions professionals adequades en l’entorn de treball.

### Resultats d'aprenentatge i criteris d'avaluació

1713.RA5. Transmet informació amb claredat, de manera ordenada i estructurada.

- 5.1 Manté una actitud ordenada i metòdica en la transmissió de la informació.

### Continguts

- Control de versions.
- Edició de documentació tècnica amb Markdown.

### Capacitats clau

- Autonomia
- Organització del treball
- Responsabilitat

### Semàfor ús de la IA

🟠 Aquesta activitat permet un ús parcial o restringit.

- Permès per com a eina de suport en la millora de la redacció dels informes, cerca preliminar d'informació, estructuració d'idees o explicació de conceptes teòrics complexos.
- Condicions: Cal processar, entendre i validar sempre els resultats rebuts. **Està totalment prohibit copiar l'enunciat d'un exercici directament al xat de la IA i enganxar la resposta generada** per al lliurament final sense treball propi ni anàlisi crítica.

## Enunciat de l'activitat

Crea el fitxer `fitxa-tecnica.md` dins del repositori de pràctiques amb aquesta estructura:

```markdown
# Fitxa tècnica: [títol]

## Objectiu

## Materials

## Procediment

1. Pas inicial.
2. Segon pas.
...

## Comprovacions

- [ ] Primera comprovació
- [ ] Segona comprovació

## Incidències i solucions

| Incidència | Solució |
|---         |---      |
| Exemple    | Exemple |

## Recursos

- [Documentació consultada](https://docs.github.com/)

```

El tema pot ser una instal·lació de programari, la configuració d'una xarxa petita o una pràctica feta a classe. Inclou alguna imatge per il·lustrar el procés.

## Tasques

### 1. Crear el document amb Visual Studio Code

1. Crea `fitxa-tecnica.md`.
2. Escriu el títol i l'objectiu.
3. Afegeix una llista ordenada de passos.
4. Afegeix una llista de comprovació.
5. Inclou una taula, una imatge i un enllaç.
6. Insereix una comanda dins d'un bloc de codi.
7. Obre la previsualització amb `Ctrl+Shift+V` i revisa el resultat.

### 2. Practicar Git en local

Obre el terminal a la carpeta del repositori i executa les ordres de la [guia de comandes](guies/02-comandes-git.md). Després de cada canvi, observa què informa Git.

Flux mínim que has de practicar:

```bash
git status
git diff
git add fitxa-tecnica.md
git status
git commit -m "Afegeix fitxa tècnica"
git log --oneline
```

Fes com a mínim tres commits més:

1. `Crea estructura de fitxa tècnica`
2. `Completa procediment i comprovacions`
3. `Revisa format i recursos`
4. `Afegeix explicació sobre el flux de treball amb Git`

Entre commits, comprova que el canvi que vols registrar és el que esperes. Al final, sincronitza'l des del terminal integrat amb ```git push origin main``` o utilitza el botó de sincronització de Visual Studio Code.

## Evidències

Lliurament a la tasca del Moodle corresponent:

- L'enllaç al repositori amb l'historial de canvis (commits).

## Materials i enllaços de suport

- Guia [02-comandes git](guies/02-comandes-git.md)

- Guia [03-Markdown](guies/03-markdown.md)

- Luis Llamas. [Curso de git](https://www.luisllamas.es/curso-git/)
