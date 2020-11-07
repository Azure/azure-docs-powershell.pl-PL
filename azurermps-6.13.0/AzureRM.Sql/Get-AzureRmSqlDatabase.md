---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 0C8AC52C-4E70-493C-A299-79CE32EC5EF1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabase.md
ms.openlocfilehash: abe58faae0f0bd761cb532e47e1358129bc21998
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717362"
---
# <span data-ttu-id="b8865-101">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b8865-101">Get-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="b8865-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b8865-102">SYNOPSIS</span></span>
<span data-ttu-id="b8865-103">Pobiera co najmniej jeden z baz danych.</span><span class="sxs-lookup"><span data-stu-id="b8865-103">Gets one or more databases.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8865-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b8865-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabase [[-DatabaseName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8865-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b8865-105">DESCRIPTION</span></span>
<span data-ttu-id="b8865-106">Polecenie cmdlet **Get-AzureRmSqlDatabase** pobiera co najmniej jeden bazę danych SQL Azure z serwera bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="b8865-106">The **Get-AzureRmSqlDatabase** cmdlet gets one or more Azure SQL databases from an Azure SQL Database Server.</span></span>
<span data-ttu-id="b8865-107">To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="b8865-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="b8865-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b8865-108">EXAMPLES</span></span>

### <span data-ttu-id="b8865-109">Przykład 1: pobieranie wszystkich baz danych na serwerze</span><span class="sxs-lookup"><span data-stu-id="b8865-109">Example 1: Get all databases on a server</span></span>
```
PS C:\>Get-AzureRmSqlDatabase -ResourceGroupName "resourcegroup01" -ServerName "server01"
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

<span data-ttu-id="b8865-110">To polecenie pobiera wszystkie bazy danych na serwerze o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="b8865-110">This command gets all databases on the server named server01.</span></span>

### <span data-ttu-id="b8865-111">Przykład 2: uzyskiwanie bazy danych według nazwy na serwerze</span><span class="sxs-lookup"><span data-stu-id="b8865-111">Example 2: Get a database by name on a server</span></span>
```
PS C:\>Get-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database02"
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

<span data-ttu-id="b8865-112">To polecenie pobiera bazę danych o nazwie Database02 z serwera o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="b8865-112">This command gets a database named Database02 from a server named Server01.</span></span>

## <span data-ttu-id="b8865-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b8865-113">PARAMETERS</span></span>

### <span data-ttu-id="b8865-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b8865-114">-DatabaseName</span></span>
<span data-ttu-id="b8865-115">Określa nazwę bazy danych, którą należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="b8865-115">Specifies the name of the database to retrieve.</span></span>

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

### <span data-ttu-id="b8865-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8865-116">-DefaultProfile</span></span>
<span data-ttu-id="b8865-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b8865-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8865-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8865-118">-ResourceGroupName</span></span>
<span data-ttu-id="b8865-119">Określa nazwę grupy zasobów, do której jest przypisany serwer bazy danych.</span><span class="sxs-lookup"><span data-stu-id="b8865-119">Specifies the name of the resource group to which the database server is assigned.</span></span>

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

### <span data-ttu-id="b8865-120">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="b8865-120">-ServerName</span></span>
<span data-ttu-id="b8865-121">Określa nazwę serwera, do którego jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="b8865-121">Specifies the name of the server to which the database is assigned.</span></span>

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

### <span data-ttu-id="b8865-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b8865-122">-Confirm</span></span>
<span data-ttu-id="b8865-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8865-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8865-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8865-124">-WhatIf</span></span>
<span data-ttu-id="b8865-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8865-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8865-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b8865-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8865-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8865-127">CommonParameters</span></span>
<span data-ttu-id="b8865-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8865-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8865-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8865-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8865-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b8865-130">INPUTS</span></span>

### <span data-ttu-id="b8865-131">System. String</span><span class="sxs-lookup"><span data-stu-id="b8865-131">System.String</span></span>

## <span data-ttu-id="b8865-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b8865-132">OUTPUTS</span></span>

### <span data-ttu-id="b8865-133">Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="b8865-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="b8865-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b8865-134">NOTES</span></span>

## <span data-ttu-id="b8865-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b8865-135">RELATED LINKS</span></span>

[<span data-ttu-id="b8865-136">Nowe — AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b8865-136">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="b8865-137">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b8865-137">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="b8865-138">Życiorys — AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b8865-138">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="b8865-139">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b8865-139">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="b8865-140">Suspend — AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b8865-140">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

