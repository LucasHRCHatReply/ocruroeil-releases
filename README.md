# Ocruroeil pour macOS

Ocruroeil rend cherchable une photo de document ou un PDF scanné. On dépose le fichier ; l'app rend, à côté de lui,
un PDF dont chaque page garde son image avec un texte invisible dessous (recherche ⌘F, sélection, copie) et un fichier
texte brut. La lecture se fait sur le Mac, avec le moteur de texte d'Apple : aucun fichier ne quitte l'ordinateur,
aucun compte, aucune télémétrie.

Ce dépôt ne contient que les versions à installer. Le code source n'est pas public.

## Ce qu'il faut

- un Mac à puce Apple (M1 ou plus récent) ;
- macOS 14 ou plus.

## Installer

Dans Terminal (Cmd + Espace, « Terminal »), une seule commande, qui installe aussi les mises à jour :

```
curl -fsSL https://raw.githubusercontent.com/LucasHRCHatReply/ocruroeil-releases/main/installer.sh | zsh
```

Le script télécharge la dernière version, vérifie l'empreinte SHA-256 du zip, l'identifiant de l'app et sa signature
(équipe Apple `JT9FY7PP7K`, `codesign --verify --deep --strict`), copie l'app dans ~/Applications, puis l'ouvre.

Autre voie : télécharger `Ocruroeil.dmg` dans les [Releases](../../releases/latest), l'ouvrir, glisser Ocruroeil sur
Applications. Le disque est signé, non notarisé : au premier lancement, clic droit sur l'app › Ouvrir.
