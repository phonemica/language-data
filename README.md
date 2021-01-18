# Languages

This repository is for our languages dataset. It is used for classification and localisation. Data is stored in `data.tsv`, which is the only file that should be changed.

## Making changes

In order to contribute, please fork the repository. Once changes have been made, request a merge, at which point if the changes are accepted, your contributions will be incorporated and show up on the site soon after. This also helps us keep track of contributions so that you can be properly acknowledged on the site.

# Data format

The dataset in this repository is in a tab separated file (tsv) with the following format:

| glottolog | local  | parent | parent2 | en          | tw     | cn     | ko     | as             | my        |
|-----------|--------|--------|---------|-------------|--------|--------|--------|----------------|-----------|
| mand1415  | 官话   |        |         | Mandarin    | 官話   | 官话   | 관화   | মান্য চীনা ভাষা | မန်ဒရင်   |
| hakk1236  | 客語   |        |         | Hakka       | 客語   | 客语   | 커쟈어 | খেচিয়া         | ဟတ်ကာစကား |
| xuan1238  | 宣州片 | 吴语   |         | Xuānzhōu Wu | 宣州片 | 宣州片 | 선주   |                |           |
| 0000yuexi | 粤西片 | 客语   |         | Yuexi Hakka | 粵台片 | 粤台片 | 월태   |                |           |

The `local` column is currently holds pre-existing labels for conversion, but is otherwise for local scripts for which there is not an i18n localisation for the entire site. For example, Nuosu Yi as ꏃꎖꉙ, which will be displayed on the relevant pages, but is not otherwise part of the localisation scheme.

The `parent` columns are temporary and will eventually be removed. Each column after holds a language, with a two-letter localisation code. These are not standard ISO codes, as we are more concerned with script than language variety in these cases. Thus `en` is English, `tw` is traditional Chinese characters, `cn` for simplified, `ko` for Korean, `as` for Assamese-Bengali and `my` for Burmese. We will add additional languages as there is demand.

## Glottocodes

Each language should be linked to either a glottocode as found on [Glottolog](https://glottolog.org/), or an internal pseudocode. Glottocodes are four letters followed by four numbers, and are provided only from Glottolog. Do not create new glottocodes. If a language variety's subgrouping is well established but the variety is not yet on Glottolog, that is something to be handled through the proper channels. Again, please **do not include invalid glottocodes** in this repository.

## Pseudocodes

Pseudocodes are our alternative language identifiers, generally in the format `0000language` where `language` is a plain form of the language name. These are only used for language which are not currently represented in Glottolog. For example, the Chuānqián 川黔 dialect of Southwestern Mandarin does not currently have a glottocode, and so internally we use the pseudocode `0000chuanqian`. All pseudocodes begin with `0000` unless conflicting with a previous pseudocode, in which case the number is incremented to `0001` and so on.
