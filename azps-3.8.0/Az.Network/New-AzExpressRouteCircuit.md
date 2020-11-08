---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E40CAF2F-ED57-4AC1-8B9A-E48042DD8F91
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuit.md
ms.openlocfilehash: 76888e38487d54c3c7f2796cb49d660872fc5c96
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053716"
---
# <span data-ttu-id="c8176-101">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c8176-101">New-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="c8176-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c8176-102">SYNOPSIS</span></span>
<span data-ttu-id="c8176-103">Umożliwia utworzenie obwodu trasy usługi Azure Express.</span><span class="sxs-lookup"><span data-stu-id="c8176-103">Creates an Azure express route circuit.</span></span>

## <span data-ttu-id="c8176-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c8176-104">SYNTAX</span></span>

### <span data-ttu-id="c8176-105">Servicedostarczającego (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="c8176-105">ServiceProvider (Default)</span></span>
```
New-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String> [-SkuTier <String>]
 [-SkuFamily <String>] -ServiceProviderName <String> -PeeringLocation <String> -BandwidthInMbps <Int32>
 [-Peering <PSPeering[]>] [-Authorization <PSExpressRouteCircuitAuthorization[]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8176-106">ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="c8176-106">ExpressRoutePort</span></span>
```
New-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String> [-SkuTier <String>]
 [-SkuFamily <String>] -ExpressRoutePort <PSExpressRoutePort> -BandwidthInGbps <Double>
 [-Peering <PSPeering[]>] [-Authorization <PSExpressRouteCircuitAuthorization[]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8176-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c8176-107">DESCRIPTION</span></span>
<span data-ttu-id="c8176-108">Polecenie cmdlet **New-AzExpressRouteCircuit** umożliwia utworzenie obwodu trasy usługi Azure Express.</span><span class="sxs-lookup"><span data-stu-id="c8176-108">The **New-AzExpressRouteCircuit** cmdlet creates an Azure express route circuit.</span></span>

## <span data-ttu-id="c8176-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c8176-109">EXAMPLES</span></span>

### <span data-ttu-id="c8176-110">Przykład 1. Tworzenie nowego obwodu ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="c8176-110">Example 1: Create a new ExpressRoute circuit</span></span>
```
$parameters = @{
    Name='ExpressRouteCircuit'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    SkuTier='Standard'
    SkuFamily='MeteredData'
    ServiceProviderName='Equinix'
    PeeringLocation='Silicon Valley'
    BandwidthInMbps=200
}
New-AzExpressRouteCircuit @parameters
```

### <span data-ttu-id="c8176-111">Przykład 2: Tworzenie nowego obwodu ExpressRoute na ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="c8176-111">Example 2: Create a new ExpressRoute circuit on ExpressRoutePort</span></span>
```
$parameters = @{
    Name='ExpressRouteCircuit'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    SkuTier='Standard'
    SkuFamily='MeteredData'
    ExpressRoutePort=$PSExpressRoutePort
    BandwidthInGbps=10.0
}
New-AzExpressRouteCircuit @parameters
```

## <span data-ttu-id="c8176-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c8176-112">PARAMETERS</span></span>

### <span data-ttu-id="c8176-113">-AllowClassicOperations</span><span class="sxs-lookup"><span data-stu-id="c8176-113">-AllowClassicOperations</span></span>
<span data-ttu-id="c8176-114">Użycie tego parametru umożliwia korzystanie z klasycznych poleceń cmdlet programu Azure PowerShell do zarządzania obwodem.</span><span class="sxs-lookup"><span data-stu-id="c8176-114">The use of this parameter allows you to use the classic Azure PowerShell cmdlets to manage the circuit.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8176-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c8176-115">-AsJob</span></span>
<span data-ttu-id="c8176-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="c8176-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c8176-117">— Autoryzacja</span><span class="sxs-lookup"><span data-stu-id="c8176-117">-Authorization</span></span>
<span data-ttu-id="c8176-118">Lista autoryzacji obwodu.</span><span class="sxs-lookup"><span data-stu-id="c8176-118">A list of circuit authorizations.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8176-119">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="c8176-119">-BandwidthInGbps</span></span>
<span data-ttu-id="c8176-120">Szerokość pasma obwodu po zainicjowaniu obwodu dla zasobu ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="c8176-120">The bandwidth of the circuit when the circuit is provisioned on an ExpressRoutePort resource.</span></span>

```yaml
Type: System.Double
Parameter Sets: ExpressRoutePort
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8176-121">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="c8176-121">-BandwidthInMbps</span></span>
<span data-ttu-id="c8176-122">Szerokość pasma obwodu.</span><span class="sxs-lookup"><span data-stu-id="c8176-122">The bandwidth of the circuit.</span></span> <span data-ttu-id="c8176-123">To musi być wartość obsługiwana przez dostawcę usługi.</span><span class="sxs-lookup"><span data-stu-id="c8176-123">This must be a value that is supported by the service provider.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ServiceProvider
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8176-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8176-124">-DefaultProfile</span></span>
<span data-ttu-id="c8176-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c8176-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8176-126">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="c8176-126">-ExpressRoutePort</span></span>
<span data-ttu-id="c8176-127">Odwołanie do zasobu ExpressRoutePort po zainicjowaniu obwodu dla zasobu ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="c8176-127">The reference to the ExpressRoutePort resource when the circuit is provisioned on an ExpressRoutePort resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: ExpressRoutePort
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8176-128">-Force</span><span class="sxs-lookup"><span data-stu-id="c8176-128">-Force</span></span>
<span data-ttu-id="c8176-129">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="c8176-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c8176-130">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="c8176-130">-Location</span></span>
<span data-ttu-id="c8176-131">Lokalizacja obwodu.</span><span class="sxs-lookup"><span data-stu-id="c8176-131">The location of the circuit.</span></span>

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

### <span data-ttu-id="c8176-132">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c8176-132">-Name</span></span>
<span data-ttu-id="c8176-133">Nazwa tworzonego obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="c8176-133">The name of the ExpressRoute circuit being created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8176-134">-Peer</span><span class="sxs-lookup"><span data-stu-id="c8176-134">-Peering</span></span>
<span data-ttu-id="c8176-135">Konfiguracja elementu równorzędnego listy.</span><span class="sxs-lookup"><span data-stu-id="c8176-135">A list peer configurations.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPeering[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8176-136">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="c8176-136">-PeeringLocation</span></span>
<span data-ttu-id="c8176-137">Nazwa lokalizacji komunikacji równorzędnej obsługiwana przez dostawcę usługi.</span><span class="sxs-lookup"><span data-stu-id="c8176-137">The name of the peering location supported by the service provider.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceProvider
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8176-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8176-138">-ResourceGroupName</span></span>
<span data-ttu-id="c8176-139">Grupa zasobów, która będzie zawierać obwód.</span><span class="sxs-lookup"><span data-stu-id="c8176-139">The resource group that will contain the circuit.</span></span>

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

### <span data-ttu-id="c8176-140">-Serviceprovidername</span><span class="sxs-lookup"><span data-stu-id="c8176-140">-ServiceProviderName</span></span>
<span data-ttu-id="c8176-141">Nazwa dostawcy usługi obwodu.</span><span class="sxs-lookup"><span data-stu-id="c8176-141">The name of the circuit service provider.</span></span> <span data-ttu-id="c8176-142">Musi być taka sama jak nazwa wymieniona za pomocą polecenia cmdlet Get-AzExpressRouteServiceProvider.</span><span class="sxs-lookup"><span data-stu-id="c8176-142">This must match a name listed by the Get-AzExpressRouteServiceProvider cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceProvider
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8176-143">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="c8176-143">-SkuFamily</span></span>
<span data-ttu-id="c8176-144">Rodzina SKU określa typ rozliczeń.</span><span class="sxs-lookup"><span data-stu-id="c8176-144">SKU family determines the billing type.</span></span> <span data-ttu-id="c8176-145">Możliwe wartości tego parametru to: `MeteredData` lub `UnlimitedData` .</span><span class="sxs-lookup"><span data-stu-id="c8176-145">Possible values for this parameter are: `MeteredData` or `UnlimitedData`.</span></span> <span data-ttu-id="c8176-146">Pamiętaj, że możesz zmienić typ rozliczeń z MeteredData na UnlimitedData, ale nie można zmienić typu z UnlimitedData na MeteredData.</span><span class="sxs-lookup"><span data-stu-id="c8176-146">Note that you can change the billing type from MeteredData to UnlimitedData, but you can't change the type from UnlimitedData to MeteredData.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: MeteredData, UnlimitedData

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8176-147">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="c8176-147">-SkuTier</span></span>
<span data-ttu-id="c8176-148">Poziom usług dla obwodu.</span><span class="sxs-lookup"><span data-stu-id="c8176-148">The tier of service for the circuit.</span></span> <span data-ttu-id="c8176-149">Możliwe wartości tego parametru to: `Standard` `Premium` lub `Local` .</span><span class="sxs-lookup"><span data-stu-id="c8176-149">Possible values for this parameter are: `Standard`, `Premium` or `Local`.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium, Local

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8176-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="c8176-150">-Tag</span></span>
<span data-ttu-id="c8176-151">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="c8176-151">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c8176-152">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="c8176-152">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c8176-153">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c8176-153">-Confirm</span></span>
<span data-ttu-id="c8176-154">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8176-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8176-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8176-155">-WhatIf</span></span>
<span data-ttu-id="c8176-156">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8176-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8176-157">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c8176-157">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8176-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8176-158">CommonParameters</span></span>
<span data-ttu-id="c8176-159">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8176-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8176-160">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8176-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8176-161">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c8176-161">INPUTS</span></span>

### <span data-ttu-id="c8176-162">System. String</span><span class="sxs-lookup"><span data-stu-id="c8176-162">System.String</span></span>

### <span data-ttu-id="c8176-163">System. Int32</span><span class="sxs-lookup"><span data-stu-id="c8176-163">System.Int32</span></span>

### <span data-ttu-id="c8176-164">Microsoft. Azure. Commands. Network. models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="c8176-164">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="c8176-165">System. Double</span><span class="sxs-lookup"><span data-stu-id="c8176-165">System.Double</span></span>

### <span data-ttu-id="c8176-166">Microsoft. Azure. Commands. Network. models. PSPeering []</span><span class="sxs-lookup"><span data-stu-id="c8176-166">Microsoft.Azure.Commands.Network.Models.PSPeering[]</span></span>

### <span data-ttu-id="c8176-167">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuitAuthorization []</span><span class="sxs-lookup"><span data-stu-id="c8176-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization[]</span></span>

### <span data-ttu-id="c8176-168">System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c8176-168">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="c8176-169">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c8176-169">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c8176-170">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c8176-170">OUTPUTS</span></span>

### <span data-ttu-id="c8176-171">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c8176-171">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="c8176-172">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c8176-172">NOTES</span></span>

## <span data-ttu-id="c8176-173">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c8176-173">RELATED LINKS</span></span>

[<span data-ttu-id="c8176-174">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c8176-174">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="c8176-175">Przenieś — AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c8176-175">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="c8176-176">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c8176-176">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="c8176-177">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c8176-177">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
