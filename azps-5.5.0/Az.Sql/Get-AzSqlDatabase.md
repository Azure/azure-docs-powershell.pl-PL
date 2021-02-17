---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0C8AC52C-4E70-493C-A299-79CE32EC5EF1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabase.md
ms.openlocfilehash: 4f90d6d0c33874750bf2f32ae7f65bf32457f63c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188106"
---
# <span data-ttu-id="5ac17-101">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5ac17-101">Get-AzSqlDatabase</span></span>

## <span data-ttu-id="5ac17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ac17-102">SYNOPSIS</span></span>
<span data-ttu-id="5ac17-103">Pobiera jedną lub więcej baz danych.</span><span class="sxs-lookup"><span data-stu-id="5ac17-103">Gets one or more databases.</span></span>

## <span data-ttu-id="5ac17-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5ac17-104">SYNTAX</span></span>

```
Get-AzSqlDatabase [[-DatabaseName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ac17-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="5ac17-105">DESCRIPTION</span></span>
<span data-ttu-id="5ac17-106">Polecenie **cmdlet Get-AzSqlDatabase** pobiera jedną lub więcej baz danych Azure SQL z serwera Azure SQL Database Server.</span><span class="sxs-lookup"><span data-stu-id="5ac17-106">The **Get-AzSqlDatabase** cmdlet gets one or more Azure SQL databases from an Azure SQL Database Server.</span></span>
<span data-ttu-id="5ac17-107">To polecenie cmdlet jest również obsługiwane przez usługę SQL Server Stretch Database na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="5ac17-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="5ac17-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5ac17-108">EXAMPLES</span></span>

### <span data-ttu-id="5ac17-109">Przykład 1. Uzyskiwanie wszystkich baz danych na serwerze</span><span class="sxs-lookup"><span data-stu-id="5ac17-109">Example 1: Get all databases on a server</span></span>
```
PS C:\>Get-AzSqlDatabase -ResourceGroupName "resourcegroup01" -ServerName "server01"
ResourceGroupName             : resourcegroup01
ServerName                    : server01
DatabaseName                  : master
Location                      : Central US
DatabaseId                    : a2a7f2db-7526-4d86-a7b2-36276ee10dc6
Edition                       : None
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              : 
MaxSizeBytes                  : 5368709120
Status                        : Online
CreationDate                  : 7/3/2015 7:32:44 AM
CurrentServiceObjectiveId     : c99ac918-dbea-463f-a475-16ec020fdc12
CurrentServiceObjectiveName   : System1
RequestedServiceObjectiveId   : c99ac918-dbea-463f-a475-16ec020fdc12
RequestedServiceObjectiveName : 
ElasticPoolName               : 
EarliestRestoreDate           : 
Tags                          : 

ResourceGroupName             : resourcegroup01
ServerName                    : server01
DatabaseName                  : database01
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              : 
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 7/3/2015 7:33:37 AM
CurrentServiceObjectiveId     : f1173c43-91bd-4aaa-973c-54e79e15235b
CurrentServiceObjectiveName   : S0
RequestedServiceObjectiveId   : f1173c43-91bd-4aaa-973c-54e79e15235b
RequestedServiceObjectiveName : 
ElasticPoolName               : 
EarliestRestoreDate           : 
Tags                          :
```

<span data-ttu-id="5ac17-110">To polecenie pobiera wszystkie bazy danych na serwerze o nazwie serwer01.</span><span class="sxs-lookup"><span data-stu-id="5ac17-110">This command gets all databases on the server named server01.</span></span>

### <span data-ttu-id="5ac17-111">Przykład 2. Uzyskiwanie bazy danych według nazwy na serwerze</span><span class="sxs-lookup"><span data-stu-id="5ac17-111">Example 2: Get a database by name on a server</span></span>
```
PS C:\>Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database02"
ResourceGroupName             : resourcegroup01
ServerName                    : server01
DatabaseName                  : database02
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              : 
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 7/3/2015 7:33:37 AM
CurrentServiceObjectiveId     : f1173c43-91bd-4aaa-973c-54e79e15235b
CurrentServiceObjectiveName   : S0
RequestedServiceObjectiveId   : f1173c43-91bd-4aaa-973c-54e79e15235b
RequestedServiceObjectiveName : 
ElasticPoolName               : 
EarliestRestoreDate           : 
Tags                          :
```

<span data-ttu-id="5ac17-112">To polecenie pobiera bazę danych o nazwie Database02 z serwera o nazwie Serwer01.</span><span class="sxs-lookup"><span data-stu-id="5ac17-112">This command gets a database named Database02 from a server named Server01.</span></span>

### <span data-ttu-id="5ac17-113">Przykład 3. Uzyskiwanie wszystkich baz danych na serwerze przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="5ac17-113">Example 3: Get all databases on a server using filtering</span></span>
```
PS C:\> Get-AzSqlDatabase -ResourceGroupName "resourcegroup01" -ServerName "server01" -DatabaseName "database*"
ResourceGroupName             : resourcegroup01
ServerName                    : server01
DatabaseName                  : database01
Location                      : Central US
DatabaseId                    : a2a7f2db-7526-4d86-a7b2-36276ee10dc6
Edition                       : None
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              : 
MaxSizeBytes                  : 5368709120
Status                        : Online
CreationDate                  : 7/3/2015 7:32:44 AM
CurrentServiceObjectiveId     : c99ac918-dbea-463f-a475-16ec020fdc12
CurrentServiceObjectiveName   : System1
RequestedServiceObjectiveId   : c99ac918-dbea-463f-a475-16ec020fdc12
RequestedServiceObjectiveName : 
ElasticPoolName               : 
EarliestRestoreDate           : 
Tags                          : 

ResourceGroupName             : resourcegroup01
ServerName                    : server01
DatabaseName                  : database02
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              : 
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 7/3/2015 7:33:37 AM
CurrentServiceObjectiveId     : f1173c43-91bd-4aaa-973c-54e79e15235b
CurrentServiceObjectiveName   : S0
RequestedServiceObjectiveId   : f1173c43-91bd-4aaa-973c-54e79e15235b
RequestedServiceObjectiveName : 
ElasticPoolName               : 
EarliestRestoreDate           : 
Tags                          :
```

<span data-ttu-id="5ac17-114">To polecenie pobiera wszystkie bazy danych na serwerze o nazwie serwer01, które zaczynają się od "bazy danych".</span><span class="sxs-lookup"><span data-stu-id="5ac17-114">This command gets all databases on the server named server01 that start with "database".</span></span>

## <span data-ttu-id="5ac17-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ac17-115">PARAMETERS</span></span>

### <span data-ttu-id="5ac17-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5ac17-116">-DatabaseName</span></span>
<span data-ttu-id="5ac17-117">Określa nazwę bazy danych do pobrania.</span><span class="sxs-lookup"><span data-stu-id="5ac17-117">Specifies the name of the database to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ac17-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ac17-118">-DefaultProfile</span></span>
<span data-ttu-id="5ac17-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="5ac17-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ac17-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ac17-120">-ResourceGroupName</span></span>
<span data-ttu-id="5ac17-121">Określa nazwę grupy zasobów, do której jest przypisany serwer bazy danych.</span><span class="sxs-lookup"><span data-stu-id="5ac17-121">Specifies the name of the resource group to which the database server is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ac17-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5ac17-122">-ServerName</span></span>
<span data-ttu-id="5ac17-123">Określa nazwę serwera, do którego jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="5ac17-123">Specifies the name of the server to which the database is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ac17-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5ac17-124">-Confirm</span></span>
<span data-ttu-id="5ac17-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5ac17-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ac17-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ac17-126">-WhatIf</span></span>
<span data-ttu-id="5ac17-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ac17-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ac17-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5ac17-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ac17-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ac17-129">CommonParameters</span></span>
<span data-ttu-id="5ac17-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ac17-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ac17-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5ac17-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ac17-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5ac17-132">INPUTS</span></span>

### <span data-ttu-id="5ac17-133">System.String</span><span class="sxs-lookup"><span data-stu-id="5ac17-133">System.String</span></span>

## <span data-ttu-id="5ac17-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5ac17-134">OUTPUTS</span></span>

### <span data-ttu-id="5ac17-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="5ac17-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="5ac17-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5ac17-136">NOTES</span></span>

## <span data-ttu-id="5ac17-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5ac17-137">RELATED LINKS</span></span>

[<span data-ttu-id="5ac17-138">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5ac17-138">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="5ac17-139">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5ac17-139">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="5ac17-140">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5ac17-140">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="5ac17-141">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5ac17-141">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="5ac17-142">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5ac17-142">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)


