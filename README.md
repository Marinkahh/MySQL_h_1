## Создание новой схемы ##

CREATE SCHEMA `homework1` ;  

## Создание таблицы ## 

CREATE TABLE `homework1`.`phone` (  
  `idphone` INT NOT NULL,  
  `ProductName` VARCHAR(45) NOT NULL,  
  ` Manufacturer` VARCHAR(45) NULL,  
  `ProductCount` INT NULL,  
  `Price` INT NULL,  
  PRIMARY KEY (`idphone`));  

## Заполнение таблицы ##

INSERT INTO `homework1`.`phone` (`ProductName`, ` Manufacturer`, `ProductCount`, `Price`) VALUES ('iPhone X', 'Apple', '3', '76000');  
INSERT INTO `homework1`.`phone` (`ProductName`, ` Manufacturer`, `ProductCount`, `Price`) VALUES ('iPhone 8', 'Apple', '2', '51000');  
INSERT INTO `homework1`.`phone` (`ProductName`, ` Manufacturer`, `ProductCount`, `Price`) VALUES ('Galaxy S9', 'Samsung', '2', '56000');  
INSERT INTO `homework1`.`phone` (`ProductName`, ` Manufacturer`, `ProductCount`, `Price`) VALUES ('Galaxy S8', 'Samsung', '1', '41000');  
INSERT INTO `homework1`.`phone` (`ProductName`, ` Manufacturer`, `ProductCount`, `Price`) VALUES ('P20 Pro', 'Huawei', '5', '36000');  

## Выведите название, производителя и цену для товаров, количество которых превышает 2 ##  

SELECT ProductName, Manufacturer, Price FROM homework1.phone  
WHERE ProductCount >=2;  

## Выведите весь ассортимент товаров марки “Samsung” ##

SELECT * FROM homework1.phone  
WHERE Manufacturer= 'Samsung';  

## С помощью регулярных выражений найти:##     

### Товары, в наименовании которых есть упоминание "Iphone" ###  

SELECT * FROM homework1.phone    
WHERE ProductName LIKE '%iPhone%';   

### Товары, в наименовании которых есть упоминание "Samsung" ###   

SELECT * FROM homework1.phone  
WHERE Manufacturer LIKE '%Samsung%';  

### Товары, в наименовании которых есть ЦИФРЫ ###   

SELECT * FROM homework1.phone   
WHERE ProductName REGEXP '[0-9]';   

### Товары, в наименовании которых есть ЦИФРА "8" ###   

SELECT * FROM homework1.phone   
WHERE ProductName LIKE '%8%';   
