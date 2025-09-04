# LAb_BDcomics

drop schema if exists comic_authors;
create schema comic_authors;
use comic_authors;

create table comic_authors(
id int auto_increment primary key,
name varchar(50) not null,
last_name varchar(50),
birthdate date,
reg_date date
);

insert into comic_authors (name, last_name, birthdate, reg_date) values
('Joaquín Salvador', 'Lavado Tejón', '1932-07-17','2020-01-10'),
('Ariel', 'Oliveti', '1967-11-15', '2018-10-14'),
('Héctor Germán', 'Oesterheld', '1919-07-23', '2017-12-25'),
('Alan', 'Moore', '1953-11-18', '2020-10-20'),
('Laura', 'Guarisco', '1991-01-01', '2024-08-20');

drop schema if exists comic_char;
create schema comic_char;
use comic_char;

create table comic_ch(
id int not null auto_increment,
name varchar(45),
species varchar(55),
quotes varchar(100),
primary key(id)
);

select *from comic_ch;

insert into comic_ch(name, species, quotes) values
('Superman', 'Alien', 'I’m here to fight for truth and justice.' ),
('Batman', 'Human', "I'm Batman"),
('Obelix', 'Human', 'These romans are crazy'),
('Rorschach', 'Human', 'lalala'),
('Conan The Barbarian', 'Human', 'For us, there is no spring. Just the wind that smells fresh before the storm.');

update comic_ch set quotes = 'Never compromise, not even in the face of Armageddon' where name= 'Rorschach';

select * from comic_ch cc where name= 'Rorschach';


use countries;



insert into countries_table (name, capital, gdp) values
('Suiza', 'Berna', 105669 ),
('Noruega', 'Oslo', 94660),
('Austria', 'Viena', 59225),
('Finlandia', 'Helsinki', 520),
('Alemania', 'Berlín', 54291);

DELETE FROM Countries.countries_table
WHERE name='Suiza';

update countries_table set gdp=55127 where capital= 'Helsinki';

