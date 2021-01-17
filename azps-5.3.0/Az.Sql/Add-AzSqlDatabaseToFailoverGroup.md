---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqldatabasetofailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlDatabaseToFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlDatabaseToFailoverGroup.md
ms.openlocfilehash: 7577809134987bd1a0092e28170d5bf25ccac04e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375608"
---
# <span data-ttu-id="3f7df-101">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="3f7df-101">Add-AzSqlDatabaseToFailoverGroup</span></span>

## <span data-ttu-id="3f7df-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3f7df-102">SYNOPSIS</span></span>
<span data-ttu-id="3f7df-103">Dodaje co najmniej jeden bazę danych do grupy trybu failover bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="3f7df-103">Adds one or more databases to an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="3f7df-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3f7df-104">SYNTAX</span></span>

```
Add-AzSqlDatabaseToFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f7df-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3f7df-105">DESCRIPTION</span></span>
<span data-ttu-id="3f7df-106">Dodaje co najmniej jeden bazę danych na serwerze podstawowym grupy usługi Azure SQL Database failover do tej grupy trybu failover.</span><span class="sxs-lookup"><span data-stu-id="3f7df-106">Adds one or more databases on a Azure SQL Database Failover Group's primary server to that Failover Group.</span></span> <span data-ttu-id="3f7df-107">Bazy danych nie mogą być pomocniczymi bazami danych w istniejących relacjach replikacji.</span><span class="sxs-lookup"><span data-stu-id="3f7df-107">The databases must not be secondary databases in existing replication relationships.</span></span> <span data-ttu-id="3f7df-108">Polecenie rozpocznie replikację geograficzną wszystkich dodanych baz danych na serwerze pomocniczym grupy trybu failover.</span><span class="sxs-lookup"><span data-stu-id="3f7df-108">The command will start geo-replication of any added databases to the Failover Group's secondary server.</span></span>
<span data-ttu-id="3f7df-109">Aby uzyskać obiekty bazy danych, do których ma zostać wypełniony parametr "-Database", użyj (na przykład) polecenia cmdlet Get-AzSqlDatabase.</span><span class="sxs-lookup"><span data-stu-id="3f7df-109">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzSqlDatabase cmdlet.</span></span>
<span data-ttu-id="3f7df-110">Aby wykonać polecenie, należy użyć głównego serwera grupy pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="3f7df-110">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="3f7df-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3f7df-111">EXAMPLES</span></span>

### <span data-ttu-id="3f7df-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3f7df-112">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Add-AzSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="3f7df-113">To polecenie umożliwia dodanie jednej bazy danych do grupy trybu failover przez przejście do niej.</span><span class="sxs-lookup"><span data-stu-id="3f7df-113">This command adds one database to a Failover Group by piping it in.</span></span>

### <span data-ttu-id="3f7df-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="3f7df-114">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Add-AzSqlDatabaseToFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzSqlDatabase)
```

<span data-ttu-id="3f7df-115">To polecenie dodaje wszystkie bazy danych z serwera do grupy trybu failover.</span><span class="sxs-lookup"><span data-stu-id="3f7df-115">This command adds all databases in a server to a Failover Group.</span></span>

### <span data-ttu-id="3f7df-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="3f7df-116">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Add-AzSqlDatabaseToFailoverGroup -Database $databases
```

<span data-ttu-id="3f7df-117">To polecenie dodaje wszystkie bazy danych z elastycznej puli do grupy trybu failover.</span><span class="sxs-lookup"><span data-stu-id="3f7df-117">This command adds all databases in an Elastic Pool to a Failover Group.</span></span>

## <span data-ttu-id="3f7df-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3f7df-118">PARAMETERS</span></span>

### <span data-ttu-id="3f7df-119">-Database</span><span class="sxs-lookup"><span data-stu-id="3f7df-119">-Database</span></span>
<span data-ttu-id="3f7df-120">Co najmniej jedna baza danych SQL Azure na serwerze podstawowym grupy trybu failover do dodania do grupy trybu failover.</span><span class="sxs-lookup"><span data-stu-id="3f7df-120">One or more Azure SQL Databases on the Failover Group's primary server to be added to the Failover Group.</span></span>

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

### <span data-ttu-id="3f7df-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f7df-121">-DefaultProfile</span></span>
<span data-ttu-id="3f7df-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="3f7df-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3f7df-123">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="3f7df-123">-FailoverGroupName</span></span>
<span data-ttu-id="3f7df-124">Nazwa grupy praca awaryjna bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="3f7df-124">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="3f7df-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f7df-125">-ResourceGroupName</span></span>
<span data-ttu-id="3f7df-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3f7df-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="3f7df-127">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="3f7df-127">-ServerName</span></span>
<span data-ttu-id="3f7df-128">Nazwa podstawowego serwera bazy danych SQL usługi Azure w grupie trybu failover.</span><span class="sxs-lookup"><span data-stu-id="3f7df-128">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="3f7df-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f7df-129">CommonParameters</span></span>
<span data-ttu-id="3f7df-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f7df-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f7df-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3f7df-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f7df-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3f7df-132">INPUTS</span></span>

### <span data-ttu-id="3f7df-133">System. String</span><span class="sxs-lookup"><span data-stu-id="3f7df-133">System.String</span></span>

### <span data-ttu-id="3f7df-134">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseModel; Microsoft. Azure. PowerShell. cmdlets. SQL, Version = 1.3.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="3f7df-134">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.PowerShell.Cmdlets.Sql, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="3f7df-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3f7df-135">OUTPUTS</span></span>

### <span data-ttu-id="3f7df-136">Microsoft. Azure. Commands. SQL. failover. model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="3f7df-136">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="3f7df-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3f7df-137">NOTES</span></span>

## <span data-ttu-id="3f7df-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3f7df-138">RELATED LINKS</span></span>

[<span data-ttu-id="3f7df-139">Nowe — AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="3f7df-139">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="3f7df-140">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="3f7df-140">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="3f7df-141">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="3f7df-141">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="3f7df-142">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="3f7df-142">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="3f7df-143">Przełącznik-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="3f7df-143">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="3f7df-144">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="3f7df-144">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="3f7df-145">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="3f7df-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
