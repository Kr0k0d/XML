# GIT Homework 1

### 1. Создать внешний репозиторий c названием XML.
  Для этого заходим в аккаунт Guthub, нажимаем на "_Repositories_" после на "_New_", называем и создаем.

---

### 2.  Клонировать репозиторий XML на локальный компьютер.
  Для клонирования репозитория нужно создать папку, после с помощью скопированого URL
```
    git clone https://github.com/Kr0k0d/XML.git
```
_Вывод_
```
    Cloning into 'XML'...
    remote: Enumerating objects: 3, done.
    remote: Counting objects: 100% (3/3), done.
    remote: Total 3 (delta 0), reused 0 (delta 0),pack-reused 0
    Receiving objects: 100% (3/3), done.

```

---
### 3. Внутри локального XML создать файл “new.xml”.
```
  touch new.xml
```

---

### 4. Добавить файл под гит.
  Подготавливаем файл: 
  ```
  git add .
  ```
  Проверяем состояние изменений:
  ```
  git status
  ```
  _Вывод_
  ```
   On branch main
   Your branch is up to date with 'origin/main'.
   Changes to be committed:
   (use "git restore --staged <file>..." to unstage)
   new file:   new.xml
   ```

---

### 5. Закоммитить файл. 
  Коммит нужен для фиксации изменений:
  ```
  git commit -m "Create new file"
  ```
  
  _Вывод_
  ```
  [main c5abba9] Create new file
  1 file changed, 0 insertions(+), 0 deletions(-)
  create mode 100644 new.xml

  ```

---

### 6. Отправить файл на внешний GitHub репозиторий.
  Отправляем коммит и принимает ответ:
  ```
  git push
  ```
  
  _Вывод_
  ```
  Enumerating objects: 4, done.
  Counting objects: 100% (4/4), done.
  Delta compression using up to 4 threads
  Compressing objects: 100% (2/2), done.
  Writing objects: 100% (3/3), 275 bytes | 275.00 KiB/s, done.
  Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
  To https://github.com/Kr0k0d/XML.git
   99eb32e..c5abba9  main -> main

  ```

---

### 7. Отредактировать содержание файла “new.xml" - написать информацию о себе (ФИО, возраст, количество домашних животных, будущая желаемая зарплата). Всё написать в формате XML.
```
nano new.xml
```
  ```
  <information>
	<FullName>Novikov Daniil Dmitrievich</FullName>
	<Age>19</Age>
	<Pet>1</Pet>
	<Salary>30000</Salary>
</Information>
  ```

---

### 8. Отправить изменения на внешний репозиторий.
Для отправки изменений выполняем теже действия, что и в пунктах 4-6
```
git add .
```
```
git commit -m "File changed"
```
_Вывод_
```
[main ca2537e] File changed
1 file changed, 6 insertions(+)
```
```         
git push
```
_Вывод_
```
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 375 bytes | 375.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/Kr0k0d/XML.git
   c5abba9..ca2537e  main -> main

```

---

### 9. Создать файл preferences.xml
```
touch preferences.xml
```
  
---

### 10.В файл preferences.xml добавить информацию о своих предпочтениях (Любимый фильм, любимый сериал, любимая еда, любимое время года, сторона которую хотели бы посетить) в формате XML.

  ```
  nano preferences.xml
  ```
  Открывется менюшка где мы вводим данные
  ```
  <information>
	<Favorite_movie>1 + 1</Favorite_movie>
	<Favotite_series>Lucifer</Favorite_seies>
	<Favorite_food>Beef steak</Favorite_food>
	<Season>Summer</Season>
	<Country>Italy</Country>
</information>
   ```
   Полсе нажимаем Ctrl+X после Y и enter.
   
---

### 11.  Создать файл sklls.xml добавить информацию о скиллах которые будут изучены на курсе в формате XML
  Все тоже самое, что и в пункте 10 
  ```
  touch sklls.xml

  nano sklls.xml
  ```
  ```
  <information>
	<Skills>
        Tesring Basics, Manual testing, Automated testing, Security testing, 
        Basics of programming, Database basics, Modern testing methods, 
        Communication and interpersonal skills,Project manegement,Tools skills(Postman)
     </Skills>
</information>
  ```
  
---

### 12. Отправить сразу 2 файла на внешний репозиторий.
  ```
  git add . 
  
  git commit -m "Added information" preferences.xml sklls.xml
  ```
  _Вывод_ 
  ```
  [main a6bb78e] Added information
 2 files changed, 10 insertions(+)
 create mode 100644 preferences.xml
 create mode 100644 sklls.xml
  ```
  ```
  git push
  ```
  _Вывод_ 
  ```
  Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 639 bytes | 319.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/Kr0k0d/XML.git
   ca2537e..a6bb78e  main -> main
  ```
---
  
### 14. На веб интерфейсе создать файл bug_report.xml.
Для этого нужно открыть GitHub, перейти в репозиторий,  нажать на кнопку "Add file" и выбрать "Create new file".
```
<bugs>
  <id>404</id>
  <Name>Ошибка при загрузке страницы</Name>
  <Description>При попытке загрузить страницу, браузер выдает ошибку "404 Not Found". Это происходит на всех страницах сайта, не только на одно</Description>
  <Environment>Windows 10 Chrome</Environment>
  <Reproduction>Открыть любую страницу на сайте и попытаться ее загрузить</Reproduction>
  <Expected_result>Страница должна загрузиться без ошибок</Expected_result>
  <Current_result> Браузер выдал ошибку "404 Not Found"</Current_result>
</bugs>
```
---

### 15. Сделать Commit changes (сохранить) изменения на веб интерфейсе.
Нажимаем на кнопку "Commit changes".

---

### 16.На веб интерфейсе модифицировать файл bug_report.xml, добавить баг репорт в формате XML.
Через GitHub внести изменение в файл bug_report.xml
```
  <Priority>Hight</Priority>
```
---

### 17. Сделать Commit changes (сохранить) изменения на веб интерфейсе.

Как и в пункте 14 коммитим изменения

---

### 18. Синхронизировать внешний и локальный репозиторий XML

Сохранить изменение на компьютере, помодет команда 

```
git pull
```
_Вывод_
```
remote: Enumerating objects: 11, done.
remote: Counting objects: 100% (11/11), done.
remote: Compressing objects: 100% (9/9), done.
remote: Total 9 (delta 3), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (9/9), 4.32 KiB | 73.00 KiB/s, done.
From https://github.com/Kr0k0d/XML
   a6bb78e..20ee9e0  main       -> origin/main
Updating a6bb78e..20ee9e0
Fast-forward
 README.md      | 207 ++++++++++++++++++++++++++++++++++++++++++++++++++++++++-
 bug_report.xml |  10 +++
 2 files changed, 216 insertions(+), 1 deletion(-)
 create mode 100644 bug_report.xml
```
