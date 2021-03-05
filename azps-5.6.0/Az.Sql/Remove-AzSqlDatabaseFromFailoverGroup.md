---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqldatabasefromfailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFromFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFromFailoverGroup.md
ms.openlocfilehash: 556cece1b4fb22067918fb84dd1474c39d8c5aeb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961377"
---
# <span data-ttu-id="5b9f4-101">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5b9f4-101">Remove-AzSqlDatabaseFromFailoverGroup</span></span>

## <span data-ttu-id="5b9f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b9f4-102">SYNOPSIS</span></span>
<span data-ttu-id="5b9f4-103">Usuwa jedną lub więcej baz danych z grupy trybu failover usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="5b9f4-103">Removes one or more databases from an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="5b9f4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5b9f4-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseFromFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-Force] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5b9f4-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="5b9f4-105">DESCRIPTION</span></span>
<span data-ttu-id="5b9f4-106">Usuwa jedną lub więcej baz danych z określonej grupy trybu failover usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="5b9f4-106">Removes one or more databases from the specified Azure SQL Database Failover Group.</span></span> <span data-ttu-id="5b9f4-107">Bazy danych i relacje replikacji pozostają nienaruszone, ale nie będą już dostępne za pośrednictwem punktów końcowych grupy trybu failover.</span><span class="sxs-lookup"><span data-stu-id="5b9f4-107">The databases and replication relationships are left intact, but they will no longer be accessible through the Failover Group endpoints.</span></span>
<span data-ttu-id="5b9f4-108">Aby uzyskać obiekty bazy danych w celu wypełnienia parametru "-Database", użyj (na przykład) Get-AzSqlDatabase cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b9f4-108">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzSqlDatabase cmdlet.</span></span>
<span data-ttu-id="5b9f4-109">Aby wykonać to polecenie, należy użyć serwera podstawowego grupy trybu failover.</span><span class="sxs-lookup"><span data-stu-id="5b9f4-109">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="5b9f4-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5b9f4-110">EXAMPLES</span></span>

### <span data-ttu-id="5b9f4-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5b9f4-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Remove-AzSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="5b9f4-112">To polecenie usuwa jedną bazę danych z grupy trybu failover, rurując ją w.</span><span class="sxs-lookup"><span data-stu-id="5b9f4-112">This command removes one database from a Failover Group by piping it in.</span></span>

### <span data-ttu-id="5b9f4-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="5b9f4-113">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Remove-AzSqlDatabaseFromFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzSqlDatabase)
```

<span data-ttu-id="5b9f4-114">To polecenie usuwa wszystkie bazy danych z grupy trybu failover.</span><span class="sxs-lookup"><span data-stu-id="5b9f4-114">This command removes all databases from a Failover Group.</span></span>

### <span data-ttu-id="5b9f4-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="5b9f4-115">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Remove-AzSqlDatabaseFromFailoverGroup -Database $databases
```

<span data-ttu-id="5b9f4-116">To polecenie usuwa wszystkie bazy danych w elastycznej puli z grupy trybu failover.</span><span class="sxs-lookup"><span data-stu-id="5b9f4-116">This command removes all databases in an Elastic Pool from a Failover Group.</span></span>

## <span data-ttu-id="5b9f4-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b9f4-117">PARAMETERS</span></span>

### <span data-ttu-id="5b9f4-118">— Baza danych</span><span class="sxs-lookup"><span data-stu-id="5b9f4-118">-Database</span></span>
<span data-ttu-id="5b9f4-119">Co najmniej jedna baza danych Azure SQL Na serwerze podstawowym grupy trybu failover zostanie usunięta z grupy trybu failover.</span><span class="sxs-lookup"><span data-stu-id="5b9f4-119">One or more Azure SQL Databases on the Failover Group's primary server to be removed from the Failover Group.</span></span>

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

### <span data-ttu-id="5b9f4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b9f4-120">-DefaultProfile</span></span>
<span data-ttu-id="5b9f4-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="5b9f4-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5b9f4-122">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="5b9f4-122">-FailoverGroupName</span></span>
<span data-ttu-id="5b9f4-123">Nazwa grupy trybu failover usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="5b9f4-123">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="5b9f4-124">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="5b9f4-124">-Force</span></span>
<span data-ttu-id="5b9f4-125">Pomiń komunikat potwierdzenia wykonania akcji.</span><span class="sxs-lookup"><span data-stu-id="5b9f4-125">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="5b9f4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b9f4-126">-ResourceGroupName</span></span>
<span data-ttu-id="5b9f4-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5b9f4-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="5b9f4-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5b9f4-128">-ServerName</span></span>
<span data-ttu-id="5b9f4-129">Nazwa podstawowego serwera usługi Azure SQL Database Server grupy trybu failover.</span><span class="sxs-lookup"><span data-stu-id="5b9f4-129">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="5b9f4-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5b9f4-130">-Confirm</span></span>
<span data-ttu-id="5b9f4-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5b9f4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b9f4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b9f4-132">-WhatIf</span></span>
<span data-ttu-id="5b9f4-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b9f4-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5b9f4-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5b9f4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b9f4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b9f4-135">CommonParameters</span></span>
<span data-ttu-id="5b9f4-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b9f4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b9f4-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5b9f4-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b9f4-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5b9f4-138">INPUTS</span></span>

### <span data-ttu-id="5b9f4-139">System.String</span><span class="sxs-lookup"><span data-stu-id="5b9f4-139">System.String</span></span>

### <span data-ttu-id="5b9f4-140">System.Collections.generic.List'1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.PowerShell.Cmdlet.Sql, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="5b9f4-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.PowerShell.Cmdlets.Sql, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="5b9f4-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5b9f4-141">OUTPUTS</span></span>

### <span data-ttu-id="5b9f4-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="5b9f4-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="5b9f4-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5b9f4-143">NOTES</span></span>

## <span data-ttu-id="5b9f4-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5b9f4-144">RELATED LINKS</span></span>

[<span data-ttu-id="5b9f4-145">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5b9f4-145">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="5b9f4-146">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5b9f4-146">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="5b9f4-147">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5b9f4-147">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="5b9f4-148">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5b9f4-148">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="5b9f4-149">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5b9f4-149">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="5b9f4-150">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5b9f4-150">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="5b9f4-151">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="5b9f4-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
