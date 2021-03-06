# Вопросы с se.ifmo.ru

## Цели и задачи интеграционного тестирования. Расположение фазы интеграционного тестирования в последовательности тестов; предшествующие и последующие виды тестирования ПО.

Интеграционные тесты проверяют корректность взаимодействия компонент системы.

### Расположение фазы интеграционного тестирования

```
 требования  <------------------бизнес требования, валидация ---------------------------------------> приемочное тестирование
 
    Анализ <--------------------Требования к ПО, Валидация, верификация -------------------> Системное тестирование
    
      Архитектурное <---------- Требования к интерфейсам ----------------------> Интеграционное тестирование
      проектирование            Верификация
      
            Детальное  <------------- Тестовый случаи -------------------> Модульноетестирование
            проектирование            Верификация
          
                                           
                                       Разработка
```

## Алгоритм интеграционного тестирования.

Рассказать, как делали лабу?

## Концепции и подходы, используемые при реализации интеграционного тестирования.

### Сверху вниз

Интеграционное тестирование __сверху вниз__ (как в лабе) - сначала тестируют только самый верхний управляющий уровень системы, без модулей более низкого уровня. Затем постепенно с более высокоуровневыми модулями интегрируются более низкоуровневые.

__Преимущества:__

- Легко обнаружить неисправности или ошибки в работе системы.
- В первую очередь проверяются важные модули, а лишь потом модули нижнего порядка.
- По сравнению с другими подходами, время на тестирование интеграции очень коротко.

__Недостатки:__

- Если в модули нижнего уровня заложена важная логика, она не может быть протестирована в первую очередь
- Использование «заглушек»становится обязательным на всех последующих проектах.

### Снизу вверх

Интеграционное тестирование __снизу вверх__ (если бы мы сначала в лабе протестировали синус и ln, потом sin, cos, lnб потом все тригонометрические и логарифмические функции и т.д) - подход подразумевает проверку низкоуровневых систем для начала: вместе и по отдельности. Другими словами процесс тестирования начинается с внутреннего уровня и постепенно доходит до наиболее критичных позиций.

__Преимущества:__

- Если определенный модуль перестает функционировать, его ошибка может быть сразу же исправлена.
- Требуется минимальное время на идентификацию и устранение ошибок.

__Недостатки:__

- Общее время проверки всех модулей довольно долгое
- Если ПО содержит много небольших модулей мелкого уровня, которые очень сложны в своей имплементации, то для завершения процесса тестирования может потребоваться больше времени.

### Большой взрыв

Тестирование методом __большого взрыва__ -  созданные и запрограммированные модули и системные компоненты соединены между собой. При объединении эти модули тестируются как единое целое. После проведения юнит-тестов, модули также проверяются вместе, еще до образования целостной программной системы.

__Преимущества:__

- Удобен  при тестировании небольших систем.
- Быстрое нахождение ошибок

__Недостатки:__

- Так как модули завязаны на одной системе, порой очень трудно найти источник дефектов.
- Если в системе используется много модулей, может уйти достаточно времени, чтобы пересмотреть все реализованные функциональности.

## Программные продукты, используемые для реализации интеграционного тестирования. Использование JUnit для интеграционных тестов.

Mockito - фреймворк с поддержкой макетирования для unit-тестов.

Greenmail — для тестироания электронной почты, который поддерживает SMTP, POP3 и IMAP с поддержкой SSL-соединения. 

MockFtpServer — библиотека, которая предоставляет две разные реализации FTP-сервера («заглушка» и «обманка»), которые можно использовать для тестирования различных сценариев.

## Автоматизация интеграционных тестов. ПО, используемое для автоматизации интеграционного тестирования.

Selenium - это инструмент для автоматизации действий веб-браузера. В большинстве случаев используется для тестирования Web-приложений

