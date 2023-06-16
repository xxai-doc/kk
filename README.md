<p align="center"><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/logo.svg"/></a><br/><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/xxai.svg"/></a></p><p align="center"><a href="https://github.com/xxai-art/doc#readme"><img alt="I18N" src="https://cdn.jsdelivr.net/gh/wactax/img/t.svg"/></a>　<a href="https://groups.google.com/u/0/g/xxai-art"><img alt="Google Groups" src="https://cdn.jsdelivr.net/gh/wactax/img/g-groups.svg"/></a></p>

Каталогқа кіргеннен кейін алдымен nodejs, [direnv](https://direnv.net) , [bun](https://github.com/oven-sh/bun) , содан кейін `direnv allow` орнату ұсынылады ( [.envrc](https://github.com/xxai-art/doc/blob/main/.envrc) каталогқа кіргеннен кейін автоматты түрде орындалады).

Мағынасы: жапон, корей, ағылшын тілдеріне қытайша аудармасы, барлық басқа тілдерге ағылшынша аудармасы. Егер сіз тек қытай және ағылшын тілін қолдағыңыз келсе, жай ғана `zh: en` деп жаза аласыз.

Мағынасы: жапон, корей, ағылшын тілдеріне қытайша аудармасы, барлық басқа тілдерге ағылшынша аудармасы. Егер сіз тек қытай және ағылшын тілін қолдағыңыз келсе, `zh: en` жаза аласыз.

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

### Құжаттарды аударуды автоматтандыру нұсқаулары

[xxai-art/doc](https://github.com/xxai-art/doc) код репозиторийін қараңыз

Каталогқа кіргеннен кейін алдымен nodejs, [direnv](https://direnv.net) , [bun](https://github.com/oven-sh/bun) , содан кейін `direnv allow` орнату ұсынылады ( [.envrc](https://github.com/xxai-art/doc/blob/main/.envrc) каталогқа кіргеннен кейін автоматты түрде орындалады).

Жүздеген тілдерге аударылған үлкен кодтық базаны болдырмау үшін мен әр тіл үшін жеке код базасын жасадым және код базасын сақтайтын ұйымды жасадым.

`GITHUB_ACCESS_TOKEN` ортасының айнымалы мәнін орнату және одан кейін [create.github.coffee](https://github.com/xxai-art/doc/blob/main/create.github.coffee) іске қосу код репозиторийін автоматты түрде жасайды.

Әрине, оны кодтық базаға қоюға да болады.

Аударма сценарийіне сілтеме [run.sh](https://github.com/xxai-art/doc/blob/main/run.sh)

Сценарий коды келесідей түсіндіріледі:

[bunx](https://bun.sh/docs/cli/bunx) - npx орнына жылдамырақ. Әрине, егер сізде bun орнатылмаған болса, оның орнына `npx` пайдалануға болады.

`bunx mdt zh` `.mdt` zh каталогында `.md` ретінде көрсетеді, төмендегі 2 байланыстырылған файлды қараңыз

* [coffee_plus.mdt](https://github.com/xxai-doc/zh/blob/main/coffee_plus.mdt)
* [coffee_plus.md](https://github.com/xxai-doc/zh/blob/main/coffee_plus.md)

`bunx i18n` аударманың негізгі коды болып табылады (егер сізде тек `nodejs` орнатылған болса, бірақ `bun` және `direnv` орнатылмаған болса, аудару үшін `npx i18n` бағдарламасын да іске қосуға болады).

Ол [i18n.yml](https://github.com/xxai-art/doc/blob/main/i18n.yml) талдайды, бұл құжаттағы `i18n.yml` конфигурациясы келесідей:

```
en:
zh: ja ko en
```

Мағынасы: жапон, корей, ағылшын тілдеріне қытайша аудармасы, барлық басқа тілдерге ағылшынша аудармасы. Егер сіз тек қытай және ағылшын тілін қолдағыңыз келсе, жай ғана `zh: en` деп жаза аласыз.

Соңғысы [gen.README.coffee](https://github.com/xxai-art/doc/blob/main/gen.README.coffee) болып табылады, ол `README.md` жазбасын жасау үшін әрбір тілдің `README.md` негізгі тақырыбы мен бірінші субтитр арасындағы мазмұнды шығарады. Код өте қарапайым, оны өзіңіз қарай аласыз.

Google API тегін аудару үшін пайдаланылады. Google жүйесіне кіре алмасаңыз, проксиді конфигурациялаңыз және орнатыңыз, мысалы:

```
export https_proxy=http://127.0.0.1:7890 http_proxy=http://127.0.0.1:7890 all_proxy=socks5://127.0.0.1:7890
```

Аударма сценарийі `.i18n` каталогында аударылған кэшті жасайды, қайталанатын аудармаларды болдырмау үшін оны `git status` тексеріп, код репозиторийіне қосыңыз.

Кэшті жаңарту үшін аударманы өзгерткен сайын `bunx i18n` іске қосыңыз.

Түпнұсқа мәтін мен аударма бір уақытта өзгертілсе, кэш шатастырылады, сондықтан өзгерткіңіз келсе, тек біреуін ғана өзгерте аласыз, содан кейін кэшті жаңарту үшін `bunx i18n` іске қосыңыз.
