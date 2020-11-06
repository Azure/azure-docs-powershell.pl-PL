---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRoutePort.md
ms.openlocfilehash: 8d3b204815fc273f97a549582a193002f5f4a48d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543684"
---
# <span data-ttu-id="41592-101">New-AzureRmExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="41592-101">New-AzureRmExpressRoutePort</span></span>

## <span data-ttu-id="41592-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="41592-102">SYNOPSIS</span></span>
<span data-ttu-id="41592-103">Tworzy usługę Azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="41592-103">Creates an Azure ExpressRoutePort.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41592-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="41592-104">SYNTAX</span></span>

### <span data-ttu-id="41592-105">ResourceNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="41592-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzureRmExpressRoutePort -ResourceGroupName <String> -Name <String> -PeeringLocation <String>
 -BandwidthInGbps <Int32> -Encapsulation <String> -Location <String> [-Tag <Hashtable>]
 [-Link <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink]>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41592-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="41592-106">ResourceIdParameterSet</span></span>
```
New-AzureRmExpressRoutePort -ResourceId <String> -PeeringLocation <String> -BandwidthInGbps <Int32>
 -Encapsulation <String> -Location <String> [-Tag <Hashtable>]
 [-Link <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink]>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41592-107">Opis</span><span class="sxs-lookup"><span data-stu-id="41592-107">DESCRIPTION</span></span>
<span data-ttu-id="41592-108">Polecenie cmdlet **New-AzureRmExpressRoutePort** tworzy składnik Azure ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="41592-108">The **New-AzureRmExpressRoutePort** cmdlet creates an Azure ExpressRoutePort</span></span>

## <span data-ttu-id="41592-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="41592-109">EXAMPLES</span></span>

### <span data-ttu-id="41592-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="41592-110">Example 1</span></span>
```powershell
PS C:\> $parameters = @{
    Name='ExpressRoutePort'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    PeeringLocation='Silicon Valley'
    BandwidthInGbps=100
    Encapsulation='QinQ'
}
PS C:\> New-AzureRmExpressRoutePort @parameters
```

### <span data-ttu-id="41592-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="41592-111">Example 2</span></span>
```powershell
PS C:\> $parameters = @{
    ResourceId='/subscriptions/<SubId>/resourceGroups/<ResourceGroupName>/providers/Microsoft.Network/expressRoutePorts/<PortName>'
    Location='West US'
    PeeringLocation='Silicon Valley'
    BandwidthInGbps=100
    Encapsulation='QinQ'
}
PS C:\> New-AzureRmExpressRoutePort @parameters
```

## <span data-ttu-id="41592-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="41592-112">PARAMETERS</span></span>

### <span data-ttu-id="41592-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="41592-113">-AsJob</span></span>
<span data-ttu-id="41592-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="41592-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="41592-115">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="41592-115">-BandwidthInGbps</span></span>
<span data-ttu-id="41592-116">Przepustowość nazyskanych portów w GB/s</span><span class="sxs-lookup"><span data-stu-id="41592-116">Bandwidth of procured ports in Gbps</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41592-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41592-117">-DefaultProfile</span></span>
<span data-ttu-id="41592-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="41592-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41592-119">-Hermetyzacja</span><span class="sxs-lookup"><span data-stu-id="41592-119">-Encapsulation</span></span>
<span data-ttu-id="41592-120">Metoda kapsułowania na portach fizycznych.</span><span class="sxs-lookup"><span data-stu-id="41592-120">Encapsulation method on physical ports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41592-121">-Force</span><span class="sxs-lookup"><span data-stu-id="41592-121">-Force</span></span>
<span data-ttu-id="41592-122">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="41592-122">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="41592-123">-Link</span><span class="sxs-lookup"><span data-stu-id="41592-123">-Link</span></span>
<span data-ttu-id="41592-124">Zestaw linków fizycznych zasobu ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="41592-124">The set of physical links of the ExpressRoutePort resource</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41592-125">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="41592-125">-Location</span></span>
<span data-ttu-id="41592-126">Lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="41592-126">The location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41592-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="41592-127">-Name</span></span>
<span data-ttu-id="41592-128">Nazwa ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="41592-128">The name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41592-129">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="41592-129">-PeeringLocation</span></span>
<span data-ttu-id="41592-130">Nazwa lokalizacji równorzędnej, w której ExpressRoutePort jest mapowana fizycznie.</span><span class="sxs-lookup"><span data-stu-id="41592-130">The name of the peering location that the ExpressRoutePort is mapped to physically.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41592-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41592-131">-ResourceGroupName</span></span>
<span data-ttu-id="41592-132">Nazwa grupy zasobów ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="41592-132">The resource group name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41592-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="41592-133">-ResourceId</span></span>
<span data-ttu-id="41592-134">Identyfikator zasobu Express Route port.</span><span class="sxs-lookup"><span data-stu-id="41592-134">ResourceId of the express route port.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41592-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="41592-135">-Tag</span></span>
<span data-ttu-id="41592-136">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="41592-136">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41592-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="41592-137">-Confirm</span></span>
<span data-ttu-id="41592-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41592-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41592-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41592-139">-WhatIf</span></span>
<span data-ttu-id="41592-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41592-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41592-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="41592-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41592-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41592-142">CommonParameters</span></span>
<span data-ttu-id="41592-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41592-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41592-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41592-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41592-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="41592-145">INPUTS</span></span>

### <span data-ttu-id="41592-146">System. String</span><span class="sxs-lookup"><span data-stu-id="41592-146">System.String</span></span>

### <span data-ttu-id="41592-147">System. Int32</span><span class="sxs-lookup"><span data-stu-id="41592-147">System.Int32</span></span>

### <span data-ttu-id="41592-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="41592-148">System.Collections.Hashtable</span></span>

### <span data-ttu-id="41592-149">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. Network. MODELES. PSExpressRouteLink; Microsoft. Azure. Commands. Network, Version = 6.3.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="41592-149">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink, Microsoft.Azure.Commands.Network, Version=6.3.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="41592-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="41592-150">OUTPUTS</span></span>

### <span data-ttu-id="41592-151">Microsoft. Azure. Commands. Network. models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="41592-151">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="41592-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="41592-152">NOTES</span></span>

## <span data-ttu-id="41592-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="41592-153">RELATED LINKS</span></span>
