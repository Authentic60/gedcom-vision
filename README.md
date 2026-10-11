# GEDCOM To Do - Excel genealogy analysis

**[English](#english) | [Français](#français)**

---

## English

An Excel VBA macro that reads a **GEDCOM** file (exported from Geneanet, Heredis, Gramps, etc.) and automatically generates a **to-do list** of tasks to improve your family tree.

> **Beta version**: the macro is still being tested. Please report any problem you run into (see *Contributing*).
>
> **Note**: the macro's interface (buttons, sheet names, task texts) is in French.

### What it does

Each analysis creates two new sheets in the workbook:

- **`ToDo yymmdd-hhmm`**: the to-do list, computed from the loaded file.
  - Tasks are grouped into 7 categories: preparation, missing data, family links, sources, research, quality and consistency, sharing and showcasing.
  - Each task has a priority (High, Medium, Low), a status dropdown (To do, In progress, Blocked, Done), a suggested due date and a notes column.
  - A column shows how many records are concerned, and a cell displays the overall progress.
  - Tasks that concern no record are left out.
- **`Fiches yymmdd-hhmm`**: the list of people whose record is incomplete, ranked by priority (missing parents or birth date first), with details of what is missing.

If you load another GEDCOM file later, a new pair of sheets is created: previous analyses are kept, and a history with clickable links appears on the **Accueil** (home) sheet.

### What is analysed

- Missing birth and death dates and places
- Approximate dates and year-only dates
- People without linked parents, families without a marriage or without a spouse, families without children
- Births, marriages and deaths without a source
- People without sex, placeholder first names, people with several names, exact duplicates
- Date inconsistencies (death before birth, age over 110)
- Poorly detailed places, places outside France
- Technical notes and HTML tags left by the export
- People who may still be alive (to hide before any publication)

### Requirements

- **Excel for Windows**
- **Macros enabled**

Excel for Mac is not supported, because reading the file as UTF-8 relies on a Windows component (`ADODB.Stream`).

### Installation

1. Download [`gedcom_vision_vx.xx.xlsm`] (**Download raw file** button on its page).
2. Open the file.
3. Enjoy !

### Usage

1. On the **Accueil** sheet, click **Charger le fichier GEDCOM** (load the GEDCOM file) and pick your `.ged` file.
2. Click **Lancer l'analyse** (run the analysis).
3. Open the `ToDo ...` sheet that was created, and track your progress in the **Statut** (status) column.

### Known limitations

- Windows only (see *Requirements*).
- Only for GEDCOM download from Généanet
- The macro spots obvious gaps and inconsistencies but does not replace checking the original records. Duplicate detection only finds exact duplicates (same name and same birth date).
- The figures in the to-do list are frozen at analysis time: after fixing your tree, export a new GEDCOM and run the analysis again.
- Unusual or malformed GEDCOM files may give partial results.

### Privacy

Your GEDCOM file stays on your computer: the macro does not connect to any online service.

**Never publish your GEDCOM file in this repository or in an issue**: it contains information about people, including living people. To report a problem, describe it without attaching your personal data.

### Contributing

- **Found a bug or have an idea?** Open an [issue](../../issues) with your Excel version and the error message, if any.
- **Follow the project**: click **Watch** at the top of the page, and check the **Releases** section for new versions.

### License

This project is released under the MIT license (see the `LICENSE` file).

---

## Français

Macro VBA pour Excel qui lit un fichier **GEDCOM** (export de Geneanet, Heredis, Gramps, etc.) et génère automatiquement une **to-do list** des tâches à réaliser pour améliorer votre arbre généalogique.

> **Version bêta** : la macro est en cours de test. N'hésitez pas à signaler les problèmes rencontrés (voir la section *Contribuer*).

### Ce que fait la macro

À chaque analyse, deux nouvelles feuilles sont créées dans le classeur :

- **`ToDo aammjj-hhmm`** : la to-do list, calculée d'après le fichier chargé.
  - Les tâches sont classées en 7 catégories : préparation, données manquantes, liens familiaux, sources, recherches, qualité et cohérence, partage et valorisation.
  - Chaque tâche a une priorité (Haute, Moyenne, Basse), un statut en liste déroulante (À faire, En cours, Bloqué, Terminé), une échéance proposée et une colonne de notes.
  - Une colonne indique le nombre de fiches concernées, et une case affiche l'avancement global.
  - Les tâches qui ne concernent aucune fiche n'apparaissent pas.
- **`Fiches aammjj-hhmm`** : la liste des personnes dont la fiche est incomplète, classées par priorité (parents ou date de naissance manquants en premier), avec le détail de ce qui manque.

Si vous chargez un nouveau fichier GEDCOM plus tard, une nouvelle paire de feuilles est créée : les anciennes analyses sont conservées, et un historique avec liens cliquables apparaît sur la feuille **Accueil**.

### Ce qui est analysé

- Dates et lieux de naissance et de décès manquants
- Dates approximatives et années seules
- Personnes sans parents rattachés, familles sans mariage ou sans conjoint, familles sans enfant
- Naissances, mariages et décès sans source
- Personnes sans sexe, prénoms provisoires, personnes avec plusieurs noms, doublons exacts
- Incohérences de dates (décès avant naissance, âge supérieur à 110 ans)
- Lieux peu détaillés, lieux hors de France
- Notes techniques et balises HTML laissées par l'export
- Personnes possiblement vivantes (à masquer avant toute publication)

### Prérequis

- **Excel pour Windows**
- Les **macros activées**

Excel pour Mac n'est pas pris en charge, car la lecture du fichier en UTF-8 utilise un composant propre à Windows (`ADODB.Stream`).

### Installation

1. Téléchargez le fichier [`gedcom_vision_vx.xx.xlsm`] (bouton **Download raw file** sur sa page).
2. Ouvrez le fichier Excel.
3. Amusez-vous !

### Utilisation

1. Sur la feuille **Accueil**, cliquez sur **Charger le fichier GEDCOM** et choisissez votre fichier `.ged`.
2. Cliquez sur **Lancer l'analyse**.
3. Consultez la feuille `ToDo ...` créée, et suivez vos avancées dans la colonne **Statut**.

### Limites connues

- Windows uniquement (voir *Prérequis*).
- Uniquement pour les GEDCOM téléchargés depuis Généanet
- La macro détecte les manques et incohérences évidents, mais ne remplace pas la vérification dans les actes. Les doublons détectés sont uniquement les doublons exacts (même nom et même date de naissance).
- Les chiffres de la to-do list sont figés au moment de l'analyse : après avoir corrigé votre arbre, exportez un nouveau GEDCOM et relancez l'analyse.
- Les fichiers GEDCOM très atypiques ou mal formés peuvent produire des résultats partiels.

### Confidentialité

Votre fichier GEDCOM reste sur votre ordinateur : la macro ne se connecte à aucun service en ligne.

**Ne publiez jamais votre fichier GEDCOM sur ce dépôt ni dans une « issue »** : il contient des informations sur des personnes, dont des personnes vivantes. Pour signaler un problème, décrivez-le sans joindre vos données personnelles.

### Contribuer

- **Un bug ou une idée ?** Ouvrez une [issue](../../issues) en indiquant votre version d'Excel et le message d'erreur éventuel.
- **Suivre l'évolution du projet** : cliquez sur **Watch** en haut de la page, et consultez la section **Releases** pour les nouvelles versions.

### Licence

Ce projet est distribué sous licence MIT (voir le fichier `LICENSE`).
