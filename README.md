Установит запрет v70  
Включит скрипт для дискорда, установит рабочие на данный момент стратегии.  
Всё что нужно - это ввести команду ниже и нажать Enter. Затем повторить нажатие Enter на любые запросы.  
Метод подключения к серверу выбираете самостоятельно.  
Проверено на rocketcloud.ru ubuntu 22/24v, debian 12.  
  
Установка и развёртвывание zapret antiDPI под ключ на российских VPS (проверено на rocketcloud.ru) копируем и вставляем в ssh:  
```
bash <(curl -Ls https://raw.githubusercontent.com/IndeecFOX/zapret4rocket/refs/heads/master/fast_install.sh)
```  
На все вопросы жмём Enter (В самом начале скрипт спрашивает установить ли 3x-ui панель или аналоги (жмите Enter, если ничего не нужно или введите соответствущий текст)).   
По окончании всех прожатий enter всё будет работать.   
К серверу подключаетесь как хотите уже, WG/VLESS/OpenVPN YouTube летает, есть доступы к ntc.party, meduza.io и прочему.  
Дискорд (Discord) работает (при подключении через TUN для VLESS или протоколы с поддержкой UDP, иначе войса не будет)  
  
Чат: https://t.me/zee4r/

Тестовый сервер
```
vless://test@45.156.21.250:443?type=tcp&security=reality&pbk=T_PUQPpUcIDBj3bD5CwngfOS5LxzS6RGD-Lk5hITQhI&fp=chrome&sni=rutube.ru&sid=51&spx=%2F&flow=xtls-rprx-vision#Z4R-test
```
Fork Upd 07.02.25: добавлен простенький скрипт для установки на OpenWRT
```
opkg install bash curl && bash <(curl -Ls https://raw.githubusercontent.com/IndeecFOX/zapret4rocket/refs/heads/master/fast_install_for_OWRT.sh)
``` 
Upd 08.02.25:
- Update zapret to v70
- Убрана проверка наличия zip и его скачивание при отсутствии (фикс двойного скачивания так же из-за этого)

Upd 19.01.25: Добавлен вариант установки Marzban помимо 3xui и прочего

Upd 17.01.25:
- Включена работа с ipv6 по-умолчанию
- Добавлена возможность так же установить wg или 3proxy в начале работы скрипта (Ранее был только 3xui)

Upd 31.12.24:
- Обновление 69.8 > 69.9v 
- Добавлено удаление архива после установки
  
UPD 30.12.24: Команда установки сокращена, скрипт теперь не скачивается на ваш сервер для своего исполнения  
  
UPD 29.12.24(3): Фикс ввода Y при запросе на установку 3x-ui, если ранее был ввод русскими буквами  
  
UPD 29.12.24(2):
- Изменена стратегия udp quick под VDS хостинг. На рокете так же отлично работает. Будем считать универсальной.  
- Добавлена перезагрузка zapret. Повышает стабильной. Хз почему. Но это так.  
  
UPD 29.12.24:
- Оптимизация под другие хостинги (убран принудительный выбор wan интерфейса)  
- Добавлена возможность в самом начале скрипта попросить установить 3x-ui панель (просто ввести Y на вопрос)  
  
UPD 28.12.24:  
Добавлена проверка на наличие архива запрета, дабы избежать повторного скачивания и размножения архивов  
  
UPD 26.12.24:  
Обновлена стратегия под googlevideo.com 
