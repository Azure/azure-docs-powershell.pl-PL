---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: be1f2fc5c0aa2abda5f036580e377f05b26c2eb2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976305"
---
# <span data-ttu-id="a7015-101">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a7015-101">New-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="a7015-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7015-102">SYNOPSIS</span></span>
<span data-ttu-id="a7015-103">To polecenie tworzy nową grupę trybu failover bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="a7015-103">This command creates a new Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="a7015-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a7015-104">SYNTAX</span></span>

```
New-AzSqlDatabaseFailoverGroup [-ServerName] <String> -FailoverGroupName <String>
 [-PartnerResourceGroupName <String>] -PartnerServerName <String> [-FailoverPolicy <FailoverPolicy>]
 [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7015-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a7015-105">DESCRIPTION</span></span>
<span data-ttu-id="a7015-106">Tworzy nową grupę trybu failover bazy danych Azure SQL Database dla określonych serwerów.</span><span class="sxs-lookup"><span data-stu-id="a7015-106">Creates a new Azure SQL Database Failover Group for the specified servers.</span></span>
<span data-ttu-id="a7015-107">Dwa punkty końcowe TDS usługi Azure SQL Database są tworzone w witrynie FailoverGroupName.SqlDatabaseDnsSuffix (na przykład FailoverGroupName.database.windows.net) i FailoverGroupName.secondary.SqlDatabaseDnsSuffix.</span><span class="sxs-lookup"><span data-stu-id="a7015-107">Two Azure SQL Database TDS endpoints are created at FailoverGroupName.SqlDatabaseDnsSuffix (for example, FailoverGroupName.database.windows.net) and FailoverGroupName.secondary.SqlDatabaseDnsSuffix.</span></span> <span data-ttu-id="a7015-108">Te punkty końcowe mogą być używane do łączenia się odpowiednio z serwerami podstawowymi i pomocniczmi w grupie trybu failover.</span><span class="sxs-lookup"><span data-stu-id="a7015-108">These endpoints may be used to connect to the primary and secondary servers in the Failover Group, respectively.</span></span> <span data-ttu-id="a7015-109">Jeśli na serwer podstawowy wpływa awarii, automatyczne trybu failover punktów końcowych i baz danych zostanie wyzwolone zgodnie z zasadami grupy trybu failover i okresem prolongaty.</span><span class="sxs-lookup"><span data-stu-id="a7015-109">If the primary server is affected by an outage, automatic failover of the endpoints and databases will be triggered as dictated by the Failover Group's failover policy and grace period.</span></span>
<span data-ttu-id="a7015-110">Nowo utworzone grupy trybu failover nie zawierają żadnych baz danych.</span><span class="sxs-lookup"><span data-stu-id="a7015-110">Newly created Failover Groups do not contain any databases.</span></span> <span data-ttu-id="a7015-111">Aby kontrolować zestaw baz danych w grupie trybu failover, użyj polecenia cmdlet "Add-AzSqlDatabaseToFailoverGroup" i "Remove-AzSqlDatabaseFromFailoverGroup".</span><span class="sxs-lookup"><span data-stu-id="a7015-111">To control the set of databases in a Failover Group, use the 'Add-AzSqlDatabaseToFailoverGroup' and 'Remove-AzSqlDatabaseFromFailoverGroup' cmdlets.</span></span>
<span data-ttu-id="a7015-112">Dla parametru "-GracePeriodWithDataLossHours" są obsługiwane tylko wartości większe niż lub równe 1 godzinie.</span><span class="sxs-lookup"><span data-stu-id="a7015-112">Only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="a7015-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a7015-113">EXAMPLES</span></span>

### <span data-ttu-id="a7015-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a7015-114">Example 1</span></span>
```
C:\> $failoverGroup = New-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -PartnerServerName secondaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="a7015-115">To polecenie tworzy nową grupę trybu failover z zasadami trybu failover "Automatic" dla dwóch serwerów w tej samej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="a7015-115">This command creates a new Failover Group with failover policy 'Automatic' for two servers in the same resource group.</span></span>

### <span data-ttu-id="a7015-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a7015-116">Example 2</span></span>
```
C:\> $failoverGroup = New-AzSqlDatabaseFailoverGroup -ResourceGroupName rg1 -ServerName primaryserver -PartnerResourceGroupName rg2 -PartnerServerName secondaryserver1 -FailoverGroupName fg -FailoverPolicy Manual
```

<span data-ttu-id="a7015-117">To polecenie tworzy nową grupę trybu failover z zasadami trybu failover "Ręczny" dla dwóch serwerów w różnych grupach zasobów.</span><span class="sxs-lookup"><span data-stu-id="a7015-117">This command creates a new Failover Group with failover policy 'Manual' for two servers in different resource groups.</span></span>

## <span data-ttu-id="a7015-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a7015-118">PARAMETERS</span></span>

### <span data-ttu-id="a7015-119">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="a7015-119">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="a7015-120">Określa, czy podczas awarii na serwerze pomocniczym ma być wyzwalana automatyczna funkcja trybu failover punktu końcowego tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="a7015-120">Whether an outage on the secondary server should trigger automatic failover of the read-only endpoint.</span></span> <span data-ttu-id="a7015-121">Ta funkcja nie jest jeszcze obsługiwana.</span><span class="sxs-lookup"><span data-stu-id="a7015-121">This feature is not yet supported.</span></span>

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

### <span data-ttu-id="a7015-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7015-122">-DefaultProfile</span></span>
<span data-ttu-id="a7015-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="a7015-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a7015-124">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="a7015-124">-FailoverGroupName</span></span>
<span data-ttu-id="a7015-125">Nazwa grupy trybu failover bazy danych Azure SQL Database do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="a7015-125">The name of the Azure SQL Database Failover Group to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7015-126">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="a7015-126">-FailoverPolicy</span></span>
<span data-ttu-id="a7015-127">Zasady trybu failover grupy trybu failover usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="a7015-127">The failover policy of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="a7015-128">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="a7015-128">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="a7015-129">Interwał przed zainicjowanym automatycznym trybem failover, jeśli na serwerze podstawowym wystąpi przerwa w awarii, a trybu failover nie można ukończyć bez utraty danych.</span><span class="sxs-lookup"><span data-stu-id="a7015-129">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

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

### <span data-ttu-id="a7015-130">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7015-130">-PartnerResourceGroupName</span></span>
<span data-ttu-id="a7015-131">Nazwa grupy zasobów pomocniczych grupy trybu failover usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="a7015-131">The name of the secondary resource group of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7015-132">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="a7015-132">-PartnerServerName</span></span>
<span data-ttu-id="a7015-133">Nazwa serwera pomocniczego grupy trybu failover usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="a7015-133">The name of the secondary server of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7015-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7015-134">-ResourceGroupName</span></span>
<span data-ttu-id="a7015-135">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a7015-135">The name of the resource group.</span></span>

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

### <span data-ttu-id="a7015-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a7015-136">-ServerName</span></span>
<span data-ttu-id="a7015-137">Nazwa podstawowego serwera usługi Azure SQL Database Server grupy trybu failover.</span><span class="sxs-lookup"><span data-stu-id="a7015-137">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="a7015-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7015-138">CommonParameters</span></span>
<span data-ttu-id="a7015-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7015-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7015-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a7015-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7015-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a7015-141">INPUTS</span></span>

### <span data-ttu-id="a7015-142">System.String</span><span class="sxs-lookup"><span data-stu-id="a7015-142">System.String</span></span>

## <span data-ttu-id="a7015-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a7015-143">OUTPUTS</span></span>

### <span data-ttu-id="a7015-144">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="a7015-144">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="a7015-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a7015-145">NOTES</span></span>

## <span data-ttu-id="a7015-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a7015-146">RELATED LINKS</span></span>

[<span data-ttu-id="a7015-147">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a7015-147">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="a7015-148">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a7015-148">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="a7015-149">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a7015-149">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="a7015-150">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a7015-150">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="a7015-151">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a7015-151">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="a7015-152">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a7015-152">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="a7015-153">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="a7015-153">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
