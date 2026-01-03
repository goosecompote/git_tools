# Домашнее задание к занятию «Инструменты Git» Павлов Дмитрий    

## Инструкция к заданию  

    Склонируйте репозиторий с исходным кодом Terraform.    
    Создайте файл для ответов на задания в своём репозитории, после выполнения прикрепите ссылку на .md-файл с ответами в личном кабинете.  
    Любые вопросы по решению задач задавайте в разделе "Вопросы по заданию".  

## Задание  

В клонированном репозитории:  

## 1. Найдите полный хеш и комментарий коммита, хеш которого начинается на aefea.  
## Решение:   
Выполним комманду в склоненном репозитарии: git show aefea  
Вывод:  
commit aefead2207ef7e2aa5dc81a34aedf0cad4c32545  
Author: Alisdair McDiarmid <alisdair@users.noreply.github.com>  
Date:   Thu Jun 18 10:29:58 2020 -0400  

    Update CHANGELOG.md  

    
## 2. Ответьте на вопросы.  
## Какому тегу соответствует коммит 85024d3?  
## Решение:  
Выполним комманду в склоненном репозитарии: git show 85024d3  
Вывод:  

commit 85024d3100126de36331c6982bfaac02cdab9e76 (tag: v0.12.23)
Author: tf-release-bot <terraform@hashicorp.com>
Date:   Thu Mar 5 20:56:10 2020 +0000

    v0.12.23

В выводе видим что принадлежит к тегу: tag: v0.12.23  

## Сколько родителей у коммита b8d720? Напишите их хеши.  
## Решение: 
Выполним комманду в склоненном репозитарии: git show -s --format="%P" b8d720
Получим хеши родителей: 56cd7859e05c36c06b56d013b55a252d0bb7e158 9ea88f22fc6269854151c571162c5bcf958bee2b

## Перечислите хеши и комментарии всех коммитов, которые были сделаны между тегами v0.12.23 и v0.12.24.  
## Решение: 
Выполним комманду в склоненном репозитарии: git log --oneline v0.12.23..v0.12.24  
Вывод:  
3ff1c03bb (tag: v0.12.24) v0.12.24  
b14b74c493 [Website] vmc provider links  
3f235065b9 Update CHANGELOG.md  
6ae64e247b registry: Fix panic when server is unreachable  
5c619ca1ba website: Remove links to the getting started guide's old location  
06275647e2 Update CHANGELOG.md  
d5f9411f51 command: Fix bug when using terraform login on Windows  
4b6d06cc5d Update CHANGELOG.md  
dd01a35078 Update CHANGELOG.md  
225466bc3e Cleanup after v0.12.23 release  

## Найдите коммит, в котором была создана функция func providerSource, её определение в коде выглядит так: func providerSource(...) (вместо троеточия перечислены аргументы).  
## Решение:   
Выполним комманду в склоненном репозитарии: git log -S"func providerSource(" --oneline
Вывод: 8c928e8358 main: Consult local directories as potential mirrors of providers

## Найдите все коммиты, в которых была изменена функция globalPluginDirs.  
## Решение:   
Выполним комманду в склоненном репозитарии: git log -G '^func globalPluginDirs' --oneline
Вывод: 
7c4aeac5f3 stacks: load credentials from config file on startup (#35952)  
8364383c35 Push plugin discovery down into command package  
## Кто автор функции synchronizedWriters?  
## Решение:   
Выполним комманду в склоненном репозитарии: git log -S"func synchronizedWriters("
Вывод: Martin Atkins mart@degeneration.co.uk

