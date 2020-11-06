---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E40CAF2F-ED57-4AC1-8B9A-E48042DD8F91
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: cee0318367ad764a9cc9e37995f092462cd157a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545075"
---
# <span data-ttu-id="de3b8-101">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="de3b8-101">New-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="de3b8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="de3b8-102">SYNOPSIS</span></span>
<span data-ttu-id="de3b8-103">Umożliwia utworzenie obwodu trasy usługi Azure Express.</span><span class="sxs-lookup"><span data-stu-id="de3b8-103">Creates an Azure express route circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de3b8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="de3b8-104">SYNTAX</span></span>

### <span data-ttu-id="de3b8-105">Servicedostarczający</span><span class="sxs-lookup"><span data-stu-id="de3b8-105">ServiceProvider</span></span>
```
New-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 [-SkuTier <String>] [-SkuFamily <String>] [-ServiceProviderName <String>] [-PeeringLocation <String>]
 [-BandwidthInMbps <Int32>]
 [-Peering <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPeering]>]
 [-Authorization <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de3b8-106">ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="de3b8-106">ExpressRoutePort</span></span>
```
New-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 [-SkuTier <String>] [-SkuFamily <String>] [-ExpressRoutePort <PSExpressRoutePort>] [-BandwidthInGbps <Double>]
 [-Peering <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPeering]>]
 [-Authorization <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de3b8-107">Opis</span><span class="sxs-lookup"><span data-stu-id="de3b8-107">DESCRIPTION</span></span>
<span data-ttu-id="de3b8-108">Polecenie cmdlet **New-AzureRmExpressRouteCircuit** umożliwia utworzenie obwodu trasy usługi Azure Express.</span><span class="sxs-lookup"><span data-stu-id="de3b8-108">The **New-AzureRmExpressRouteCircuit** cmdlet creates an Azure express route circuit.</span></span>

## <span data-ttu-id="de3b8-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="de3b8-109">EXAMPLES</span></span>

### <span data-ttu-id="de3b8-110">Przykład 1. Tworzenie nowego obwodu ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="de3b8-110">Example 1: Create a new ExpressRoute circuit</span></span>
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
New-AzureRmExpressRouteCircuit @parameters
```

### <span data-ttu-id="de3b8-111">Przykład 2: Tworzenie nowego obwodu ExpressRoute na ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="de3b8-111">Example 2: Create a new ExpressRoute circuit on ExpressRoutePort</span></span>
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
New-AzureRmExpressRouteCircuit @parameters
```

## <span data-ttu-id="de3b8-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="de3b8-112">PARAMETERS</span></span>

### <span data-ttu-id="de3b8-113">-AllowClassicOperations</span><span class="sxs-lookup"><span data-stu-id="de3b8-113">-AllowClassicOperations</span></span>
<span data-ttu-id="de3b8-114">Użycie tego parametru umożliwia korzystanie z klasycznych poleceń cmdlet programu Azure PowerShell do zarządzania obwodem.</span><span class="sxs-lookup"><span data-stu-id="de3b8-114">The use of this parameter allows you to use the classic Azure PowerShell cmdlets to manage the circuit.</span></span>

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

### <span data-ttu-id="de3b8-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="de3b8-115">-AsJob</span></span>
<span data-ttu-id="de3b8-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="de3b8-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="de3b8-117">— Autoryzacja</span><span class="sxs-lookup"><span data-stu-id="de3b8-117">-Authorization</span></span>
<span data-ttu-id="de3b8-118">Lista autoryzacji obwodu.</span><span class="sxs-lookup"><span data-stu-id="de3b8-118">A list of circuit authorizations.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de3b8-119">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="de3b8-119">-BandwidthInGbps</span></span>
<span data-ttu-id="de3b8-120">Szerokość pasma obwodu po zainicjowaniu obwodu dla zasobu ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="de3b8-120">The bandwidth of the circuit when the circuit is provisioned on an ExpressRoutePort resource.</span></span>

```yaml
Type: Double
Parameter Sets: ExpressRoutePort
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de3b8-121">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="de3b8-121">-BandwidthInMbps</span></span>
<span data-ttu-id="de3b8-122">Szerokość pasma obwodu.</span><span class="sxs-lookup"><span data-stu-id="de3b8-122">The bandwidth of the circuit.</span></span> <span data-ttu-id="de3b8-123">To musi być wartość obsługiwana przez dostawcę usługi.</span><span class="sxs-lookup"><span data-stu-id="de3b8-123">This must be a value that is supported by the service provider.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ServiceProvider
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de3b8-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de3b8-124">-DefaultProfile</span></span>
<span data-ttu-id="de3b8-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="de3b8-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de3b8-126">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="de3b8-126">-ExpressRoutePort</span></span>
<span data-ttu-id="de3b8-127">Odwołanie do zasobu ExpressRoutePort po zainicjowaniu obwodu dla zasobu ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="de3b8-127">The reference to the ExpressRoutePort resource when the circuit is provisioned on an ExpressRoutePort resource.</span></span>

```yaml
Type: PSExpressRoutePort
Parameter Sets: ExpressRoutePort
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de3b8-128">-Force</span><span class="sxs-lookup"><span data-stu-id="de3b8-128">-Force</span></span>
<span data-ttu-id="de3b8-129">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="de3b8-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="de3b8-130">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="de3b8-130">-Location</span></span>
<span data-ttu-id="de3b8-131">Lokalizacja obwodu.</span><span class="sxs-lookup"><span data-stu-id="de3b8-131">The location of the circuit.</span></span>

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

### <span data-ttu-id="de3b8-132">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="de3b8-132">-Name</span></span>
<span data-ttu-id="de3b8-133">Nazwa tworzonego obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="de3b8-133">The name of the ExpressRoute circuit being created.</span></span>

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

### <span data-ttu-id="de3b8-134">-Peer</span><span class="sxs-lookup"><span data-stu-id="de3b8-134">-Peering</span></span>
<span data-ttu-id="de3b8-135">Konfiguracja elementu równorzędnego listy.</span><span class="sxs-lookup"><span data-stu-id="de3b8-135">A list peer configurations.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPeering]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de3b8-136">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="de3b8-136">-PeeringLocation</span></span>
<span data-ttu-id="de3b8-137">Nazwa lokalizacji komunikacji równorzędnej obsługiwana przez dostawcę usługi.</span><span class="sxs-lookup"><span data-stu-id="de3b8-137">The name of the peering location supported by the service provider.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceProvider
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de3b8-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de3b8-138">-ResourceGroupName</span></span>
<span data-ttu-id="de3b8-139">Grupa zasobów, która będzie zawierać obwód.</span><span class="sxs-lookup"><span data-stu-id="de3b8-139">The resource group that will contain the circuit.</span></span>

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

### <span data-ttu-id="de3b8-140">-Serviceprovidername</span><span class="sxs-lookup"><span data-stu-id="de3b8-140">-ServiceProviderName</span></span>
<span data-ttu-id="de3b8-141">Nazwa dostawcy usługi obwodu.</span><span class="sxs-lookup"><span data-stu-id="de3b8-141">The name of the circuit service provider.</span></span> <span data-ttu-id="de3b8-142">Musi być taka sama jak nazwa wymieniona za pomocą polecenia cmdlet Get-AzureRmExpressRouteServiceProvider.</span><span class="sxs-lookup"><span data-stu-id="de3b8-142">This must match a name listed by the Get-AzureRmExpressRouteServiceProvider cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceProvider
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de3b8-143">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="de3b8-143">-SkuFamily</span></span>
<span data-ttu-id="de3b8-144">Rodzina SKU określa typ rozliczeń.</span><span class="sxs-lookup"><span data-stu-id="de3b8-144">SKU family determines the billing type.</span></span> <span data-ttu-id="de3b8-145">Możliwe wartości tego parametru to: `MeteredData` lub `UnlimitedData` .</span><span class="sxs-lookup"><span data-stu-id="de3b8-145">Possible values for this parameter are: `MeteredData` or `UnlimitedData`.</span></span> <span data-ttu-id="de3b8-146">Pamiętaj, że możesz zmienić typ rozliczeń z MeteredData na UnlimitedData, ale nie można zmienić typu z UnlimitedData na MeteredData.</span><span class="sxs-lookup"><span data-stu-id="de3b8-146">Note that you can change the billing type from MeteredData to UnlimitedData, but you can't change the type from UnlimitedData to MeteredData.</span></span>

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

### <span data-ttu-id="de3b8-147">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="de3b8-147">-SkuTier</span></span>
<span data-ttu-id="de3b8-148">Poziom usług dla obwodu.</span><span class="sxs-lookup"><span data-stu-id="de3b8-148">The tier of service for the circuit.</span></span> <span data-ttu-id="de3b8-149">Możliwe wartości tego parametru to: `Standard` lub `Premium` .</span><span class="sxs-lookup"><span data-stu-id="de3b8-149">Possible values for this parameter are: `Standard` or `Premium`.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de3b8-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="de3b8-150">-Tag</span></span>
<span data-ttu-id="de3b8-151">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="de3b8-151">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="de3b8-152">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="de3b8-152">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="de3b8-153">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="de3b8-153">-Confirm</span></span>
<span data-ttu-id="de3b8-154">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de3b8-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de3b8-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de3b8-155">-WhatIf</span></span>
<span data-ttu-id="de3b8-156">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de3b8-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de3b8-157">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="de3b8-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de3b8-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de3b8-158">CommonParameters</span></span>
<span data-ttu-id="de3b8-159">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de3b8-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de3b8-160">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de3b8-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de3b8-161">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="de3b8-161">INPUTS</span></span>

### <span data-ttu-id="de3b8-162">System. String</span><span class="sxs-lookup"><span data-stu-id="de3b8-162">System.String</span></span>

### <span data-ttu-id="de3b8-163">System. Int32</span><span class="sxs-lookup"><span data-stu-id="de3b8-163">System.Int32</span></span>

### <span data-ttu-id="de3b8-164">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. Network. MODELES. PSPeering; Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="de3b8-164">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSPeering, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="de3b8-165">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. Network. MODELES. PSExpressRouteCircuitAuthorization; Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="de3b8-165">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="de3b8-166">System. Nullable "1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="de3b8-166">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="de3b8-167">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="de3b8-167">System.Collections.Hashtable</span></span>

## <span data-ttu-id="de3b8-168">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="de3b8-168">OUTPUTS</span></span>

### <span data-ttu-id="de3b8-169">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="de3b8-169">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="de3b8-170">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="de3b8-170">NOTES</span></span>

## <span data-ttu-id="de3b8-171">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="de3b8-171">RELATED LINKS</span></span>

[<span data-ttu-id="de3b8-172">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="de3b8-172">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="de3b8-173">Przenieś — AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="de3b8-173">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="de3b8-174">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="de3b8-174">Remove-AzureRmExpressRouteCircuit</span></span>](Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="de3b8-175">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="de3b8-175">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
