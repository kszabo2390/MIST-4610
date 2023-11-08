# Team 4 MIST 4610 Group Project 1

## Team Name
15061 Group 4

## Team Members
1) Joey Lund [@jl4600](https://github.com/jl4600) 
2) Armon Parsa [@armon222](https://github.com/armon222)
3) Kyle Szabo [@kszabo2390](https://github.com/kszabo2390)

## Problem Description:

The challenge is to model and build a relational database for the operations of a new football club called the Georgia Lions. In the model, the main entity is Players, which describes all of the player's personal information and statistics on the field. The other entities either support, magnify, monetize, or track player performance and relationships with other parts of the Georgia Lions operation. For this new team, we want to comprehensively model these relationships, obtain data for the entities, and use queries to answer questions that will help evaluate performance of the club. 

## Data Model:

### Explanation of data model:

The data model is based on the necessary operations for a football club. The managers entity describes all the different types of people who work in the front office of the club in scouting, player development, and overall team evaluation. The managers hire many coaches, who report to the many managers as their bosses. This creates a many-to-many relationship between Coaches and Managers, with Managers_has_Coaches as the weak entity. The coaches entity describes the many coaches in the organization by name, role, and salary. 
The coaches have many players that they coach, but each player has one coach that trains them specifically (ex. Defensive coach trains the defensive players). This establishes the one-to-many relationship between Players and Coaches. As described earlier, Players is the main entry in the database, representing information about the player's name, nationality, individual statistics, and who is their coach. 


The Players table branches off in a few different directions, the Youth Academy table represents all the players who are on the youth squad. This table gives the youth player’s name, birthday, position, nationality, and ID. There are many players in the youth academy, but players can only belong to one Youth Academy, creating a one-to-many relationship. Going to another branch, Players can play in many Matches, and this creates a many-to-many relationship where Injuries are the associative entity. Matches allow for all team results on the schedule to be tracked. The Injuries table illustrates injury type and severity for a player in a match. 


The external factors of the club are tracked as well, The Fans table shows a fan’s name, email address, the amount of team merchandise they have purchased, and whether or not they are a season ticket holder. Fans attend many Matches, and Matches have many Fans, so this creates another many-to-many relationship, creating an associative entity we call Stadiums. The stadium's entity uniquely identifies each stadium, which fans are in attendance, which match is being played at the stadium, as well as the stadium name and capacity. 


The sponsors table describes the important details about our club sponsors like sponsor name, contact information, and the value of their contract with the club. Sponsors are at many Matches, and Matches have many Sponsors, so we created an associative entity called Sponsorship, giving more granular detail about each individual sponsorship at each match. 


Lastly, the Fans entity and Players entity have a many-to-many relationship, because fans like many Players, and Players have many Fans. We created the Favorite Players entity to track which Players are fan favorites!

### The Data Model

![pic1](https://github.com/armon222/MIST-4600/assets/62662242/0f569885-8670-45c4-9873-c9ff335f961b)

## Data Dictionary

### Table: Matches

![pic2](https://github.com/armon222/MIST-4600/assets/62662242/c6c7b2a1-5c31-4165-8b7c-c136198837ca)

### Table: Coaches

![pic3](https://github.com/armon222/MIST-4600/assets/62662242/1e424e94-743b-43e2-8f72-07069339fe91)

### Table: Fans

![pic4](https://github.com/armon222/MIST-4600/assets/62662242/ef7d6d74-1e51-43fd-b0b9-5ea552364acf)

### Table: FavoritePlayers

![pic5](https://github.com/armon222/MIST-4600/assets/62662242/86afdfff-ea42-45f9-8c53-c0c962726be9)

### Table: Managers

![pic6](https://github.com/armon222/MIST-4600/assets/62662242/85c83a57-ec2b-4035-ab38-e3509f972bbd)

### Table: Sponsors

![pic7](https://github.com/armon222/MIST-4600/assets/62662242/7dc9d16c-751e-45b6-a85f-e28a25d93cf5)

### Table: Sponsorships

![pic8](https://github.com/armon222/MIST-4600/assets/62662242/94eebddd-b633-4102-97e9-17ae9c8612da)

### Table: Stadium

![pic9](https://github.com/armon222/MIST-4600/assets/62662242/f80f3059-4634-4298-a400-e488a8bd35a0)

### Table: Youth Academy

![pic10](https://github.com/armon222/MIST-4600/assets/62662242/7fce634d-265c-45cc-b0cf-3a3e30915597)

### Table: Players

![pic11](https://github.com/armon222/MIST-4600/assets/62662242/1b2ea803-7e92-4b70-b4af-e6d48c3b7b4d)

### Table: Injuries

![pic12](https://github.com/armon222/MIST-4600/assets/62662242/5d854cae-84c0-41e2-8acb-94ffb3d35ea3)

### Table: Manager_has_Coaches

![pic13](https://github.com/armon222/MIST-4600/assets/62662242/3a3f87a9-520e-4c90-a9ad-dca1066eb144)

## Queries

### Feature Matrix

![image matrix](https://github.com/armon222/MIST-4600/assets/148259051/51953ddf-b6d2-4383-b79d-37e64e7b5263)


### Query 1

Query lists the injuries players on the Lions have suffered playing at their home field. 

![project query 1](https://github.com/armon222/MIST-4600/assets/148259051/ccc9fa81-952e-47d2-80b1-7607d7da29b7)


Query one allows the managers to see the number and type of injuries occurring to players on the Lions' home field. This shows potential dangers that might arise from the design or texture of the playing surface. This query influences managers' decisions on how to design the field in the future, as well as lets the medical and training staff better prepare for injuries that may occur during a game

### Query 2

Query 2 lists the favorite players of fans who are from the United States. The query concatenates the player's first and last name, and results are ordered by the player's first and last name descending.

![query 2 project A](https://github.com/armon222/MIST-4600/assets/148259051/c4475963-4a50-4612-82e9-d394a8e73d0e)


Query 2 allows the managers to see who the most popular players on the team are who are from the United States. This is particularly important since the Lions play in Georgia and the American players might be more marketable to the fans. Seeing this information might help the management team figure out which players to use in community events or to promote the team locally. 

### Query 3

Query 3 lists the Fan's first and last name, email address, and amount spent on team merchandise that are season ticket holders.

![query3project](https://github.com/armon222/MIST-4600/assets/148259051/e371f086-192c-4e1b-b34a-477c71db9491)



Query 3 shows the management team the new Fans of the team and their contact information. This is valuable information because the team now can further contact these Fans with more deals and ways to get them into more games. The Lions also know how much they spend on Merchandise, so they can specifically offer them deals related to the cost of items they tend to purchase. 

### Query 4

Query 4 lists the player's first and last name, and the type of injury sustained only for players who have scored higher than the average amount of goals on the team. 

![query 4 project](https://github.com/armon222/MIST-4600/assets/148259051/989b39d1-48a5-488e-bf66-53bfe64d7493)


Query 4 is very important for the coaching staff because this shows the types of injuries being suffered by the team's best scoring threats. The organization needs to know what type of injuries these players sustained, so they figure out how long they need to be replaced. This information is also important to the medical staff so they can properly treat these players to get back on the field as soon as possible.

### Query 5

Query 5 lists player's last name and the average of the sum of player's goals and assists (points). The average is only listed if it is greater than the average points for the team. 

![query 5 project](https://github.com/armon222/MIST-4600/assets/148259051/97a0752f-3287-45fe-b67a-9c585d6bae41)


Query 5 shows the coaching staff which players produce the most offense for the team. This information is valuable for strategic purposes, because when the team needs a goal the coaching staff knows these players have the best chance to create offense. This query is also good for evaluating player value when players are negotiating new salaries for contracts. 

### Query 6

Query 6 shows the manager's last name, manager's role in the front office, and the average salary of the manager in the front office.

![query 6 project15](https://github.com/armon222/MIST-4600/assets/148259051/18f9bd65-2442-4c3e-a5be-1d0884e09138)

Query 6 illustrates the value of the top executives to the team. This information could help decision-making when deciding a manager's salary down the line or a comparable to new manager salaries when they are hiring. The numbers listed above can serve as a baseline for negotiations between ownership and the managers.

### Query 7

Query 7 lists the first and last name for players that have not been injured yet this season. 

![q7p](https://github.com/armon222/MIST-4600/assets/148259051/919f2979-6cfb-4b9f-aa33-3747a204a370)


Query 7 allows management to determine which players have been the most durable to the team, which helps assess the value of the player to the team. This can be important when the player and team negotiate a salary for future contracts because if the player is durable and avoids getting hurt they bring more value to the team. Query 7 is also valuable to the medical staff because they can see how the players listed above manage to stay healthy and on the field.

### Query 8 

Query 8 lists the company name, match opponent, and the average company contract amount with the club. The average amount has to be greater than 1,000,000.

![query 8 project](https://github.com/armon222/MIST-4600/assets/148259051/d8c6e7c1-9854-4c25-ab19-e2c46ed7bef1)


Query 8 shows the major sponsors of the club. The club has some smaller sponsors as well, so the having clause makes the average be at least one million to show the major company sponsors. This information helps the Lions prioritize their highest-value customers and prepare for the match dates where they are sponsors. 

### Query 9 

Query 9 lists the match result and match opponent for matches in the Lions' home stadium.

![query 9 proj](https://github.com/armon222/MIST-4600/assets/148259051/585f2b6a-f25e-4724-84ed-640bd750614a)


Query 9 is important to the organization because it illustrates how the team is performing on the home field. Even though these matches are worth the same as away games in the standings, these games are more important because our Fans pay good money to attend the games and we want to put on a winning product for them. So it's very important to win lots of games at home to appease the fans, sponsors, and management. 

### Query 10

Query 10 lists the player's last name, player position, coaching role, and the average amount of yellow cards for each player. This information is only shown if the player has an average amount of yellow cards greater or equal to 1.

![query 10 project](https://github.com/armon222/MIST-4600/assets/148259051/fe423fa2-a737-443f-a296-04f8be887752)

Query 10 demonstrates which players are getting the most yellow cards, and which coach is their position coach. Query 10 is a good way to evaluate which players are the most undisciplined, so the coaching staff can try to help the player fix this issue. Query 10 also shows which coach has the most undisciplined players, which implies this coach may need to change their tactics. Query 10 is also a good tool for player evaluation, especially when negotiating player salaries.

## Database Information

Name of the database: cs_g4p1

Additional information: Each query listed above is marked in the database using stored procedures which can be called using the following format: CALL TP_Q1();
