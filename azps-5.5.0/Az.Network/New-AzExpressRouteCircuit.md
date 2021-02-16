---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E40CAF2F-ED57-4AC1-8B9A-E48042DD8F91
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuit.md
ms.openlocfilehash: 479b89296ae52221f714992791ed73cd14bf2fe0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184515"
---
# <span data-ttu-id="9b162-101">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9b162-101">New-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="9b162-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b162-102">SYNOPSIS</span></span>
<span data-ttu-id="9b162-103">Tworzy obwód trasy ekspresowej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9b162-103">Creates an Azure express route circuit.</span></span>

## <span data-ttu-id="9b162-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9b162-104">SYNTAX</span></span>

### <span data-ttu-id="9b162-105">ServiceProvider (Default)</span><span class="sxs-lookup"><span data-stu-id="9b162-105">ServiceProvider (Default)</span></span>
```
New-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String> [-SkuTier <String>]
 [-SkuFamily <String>] -ServiceProviderName <String> -PeeringLocation <String> -BandwidthInMbps <Int32>
 [-Peering <PSPeering[]>] [-Authorization <PSExpressRouteCircuitAuthorization[]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b162-106">ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="9b162-106">ExpressRoutePort</span></span>
```
New-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String> [-SkuTier <String>]
 [-SkuFamily <String>] -ExpressRoutePort <PSExpressRoutePort> -BandwidthInGbps <Double>
 [-Peering <PSPeering[]>] [-Authorization <PSExpressRouteCircuitAuthorization[]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b162-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="9b162-107">DESCRIPTION</span></span>
<span data-ttu-id="9b162-108">Polecenie **cmdlet New-AzExpressRouteCircuit** tworzy obwód trasy ekspresowej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9b162-108">The **New-AzExpressRouteCircuit** cmdlet creates an Azure express route circuit.</span></span>

## <span data-ttu-id="9b162-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9b162-109">EXAMPLES</span></span>

### <span data-ttu-id="9b162-110">Przykład 1. Tworzenie nowego obwodu w układzie ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="9b162-110">Example 1: Create a new ExpressRoute circuit</span></span>
```powershell
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

### <span data-ttu-id="9b162-111">Przykład 2. Tworzenie nowego obwodu expressRoute w układzie ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="9b162-111">Example 2: Create a new ExpressRoute circuit on ExpressRoutePort</span></span>
```powershell
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

## <span data-ttu-id="9b162-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b162-112">PARAMETERS</span></span>

### <span data-ttu-id="9b162-113">-AllowClassicOperations</span><span class="sxs-lookup"><span data-stu-id="9b162-113">-AllowClassicOperations</span></span>
<span data-ttu-id="9b162-114">Użycie tego parametru umożliwia zarządzanie obwodem za pomocą klasycznych poleceń cmdlet programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9b162-114">The use of this parameter allows you to use the classic Azure PowerShell cmdlets to manage the circuit.</span></span>

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

### <span data-ttu-id="9b162-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="9b162-115">-AsJob</span></span>
<span data-ttu-id="9b162-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="9b162-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9b162-117">— Autoryzacja</span><span class="sxs-lookup"><span data-stu-id="9b162-117">-Authorization</span></span>
<span data-ttu-id="9b162-118">Lista autoryzacji obwodów.</span><span class="sxs-lookup"><span data-stu-id="9b162-118">A list of circuit authorizations.</span></span>

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

### <span data-ttu-id="9b162-119">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="9b162-119">-BandwidthInGbps</span></span>
<span data-ttu-id="9b162-120">Przepustowość obwodu podczas inicjowania obsługi administracyjnej obwodu w zasobie usługi ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="9b162-120">The bandwidth of the circuit when the circuit is provisioned on an ExpressRoutePort resource.</span></span>

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

### <span data-ttu-id="9b162-121">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="9b162-121">-BandwidthInMbps</span></span>
<span data-ttu-id="9b162-122">Przepustowość obwodu.</span><span class="sxs-lookup"><span data-stu-id="9b162-122">The bandwidth of the circuit.</span></span> <span data-ttu-id="9b162-123">Musi to być wartość obsługiwana przez usługodawca.</span><span class="sxs-lookup"><span data-stu-id="9b162-123">This must be a value that is supported by the service provider.</span></span>

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

### <span data-ttu-id="9b162-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b162-124">-DefaultProfile</span></span>
<span data-ttu-id="9b162-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9b162-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b162-126">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="9b162-126">-ExpressRoutePort</span></span>
<span data-ttu-id="9b162-127">Odwołanie do zasobu ExpressRoutePort, gdy obwód jest aprowowany w zasobie usługi ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="9b162-127">The reference to the ExpressRoutePort resource when the circuit is provisioned on an ExpressRoutePort resource.</span></span>

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

### <span data-ttu-id="9b162-128">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="9b162-128">-Force</span></span>
<span data-ttu-id="9b162-129">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9b162-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9b162-130">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="9b162-130">-Location</span></span>
<span data-ttu-id="9b162-131">Lokalizacja obwodu.</span><span class="sxs-lookup"><span data-stu-id="9b162-131">The location of the circuit.</span></span>

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

### <span data-ttu-id="9b162-132">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9b162-132">-Name</span></span>
<span data-ttu-id="9b162-133">Nazwa tworzonego obwodu expressRoute.</span><span class="sxs-lookup"><span data-stu-id="9b162-133">The name of the ExpressRoute circuit being created.</span></span>

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

### <span data-ttu-id="9b162-134">— Komunikacja równorzędna</span><span class="sxs-lookup"><span data-stu-id="9b162-134">-Peering</span></span>
<span data-ttu-id="9b162-135">Konfiguracje równorzędnych list.</span><span class="sxs-lookup"><span data-stu-id="9b162-135">A list peer configurations.</span></span>

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

### <span data-ttu-id="9b162-136">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="9b162-136">-PeeringLocation</span></span>
<span data-ttu-id="9b162-137">Nazwa lokalizacji komunikacji równorzędnej obsługiwanej przez usługodawca.</span><span class="sxs-lookup"><span data-stu-id="9b162-137">The name of the peering location supported by the service provider.</span></span>

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

### <span data-ttu-id="9b162-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b162-138">-ResourceGroupName</span></span>
<span data-ttu-id="9b162-139">Grupa zasobów, która będzie zawierać obwód.</span><span class="sxs-lookup"><span data-stu-id="9b162-139">The resource group that will contain the circuit.</span></span>

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

### <span data-ttu-id="9b162-140">-ServiceProviderName</span><span class="sxs-lookup"><span data-stu-id="9b162-140">-ServiceProviderName</span></span>
<span data-ttu-id="9b162-141">Nazwa obwodu usługodawca.</span><span class="sxs-lookup"><span data-stu-id="9b162-141">The name of the circuit service provider.</span></span> <span data-ttu-id="9b162-142">Musi to być zgodne z nazwą na liście Get-AzExpressRouteServiceProvider cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b162-142">This must match a name listed by the Get-AzExpressRouteServiceProvider cmdlet.</span></span>

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

### <span data-ttu-id="9b162-143">- SKUFamily</span><span class="sxs-lookup"><span data-stu-id="9b162-143">-SkuFamily</span></span>
<span data-ttu-id="9b162-144">Typ rozliczeń zależy od rodziny sku.</span><span class="sxs-lookup"><span data-stu-id="9b162-144">SKU family determines the billing type.</span></span> <span data-ttu-id="9b162-145">Możliwe wartości dla tego parametru to: `MeteredData` `UnlimitedData` lub.</span><span class="sxs-lookup"><span data-stu-id="9b162-145">Possible values for this parameter are: `MeteredData` or `UnlimitedData`.</span></span> <span data-ttu-id="9b162-146">Pamiętaj, że możesz zmienić typ rozliczeń z Dane taryfowe na Bez ograniczeńData, ale nie możesz zmienić typu z Bez ograniczeńData na Dane taryfowe.</span><span class="sxs-lookup"><span data-stu-id="9b162-146">Note that you can change the billing type from MeteredData to UnlimitedData, but you can't change the type from UnlimitedData to MeteredData.</span></span>

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

### <span data-ttu-id="9b162-147">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="9b162-147">-SkuTier</span></span>
<span data-ttu-id="9b162-148">Warstwa usługi dla obwodu.</span><span class="sxs-lookup"><span data-stu-id="9b162-148">The tier of service for the circuit.</span></span> <span data-ttu-id="9b162-149">Możliwe wartości dla tego parametru to: `Standard` `Premium` `Local` lub.</span><span class="sxs-lookup"><span data-stu-id="9b162-149">Possible values for this parameter are: `Standard`, `Premium` or `Local`.</span></span>

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

### <span data-ttu-id="9b162-150">— Tag</span><span class="sxs-lookup"><span data-stu-id="9b162-150">-Tag</span></span>
<span data-ttu-id="9b162-151">Pary klucz-wartość w postaci tabeli skrótu.</span><span class="sxs-lookup"><span data-stu-id="9b162-151">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="9b162-152">Na przykład: @{key0="value0";key1=$null;key2="wartość2"}</span><span class="sxs-lookup"><span data-stu-id="9b162-152">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="9b162-153">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9b162-153">-Confirm</span></span>
<span data-ttu-id="9b162-154">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9b162-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b162-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b162-155">-WhatIf</span></span>
<span data-ttu-id="9b162-156">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b162-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b162-157">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9b162-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b162-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b162-158">CommonParameters</span></span>
<span data-ttu-id="9b162-159">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b162-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b162-160">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b162-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b162-161">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9b162-161">INPUTS</span></span>

### <span data-ttu-id="9b162-162">System.String</span><span class="sxs-lookup"><span data-stu-id="9b162-162">System.String</span></span>

### <span data-ttu-id="9b162-163">System.Int32</span><span class="sxs-lookup"><span data-stu-id="9b162-163">System.Int32</span></span>

### <span data-ttu-id="9b162-164">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="9b162-164">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="9b162-165">System.Double</span><span class="sxs-lookup"><span data-stu-id="9b162-165">System.Double</span></span>

### <span data-ttu-id="9b162-166">Microsoft.Azure.Commands.Network.Models.PSPeering[]</span><span class="sxs-lookup"><span data-stu-id="9b162-166">Microsoft.Azure.Commands.Network.Models.PSPeering[]</span></span>

### <span data-ttu-id="9b162-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization[]</span><span class="sxs-lookup"><span data-stu-id="9b162-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization[]</span></span>

### <span data-ttu-id="9b162-168">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9b162-168">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="9b162-169">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="9b162-169">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9b162-170">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9b162-170">OUTPUTS</span></span>

### <span data-ttu-id="9b162-171">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9b162-171">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="9b162-172">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9b162-172">NOTES</span></span>

## <span data-ttu-id="9b162-173">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9b162-173">RELATED LINKS</span></span>

[<span data-ttu-id="9b162-174">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9b162-174">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="9b162-175">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9b162-175">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="9b162-176">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9b162-176">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="9b162-177">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9b162-177">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
