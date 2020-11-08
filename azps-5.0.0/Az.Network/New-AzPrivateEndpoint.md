---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
ms.openlocfilehash: df298b41ea1efa4915cb7556b9fd07b1d8f3e2de
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233300"
---
# <span data-ttu-id="de34e-101">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="de34e-101">New-AzPrivateEndpoint</span></span>

## <span data-ttu-id="de34e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="de34e-102">SYNOPSIS</span></span>
<span data-ttu-id="de34e-103">Umożliwia utworzenie prywatnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="de34e-103">Creates a private endpoint.</span></span>

## <span data-ttu-id="de34e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="de34e-104">SYNTAX</span></span>

### <span data-ttu-id="de34e-105">Cały</span><span class="sxs-lookup"><span data-stu-id="de34e-105">All</span></span>

```
New-AzPrivateEndpoint -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
 -PrivateLinkServiceConnection <PSPrivateLinkServiceConnection[]> [-ByManualRequest] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de34e-106">Opis</span><span class="sxs-lookup"><span data-stu-id="de34e-106">DESCRIPTION</span></span>

<span data-ttu-id="de34e-107">Polecenie cmdlet **New-AzPrivateEndpoint** umożliwia utworzenie prywatnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="de34e-107">The **New-AzPrivateEndpoint** cmdlet creates a private endpoint.</span></span>

## <span data-ttu-id="de34e-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="de34e-108">EXAMPLES</span></span>

### <span data-ttu-id="de34e-109">Przykład 1. Tworzenie prywatnego punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="de34e-109">Example 1: Create a private endpoint</span></span>

<span data-ttu-id="de34e-110">W poniższym przykładzie przedstawiono tworzenie prywatnego punktu końcowego z określonym IDENTYFIKATORem prywatnego łącza w określonej podsieci w sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="de34e-110">The following example creates a private endpoint with a specific private link service ID in the specified subnet in a virtual network.</span></span>

```powershell
$virtualNetwork = Get-AzVirtualNetwork -ResourceName 'myVirtualNetwork' -ResourceGroupName 'myResourceGroup'
$subnet = $virtualNetwork | Select-Object -ExpandProperty subnets | Where-Object Name -eq 'mySubnet'
$plsConnection= New-AzPrivateLinkServiceConnection -Name 'MyPLSConnections' -PrivateLinkServiceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService' -RequestMessage 'Please Approve my request'
New-AzPrivateEndpoint -Name 'MyPrivateEndpoint' -ResourceGroup 'myResourceGroup' -Location 'centralus' -PrivateLinkServiceConnection $plsConnection -Subnet $subnet
```

## <span data-ttu-id="de34e-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="de34e-111">PARAMETERS</span></span>

### <span data-ttu-id="de34e-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="de34e-112">-AsJob</span></span>

<span data-ttu-id="de34e-113">Uruchom polecenie cmdlet jako zadanie w tle.</span><span class="sxs-lookup"><span data-stu-id="de34e-113">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="de34e-114">-ByManualRequest</span><span class="sxs-lookup"><span data-stu-id="de34e-114">-ByManualRequest</span></span>

<span data-ttu-id="de34e-115">Użyj ręcznego żądania, aby nawiązać połączenie.</span><span class="sxs-lookup"><span data-stu-id="de34e-115">Use manual request to establish the connection.</span></span>

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

### <span data-ttu-id="de34e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de34e-116">-DefaultProfile</span></span>

<span data-ttu-id="de34e-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="de34e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de34e-118">-Force</span><span class="sxs-lookup"><span data-stu-id="de34e-118">-Force</span></span>

<span data-ttu-id="de34e-119">Nie pytaj o potwierdzenie zastąpienia zasobu.</span><span class="sxs-lookup"><span data-stu-id="de34e-119">Do not ask for confirmation to overwrite a resource.</span></span>

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

### <span data-ttu-id="de34e-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="de34e-120">-Location</span></span>

<span data-ttu-id="de34e-121">Określa lokalizację prywatnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="de34e-121">Specifies a location for the private endpoint.</span></span> <span data-ttu-id="de34e-122">W celu określenia prawidłowych wartości dla tego parametru Użyj parametru [Get-AzLocation](/powershell/module/az.resources/get-azlocation) .</span><span class="sxs-lookup"><span data-stu-id="de34e-122">Use [Get-AzLocation](/powershell/module/az.resources/get-azlocation) to determine valid values for this parameter.</span></span>

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

### <span data-ttu-id="de34e-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="de34e-123">-Name</span></span>

<span data-ttu-id="de34e-124">Nazwa prywatnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="de34e-124">Name of the private endpoint.</span></span>

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

### <span data-ttu-id="de34e-125">-PrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="de34e-125">-PrivateLinkServiceConnection</span></span>

<span data-ttu-id="de34e-126">Identyfikator zasobu umożliwiający połączenie z prywatnym punktem końcowym.</span><span class="sxs-lookup"><span data-stu-id="de34e-126">The resource ID to connect the private endpoint.</span></span>

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

### <span data-ttu-id="de34e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de34e-127">-ResourceGroupName</span></span>

<span data-ttu-id="de34e-128">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="de34e-128">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="de34e-129">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="de34e-129">-Subnet</span></span>

<span data-ttu-id="de34e-130">Podsieć prywatnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="de34e-130">The subnet of the private endpoint.</span></span>

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

### <span data-ttu-id="de34e-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="de34e-131">-Tag</span></span>

<span data-ttu-id="de34e-132">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="de34e-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="de34e-133">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="de34e-133">For example: @{key0='value0';key1=$null;key2='value2'}</span></span>

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

### <span data-ttu-id="de34e-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="de34e-134">-Confirm</span></span>

<span data-ttu-id="de34e-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de34e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de34e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de34e-136">-WhatIf</span></span>

<span data-ttu-id="de34e-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de34e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de34e-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="de34e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de34e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de34e-139">CommonParameters</span></span>

<span data-ttu-id="de34e-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de34e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de34e-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span><span class="sxs-lookup"><span data-stu-id="de34e-141">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>

## <span data-ttu-id="de34e-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="de34e-142">INPUTS</span></span>

### <span data-ttu-id="de34e-143">System. String</span><span class="sxs-lookup"><span data-stu-id="de34e-143">System.String</span></span>

### <span data-ttu-id="de34e-144">Microsoft. Azure. Commands. Network. models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="de34e-144">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="de34e-145">Microsoft. Azure. Commands. Network. models. PSPrivateLinkServiceConnection []</span><span class="sxs-lookup"><span data-stu-id="de34e-145">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection[]</span></span>

## <span data-ttu-id="de34e-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="de34e-146">OUTPUTS</span></span>

### <span data-ttu-id="de34e-147">Microsoft. Azure. Commands. Network. models. PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="de34e-147">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="de34e-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="de34e-148">NOTES</span></span>

## <span data-ttu-id="de34e-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="de34e-149">RELATED LINKS</span></span>

[<span data-ttu-id="de34e-150">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="de34e-150">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="de34e-151">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="de34e-151">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)

[<span data-ttu-id="de34e-152">Nowe — AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="de34e-152">New-AzPrivateLinkServiceConnection</span></span>](./New-AzPrivateLinkServiceConnection.md)