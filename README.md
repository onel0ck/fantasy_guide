# Руководство по Fantasy Manager

Это руководство поможет вам настроить аккаунты и эффективно использовать Fantasy Manager.

## Необходимые компоненты

- Twitter аккаунт с токенами
- Браузер Chrome
- Residential прокси (рекомендуемые провайдеры ниже)
- Базовое понимание работы с кошельками и приватными ключами

## Пошаговая настройка

### 1. Настройка Twitter аккаунта

1. Приобретите Twitter аккаунт с токенами
2. Установите расширение [EditThisCookie](https://chromewebstore.google.com/detail/editthiscookies/hlgpnddmgbhkmilmcnejaibhmoiljhhb)
3. Войдите в ваш Twitter аккаунт

### 2. Настройка Fantasy аккаунта

1. Перейдите на [Fantasy.top](https://fantasy.top/)
2. Войдите через ваш Twitter аккаунт
3. Важно: Каждый аккаунт необходимо активировать перед использованием daily claims и других функций

### 3. Активация аккаунта

1. Перейдите в [Fantasy Tactics](https://fantasy.top/play/tactics)
2. Зарегистрируйтесь в бесплатной тактике
   - Для большого количества аккаунтов не обязательно выбирать колоду
   - Достаточно просто нажать на регистрацию
   - Этот шаг активирует ваш аккаунт для дальнейших операций

### 4. Получение учетных данных

1. Нажмите на иконку профиля в левом нижнем углу
2. Перейдите в Settings
3. Нажмите "Export Wallet"
4. Скопируйте приватный ключ и адрес кошелька
5. Сохраните в следующем формате:
```
ПРИВАТНЫЙ_КЛЮЧ:АДРЕС_КОШЕЛЬКА
```

### 5. Настройка прокси, СТАТИЧНЫЕ ГЕНЕРИРУЕМ

#### Рекомендуемые провайдеры прокси:

1. [TravchisProxies](https://travchisproxies.com/billing/order/residential/110)
   - Рекомендуются residential прокси для лучшей производительности
   - Хорошая надежность и скорость

2. [ThunderProxy](https://www.thunderproxy.com/)
   - Позволяет генерировать в нужном формате
   - Убедитесь, что выбран HTTP формат

Требуемый формат:
```
http://login:password@ip:port
```

### 6. Настройка софта

1. Клонируйте репозиторий:
```bash
git clone https://github.com/onel0ck/fantasy-manager.git
cd fantasy-manager
```
УСТАНОВИТЕ:
![image](https://github.com/user-attachments/assets/0bae5557-c998-4fdb-84dc-4d4066c2ae63)

2. Обновите config.json под ваши настройки
3. Добавьте прокси в proxys.txt
4. Добавьте учетные данные в keys_and_addresses.txt

### Важные заметки по конфигурации

Если у ваших аккаунтов больше 6 тактик:
1. Установите `"threads": 1` в config.json
2. Установите `"old_account": true` в секции tactic
3. Убедитесь в наличии достаточного баланса для входа в тактику

Пример конфигурации для аккаунтов с 6+ тактиками:
```json
{
    "app": {
        "threads": 1,
        ...
    },
    "tactic": {
        "enabled": true,
        "old_account": true,
        ...
    }
}
```

## Распространенные проблемы и решения

1. **Rate Limiting**
   - Используйте residential прокси
   - Не запускайте слишком много потоков одновременно
   - Включите ротацию прокси в конфиге

2. **Проблемы с балансом**
   - Убедитесь в достаточном балансе для тактик
   - Проверьте настройку min_balance в конфиге
   - Отслеживайте комиссии за переводы

3. **Проблемы с аутентификацией**
   - Проверьте валидность Twitter аккаунта
   - Проверьте подключение к прокси
   - Убедитесь, что аккаунт правильно активирован

## Лучшие практики

1. **Управление аккаунтами**
   - Ведите организованный учет аккаунтов
   - Регулярно делайте backup учетных данных
   - Отслеживайте активность аккаунтов

2. **Использование прокси**
   - Используйте свежие прокси
   - Регулярно меняйте прокси
   - Отслеживайте производительность прокси

3. **Оптимизация производительности**
   - Начинайте с меньшего количества потоков
   - Постепенно увеличивайте на основе производительности
   - Отслеживайте показатели успешности

## Поддержка

По вопросам и проблемам:
- Telegram: [@unluck_1l0ck](https://t.me/unluck_1l0ck)
- GitHub Issues: [Fantasy Manager Repository](https://github.com/onel0ck/fantasy-manager/issues)

## Отказ от ответственности

Этот инструмент предназначен исключительно для образовательных целей. Используйте в соответствии с условиями использования Fantasy.top.
