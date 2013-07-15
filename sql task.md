Create database vehicles ;
Use vehicles

Create table vehicles (vehicle_id int, type varchar(20), primary key(vehicle_id) );

Create table cars (car_id int, maker varchar(20), model varchar(20),  year int, nomer_kyzova int, engine¬¬_volume int, engine¬¬_power int, transmition_type char(1), seats int, color varchar(20), price int, primary key(car_id), foreign key(car_id) references vehicles (vehicle_id) );

Create table motorcycles ( motorcycle_id int, maker varchar(20), model varchar(20), year int,  nomer_kyzova int , engine¬¬_volume int, engine¬-_power int, transmition_type char(1), color varchar(20), price int, primary key(motorcycle_id), foreign key(motorcycle_id) references vehicles (vehical_id) );

Insert into vehicles values ( ‘001’, ‘car’), (‘002’, ‘car’), (‘003’, ‘motorcycle’), (‘004’, ‘car’),( ‘005’, ‘car’), ( ‘006’, ‘motorcycle’), (‘007’, ‘car’) );

Insert into cars values (‘001’, ‘Toyota’, ‘Camry’, ‘2013’, ‘11111111’, ‘3000’, ‘220’, ‘a’, ‘5’, ‘black’, ‘32000’), (‘002’, ‘Mazda’, ‘CX7’, ‘2009’, ‘22222222’, ‘2300’, ‘220’,’ a’, ‘5’, ‘silver’, ‘20000’), (‘004’, ‘Honda’, ‘Accord’, ‘2011’, ‘44444444’, ‘2400’, ‘195’, ‘a’, ‘5’, ‘white’, ‘28000’), (‘005’, ‘Mazda’, ‘6’, ‘2013’, ‘55555555’, ‘2000’, ‘160’,’ a’, ‘5’, ‘black’, ‘28000’), (‘007’, ‘BMW’, ‘760’, ‘2009’, ‘7777777’, ‘6000’, ‘450’,’ a’, ‘5’, ‘black’, ‘50000’);

Insert into motorcycles values (‘003’, ‘Kawasaki’, ‘Ninja’, ‘2013’, ‘33333333’, ‘250’, ‘35’, ‘m’, ‘black’, ‘18000’), (‘006’, ‘Suzuki’, ‘Bandit’, ‘2011’, ‘66666666’, ‘400’, ‘60’, ‘m’, ‘silver’, ‘12000’);


Select car_id, maker from cars where maker like “m%”;
Select * from cars, motorcycles where cars.color=motorcycles.color;
Select Count(model) from motorcycles;


