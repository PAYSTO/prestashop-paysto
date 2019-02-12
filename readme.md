**Инструкция по настройке модуля оплаты Paysto на сайт работающий под управлением Prestashop CMS**

1. Установка модуля:
Перейдите на вкладку “Модули” в админ панели. Сверху будет кнопка “Загрузить модуль”, нажмите ее. После загрузки модуля установите его (начиная с версии Prestashop 1.7.x.x модуль устанавливается автоматически).

ВАЖНО ПРИ УСТАНОВКЕ: 
Необходимо чтобы архив для установке назывался как paysto.zip а файлы установки и папки:
classes
controllers
translations
views
config.xml
config_fr.xml
config_ru.xml
index.php
logo.gif
paysto.php
Рапологались в корневой директории архива.

2. Настройка модуля:
Перед тем, как начать пользоваться модулем, его нужно настроить. Для этого вы должны быть подключены к платежной системе Paysto. Там вам нужно будет добавить свой сайт, после чего будет доступен код магазина (Merchant id), и возможность создать свой секретный ключ. Эти параметры вам также нужно будет прописать в настройках модуля. 
3. Для лучшей безопасности вам нужно будет установить разрешения для осуществления обратных вызовов только от определенных IP адресов серверов Paysto:
 95.213.209.218,
 95.213.209.219,
 95.213.209.220,
 95.213.209.221,
 95.213.209.222
4. Дополнительные настройки:
Перед оплатой заказа в Paysto передаются данные для Онлайн-Кассы: налог на товар, название, цена, количество.
Налог на товар настраивается для каждого товара отдельно. Для этого используется стандартный функционал Prestashop, который находится в форме редактирования товара, на вкладке “цены”. Значение “Не начислять” равно 0% налога. Чтобы эта опция работала, налог в магазине должен быть включен. Если налог отключен, то в данных для онлайн-кассы налог будет указан, как “нет налога”.
5. Кроме того вам необходиом будет указать ставку НДС для доставки. Есть или нет. 