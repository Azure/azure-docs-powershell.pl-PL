---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePort.md
ms.openlocfilehash: 7f6b68b02644b8244459398028680c9872fffa84
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709312"
---
# <span data-ttu-id="75ad3-101">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="75ad3-101">New-AzExpressRoutePort</span></span>

## <span data-ttu-id="75ad3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="75ad3-102">SYNOPSIS</span></span>
<span data-ttu-id="75ad3-103">Tworzy usługę Azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="75ad3-103">Creates an Azure ExpressRoutePort.</span></span>

## <span data-ttu-id="75ad3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="75ad3-104">SYNTAX</span></span>

### <span data-ttu-id="75ad3-105">ResourceNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="75ad3-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzExpressRoutePort -ResourceGroupName <String> -Name <String> -PeeringLocation <String>
 -BandwidthInGbps <Int32> -Encapsulation <String> -Location <String> [-Tag <Hashtable>]
 [-Link <PSExpressRouteLink[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75ad3-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="75ad3-106">ResourceIdParameterSet</span></span>
```
New-AzExpressRoutePort -ResourceId <String> -PeeringLocation <String> -BandwidthInGbps <Int32>
 -Encapsulation <String> -Location <String> [-Tag <Hashtable>] [-Link <PSExpressRouteLink[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75ad3-107">Opis</span><span class="sxs-lookup"><span data-stu-id="75ad3-107">DESCRIPTION</span></span>
<span data-ttu-id="75ad3-108">Polecenie cmdlet **New-AzExpressRoutePort** tworzy składnik Azure ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="75ad3-108">The **New-AzExpressRoutePort** cmdlet creates an Azure ExpressRoutePort</span></span>

## <span data-ttu-id="75ad3-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="75ad3-109">EXAMPLES</span></span>

### <span data-ttu-id="75ad3-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="75ad3-110">Example 1</span></span>
```powershell
PS C:\> $parameters = @{
    Name='ExpressRoutePort'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    PeeringLocation='Silicon Valley'
    BandwidthInGbps=100
    Encapsulation='QinQ'
}
PS C:\> New-AzExpressRoutePort @parameters
```

### <span data-ttu-id="75ad3-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="75ad3-111">Example 2</span></span>
```powershell
PS C:\> $parameters = @{
    ResourceId='/subscriptions/<SubId>/resourceGroups/<ResourceGroupName>/providers/Microsoft.Network/expressRoutePorts/<PortName>'
    Location='West US'
    PeeringLocation='Silicon Valley'
    BandwidthInGbps=100
    Encapsulation='QinQ'
}
PS C:\> New-AzExpressRoutePort @parameters
```

## <span data-ttu-id="75ad3-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="75ad3-112">PARAMETERS</span></span>

### <span data-ttu-id="75ad3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="75ad3-113">-AsJob</span></span>
<span data-ttu-id="75ad3-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="75ad3-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="75ad3-115">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="75ad3-115">-BandwidthInGbps</span></span>
<span data-ttu-id="75ad3-116">Przepustowość nazyskanych portów w GB/s</span><span class="sxs-lookup"><span data-stu-id="75ad3-116">Bandwidth of procured ports in Gbps</span></span>

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

### <span data-ttu-id="75ad3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75ad3-117">-DefaultProfile</span></span>
<span data-ttu-id="75ad3-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="75ad3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75ad3-119">-Hermetyzacja</span><span class="sxs-lookup"><span data-stu-id="75ad3-119">-Encapsulation</span></span>
<span data-ttu-id="75ad3-120">Metoda kapsułowania na portach fizycznych.</span><span class="sxs-lookup"><span data-stu-id="75ad3-120">Encapsulation method on physical ports.</span></span>

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

### <span data-ttu-id="75ad3-121">-Force</span><span class="sxs-lookup"><span data-stu-id="75ad3-121">-Force</span></span>
<span data-ttu-id="75ad3-122">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="75ad3-122">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="75ad3-123">-Link</span><span class="sxs-lookup"><span data-stu-id="75ad3-123">-Link</span></span>
<span data-ttu-id="75ad3-124">Zestaw linków fizycznych zasobu ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="75ad3-124">The set of physical links of the ExpressRoutePort resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75ad3-125">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="75ad3-125">-Location</span></span>
<span data-ttu-id="75ad3-126">Lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="75ad3-126">The location.</span></span>

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

### <span data-ttu-id="75ad3-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="75ad3-127">-Name</span></span>
<span data-ttu-id="75ad3-128">Nazwa ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="75ad3-128">The name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="75ad3-129">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="75ad3-129">-PeeringLocation</span></span>
<span data-ttu-id="75ad3-130">Nazwa lokalizacji równorzędnej, w której ExpressRoutePort jest mapowana fizycznie.</span><span class="sxs-lookup"><span data-stu-id="75ad3-130">The name of the peering location that the ExpressRoutePort is mapped to physically.</span></span>

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

### <span data-ttu-id="75ad3-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75ad3-131">-ResourceGroupName</span></span>
<span data-ttu-id="75ad3-132">Nazwa grupy zasobów ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="75ad3-132">The resource group name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="75ad3-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75ad3-133">-ResourceId</span></span>
<span data-ttu-id="75ad3-134">Identyfikator zasobu Express Route port.</span><span class="sxs-lookup"><span data-stu-id="75ad3-134">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="75ad3-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="75ad3-135">-Tag</span></span>
<span data-ttu-id="75ad3-136">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="75ad3-136">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="75ad3-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="75ad3-137">-Confirm</span></span>
<span data-ttu-id="75ad3-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75ad3-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75ad3-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75ad3-139">-WhatIf</span></span>
<span data-ttu-id="75ad3-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75ad3-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75ad3-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="75ad3-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75ad3-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75ad3-142">CommonParameters</span></span>
<span data-ttu-id="75ad3-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75ad3-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75ad3-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75ad3-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75ad3-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="75ad3-145">INPUTS</span></span>

### <span data-ttu-id="75ad3-146">System. String</span><span class="sxs-lookup"><span data-stu-id="75ad3-146">System.String</span></span>

### <span data-ttu-id="75ad3-147">System. Int32</span><span class="sxs-lookup"><span data-stu-id="75ad3-147">System.Int32</span></span>

### <span data-ttu-id="75ad3-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="75ad3-148">System.Collections.Hashtable</span></span>

### <span data-ttu-id="75ad3-149">Microsoft. Azure. Commands. Network. models. PSExpressRouteLink []</span><span class="sxs-lookup"><span data-stu-id="75ad3-149">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink[]</span></span>

## <span data-ttu-id="75ad3-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="75ad3-150">OUTPUTS</span></span>

### <span data-ttu-id="75ad3-151">Microsoft. Azure. Commands. Network. models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="75ad3-151">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="75ad3-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="75ad3-152">NOTES</span></span>

## <span data-ttu-id="75ad3-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="75ad3-153">RELATED LINKS</span></span>

[<span data-ttu-id="75ad3-154">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="75ad3-154">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="75ad3-155">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="75ad3-155">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)

[<span data-ttu-id="75ad3-156">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="75ad3-156">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)
