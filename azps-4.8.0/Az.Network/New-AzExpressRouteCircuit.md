---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E40CAF2F-ED57-4AC1-8B9A-E48042DD8F91
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuit.md
ms.openlocfilehash: 479b89296ae52221f714992791ed73cd14bf2fe0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221973"
---
# <span data-ttu-id="24fd9-101">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="24fd9-101">New-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="24fd9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="24fd9-102">SYNOPSIS</span></span>
<span data-ttu-id="24fd9-103">Umożliwia utworzenie obwodu trasy usługi Azure Express.</span><span class="sxs-lookup"><span data-stu-id="24fd9-103">Creates an Azure express route circuit.</span></span>

## <span data-ttu-id="24fd9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="24fd9-104">SYNTAX</span></span>

### <span data-ttu-id="24fd9-105">Servicedostarczającego (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="24fd9-105">ServiceProvider (Default)</span></span>
```
New-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String> [-SkuTier <String>]
 [-SkuFamily <String>] -ServiceProviderName <String> -PeeringLocation <String> -BandwidthInMbps <Int32>
 [-Peering <PSPeering[]>] [-Authorization <PSExpressRouteCircuitAuthorization[]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24fd9-106">ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="24fd9-106">ExpressRoutePort</span></span>
```
New-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String> [-SkuTier <String>]
 [-SkuFamily <String>] -ExpressRoutePort <PSExpressRoutePort> -BandwidthInGbps <Double>
 [-Peering <PSPeering[]>] [-Authorization <PSExpressRouteCircuitAuthorization[]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24fd9-107">Opis</span><span class="sxs-lookup"><span data-stu-id="24fd9-107">DESCRIPTION</span></span>
<span data-ttu-id="24fd9-108">Polecenie cmdlet **New-AzExpressRouteCircuit** umożliwia utworzenie obwodu trasy usługi Azure Express.</span><span class="sxs-lookup"><span data-stu-id="24fd9-108">The **New-AzExpressRouteCircuit** cmdlet creates an Azure express route circuit.</span></span>

## <span data-ttu-id="24fd9-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="24fd9-109">EXAMPLES</span></span>

### <span data-ttu-id="24fd9-110">Przykład 1. Tworzenie nowego obwodu ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="24fd9-110">Example 1: Create a new ExpressRoute circuit</span></span>
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

### <span data-ttu-id="24fd9-111">Przykład 2: Tworzenie nowego obwodu ExpressRoute na ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="24fd9-111">Example 2: Create a new ExpressRoute circuit on ExpressRoutePort</span></span>
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

## <span data-ttu-id="24fd9-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="24fd9-112">PARAMETERS</span></span>

### <span data-ttu-id="24fd9-113">-AllowClassicOperations</span><span class="sxs-lookup"><span data-stu-id="24fd9-113">-AllowClassicOperations</span></span>
<span data-ttu-id="24fd9-114">Użycie tego parametru umożliwia korzystanie z klasycznych poleceń cmdlet programu Azure PowerShell do zarządzania obwodem.</span><span class="sxs-lookup"><span data-stu-id="24fd9-114">The use of this parameter allows you to use the classic Azure PowerShell cmdlets to manage the circuit.</span></span>

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

### <span data-ttu-id="24fd9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="24fd9-115">-AsJob</span></span>
<span data-ttu-id="24fd9-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="24fd9-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="24fd9-117">— Autoryzacja</span><span class="sxs-lookup"><span data-stu-id="24fd9-117">-Authorization</span></span>
<span data-ttu-id="24fd9-118">Lista autoryzacji obwodu.</span><span class="sxs-lookup"><span data-stu-id="24fd9-118">A list of circuit authorizations.</span></span>

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

### <span data-ttu-id="24fd9-119">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="24fd9-119">-BandwidthInGbps</span></span>
<span data-ttu-id="24fd9-120">Szerokość pasma obwodu po zainicjowaniu obwodu dla zasobu ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="24fd9-120">The bandwidth of the circuit when the circuit is provisioned on an ExpressRoutePort resource.</span></span>

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

### <span data-ttu-id="24fd9-121">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="24fd9-121">-BandwidthInMbps</span></span>
<span data-ttu-id="24fd9-122">Szerokość pasma obwodu.</span><span class="sxs-lookup"><span data-stu-id="24fd9-122">The bandwidth of the circuit.</span></span> <span data-ttu-id="24fd9-123">To musi być wartość obsługiwana przez dostawcę usługi.</span><span class="sxs-lookup"><span data-stu-id="24fd9-123">This must be a value that is supported by the service provider.</span></span>

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

### <span data-ttu-id="24fd9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24fd9-124">-DefaultProfile</span></span>
<span data-ttu-id="24fd9-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="24fd9-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24fd9-126">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="24fd9-126">-ExpressRoutePort</span></span>
<span data-ttu-id="24fd9-127">Odwołanie do zasobu ExpressRoutePort po zainicjowaniu obwodu dla zasobu ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="24fd9-127">The reference to the ExpressRoutePort resource when the circuit is provisioned on an ExpressRoutePort resource.</span></span>

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

### <span data-ttu-id="24fd9-128">-Force</span><span class="sxs-lookup"><span data-stu-id="24fd9-128">-Force</span></span>
<span data-ttu-id="24fd9-129">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="24fd9-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="24fd9-130">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="24fd9-130">-Location</span></span>
<span data-ttu-id="24fd9-131">Lokalizacja obwodu.</span><span class="sxs-lookup"><span data-stu-id="24fd9-131">The location of the circuit.</span></span>

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

### <span data-ttu-id="24fd9-132">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="24fd9-132">-Name</span></span>
<span data-ttu-id="24fd9-133">Nazwa tworzonego obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="24fd9-133">The name of the ExpressRoute circuit being created.</span></span>

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

### <span data-ttu-id="24fd9-134">-Peer</span><span class="sxs-lookup"><span data-stu-id="24fd9-134">-Peering</span></span>
<span data-ttu-id="24fd9-135">Konfiguracja elementu równorzędnego listy.</span><span class="sxs-lookup"><span data-stu-id="24fd9-135">A list peer configurations.</span></span>

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

### <span data-ttu-id="24fd9-136">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="24fd9-136">-PeeringLocation</span></span>
<span data-ttu-id="24fd9-137">Nazwa lokalizacji komunikacji równorzędnej obsługiwana przez dostawcę usługi.</span><span class="sxs-lookup"><span data-stu-id="24fd9-137">The name of the peering location supported by the service provider.</span></span>

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

### <span data-ttu-id="24fd9-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24fd9-138">-ResourceGroupName</span></span>
<span data-ttu-id="24fd9-139">Grupa zasobów, która będzie zawierać obwód.</span><span class="sxs-lookup"><span data-stu-id="24fd9-139">The resource group that will contain the circuit.</span></span>

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

### <span data-ttu-id="24fd9-140">-Serviceprovidername</span><span class="sxs-lookup"><span data-stu-id="24fd9-140">-ServiceProviderName</span></span>
<span data-ttu-id="24fd9-141">Nazwa dostawcy usługi obwodu.</span><span class="sxs-lookup"><span data-stu-id="24fd9-141">The name of the circuit service provider.</span></span> <span data-ttu-id="24fd9-142">Musi być taka sama jak nazwa wymieniona za pomocą polecenia cmdlet Get-AzExpressRouteServiceProvider.</span><span class="sxs-lookup"><span data-stu-id="24fd9-142">This must match a name listed by the Get-AzExpressRouteServiceProvider cmdlet.</span></span>

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

### <span data-ttu-id="24fd9-143">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="24fd9-143">-SkuFamily</span></span>
<span data-ttu-id="24fd9-144">Rodzina SKU określa typ rozliczeń.</span><span class="sxs-lookup"><span data-stu-id="24fd9-144">SKU family determines the billing type.</span></span> <span data-ttu-id="24fd9-145">Możliwe wartości tego parametru to: `MeteredData` lub `UnlimitedData` .</span><span class="sxs-lookup"><span data-stu-id="24fd9-145">Possible values for this parameter are: `MeteredData` or `UnlimitedData`.</span></span> <span data-ttu-id="24fd9-146">Pamiętaj, że możesz zmienić typ rozliczeń z MeteredData na UnlimitedData, ale nie można zmienić typu z UnlimitedData na MeteredData.</span><span class="sxs-lookup"><span data-stu-id="24fd9-146">Note that you can change the billing type from MeteredData to UnlimitedData, but you can't change the type from UnlimitedData to MeteredData.</span></span>

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

### <span data-ttu-id="24fd9-147">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="24fd9-147">-SkuTier</span></span>
<span data-ttu-id="24fd9-148">Poziom usług dla obwodu.</span><span class="sxs-lookup"><span data-stu-id="24fd9-148">The tier of service for the circuit.</span></span> <span data-ttu-id="24fd9-149">Możliwe wartości tego parametru to: `Standard` `Premium` lub `Local` .</span><span class="sxs-lookup"><span data-stu-id="24fd9-149">Possible values for this parameter are: `Standard`, `Premium` or `Local`.</span></span>

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

### <span data-ttu-id="24fd9-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="24fd9-150">-Tag</span></span>
<span data-ttu-id="24fd9-151">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="24fd9-151">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="24fd9-152">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="24fd9-152">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="24fd9-153">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="24fd9-153">-Confirm</span></span>
<span data-ttu-id="24fd9-154">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24fd9-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24fd9-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24fd9-155">-WhatIf</span></span>
<span data-ttu-id="24fd9-156">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24fd9-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24fd9-157">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="24fd9-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24fd9-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24fd9-158">CommonParameters</span></span>
<span data-ttu-id="24fd9-159">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24fd9-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24fd9-160">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24fd9-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24fd9-161">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="24fd9-161">INPUTS</span></span>

### <span data-ttu-id="24fd9-162">System. String</span><span class="sxs-lookup"><span data-stu-id="24fd9-162">System.String</span></span>

### <span data-ttu-id="24fd9-163">System. Int32</span><span class="sxs-lookup"><span data-stu-id="24fd9-163">System.Int32</span></span>

### <span data-ttu-id="24fd9-164">Microsoft. Azure. Commands. Network. models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="24fd9-164">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="24fd9-165">System. Double</span><span class="sxs-lookup"><span data-stu-id="24fd9-165">System.Double</span></span>

### <span data-ttu-id="24fd9-166">Microsoft. Azure. Commands. Network. models. PSPeering []</span><span class="sxs-lookup"><span data-stu-id="24fd9-166">Microsoft.Azure.Commands.Network.Models.PSPeering[]</span></span>

### <span data-ttu-id="24fd9-167">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuitAuthorization []</span><span class="sxs-lookup"><span data-stu-id="24fd9-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization[]</span></span>

### <span data-ttu-id="24fd9-168">System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="24fd9-168">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="24fd9-169">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="24fd9-169">System.Collections.Hashtable</span></span>

## <span data-ttu-id="24fd9-170">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="24fd9-170">OUTPUTS</span></span>

### <span data-ttu-id="24fd9-171">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="24fd9-171">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="24fd9-172">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="24fd9-172">NOTES</span></span>

## <span data-ttu-id="24fd9-173">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="24fd9-173">RELATED LINKS</span></span>

[<span data-ttu-id="24fd9-174">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="24fd9-174">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="24fd9-175">Przenieś — AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="24fd9-175">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="24fd9-176">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="24fd9-176">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="24fd9-177">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="24fd9-177">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
