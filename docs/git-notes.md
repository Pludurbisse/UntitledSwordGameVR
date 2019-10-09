# Git Notes

<!-- toc -->

- [Remplacer le contenu d'une branche par une autre](#Remplacer-le-contenu-dune-branche-par-une-autre)
- [Réinitialisier une branche à sa version originelle](#Réinitialisier-une-branche-à-sa-version-originelle)
- [Remplacer le contenu d'une branche avec le contenu local](#Remplacer-le-contenu-dune-branche-avec-le-contenu-local)

<!-- tocstop -->

## Remplacer le contenu d'une branche par une autre

Pour remplacer le contenu d'une branche par une autre, par exemple pour mettre à jour la branche de développement avec la branche principale, utiliser les instructions suivantes :

```
git checkout master
git merge -s ours dev
git checkout dev
git merge master
```
Remplace le contenu de **dev** avec le contenu de **master** (*replace dev with master*).

## Réinitialisier une branche à sa version originelle

```
git checkout dev
git reset --hard origin/dev
```
Remplace le contenu de la branche **dev** en local avec celui de la branche **dev** sur le réseau.

## Remplacer le contenu d'une branche avec le contenu local
```
git fetch
git reset --hard origin/dev
```
Remplacer le contenu de la branche **dev** sur le réseau avec celui de la branche **dev** en local (en supposant que l'on travaille sur la branche **dev** en local).
