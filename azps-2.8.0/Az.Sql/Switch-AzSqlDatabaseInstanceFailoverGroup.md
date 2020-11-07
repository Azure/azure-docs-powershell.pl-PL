---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/switch-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 7d52c80bba03d0e88d6e5302647fd9e6de94675f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93887690"
---
# <span data-ttu-id="8368e-101">Switch-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="8368e-101">Switch-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="8368e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8368e-102">SYNOPSIS</span></span>
<span data-ttu-id="8368e-103">Wykonuje przejście do trybu failover w grupie praca awaryjna wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="8368e-103">Executes a failover of an Instance Failover Group.</span></span>

## <span data-ttu-id="8368e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8368e-104">SYNTAX</span></span>

### <span data-ttu-id="8368e-105">SwitchIFGDefault (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8368e-105">SwitchIFGDefault (Default)</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String>
 [-Name] <String> [-AllowDataLoss] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8368e-106">Przełączanie grupy trybu failover wystąpienia z identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="8368e-106">Switch a Instance Failover Group from Resource Id</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-AllowDataLoss]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8368e-107">Przełączanie grupy awarii wystąpienia z definicji wystąpienia AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="8368e-107">Switch a Instance Failover Group from AzureSqlInstanceFailoverGroupModel instance definition</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup -InputObject <AzureSqlInstanceFailoverGroupModel>
 [-AllowDataLoss] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8368e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8368e-108">DESCRIPTION</span></span>
<span data-ttu-id="8368e-109">To polecenie zamienia role wystąpień zarządzanych w grupie praca awaryjna wystąpienia, przełączając się do określonego regionu podrzędnego, tworząc nowy region podstawowy.</span><span class="sxs-lookup"><span data-stu-id="8368e-109">This command swaps the roles of the managed instances in a Instance Failover Group by failing over to the specified secondary region, making it the new primary region.</span></span> <span data-ttu-id="8368e-110">Wszystkie nowe sesje TDS łączące się z podstawowym punktem końcowym zostaną automatycznie przekierowane do nowego regionu podstawowego.</span><span class="sxs-lookup"><span data-stu-id="8368e-110">All new TDS sessions connecting to the primary endpoint are automatically re-routed to the new primary region.</span></span> 

## <span data-ttu-id="8368e-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8368e-111">EXAMPLES</span></span>

### <span data-ttu-id="8368e-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8368e-112">Example 1</span></span>
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

<span data-ttu-id="8368e-113">Wygeneruj operację przełączania awaryjnego umożliwiającą utratę danych przez potok w grupie praca awaryjna wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="8368e-113">Issue a failover operation allowing data loss by piping in the Instance Failover Group.</span></span>

### <span data-ttu-id="8368e-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="8368e-114">Example 2</span></span>
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

<span data-ttu-id="8368e-115">Wydaj optymalną operację przejęcia awaryjnego, która zakończy się powodzeniem bez utraty danych lub niepowodzenia i wycofania.</span><span class="sxs-lookup"><span data-stu-id="8368e-115">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="8368e-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8368e-116">PARAMETERS</span></span>

### <span data-ttu-id="8368e-117">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="8368e-117">-AllowDataLoss</span></span>
<span data-ttu-id="8368e-118">Ukończ pracę awaryjną, nawet jeśli to może spowodować utratę danych.</span><span class="sxs-lookup"><span data-stu-id="8368e-118">Complete the failover even if doing so may result in data loss.</span></span>
<span data-ttu-id="8368e-119">Umożliwi to kontynuowanie pracy awaryjnej nawet wtedy, gdy podstawowa baza danych jest niedostępna.</span><span class="sxs-lookup"><span data-stu-id="8368e-119">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8368e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8368e-120">-DefaultProfile</span></span>
<span data-ttu-id="8368e-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8368e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8368e-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8368e-122">-InputObject</span></span>
<span data-ttu-id="8368e-123">Obiekt grupy trybu failover wystąpienia do przełączenia</span><span class="sxs-lookup"><span data-stu-id="8368e-123">The Instance Failover Group object to switch</span></span>

```yaml
Type: AzureSqlInstanceFailoverGroupModel
Parameter Sets: Switch a Instance Failover Group from AzureSqlInstanceFailoverGroupModel instance definition
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8368e-124">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="8368e-124">-Location</span></span>
<span data-ttu-id="8368e-125">Nazwa regionu lokalnego, z którego ma zostać pobrana Grupa wystąpienie trybu failover.</span><span class="sxs-lookup"><span data-stu-id="8368e-125">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: SwitchIFGDefault, Switch a Instance Failover Group from Resource Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8368e-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8368e-126">-Name</span></span>
<span data-ttu-id="8368e-127">Nazwa grupy tryb failover wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="8368e-127">The name of the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: SwitchIFGDefault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8368e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8368e-128">-ResourceGroupName</span></span>
<span data-ttu-id="8368e-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8368e-129">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: SwitchIFGDefault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8368e-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8368e-130">-ResourceId</span></span>
<span data-ttu-id="8368e-131">Identyfikator zasobu grupy trybu failover wystąpienia do przełączenia.</span><span class="sxs-lookup"><span data-stu-id="8368e-131">The Resource ID of the Instance Failover Group to switch.</span></span>

```yaml
Type: String
Parameter Sets: Switch a Instance Failover Group from Resource Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8368e-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8368e-132">-Confirm</span></span>
<span data-ttu-id="8368e-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8368e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8368e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8368e-134">-WhatIf</span></span>
<span data-ttu-id="8368e-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8368e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8368e-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8368e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8368e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8368e-137">CommonParameters</span></span>
<span data-ttu-id="8368e-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8368e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8368e-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8368e-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8368e-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8368e-140">INPUTS</span></span>

### <span data-ttu-id="8368e-141">Microsoft. Azure. Commands. SQL. InstanceFailoverGroup. model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="8368e-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="8368e-142">System. String</span><span class="sxs-lookup"><span data-stu-id="8368e-142">System.String</span></span>

## <span data-ttu-id="8368e-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8368e-143">OUTPUTS</span></span>

### <span data-ttu-id="8368e-144">Microsoft. Azure. Commands. SQL. InstanceFailoverGroup. model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="8368e-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="8368e-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8368e-145">NOTES</span></span>

## <span data-ttu-id="8368e-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8368e-146">RELATED LINKS</span></span>
