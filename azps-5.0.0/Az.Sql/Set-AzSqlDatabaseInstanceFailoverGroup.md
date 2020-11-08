---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 79d7482d51ffc7c03703dbf62e00fd9230f9976d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234250"
---
# <span data-ttu-id="f70df-101">Set-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f70df-101">Set-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="f70df-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f70df-102">SYNOPSIS</span></span>
<span data-ttu-id="f70df-103">Modyfikuje konfigurację grupy trybu failover wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="f70df-103">Modifies the configuration of an Instance Failover Group.</span></span>

## <span data-ttu-id="f70df-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f70df-104">SYNTAX</span></span>

### <span data-ttu-id="f70df-105">SetInstanceFailoverGroupDefaultSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f70df-105">SetInstanceFailoverGroupDefaultSet (Default)</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-FailoverPolicy <String>] [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f70df-106">SetInstanceFailoverGroupByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f70df-106">SetInstanceFailoverGroupByResourceIdSet</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-FailoverPolicy <String>]
 [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f70df-107">SetInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span><span class="sxs-lookup"><span data-stu-id="f70df-107">SetInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel>
 [-FailoverPolicy <String>] [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f70df-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f70df-108">DESCRIPTION</span></span>
<span data-ttu-id="f70df-109">To polecenie modyfikuje konfigurację grupy trybu failover wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="f70df-109">This command modifies the configuration of an Instance Failover Group.</span></span>

<span data-ttu-id="f70df-110">Aby wykonać polecenie, należy użyć głównego regionu grupy tryb failover.</span><span class="sxs-lookup"><span data-stu-id="f70df-110">The Instance Failover Group's primary region should be used to execute the command.</span></span>

<span data-ttu-id="f70df-111">Podczas wyświetlania podglądu funkcji grup pracy awaryjnej w parametrze "-GracePeriodWithDataLossHours" są obsługiwane tylko wartości większe niż lub równe 1 godzina.</span><span class="sxs-lookup"><span data-stu-id="f70df-111">During preview of the Instance Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="f70df-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f70df-112">EXAMPLES</span></span>

### <span data-ttu-id="f70df-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f70df-113">Example 1</span></span>
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

<span data-ttu-id="f70df-114">Ustawia zasady pracy awaryjnej grupy dla wystąpienia jako "ręczna" przez potok w grupie trybu failover.</span><span class="sxs-lookup"><span data-stu-id="f70df-114">Sets a Instance Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="f70df-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f70df-115">PARAMETERS</span></span>

### <span data-ttu-id="f70df-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="f70df-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="f70df-117">Informacja o tym, czy w przypadku dzieci na serwerze pomocniczym powinna być wyzwalana automatyczna praca awaryjna punktu końcowego tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="f70df-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>
<span data-ttu-id="f70df-118">Ta funkcja nie jest jeszcze obsługiwana.</span><span class="sxs-lookup"><span data-stu-id="f70df-118">This feature is not yet supported.</span></span>

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

### <span data-ttu-id="f70df-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f70df-119">-DefaultProfile</span></span>
<span data-ttu-id="f70df-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f70df-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f70df-121">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="f70df-121">-FailoverPolicy</span></span>
<span data-ttu-id="f70df-122">Zasady pracy awaryjnej w grupie praca awaryjna wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="f70df-122">The failover policy of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="f70df-123">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="f70df-123">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="f70df-124">Interwał przed zainicjowaniem automatycznej pracy awaryjnej, jeśli na serwerze podstawowym wystąpi awaria i nie można ukończyć pracy awaryjnej bez utraty danych.</span><span class="sxs-lookup"><span data-stu-id="f70df-124">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

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

### <span data-ttu-id="f70df-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f70df-125">-InputObject</span></span>
<span data-ttu-id="f70df-126">Obiekt grupy trybu failover wystąpienia do ustawienia</span><span class="sxs-lookup"><span data-stu-id="f70df-126">The Instance Failover Group object to set</span></span>

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

### <span data-ttu-id="f70df-127">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f70df-127">-Location</span></span>
<span data-ttu-id="f70df-128">Nazwa regionu lokalnego, z którego ma zostać pobrana Grupa wystąpienie trybu failover.</span><span class="sxs-lookup"><span data-stu-id="f70df-128">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

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

### <span data-ttu-id="f70df-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f70df-129">-Name</span></span>
<span data-ttu-id="f70df-130">Nazwa grupy tryb failover wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="f70df-130">The name of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="f70df-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f70df-131">-ResourceGroupName</span></span>
<span data-ttu-id="f70df-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f70df-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="f70df-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f70df-133">-ResourceId</span></span>
<span data-ttu-id="f70df-134">Identyfikator zasobu grupy trybu failover wystąpienia do ustawienia.</span><span class="sxs-lookup"><span data-stu-id="f70df-134">The Resource ID of the Instance Failover Group to set.</span></span>

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

### <span data-ttu-id="f70df-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f70df-135">-Confirm</span></span>
<span data-ttu-id="f70df-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f70df-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f70df-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f70df-137">-WhatIf</span></span>
<span data-ttu-id="f70df-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f70df-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f70df-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f70df-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f70df-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f70df-140">CommonParameters</span></span>
<span data-ttu-id="f70df-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f70df-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f70df-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f70df-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f70df-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f70df-143">INPUTS</span></span>

### <span data-ttu-id="f70df-144">Microsoft. Azure. Commands. SQL. InstanceFailoverGroup. model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="f70df-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="f70df-145">System. String</span><span class="sxs-lookup"><span data-stu-id="f70df-145">System.String</span></span>

## <span data-ttu-id="f70df-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f70df-146">OUTPUTS</span></span>

### <span data-ttu-id="f70df-147">Microsoft. Azure. Commands. SQL. InstanceFailoverGroup. model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="f70df-147">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="f70df-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f70df-148">NOTES</span></span>

## <span data-ttu-id="f70df-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f70df-149">RELATED LINKS</span></span>
