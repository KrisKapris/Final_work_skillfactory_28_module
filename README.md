>## :briefcase: ИТОГОВЫЙ ПРОЕКТ ПО АВТОМАТИЗАЦИИ ТЕСТИРОВАНИЯ SKILLFACTORY QAP-1035 

### Необходимо протестировать новый интерфейс авторизации в личном кабинете от заказчика Ростелеком.

→ Объект тестирования: https://b2c.passport.rt.ru


→ [Требования по проекту (.doc)](https://docs.google.com/document/d/1o8Zpy0pgiscX11AlZL4NqvI7td2OQvsq/edit?usp=sharing&ouid=105971517531308400217&rtpof=true&sd=true)




**:bookmark_tabs: Заказчик передал вам следующее задание:**

1. Протестировать требования.
2. Разработать тест-кейсы (не менее 15). Необходимо применить несколько техник тест-дизайна.
3. Провести автоматизированное тестирование продукта (не менее 20 автотестов). Заказчик ожидает по одному автотесту на каждый написанный тест-кейс. Оформите свой набор автотестов в GitHub.
4. Оформить описание обнаруженных дефектов. Во время обучения вы работали с разными сервисами и шаблонами, используйте их для оформления тест-кейсов и обнаруженных дефектов. (если дефекты не будут обнаружены, то составить описание трех дефектов)

**:bookmark_tabs: Ожидаемый результат**

1. Перечислены инструменты, которые применялись для тестирования.

   * Почему именно этот инструмент и эту технику.
   * Что им проверялось.
   * Что именно в нем сделано.
   
2. К выполненному заданию прикреплены:

   * Набор тест-кейсов;
   * Набор автотестов на GitHub. Обратите внимание, что в репозитории должен находиться файл README.md, где будет описано, что именно проверяют данные тестовые сценарии и какие команды необходимо выполнить для запуска тестов. Описанные команды должны работать на любом компьютере с установленными Python3 и PyTest;
   * Описание оформленных дефектов.

***
**:bookmark_tabs: В корневом каталоге проекта содержаться:**
* [config.py](https://github.com/KrisKapris/Final_work_skillfactory_28_module/blob/e491cc7f5d33a97bea8d139b7e5ece7bad8fe39f/config.py) - содержит переменные используемые в проекте;
* [README.md](https://github.com/KrisKapris/Final_work_skillfactory_28_module/blob/446b806d8575e042768357003e53796a7591856f/README.md) - содержит информацию в целом о проекте;
* [requirements.txt](https://github.com/KrisKapris/Final_work_skillfactory_28_module/blob/446b806d8575e042768357003e53796a7591856f/requirements.txt) - содержит все библиотеки и зависимости проекта.
***
**:bookmark_tabs: Директория driver содержит:**
* [chromedriver.exe](https://github.com/KrisKapris/Final_work_skillfactory_28_module/tree/446b806d8575e042768357003e53796a7591856f/chromedriver_mac_arm64) - драйвер для управления браузером Chrome.
***
**:bookmark_tabs: Директория tests содержит:**
* [test_authorization_interface.py](https://github.com/KrisKapris/Final_work_skillfactory_28_module/blob/446b806d8575e042768357003e53796a7591856f/tests/test_authorization_interface.py) - файл автотестов;
* [conftest.py](https://github.com/KrisKapris/Final_work_skillfactory_28_module/blob/446b806d8575e042768357003e53796a7591856f/tests/conftest.py) - условия для выполнения тестовых задач.
***
**:bookmark_tabs: Директория pages содержит:**
* [locators.py](https://github.com/KrisKapris/Final_work_skillfactory_28_module/blob/446b806d8575e042768357003e53796a7591856f/pages/locators.py) - содержит описание локаторов проекта;
* [base_page.py](https://github.com/KrisKapris/Final_work_skillfactory_28_module/blob/446b806d8575e042768357003e53796a7591856f/pages/base_page.py) - содержит базовые функции и методы.
***


→ [Протестированные требования (.doc).](https://docs.google.com/document/d/1bXnoPMj2mCpIH-0sEYF6w0exoV_dC41i/edit?usp=sharing&ouid=105971517531308400217&rtpof=true&sd=true) Оформлены в виде комментариев (в комментариях указано как это выглядит на сайте).


→ [Тест-кейсы, дефекты (.excel)](https://docs.google.com/spreadsheets/d/18VQkpXNBNLvBAAgzLTzRvRd_rO1bYEgy8nKsURoegmU/edit?usp=sharing)

### При разработке тест-кейсов были применены следующие техники тест-дизайна: 
 
* эквивалентное разбиение
* анализ граничных значений
* [диаграмма перехода состояния (.jpeg)](https://drive.google.com/file/d/1dVfLti8FRcahbYu3xlJDFGCJK10AjtZF/view?usp=sharing)


### Инструменты, которые применялись для тестирования.

* Для тестирования сайта был использован 
интсрумент [Selenium](https://www.selenium.dev/);
* Для определения локаторов использовались 
следующие инструменты: DevTools, [ChroPath](https://chrome.google.com/webstore/detail/chropath/ljngjbnaijcbncmcnjfhigebomdlkcjo). 

### Запуск тестов:
* установить все библиотеки и зависимости: `pip install -r requirements.txt`;
* загрузите [Selenium WebDriver](https://chromedriver.chromium.org/downloads) (выберите версию, совместимую с вашим браузером) и прописать путь к драйверу в переменную PATH в файле config.py;
* запустить тест: `python -m pytest -v --driver Chrome --driver-path Final_work_QAP1031/chromedriver_mac_arm64/chromedriver tests/test_authorization_interface.py`.

