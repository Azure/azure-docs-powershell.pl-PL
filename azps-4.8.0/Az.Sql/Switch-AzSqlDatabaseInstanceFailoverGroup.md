---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/switch-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 9f82c8a50cba86fed394d55692d03eeec2ef97ef
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220255"
---
# <span data-ttu-id="0e4c6-101">Switch-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="0e4c6-101">Switch-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="0e4c6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0e4c6-102">SYNOPSIS</span></span>
<span data-ttu-id="0e4c6-103">Wykonuje przejście do trybu failover w grupie praca awaryjna wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="0e4c6-103">Executes a failover of an Instance Failover Group.</span></span>

## <span data-ttu-id="0e4c6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0e4c6-104">SYNTAX</span></span>

### <span data-ttu-id="0e4c6-105">SwitchInstanceFailoverGroupDefaultSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0e4c6-105">SwitchInstanceFailoverGroupDefaultSet (Default)</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-AllowDataLoss] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e4c6-106">SwitchInstanceFailoverGroupByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0e4c6-106">SwitchInstanceFailoverGroupByResourceIdSet</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-AllowDataLoss]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e4c6-107">SwitchInstanceFailoverGroupByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0e4c6-107">SwitchInstanceFailoverGroupByInputObjectSet</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel> [-AllowDataLoss]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e4c6-108">Opis</span><span class="sxs-lookup"><span data-stu-id="0e4c6-108">DESCRIPTION</span></span>
<span data-ttu-id="0e4c6-109">To polecenie zamienia role wystąpień zarządzanych w grupie praca awaryjna wystąpienia, przełączając się do określonego regionu podrzędnego, tworząc nowy region podstawowy.</span><span class="sxs-lookup"><span data-stu-id="0e4c6-109">This command swaps the roles of the managed instances in a Instance Failover Group by failing over to the specified secondary region, making it the new primary region.</span></span> <span data-ttu-id="0e4c6-110">Wszystkie nowe sesje TDS łączące się z podstawowym punktem końcowym zostaną automatycznie przekierowane do nowego regionu podstawowego.</span><span class="sxs-lookup"><span data-stu-id="0e4c6-110">All new TDS sessions connecting to the primary endpoint are automatically re-routed to the new primary region.</span></span> 

## <span data-ttu-id="0e4c6-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0e4c6-111">EXAMPLES</span></span>

### <span data-ttu-id="0e4c6-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0e4c6-112">Example 1</span></span>
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

<span data-ttu-id="0e4c6-113">Wygeneruj operację przełączania awaryjnego umożliwiającą utratę danych przez potok w grupie praca awaryjna wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="0e4c6-113">Issue a failover operation allowing data loss by piping in the Instance Failover Group.</span></span>

### <span data-ttu-id="0e4c6-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="0e4c6-114">Example 2</span></span>
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

<span data-ttu-id="0e4c6-115">Wydaj optymalną operację przejęcia awaryjnego, która zakończy się powodzeniem bez utraty danych lub niepowodzenia i wycofania.</span><span class="sxs-lookup"><span data-stu-id="0e4c6-115">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="0e4c6-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0e4c6-116">PARAMETERS</span></span>

### <span data-ttu-id="0e4c6-117">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="0e4c6-117">-AllowDataLoss</span></span>
<span data-ttu-id="0e4c6-118">Ukończ pracę awaryjną, nawet jeśli to może spowodować utratę danych.</span><span class="sxs-lookup"><span data-stu-id="0e4c6-118">Complete the failover even if doing so may result in data loss.</span></span>
<span data-ttu-id="0e4c6-119">Umożliwi to kontynuowanie pracy awaryjnej nawet wtedy, gdy podstawowa baza danych jest niedostępna.</span><span class="sxs-lookup"><span data-stu-id="0e4c6-119">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

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

### <span data-ttu-id="0e4c6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e4c6-120">-DefaultProfile</span></span>
<span data-ttu-id="0e4c6-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0e4c6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e4c6-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0e4c6-122">-InputObject</span></span>
<span data-ttu-id="0e4c6-123">Obiekt grupy trybu failover wystąpienia do przełączenia</span><span class="sxs-lookup"><span data-stu-id="0e4c6-123">The Instance Failover Group object to switch</span></span>

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

### <span data-ttu-id="0e4c6-124">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="0e4c6-124">-Location</span></span>
<span data-ttu-id="0e4c6-125">Nazwa regionu lokalnego, z którego ma zostać pobrana Grupa wystąpienie trybu failover.</span><span class="sxs-lookup"><span data-stu-id="0e4c6-125">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

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

### <span data-ttu-id="0e4c6-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0e4c6-126">-Name</span></span>
<span data-ttu-id="0e4c6-127">Nazwa grupy tryb failover wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="0e4c6-127">The name of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="0e4c6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e4c6-128">-ResourceGroupName</span></span>
<span data-ttu-id="0e4c6-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0e4c6-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="0e4c6-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e4c6-130">-ResourceId</span></span>
<span data-ttu-id="0e4c6-131">Identyfikator zasobu grupy trybu failover wystąpienia do przełączenia.</span><span class="sxs-lookup"><span data-stu-id="0e4c6-131">The Resource ID of the Instance Failover Group to switch.</span></span>

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

### <span data-ttu-id="0e4c6-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0e4c6-132">-Confirm</span></span>
<span data-ttu-id="0e4c6-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e4c6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e4c6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e4c6-134">-WhatIf</span></span>
<span data-ttu-id="0e4c6-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e4c6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e4c6-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0e4c6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e4c6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e4c6-137">CommonParameters</span></span>
<span data-ttu-id="0e4c6-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e4c6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e4c6-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0e4c6-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e4c6-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0e4c6-140">INPUTS</span></span>

### <span data-ttu-id="0e4c6-141">Microsoft. Azure. Commands. SQL. InstanceFailoverGroup. model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="0e4c6-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="0e4c6-142">System. String</span><span class="sxs-lookup"><span data-stu-id="0e4c6-142">System.String</span></span>

## <span data-ttu-id="0e4c6-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0e4c6-143">OUTPUTS</span></span>

### <span data-ttu-id="0e4c6-144">Microsoft. Azure. Commands. SQL. InstanceFailoverGroup. model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="0e4c6-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="0e4c6-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0e4c6-145">NOTES</span></span>

## <span data-ttu-id="0e4c6-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0e4c6-146">RELATED LINKS</span></span>
