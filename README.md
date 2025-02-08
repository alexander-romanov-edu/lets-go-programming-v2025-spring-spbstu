# RULES

## Общие правила

Каждая практическая работа студента проходит ручную проверку:
- [В рамках практических занятий](#проверка-практических-работ-в-рамках-практических-занятий);
- [Code Review Pull Request'а вне практических занятий](#дополнительная-проверка-практических-работ-в-рамках-code-review-pr).

Работа считается принятой в случае успешного прохождения ручной проверки 
и добавления решения в root-репозиторий на ветке `master`.

> Срок сдачи каждой практической работы - не более **3 недель** с момента выдачи 
> 
> Рекомендованный срок сдачи - 2 недели с момента выдачи, 
> последнюю неделю предлагается использовать для исправления ошибок в решении.

## Правила оформления практических работ

1. Название основной директории, в которой студент размещает все свои практические работы,
должно состоять из имени и фамилии студента на английском языке, должно быть написано строчными буквами.
Имя и фамилия должны быть разделены точкой.

```none
– ivan.ivanov/
– anton.petrov/
```

2. Каждая практическая работа размещается в основной директории с указанием номера этой работы. 
Название практической работы – `task-<task-number>`.  В случае, если практическая работа включает в себя 
несколько подзаданий, то для каждого подзадания создается отдельная директория.
Название директория для подзадания – `task-<task-number>-<subtask-number>`.

```none
–  ivan.ivanov/task-1/
–  ivan.ivanov/task-2-1/
–  ivan.ivanov/task-2-2/
```

3. Решение каждой практической работы должно содержать в себе `go.mod` файл с описанием модуля (`go mod init`).

4. Точка входа в программу (файл `main.go` с функцией `main`) должна быть расположена по пути `cmd/service/`.
Если практическая работа требует реализации нескольких сервисов - каждая 
точка входа размещается в своей поддиректории `cmd/`.

```none
–   ivan.ivanov/task-1/cmd/service/main.go
–   ivan.ivanov/task-2/cmd/connector/main.go
–   ivan.ivanov/task-2/cmd/backend/main.go
```

>  Примечание: в качестве имени модуля *рекомендуется* использовать `github.com/<your-user-name>/task-<task-number>`.

## Требования к публикации практических работ

1. Практические работы публикуются в root-репозитории посредством  создания Pull Request (далее – PR)
из fork-репозитория студента на ветку `master` root-репозитория.

> Примечание: за актуальность кода в `HEAD` `master` ветки своего fork-репозитория отвечает студент.
> Публикуемые работы должен содержать актуальные изменения из root-репозитория на момент отправки работы на проверку.

2. Если в практической работе одно задание –  на всю практическую работу должен быть создан только один PR.
В случае нескольких подзадач в одной практической работе – каждое подзадание публикуется в виде отдельного PR.

3. Название каждого PR должно содержать номер задания.
В случае, если практическая работа включает в себя несколько подзаданий, 
то название PR должно содержать номер задания и номер подзадания.

```none
–  TASK-1
–  TASK-2-1
–  TASK-2-2
```

4. Каждый коммит в PR должен содержать законченные изменения. В названии каждого коммита должен быть номер работы 
в квадратных скобках и краткое описание внесенных изменений на английском языке.

```none
–  [TASK-1] Initial commit
–  [TASK-1] Add unit tests
```

5. Коммиты в PR не должны вносить изменения в файлы и директории, относящиеся к директориям
с решениям других студентов, а также в common-файлы root-репозитория.

## Ручная проверка практических работ

### Общие правила ручной проверки

1. Оценивание практической работы является субъективным и может быть оспорено в рамках Code Review или на практическом
занятии в виде дискуссии между студентом и преподавателем,
Не позднее срока, выделенного на сдачу практической работы (см. [Общие правила](#общие-правила)).

2. Шаг ручной проверки может быть пропущен по решению преподавателей курса.

### Проверка практических работ в рамках практических занятий

1. В рамках практических занятий студент демонстрирует решение преподавателям курса на своей машине.

2. В ходе демонстрации решения студент дает пояснительные комментарии, а также отвечает на вопросы преподавателей.

3. Все недочеты и комментарии к работе оформляются преподавателями в качестве комментариев к PR с 
работой студента во время или после демонстрации работы.

4. В случае некорректного решения практической работы или наличия недочетов, PR получает статус `Closed` в 
системе GitHub до устранения ошибок и его переоткрытия студентом.

5. В случае корректного решения практической работы, PR получает статус `Merged` в системе GitHub, 
а исходных код решения добавляется в `master` ветку root-репозитория.


### Дополнительная проверка практических работ в рамках Code Review PR

1. В случае если работа студента содержит незначительные недочеты, то после их исправлений 
преподаватели курса могут произвести дополнительную проверку работы вне практических занятий.

2. В случае некорректных исправлений в практической работе, PR получает статус `Closed` в 
системе GitHub до устранения ошибок и его переоткрытия студентом.

3. В случае корректного решения практической работы, PR получает статус `Merged` в системе GitHub, 
а исходных код решения добавляется в `master` ветку root-репозитория.

**Enjoy the course and May the odds be ever in your favor!**

