---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzAvailabilitySet.md
ms.openlocfilehash: 689336bb7fbb7ef59be96a5bd6bcbfe49ddb64c0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225734"
---
# <span data-ttu-id="1bec1-101">Update-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="1bec1-101">Update-AzAvailabilitySet</span></span>

## <span data-ttu-id="1bec1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1bec1-102">SYNOPSIS</span></span>
<span data-ttu-id="1bec1-103">Umożliwia zaktualizowanie zestawu dostępności.</span><span class="sxs-lookup"><span data-stu-id="1bec1-103">Updates an availability set.</span></span>

## <span data-ttu-id="1bec1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1bec1-104">SYNTAX</span></span>

```
Update-AzAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [[-Sku] <String>]
 [-ProximityPlacementGroupId <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1bec1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1bec1-105">DESCRIPTION</span></span>
<span data-ttu-id="1bec1-106">Polecenie cmdlet **Update-AzAvailabilitySet** aktualizuje zestaw dostępności.</span><span class="sxs-lookup"><span data-stu-id="1bec1-106">The **Update-AzAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="1bec1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1bec1-107">EXAMPLES</span></span>

### <span data-ttu-id="1bec1-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1bec1-108">Example 1</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzAvailabilitySet -Managed;
```

<span data-ttu-id="1bec1-109">To polecenie aktualizuje zestaw dostępności o nazwie "AvSet01" w grupie zasobów o nazwie "ResourceGroup01" do zestawu dostępności zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="1bec1-109">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="1bec1-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1bec1-110">PARAMETERS</span></span>

### <span data-ttu-id="1bec1-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1bec1-111">-AsJob</span></span>
<span data-ttu-id="1bec1-112">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="1bec1-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="1bec1-113">-AvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="1bec1-113">-AvailabilitySet</span></span>
<span data-ttu-id="1bec1-114">Określa obiekt zestawu dostępności do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="1bec1-114">Specifies the availability set object to be updated.</span></span>

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

### <span data-ttu-id="1bec1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bec1-115">-DefaultProfile</span></span>
<span data-ttu-id="1bec1-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1bec1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1bec1-117">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="1bec1-117">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="1bec1-118">Identyfikator zasobu grupy położenia zbliżeniowe, który ma być używany z tym zestawem dostępności.</span><span class="sxs-lookup"><span data-stu-id="1bec1-118">The resource id of the Proximity Placement Group to use with this availability set.</span></span>

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

### <span data-ttu-id="1bec1-119">-SKU</span><span class="sxs-lookup"><span data-stu-id="1bec1-119">-Sku</span></span>
<span data-ttu-id="1bec1-120">Nazwa SKU</span><span class="sxs-lookup"><span data-stu-id="1bec1-120">The Name of Sku</span></span>

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

### <span data-ttu-id="1bec1-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="1bec1-121">-Tag</span></span>
<span data-ttu-id="1bec1-122">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="1bec1-122">Key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="1bec1-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1bec1-123">-Confirm</span></span>
<span data-ttu-id="1bec1-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1bec1-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bec1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bec1-125">-WhatIf</span></span>
<span data-ttu-id="1bec1-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1bec1-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1bec1-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1bec1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bec1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bec1-128">CommonParameters</span></span>
<span data-ttu-id="1bec1-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bec1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bec1-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1bec1-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bec1-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1bec1-131">INPUTS</span></span>

### <span data-ttu-id="1bec1-132">Microsoft. Azure. Commands. COMPUTE. models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="1bec1-132">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="1bec1-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1bec1-133">OUTPUTS</span></span>

### <span data-ttu-id="1bec1-134">Microsoft. Azure. Commands. COMPUTE. models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="1bec1-134">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="1bec1-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1bec1-135">NOTES</span></span>

## <span data-ttu-id="1bec1-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1bec1-136">RELATED LINKS</span></span>
