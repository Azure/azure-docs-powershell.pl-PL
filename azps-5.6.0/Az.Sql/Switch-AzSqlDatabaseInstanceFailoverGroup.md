---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/switch-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: a20f2196b6052befb74cd74366c96bf262cdd325
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992286"
---
# <span data-ttu-id="b8dee-101">Switch-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b8dee-101">Switch-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="b8dee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8dee-102">SYNOPSIS</span></span>
<span data-ttu-id="b8dee-103">Wykonuje failover wystąpienia grupy trybu failover.</span><span class="sxs-lookup"><span data-stu-id="b8dee-103">Executes a failover of an Instance Failover Group.</span></span>

## <span data-ttu-id="b8dee-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b8dee-104">SYNTAX</span></span>

### <span data-ttu-id="b8dee-105">SwitchInstanceFailoverGroupDefaultSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="b8dee-105">SwitchInstanceFailoverGroupDefaultSet (Default)</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-AllowDataLoss] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8dee-106">SwitchInstanceFailoverGroupByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b8dee-106">SwitchInstanceFailoverGroupByResourceIdSet</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-AllowDataLoss]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8dee-107">SwitchInstanceFailoverGroupByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b8dee-107">SwitchInstanceFailoverGroupByInputObjectSet</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel> [-AllowDataLoss]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8dee-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="b8dee-108">DESCRIPTION</span></span>
<span data-ttu-id="b8dee-109">To polecenie zamienia role wystąpień zarządzanych w grupie trybu failover wystąpienia przez zamianę trybu failover na określony region pomocniczy, co czyni je nowym regionem podstawowym.</span><span class="sxs-lookup"><span data-stu-id="b8dee-109">This command swaps the roles of the managed instances in a Instance Failover Group by failing over to the specified secondary region, making it the new primary region.</span></span> <span data-ttu-id="b8dee-110">Wszystkie nowe sesje TDS łączące się z podstawowym punktem końcowym są automatycznie kierowane ponownie do nowego regionu podstawowego.</span><span class="sxs-lookup"><span data-stu-id="b8dee-110">All new TDS sessions connecting to the primary endpoint are automatically re-routed to the new primary region.</span></span> 

## <span data-ttu-id="b8dee-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b8dee-111">EXAMPLES</span></span>

### <span data-ttu-id="b8dee-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b8dee-112">Example 1</span></span>
```
C:\> Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Switch-AzSqlDatabaseInstanceFailoverGroup -AllowDataLoss
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

<span data-ttu-id="b8dee-113">Problem z operacją trybu failover pozwalającą na utratę danych przez rury w grupie trybu failover wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="b8dee-113">Issue a failover operation allowing data loss by piping in the Instance Failover Group.</span></span>

### <span data-ttu-id="b8dee-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b8dee-114">Example 2</span></span>
```
C:\> Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Switch-AzSqlDatabaseInstanceFailoverGroup
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

<span data-ttu-id="b8dee-115">Omiń operację trybu failover o najlepszym namysłzie, która zakończy się powodzeniem bez utraty danych lub nie zakończy się niepowodzeniem i zostanie wycofana.</span><span class="sxs-lookup"><span data-stu-id="b8dee-115">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="b8dee-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b8dee-116">PARAMETERS</span></span>

### <span data-ttu-id="b8dee-117">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="b8dee-117">-AllowDataLoss</span></span>
<span data-ttu-id="b8dee-118">Ukończ trybu failover, nawet jeśli spowoduje to utratę danych.</span><span class="sxs-lookup"><span data-stu-id="b8dee-118">Complete the failover even if doing so may result in data loss.</span></span>
<span data-ttu-id="b8dee-119">Umożliwi to kontynuowanie trybu failover nawet wtedy, gdy podstawowa baza danych jest niedostępna.</span><span class="sxs-lookup"><span data-stu-id="b8dee-119">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

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

### <span data-ttu-id="b8dee-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8dee-120">-DefaultProfile</span></span>
<span data-ttu-id="b8dee-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b8dee-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8dee-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8dee-122">-InputObject</span></span>
<span data-ttu-id="b8dee-123">Obiekt Grupy trybu failover wystąpienia do przełączenia</span><span class="sxs-lookup"><span data-stu-id="b8dee-123">The Instance Failover Group object to switch</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel
Parameter Sets: SwitchInstanceFailoverGroupByInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8dee-124">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="b8dee-124">-Location</span></span>
<span data-ttu-id="b8dee-125">Nazwa regionu lokalnego, z którego ma zostać pobrana grupa trybu failover wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="b8dee-125">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: SwitchInstanceFailoverGroupDefaultSet, SwitchInstanceFailoverGroupByResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8dee-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b8dee-126">-Name</span></span>
<span data-ttu-id="b8dee-127">Nazwa grupy wystąpienia trybu failover.</span><span class="sxs-lookup"><span data-stu-id="b8dee-127">The name of the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: SwitchInstanceFailoverGroupDefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8dee-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8dee-128">-ResourceGroupName</span></span>
<span data-ttu-id="b8dee-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b8dee-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SwitchInstanceFailoverGroupDefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8dee-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8dee-130">-ResourceId</span></span>
<span data-ttu-id="b8dee-131">Identyfikator zasobu grupy trybu failover wystąpienia do przełączenia.</span><span class="sxs-lookup"><span data-stu-id="b8dee-131">The Resource ID of the Instance Failover Group to switch.</span></span>

```yaml
Type: System.String
Parameter Sets: SwitchInstanceFailoverGroupByResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8dee-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b8dee-132">-Confirm</span></span>
<span data-ttu-id="b8dee-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b8dee-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8dee-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8dee-134">-WhatIf</span></span>
<span data-ttu-id="b8dee-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8dee-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8dee-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b8dee-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8dee-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8dee-137">CommonParameters</span></span>
<span data-ttu-id="b8dee-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8dee-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8dee-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b8dee-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8dee-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b8dee-140">INPUTS</span></span>

### <span data-ttu-id="b8dee-141">Microsoft.Azure.Commands.sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="b8dee-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="b8dee-142">System.String</span><span class="sxs-lookup"><span data-stu-id="b8dee-142">System.String</span></span>

## <span data-ttu-id="b8dee-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b8dee-143">OUTPUTS</span></span>

### <span data-ttu-id="b8dee-144">Microsoft.Azure.Commands.sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="b8dee-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="b8dee-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b8dee-145">NOTES</span></span>

## <span data-ttu-id="b8dee-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b8dee-146">RELATED LINKS</span></span>
