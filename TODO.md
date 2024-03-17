# Charset

- [x]: import fichier historique `ecrire/inc/charsets.php`, `ecrire/charsets/*.php`
- [ ]: composerisation

## Fichiers historiques

- `ecrire/inc/charsets.php`
- `ecrire/charsets/*.php`
- inclus dans `ecrire/tests/Texte/CouperTest.php` pour tester `couper()`
  - pas de tests dédiés
- appels `inc/charsets`:
  - spip/spip:
  - plugins-dist:

## Dépendances

### Constantes

_DEFAULT_CHARSET

### Globales

déclare `$GLOBALS['CHARSET'][...]` dans `charsets/*.php`

### Metas

'pcre_u'

### Config

'charset'

### Fonctions

- `include_spip()`
- `find_in_path()`
- `spip_logger()`
- `ecrire_meta()`
- `lire_config()`
- `corriger_caracteres()`

par autoloading spip

- 'inc/config' pour lire_config('charset')
- 'inc/meta' pour ecrire_meta()
- 'inc/filtres' pour corriger_caracteres()

## Récup historique git

```bash
git clone --single-branch --no-tags git@git.spip.net:spip/spip.git charset
cd charset
git filter-repo \
  --path ecrire/inc/charsets.php \
  --path ecrire/charsets
  --path-rename ecrire/inc/charsets.php:inc/charsets.php \
  --path-rename ecrire/charsets:charsets \
  --force
git branch -m 0.1
```

## composer
