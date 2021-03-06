# Первая встреча сообщества

```
Дата:   20.04
Время:  19:00
Тема:   Основы ФП, Unidirectional Data Flow
Место:  Чайная "Мойчай", ул. Серафимовича 74
```

## Основы ФП

Обговорили, какой минимальный набор свойств необходимо иметь стилю, чтобы называться функциональным. Остановились на трех свойствах:

1. Иммутабельность
2. Функции высшего порядка
3. Поддержка рекурсии

_Прим. автора: если вы все еще сомневаетесь, что вам стоит изучить ФП или хотите какую-нибудь ссылочку, которой можно кидаться в своих коллег в жарких спорах, взгляните на это видео [Ted Neward - Why Functional Programming Matters](https://youtu.be/7hOM5PPzMC8)_

## UDF

Unidirectional Data Flow - очень популярный подход к написанию фронтенда, и одному из собравшихся, android-разработчику, очень захотелось порасспрашивать коллег из веба про этот подход.

В целом, подход заключается в том, чтобы превратить взаимодействие пользователя с UI в поток данных. То есть реальных структур данных, описывающих интеракции пользователя, затем обрабатываемых моделью, которая в свою очередь отдает структуру данных, которую UI визуализирует.

Разбирали различия между React-redux и elm, о том, где и как выполнять сайд-эффекты.

Подход    | Особенности
-------- | -----------------------------------
React-redux | Нет стандартного подхода в вопросе выполнения сайд-эффектов. Лечится добавлением redux-saga или аналогов
Elm | Из коробки заставляет описывать эффекты декларативно, выполняя их только за пределами пользовательского elm код

## FRP: Hoplon

В конце встречи разгорелся спор о том, что на самом деле, UDF накладывает большие ограничения и дополнительные расходы за счет наличия virtual-DOM и потребности в алгоритмах для реконсиляции.

Один из участников вспомнил про [Hoplon](https://github.com/hoplon/hoplon) - FRP фреймворк для ClojureScript, который позволяет также декларативно описывать UI без необходимости строить диффы деревьев. Однако полностью раскрыть тему не хватило времени и было решено перенести обсуждение FRP на следующую встречу

_Прим. автора: про алгоритмы реконсиляции есть интересный [выпуск](https://hardcode.fm/2019/03/26/episode010.html) подкаста HardcodeFM с Андреем Зайцевым из JetBrains, работающим над проектом абстрактного алгоритма реконсиляции [Noria](https://github.com/JetBrains/noria-clj)_
