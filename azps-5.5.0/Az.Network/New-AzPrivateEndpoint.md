---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
ms.openlocfilehash: df298b41ea1efa4915cb7556b9fd07b1d8f3e2de
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184387"
---
# <span data-ttu-id="6ebcc-101">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="6ebcc-101">New-AzPrivateEndpoint</span></span>

## <span data-ttu-id="6ebcc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ebcc-102">SYNOPSIS</span></span>
<span data-ttu-id="6ebcc-103">Tworzy prywatny punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="6ebcc-103">Creates a private endpoint.</span></span>

## <span data-ttu-id="6ebcc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6ebcc-104">SYNTAX</span></span>

### <span data-ttu-id="6ebcc-105">Wszystko</span><span class="sxs-lookup"><span data-stu-id="6ebcc-105">All</span></span>

```
New-AzPrivateEndpoint -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
 -PrivateLinkServiceConnection <PSPrivateLinkServiceConnection[]> [-ByManualRequest] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ebcc-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="6ebcc-106">DESCRIPTION</span></span>

<span data-ttu-id="6ebcc-107">Polecenie **cmdlet New-AzPrivateEndpoint** tworzy prywatny punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="6ebcc-107">The **New-AzPrivateEndpoint** cmdlet creates a private endpoint.</span></span>

## <span data-ttu-id="6ebcc-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6ebcc-108">EXAMPLES</span></span>

### <span data-ttu-id="6ebcc-109">Przykład 1. Tworzenie prywatnego punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="6ebcc-109">Example 1: Create a private endpoint</span></span>

<span data-ttu-id="6ebcc-110">W poniższym przykładzie jest tworzyny prywatny punkt końcowy z określonym identyfikatorem usługi łączenia prywatnego w określonej podsieci w sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6ebcc-110">The following example creates a private endpoint with a specific private link service ID in the specified subnet in a virtual network.</span></span>

```powershell
$virtualNetwork = Get-AzVirtualNetwork -ResourceName 'myVirtualNetwork' -ResourceGroupName 'myResourceGroup'
$subnet = $virtualNetwork | Select-Object -ExpandProperty subnets | Where-Object Name -eq 'mySubnet'
$plsConnection= New-AzPrivateLinkServiceConnection -Name 'MyPLSConnections' -PrivateLinkServiceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService' -RequestMessage 'Please Approve my request'
New-AzPrivateEndpoint -Name 'MyPrivateEndpoint' -ResourceGroup 'myResourceGroup' -Location 'centralus' -PrivateLinkServiceConnection $plsConnection -Subnet $subnet
```

## <span data-ttu-id="6ebcc-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6ebcc-111">PARAMETERS</span></span>

### <span data-ttu-id="6ebcc-112">— AsJob</span><span class="sxs-lookup"><span data-stu-id="6ebcc-112">-AsJob</span></span>

<span data-ttu-id="6ebcc-113">Uruchom polecenie cmdlet jako zadanie w tle.</span><span class="sxs-lookup"><span data-stu-id="6ebcc-113">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="6ebcc-114">-ByManualRequest</span><span class="sxs-lookup"><span data-stu-id="6ebcc-114">-ByManualRequest</span></span>

<span data-ttu-id="6ebcc-115">Aby nawiązać połączenie, użyj ręcznego żądania.</span><span class="sxs-lookup"><span data-stu-id="6ebcc-115">Use manual request to establish the connection.</span></span>

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

### <span data-ttu-id="6ebcc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ebcc-116">-DefaultProfile</span></span>

<span data-ttu-id="6ebcc-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6ebcc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ebcc-118">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="6ebcc-118">-Force</span></span>

<span data-ttu-id="6ebcc-119">Nie należy prosić o potwierdzenie zastąpienia zasobu.</span><span class="sxs-lookup"><span data-stu-id="6ebcc-119">Do not ask for confirmation to overwrite a resource.</span></span>

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

### <span data-ttu-id="6ebcc-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="6ebcc-120">-Location</span></span>

<span data-ttu-id="6ebcc-121">Określa lokalizację dla prywatnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="6ebcc-121">Specifies a location for the private endpoint.</span></span> <span data-ttu-id="6ebcc-122">Użyj [funkcji Get-AzLocation](/powershell/module/az.resources/get-azlocation) do określenia prawidłowych wartości dla tego parametru.</span><span class="sxs-lookup"><span data-stu-id="6ebcc-122">Use [Get-AzLocation](/powershell/module/az.resources/get-azlocation) to determine valid values for this parameter.</span></span>

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

### <span data-ttu-id="6ebcc-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6ebcc-123">-Name</span></span>

<span data-ttu-id="6ebcc-124">Nazwa prywatnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="6ebcc-124">Name of the private endpoint.</span></span>

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

### <span data-ttu-id="6ebcc-125">-PrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="6ebcc-125">-PrivateLinkServiceConnection</span></span>

<span data-ttu-id="6ebcc-126">Identyfikator zasobu do połączenia prywatnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="6ebcc-126">The resource ID to connect the private endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ebcc-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ebcc-127">-ResourceGroupName</span></span>

<span data-ttu-id="6ebcc-128">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6ebcc-128">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="6ebcc-129">-Subnet</span><span class="sxs-lookup"><span data-stu-id="6ebcc-129">-Subnet</span></span>

<span data-ttu-id="6ebcc-130">Podsieci prywatnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="6ebcc-130">The subnet of the private endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ebcc-131">— Tag</span><span class="sxs-lookup"><span data-stu-id="6ebcc-131">-Tag</span></span>

<span data-ttu-id="6ebcc-132">Pary klucz-wartość w postaci tabeli skrótu.</span><span class="sxs-lookup"><span data-stu-id="6ebcc-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6ebcc-133">Na przykład: @{key0='value0';key1=$null;key2='wartość2'}</span><span class="sxs-lookup"><span data-stu-id="6ebcc-133">For example: @{key0='value0';key1=$null;key2='value2'}</span></span>

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

### <span data-ttu-id="6ebcc-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6ebcc-134">-Confirm</span></span>

<span data-ttu-id="6ebcc-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6ebcc-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ebcc-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ebcc-136">-WhatIf</span></span>

<span data-ttu-id="6ebcc-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ebcc-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ebcc-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6ebcc-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ebcc-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ebcc-139">CommonParameters</span></span>

<span data-ttu-id="6ebcc-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ebcc-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ebcc-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](/powershell/module/microsoft.powershell.core/about/about_commonparameters)</span><span class="sxs-lookup"><span data-stu-id="6ebcc-141">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>

## <span data-ttu-id="6ebcc-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6ebcc-142">INPUTS</span></span>

### <span data-ttu-id="6ebcc-143">System.String</span><span class="sxs-lookup"><span data-stu-id="6ebcc-143">System.String</span></span>

### <span data-ttu-id="6ebcc-144">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="6ebcc-144">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="6ebcc-145">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection[]</span><span class="sxs-lookup"><span data-stu-id="6ebcc-145">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection[]</span></span>

## <span data-ttu-id="6ebcc-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6ebcc-146">OUTPUTS</span></span>

### <span data-ttu-id="6ebcc-147">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="6ebcc-147">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="6ebcc-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6ebcc-148">NOTES</span></span>

## <span data-ttu-id="6ebcc-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6ebcc-149">RELATED LINKS</span></span>

[<span data-ttu-id="6ebcc-150">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="6ebcc-150">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="6ebcc-151">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="6ebcc-151">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)

[<span data-ttu-id="6ebcc-152">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="6ebcc-152">New-AzPrivateLinkServiceConnection</span></span>](./New-AzPrivateLinkServiceConnection.md)