** IN HERES THERES ONLY ANSWERS OF QUESTIONS AND THEIR SCREENSHOTS, QUESTION'S REFERENCE WILL BE AVAILABLE**

**WEEK 3**
**SINGLE TABLE QUERY:**
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

Q:10)ANSWER: 

**MULTIPLE TABLE QUERY**
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
