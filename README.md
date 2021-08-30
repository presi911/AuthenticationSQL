# AuthenticationSQL

-- --------------------------------------------------
-- Creating all tables
-- --------------------------------------------------

-- Creating table 'SEC_ROLE'
CREATE TABLE [dbo].[SEC_ROLE] (
    [ID] int IDENTITY(1,1) NOT NULL,
    [NAME] nvarchar(100)  NULL,
    [REMOVED] bit  NOT NULL,
    [DESCRIPTION] nvarchar(200)  NULL
);
GO

-- Creating table 'SEC_SESSION'
CREATE TABLE [dbo].[SEC_SESSION] (
    [ID] bigint IDENTITY(1,1) NOT NULL,
    [USERID] int  NOT NULL,
    [LOGIN_DATE] datetime  NOT NULL,
    [IP_ADDRESS] nvarchar(40)  NOT NULL,
    [TOKEN] nvarchar(100)  NOT NULL,
    [TOKEN_STATUS] bit  NOT NULL
);
GO

-- Creating table 'SEC_USER'
CREATE TABLE [dbo].[SEC_USER] (
    [ID] int IDENTITY(1,1) NOT NULL,
    [NAME] nvarchar(50)  NOT NULL,
    [LASTNAME] nvarchar(100)  NOT NULL,
    [DOCUMENT] nvarchar(50)  NOT NULL,
    [CELLPHONE] nvarchar(30)  NULL,
    [EMAIL] nvarchar(100)  NULL,
    [USER_PASSWORD] nvarchar(100)  NOT NULL,
    [REMOVED] bit  NOT NULL,
    [REMOVE_DATE] datetime  NULL,
    [CREATE_DATE] datetime  NOT NULL,
    [UPDATE_DATE] datetime  NULL,
    [REMOVE_USER_ID] int  NULL,
    [CREATE_USER_ID] int  NULL,
    [UPDATE_USER_ID] int  NULL,
    [CITY] nvarchar(100)  NULL
);
GO

-- Creating table 'SEC_USER_ROLE'
CREATE TABLE [dbo].[SEC_USER_ROLE] (
    [ID] int IDENTITY(1,1) NOT NULL,
    [USERID] int  NOT NULL,
    [ROLEID] int  NOT NULL
);
GO

serverinitial.database.windows.net
