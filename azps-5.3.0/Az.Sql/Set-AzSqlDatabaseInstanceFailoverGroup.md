---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: f8ac83b684718a6a2698fd1b304b85ffa1ae5d45
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489473"
---
# <span data-ttu-id="800a5-101">Set-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="800a5-101">Set-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="800a5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="800a5-102">SYNOPSIS</span></span>
<span data-ttu-id="800a5-103">Modyfikuje konfigurację grupy trybu failover wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="800a5-103">Modifies the configuration of an Instance Failover Group.</span></span>

## <span data-ttu-id="800a5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="800a5-104">SYNTAX</span></span>

### <span data-ttu-id="800a5-105">SetInstanceFailoverGroupDefaultSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="800a5-105">SetInstanceFailoverGroupDefaultSet (Default)</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-FailoverPolicy <String>] [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="800a5-106">SetInstanceFailoverGroupByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="800a5-106">SetInstanceFailoverGroupByResourceIdSet</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-FailoverPolicy <String>]
 [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="800a5-107">SetInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span><span class="sxs-lookup"><span data-stu-id="800a5-107">SetInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel>
 [-FailoverPolicy <String>] [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="800a5-108">Opis</span><span class="sxs-lookup"><span data-stu-id="800a5-108">DESCRIPTION</span></span>
<span data-ttu-id="800a5-109">To polecenie modyfikuje konfigurację grupy trybu failover wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="800a5-109">This command modifies the configuration of an Instance Failover Group.</span></span>

<span data-ttu-id="800a5-110">Aby wykonać polecenie, należy użyć głównego regionu grupy tryb failover.</span><span class="sxs-lookup"><span data-stu-id="800a5-110">The Instance Failover Group's primary region should be used to execute the command.</span></span>

<span data-ttu-id="800a5-111">Podczas wyświetlania podglądu funkcji grup pracy awaryjnej w parametrze "-GracePeriodWithDataLossHours" są obsługiwane tylko wartości większe niż lub równe 1 godzina.</span><span class="sxs-lookup"><span data-stu-id="800a5-111">During preview of the Instance Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="800a5-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="800a5-112">EXAMPLES</span></span>

### <span data-ttu-id="800a5-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="800a5-113">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Set-AzSqlDatabaseInstanceFailoverGroup -FailoverPolicy Manual
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

<span data-ttu-id="800a5-114">Ustawia zasady pracy awaryjnej grupy dla wystąpienia jako "ręczna" przez potok w grupie trybu failover.</span><span class="sxs-lookup"><span data-stu-id="800a5-114">Sets a Instance Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="800a5-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="800a5-115">PARAMETERS</span></span>

### <span data-ttu-id="800a5-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="800a5-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="800a5-117">Informacja o tym, czy w przypadku dzieci na serwerze pomocniczym powinna być wyzwalana automatyczna praca awaryjna punktu końcowego tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="800a5-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>

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

### <span data-ttu-id="800a5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="800a5-118">-DefaultProfile</span></span>
<span data-ttu-id="800a5-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="800a5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="800a5-120">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="800a5-120">-FailoverPolicy</span></span>
<span data-ttu-id="800a5-121">Zasady pracy awaryjnej w grupie praca awaryjna wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="800a5-121">The failover policy of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="800a5-122">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="800a5-122">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="800a5-123">Interwał przed zainicjowaniem automatycznej pracy awaryjnej, jeśli na serwerze podstawowym wystąpi awaria i nie można ukończyć pracy awaryjnej bez utraty danych.</span><span class="sxs-lookup"><span data-stu-id="800a5-123">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

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

### <span data-ttu-id="800a5-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="800a5-124">-InputObject</span></span>
<span data-ttu-id="800a5-125">Obiekt grupy trybu failover wystąpienia do ustawienia</span><span class="sxs-lookup"><span data-stu-id="800a5-125">The Instance Failover Group object to set</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel
Parameter Sets: SetInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="800a5-126">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="800a5-126">-Location</span></span>
<span data-ttu-id="800a5-127">Nazwa regionu lokalnego, z którego ma zostać pobrana Grupa wystąpienie trybu failover.</span><span class="sxs-lookup"><span data-stu-id="800a5-127">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFailoverGroupDefaultSet, SetInstanceFailoverGroupByResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="800a5-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="800a5-128">-Name</span></span>
<span data-ttu-id="800a5-129">Nazwa grupy tryb failover wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="800a5-129">The name of the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFailoverGroupDefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="800a5-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="800a5-130">-ResourceGroupName</span></span>
<span data-ttu-id="800a5-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="800a5-131">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFailoverGroupDefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="800a5-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="800a5-132">-ResourceId</span></span>
<span data-ttu-id="800a5-133">Identyfikator zasobu grupy trybu failover wystąpienia do ustawienia.</span><span class="sxs-lookup"><span data-stu-id="800a5-133">The Resource ID of the Instance Failover Group to set.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFailoverGroupByResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="800a5-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="800a5-134">-Confirm</span></span>
<span data-ttu-id="800a5-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="800a5-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="800a5-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="800a5-136">-WhatIf</span></span>
<span data-ttu-id="800a5-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="800a5-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="800a5-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="800a5-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="800a5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="800a5-139">CommonParameters</span></span>
<span data-ttu-id="800a5-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="800a5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="800a5-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="800a5-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="800a5-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="800a5-142">INPUTS</span></span>

### <span data-ttu-id="800a5-143">Microsoft. Azure. Commands. SQL. InstanceFailoverGroup. model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="800a5-143">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="800a5-144">System. String</span><span class="sxs-lookup"><span data-stu-id="800a5-144">System.String</span></span>

## <span data-ttu-id="800a5-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="800a5-145">OUTPUTS</span></span>

### <span data-ttu-id="800a5-146">Microsoft. Azure. Commands. SQL. InstanceFailoverGroup. model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="800a5-146">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="800a5-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="800a5-147">NOTES</span></span>

## <span data-ttu-id="800a5-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="800a5-148">RELATED LINKS</span></span>
