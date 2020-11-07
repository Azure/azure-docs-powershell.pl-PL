---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azproximityplacementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzProximityPlacementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzProximityPlacementGroup.md
ms.openlocfilehash: 07adbff46713136ec412d10bd428765230e1838c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93896774"
---
# <span data-ttu-id="bc73e-101">Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="bc73e-101">Remove-AzProximityPlacementGroup</span></span>

## <span data-ttu-id="bc73e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bc73e-102">SYNOPSIS</span></span>
<span data-ttu-id="bc73e-103">Usuwanie zasobu grupy położenia zbliżeniowe.</span><span class="sxs-lookup"><span data-stu-id="bc73e-103">Delete Proximity Placement Group resource.</span></span>

## <span data-ttu-id="bc73e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bc73e-104">SYNTAX</span></span>

### <span data-ttu-id="bc73e-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bc73e-105">DefaultParameter (Default)</span></span>
```
Remove-AzProximityPlacementGroup [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc73e-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="bc73e-106">ResourceIdParameter</span></span>
```
Remove-AzProximityPlacementGroup [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc73e-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="bc73e-107">ObjectParameter</span></span>
```
Remove-AzProximityPlacementGroup [-Force] [-InputObject] <PSProximityPlacementGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc73e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="bc73e-108">DESCRIPTION</span></span>
<span data-ttu-id="bc73e-109">To polecenie cmdlet spowoduje usunięcie zasobu grupy położenia zbliżeniowe.</span><span class="sxs-lookup"><span data-stu-id="bc73e-109">This cmdlet will delete Proximity Placement Group resource.</span></span>

## <span data-ttu-id="bc73e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bc73e-110">EXAMPLES</span></span>

### <span data-ttu-id="bc73e-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bc73e-111">Example 1</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup  -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName  | Remove-AzureRmProximityPlacementGroup
```

<span data-ttu-id="bc73e-112">To polecenie umożliwia usunięcie danej grupy położenia zbliżeniowe.</span><span class="sxs-lookup"><span data-stu-id="bc73e-112">This command removes the given proximity placement group.</span></span>

## <span data-ttu-id="bc73e-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bc73e-113">PARAMETERS</span></span>

### <span data-ttu-id="bc73e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bc73e-114">-AsJob</span></span>
<span data-ttu-id="bc73e-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="bc73e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bc73e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc73e-116">-DefaultProfile</span></span>
<span data-ttu-id="bc73e-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bc73e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc73e-118">-Force</span><span class="sxs-lookup"><span data-stu-id="bc73e-118">-Force</span></span>
<span data-ttu-id="bc73e-119">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="bc73e-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bc73e-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bc73e-120">-InputObject</span></span>
<span data-ttu-id="bc73e-121">Obiekt grupy umieszczenia zbliżeniowe w PS</span><span class="sxs-lookup"><span data-stu-id="bc73e-121">The PS Proximity Placement Group Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup
Parameter Sets: ObjectParameter
Aliases: ProximityPlacementGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc73e-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bc73e-122">-Name</span></span>
<span data-ttu-id="bc73e-123">Nazwa grupy położenia zbliżeniowe.</span><span class="sxs-lookup"><span data-stu-id="bc73e-123">The name of the proximity placement group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: ProximityPlacementGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc73e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc73e-124">-ResourceGroupName</span></span>
<span data-ttu-id="bc73e-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bc73e-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc73e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bc73e-126">-ResourceId</span></span>
<span data-ttu-id="bc73e-127">Identyfikator zasobu dla grupy rozmieszczenia zbliżeniowe.</span><span class="sxs-lookup"><span data-stu-id="bc73e-127">The resource id for the proximity placement group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc73e-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bc73e-128">-Confirm</span></span>
<span data-ttu-id="bc73e-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc73e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc73e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc73e-130">-WhatIf</span></span>
<span data-ttu-id="bc73e-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc73e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc73e-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bc73e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc73e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc73e-133">CommonParameters</span></span>
<span data-ttu-id="bc73e-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc73e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc73e-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bc73e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc73e-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bc73e-136">INPUTS</span></span>

### <span data-ttu-id="bc73e-137">System. String</span><span class="sxs-lookup"><span data-stu-id="bc73e-137">System.String</span></span>

### <span data-ttu-id="bc73e-138">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="bc73e-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span></span>

## <span data-ttu-id="bc73e-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bc73e-139">OUTPUTS</span></span>

### <span data-ttu-id="bc73e-140">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="bc73e-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="bc73e-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bc73e-141">NOTES</span></span>

## <span data-ttu-id="bc73e-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bc73e-142">RELATED LINKS</span></span>
