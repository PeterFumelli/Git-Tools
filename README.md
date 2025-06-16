# Домашнее задание к занятию "Инструменты Git" - Петр Фумелли

### Задание 1

1) Найдите полный хеш и комментарий коммита, хеш которого начинается на aefea.

```
  git log --oneline | grep aefea

  aefead2207 Update CHANGELOG.md
```
2) Какому тегу соответствует коммит 85024d3?

```
  git tag --contains 85024d3

  v0.12.23
  v0.12.24
  v0.12.25
  v0.12.26
  v0.12.27
  v0.12.28
  v0.12.29
  v0.12.30
  v0.12.31
```

3)Сколько родителей у коммита b8d720? Напишите их хеши.

```
  git show --pretty=%P b8d720

  56cd7859e05c36c06b56d013b55a252d0bb7e158 9ea88f22fc6269854151c571162c5bcf958bee2b
```

4)Перечислите хеши и комментарии всех коммитов между тегами v0.12.23 и v0.12.24.

```
  git log --oneline v0.12.23..v0.12.24

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
```

5)Найдите коммит, в котором была создана функция func providerSource(...).

```
  git log -S'func providerSource' --oneline

5af1e6234a main: Honor explicit provider_installation CLI config when present
8c928e8358 main: Consult local directories as potential mirrors of providers
```

6) Найдите все коммиты, в которых была изменена функция globalPluginDirs.

```
  git
```

7)Кто автор функции synchronizedWriters?

```
  git log -S'synchronizedWriters' --pretty=format:"%h %an %s"

 bdfea50cc8 James Bardin remove unused
 fd4f7eb0b9 James Bardin remove prefixed io
 5ac311e2a9 Martin Atkins main: synchronize writes to VT100-faker on Windows
```
