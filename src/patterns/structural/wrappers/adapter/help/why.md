##Шаги реализации

- #####Убедитесь, что у вас есть два класса с несовместимыми интерфейсами:

    - полезный сервис — служебный класс, который вы не можете изменять (он либо сторонний, либо от него зависит другой код);

    - один или несколько клиентов — существующих классов приложения, несовместимых с сервисом из-за неудобного или несовпадающего интерфейса.

- #####Опишите клиентский интерфейс, через который классы приложения смогли бы использовать класс сервиса.

- #####Создайте класс адаптера, реализовав этот интерфейс.

- #####Поместите в адаптер поле, которое будет хранить ссылку на объект сервиса. Обычно это поле заполняют объектом, переданным в конструктор адаптера. В случае простой адаптации этот объект можно передавать через параметры методов адаптера.

- #####Реализуйте все методы клиентского интерфейса в адаптере. Адаптер должен делегировать основную работу сервису.

- #####Приложение должно использовать адаптер только через клиентский интерфейс. Это позволит легко изменять и добавлять адаптеры в будущем.

##Преимущества 

- #####Отделяет и скрывает от клиента подробности преобразования различных интерфейсов.

##Недостатки

- #####Усложняет код программы из-за введения дополнительных классов.