# Домашнее задание к занятию «Инструменты Git» - Петр Петров
### Ответы на задание
1. Найдите полный хеш и комментарий коммита, хеш которого начинается на aefea:  
`git show aefea`  
Полный хеш: aefead2207ef7e2aa5dc81a34aedf0cad4c32545  
Комментарий: Update CHANGELOG.md  

2. Ответьте на вопросы.

* Какому тегу соответствует коммит 85024d3?  
`git tag --contains 85024d3`  
Коммит 85024d3 соответствует тегам:  
v0.12.23  
v0.12.24  
v0.12.25  
v0.12.26  
v0.12.27  
v0.12.28  
v0.12.29  
v0.12.30  
v0.12.31  

* Сколько родителей у коммита b8d720? Напишите их хеши.  
`git show --pretty=raw b8d720`
Коммит имеет 2 родителя  

* Перечислите хеши и комментарии всех коммитов, которые были сделаны между тегами v0.12.23 и v0.12.24  
`git log v0.12.23..v0.12.24 --oneline`  

33ff1c03bb (tag: v0.12.24) v0.12.24  
b14b74c493 [Website] vmc provider links  
3f235065b9 Update CHANGELOG.md  
6ae64e247b registry: Fix panic when server is unreachable  
5c619ca1ba website: Remove links to the getting started guide's old location  
06275647e2 Update CHANGELOG.md  
d5f9411f51 command: Fix bug when using terraform login on Windows  
4b6d06cc5d Update CHANGELOG.md  
dd01a35078 Update CHANGELOG.md  
225466bc3e Cleanup after v0.12.23 release  

* Найдите коммит, в котором была создана функция func providerSource, её определение в коде выглядит так: func providerSource(...) (вместо троеточия перечислены аргументы).
`git log -S "func providerSource"`  

Коммит создания функции func providerSource - 8c928e8358  

* Найдите все коммиты, в которых была изменена функция globalPluginDirs  

`git log -S "globalPluginDirs"`

7c4aeac5f30aed09c5ef3198141b033eea9912be — stacks: load credentials from config file on startup

65c4ba736375607b6af6c035972f7f151232b6c6 — Remove terraform binary

125eb51dc40b049b38bf2ed11c32c6f594c8ef96 — Remove accidentally-committed binary

22c121df8631c4499d070329c9aa7f5b291494e1 — Bump compatibility version to 1.3.0 for terraform core release

7c7e5d8f0a6a50812e6e4db3016ebfd36fa5eaef — Don't show data while input if sensitive

35a058fb3ddfae9cfee0b3893822c9a95b920f4c — main: configure credentials from the CLI config file

c0b17610965450a89598da491ce9b6b5cbd6393f — prevent log output during init

8364383c359a6b738a436d1b7745ccdce178df47 — Push plugin discovery down into command package

* Кто автор функции synchronizedWriters  
`git log -S synchronizedWriters`   
commit 5ac311e2a91e381e2f52234668b49ba670aa0fe5  
Author: Martin Atkins <mart@degeneration.co.uk>  
Date:   Wed May 3 16:25:41 2017 -0700  

`git show 5ac311e2a91e381e2f52234668b49ba670aa0fe5`  
commit 5ac311e2a91e381e2f52234668b49ba670aa0fe5
Author: Martin Atkins <mart@degeneration.co.uk>
Date:   Wed May 3 16:25:41 2017 -0700

diff --git a/synchronized_writers.go b/synchronized_writers.go  
new file mode 100644  
index 0000000000..2533d1316c  
--- /dev/null  
Файла synchronized_writers.go до этого коммита не существовало, значит автор - Martin Atkins  
