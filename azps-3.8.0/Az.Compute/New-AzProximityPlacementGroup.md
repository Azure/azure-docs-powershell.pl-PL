---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azproximityplacementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzProximityPlacementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzProximityPlacementGroup.md
ms.openlocfilehash: cf8c4867fcc623065cce73fa392cb78d513200fc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050418"
---
# <span data-ttu-id="d5b36-101">New-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="d5b36-101">New-AzProximityPlacementGroup</span></span>

## <span data-ttu-id="d5b36-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d5b36-102">SYNOPSIS</span></span>
<span data-ttu-id="d5b36-103">Tworzenie zasobu grupy położenia zbliżeniowe.</span><span class="sxs-lookup"><span data-stu-id="d5b36-103">Create Proximity Placement Group resource.</span></span>

## <span data-ttu-id="d5b36-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d5b36-104">SYNTAX</span></span>

```
New-AzProximityPlacementGroup [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-ProximityPlacementGroupType <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5b36-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d5b36-105">DESCRIPTION</span></span>
<span data-ttu-id="d5b36-106">To polecenie cmdlet utworzy zasób grupy umieszczenia zbliżeniowe.</span><span class="sxs-lookup"><span data-stu-id="d5b36-106">This cmdlet will create Proximity Placement Group resource.</span></span>

## <span data-ttu-id="d5b36-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d5b36-107">EXAMPLES</span></span>

### <span data-ttu-id="d5b36-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d5b36-108">Example 1</span></span>
```
PS C:\> New-AzureRmProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName -Location $location -Tag @{key1 = "val1"}

ResourceGroupName           : rg0
ProximityPlacementGroupType : Standard
Id                          : /subscriptions/5393f919-a68a-43d0-9063-4b2bda6bffdf/resourceGroups/rg0/providers/Microsoft.Compute/proximityPlacementGroups/ppg0
Name                        : ppg0
Type                        : Microsoft.Compute/proximityPlacementGroups
Location                    : westcentralus
Tags                        : {"key1":"val1"}
```

<span data-ttu-id="d5b36-109">To polecenie tworzy grupę "miejsce zbliżeniowe" w danej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="d5b36-109">This command creates a proximity place group in the given location.</span></span>

## <span data-ttu-id="d5b36-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d5b36-110">PARAMETERS</span></span>

### <span data-ttu-id="d5b36-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d5b36-111">-AsJob</span></span>
<span data-ttu-id="d5b36-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d5b36-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d5b36-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5b36-113">-DefaultProfile</span></span>
<span data-ttu-id="d5b36-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d5b36-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5b36-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d5b36-115">-Location</span></span>
<span data-ttu-id="d5b36-116">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="d5b36-116">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5b36-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d5b36-117">-Name</span></span>
<span data-ttu-id="d5b36-118">Nazwa grupy położenia zbliżeniowe.</span><span class="sxs-lookup"><span data-stu-id="d5b36-118">The name of the proximity placement group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProximityPlacementGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5b36-119">-ProximityPlacementGroupType</span><span class="sxs-lookup"><span data-stu-id="d5b36-119">-ProximityPlacementGroupType</span></span>
<span data-ttu-id="d5b36-120">Określa typ grupy położenia zbliżeniowe.</span><span class="sxs-lookup"><span data-stu-id="d5b36-120">Specifies the type of the proximity placement group.</span></span>  <span data-ttu-id="d5b36-121">Możliwe wartości: Standard lub Ultra</span><span class="sxs-lookup"><span data-stu-id="d5b36-121">Possible values are: Standard or Ultra</span></span>

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

### <span data-ttu-id="d5b36-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5b36-122">-ResourceGroupName</span></span>
<span data-ttu-id="d5b36-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d5b36-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="d5b36-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="d5b36-124">-Tag</span></span>
<span data-ttu-id="d5b36-125">Znaczniki zasobów</span><span class="sxs-lookup"><span data-stu-id="d5b36-125">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5b36-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d5b36-126">-Confirm</span></span>
<span data-ttu-id="d5b36-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5b36-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5b36-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5b36-128">-WhatIf</span></span>
<span data-ttu-id="d5b36-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5b36-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5b36-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d5b36-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5b36-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5b36-131">CommonParameters</span></span>
<span data-ttu-id="d5b36-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5b36-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5b36-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d5b36-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5b36-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d5b36-134">INPUTS</span></span>

### <span data-ttu-id="d5b36-135">System. String</span><span class="sxs-lookup"><span data-stu-id="d5b36-135">System.String</span></span>

## <span data-ttu-id="d5b36-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d5b36-136">OUTPUTS</span></span>

### <span data-ttu-id="d5b36-137">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="d5b36-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span></span>

## <span data-ttu-id="d5b36-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d5b36-138">NOTES</span></span>

## <span data-ttu-id="d5b36-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d5b36-139">RELATED LINKS</span></span>
