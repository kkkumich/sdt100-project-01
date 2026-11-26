# Project 1. Development environment

Canvas: https://auk.instructure.com/courses/1274/assignments/33042

## Состав

- `part1_hello.Main`

## Запуск

Требуется JDK 21. В IntelliJ: открыть проект, выбрать JDK, отметить src как Sources Root. Каждая часть запускается своим main. Рабочая папка — корень этого проекта.

Из PowerShell:

```powershell
$sourceFiles = @(Get-ChildItem src -Recurse -Filter *.java | ForEach-Object FullName)
javac -encoding UTF-8 -d build @sourceFiles
java -cp build part1_hello.Main
```

## Что показать на защите

Запусти part1_hello.Main. Покажи исходник, вывод трёх строк, выбранный JDK, структуру src/part1_hello и историю коммитов.

## Как объяснить

Программа начинается с public static void main(String[] args). println выводит строку и переводит курсор на новую строку. JDK содержит компилятор javac; java запускает скомпилированный байт-код в JVM. Git хранит локальную историю, GitHub — удалённый репозиторий.

## Возможные вопросы

- **Чем commit отличается от push?** Commit фиксирует изменения локально, push отправляет коммиты в удалённый репозиторий.
- **Что делает clone?** Создаёт локальную копию репозитория вместе с историей.
- **Зачем package?** Создаёт пространство имён и группирует связанные классы.

## Замечания

В IntelliJ открой папку проекта, выбери JDK 21, пометь src как Sources Root, запусти main и сделай настоящий скриншот IDE. Отдельное Git/GitHub Classroom-приглашение из условия сейчас ведёт на сообщение о закрытии Classroom; старую инструкцию нужно согласовать с преподавателем.

Файл RUNS.txt содержит настоящие результаты локального запуска с демонстрационным вводом. Это журналы, а не скриншоты IntelliJ. Проверка выполнена 26 ноября 2026. Ошибочные учебные примеры находятся отдельно от src.
