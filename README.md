# L'Atelier du Bon Document

> Dix-sept savoir-faire d'écriture professionnelle, sculptés pour les agents d'IA.
> Chaque dossier est une compétence : il transforme un sujet vague en un document qu'un
> comité peut lire, critiquer… et approuver.

TDR, mémos de décision, budgets justifiés, OKR alignés, dossiers de recrutement, veille
réglementaire, audits qualité… **Ce dépôt est une boîte à outils complète** pour quiconque
travaille avec un agent d'IA et doit produire des documents qui tiennent la route devant
une hiérarchie, un donateur ou un client.

---

## 🧭 Pourquoi cette collection existe

Un document professionnel ne se rédige pas : il **se construit**. Chaque dossier ici
encapsule des années de pratique — méthode, pièges, séquences de rédaction, contrôles de
qualité — et la confie à un agent d'IA.

Le fil conducteur : **MPR** (*Méthode – Planning – Ressources*). La qualité, le coût et les
délais ne se décrètent pas ; ils sont la conséquence d'une méthode, d'un planning et de
ressources. Tout le reste — l'ordre de rédaction, les portes de validation, les tests
d'orphelins — découle de ce principe.

## 🗂 Les dix-sept compétences

| Compétence | Elle écrit / prépare | Pour qui |
|---|---|---|
| **`tor-writer`** | Termes de référence et leurs dix variantes (note de cadrage, plan de travail, cahier des charges, dossier d'appel d'offres, proposition technique, plan directeur…) | Maîtres d'ouvrage, consultants |
| **`decision-memo`** | Mémorandum de décision ou d'arbitrage : options comparées, critères, **une** recommandation, un responsable nommé | Tout niveau hiérarchique |
| **`exec-summary`** | Synthèse d'une page, conclusion en premier (principe de la pyramide) | Décideurs pressés |
| **`budget-planner`** | Budget justifié ligne par ligne, suivi d'exécution, analyse d'écarts, re-prévision | Directeurs, chefs de projet |
| **`project-tracker`** | Suivi opérationnel : tableau de bord, planning détaillé, rapports d'avancement, journal des décisions et blocages | Chefs de projet |
| **`risk-analysis`** | Analyse des risques complète : identification, évaluation, analyse, traitement | Risqueurs, auditeurs |
| **`stakeholder-mapper`** | Cartographie des parties prenantes (pouvoir × intérêt) et stratégie d'engagement différenciée, matrice RACI | Porteurs de changement |
| **`meeting-facilitator`** | Réunions qui **décident** : ordre du jour, plan d'animation, journal des décisions et actions | Animateurs de réunion |
| **`negotiation-prep`** | Négociations structurées : BATNA, ZOPA, point de réserve, arguments | Négociateurs |
| **`okr-cascader`** | Traduction d'objectifs stratégiques en OKR mesurables, alignés sans copie servile | Management |
| **`performance-review`** | Entretiens annuels, feedback structuré (SBI), plans de développement | Managers, RH |
| **`recruitment-writer`** | Fiches de poste, grilles d'entretien, questions comportementales, synthèses comparatives | Recruteurs |
| **`presentation-writer`** | Supports de présentation et dossiers visuels : compte-rendu, dossier de financement, pitch | Orateurs, levée de fonds |
| **`procedure-writer`** | Documentation d'un SMQ : procédures, manuel qualité, fiches de processus, instructions de travail | Qualité |
| **`smq-analysis`** | Analyse et écart d'un système de management de la qualité (approche processus, exigences normatives) | Auditeurs, qualité |
| **`regulatory-watch`** | Veille réglementaire : périmètre, cadence, format d'alerte, journal de veille | Conformité |
| **`mail-writer`** | Correspondance professionnelle au registre juste — y compris l'administratif français | Tous |

## 🔗 Des compétences qui travaillent ensemble

Chaque dossier se termine par un relais naturel. Un `tor-writer` validé appelle un
`project-tracker` pour tenir le planning qu'il a posé ; une négociation préparée par
`negotiation-prep` nourrit un `decision-memo` ; un `risk-analysis` chiffré est cité
**verbatim** dans un mémo de décision, jamais réécrit de mémoire. Les documents se
répondent, comme dans un vrai bureau.

## 🛠 Installation

Chaque dossier est autonome et suit la structure d'une **Claude Agent Skill** :

```
skill/
├── SKILL.md                  ← les instructions (le déclenchement, le pipeline)
├── references/               ← méthodes, pièges, exemples commentés
└── assets/                   ← gabarits de tableaux, guides de style .docx
```

1. Copiez le dossier d'une compétence (ex. `decision-memo`) dans le répertoire des
   compétences de votre agent.
2. Déclenchez-la avec une phrase simple, dans la langue que vous écrivez :
   - « Rédige les TDR pour… »
   - « Aide-moi à préparer cette négociation avec… »
   - « Prépare le budget justifié de… »
   - « Donne-moi une synthèse d'une page de ce rapport. »
3. Suivez les portes de validation — elles sont là pour votre bien, jamais sautées.

## ⚖️ Valeurs qui traversent les dix-sept dossiers

- **Ne jamais inventer** un montant, un effectif, une date, une référence légale. Ce qui
  manque se *signale* (`[À COMPLÉTER : …]`), jamais se *fabrique*.
- **Une recommandation, pas un menu.** Les options se comparent pour choisir, pas pour
  refiler le choix au décideur.
- **Un propriétaire nommé, jamais un collectif.** « L'équipe mettra en œuvre » n'engage
  personne.
- **Un ordre de rédaction rigoureux** — la méthode avant les ressources, les ressources
  avant le planning, le planning avant le coût, le coût avant la synthèse.
- **Résultats dans la langue de l'utilisateur**, Markdown dans la conversation,
  `.docx` à la demande.

## 📄 Licence

Non spécifiée — le dépôt est ouvert. Utilisez, adaptez, et faites vivre ces méthodes.

---

*Dix-sept métiers du document, un seul standard : le document qui se défend tout seul
devant un comité.*
