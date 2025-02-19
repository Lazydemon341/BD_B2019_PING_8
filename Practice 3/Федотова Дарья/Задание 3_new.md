﻿**Задание 1: Почему любое отношение в реляционной схеме имеет по крайней мере один ключ?**

Любое отношение в реляционной схеме имеет хотя бы один ключ, поскольку каждое отношение должно иметь уникальное значение (имя или номер). 



**Задание 2: Переведите все диаграммы ER из предыдущей домашней работы в реляционные схемы.**

1. ![task1\_new](./task1\_new.jpg)

Entities:

- Book: {[ISBN: integer, Year: datetime, Title: string, Author: string, Number-of-pages: integer]}
- Copy: {[Copy-ID: integer, ISBN, Position-on-the-shelf: integer]}
- Categories: {[ParentCategoryName: string, Name: string]}
- Publisher: {[Name: string, Address: string]}
- Reader: {[Reader-ID: integer, Last-Name: string, First-Name: string, Address: string, Birthday: datetime]}

Relationships:

- Exist: {[ISBN: integer, Title: string]}
- Assign: {[ ISBN: integer, Title: string]}
- Publish: {[ISBN: integer, Title: string, Name: string]}
- Get: {[ ISBN: integer, Title: string, Reader-ID: integer, Date-of-returnment: datetime]}



1. ![task2\_1](./task2\_1.jpg)

Entities:

- Country: {[Country-Name: string]}
- City: {[Country-Name: string, City-Name: string]}
- Street: {[Country-Name: string, City-Name: string, Street-Name: string]}
- House: {[Country-Name: string, City-Name: string, Street-Name: string, House-Number: integer]}
- Apartment: {[Country-Name: string, City-Name: string, Street-Name: string, House-Number: integer, Apartment-Number: integer]}

Same schemes for ‘located’ relationships.



1. ![task2\_2\_new](./task2\_2\_new.jpg)

Entities:

- Arbitrator: {[Arbitrator-Name: string]}
- Team: {[Team-Name: string]}

Relationships:

- Umpire: {[Arbitrator-Name: string, Team-Name: string]}


1. ![task2\_3\_new](./task2\_3\_new.jpg)

Entities:

- Man: {[Mans-Name: string]}
- Woman: {[Womans-Name: string]}

Relationships:

- Is a father: {[Mans-Name: string, Childs-Name: string]}
- Is a mother: {[Womans-Name: string, Childs-Name: string]}


1. ![task3\_new](./task3\_new.jpg)

Entities:

- Entity: {[Entity-Name: string]}
- Relationship: {[Relationship-Name: string]}
- Attribute of relationship: {[Attribute-Name: string]}

Relationships:

- Participate: {[Function: string, Role: string, Min: integer, Max: integer]}
- Has: {[Entity-Name: string, Attribute-Name: string]}



**Задание 3: Переведите приведенные диаграммы ER в реляционные схемы.** 

1. ![3\_1](./3\_1.jpg)

Entities:

- Station: {[Name: string, #Tracks: integer]}
- City: {[Name: string, Region: string]}
- Train: {[TrainNr: integer, Length: integer, StartStation: string, EndStation: string]}

Relationships:

- Lie-in: {[Name: string, Name: string]}
- Start: {[Name: string, TrainNr: integer]}
- End: {[Name: string, TrainNr: integer]}
- Connected: {[StartStation: string, TrainNr: integer, EndStation: string, Departure: datetime, Arrival: datetime]}



1. ![3\_2](./3\_2.jpg)

Entities:

- StationPersonell: {[PersNr: integer, #Name: string]}
- Caregiver: {[PersNr: integer, #Name: string, Qualification: string]}
- Doctor: {[PersNr: integer, #Name: string, Area: string, Rank: string, Treats: string]}
- Patient: {[PatientNr: integer, Name: string, Disease: string, PersNr: integer]}
- Station: {[StatNr: integer, Name: string]}
- Room: {[StatNe: integer, RoomNr: integer, #Beds: integer]}

Relationships:

- Works-for: {[PersNr: integer, StatNr: integer]}
- Treats: {[PersNr: integer, PatientNr: integer]}
- Has: {[StatNr: integer, RoomNr: integer]}
- Admission: {[StatNr: integer, RoomNr: integer, PatientNr: integer, from: string, to: string]}
