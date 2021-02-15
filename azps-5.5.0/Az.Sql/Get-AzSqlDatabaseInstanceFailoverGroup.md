---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: bd2a157a1fb05baf0fa6e02b061462718ffad314
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188962"
---
# <span data-ttu-id="8ee2f-101">Get-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="8ee2f-101">Get-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="8ee2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ee2f-102">SYNOPSIS</span></span>
<span data-ttu-id="8ee2f-103">Pobiera lub wyświetla grupy wystąpienia trybu failover.</span><span class="sxs-lookup"><span data-stu-id="8ee2f-103">Gets or lists Instance Failover Groups.</span></span>

## <span data-ttu-id="8ee2f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8ee2f-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseInstanceFailoverGroup [[-Name] <String>] [-ResourceGroupName] <String> [-Location] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ee2f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="8ee2f-105">DESCRIPTION</span></span>
<span data-ttu-id="8ee2f-106">Pobiera określoną grupę wystąpienia trybu failover lub wyświetla grupy wystąpienia trybu failover w regionie w ramach subskrypcji użytkownika.</span><span class="sxs-lookup"><span data-stu-id="8ee2f-106">Gets a specific Instance Failover Group or lists the Instance Failover Groups in a region under the user's subscription.</span></span>

<span data-ttu-id="8ee2f-107">Do wykonania polecenia może zostać użyty jeden z regionów w grupie Wystąpienie trybu failover.</span><span class="sxs-lookup"><span data-stu-id="8ee2f-107">Either region in the Instance Failover Group may be used to execute the command.</span></span> <span data-ttu-id="8ee2f-108">Zwracane wartości będą odzwierciedlać stan wystąpień zarządzanych w tym regionie względem grupy trybu failover wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="8ee2f-108">The returned values will reflect the state of the Managed Instances in that region with respect to the Instance Failover Group.</span></span>

## <span data-ttu-id="8ee2f-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8ee2f-109">EXAMPLES</span></span>

### <span data-ttu-id="8ee2f-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8ee2f-110">Example 1</span></span>
```
PS C:\> $failoverGroups = Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location
Output:
{
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
}
```

<span data-ttu-id="8ee2f-111">Lista wszystkich grup trybu failover w regionie</span><span class="sxs-lookup"><span data-stu-id="8ee2f-111">Lists all Failover Groups in the region</span></span>

### <span data-ttu-id="8ee2f-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="8ee2f-112">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg
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

<span data-ttu-id="8ee2f-113">Pobierz konkretną grupę trybu failover wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="8ee2f-113">Get a specific Instance Failover Group.</span></span>

## <span data-ttu-id="8ee2f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ee2f-114">PARAMETERS</span></span>

### <span data-ttu-id="8ee2f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ee2f-115">-DefaultProfile</span></span>
<span data-ttu-id="8ee2f-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8ee2f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ee2f-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="8ee2f-117">-Location</span></span>
<span data-ttu-id="8ee2f-118">Nazwa regionu lokalnego, z którego ma zostać pobrana grupa trybu failover wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="8ee2f-118">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

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

### <span data-ttu-id="8ee2f-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8ee2f-119">-Name</span></span>
<span data-ttu-id="8ee2f-120">Nazwa grupy trybu failover wystąpienia do pobrania.</span><span class="sxs-lookup"><span data-stu-id="8ee2f-120">The name of the Instance Failover Group to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ee2f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ee2f-121">-ResourceGroupName</span></span>
<span data-ttu-id="8ee2f-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8ee2f-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="8ee2f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ee2f-123">CommonParameters</span></span>
<span data-ttu-id="8ee2f-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ee2f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ee2f-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8ee2f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ee2f-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8ee2f-126">INPUTS</span></span>

### <span data-ttu-id="8ee2f-127">System.String</span><span class="sxs-lookup"><span data-stu-id="8ee2f-127">System.String</span></span>

## <span data-ttu-id="8ee2f-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8ee2f-128">OUTPUTS</span></span>

### <span data-ttu-id="8ee2f-129">Microsoft.Azure.Commands.sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="8ee2f-129">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="8ee2f-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8ee2f-130">NOTES</span></span>

## <span data-ttu-id="8ee2f-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8ee2f-131">RELATED LINKS</span></span>
