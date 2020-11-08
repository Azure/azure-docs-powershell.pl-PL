---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: bd2a157a1fb05baf0fa6e02b061462718ffad314
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063167"
---
# <span data-ttu-id="8954b-101">Get-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="8954b-101">Get-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="8954b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8954b-102">SYNOPSIS</span></span>
<span data-ttu-id="8954b-103">Pobiera lub wyświetla grupy trybu failover wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="8954b-103">Gets or lists Instance Failover Groups.</span></span>

## <span data-ttu-id="8954b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8954b-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseInstanceFailoverGroup [[-Name] <String>] [-ResourceGroupName] <String> [-Location] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8954b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8954b-105">DESCRIPTION</span></span>
<span data-ttu-id="8954b-106">Pobiera określoną grupę wystąpień awaryjnych lub listę grup trybu failover wystąpienia w regionie poniżej abonamentu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="8954b-106">Gets a specific Instance Failover Group or lists the Instance Failover Groups in a region under the user's subscription.</span></span>

<span data-ttu-id="8954b-107">Do wykonania polecenia może być wykorzystywany dowolny region w grupie praca awaryjna wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="8954b-107">Either region in the Instance Failover Group may be used to execute the command.</span></span> <span data-ttu-id="8954b-108">Zwracane wartości będą odzwierciedlać stan zarządzanych wystąpień w tym regionie w odniesieniu do grupy trybu failover wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="8954b-108">The returned values will reflect the state of the Managed Instances in that region with respect to the Instance Failover Group.</span></span>

## <span data-ttu-id="8954b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8954b-109">EXAMPLES</span></span>

### <span data-ttu-id="8954b-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8954b-110">Example 1</span></span>
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

<span data-ttu-id="8954b-111">Lista wszystkich grup pracy awaryjnej w regionie</span><span class="sxs-lookup"><span data-stu-id="8954b-111">Lists all Failover Groups in the region</span></span>

### <span data-ttu-id="8954b-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="8954b-112">Example 2</span></span>
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

<span data-ttu-id="8954b-113">Pobierz określoną grupę wystąpień awaryjnych.</span><span class="sxs-lookup"><span data-stu-id="8954b-113">Get a specific Instance Failover Group.</span></span>

## <span data-ttu-id="8954b-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8954b-114">PARAMETERS</span></span>

### <span data-ttu-id="8954b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8954b-115">-DefaultProfile</span></span>
<span data-ttu-id="8954b-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8954b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8954b-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="8954b-117">-Location</span></span>
<span data-ttu-id="8954b-118">Nazwa regionu lokalnego, z którego ma zostać pobrana Grupa wystąpienie trybu failover.</span><span class="sxs-lookup"><span data-stu-id="8954b-118">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

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

### <span data-ttu-id="8954b-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8954b-119">-Name</span></span>
<span data-ttu-id="8954b-120">Nazwa grupy tryb failover wystąpienia do pobrania.</span><span class="sxs-lookup"><span data-stu-id="8954b-120">The name of the Instance Failover Group to retrieve.</span></span>

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

### <span data-ttu-id="8954b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8954b-121">-ResourceGroupName</span></span>
<span data-ttu-id="8954b-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8954b-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="8954b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8954b-123">CommonParameters</span></span>
<span data-ttu-id="8954b-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8954b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8954b-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8954b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8954b-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8954b-126">INPUTS</span></span>

### <span data-ttu-id="8954b-127">System. String</span><span class="sxs-lookup"><span data-stu-id="8954b-127">System.String</span></span>

## <span data-ttu-id="8954b-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8954b-128">OUTPUTS</span></span>

### <span data-ttu-id="8954b-129">Microsoft. Azure. Commands. SQL. InstanceFailoverGroup. model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="8954b-129">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="8954b-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8954b-130">NOTES</span></span>

## <span data-ttu-id="8954b-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8954b-131">RELATED LINKS</span></span>
