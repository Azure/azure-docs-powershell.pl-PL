---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 04ed033559abe6fe6a60922f7b11a498ff4026bc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93887397"
---
# <span data-ttu-id="ad933-101">New-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ad933-101">New-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="ad933-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ad933-102">SYNOPSIS</span></span>
<span data-ttu-id="ad933-103">To polecenie tworzy nową grupę trybu failover wystąpienia bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="ad933-103">This command creates a new Azure SQL Database Instance Failover Group.</span></span>

## <span data-ttu-id="ad933-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ad933-104">SYNTAX</span></span>

```
New-AzSqlDatabaseInstanceFailoverGroup -Name <String> [-PartnerResourceGroupName <String>] [-PartnerSubscriptionId <String>]
 -PartnerRegion <String> -PrimaryManagedInstanceName <String> -PartnerManagedInstanceName <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-ResourceGroupName] <String>
 [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad933-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ad933-105">DESCRIPTION</span></span>
<span data-ttu-id="ad933-106">Umożliwia utworzenie nowej grupy trybu failover wystąpienia bazy danych SQL platformy Azure między określonymi regionami z zanotowaną parą wystąpień zarządzanych.</span><span class="sxs-lookup"><span data-stu-id="ad933-106">Creates a new Azure SQL Database Instance Failover Group between the specified regions with the noted Managed Instance pair.</span></span>

<span data-ttu-id="ad933-107">W programie Name. SqlDatabaseDnsSuffix (na przykład Name.database.windows.net) i Name. Data. SqlDatabaseDnsSuffix nie są tworzone dwa punkty końcowe TDS bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="ad933-107">Two Azure SQL Database TDS endpoints are created at Name.SqlDatabaseDnsSuffix (for example, Name.database.windows.net) and Name.secondary.SqlDatabaseDnsSuffix.</span></span> <span data-ttu-id="ad933-108">Te punkty końcowe mogą być używane do nawiązywania połączeń z podstawowym i pomocniczym regionem grupy trybu failover.</span><span class="sxs-lookup"><span data-stu-id="ad933-108">These endpoints may be used to connect to the primary and secondary regions of the Failover Group, respectively.</span></span> <span data-ttu-id="ad933-109">Jeśli na podstawowym regionie wpłynie awaria, automatyczna praca awaryjna punktów końcowych i baz danych zostanie wyzwolona jako podyktowana przez zasady pracy awaryjnej grupy awaryjnej wystąpienia oraz okres prolongaty.</span><span class="sxs-lookup"><span data-stu-id="ad933-109">If the primary region is affected by an outage, automatic failover of the endpoints and databases will be triggered as dictated by the Instance Failover Group's failover policy and grace period.</span></span>

<span data-ttu-id="ad933-110">Podczas wyświetlania podglądu funkcji grup pracy awaryjnej w parametrze "-GracePeriodWithDataLossHours" są obsługiwane tylko wartości większe niż lub równe 1 godzina.</span><span class="sxs-lookup"><span data-stu-id="ad933-110">During preview of the Instance Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="ad933-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ad933-111">EXAMPLES</span></span>

### <span data-ttu-id="ad933-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ad933-112">Example 1</span></span>
```
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

<span data-ttu-id="ad933-113">To polecenie tworzy nową grupę trybu failover wystąpienia z zasadami trybu failover "automatyczna" dla pary zarządzanych wystąpień.</span><span class="sxs-lookup"><span data-stu-id="ad933-113">This command creates a new Instance Failover Group with failover policy 'Automatic' for the Managed Instance pair.</span></span>

### <span data-ttu-id="ad933-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="ad933-114">Example 2</span></span>
```
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

<span data-ttu-id="ad933-115">To polecenie tworzy nową grupę trybu failover wystąpienia z zasadami pracy awaryjnej dla pary zarządzanych wystąpień.</span><span class="sxs-lookup"><span data-stu-id="ad933-115">This command creates a new Instance Failover Group with failover policy 'Manual' for the Managed Instance pair.</span></span>

## <span data-ttu-id="ad933-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ad933-116">PARAMETERS</span></span>

### <span data-ttu-id="ad933-117">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="ad933-117">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="ad933-118">Czy awaria na serwerze pomocniczym powinna wyzwalać automatyczną pracę awaryjną punktu końcowego tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="ad933-118">Whether an outage on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>
<span data-ttu-id="ad933-119">Ta funkcja nie jest jeszcze obsługiwana.</span><span class="sxs-lookup"><span data-stu-id="ad933-119">This feature is not yet supported.</span></span>

```yaml
Type: AllowReadOnlyFailoverToPrimary
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad933-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad933-120">-DefaultProfile</span></span>
<span data-ttu-id="ad933-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ad933-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad933-122">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="ad933-122">-FailoverPolicy</span></span>
<span data-ttu-id="ad933-123">Zasady pracy awaryjnej w grupie praca awaryjna wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="ad933-123">The failover policy of the Instance Failover Group.</span></span>

```yaml
Type: FailoverPolicy
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad933-124">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="ad933-124">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="ad933-125">Interwał przed zainicjowaniem automatycznej pracy awaryjnej, jeśli na serwerze podstawowym wystąpi awaria i nie można ukończyć pracy awaryjnej bez utraty danych.</span><span class="sxs-lookup"><span data-stu-id="ad933-125">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad933-126">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ad933-126">-Location</span></span>
<span data-ttu-id="ad933-127">Nazwa regionu lokalnego, z którego ma zostać pobrana Grupa wystąpienie trybu failover.</span><span class="sxs-lookup"><span data-stu-id="ad933-127">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad933-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ad933-128">-Name</span></span>
<span data-ttu-id="ad933-129">Nazwa grupy trybu failover bazy danych SQL Azure do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="ad933-129">The name of the Azure SQL Database Failover Group to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad933-130">-PartnerManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="ad933-130">-PartnerManagedInstanceName</span></span>
<span data-ttu-id="ad933-131">Nazwa wystąpienia zarządzanego w regionie partnerskim, które ma zostać dodane do grupy wystąpienie trybu failover.</span><span class="sxs-lookup"><span data-stu-id="ad933-131">The name of the Managed Instance in the partner region to be added to the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad933-132">-PartnerRegion</span><span class="sxs-lookup"><span data-stu-id="ad933-132">-PartnerRegion</span></span>
<span data-ttu-id="ad933-133">Nazwa regionu partnera w grupie praca awaryjna wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="ad933-133">The name of the partner region of the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad933-134">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad933-134">-PartnerResourceGroupName</span></span>
<span data-ttu-id="ad933-135">Nazwa grupy pomocniczej zasobu w grupie praca awaryjna wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="ad933-135">The name of the secondary resource group of the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad933-136">-PartnerSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ad933-136">-PartnerSubscriptionId</span></span>
<span data-ttu-id="ad933-137">Identyfikator subskrypcji pomocniczego wystąpienia zarządzanego grupy trybu failover wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="ad933-137">The subscription id of the secondary Managed Instance of the Instance Failover Group.</span></span> <span data-ttu-id="ad933-138">Ten parametr jest potrzebny tylko w przypadku konfiguracji abonamentu krzyżowego</span><span class="sxs-lookup"><span data-stu-id="ad933-138">This parameter is only needed for cross-subscription setup</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad933-139">-PrimaryManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="ad933-139">-PrimaryManagedInstanceName</span></span>
<span data-ttu-id="ad933-140">Nazwa wystąpienia zarządzanego w regionie lokalnym, które ma zostać dodane do grupy wystąpienie trybu failover.</span><span class="sxs-lookup"><span data-stu-id="ad933-140">The name of the Managed Instance in the local region to be added to the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad933-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad933-141">-ResourceGroupName</span></span>
<span data-ttu-id="ad933-142">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ad933-142">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad933-143">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ad933-143">-Confirm</span></span>
<span data-ttu-id="ad933-144">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad933-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad933-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad933-145">-WhatIf</span></span>
<span data-ttu-id="ad933-146">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad933-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad933-147">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ad933-147">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad933-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad933-148">CommonParameters</span></span>
<span data-ttu-id="ad933-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad933-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad933-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad933-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad933-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ad933-151">INPUTS</span></span>

### <span data-ttu-id="ad933-152">System. String</span><span class="sxs-lookup"><span data-stu-id="ad933-152">System.String</span></span>

## <span data-ttu-id="ad933-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ad933-153">OUTPUTS</span></span>

### <span data-ttu-id="ad933-154">Microsoft. Azure. Commands. SQL. InstanceFailoverGroup. model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="ad933-154">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="ad933-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ad933-155">NOTES</span></span>

## <span data-ttu-id="ad933-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ad933-156">RELATED LINKS</span></span>
