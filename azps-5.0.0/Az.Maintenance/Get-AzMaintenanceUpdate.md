---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azmaintenanceupdate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceUpdate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceUpdate.md
ms.openlocfilehash: d8d3e4df3349acb1340a24362043d32d528fc284
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94231823"
---
# <span data-ttu-id="e2e4f-101">Get-AzMaintenanceUpdate</span><span class="sxs-lookup"><span data-stu-id="e2e4f-101">Get-AzMaintenanceUpdate</span></span>

## <span data-ttu-id="e2e4f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e2e4f-102">SYNOPSIS</span></span>
<span data-ttu-id="e2e4f-103">Uzyskaj oczekujące aktualizacje konserwacji zasobu.</span><span class="sxs-lookup"><span data-stu-id="e2e4f-103">Get pending maintenance updates to resource.</span></span>

## <span data-ttu-id="e2e4f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e2e4f-104">SYNTAX</span></span>

```
Get-AzMaintenanceUpdate [-ResourceGroupName] <String> [-ProviderName] <String> [-ResourceParentType <String>]
 [-ResourceParentName <String>] [-ResourceType] <String> [-ResourceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2e4f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e2e4f-105">DESCRIPTION</span></span>
<span data-ttu-id="e2e4f-106">Uzyskaj oczekujące aktualizacje konserwacji zasobu.</span><span class="sxs-lookup"><span data-stu-id="e2e4f-106">Get pending maintenance updates to resource.</span></span>

## <span data-ttu-id="e2e4f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e2e4f-107">EXAMPLES</span></span>

### <span data-ttu-id="e2e4f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e2e4f-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMaintenanceUpdate -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute

MaintenanceScope    : Host
ImpactType          : Freeze
Status              : Pending
ImpactDurationInSec : 9
NotBefore           : 1/24/2020 5:11:41 AM
ResourceId          : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2
```

<span data-ttu-id="e2e4f-109">Uzyskaj oczekujące aktualizacje konserwacji zasobu.</span><span class="sxs-lookup"><span data-stu-id="e2e4f-109">Get pending maintenance updates to resource.</span></span>

## <span data-ttu-id="e2e4f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e2e4f-110">PARAMETERS</span></span>

### <span data-ttu-id="e2e4f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2e4f-111">-DefaultProfile</span></span>
<span data-ttu-id="e2e4f-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e2e4f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2e4f-113">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="e2e4f-113">-ProviderName</span></span>
<span data-ttu-id="e2e4f-114">Nazwa dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e2e4f-114">The resource provider Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e4f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2e4f-115">-ResourceGroupName</span></span>
<span data-ttu-id="e2e4f-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e2e4f-116">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e4f-117">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="e2e4f-117">-ResourceName</span></span>
<span data-ttu-id="e2e4f-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="e2e4f-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e4f-119">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="e2e4f-119">-ResourceParentName</span></span>
<span data-ttu-id="e2e4f-120">Nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="e2e4f-120">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e4f-121">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="e2e4f-121">-ResourceParentType</span></span>
<span data-ttu-id="e2e4f-122">Nadrzędny typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="e2e4f-122">The parent resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e4f-123">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="e2e4f-123">-ResourceType</span></span>
<span data-ttu-id="e2e4f-124">Typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="e2e4f-124">The resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e4f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2e4f-125">CommonParameters</span></span>
<span data-ttu-id="e2e4f-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2e4f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2e4f-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e2e4f-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2e4f-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e2e4f-128">INPUTS</span></span>

### <span data-ttu-id="e2e4f-129">System. String</span><span class="sxs-lookup"><span data-stu-id="e2e4f-129">System.String</span></span>

## <span data-ttu-id="e2e4f-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e2e4f-130">OUTPUTS</span></span>

### <span data-ttu-id="e2e4f-131">Microsoft. Azure. Management. Maintenance. MODELES. Update</span><span class="sxs-lookup"><span data-stu-id="e2e4f-131">Microsoft.Azure.Management.Maintenance.Models.Update</span></span>

## <span data-ttu-id="e2e4f-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e2e4f-132">NOTES</span></span>

## <span data-ttu-id="e2e4f-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e2e4f-133">RELATED LINKS</span></span>
