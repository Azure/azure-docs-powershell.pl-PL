---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azproximityplacementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzProximityPlacementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzProximityPlacementGroup.md
ms.openlocfilehash: 88cdb68da94f84dc1af977ba5b12b5bfb4d73914
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706334"
---
# <span data-ttu-id="7c8c3-101">New-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="7c8c3-101">New-AzProximityPlacementGroup</span></span>

## <span data-ttu-id="7c8c3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7c8c3-102">SYNOPSIS</span></span>
<span data-ttu-id="7c8c3-103">Tworzenie zasobu grupy położenia zbliżeniowe.</span><span class="sxs-lookup"><span data-stu-id="7c8c3-103">Create Proximity Placement Group resource.</span></span>

## <span data-ttu-id="7c8c3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7c8c3-104">SYNTAX</span></span>

```
New-AzProximityPlacementGroup [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-ProximityPlacementGroupType <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c8c3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7c8c3-105">DESCRIPTION</span></span>
<span data-ttu-id="7c8c3-106">To polecenie cmdlet utworzy zasób grupy umieszczenia zbliżeniowe.</span><span class="sxs-lookup"><span data-stu-id="7c8c3-106">This cmdlet will create Proximity Placement Group resource.</span></span>

## <span data-ttu-id="7c8c3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7c8c3-107">EXAMPLES</span></span>

### <span data-ttu-id="7c8c3-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7c8c3-108">Example 1</span></span>
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

<span data-ttu-id="7c8c3-109">To polecenie tworzy grupę "miejsce zbliżeniowe" w danej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="7c8c3-109">This command creates a proximity place group in the given location.</span></span>

## <span data-ttu-id="7c8c3-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7c8c3-110">PARAMETERS</span></span>

### <span data-ttu-id="7c8c3-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7c8c3-111">-AsJob</span></span>
<span data-ttu-id="7c8c3-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="7c8c3-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7c8c3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c8c3-113">-DefaultProfile</span></span>
<span data-ttu-id="7c8c3-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7c8c3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c8c3-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="7c8c3-115">-Location</span></span>
<span data-ttu-id="7c8c3-116">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="7c8c3-116">Resource location</span></span>

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

### <span data-ttu-id="7c8c3-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7c8c3-117">-Name</span></span>
<span data-ttu-id="7c8c3-118">Nazwa grupy położenia zbliżeniowe.</span><span class="sxs-lookup"><span data-stu-id="7c8c3-118">The name of the proximity placement group.</span></span>

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

### <span data-ttu-id="7c8c3-119">-ProximityPlacementGroupType</span><span class="sxs-lookup"><span data-stu-id="7c8c3-119">-ProximityPlacementGroupType</span></span>
<span data-ttu-id="7c8c3-120">Określa typ grupy położenia zbliżeniowe.</span><span class="sxs-lookup"><span data-stu-id="7c8c3-120">Specifies the type of the proximity placement group.</span></span>  <span data-ttu-id="7c8c3-121">Możliwe wartości: Standard lub Ultra</span><span class="sxs-lookup"><span data-stu-id="7c8c3-121">Possible values are: Standard or Ultra</span></span>

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

### <span data-ttu-id="7c8c3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c8c3-122">-ResourceGroupName</span></span>
<span data-ttu-id="7c8c3-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7c8c3-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="7c8c3-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="7c8c3-124">-Tag</span></span>
<span data-ttu-id="7c8c3-125">Znaczniki zasobów</span><span class="sxs-lookup"><span data-stu-id="7c8c3-125">Resource tags</span></span>

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

### <span data-ttu-id="7c8c3-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7c8c3-126">-Confirm</span></span>
<span data-ttu-id="7c8c3-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c8c3-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c8c3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c8c3-128">-WhatIf</span></span>
<span data-ttu-id="7c8c3-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c8c3-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c8c3-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7c8c3-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c8c3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c8c3-131">CommonParameters</span></span>
<span data-ttu-id="7c8c3-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c8c3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c8c3-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7c8c3-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c8c3-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7c8c3-134">INPUTS</span></span>

### <span data-ttu-id="7c8c3-135">System. String</span><span class="sxs-lookup"><span data-stu-id="7c8c3-135">System.String</span></span>

## <span data-ttu-id="7c8c3-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7c8c3-136">OUTPUTS</span></span>

### <span data-ttu-id="7c8c3-137">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="7c8c3-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span></span>

## <span data-ttu-id="7c8c3-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7c8c3-138">NOTES</span></span>

## <span data-ttu-id="7c8c3-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7c8c3-139">RELATED LINKS</span></span>
