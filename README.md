    

## Хэш коммита
---
    Хэш коммита - идентификатор коммита, полученный с помощью алгоритма SHA-1.  

    Хэш обладает свойством: если хоть что-то в исходных данных поменяется, хеш тоже изменится.  

    Git хранит таблицу соответствий хеш → информация о коммите в служебных файлах .git.  

    Лог - список коммитов с описанием, содержит хеш, автора, дату и сообщение к коммиту.  

    Сокращённый лог - список коммитов с описанием, содержит только первые несколько символов хеша и комментарии.  
---
## Файл HEAD
---
    Файл HEAD указывает на последний (самый новый) коммит.  

    При работе с Git указатель HEAD используется часто, вместо хеша последнего коммита можно просто написать слово HEAD.  
--- 

## Статусы файлов
---  

  *Git* использует статусы файлов для отслеживания изменений в репозитории.  
    
Статусы файлов включают:   

_untracked,  staged, modified, and tracked._  
    
* Untracked файлы - новые файлы, не отслеживаемые Git'ом.  
    
* Staged файлы - файлы, добавленные в staging area командой git add.  
    
* Modified файлы - файлы с изменениями, найденными Git'ом.  
    
* Tracked файлы - файлы, закоммиченные или добавленные в staging area.  
--- 
    
Жизненный цикл файла в Git: создание, добавление в staging area, коммит, изменение, повторное добавление в staging area, коммит.  

Команда git status показывает статусы файлов: _staged, modified, untracked_

---


```mermaid
graph LR;

 	A[untracked] -- "git add" --> B{staged};
	B -- "git commit" --> C{tracked};
	B -- "changes" --> D{modified};
	C -- "changes" --> D{modified};
	D -- "git add" --> B{staged};

%% описание схемы
```

---


























