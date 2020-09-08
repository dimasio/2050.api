# Приватная интеграция SRM

**Приватной интеграцией** называется простейший вид интеграции, который устанавливается для одного аккаунта

Создание подобной интеграции заключается в следующих шагах:
1. Авторизация в системе 
2. Настройка интеграции
3. Получить ключи доступа и настроить обмен данными

**Пример реализации на php используя oAuth 2.0**

```php
<?php
class x360SimpleApi {
	private $auth = [
		'username' => '',
		'client_id' => '',
		'client_secret' => '',
		'grant_type' => 'authorization_code',
		'code' => '',
		'redirect_uri' => '',
    ];
?>
```

# Список доступных методов

## Список план-графиков
| Тип | Свойство |
| :------ | :------ |
| Метод | GET, POST /api/my/srm/pp/list |
| Описание  | Позволяет получить список план-графиков |
| Ограничения | Метод доступен в соответствии с правами пользователя |
| GET, POST параметры | ... |
| Заголовок типа данных при успешном результате | Content-Type: application/hal+json |
| Заголовок типа данных при ошибке | Content-Type: application/problem+json |
| HTTP коды ответа |200 - Успешно, 401 - Unauthorized |
| Параметры ответа | ... |
| Пример ответа | ... |

## Сознание нового план-графика
| Тип | Свойство |
| :------ | :------ |
| Метод | POST /api/my/srm/pp/create |
| Описание  | Позволяет создать план-график |
| Ограничения | Метод доступен в соответствии с правами пользователя |
| POST параметры | ... |
| Заголовок типа данных при успешном результате | Content-Type: application/hal+json |
| Заголовок типа данных при ошибке | Content-Type: application/problem+json |
| HTTP коды ответа |200 - Успешно, 401 - Unauthorized, 400 - Uncorrect data |
| Параметры ответа | ... |
| Пример ответа | ... |

## Получение списка закупок по ID
| Тип | Свойство |
| :------ | :------ |
| Метод | GET /api/my/srm/pp/:id/active/ppp/list |
| Описание  | Позволяет получить список закупок для активной версии выбранного плана закупок |
| Ограничения | Метод доступен в соответствии с правами пользователя |
| GET параметры | ... |
| Заголовок типа данных при успешном результате | Content-Type: application/hal+json |
| Заголовок типа данных при ошибке | Content-Type: application/problem+json |
| HTTP коды ответа |200 - Успешно, 401 - Unauthorized, 204 - Undefined ID |
| Параметры ответа | ... |
| Пример ответа | ... |

## Получение перечня номенклатуры
| Тип | Свойство |
| :------ | :------ |
| Метод | GET, POST /api/my/srm/goods/list |
| Описание  | Позволяет получить перечень номенклатуры |
| Ограничения | Метод доступен в соответствии с правами пользователя |
| GET, POST параметры | ... |
| Заголовок типа данных при успешном результате | Content-Type: application/hal+json |
| Заголовок типа данных при ошибке | Content-Type: application/problem+json |
| HTTP коды ответа |200 - Успешно, 401 - Unauthorized |
| Параметры ответа | ... |
| Пример ответа | ... |

## Cоздание новой версии план-графика
| Тип | Свойство |
| :------ | :------ |
| Метод | POST /api/my/srm/pp/:id/newversion |
| Описание  | Позволяет создать новую версию плана-графика |
| Ограничения | Метод доступен в соответствии с правами пользователя |
| POST параметры | ... |
| Заголовок типа данных при успешном результате | Content-Type: application/hal+json |
| Заголовок типа данных при ошибке | Content-Type: application/problem+json |
| HTTP коды ответа |200 - Успешно, 401 - Unauthorized, 204 - Undefined ID |
| Параметры ответа | ... |
| Пример ответа | ... |
