---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/set-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 3031878e30307cd5ff733de6177bc3c65c61a5bc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967329"
---
# <span data-ttu-id="ce985-101">Set-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ce985-101">Set-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="ce985-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce985-102">SYNOPSIS</span></span>
<span data-ttu-id="ce985-103">Modyfikuje konfigurację grupy trybu failover wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="ce985-103">Modifies the configuration of an Instance Failover Group.</span></span>

## <span data-ttu-id="ce985-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ce985-104">SYNTAX</span></span>

### <span data-ttu-id="ce985-105">SetInstanceFailoverGroupDefaultSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="ce985-105">SetInstanceFailoverGroupDefaultSet (Default)</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-FailoverPolicy <String>] [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce985-106">SetInstanceFailoverGroupByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ce985-106">SetInstanceFailoverGroupByResourceIdSet</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-FailoverPolicy <String>]
 [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce985-107">SetInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span><span class="sxs-lookup"><span data-stu-id="ce985-107">SetInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel>
 [-FailoverPolicy <String>] [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce985-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="ce985-108">DESCRIPTION</span></span>
<span data-ttu-id="ce985-109">To polecenie modyfikuje konfigurację grupy trybu failover wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="ce985-109">This command modifies the configuration of an Instance Failover Group.</span></span>

<span data-ttu-id="ce985-110">Do wykonania polecenia należy użyć podstawowego obszaru grupy trybu failover wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="ce985-110">The Instance Failover Group's primary region should be used to execute the command.</span></span>

<span data-ttu-id="ce985-111">Podczas podglądu funkcji Grupy wystąpienia trybu failover dla parametru "-GracePeriodWithDataLossHours" są obsługiwane tylko wartości większe niż lub równe 1 godzinę.</span><span class="sxs-lookup"><span data-stu-id="ce985-111">During preview of the Instance Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="ce985-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ce985-112">EXAMPLES</span></span>

### <span data-ttu-id="ce985-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ce985-113">Example 1</span></span>
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

<span data-ttu-id="ce985-114">Ustawia zasady trybu failover grupy trybu failover wystąpienia na wartość "Ręcznie", korzystając z funkcji rurowych w grupie trybu failover.</span><span class="sxs-lookup"><span data-stu-id="ce985-114">Sets a Instance Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="ce985-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ce985-115">PARAMETERS</span></span>

### <span data-ttu-id="ce985-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="ce985-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="ce985-117">Określa, czy usługi awarii na serwerze pomocniczym powinny wyzwalać automatyczne trybu failover punktu końcowego tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="ce985-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>

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

### <span data-ttu-id="ce985-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce985-118">-DefaultProfile</span></span>
<span data-ttu-id="ce985-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ce985-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce985-120">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="ce985-120">-FailoverPolicy</span></span>
<span data-ttu-id="ce985-121">Zasady trybu failover grupy trybu failover wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="ce985-121">The failover policy of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="ce985-122">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="ce985-122">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="ce985-123">Interwał przed zainicjowanym automatycznym trybem failover, jeśli na serwerze podstawowym wystąpi przerwa w awarii, a trybu failover nie można ukończyć bez utraty danych.</span><span class="sxs-lookup"><span data-stu-id="ce985-123">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

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

### <span data-ttu-id="ce985-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ce985-124">-InputObject</span></span>
<span data-ttu-id="ce985-125">Obiekt Grupy trybu failover wystąpienia, który należy ustawić</span><span class="sxs-lookup"><span data-stu-id="ce985-125">The Instance Failover Group object to set</span></span>

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

### <span data-ttu-id="ce985-126">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ce985-126">-Location</span></span>
<span data-ttu-id="ce985-127">Nazwa regionu lokalnego, z którego ma zostać pobrana grupa trybu failover wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="ce985-127">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

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

### <span data-ttu-id="ce985-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ce985-128">-Name</span></span>
<span data-ttu-id="ce985-129">Nazwa grupy wystąpienia trybu failover.</span><span class="sxs-lookup"><span data-stu-id="ce985-129">The name of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="ce985-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce985-130">-ResourceGroupName</span></span>
<span data-ttu-id="ce985-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ce985-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="ce985-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ce985-132">-ResourceId</span></span>
<span data-ttu-id="ce985-133">Identyfikator zasobu grupy trybu failover wystąpienia, który należy ustawić.</span><span class="sxs-lookup"><span data-stu-id="ce985-133">The Resource ID of the Instance Failover Group to set.</span></span>

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

### <span data-ttu-id="ce985-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ce985-134">-Confirm</span></span>
<span data-ttu-id="ce985-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ce985-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce985-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce985-136">-WhatIf</span></span>
<span data-ttu-id="ce985-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce985-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce985-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ce985-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce985-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce985-139">CommonParameters</span></span>
<span data-ttu-id="ce985-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce985-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce985-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ce985-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce985-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ce985-142">INPUTS</span></span>

### <span data-ttu-id="ce985-143">Microsoft.Azure.Commands.sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="ce985-143">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="ce985-144">System.String</span><span class="sxs-lookup"><span data-stu-id="ce985-144">System.String</span></span>

## <span data-ttu-id="ce985-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ce985-145">OUTPUTS</span></span>

### <span data-ttu-id="ce985-146">Microsoft.Azure.Commands.sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="ce985-146">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="ce985-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ce985-147">NOTES</span></span>

## <span data-ttu-id="ce985-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ce985-148">RELATED LINKS</span></span>
