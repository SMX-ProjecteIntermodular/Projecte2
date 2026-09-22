# Activitat 3. El meu repositori de perfil professional

**Durada:** 4 hores, en 2 sessions de 2 hores  
**Modalitat:** projecte individual i presentació breu  
**Prerequisits:** Activitats 1 i 2 finalitzades

## Repte

Transformaràs el repositori creat a l'activitat 1 en una carta de presentació professional. El resultat ha de permetre que una persona que no et coneix entengui què estàs estudiant, què saps fer i cap a on vols avançar.

## Estructura mínima del `README.md`

```markdown
# Nom o àlies professional

Una frase de presentació.

## Sobre mi

## Què estic aprenent

## Tecnologies

- Tecnologia 1
- Tecnologia 2

## Projectes i pràctiques

| Projecte | Descripció | Estat |
|---|---|---|
| Projecte 1 | ... | En curs |

## Objectius

## Contacte o enllaços
```

Pots afegir una imatge o avatar, sempre que tinguis dret a utilitzar-lo i que no exposi informació que no vulguis fer pública.

## Tasques

### 1. Planificar

Abans d'escriure, defineix:

- Quin nom o àlies vols mostrar.
- Tres competències actuals o en desenvolupament.
- Tres tecnologies que vols aprendre.
- Dos projectes de classe que podràs documentar.
- Un objectiu professional a curt termini.

### 2. Editar en local

1. Obre el repositori amb Visual Studio Code.
2. Reescriu el `README.md` amb contingut propi.
3. Utilitza la previsualització Markdown.
4. Revisa els enllaços i la informació pública.
5. Desa el canvi i consulta `git diff`.
6. Fes com a mínim dos commits amb missatges concrets, per exemple:

```bash
git add README.md
git commit -m "Afegeix perfil professional"
git push
```

```bash
git add README.md
git commit -m "Millora estructura i enllaços del perfil"
git push
```

### 3. Revisar el perfil publicat

Obre el repositori a GitHub com si fossis una persona externa i comprova:

- El títol identifica clarament el perfil.
- La informació més important apareix al principi.
- El text no conté faltes greus ni dades sensibles.
- Els enllaços funcionen.
- La taula i les llistes es renderitzen correctament.
- L'historial mostra una evolució real.

### 4. Presentar

Fes una presentació d'un minut que inclogui:

1. Qui ets i què estudies.
2. Què mostra el repositori.
3. Quin canvi has fet en local i com l'has pujat.
4. Quin aspecte continuaràs millorant.

## Lliurament

Lliura al professorat:

- URL del repositori de perfil.
- Una còpia o exportació del `README.md`, si es demana.
- Historial visible amb almenys 5 commits en total.
- Autoavaluació de 5-10 línies.

## Rúbrica específica

| Aspecte | Excel·lent | Assolit | En procés |
|---|---|---|---|
| Perfil | Clar, personal i professional | Compleix l'estructura mínima | Incomplet o difícil d'entendre |
| Markdown | Sintaxi variada i ben renderitzada | Usa la sintaxi bàsica | Presenta errors freqüents |
| Git | Historial coherent i sincronització autònoma | Fa el flux amb alguna ajuda | No pot explicar el flux |
| Seguretat | No exposa dades sensibles | Revisa la informació pública | Publica dades inadequades |
| Revisió | Millora el perfil a partir de feedback | Fa una revisió bàsica | No incorpora revisions |
