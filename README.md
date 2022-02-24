DROP TABLE IF EXISTS [Tavern];
CREATE TABLE [Tavern](
    TavernID INT IDENTITY(1, 1),
    TavernName varchar(250),
    FloorCount INT,
    OwnerID INT,
    LocationID INT
);

INSERT INTO [Tavern] 
VALUES (1,Excelsior,5,1,1)
INSERT INTO [Tavern] 
VALUES (2,Summit,5,2,2)
INSERT INTO [Tavern]
VALUES (3,Final Sleep,4,3,3)
INSERT INTO [Tavern]
VALUES (4,Stay Inn,5,4,4)
INSERT INTO [Tavern]
VALUES (5,Hotel Motel,5,5,5)

DROP TABLE IF EXISTS [Users];
CREATE TABLE [Users](
    ID INT IDENTITY(1,1),
    UserName varchar(250),
    Role varchar(25)
);

INSERT INTO [Users]
VALUES 

DROP TABLE IF EXISTS [Supplies];
CREATE TABLE [Supplies](
    SupplyID INT IDENTITY(1, 1),
    Unit varchar(250),
    SupplyName varchar(250)
);

DROP TABLE IF EXISTS [Inventory];
CREATE TABLE [Inventory](
    SupplyID INT IDENTITY(1, 1),
    TavernID INT,
    DateOfInventory DATETIME,
    Quantity INT
);

DROP TABLE IF EXISTS [GoodsReceived];
CREATE TABLE [GoodsReceived](
    SupplyID INT IDENTITY(1, 1),
    TavernID INT,
    Cost INT,
    Amount INT,
    Date DATETIME
);

DROP TABLE IF EXISTS [Services];
CREATE TABLE [Services](
    ServiceID INT IDENTITY(1, 1),
    ServiceName varchar(250),
    StatusID INT
);

DROP TABLE IF EXISTS [ServiceStatus];
CREATE TABLE [ServiceStatus](
    StatusID INT IDENTITY(1, 1),
    Status varchar(250)
);

DROP TABLE IF EXISTS [Sales];
CREATE TABLE [Sales](
    ServiceID INT IDENTITY(1, 1),
    Guest varchar(250),
    Price INT,
    DatePurchased DATETIME,
    AmountPurchased INT,
    TavernID INT
);