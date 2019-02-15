# Project-Analysis
SQL queries to execute the desired results

Task: 
1.a. A list of all property names and their property id’s for Owner Id: 1426.
SELECT OwnerId = 1426, PropertyName, PropertyId
FROM [dbo].[OwnerProperty]
INNER JOIN [dbo].[Occupied] ON OwnerProperty.OwnerId = Occupied.OwnerId

1.b. Display the current home value for each property in question a). 
SELECT OwnerId = 1426, PropertyName, Value
FROM [Keys].[dbo].[OwnerProperty]
INNER JOIN [dbo].[Occupied] ON OwnerProperty.OwnerId = Occupied.OwnerId
INNER JOIN [dbo].[PropertyHomeValue] ON OwnerProperty.PropertyId = PropertyHomeValue.PropertyId
