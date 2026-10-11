# Security Policy / Politique de sécurité
 
**[English](#english) | [Français](#français)**
 
---
 
## English
 
### Supported versions
 
This project is in **beta**. Only the **latest release** (and the current version of `AnalyseGedcom.bas` on the main branch) receives fixes.
 
| Version | Supported |
|---|---|
| Latest release | Yes |
| Older releases | No |
 
### Reporting a vulnerability
 
Please **do not report security problems in a public issue**.
 
1. Go to the **Security** tab of this repository.
2. Click **Report a vulnerability** (GitHub private vulnerability reporting).
3. Describe the problem: what you observed, the steps to reproduce it, and your Excel version.
If the **Report a vulnerability** button is not available, open a public issue titled "Security contact request" **without any technical details**, and a private way to exchange will be arranged.
 
**Never attach your GEDCOM file** or any file containing personal data, even in a private report. A small, anonymised extract that reproduces the problem is enough.
 
### What to expect
 
This is a personal open-source project maintained on a best-effort basis. Reports are read as soon as possible, but no response time is guaranteed. Confirmed issues are fixed in a new release, and the reporter is credited if they wish.
 
### Scope
 
The macro runs locally in Excel and does not connect to any online service. Relevant reports include, for example:
 
- code in the macro that could run unintended actions on the user's computer
- a crafted GEDCOM file that makes the macro behave dangerously (not just fail with an error)
- a release file that does not match the source code in this repository
Not in scope: general limitations listed in the documentation (for example, Windows-only support), or Excel's own macro security settings.
 
### Advice for users
 
- Macros are code that runs on your computer. Download `AnalyseGedcom.bas` or the `.xlsm` file **only from this repository's official page or its Releases**.
- You can open the `.bas` file in a text editor and read it before importing it.
- Keep Excel's macro security enabled, and only enable macros in files you trust.
---
 
## Français
 
### Versions prises en charge
 
Ce projet est en **bêta**. Seule la **dernière version publiée** (et la version actuelle de `AnalyseGedcom.bas` sur la branche principale) reçoit des corrections.
 
| Version | Prise en charge |
|---|---|
| Dernière version publiée | Oui |
| Versions plus anciennes | Non |
 
### Signaler une vulnérabilité
 
Merci de **ne pas signaler un problème de sécurité dans une issue publique**.
 
1. Allez dans l'onglet **Security** de ce dépôt.
2. Cliquez sur **Report a vulnerability** (signalement privé de GitHub).
3. Décrivez le problème : ce que vous avez observé, les étapes pour le reproduire et votre version d'Excel.
Si le bouton **Report a vulnerability** n'est pas disponible, ouvrez une issue publique intitulée « Security contact request » **sans aucun détail technique**, et un moyen d'échange privé sera mis en place.
 
**Ne joignez jamais votre fichier GEDCOM** ni aucun fichier contenant des données personnelles, même dans un signalement privé. Un petit extrait anonymisé qui reproduit le problème suffit.
 
### À quoi s'attendre
 
Ce projet open source est personnel et maintenu au mieux de ses possibilités. Les signalements sont lus dès que possible, mais aucun délai de réponse n'est garanti. Les problèmes confirmés sont corrigés dans une nouvelle version, et la personne à l'origine du signalement est citée si elle le souhaite.
 
### Périmètre
 
La macro s'exécute localement dans Excel et ne se connecte à aucun service en ligne. Sont par exemple concernés :
 
- du code dans la macro qui pourrait exécuter des actions non voulues sur l'ordinateur de l'utilisateur
- un fichier GEDCOM spécialement construit qui fait se comporter la macro de façon dangereuse (et pas seulement afficher une erreur)
- un fichier de version publiée qui ne correspond pas au code source de ce dépôt
Ne sont pas concernés : les limites générales indiquées dans la documentation (par exemple, la prise en charge de Windows uniquement) ou les paramètres de sécurité des macros d'Excel.
 
### Conseils aux utilisateurs
 
- Une macro est du code qui s'exécute sur votre ordinateur. Téléchargez `AnalyseGedcom.bas` ou le fichier `.xlsm` **uniquement depuis la page officielle de ce dépôt ou ses Releases**.
- Vous pouvez ouvrir le fichier `.bas` dans un éditeur de texte et le lire avant de l'importer.
- Gardez la sécurité des macros d'Excel activée, et n'activez les macros que dans des fichiers de confiance.
