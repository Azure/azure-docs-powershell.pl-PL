---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 94f4448816bc7cf60272f602caafbf5be6f1a3f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994911"
---
# <span data-ttu-id="72de4-101">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="72de4-101">Set-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="72de4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72de4-102">SYNOPSIS</span></span>
<span data-ttu-id="72de4-103">Modyfikuje konfigurację grupy trybu failover bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="72de4-103">Modifies the configuration of an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="72de4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="72de4-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72de4-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="72de4-105">DESCRIPTION</span></span>
<span data-ttu-id="72de4-106">To polecenie modyfikuje konfigurację grupy trybu failover usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="72de4-106">This command modifies the configuration of an Azure SQL Database Failover Group.</span></span>
<span data-ttu-id="72de4-107">Do wykonania polecenia należy użyć serwera podstawowego grupy trybu failover.</span><span class="sxs-lookup"><span data-stu-id="72de4-107">The Failover Group's primary server should be used to execute the command.</span></span>
<span data-ttu-id="72de4-108">Aby kontrolować zestaw baz danych w grupie, użyj zamiast tego "Add-AzSqlDatabaseToFailoverGroup" i "Remove-AzSqlDatabaseFromFailoverGroup".</span><span class="sxs-lookup"><span data-stu-id="72de4-108">To control the set of databases in the group, use 'Add-AzSqlDatabaseToFailoverGroup' and 'Remove-AzSqlDatabaseFromFailoverGroup' instead.</span></span>
<span data-ttu-id="72de4-109">Podczas podglądu funkcji Grupy trybu failover dla parametru "-GracePeriodWithDataLossHours" są obsługiwane tylko wartości większe niż lub równe 1 godzinie.</span><span class="sxs-lookup"><span data-stu-id="72de4-109">During preview of the Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="72de4-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="72de4-110">EXAMPLES</span></span>

### <span data-ttu-id="72de4-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="72de4-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Set-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="72de4-112">Ustawia zasady trybu failover grupy trybu failover na "Automatyczne".</span><span class="sxs-lookup"><span data-stu-id="72de4-112">Sets a Failover Group's failover policy to 'Automatic.'</span></span>

### <span data-ttu-id="72de4-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="72de4-113">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg | Set-AzSqlDatabaseFailoverGroup -FailoverPolicy Manual
```

<span data-ttu-id="72de4-114">Ustawia zasady trybu failover grupy trybu failover na wartość "Ręcznie", korzystając z funkcji rurowych w grupie trybu failover.</span><span class="sxs-lookup"><span data-stu-id="72de4-114">Sets a Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="72de4-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="72de4-115">PARAMETERS</span></span>

### <span data-ttu-id="72de4-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="72de4-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="72de4-117">Określa, czy usługi awarii na serwerze pomocniczym powinny wyzwalać automatyczne trybu failover punktu końcowego tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="72de4-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AllowReadOnlyFailoverToPrimary
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72de4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72de4-118">-DefaultProfile</span></span>
<span data-ttu-id="72de4-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="72de4-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72de4-120">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="72de4-120">-FailoverGroupName</span></span>
<span data-ttu-id="72de4-121">Nazwa grupy trybu failover usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="72de4-121">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="72de4-122">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="72de4-122">-FailoverPolicy</span></span>
<span data-ttu-id="72de4-123">Zasady trybu failover grupy trybu failover usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="72de4-123">The failover policy of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.FailoverGroup.Model.FailoverPolicy
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: Automatic
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72de4-124">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="72de4-124">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="72de4-125">Interwał przed zainicjowanym automatycznym trybem failover w przypadku awarii na serwerze podstawowym.</span><span class="sxs-lookup"><span data-stu-id="72de4-125">Interval before automatic failover is initiated if an outage occurs on the primary server.</span></span> <span data-ttu-id="72de4-126">Oznacza to, że usługa Azure SQL Database nie rozpocznie automatycznego trybu failover przed upływem okresu prolongaty.</span><span class="sxs-lookup"><span data-stu-id="72de4-126">This indicates that Azure SQL Database will not initiate automatic failover before the grace period expires.</span></span> <span data-ttu-id="72de4-127">Pamiętaj, że operacja trybu failover z opcją AllowDataLoss może spowodować utratę danych ze względu na rodzaj asynchronicznej synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="72de4-127">Please note that failover operation with AllowDataLoss option might cause data loss due to the nature of asynchronous synchronization.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72de4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72de4-128">-ResourceGroupName</span></span>
<span data-ttu-id="72de4-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="72de4-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="72de4-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="72de4-130">-ServerName</span></span>
<span data-ttu-id="72de4-131">Nazwa podstawowego serwera usługi Azure SQL Database Server grupy trybu failover.</span><span class="sxs-lookup"><span data-stu-id="72de4-131">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="72de4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72de4-132">CommonParameters</span></span>
<span data-ttu-id="72de4-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72de4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72de4-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="72de4-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72de4-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="72de4-135">INPUTS</span></span>

### <span data-ttu-id="72de4-136">System.String</span><span class="sxs-lookup"><span data-stu-id="72de4-136">System.String</span></span>

## <span data-ttu-id="72de4-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="72de4-137">OUTPUTS</span></span>

### <span data-ttu-id="72de4-138">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="72de4-138">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="72de4-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="72de4-139">NOTES</span></span>

## <span data-ttu-id="72de4-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="72de4-140">RELATED LINKS</span></span>

[<span data-ttu-id="72de4-141">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="72de4-141">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="72de4-142">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="72de4-142">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="72de4-143">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="72de4-143">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="72de4-144">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="72de4-144">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="72de4-145">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="72de4-145">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="72de4-146">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="72de4-146">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="72de4-147">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="72de4-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
