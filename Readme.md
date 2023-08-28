# PHP Demo project serialization

Демонстрационный проект по работе с PHP в части сериализации / десериализации данных.

## Исходная постановка
Необходимо реализовать набор классов для передачи сообщений в текстовой среде (HTTP запросы к примеру).
Классы для реализации:
- Message
-- Meta
-- Event
-- Payload

Данные классы должны сериализоваться в json строку, посредством метода serialize и десерилиазоваться из строки обратно в объект.
2 базовых теста на проверку
- пустой объект
- объект с данными

Каждый объект может содержать элементы разных классов, а так же nested объекты и массивы других объектов.

Результатом тестового задания должно быть:
- Классы Message, Meta, Event, Payload
- UnitTest класс MessageEntityTest с двумя тест методами (пустой и с данными), критерий приемки $this->assertEquals($message, Message::deserialize($message->serialize());