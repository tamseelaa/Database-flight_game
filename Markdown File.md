** IN HERES THERES ONLY ANSWERS OF QUESTIONS AND THEIR SCREENSHOTS, QUESTION'S REFERENCE WILL BE AVAILABLE**
                                            **WEEK 1**
**EXERCISE:1) BASIC CONCEPTS OF RELATIONAL DATABASE**
![Screenshot (192)](https://github.com/user-attachments/assets/2613f01e-db89-47ee-9671-2a47b5367aee)
![Screenshot (191)](https://github.com/user-attachments/assets/48354019-b230-42f8-87cd-0772cfa9fdf7)


                                             **WEEK 3**
**EXERCISE:2) SINGLE TABLE QUERY:**
Q:1)ANSWER : select * from goal;
<img width="636" alt="w3e1" src="https://github.com/user-attachments/assets/1f5ab892-8759-4f53-8a61-9fc7269df518">


Q:2)ANSWER: select name from airport where iso_country = "FI";
![image](https://github.com/user-attachments/assets/5706a447-9c75-45af-bb1d-814e2ea87619)
<img width="262" alt="w3e2 1" src="https://github.com/user-attachments/assets/5596298d-5289-44e9-9a4f-88e76536ac82">

Q:3)ANSWER: select name from airport where iso_country = "FI" order by name;
![Screenshot (172)](https://github.com/user-attachments/assets/b7cf948a-176c-4ed7-89d0-b46cbaf627c5)
![Screenshot (173)](https://github.com/user-attachments/assets/f38f7b87-133a-4a93-9f25-e5272aee7919)


Q:4)ANSWER: select name, type from airport where iso_country = "FI" order by type, name;
![Screenshot (174)](https://github.com/user-attachments/assets/b8a9f6f1-7426-40e2-9e25-d5b829cb14e5)
![Screenshot (175)](https://github.com/user-attachments/assets/9b4199d1-995c-4ea4-807c-b43373738055)
Q:5)ANSWER: select name from country where name like "F%";
<img width="485" alt="w3e5" src="https://github.com/user-attachments/assets/ca9ee14d-298e-440d-b218-2a505f38996f">

Q:6)ANSWER: select name from country where name like "%F%"; |  
<img width="417" alt="w3e6" src="https://github.com/user-attachments/assets/53c9fb60-97d9-4753-9495-ae8070c924a9">

Q:7)ANSWER: select location from game where screen_name = "Vesa";
<img width="464" alt="w3e7" src="https://github.com/user-attachments/assets/5b98a767-0b99-4357-91c8-e480745b7413">

Q:8)ANSWER: select co2_consumed from game where screen_name = "Ilkka";
<img width="459" alt="w3e8" src="https://github.com/user-attachments/assets/16f64786-68ce-427f-9f7c-d49843d5c6e8">

Q:9)ANSWER: select distinct co2_budget from game;
<img width="366" alt="w3e9" src="https://github.com/user-attachments/assets/a7e5c34f-47ae-4272-9ca6-381121d8bd7c">

Q:10)ANSWER: ![image](https://github.com/user-attachments/assets/6339c1e5-8391-43d9-83c2-14d9ed8a8165)


**EXERCISE:3) MULTIPLE TABLE QUERY**
Q:1) ANSWER= select country.name as "country name", airport.name as "airport name"
from airport, country
where airport.iso_country = country.iso_country and country.name = "Iceland";
![Screenshot (179)](https://github.com/user-attachments/assets/3250a03a-3bf6-4034-8231-3fafdb0ee90c)
![Screenshot (178)](https://github.com/user-attachments/assets/ef060ed1-13f6-4dea-885d-009d7bfca5d1)


Q:2) ANSWER= select airport.name as "airport name"
from airport, country
where airport.iso_country = country.iso_country and country.name = "France" and airport.type = "large_airport";
![Screenshot (180)](https://github.com/user-attachments/assets/ac8dc270-567e-42ed-b592-bc75f560fb48)

Q:3) ANSWER= select country.name as country_name, airport.name as airport_name
from airport, country
where airport.iso_country = country.iso_country and country.continent = "AN";
![Screenshot (181)](https://github.com/user-attachments/assets/ab211224-13b7-4827-b477-406c0a5edd16)
![Screenshot (182)](https://github.com/user-attachments/assets/61b2fcd1-11dd-4323-bb89-b679a657b4b7)

Q:4) ANSWER= select elevation_ft
from airport, game
where location = ident and screen_name = "Heini";
![Screenshot (183)](https://github.com/user-attachments/assets/e5a648be-0c9a-4ec6-aad6-3918d1717779)

Q:5) ANSWER= select elevation_ft * 0.3048 as elevation_m
from airport, game
where location = ident and screen_name = "Heini";
![Screenshot (184)](https://github.com/user-attachments/assets/84859b3b-b64a-4dc2-8475-9debb03b7975)

Q:6) ANSWER= select name
from airport, game
where location = ident and screen_name = "Ilkka";
![Screenshot (185)](https://github.com/user-attachments/assets/5d353b03-2976-4d8a-a5df-4d0c58a79c03)

Q:7) ANSWER= select country.name
from airport, game, country
where location = ident and airport.iso_country = country.iso_country  and screen_name = "Ilkka";
![Screenshot (186)](https://github.com/user-attachments/assets/37f3f60b-a4fa-4327-884f-c9546b1d09ee)

Q:8) ANSWER= select name
from goal, goal_reached, game
where game.id = game_id and goal.id = goal_id and screen_name = "Heini";
![Screenshot (187)](https://github.com/user-attachments/assets/bafad3f8-0324-4c3f-a5b8-00bc1464b492)

Q:9) ANSWER= select airport.name
from airport, game, goal, goal_reached
where ident = location and game.id = game_id and goal.id = goal_id and screen_name = "Ilkka" and goal.name = "CLOUDS";
![Screenshot (188)](https://github.com/user-attachments/assets/02f1de4d-7c07-42d0-bf73-70b58a21db70)

Q:10) ANSWER= select country.name
from country, airport, game, goal, goal_reached
where airport.iso_country = country.iso_country and ident = location and game.id = game_id and goal.id = goal_id and screen_name = "Ilkka" and goal.name = "CLOUDS";
![Screenshot (189)](https://github.com/user-attachments/assets/81d41c09-a2be-448f-bb7d-83069df93ed3)
                                           **WEEK 3 DONE HERE**

                                              **WEEK 4**
**EXERCISE:4) JOIN**
Q:1)ANSWER: select country.name as "country name", airport.name as "airport name"
from country inner join airport on airport.iso_country = country.iso_country
where country.name = "Finland" and scheduled_service = "yes";
![Screenshot (193)](https://github.com/user-attachments/assets/74304c8a-3782-4668-ae47-68e0bf05285c)


Q:2)ANSWER: select screen_name, airport.name
from game inner join airport on location = ident;
![Screenshot (194)](https://github.com/user-attachments/assets/c1e2276c-3f23-4636-8d88-bafeb184d0a7)



Q:3)ANSWER: select screen_name, country.name
from game inner join airport on location = ident inner join country on airport.iso_country = country.iso_country;
![Screenshot (195)](https://github.com/user-attachments/assets/e09595b7-776e-48db-8fb6-115867bc5641)


Q:4)ANSWER: select airport.name, screen_name
from airport left join game on ident = location where name like "%Hels%";
![Screenshot (196)](https://github.com/user-attachments/assets/386e2dee-ca90-4b08-a848-271a69b28032)

Q:5)ANSWER: select name, screen_name
from goal left join goal_reached on goal.id = goal_id  left join game on game.id = game_id;
![Screenshot (198)](https://github.com/user-attachments/assets/7c4ccfc1-b2fe-4b9e-a94b-d0f6a97999eb)

**EXERCISE:5) SUBQUERIES**
Q:1)ANSWER: select name from country where iso_country in(select iso_country
 from airport where name like "Satsuma%");
 ![Screenshot (199)](https://github.com/user-attachments/assets/ffec3a0f-51d5-4a30-afa2-3e7467f88229)

Q:2)ANSWER: select name from airport where iso_country in(
select iso_country from country where name = "Monaco"
);
![Screenshot (200)](https://github.com/user-attachments/assets/1f005aa9-b88a-4d0a-a87f-d0908da7c9c8)

Q:3)ANSWER: select screen_name from game where id in (
select game_id from goal_reached where goal_id in(
select id from goal where name = "CLOUDS")
);
![Screenshot (201)](https://github.com/user-attachments/assets/3295f820-1bad-4f60-850f-6745b97a30c7)

Q:4)ANSWER: select country.name from country where iso_country not in
(select airport.iso_country from airport);
![Screenshot (202)](https://github.com/user-attachments/assets/26647842-0b95-4659-9a3a-8dc5be360ab5)

Q:5)ANSWER: select name from goal where id not in(
select goal.id from goal, goal_reached, game where game.id = game_id and goal.id = goal_id and screen_name = "Heini");
![Screenshot (203)](https://github.com/user-attachments/assets/fb4db200-545b-4fce-8dc8-347d298ded3e)
                                **WEEK 4 DONE**

                                **WEEK 5**
**EXERCISE:6) Aggregate Queries**
Q:1)ANSWER: select max(elevation_ft)
from airport;
![Screenshot (204)](https://github.com/user-attachments/assets/fac42f05-88eb-4ad5-84af-6de5c9c7a2cb)

Q:2)ANSWER:select continent, count(*) from country group by continent;
![Screenshot (205)](https://github.com/user-attachments/assets/f2dd5b3e-7817-4f5b-8545-f27401c1bdfc)

Q:3)ANSWER:select screen_name, count(*) from game, goal_reached where id = game_id group by screen_name;
![Screenshot (206)](https://github.com/user-attachments/assets/94f73e6f-8a49-46e9-9284-ec59bb4dc0ca)

Q:4)ANSWER: select screen_name from game where co2_consumed in(
select min(co2_consumed) from game);
![Screenshot (207)](https://github.com/user-attachments/assets/53da5d87-d878-417b-b79b-27be152f27cc)


Q:5)ANSWER: select country.name, count(*) from airport, country
 where airport.iso_country = country.iso_country
 group by country.iso_country order by count(*) desc limit 50;
 ![Screenshot (208)](https://github.com/user-attachments/assets/03c47db0-aa5e-48a4-88f6-1ed6e3f6186c)


Q:6)ANSWER: select country.name
 from airport, country where airport.iso_country = country.iso_country
 group by country.iso_country having count(*) > 1000;
![Screenshot (209)](https://github.com/user-attachments/assets/e9c465e7-c3da-405b-8877-390475662be5)


Q:7)ANSWER: select name from airport where elevation_ft in (
select max(elevation_ft) from airport);
![Screenshot (210)](https://github.com/user-attachments/assets/a889c074-8da3-4c32-8e72-30a4373cf041)

Q:8)ANSWER: select name from country where iso_country in (
select iso_country from airport where elevation_ft in(
select max(elevation_ft) from airport));
![Screenshot (211)](https://github.com/user-attachments/assets/f2b981ac-f609-483c-8f28-6f58da911484)


Q:9)ANSWER: select count(*) from game, goal_reached where id = game_id and screen_name = "Vesa" group by screen_name;
![Screenshot (212)](https://github.com/user-attachments/assets/cc1994df-6ef5-4eff-8db9-fe4a5cdd4092)

Q:10)ANSWER:select name from airport where latitude_deg in(
select min(latitude_deg)from airport); 
![Screenshot (213)](https://github.com/user-attachments/assets/0c74d2bb-e60c-4e37-a959-a72f56c4a37e)

**EXERCISE 7)Update Queries**
Q:1)ANSWER: update game
 set  location = (select ident from airport where name = "Nottingham Airport"), co2_consumed = co2_consumed+500
 where screen_name = "Vesa";
select * from game;
![Screenshot (215)](https://github.com/user-attachments/assets/9439e48d-1f93-496a-97f6-215b09159ba4)


Q:2)ANSWER: ![Screenshot (216)](https://github.com/user-attachments/assets/e9f6dcbb-b606-4b87-8181-6336e8556bc9)
![Screenshot (219)](https://github.com/user-attachments/assets/92fd7e06-5d67-4bef-afc8-b7c79b4c605c)


Q:3)ANSWER: delete from goal_reached;
select * from goal_reached;
![Screenshot (217)](https://github.com/user-attachments/assets/54011895-d786-436c-9ab2-d6d43b85106f)



Q:4)ANSWER: delete from game;
select * from game;
![Screenshot (218)](https://github.com/user-attachments/assets/60e32ce2-5be4-4fc4-9570-5a4d27a8063d)
                                          **WEEK 5 DONE**
