# Activitat 2. Documentar i versionar: Markdown i Git local

**Durada:** 4 hores, en 2 sessions de 2 hores  
**Modalitat:** pràctica individual amb revisió entre iguals  
**Prerequisits:** Activitat 1 finalitzada

## Situació

La documentació tècnica ha de ser llegible tant per a persones com per a eines de desenvolupament. En aquesta activitat crearàs una fitxa tècnica en Markdown i practicaràs el cicle bàsic de Git en local abans de sincronitzar-la.

## Objectius

- Utilitzar títols, llistes, enllaços, imatges, codi i taules en Markdown.
- Entendre l'estat d'un repositori local.
- Practicar `status`, `add`, `commit`, `log` i `diff`.
- Fer commits petits i descriptius.
- Recuperar informació de l'historial sense perdre feina.

## Producte

Crea el fitxer `fitxa-tecnica.md` dins del repositori de pràctiques amb aquesta estructura:

```markdown
# Fitxa tècnica: [títol]

## Objectiu

## Materials

## Procediment

1. Pas inicial.
2. Segon pas.

## Comprovacions

- [ ] Primera comprovació
- [ ] Segona comprovació

## Incidències i solucions

| Incidència | Solució |
|---|---|
| Exemple | Exemple |

## Recursos

- [Documentació consultada](https://docs.github.com/)

```text
Comanda o sortida d'exemple
```
```

El tema pot ser una instal·lació de programari, la configuració d'una xarxa petita o una pràctica feta a classe. No incloguis contrasenyes ni adreces personals.

## Tasques

### 1. Crear el document amb Visual Studio Code

1. Crea `fitxa-tecnica.md`.
2. Escriu el títol i l'objectiu.
3. Afegeix una llista ordenada de passos.
4. Afegeix una llista de comprovació.
5. Inclou una taula i un enllaç.
6. Insereix una comanda dins d'un bloc de codi.
7. Obre la previsualització amb `Ctrl+Shift+V` i revisa el resultat.

### 2. Practicar Git en local

Obre el terminal a la carpeta del repositori i executa les ordres de la [guia de comandes](guias/02-comandes-git.md). Després de cada canvi, observa què informa Git.

Flux mínim que has de practicar:

```bash
git status
git diff
git add fitxa-tecnica.md
git status
git commit -m "Afegeix fitxa tecnica"
git log --oneline
```

Fes com a mínim tres commits:

1. `Crea estructura de fitxa tecnica`
2. `Completa procediment i comprovacions`
3. `Revisa format i recursos`

Entre commits, comprova que el canvi que vols registrar és el que esperes. Al final, sincronitza'l:

```bash
git push
```

### 3. Revisió entre iguals

Intercanvia el repositori amb una parella i revisa:

- Els títols segueixen una jerarquia clara.
- Les llistes i la taula es veuen correctament.
- Les instruccions es poden seguir.
- Els enllaços funcionen.
- No hi ha dades sensibles.
- Els commits expliquen canvis reals.

Fes una millora a partir del retorn i registra-la amb un commit nou.

## Evidències

- `fitxa-tecnica.md` publicat al repositori.
- Historial amb com a mínim 4 commits.
- Captura de la previsualització Markdown.
- Resposta breu: quina diferència hi ha entre `git add` i `git commit`?

## Criteris d'èxit

- El document usa almenys sis elements de Markdown.
- La previsualització és llegible.
- Els canvis passen per l'estat de preparació abans del commit.
- L'historial és ordenat i descriptiu.
- El fitxer final està sincronitzat amb GitHub.
