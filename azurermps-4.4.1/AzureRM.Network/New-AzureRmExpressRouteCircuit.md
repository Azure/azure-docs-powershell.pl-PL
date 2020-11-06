---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E40CAF2F-ED57-4AC1-8B9A-E48042DD8F91
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: 4a5c59f6cc561bdd5f12462aab1e4cd634e70fc4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544684"
---
# <span data-ttu-id="d0469-101">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d0469-101">New-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="d0469-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d0469-102">SYNOPSIS</span></span>
<span data-ttu-id="d0469-103">Umożliwia utworzenie obwodu trasy usługi Azure Express.</span><span class="sxs-lookup"><span data-stu-id="d0469-103">Creates an Azure express route circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0469-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d0469-104">SYNTAX</span></span>

```
New-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 [-SkuTier <String>] [-SkuFamily <String>] -ServiceProviderName <String> -PeeringLocation <String>
 -BandwidthInMbps <Int32>
 [-Peering <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPeering]>]
 [-Authorization <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0469-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d0469-105">DESCRIPTION</span></span>
<span data-ttu-id="d0469-106">Polecenie cmdlet **New-AzureRmExpressRouteCircuit** umożliwia utworzenie obwodu trasy usługi Azure Express.</span><span class="sxs-lookup"><span data-stu-id="d0469-106">The **New-AzureRmExpressRouteCircuit** cmdlet creates an Azure express route circuit.</span></span>

## <span data-ttu-id="d0469-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d0469-107">EXAMPLES</span></span>

### <span data-ttu-id="d0469-108">Przykład 1. Tworzenie nowego obwodu ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="d0469-108">Example 1: Create a new ExpressRoute circuit</span></span>
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

## <span data-ttu-id="d0469-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d0469-109">PARAMETERS</span></span>

### <span data-ttu-id="d0469-110">-AllowClassicOperations</span><span class="sxs-lookup"><span data-stu-id="d0469-110">-AllowClassicOperations</span></span>
<span data-ttu-id="d0469-111">Użycie tego parametru umożliwia korzystanie z klasycznych poleceń cmdlet programu Azure PowerShell do zarządzania obwodem.</span><span class="sxs-lookup"><span data-stu-id="d0469-111">The use of this parameter allows you to use the classic Azure PowerShell cmdlets to manage the circuit.</span></span>

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

### <span data-ttu-id="d0469-112">— Autoryzacja</span><span class="sxs-lookup"><span data-stu-id="d0469-112">-Authorization</span></span>
<span data-ttu-id="d0469-113">Lista autoryzacji obwodu.</span><span class="sxs-lookup"><span data-stu-id="d0469-113">A list of circuit authorizations.</span></span>

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

### <span data-ttu-id="d0469-114">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="d0469-114">-BandwidthInMbps</span></span>
<span data-ttu-id="d0469-115">Szerokość pasma obwodu.</span><span class="sxs-lookup"><span data-stu-id="d0469-115">The bandwidth of the circuit.</span></span> <span data-ttu-id="d0469-116">To musi być wartość obsługiwana przez dostawcę usługi.</span><span class="sxs-lookup"><span data-stu-id="d0469-116">This must be a value that is supported by the service provider.</span></span>

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

### <span data-ttu-id="d0469-117">-Force</span><span class="sxs-lookup"><span data-stu-id="d0469-117">-Force</span></span>
<span data-ttu-id="d0469-118">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="d0469-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d0469-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d0469-119">-Location</span></span>
<span data-ttu-id="d0469-120">Lokalizacja obwodu.</span><span class="sxs-lookup"><span data-stu-id="d0469-120">The location of the circuit.</span></span>

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

### <span data-ttu-id="d0469-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d0469-121">-Name</span></span>
<span data-ttu-id="d0469-122">Nazwa tworzonego obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="d0469-122">The name of the ExpressRoute circuit being created.</span></span>

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

### <span data-ttu-id="d0469-123">-Peer</span><span class="sxs-lookup"><span data-stu-id="d0469-123">-Peering</span></span>
<span data-ttu-id="d0469-124">Konfiguracja elementu równorzędnego listy.</span><span class="sxs-lookup"><span data-stu-id="d0469-124">A list peer configurations.</span></span>

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

### <span data-ttu-id="d0469-125">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="d0469-125">-PeeringLocation</span></span>
<span data-ttu-id="d0469-126">Nazwa lokalizacji komunikacji równorzędnej obsługiwana przez dostawcę usługi.</span><span class="sxs-lookup"><span data-stu-id="d0469-126">The name of the peering location supported by the service provider.</span></span>

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

### <span data-ttu-id="d0469-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0469-127">-ResourceGroupName</span></span>
<span data-ttu-id="d0469-128">Grupa zasobów, która będzie zawierać obwód.</span><span class="sxs-lookup"><span data-stu-id="d0469-128">The resource group that will contain the circuit.</span></span>

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

### <span data-ttu-id="d0469-129">-Serviceprovidername</span><span class="sxs-lookup"><span data-stu-id="d0469-129">-ServiceProviderName</span></span>
<span data-ttu-id="d0469-130">Nazwa dostawcy usługi obwodu.</span><span class="sxs-lookup"><span data-stu-id="d0469-130">The name of the circuit service provider.</span></span> <span data-ttu-id="d0469-131">Musi być taka sama jak nazwa wymieniona za pomocą polecenia cmdlet Get-AzureRmExpressRouteServiceProvider.</span><span class="sxs-lookup"><span data-stu-id="d0469-131">This must match a name listed by the Get-AzureRmExpressRouteServiceProvider cmdlet.</span></span>

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

### <span data-ttu-id="d0469-132">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="d0469-132">-SkuFamily</span></span>
<span data-ttu-id="d0469-133">Rodzina SKU określa typ rozliczeń.</span><span class="sxs-lookup"><span data-stu-id="d0469-133">SKU family determines the billing type.</span></span> <span data-ttu-id="d0469-134">Możliwe wartości tego parametru to: `MeteredData` lub `UnlimitedData` .</span><span class="sxs-lookup"><span data-stu-id="d0469-134">Possible values for this parameter are: `MeteredData` or `UnlimitedData`.</span></span> <span data-ttu-id="d0469-135">Pamiętaj, że możesz zmienić typ rozliczeń z MeteredData na UnlimitedData, ale nie można zmienić typu z UnlimitedData na MeteredData.</span><span class="sxs-lookup"><span data-stu-id="d0469-135">Note that you can change the billing type from MeteredData to UnlimitedData, but you can't change the type from UnlimitedData to MeteredData.</span></span>

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

### <span data-ttu-id="d0469-136">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="d0469-136">-SkuTier</span></span>
<span data-ttu-id="d0469-137">Poziom usług dla obwodu.</span><span class="sxs-lookup"><span data-stu-id="d0469-137">The tier of service for the circuit.</span></span> <span data-ttu-id="d0469-138">Możliwe wartości tego parametru to: `Standard` lub `Premium` .</span><span class="sxs-lookup"><span data-stu-id="d0469-138">Possible values for this parameter are: `Standard` or `Premium`.</span></span>

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

### <span data-ttu-id="d0469-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="d0469-139">-Tag</span></span>
<span data-ttu-id="d0469-140">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="d0469-140">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d0469-141">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="d0469-141">For example:</span></span>

<span data-ttu-id="d0469-142">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="d0469-142">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="d0469-143">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d0469-143">-Confirm</span></span>
<span data-ttu-id="d0469-144">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0469-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0469-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0469-145">-WhatIf</span></span>
<span data-ttu-id="d0469-146">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0469-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0469-147">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d0469-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0469-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0469-148">-DefaultProfile</span></span>
<span data-ttu-id="d0469-149">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d0469-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0469-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0469-150">CommonParameters</span></span>
<span data-ttu-id="d0469-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0469-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0469-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0469-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0469-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d0469-153">INPUTS</span></span>

## <span data-ttu-id="d0469-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d0469-154">OUTPUTS</span></span>

### <span data-ttu-id="d0469-155">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d0469-155">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="d0469-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d0469-156">NOTES</span></span>

## <span data-ttu-id="d0469-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d0469-157">RELATED LINKS</span></span>

[<span data-ttu-id="d0469-158">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d0469-158">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="d0469-159">Przenieś — AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d0469-159">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="d0469-160">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d0469-160">Remove-AzureRmExpressRouteCircuit</span></span>](Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="d0469-161">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d0469-161">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
