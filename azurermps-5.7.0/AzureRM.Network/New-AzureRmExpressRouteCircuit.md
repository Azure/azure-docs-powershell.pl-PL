---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E40CAF2F-ED57-4AC1-8B9A-E48042DD8F91
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: 0c611edc0ef8cb117e556a19e22f93d1f8db96ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548912"
---
# <span data-ttu-id="05a39-101">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="05a39-101">New-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="05a39-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="05a39-102">SYNOPSIS</span></span>
<span data-ttu-id="05a39-103">Umożliwia utworzenie obwodu trasy usługi Azure Express.</span><span class="sxs-lookup"><span data-stu-id="05a39-103">Creates an Azure express route circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05a39-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="05a39-104">SYNTAX</span></span>

```
New-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 [-SkuTier <String>] [-SkuFamily <String>] -ServiceProviderName <String> -PeeringLocation <String>
 -BandwidthInMbps <Int32>
 [-Peering <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPeering]>]
 [-Authorization <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05a39-105">Opis</span><span class="sxs-lookup"><span data-stu-id="05a39-105">DESCRIPTION</span></span>
<span data-ttu-id="05a39-106">Polecenie cmdlet **New-AzureRmExpressRouteCircuit** umożliwia utworzenie obwodu trasy usługi Azure Express.</span><span class="sxs-lookup"><span data-stu-id="05a39-106">The **New-AzureRmExpressRouteCircuit** cmdlet creates an Azure express route circuit.</span></span>

## <span data-ttu-id="05a39-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="05a39-107">EXAMPLES</span></span>

### <span data-ttu-id="05a39-108">Przykład 1. Tworzenie nowego obwodu ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="05a39-108">Example 1: Create a new ExpressRoute circuit</span></span>
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

## <span data-ttu-id="05a39-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="05a39-109">PARAMETERS</span></span>

### <span data-ttu-id="05a39-110">-AllowClassicOperations</span><span class="sxs-lookup"><span data-stu-id="05a39-110">-AllowClassicOperations</span></span>
<span data-ttu-id="05a39-111">Użycie tego parametru umożliwia korzystanie z klasycznych poleceń cmdlet programu Azure PowerShell do zarządzania obwodem.</span><span class="sxs-lookup"><span data-stu-id="05a39-111">The use of this parameter allows you to use the classic Azure PowerShell cmdlets to manage the circuit.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05a39-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="05a39-112">-AsJob</span></span>
<span data-ttu-id="05a39-113">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="05a39-113">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05a39-114">— Autoryzacja</span><span class="sxs-lookup"><span data-stu-id="05a39-114">-Authorization</span></span>
<span data-ttu-id="05a39-115">Lista autoryzacji obwodu.</span><span class="sxs-lookup"><span data-stu-id="05a39-115">A list of circuit authorizations.</span></span>

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

### <span data-ttu-id="05a39-116">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="05a39-116">-BandwidthInMbps</span></span>
<span data-ttu-id="05a39-117">Szerokość pasma obwodu.</span><span class="sxs-lookup"><span data-stu-id="05a39-117">The bandwidth of the circuit.</span></span> <span data-ttu-id="05a39-118">To musi być wartość obsługiwana przez dostawcę usługi.</span><span class="sxs-lookup"><span data-stu-id="05a39-118">This must be a value that is supported by the service provider.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05a39-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05a39-119">-DefaultProfile</span></span>
<span data-ttu-id="05a39-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="05a39-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05a39-121">-Force</span><span class="sxs-lookup"><span data-stu-id="05a39-121">-Force</span></span>
<span data-ttu-id="05a39-122">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="05a39-122">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05a39-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="05a39-123">-Location</span></span>
<span data-ttu-id="05a39-124">Lokalizacja obwodu.</span><span class="sxs-lookup"><span data-stu-id="05a39-124">The location of the circuit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05a39-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="05a39-125">-Name</span></span>
<span data-ttu-id="05a39-126">Nazwa tworzonego obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="05a39-126">The name of the ExpressRoute circuit being created.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05a39-127">-Peer</span><span class="sxs-lookup"><span data-stu-id="05a39-127">-Peering</span></span>
<span data-ttu-id="05a39-128">Konfiguracja elementu równorzędnego listy.</span><span class="sxs-lookup"><span data-stu-id="05a39-128">A list peer configurations.</span></span>

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

### <span data-ttu-id="05a39-129">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="05a39-129">-PeeringLocation</span></span>
<span data-ttu-id="05a39-130">Nazwa lokalizacji komunikacji równorzędnej obsługiwana przez dostawcę usługi.</span><span class="sxs-lookup"><span data-stu-id="05a39-130">The name of the peering location supported by the service provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05a39-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05a39-131">-ResourceGroupName</span></span>
<span data-ttu-id="05a39-132">Grupa zasobów, która będzie zawierać obwód.</span><span class="sxs-lookup"><span data-stu-id="05a39-132">The resource group that will contain the circuit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05a39-133">-Serviceprovidername</span><span class="sxs-lookup"><span data-stu-id="05a39-133">-ServiceProviderName</span></span>
<span data-ttu-id="05a39-134">Nazwa dostawcy usługi obwodu.</span><span class="sxs-lookup"><span data-stu-id="05a39-134">The name of the circuit service provider.</span></span> <span data-ttu-id="05a39-135">Musi być taka sama jak nazwa wymieniona za pomocą polecenia cmdlet Get-AzureRmExpressRouteServiceProvider.</span><span class="sxs-lookup"><span data-stu-id="05a39-135">This must match a name listed by the Get-AzureRmExpressRouteServiceProvider cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05a39-136">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="05a39-136">-SkuFamily</span></span>
<span data-ttu-id="05a39-137">Rodzina SKU określa typ rozliczeń.</span><span class="sxs-lookup"><span data-stu-id="05a39-137">SKU family determines the billing type.</span></span> <span data-ttu-id="05a39-138">Możliwe wartości tego parametru to: `MeteredData` lub `UnlimitedData` .</span><span class="sxs-lookup"><span data-stu-id="05a39-138">Possible values for this parameter are: `MeteredData` or `UnlimitedData`.</span></span> <span data-ttu-id="05a39-139">Pamiętaj, że możesz zmienić typ rozliczeń z MeteredData na UnlimitedData, ale nie można zmienić typu z UnlimitedData na MeteredData.</span><span class="sxs-lookup"><span data-stu-id="05a39-139">Note that you can change the billing type from MeteredData to UnlimitedData, but you can't change the type from UnlimitedData to MeteredData.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: MeteredData, UnlimitedData

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05a39-140">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="05a39-140">-SkuTier</span></span>
<span data-ttu-id="05a39-141">Poziom usług dla obwodu.</span><span class="sxs-lookup"><span data-stu-id="05a39-141">The tier of service for the circuit.</span></span> <span data-ttu-id="05a39-142">Możliwe wartości tego parametru to: `Standard` lub `Premium` .</span><span class="sxs-lookup"><span data-stu-id="05a39-142">Possible values for this parameter are: `Standard` or `Premium`.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05a39-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="05a39-143">-Tag</span></span>
<span data-ttu-id="05a39-144">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="05a39-144">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="05a39-145">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="05a39-145">For example:</span></span>

<span data-ttu-id="05a39-146">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="05a39-146">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05a39-147">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="05a39-147">-Confirm</span></span>
<span data-ttu-id="05a39-148">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05a39-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05a39-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05a39-149">-WhatIf</span></span>
<span data-ttu-id="05a39-150">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05a39-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05a39-151">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="05a39-151">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05a39-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05a39-152">CommonParameters</span></span>
<span data-ttu-id="05a39-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05a39-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05a39-154">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05a39-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05a39-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="05a39-155">INPUTS</span></span>

### <span data-ttu-id="05a39-156">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="05a39-156">None</span></span>
<span data-ttu-id="05a39-157">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="05a39-157">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="05a39-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="05a39-158">OUTPUTS</span></span>

### <span data-ttu-id="05a39-159">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="05a39-159">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="05a39-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="05a39-160">NOTES</span></span>

## <span data-ttu-id="05a39-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="05a39-161">RELATED LINKS</span></span>

[<span data-ttu-id="05a39-162">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="05a39-162">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="05a39-163">Przenieś — AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="05a39-163">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="05a39-164">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="05a39-164">Remove-AzureRmExpressRouteCircuit</span></span>](Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="05a39-165">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="05a39-165">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
