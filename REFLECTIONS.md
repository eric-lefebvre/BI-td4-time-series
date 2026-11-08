# REFLECTIONS — TD4 : séries temporelles

## Stage 0 — Framing

**Reflection 1.** Il aurait suffi de faire une seule requête de test vers l'API avant
de concevoir quoi que ce soit : ouvrir dans le navigateur
`https://air-quality-api.open-meteo.com/v1/air-quality?latitude=48.0061&longitude=0.1996&hourly=carbon_dioxide&past_days=90`
(ou lire le paramètre `past_days` dans la documentation de l'Air Quality API) et regarder
si la réponse contenait bien 90 jours de valeurs horaires non nulles. Cette vérification
prend cinq minutes, alors que l'hypothèse « pas d'historique réel disponible » a orienté
toute la conception (données synthétiques). Une hypothèse sur la disponibilité des données
doit être testée comme n'importe quelle affirmation, pas servir de point de départ à la conception.

## Stage 1 — Collection

**Reflection 2.** *Prédiction faite avant d'exécuter le script (le 2026-11-08) :* je m'attends
à ce que le CO2 au Mans soit **en hausse** sur les 90 derniers jours (de mi-août à début
novembre). Dans l'hémisphère Nord, la photosynthèse de la végétation fait baisser le CO2
pendant la saison de croissance, avec un minimum vers fin août-septembre. Ensuite, la chute
des feuilles, la décomposition et le début du chauffage le font remonter jusqu'au printemps.
Comme la fenêtre commence près de ce minimum, la pente devrait être positive, de l'ordre de
quelques dixièmes de ppm par jour, avec un bruit journalier non négligeable lié à la météo
locale (vent, couche limite). Vérification au Stage 3.

## Stage 2 — Cleaning

**Reflection 3.** _À compléter._

## Stage 3 — Modeling

**Reflection 4.** _À compléter._

## Stage 4 — Storage

**Reflection 5.** _À compléter._

## Stage 5 — Visualization

**Reflection 6.** _À compléter._

## Stage 6 — On your own

**Reflection 7.** _À compléter._
