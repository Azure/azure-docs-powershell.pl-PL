---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzAvailabilitySet.md
ms.openlocfilehash: 689336bb7fbb7ef59be96a5bd6bcbfe49ddb64c0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177411"
---
# <span data-ttu-id="f566a-101">Update-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f566a-101">Update-AzAvailabilitySet</span></span>

## <span data-ttu-id="f566a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f566a-102">SYNOPSIS</span></span>
<span data-ttu-id="f566a-103">Aktualizuje zestaw dostępności.</span><span class="sxs-lookup"><span data-stu-id="f566a-103">Updates an availability set.</span></span>

## <span data-ttu-id="f566a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f566a-104">SYNTAX</span></span>

```
Update-AzAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [[-Sku] <String>]
 [-ProximityPlacementGroupId <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f566a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f566a-105">DESCRIPTION</span></span>
<span data-ttu-id="f566a-106">Polecenie **cmdlet Update-AzAvailabilitySet** aktualizuje zestaw dostępności.</span><span class="sxs-lookup"><span data-stu-id="f566a-106">The **Update-AzAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="f566a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f566a-107">EXAMPLES</span></span>

### <span data-ttu-id="f566a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f566a-108">Example 1</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzAvailabilitySet -Managed;
```

<span data-ttu-id="f566a-109">To polecenie aktualizuje zestaw dostępności o nazwie "AvSet01" w grupie zasobów o nazwie "ResourceGroup01" na zarządzany zestaw dostępności.</span><span class="sxs-lookup"><span data-stu-id="f566a-109">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="f566a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f566a-110">PARAMETERS</span></span>

### <span data-ttu-id="f566a-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="f566a-111">-AsJob</span></span>
<span data-ttu-id="f566a-112">Uruchom polecenie cmdlet w tle i zwróć zadanie w celu śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="f566a-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="f566a-113">-AvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f566a-113">-AvailabilitySet</span></span>
<span data-ttu-id="f566a-114">Określa obiekt zestawu dostępności do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="f566a-114">Specifies the availability set object to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f566a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f566a-115">-DefaultProfile</span></span>
<span data-ttu-id="f566a-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f566a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f566a-117">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="f566a-117">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="f566a-118">Identyfikator zasobu grupy Położenie odległości do użycia z tym zestawem dostępności.</span><span class="sxs-lookup"><span data-stu-id="f566a-118">The resource id of the Proximity Placement Group to use with this availability set.</span></span>

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

### <span data-ttu-id="f566a-119">- SKU</span><span class="sxs-lookup"><span data-stu-id="f566a-119">-Sku</span></span>
<span data-ttu-id="f566a-120">Nazwa sku</span><span class="sxs-lookup"><span data-stu-id="f566a-120">The Name of Sku</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f566a-121">— Tag</span><span class="sxs-lookup"><span data-stu-id="f566a-121">-Tag</span></span>
<span data-ttu-id="f566a-122">Pary klucz-wartość w postaci tabeli skrótu.</span><span class="sxs-lookup"><span data-stu-id="f566a-122">Key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="f566a-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f566a-123">-Confirm</span></span>
<span data-ttu-id="f566a-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f566a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f566a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f566a-125">-WhatIf</span></span>
<span data-ttu-id="f566a-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f566a-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f566a-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f566a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f566a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f566a-128">CommonParameters</span></span>
<span data-ttu-id="f566a-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f566a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f566a-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f566a-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f566a-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f566a-131">INPUTS</span></span>

### <span data-ttu-id="f566a-132">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f566a-132">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="f566a-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f566a-133">OUTPUTS</span></span>

### <span data-ttu-id="f566a-134">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f566a-134">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="f566a-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f566a-135">NOTES</span></span>

## <span data-ttu-id="f566a-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f566a-136">RELATED LINKS</span></span>
