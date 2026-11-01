# Reconnaissance intelligente d'événements par fusion multimodale des informations visuelles et sonores

**Projet de Fin d'Année (PFA) – Fiche n°15**
Cycle ingénieur – 5ᵉ année | EMSI Casablanca | Année universitaire 2026

---

## Équipe

| Nom | Rôle |
|---|---|
| Marwa Elomari Alaoui | Étudiante ingénieure |
| Zainab Belgas | Étudiante ingénieure |
| Chaimaa Ezzerag | Étudiante ingénieure |

**Encadrant :** Pr. Mohammed Mestari


---

## Résumé

Certains événements sont plus facilement reconnaissables lorsque les informations visuelles et sonores sont exploitées conjointement. Ce projet vise à concevoir un système de classification multimodale associant deux réseaux d'extraction de caractéristiques (un encodeur visuel et un encodeur audio). Nous comparons plusieurs stratégies de fusion et mesurons la robustesse du modèle lorsque l'une des modalités est dégradée ou absente.

## Problématique

Dans quelle mesure la fusion des représentations visuelles et sonores améliore-t-elle la reconnaissance d'événements par rapport à des modèles exploitant une seule modalité ?

## Objectifs

1. Étudier les approches d'apprentissage multimodal et de fusion de caractéristiques.
2. Préparer un corpus d'extraits vidéo accompagnés de leur piste sonore.
3. Développer deux modèles unimodaux de référence (vision et audio).
4. Implémenter une stratégie de fusion multimodale.
5. Évaluer la robustesse du système face au bruit et aux modalités manquantes.

## Architecture

```
Vidéo → Encodeur visuel ↘
                         Fusion → Classificateur → Événement reconnu
Audio → Encodeur audio  ↗
```

## Méthodologie

- Sous-ensemble réduit d'événements audio-visuels (4 à 6 classes, extraits courts).
- Extraction des représentations par des modèles préentraînés (visuel et audio).
- Comparaison d'une **fusion tardive** simple et d'une **fusion de caractéristiques**.
- Analyse des performances lorsque la qualité du son ou de l'image diminue.

## Technologies

Python · PyTorch · OpenCV · Librosa · modèles préentraînés visuels et audio

## Livrables

- Deux modèles unimodaux (vision, audio)
- Modèle de fusion multimodale
- Démonstrateur de classification d'extraits
- Analyse comparative des performances
- Rapport scientifique et code reproductible

## Métriques d'évaluation

Macro-F1 · Accuracy · Robustesse au bruit · Temps d'inférence · Performance en l'absence d'une modalité

## Calendrier (12 semaines)

| Période | Phase | Jalon |
|---|---|---|
| Semaines 1–3 | Validation scientifique | Note de cadrage validée |
| Semaines 4–6 | Première réalisation | Démonstration intermédiaire |
| Semaines 7–10 | Contribution avancée | Validation expérimentale |
| Semaines 11–12 | Finalisation et soutenance | Dépôt des livrables |

## Structure du dépôt

```
PFA/
├── data/          # Jeux de données (non versionnés)
├── notebooks/     # Expérimentations
├── src/           # Code source (modèles, fusion, évaluation)
├── demo/          # Démonstrateur
├── report/        # Rapport et présentation
└── README.md
```

## Périmètre

Quatre à six classes d'événements, extraits courts, extraction de caractéristiques par modèles préentraînés.

---

*EMSI Casablanca – Filière IA – 2026*
