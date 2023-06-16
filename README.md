<p align="center"><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/logo.svg"/></a><br/><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/xxai.svg"/></a></p><p align="center"><a href="https://github.com/xxai-art/doc#readme"><img alt="I18N" src="https://cdn.jsdelivr.net/gh/wactax/img/t.svg"/></a>　<a href="https://groups.google.com/u/0/g/xxai-art"><img alt="Google Groups" src="https://cdn.jsdelivr.net/gh/wactax/img/g-groups.svg"/></a></p>

# xxAI.art

Веб-сайт кодының бір бөлігі ашық бастапқы коды болып табылады, аударманы оңтайландыруға көмектесуге қош келдіңіз.

## алдыңғы код

* [алдыңғы код](https://github.com/xxai-art/web)
* [Жалпы сайтқа арналған тіл пакеттері](https://github.com/xxai-art/web/tree/main/i18n)
* [Кіру модульдері үшін тіл бумалары](https://github.com/wacpkg/user/tree/main/ui.i18n)
* [Веб-сайттың көптілді құжаттамасы](https://github.com/xxai-doc)

Функционалды бағдарламалау тілі [@w5/coffee_plus](http://npmjs.com/@w5/coffee_plus) болып табылады, ол кофескрипт синтаксисіне негізделген кейбір мүмкіндіктерді қосады, [./coffee_plus.md](./coffee_plus.md) қараңыз.

## Веб-сайттар мен құжаттарды интернационалдандыру

Келесі 3 жобаны құрастырыңыз

* [@w5/mdt](https://www.npmjs.com/package/@w5/mdt)

  `.mdt` жұрнағы, сыртқы файлдарға сілтеме жасау үшін `<+ ./coffee_plus/import.js>` ұқсас синтаксисті пайдалануға және `.md` жұрнағы арқылы белгілерді жасауға болады.

* [@w5/trmd](https://www.npmjs.com/package/@w5/trmd)

  Markdown аудармасы кодтар мен сілтемелерді аудармайды және аударылған сөйлемдерді кэштейді. Аударма өзгертілсе, бірақ түпнұсқа мәтін өзгертілмесе, оны қайта орындау аударманың өзгертуін қайта жазбайды.

* [@w5/i18n](https://www.npmjs.com/package/@w5/i18n)

  `yaml` жасалған веб-сайттарды аударуға арналған тіл файлдары.
