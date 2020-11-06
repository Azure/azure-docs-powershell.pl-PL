---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/add-azurermsqldatabasetofailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlDatabaseToFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlDatabaseToFailoverGroup.md
ms.openlocfilehash: c195215bb38152287e1aa65457a5a0ff4b5452cf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546416"
---
# <span data-ttu-id="ba489-101">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ba489-101">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>

## <span data-ttu-id="ba489-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ba489-102">SYNOPSIS</span></span>
<span data-ttu-id="ba489-103">Dodaje co najmniej jeden bazę danych do grupy trybu failover bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="ba489-103">Adds one or more databases to an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba489-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ba489-104">SYNTAX</span></span>

```
Add-AzureRmSqlDatabaseToFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba489-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ba489-105">DESCRIPTION</span></span>
<span data-ttu-id="ba489-106">Dodaje co najmniej jeden bazę danych na serwerze podstawowym grupy usługi Azure SQL Database failover do tej grupy trybu failover.</span><span class="sxs-lookup"><span data-stu-id="ba489-106">Adds one or more databases on a Azure SQL Database Failover Group's primary server to that Failover Group.</span></span> <span data-ttu-id="ba489-107">Bazy danych nie mogą być pomocniczymi bazami danych w istniejących relacjach replikacji.</span><span class="sxs-lookup"><span data-stu-id="ba489-107">The databases must not be secondary databases in existing replication relationships.</span></span> <span data-ttu-id="ba489-108">Polecenie rozpocznie replikację geograficzną wszystkich dodanych baz danych na serwerze pomocniczym grupy trybu failover.</span><span class="sxs-lookup"><span data-stu-id="ba489-108">The command will start geo-replication of any added databases to the Failover Group's secondary server.</span></span>
<span data-ttu-id="ba489-109">Aby uzyskać obiekty bazy danych, do których ma zostać wypełniony parametr "-Database", użyj (na przykład) polecenia cmdlet Get-AzureRmSqlDatabase.</span><span class="sxs-lookup"><span data-stu-id="ba489-109">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzureRmSqlDatabase cmdlet.</span></span>
<span data-ttu-id="ba489-110">Aby wykonać polecenie, należy użyć głównego serwera grupy pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="ba489-110">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="ba489-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ba489-111">EXAMPLES</span></span>

### <span data-ttu-id="ba489-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ba489-112">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="ba489-113">To polecenie umożliwia dodanie jednej bazy danych do grupy trybu failover przez przejście do niej.</span><span class="sxs-lookup"><span data-stu-id="ba489-113">This command adds one database to a Failover Group by piping it in.</span></span>

### <span data-ttu-id="ba489-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="ba489-114">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzureRmSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Add-AzureRmSqlDatabaseToFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzureRmSqlDatabase)
```

<span data-ttu-id="ba489-115">To polecenie dodaje wszystkie bazy danych z serwera do grupy trybu failover.</span><span class="sxs-lookup"><span data-stu-id="ba489-115">This command adds all databases in a server to a Failover Group.</span></span>

### <span data-ttu-id="ba489-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="ba489-116">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzureRmSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Add-AzureRmSqlDatabaseToFailoverGroup -Database $databases
```

<span data-ttu-id="ba489-117">To polecenie dodaje wszystkie bazy danych z elastycznej puli do grupy trybu failover.</span><span class="sxs-lookup"><span data-stu-id="ba489-117">This command adds all databases in an Elastic Pool to a Failover Group.</span></span>

## <span data-ttu-id="ba489-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ba489-118">PARAMETERS</span></span>

### <span data-ttu-id="ba489-119">-Database</span><span class="sxs-lookup"><span data-stu-id="ba489-119">-Database</span></span>
<span data-ttu-id="ba489-120">Co najmniej jedna baza danych SQL Azure na serwerze podstawowym grupy trybu failover do dodania do grupy trybu failover.</span><span class="sxs-lookup"><span data-stu-id="ba489-120">One or more Azure SQL Databases on the Failover Group's primary server to be added to the Failover Group.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba489-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba489-121">-DefaultProfile</span></span>
<span data-ttu-id="ba489-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ba489-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba489-123">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="ba489-123">-FailoverGroupName</span></span>
<span data-ttu-id="ba489-124">Nazwa grupy praca awaryjna bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="ba489-124">The name of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba489-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba489-125">-ResourceGroupName</span></span>
<span data-ttu-id="ba489-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ba489-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="ba489-127">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="ba489-127">-ServerName</span></span>
<span data-ttu-id="ba489-128">Nazwa podstawowego serwera bazy danych SQL usługi Azure w grupie trybu failover.</span><span class="sxs-lookup"><span data-stu-id="ba489-128">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="ba489-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba489-129">CommonParameters</span></span>
<span data-ttu-id="ba489-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba489-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba489-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba489-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba489-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ba489-132">INPUTS</span></span>

### <span data-ttu-id="ba489-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ba489-133">System.String</span></span>

### <span data-ttu-id="ba489-134">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseModel; Microsoft. Azure. Commands. SQL, Version = 4.11.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ba489-134">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.Commands.Sql, Version=4.11.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ba489-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ba489-135">OUTPUTS</span></span>

### <span data-ttu-id="ba489-136">Microsoft. Azure. Commands. SQL. failover. model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="ba489-136">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="ba489-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ba489-137">NOTES</span></span>

## <span data-ttu-id="ba489-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ba489-138">RELATED LINKS</span></span>

[<span data-ttu-id="ba489-139">Nowe — AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ba489-139">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="ba489-140">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ba489-140">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="ba489-141">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ba489-141">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="ba489-142">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ba489-142">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="ba489-143">Przełącznik-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ba489-143">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="ba489-144">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ba489-144">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="ba489-145">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="ba489-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
