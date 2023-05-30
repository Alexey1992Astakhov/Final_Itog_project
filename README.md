Задание
1. Используя команду cat в терминале операционной системы Linux, создать
   два файла Домашние животные (заполнив файл собаками, кошками,
   хомяками) и Вьючные животными заполнив файл Лошадьми, верблюдами и
   ослы), а затем объединить их. Просмотреть содержимое созданного файла.
   Переименовать файл, дав ему новое имя (Друзья человека).
   ![](screenshots/1.png)
2. Создать директорию, переместить файл туда.

   ![](screenshots/2.png)
3. Подключить дополнительный репозиторий MySQL. Установить любой пакет
   из этого репозитория.
   - скачиваем репозиторий:
   

    wget https://dev.mysql.com/get/mysql-apt-config_0.8.24-1_all.deb
   ![](screenshots/3.1.png)
   - устанавливаем репозиторий:
   

    sudo dpkg -i mysql-apt-config_0.8.24-1_all.deb
   ![](screenshots/3.2.png)
    
   - устанавливаем один из пакетов в репозитории:

    sudo apt-get install mysql-client
   ![](screenshots/3.3.png)

4. Установить и удалить deb-пакет с помощью dpkg.
    

    wget http://archive.ubuntu.com/ubuntu/pool/universe/p/pacman/pacman_10-17.2_amd64.deb

    sudo dpkg -i pacman_10-17.2_amd64.deb
   ![](screenshots/4.1.png)
   

    sudo dpkg -r pacman
   ![](screenshots/4.2.png)

5. Выложить историю команд в терминале ubuntu
    ![](screenshots/5.png)


6. Нарисовать диаграмму, в которой есть класс родительский класс, домашние
   животные и вьючные животные, в составы которых в случае домашних
   животных войдут классы: собаки, кошки, хомяки, а в класс вьючные животные
   войдут: Лошади, верблюды и ослы).

    ![](screenshots/Диаграмма.drawio.png)

7. В подключенном MySQL репозитории создать базу данных “Друзья
   человека”

    ![](screenshots/7.png)

8. Создать таблицы с иерархией из диаграммы в БД


     *human_friends.sql*


9. Заполнить низкоуровневые таблицы именами(животных), командами
   которые они выполняют и датами рождения
    

    *add_human_friends.sql*

    *commands.sql*


10. Удалив из таблицы верблюдов, т.к. верблюдов решили перевезти в другой
    питомник на зимовку. Объединить таблицы лошади, и ослы в одну таблицу.


    *delete_camel.sql*

    *union_horse_and_donkey.sql*
    

11. Создать новую таблицу “молодые животные” в которую попадут все
    животные старше 1 года, но младше 3 лет и в отдельном столбце с точностью
    до месяца подсчитать возраст животных в новой таблице
    

    *young_pets.sql*


12. Объединить все таблицы в одну, при этом сохраняя поля, указывающие на
    прошлую принадлежность к старым таблицам.


    *union_all_tables.sql*


13. Создать класс с Инкапсуляцией методов и наследованием по диаграмме.
14. Написать программу, имитирующую работу реестра домашних животных.
    В программе должен быть реализован следующий функционал:
    14.1 Завести новое животное
    14.2 определять животное в правильный класс
    14.3 увидеть список команд, которое выполняет животное
    14.4 обучить животное новым командам
    14.5 Реализовать навигацию по меню
15. Создайте класс Счетчик, у которого есть метод add(), увеличивающий̆
    значение внутренней̆ int переменной̆на 1 при нажатие “Завести новое
    животное” Сделайте так, чтобы с объектом такого типа можно было работать в
    блоке try-with-resources. Нужно бросить исключение, если работа с объектом
    типа счетчик была не в ресурсном try и/или ресурс остался открыт. Значение
    считать в ресурсе try, если при заведения животного заполнены все поля.