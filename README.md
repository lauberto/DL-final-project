# DL-final-project
#### Андреа Грилланди
## Итоговый проект для курса "Глубокое Обучение" - Компьютерная лингвистика, ВШЭ НИУ 

### Описание задача
Задача этого проекта заключается в суммаризации новостных статьей. Задача входит в рамках конференции "Диалог" (2019г).
(https://vk.com/@headline_gen-announcement)
Данные взяты от "РИА Новости" и они задаются в формате:  
```
[{'text': 'document body',
  'title': 'title text'}]
```
В этом проекте был использован весь датасет, который содержит 1003869 статьей на русском языке.
Цель этого проекта - создавать модель, позволяющую сгенерировать заголовок при заданном новостном тексте.
Для того, чтобы оценить прогресс обучения использовалась метрика BLEU.

### Обзор задачи
В этом проект была устроена LSTM модель с механизмом аттеншна. Такое решение не впервые используется для решения этой задачи. Например, уже в 2015г. в проекте (https://nlp.stanford.edu/courses/cs224n/2015/reports/1.pdf) предлагается решение с помощью LSTM сети и аттеншна.  
В этом проекте механизм аттеншна был применен, задавая эмбеддинги энкодера и декодера трем "головам" - query key и value.
После обучения задаются два пробных текстов на генерации.

### Комментарий
Проект был проделан одним человеком (мною). В рамках проекта, я применял теоритеческие знания о языковом моделировании. Сначала я попробовал создавать модель без аттеншна, потому что было сложно понять как практически его применить. В итоге, получилось и я научился что значит устроить модель на практике. Особенно было полезно, чтобы лучше разобраться с использованием PyTorch. В конце получились хорошие метрики. Модель нормально обучалась, лосс подался, BLEU росла. Все-таки, может быть что она переобучалась на использованных данных, потому что генерация рандомного текста выдает странные результаты.


