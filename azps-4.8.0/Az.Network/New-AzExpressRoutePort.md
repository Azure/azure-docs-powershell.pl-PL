---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePort.md
ms.openlocfilehash: 54cdcbbd1d9564dde4fbe4a9aa0b0bea8a0325a3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223828"
---
# <span data-ttu-id="fbee9-101">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="fbee9-101">New-AzExpressRoutePort</span></span>

## <span data-ttu-id="fbee9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fbee9-102">SYNOPSIS</span></span>
<span data-ttu-id="fbee9-103">Tworzy usługę Azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="fbee9-103">Creates an Azure ExpressRoutePort.</span></span>

## <span data-ttu-id="fbee9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fbee9-104">SYNTAX</span></span>

### <span data-ttu-id="fbee9-105">ResourceNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="fbee9-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzExpressRoutePort -ResourceGroupName <String> -Name <String> -PeeringLocation <String>
 -BandwidthInGbps <Int32> -Encapsulation <String> -Location <String> [-Tag <Hashtable>]
 [-Link <PSExpressRouteLink[]>] [-Force] [-AsJob] [-Identity <PSManagedServiceIdentity>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbee9-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fbee9-106">ResourceIdParameterSet</span></span>
```
New-AzExpressRoutePort -ResourceId <String> -PeeringLocation <String> -BandwidthInGbps <Int32>
 -Encapsulation <String> -Location <String> [-Tag <Hashtable>] [-Link <PSExpressRouteLink[]>] [-Force] [-AsJob]
 [-Identity <PSManagedServiceIdentity>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fbee9-107">Opis</span><span class="sxs-lookup"><span data-stu-id="fbee9-107">DESCRIPTION</span></span>
<span data-ttu-id="fbee9-108">Polecenie cmdlet **New-AzExpressRoutePort** tworzy składnik Azure ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="fbee9-108">The **New-AzExpressRoutePort** cmdlet creates an Azure ExpressRoutePort</span></span>

## <span data-ttu-id="fbee9-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fbee9-109">EXAMPLES</span></span>

### <span data-ttu-id="fbee9-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fbee9-110">Example 1</span></span>
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

### <span data-ttu-id="fbee9-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="fbee9-111">Example 2</span></span>
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

## <span data-ttu-id="fbee9-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fbee9-112">PARAMETERS</span></span>

### <span data-ttu-id="fbee9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fbee9-113">-AsJob</span></span>
<span data-ttu-id="fbee9-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="fbee9-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fbee9-115">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="fbee9-115">-BandwidthInGbps</span></span>
<span data-ttu-id="fbee9-116">Przepustowość nazyskanych portów w GB/s</span><span class="sxs-lookup"><span data-stu-id="fbee9-116">Bandwidth of procured ports in Gbps</span></span>

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

### <span data-ttu-id="fbee9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbee9-117">-DefaultProfile</span></span>
<span data-ttu-id="fbee9-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fbee9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbee9-119">-Hermetyzacja</span><span class="sxs-lookup"><span data-stu-id="fbee9-119">-Encapsulation</span></span>
<span data-ttu-id="fbee9-120">Metoda kapsułowania na portach fizycznych.</span><span class="sxs-lookup"><span data-stu-id="fbee9-120">Encapsulation method on physical ports.</span></span>

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

### <span data-ttu-id="fbee9-121">-Force</span><span class="sxs-lookup"><span data-stu-id="fbee9-121">-Force</span></span>
<span data-ttu-id="fbee9-122">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="fbee9-122">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="fbee9-123">-Identity (tożsamość)</span><span class="sxs-lookup"><span data-stu-id="fbee9-123">-Identity</span></span>
<span data-ttu-id="fbee9-124">Tożsamość przypisana przez użytkownika do czytania konfiguracji MacSec</span><span class="sxs-lookup"><span data-stu-id="fbee9-124">User Assigned Identity for reading MacSec configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbee9-125">-Link</span><span class="sxs-lookup"><span data-stu-id="fbee9-125">-Link</span></span>
<span data-ttu-id="fbee9-126">Zestaw linków fizycznych zasobu ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="fbee9-126">The set of physical links of the ExpressRoutePort resource</span></span>

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

### <span data-ttu-id="fbee9-127">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="fbee9-127">-Location</span></span>
<span data-ttu-id="fbee9-128">Lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="fbee9-128">The location.</span></span>

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

### <span data-ttu-id="fbee9-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fbee9-129">-Name</span></span>
<span data-ttu-id="fbee9-130">Nazwa ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="fbee9-130">The name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="fbee9-131">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="fbee9-131">-PeeringLocation</span></span>
<span data-ttu-id="fbee9-132">Nazwa lokalizacji równorzędnej, w której ExpressRoutePort jest mapowana fizycznie.</span><span class="sxs-lookup"><span data-stu-id="fbee9-132">The name of the peering location that the ExpressRoutePort is mapped to physically.</span></span>

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

### <span data-ttu-id="fbee9-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbee9-133">-ResourceGroupName</span></span>
<span data-ttu-id="fbee9-134">Nazwa grupy zasobów ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="fbee9-134">The resource group name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="fbee9-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fbee9-135">-ResourceId</span></span>
<span data-ttu-id="fbee9-136">Identyfikator zasobu Express Route port.</span><span class="sxs-lookup"><span data-stu-id="fbee9-136">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="fbee9-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="fbee9-137">-Tag</span></span>
<span data-ttu-id="fbee9-138">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="fbee9-138">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="fbee9-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fbee9-139">-Confirm</span></span>
<span data-ttu-id="fbee9-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbee9-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbee9-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbee9-141">-WhatIf</span></span>
<span data-ttu-id="fbee9-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbee9-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbee9-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fbee9-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbee9-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbee9-144">CommonParameters</span></span>
<span data-ttu-id="fbee9-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbee9-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbee9-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbee9-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbee9-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fbee9-147">INPUTS</span></span>

### <span data-ttu-id="fbee9-148">System. String</span><span class="sxs-lookup"><span data-stu-id="fbee9-148">System.String</span></span>

### <span data-ttu-id="fbee9-149">System. Int32</span><span class="sxs-lookup"><span data-stu-id="fbee9-149">System.Int32</span></span>

### <span data-ttu-id="fbee9-150">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="fbee9-150">System.Collections.Hashtable</span></span>

### <span data-ttu-id="fbee9-151">Microsoft. Azure. Commands. Network. models. PSExpressRouteLink []</span><span class="sxs-lookup"><span data-stu-id="fbee9-151">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink[]</span></span>

## <span data-ttu-id="fbee9-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fbee9-152">OUTPUTS</span></span>

### <span data-ttu-id="fbee9-153">Microsoft. Azure. Commands. Network. models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="fbee9-153">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="fbee9-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fbee9-154">NOTES</span></span>

## <span data-ttu-id="fbee9-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fbee9-155">RELATED LINKS</span></span>

[<span data-ttu-id="fbee9-156">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="fbee9-156">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="fbee9-157">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="fbee9-157">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)

[<span data-ttu-id="fbee9-158">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="fbee9-158">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)
