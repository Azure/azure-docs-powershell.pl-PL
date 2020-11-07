---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasefromfailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFromFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFromFailoverGroup.md
ms.openlocfilehash: 4a39cd97936ef72615e30072de1988304fc5ad09
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707825"
---
# <span data-ttu-id="7e037-101">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="7e037-101">Remove-AzSqlDatabaseFromFailoverGroup</span></span>

## <span data-ttu-id="7e037-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7e037-102">SYNOPSIS</span></span>
<span data-ttu-id="7e037-103">Usuwa co najmniej jeden z baz danych z grupy usługi Azure SQL Database failover.</span><span class="sxs-lookup"><span data-stu-id="7e037-103">Removes one or more databases from an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="7e037-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7e037-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseFromFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-Force] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7e037-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7e037-105">DESCRIPTION</span></span>
<span data-ttu-id="7e037-106">Usuwa co najmniej jeden z baz danych z określonej grupy usługi Azure SQL Database failover.</span><span class="sxs-lookup"><span data-stu-id="7e037-106">Removes one or more databases from the specified Azure SQL Database Failover Group.</span></span> <span data-ttu-id="7e037-107">Bazy danych i relacje replikacji pozostają nienaruszone, ale nie będą już dostępne w punktach końcowych grup pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="7e037-107">The databases and replication relationships are left intact, but they will no longer be accessible through the Failover Group endpoints.</span></span>
<span data-ttu-id="7e037-108">Aby uzyskać obiekty bazy danych, do których ma zostać wypełniony parametr "-Database", użyj (na przykład) polecenia cmdlet Get-AzSqlDatabase.</span><span class="sxs-lookup"><span data-stu-id="7e037-108">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzSqlDatabase cmdlet.</span></span>
<span data-ttu-id="7e037-109">Aby wykonać polecenie, należy użyć głównego serwera grupy pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="7e037-109">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="7e037-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7e037-110">EXAMPLES</span></span>

### <span data-ttu-id="7e037-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7e037-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Remove-AzSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="7e037-112">To polecenie umożliwia usunięcie jednej bazy danych z grupy trybu failover przez przejście do niej.</span><span class="sxs-lookup"><span data-stu-id="7e037-112">This command removes one database from a Failover Group by piping it in.</span></span>

### <span data-ttu-id="7e037-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="7e037-113">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Remove-AzSqlDatabaseFromFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzSqlDatabase)
```

<span data-ttu-id="7e037-114">To polecenie usuwa wszystkie bazy danych z grupy trybu failover.</span><span class="sxs-lookup"><span data-stu-id="7e037-114">This command removes all databases from a Failover Group.</span></span>

### <span data-ttu-id="7e037-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="7e037-115">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Remove-AzSqlDatabaseFromFailoverGroup -Database $databases
```

<span data-ttu-id="7e037-116">To polecenie usuwa wszystkie bazy danych z grupy elastycznej pracy w trybie failover.</span><span class="sxs-lookup"><span data-stu-id="7e037-116">This command removes all databases in an Elastic Pool from a Failover Group.</span></span>

## <span data-ttu-id="7e037-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7e037-117">PARAMETERS</span></span>

### <span data-ttu-id="7e037-118">-Database</span><span class="sxs-lookup"><span data-stu-id="7e037-118">-Database</span></span>
<span data-ttu-id="7e037-119">Co najmniej jedna baza danych SQL Azure na serwerze podstawowym grupy trybu failover do usunięcia z grupy trybu failover.</span><span class="sxs-lookup"><span data-stu-id="7e037-119">One or more Azure SQL Databases on the Failover Group's primary server to be removed from the Failover Group.</span></span>

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

### <span data-ttu-id="7e037-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e037-120">-DefaultProfile</span></span>
<span data-ttu-id="7e037-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="7e037-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7e037-122">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="7e037-122">-FailoverGroupName</span></span>
<span data-ttu-id="7e037-123">Nazwa grupy praca awaryjna bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="7e037-123">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="7e037-124">-Force</span><span class="sxs-lookup"><span data-stu-id="7e037-124">-Force</span></span>
<span data-ttu-id="7e037-125">Pomiń komunikat potwierdzający wykonanie akcji.</span><span class="sxs-lookup"><span data-stu-id="7e037-125">Skip confirmation message for performing the action.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e037-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e037-126">-ResourceGroupName</span></span>
<span data-ttu-id="7e037-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7e037-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="7e037-128">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="7e037-128">-ServerName</span></span>
<span data-ttu-id="7e037-129">Nazwa podstawowego serwera bazy danych SQL usługi Azure w grupie trybu failover.</span><span class="sxs-lookup"><span data-stu-id="7e037-129">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="7e037-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7e037-130">-Confirm</span></span>
<span data-ttu-id="7e037-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e037-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e037-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e037-132">-WhatIf</span></span>
<span data-ttu-id="7e037-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e037-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7e037-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7e037-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e037-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e037-135">CommonParameters</span></span>
<span data-ttu-id="7e037-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e037-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e037-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7e037-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e037-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7e037-138">INPUTS</span></span>

### <span data-ttu-id="7e037-139">System. String</span><span class="sxs-lookup"><span data-stu-id="7e037-139">System.String</span></span>

### <span data-ttu-id="7e037-140">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseModel; Microsoft. Azure. PowerShell. cmdlets. SQL, Version = 1.3.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="7e037-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.PowerShell.Cmdlets.Sql, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="7e037-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7e037-141">OUTPUTS</span></span>

### <span data-ttu-id="7e037-142">Microsoft. Azure. Commands. SQL. failover. model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="7e037-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="7e037-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7e037-143">NOTES</span></span>

## <span data-ttu-id="7e037-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7e037-144">RELATED LINKS</span></span>

[<span data-ttu-id="7e037-145">Nowe — AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="7e037-145">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="7e037-146">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="7e037-146">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="7e037-147">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="7e037-147">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="7e037-148">Dodaj-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="7e037-148">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="7e037-149">Przełącznik-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="7e037-149">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="7e037-150">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="7e037-150">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="7e037-151">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="7e037-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)