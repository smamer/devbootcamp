DROP TABLE IF EXISTS [Tavern];
CREATE TABLE [Tavern](
    ID INT IDENTITY(1,1),
    TavernName varchar(250)
    FloorCount INT
    OwnerID INT
    LocationID INT
);
INSERT INTO [Tavern] (ID,TavernName,FloorCount,OwnerID,LocationID)
VALUES (1,Excelsior,5,1,1)
INSERT INTO [Tavern] (ID,TavernName,FloorCount,OwnerID,LocationID)
VALUES (2,Summit,5,2,2)
INSERT INTO [Tavern] (ID,TavernName,FloorCount,OwnerID,LocationID)
VALUES (3,Final Sleep,4,3,3)
INSERT INTO [Tavern] (ID,TavernName,FloorCount,OwnerID,LocationID)
VALUES (4,Stay Inn,5,4,4)
INSERT INTO [Tavern] (ID,TavernName,FloorCount,OwnerID,LocationID)
VALUES (5,Hotel Motel,5,5,5)
DROP TABLE IF EXISTS [Users];
CREATE TABLE [Users](
    ID INT IDENTITY(1,1)
    Name varchar(250)
    Role
)