---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringreceivedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringReceivedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringReceivedRoute.md
ms.openlocfilehash: 14557809041fc6f4268dbe28ad9d8f13a70e4054
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184050"
---
# <span data-ttu-id="dc3b5-101">Get-AzPeeringReceivedRoute</span><span class="sxs-lookup"><span data-stu-id="dc3b5-101">Get-AzPeeringReceivedRoute</span></span>

## <span data-ttu-id="dc3b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc3b5-102">SYNOPSIS</span></span>
<span data-ttu-id="dc3b5-103">Wyświetla listę otrzymanych tras dla komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="dc3b5-103">Lists the received routes for a Peering.</span></span>

## <span data-ttu-id="dc3b5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="dc3b5-104">SYNTAX</span></span>

### <span data-ttu-id="dc3b5-105">ByResourceGroupAndName (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="dc3b5-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringReceivedRoute [-ResourceGroupName] <String> -Name <String> [-Prefix <String>] [-AsPath <String>]
 [-OriginAsValidationState <String>] [-RPKIValidationState <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dc3b5-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="dc3b5-106">ByResourceId</span></span>
```
Get-AzPeeringReceivedRoute [-ResourceId] <String> [-Prefix <String>] [-AsPath <String>]
 [-OriginAsValidationState <String>] [-RPKIValidationState <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dc3b5-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="dc3b5-107">DESCRIPTION</span></span>
<span data-ttu-id="dc3b5-108">Listy otrzymane trasy z komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="dc3b5-108">Lists recieved routes from a Peering</span></span>

## <span data-ttu-id="dc3b5-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="dc3b5-109">EXAMPLES</span></span>

### <span data-ttu-id="dc3b5-110">Lista 100 najlepszych tras odebranych dla komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="dc3b5-110">List top 100 received routes for a peering</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName
```

<span data-ttu-id="dc3b5-111">Lista wszystkich odebranych tras dla komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="dc3b5-111">Lists all of the received routes for a peering</span></span>

### <span data-ttu-id="dc3b5-112">Filtrowanie według ścieżki AS</span><span class="sxs-lookup"><span data-stu-id="dc3b5-112">Filter by AS Path</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -AsPath "1234 5674 9834"
```

<span data-ttu-id="dc3b5-113">Lista wszystkich otrzymanych tras dla komunikacji równorzędnej z filtrem w js.</span><span class="sxs-lookup"><span data-stu-id="dc3b5-113">Lists all of the received routes for a peering with a filter on AS</span></span> 

### <span data-ttu-id="dc3b5-114">Filter by RPKIValidationState</span><span class="sxs-lookup"><span data-stu-id="dc3b5-114">Filter by RPKIValidationState</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -RPKIValidationState "Valid"
```

<span data-ttu-id="dc3b5-115">Wyświetla listę wszystkich otrzymanych tras dla komunikacji równorzędnej za pomocą filtru na stronieENIAKIValidationState.</span><span class="sxs-lookup"><span data-stu-id="dc3b5-115">Lists all of the received routes for a peering with a filter on RPKIValidationState</span></span>

### <span data-ttu-id="dc3b5-116">Filter by OriginAsValidationState</span><span class="sxs-lookup"><span data-stu-id="dc3b5-116">Filter by OriginAsValidationState</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -OriginAsValidationState "Valid"
```

<span data-ttu-id="dc3b5-117">Lista wszystkich otrzymanych tras dla komunikacji równorzędnej za pomocą filtru w stanie OriginAsValidation</span><span class="sxs-lookup"><span data-stu-id="dc3b5-117">Lists all of the received routes for a peering with a filter on OriginAsValidationState</span></span>

## <span data-ttu-id="dc3b5-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dc3b5-118">PARAMETERS</span></span>

### <span data-ttu-id="dc3b5-119">-AsPath</span><span class="sxs-lookup"><span data-stu-id="dc3b5-119">-AsPath</span></span>
<span data-ttu-id="dc3b5-120">Filtruj według ścieżki AS.</span><span class="sxs-lookup"><span data-stu-id="dc3b5-120">Filter by AS Path.</span></span>
<span data-ttu-id="dc3b5-121">Przykład: '9342 1234 4567'</span><span class="sxs-lookup"><span data-stu-id="dc3b5-121">Example: '9342 1234 4567'</span></span>

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

### <span data-ttu-id="dc3b5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc3b5-122">-DefaultProfile</span></span>
<span data-ttu-id="dc3b5-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="dc3b5-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc3b5-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="dc3b5-124">-Name</span></span>
<span data-ttu-id="dc3b5-125">Unikatowa nazwa pliku PSPeering.</span><span class="sxs-lookup"><span data-stu-id="dc3b5-125">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc3b5-126">-OriginAsValidationState</span><span class="sxs-lookup"><span data-stu-id="dc3b5-126">-OriginAsValidationState</span></span>
<span data-ttu-id="dc3b5-127">Filtruj według pochodzenia jako stanu sprawdzania poprawności.</span><span class="sxs-lookup"><span data-stu-id="dc3b5-127">Filter by origin AS validation state.</span></span>

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

### <span data-ttu-id="dc3b5-128">— Prefiks</span><span class="sxs-lookup"><span data-stu-id="dc3b5-128">-Prefix</span></span>
<span data-ttu-id="dc3b5-129">Filtruj według prefiksu.</span><span class="sxs-lookup"><span data-stu-id="dc3b5-129">Filter by prefix.</span></span>

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

### <span data-ttu-id="dc3b5-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc3b5-130">-ResourceGroupName</span></span>
<span data-ttu-id="dc3b5-131">Tworzenie lub używanie nazwy istniejącej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="dc3b5-131">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc3b5-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dc3b5-132">-ResourceId</span></span>
<span data-ttu-id="dc3b5-133">Nazwa ciągu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="dc3b5-133">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc3b5-134">-PODCZASKIValidationState</span><span class="sxs-lookup"><span data-stu-id="dc3b5-134">-RPKIValidationState</span></span>
<span data-ttu-id="dc3b5-135">Filtruj według stanu sprawdzania poprawności PROCKI.</span><span class="sxs-lookup"><span data-stu-id="dc3b5-135">Filter by RPKI validation state.</span></span>

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

### <span data-ttu-id="dc3b5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc3b5-136">CommonParameters</span></span>
<span data-ttu-id="dc3b5-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc3b5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc3b5-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dc3b5-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc3b5-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dc3b5-139">INPUTS</span></span>

### <span data-ttu-id="dc3b5-140">System.String</span><span class="sxs-lookup"><span data-stu-id="dc3b5-140">System.String</span></span>

## <span data-ttu-id="dc3b5-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dc3b5-141">OUTPUTS</span></span>

### <span data-ttu-id="dc3b5-142">Microsoft.Azure.PowerShell.Cmdlet.Peering.Models.PSPeeringReceivedRoute</span><span class="sxs-lookup"><span data-stu-id="dc3b5-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringReceivedRoute</span></span>

## <span data-ttu-id="dc3b5-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="dc3b5-143">NOTES</span></span>

## <span data-ttu-id="dc3b5-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dc3b5-144">RELATED LINKS</span></span>
