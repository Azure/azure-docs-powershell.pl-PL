---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 99be70e225dd607c580c4571f4ae332e7badf33a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191034"
---
# <span data-ttu-id="dcc8c-101">New-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="dcc8c-101">New-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="dcc8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dcc8c-102">SYNOPSIS</span></span>
<span data-ttu-id="dcc8c-103">To polecenie tworzy nową grupę trybu failover wystąpienia usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="dcc8c-103">This command creates a new Azure SQL Database Instance Failover Group.</span></span>

## <span data-ttu-id="dcc8c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="dcc8c-104">SYNTAX</span></span>

```
New-AzSqlDatabaseInstanceFailoverGroup [-Name] <String> [-PartnerResourceGroupName <String>]
 -PartnerRegion <String> -PrimaryManagedInstanceName <String> -PartnerManagedInstanceName <String>
 [-PartnerSubscriptionId <String>] [-FailoverPolicy <String>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <String>] [-ResourceGroupName] <String> [-Location] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcc8c-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="dcc8c-105">DESCRIPTION</span></span>
<span data-ttu-id="dcc8c-106">Tworzy nową grupę trybu failover wystąpienia usługi Azure SQL Database między określonymi regionami przy użyciu pary zanotowanego wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="dcc8c-106">Creates a new Azure SQL Database Instance Failover Group between the specified regions with the noted Managed Instance pair.</span></span>

<span data-ttu-id="dcc8c-107">W witrynie Name.SqlDataBaseDnsSuffix (na przykład Name.database.windows.net) i Name.secondary.SqlDataBaseDnsSuffix są tworzone dwa punkty końcowe TDS usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="dcc8c-107">Two Azure SQL Database TDS endpoints are created at Name.SqlDatabaseDnsSuffix (for example, Name.database.windows.net) and Name.secondary.SqlDatabaseDnsSuffix.</span></span> <span data-ttu-id="dcc8c-108">Te punkty końcowe mogą być używane do łączenia się odpowiednio z regionami podstawowymi i pomocniczmi grupy trybu failover.</span><span class="sxs-lookup"><span data-stu-id="dcc8c-108">These endpoints may be used to connect to the primary and secondary regions of the Failover Group, respectively.</span></span> <span data-ttu-id="dcc8c-109">Jeśli na region podstawowy ma wpływ awarii, zostanie wyzwolona automatyczna funkcja trybu failover dla punktów końcowych i baz danych zgodnie z zasadami grupy trybu failover wystąpienia i okresem prolongaty.</span><span class="sxs-lookup"><span data-stu-id="dcc8c-109">If the primary region is affected by an outage, automatic failover of the endpoints and databases will be triggered as dictated by the Instance Failover Group's failover policy and grace period.</span></span>

<span data-ttu-id="dcc8c-110">Podczas podglądu funkcji Grupy wystąpienia trybu failover dla parametru "-GracePeriodWithDataLossHours" są obsługiwane tylko wartości większe niż lub równe 1 godzinę.</span><span class="sxs-lookup"><span data-stu-id="dcc8c-110">During preview of the Instance Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="dcc8c-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="dcc8c-111">EXAMPLES</span></span>

### <span data-ttu-id="dcc8c-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="dcc8c-112">Example 1</span></span>
```powershell
C:\> $failoverGroup = New-AzSqlDatabaseInstanceFailoverGroup -Name fgName -Location location -ResourceGroupName rg -PrimaryManagedInstanceName $managedInstance.Name -PartnerRegion $partnerRegion -PartnerManagedInstanceName $partnerManagedInstance.Name -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
Output:
ResourceGroupName                     : rg
Location                              : East US
Name                                  : fg
PartnerResourceGroupName              : rg
PartnerRegion                         : West US
PrimaryManagedInstanceName            : managedInstance1
PartnerManagedInstanceName            : managedInstance2
ReplicationRole                       : Primary
ReplicationState                      : CATCH_UP
ReadWriteFailoverPolicy               : Automatic
FailoverWithDataLossGracePeriodHours  : 1
ReadOnlyFailoverPolicy                : Disabled
Id                                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/rg/providers/Microsoft.Sql/locations/eastus/instanceFailoverGroups/fg
```

<span data-ttu-id="dcc8c-113">To polecenie tworzy nową grupę trybu failover wystąpienia z zasadami trybu failover "Automatic" dla pary Zarządzane wystąpienie.</span><span class="sxs-lookup"><span data-stu-id="dcc8c-113">This command creates a new Instance Failover Group with failover policy 'Automatic' for the Managed Instance pair.</span></span>

### <span data-ttu-id="dcc8c-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="dcc8c-114">Example 2</span></span>
```powershell
C:\> $failoverGroup = New-AzSqlDatabaseInstanceFailoverGroup -Name fgName -Location location -ResourceGroupName rg -PrimaryManagedInstanceName $managedInstance.Name -PartnerRegion $partnerRegion -PartnerManagedInstanceName $partnerManagedInstance.Name -FailoverPolicy Manual
Output:
ResourceGroupName                     : rg
Location                              : East US
Name                                  : fg
PartnerResourceGroupName              : rg
PartnerRegion                         : West US
PrimaryManagedInstanceName            : managedInstance1
PartnerManagedInstanceName            : managedInstance2
ReplicationRole                       : Primary
ReplicationState                      : CATCH_UP
ReadWriteFailoverPolicy               : Manual
FailoverWithDataLossGracePeriodHours  : 
ReadOnlyFailoverPolicy                : Disabled
Id                                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/rg/providers/Microsoft.Sql/locations/eastus/instanceFailoverGroups/fg
```

<span data-ttu-id="dcc8c-115">To polecenie tworzy nową grupę wystąpienia trybu failover z zasadą trybu failover "Ręcznie" dla pary Wystąpienie zarządzane.</span><span class="sxs-lookup"><span data-stu-id="dcc8c-115">This command creates a new Instance Failover Group with failover policy 'Manual' for the Managed Instance pair.</span></span>

### <span data-ttu-id="dcc8c-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="dcc8c-116">Example 3</span></span>

<span data-ttu-id="dcc8c-117">To polecenie tworzy nową grupę trybu failover wystąpienia usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="dcc8c-117">This command creates a new Azure SQL Database Instance Failover Group.</span></span> <span data-ttu-id="dcc8c-118">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="dcc8c-118">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzSqlDatabaseInstanceFailoverGroup -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1 -Location location -Name fgName -PartnerManagedInstanceName $partnerManagedInstance.Name -PartnerRegion $partnerRegion -PartnerResourceGroupName rg2 -PrimaryManagedInstanceName $managedInstance.Name -ResourceGroupName rg
```

## <span data-ttu-id="dcc8c-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dcc8c-119">PARAMETERS</span></span>

### <span data-ttu-id="dcc8c-120">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="dcc8c-120">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="dcc8c-121">Określa, czy podczas awarii na serwerze pomocniczym ma być wyzwalana automatyczna funkcja trybu failover punktu końcowego tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="dcc8c-121">Whether an outage on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>

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

### <span data-ttu-id="dcc8c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcc8c-122">-DefaultProfile</span></span>
<span data-ttu-id="dcc8c-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="dcc8c-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dcc8c-124">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="dcc8c-124">-FailoverPolicy</span></span>
<span data-ttu-id="dcc8c-125">Zasady trybu failover grupy trybu failover wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="dcc8c-125">The failover policy of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="dcc8c-126">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="dcc8c-126">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="dcc8c-127">Interwał przed zainicjowanym automatycznym trybem failover, jeśli na serwerze podstawowym wystąpi przerwa w pracy, a trybu failover nie można ukończyć bez utraty danych.</span><span class="sxs-lookup"><span data-stu-id="dcc8c-127">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcc8c-128">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="dcc8c-128">-Location</span></span>
<span data-ttu-id="dcc8c-129">Nazwa regionu lokalnego, z którego ma zostać pobrana grupa trybu failover wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="dcc8c-129">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcc8c-130">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="dcc8c-130">-Name</span></span>
<span data-ttu-id="dcc8c-131">Nazwa grupy trybu failover bazy danych Azure SQL Database do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="dcc8c-131">The name of the Azure SQL Database Failover Group to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcc8c-132">-PartnerManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="dcc8c-132">-PartnerManagedInstanceName</span></span>
<span data-ttu-id="dcc8c-133">Nazwa wystąpienia zarządzanego w regionie partnerskim, które ma zostać dodane do grupy trybu failover wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="dcc8c-133">The name of the Managed Instance in the partner region to be added to the Instance Failover Group.</span></span>

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

### <span data-ttu-id="dcc8c-134">-PartnerRegion</span><span class="sxs-lookup"><span data-stu-id="dcc8c-134">-PartnerRegion</span></span>
<span data-ttu-id="dcc8c-135">Nazwa regionu partnerskiego grupy trybu failover wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="dcc8c-135">The name of the partner region of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="dcc8c-136">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcc8c-136">-PartnerResourceGroupName</span></span>
<span data-ttu-id="dcc8c-137">Nazwa grupy zasobów pomocniczych grupy Wystąpienie trybu failover.</span><span class="sxs-lookup"><span data-stu-id="dcc8c-137">The name of the secondary resource group of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="dcc8c-138">-PartnerSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dcc8c-138">-PartnerSubscriptionId</span></span>
<span data-ttu-id="dcc8c-139">Identyfikator subskrypcji pomocniczego zarządzanego wystąpienia grupy trybu failover wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="dcc8c-139">The subscription id of the secondary Managed Instance of the Instance Failover Group.</span></span> <span data-ttu-id="dcc8c-140">Ten parametr jest potrzebny tylko do konfiguracji między subskrypcjami</span><span class="sxs-lookup"><span data-stu-id="dcc8c-140">This parameter is only needed for cross-subscription setup</span></span>

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

### <span data-ttu-id="dcc8c-141">-PrimaryManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="dcc8c-141">-PrimaryManagedInstanceName</span></span>
<span data-ttu-id="dcc8c-142">Nazwa wystąpienia zarządzanego w regionie lokalnym, które ma zostać dodane do grupy trybu failover wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="dcc8c-142">The name of the Managed Instance in the local region to be added to the Instance Failover Group.</span></span>

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

### <span data-ttu-id="dcc8c-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcc8c-143">-ResourceGroupName</span></span>
<span data-ttu-id="dcc8c-144">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="dcc8c-144">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcc8c-145">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dcc8c-145">-Confirm</span></span>
<span data-ttu-id="dcc8c-146">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="dcc8c-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcc8c-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcc8c-147">-WhatIf</span></span>
<span data-ttu-id="dcc8c-148">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dcc8c-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dcc8c-149">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="dcc8c-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcc8c-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcc8c-150">CommonParameters</span></span>
<span data-ttu-id="dcc8c-151">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcc8c-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcc8c-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dcc8c-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcc8c-153">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dcc8c-153">INPUTS</span></span>

### <span data-ttu-id="dcc8c-154">System.String</span><span class="sxs-lookup"><span data-stu-id="dcc8c-154">System.String</span></span>

## <span data-ttu-id="dcc8c-155">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dcc8c-155">OUTPUTS</span></span>

### <span data-ttu-id="dcc8c-156">Microsoft.Azure.Commands.sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="dcc8c-156">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="dcc8c-157">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="dcc8c-157">NOTES</span></span>

## <span data-ttu-id="dcc8c-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dcc8c-158">RELATED LINKS</span></span>
