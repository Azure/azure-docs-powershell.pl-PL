---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringreceivedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringReceivedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringReceivedRoute.md
ms.openlocfilehash: 14557809041fc6f4268dbe28ad9d8f13a70e4054
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232405"
---
# <span data-ttu-id="dc03f-101">Get-AzPeeringReceivedRoute</span><span class="sxs-lookup"><span data-stu-id="dc03f-101">Get-AzPeeringReceivedRoute</span></span>

## <span data-ttu-id="dc03f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dc03f-102">SYNOPSIS</span></span>
<span data-ttu-id="dc03f-103">Wyświetla listę odebranych tras dla komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="dc03f-103">Lists the received routes for a Peering.</span></span>

## <span data-ttu-id="dc03f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dc03f-104">SYNTAX</span></span>

### <span data-ttu-id="dc03f-105">ByResourceGroupAndName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="dc03f-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringReceivedRoute [-ResourceGroupName] <String> -Name <String> [-Prefix <String>] [-AsPath <String>]
 [-OriginAsValidationState <String>] [-RPKIValidationState <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dc03f-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="dc03f-106">ByResourceId</span></span>
```
Get-AzPeeringReceivedRoute [-ResourceId] <String> [-Prefix <String>] [-AsPath <String>]
 [-OriginAsValidationState <String>] [-RPKIValidationState <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dc03f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="dc03f-107">DESCRIPTION</span></span>
<span data-ttu-id="dc03f-108">Wyświetla listę odebranych tras od komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="dc03f-108">Lists recieved routes from a Peering</span></span>

## <span data-ttu-id="dc03f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dc03f-109">EXAMPLES</span></span>

### <span data-ttu-id="dc03f-110">Lista najlepszych 100 odebranych tras dla komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="dc03f-110">List top 100 received routes for a peering</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName
```

<span data-ttu-id="dc03f-111">Wyświetla listę wszystkich odebranych tras dla komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="dc03f-111">Lists all of the received routes for a peering</span></span>

### <span data-ttu-id="dc03f-112">Filtruj według ścieżki</span><span class="sxs-lookup"><span data-stu-id="dc03f-112">Filter by AS Path</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -AsPath "1234 5674 9834"
```

<span data-ttu-id="dc03f-113">Wyświetla listę wszystkich odebranych tras dla komunikacji równorzędnej z filtrem jako</span><span class="sxs-lookup"><span data-stu-id="dc03f-113">Lists all of the received routes for a peering with a filter on AS</span></span> 

### <span data-ttu-id="dc03f-114">Filtruj według RPKIValidationState</span><span class="sxs-lookup"><span data-stu-id="dc03f-114">Filter by RPKIValidationState</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -RPKIValidationState "Valid"
```

<span data-ttu-id="dc03f-115">Wyświetla listę wszystkich odebranych tras dla komunikacji równorzędnej z filtrem na RPKIValidationState</span><span class="sxs-lookup"><span data-stu-id="dc03f-115">Lists all of the received routes for a peering with a filter on RPKIValidationState</span></span>

### <span data-ttu-id="dc03f-116">Filtruj według OriginAsValidationState</span><span class="sxs-lookup"><span data-stu-id="dc03f-116">Filter by OriginAsValidationState</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -OriginAsValidationState "Valid"
```

<span data-ttu-id="dc03f-117">Wyświetla listę wszystkich odebranych tras dla komunikacji równorzędnej z filtrem na OriginAsValidationState</span><span class="sxs-lookup"><span data-stu-id="dc03f-117">Lists all of the received routes for a peering with a filter on OriginAsValidationState</span></span>

## <span data-ttu-id="dc03f-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dc03f-118">PARAMETERS</span></span>

### <span data-ttu-id="dc03f-119">-AsPath</span><span class="sxs-lookup"><span data-stu-id="dc03f-119">-AsPath</span></span>
<span data-ttu-id="dc03f-120">Filtruj według ścieżki.</span><span class="sxs-lookup"><span data-stu-id="dc03f-120">Filter by AS Path.</span></span>
<span data-ttu-id="dc03f-121">Przykład: ' 9342 1234 4567 '</span><span class="sxs-lookup"><span data-stu-id="dc03f-121">Example: '9342 1234 4567'</span></span>

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

### <span data-ttu-id="dc03f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc03f-122">-DefaultProfile</span></span>
<span data-ttu-id="dc03f-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dc03f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc03f-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dc03f-124">-Name</span></span>
<span data-ttu-id="dc03f-125">Unikatowa nazwa PSPeering.</span><span class="sxs-lookup"><span data-stu-id="dc03f-125">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="dc03f-126">-OriginAsValidationState</span><span class="sxs-lookup"><span data-stu-id="dc03f-126">-OriginAsValidationState</span></span>
<span data-ttu-id="dc03f-127">Filtruj według pochodzenia jako stan sprawdzania poprawności.</span><span class="sxs-lookup"><span data-stu-id="dc03f-127">Filter by origin AS validation state.</span></span>

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

### <span data-ttu-id="dc03f-128">-Prefix</span><span class="sxs-lookup"><span data-stu-id="dc03f-128">-Prefix</span></span>
<span data-ttu-id="dc03f-129">Filtruj według prefiksu.</span><span class="sxs-lookup"><span data-stu-id="dc03f-129">Filter by prefix.</span></span>

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

### <span data-ttu-id="dc03f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc03f-130">-ResourceGroupName</span></span>
<span data-ttu-id="dc03f-131">Tworzenie lub używanie istniejącej nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="dc03f-131">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="dc03f-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dc03f-132">-ResourceId</span></span>
<span data-ttu-id="dc03f-133">Nazwa ciągu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="dc03f-133">The resource id string name.</span></span>

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

### <span data-ttu-id="dc03f-134">-RPKIValidationState</span><span class="sxs-lookup"><span data-stu-id="dc03f-134">-RPKIValidationState</span></span>
<span data-ttu-id="dc03f-135">Filtruj według RPKI stan sprawdzania poprawności.</span><span class="sxs-lookup"><span data-stu-id="dc03f-135">Filter by RPKI validation state.</span></span>

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

### <span data-ttu-id="dc03f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc03f-136">CommonParameters</span></span>
<span data-ttu-id="dc03f-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc03f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc03f-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dc03f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc03f-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dc03f-139">INPUTS</span></span>

### <span data-ttu-id="dc03f-140">System. String</span><span class="sxs-lookup"><span data-stu-id="dc03f-140">System.String</span></span>

## <span data-ttu-id="dc03f-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dc03f-141">OUTPUTS</span></span>

### <span data-ttu-id="dc03f-142">Microsoft. Azure. PowerShell. cmdlet. peer. MODELES. PSPeeringReceivedRoute</span><span class="sxs-lookup"><span data-stu-id="dc03f-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringReceivedRoute</span></span>

## <span data-ttu-id="dc03f-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dc03f-143">NOTES</span></span>

## <span data-ttu-id="dc03f-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dc03f-144">RELATED LINKS</span></span>
