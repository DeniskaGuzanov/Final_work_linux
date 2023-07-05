### 1.

* cat > "Домашние животные"
Собаки
Кошки
Хомяки
* 'Ctrl+d'


* cat > "Вьючные животные"
Лошади
Верблюды
Ослы
* 'Ctrl+d'


* cat "Домашние животные" "Вьючные животные" > Animals
cat Animals
* mv "Animals" "Друзья человека"

![1](https://github.com/DeniskaGuzanov/Final_work_linux/blob/master/1_2.png


### 2. 


* mkdir folder_for_attestation
mv 'Друзья человека' folder_for_attestation/
ls
cd folder_for_attestation/
ls

![2](https://github.com/DeniskaGuzanov/Final_work_linux/blob/master/2.png

### 3.

* sudo apt-get update
sudo apt update
sudo apt install mysql-server
sudo service mysql status

![3](https://github.com/DeniskaGuzanov/Final_work_linux/blob/master/3_1.png
![3.1](https://github.com/DeniskaGuzanov/Final_work_linux/blob/master/3_2.png
![3.2](https://github.com/DeniskaGuzanov/Final_work_linux/blob/master/3_3.png
![3.3](https://github.com/DeniskaGuzanov/Final_work_linux/blob/master/3_4.png

### 4.

* wget http://ftp.us.debian.org/debian/pool/main/s/sl/sl_5.02-1_amd64.deb
sudo dpkg -i sl_5.02-1_amd64.deb
sudo dpkg -r sl

![4](https://github.com/DeniskaGuzanov/Final_work_linux/blob/master/4_2.png

### 5.

* 730  mkdir attestation
* 731  cd attestation/
* 732  cat > Домашние животные
* 733  cat > "Домашние животные"
* 734  cat > "Вьючные животные"
* 735  cat "Домашние животные" "Вьючные животные" > Animals
* 736  cat Animals
* 737  mv "Animals" "Друзья человека"
* 738  clear
* 739  mkdir folder_for_attestation && mv "Друзья человека" /attestation/folder_for_attestation
* 740  ls
* 741  rmdir folder_for_attestation/
* 742  ls
* 743  clear
* 744  mkdir folder_for_attestation
* 745  mv "Друзья человека" /attestation/folder_for_attestation
* 746  mv "Друзья человека" attestation/folder_for_attestation
* 747  ls
* 748  mkdir folder_for_attestation
* 749  rmdir folder_for_attestation
* 750  clear
* 751  mkdir folder_for_attestation
* 752  mv 'Друзья человека' attestation/folder_for_attestation/
* 753  mv 'Друзья человека' folder_for_attestation/
* 754  ls
* 755  cd folder_for_attestation/
* 756  ls
* 757  clear
* 758  cd..
* 759  cd.
* 760  cd..
* 761  cd
* 762  cd attestation/
* 763  clear
* 764  sudo apt-get update
* 765  sudo apt update
* 766  sudo apt install mysql
* 767  sudo apt install mysql-server
* 768  sudo service mysql status
* 769  clear
* 770  wget http://ftp.us.debian.org/debian/pool/main/s/sl/sl_5.02-1_amd64.deb
* 771  sudo dpkg -i sl_5.02-1_amd64.deb
* 772  sudo dpkg -r sl
* 773  clear
* 774  history

![5](https://github.com/DeniskaGuzanov/Final_work_linux/blob/master/5.png

### 6.

![6](https://github.com/DeniskaGuzanov/Final_work_linux/blob/master/diagram.png

### 7.
* CREATE DATABASE Друзья_человека;

![7](https://github.com/DeniskaGuzanov/Final_work_linux/blob/master/7.png


### 8.


* CREATE TABLE Родительский_класс (
id INT PRIMARY KEY AUTO_INCREMENT,
тип VARCHAR(50)
);


* CREATE TABLE Домашние_животные (
id INT PRIMARY KEY,
вид VARCHAR(50),
FOREIGN KEY (id) REFERENCES Родительский_класс(id)
);


* CREATE TABLE Собаки (
id INT PRIMARY KEY,
имя VARCHAR(50),
команда VARCHAR(50),
дата_рождения DATE,
FOREIGN KEY (id) REFERENCES Домашние_животные(id)
);


* CREATE TABLE Кошки (
id INT PRIMARY KEY,
имя VARCHAR(50),
команда VARCHAR(50),
дата_рождения DATE,
FOREIGN KEY (id) REFERENCES Домашние_животные(id)
);


* CREATE TABLE Хомяки (
id INT PRIMARY KEY,
имя VARCHAR(50),
команда VARCHAR(50),
дата_рождения DATE,
FOREIGN KEY (id) REFERENCES Домашние_животные(id)
);


* CREATE TABLE Вьючные_животные (
id INT PRIMARY KEY,
вид VARCHAR(50),
FOREIGN KEY (id) REFERENCES Родительский_класс(id)
);


* CREATE TABLE Лошади (
id INT PRIMARY KEY,
имя VARCHAR(50),
команда VARCHAR(50),
дата_рождения DATE,
FOREIGN KEY (id) REFERENCES Вьючные_животные(id)
);


* CREATE TABLE Верблюды (
id INT PRIMARY KEY,
имя VARCHAR(50),
команда VARCHAR(50),
дата_рождения DATE,
FOREIGN KEY (id) REFERENCES Вьючные_животные(id)
);


* CREATE TABLE Ослы (
id INT PRIMARY KEY,
имя VARCHAR(50),
команда VARCHAR(50),
дата_рождения DATE,
FOREIGN KEY (id) REFERENCES Вьючные_животные(id)
);

show databases;
show tables;

![8](https://github.com/DeniskaGuzanov/Final_work_linux/blob/master/8.png

### 9.

* INSERT INTO Верблюды ( имя, команда, дата_рождения)
VALUES ('Зефир', 'Но, пошел', '2019-09-01'),
('Багдад', 'На месте' '2020-11-12'),
('Скорость', 'Ждать' '2021-04-05');

* INSERT INTO Кошки ( имя, команда, дата_рождения)
VALUES ('Маркиз', 'Кис-кис', '2021-01-20'),
('Снежка', 'Давай играть', '2022-03-08');

* INSERT INTO Лошади ( имя, команда, дата_рождения)
VALUES ('Спирит', 'Но', '2020-01-21'),
('Воронок', 'Бррррр', '2022-03-08');

* INSERT INTO Ослы ( имя, команда, дата_рождения)
VALUES ('Нарик', 'Пошёл', '2019-01-21'),
('Степан', 'Стой', '2021-03-08');

* INSERT INTO Собаки ( имя, команда, дата_рождения)
VALUES ('Шарик', 'Дай лапу', '2019-01-21'),
('Бим', 'Лежать', '2020-03-08');

* INSERT INTO Хомяки ( имя, команда, дата_рождения)
VALUES ('Долгожитель', 'Кушать', '2022-01-21'),
('Хома', 'Отойди', '2023-03-08');

### 10.

* TRUNCATE TABLE Верблюды;

* CREATE TABLE Парнокопытные AS
SELECT * FROM Лошади
UNION
SELECT * FROM Ослы;


### 11.

* CREATE TABLE Парнокопытные AS
* SELECT *, TIMESTAMPDIFF(MONTH, дата_рождения, CURDATE()) AS возраст_в_месяцах
FROM (
* SELECT 'Собаки' AS тип_животного, имя, команда, дата_рождения FROM Собаки
UNION ALL
* SELECT 'Кошки' AS тип_животного, имя, команда, дата_рождения FROM Кошки
UNION ALL
* SELECT 'Хомяки' AS тип_животного, имя, команда, дата_рождения FROM Хомяки
UNION ALL
* SELECT 'Лошади' AS тип_животного, имя, команда, дата_рождения FROM Лошади
UNION ALL
* SELECT 'Ослы' AS тип_животного, имя, команда, дата_рождения FROM Ослы
) AS животные
* WHERE дата_рождения >= DATE_SUB(CURDATE(), INTERVAL 3 YEAR)
* AND дата_рождения <= DATE_SUB(CURDATE(), INTERVAL 1 YEAR);


### 12. 

CREATE TABLE Полный_состав AS
* SELECT 'Собаки' AS тип_животного, имя, команда, дата_рождения FROM Собаки
UNION ALL
* SELECT 'Кошки' AS тип_животного, имя, команда, дата_рождения FROM Кошки
UNION ALL
* SELECT 'Хомяки' AS тип_животного, имя, команда, дата_рождения FROM Хомяки
UNION ALL
* SELECT 'Лошади' AS тип_животного, имя, команда, дата_рождения FROM Лошади
UNION ALL
* SELECT 'Ослы' AS тип_животного, имя, команда, дата_рождения FROM Ослы;

### 13 - Java ![Перейти](https://github.com/DeniskaGuzanov/Final_work_linux/tree/master/src/Java
### 14 - Java ![Перейти](https://github.com/DeniskaGuzanov/Final_work_linux/tree/master/src/Java
### 15 - Java ![Перейти](https://github.com/DeniskaGuzanov/Final_work_linux/tree/master/src/Java
