---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
ms.openlocfilehash: c72af57f860dcc1c889ecf81111341fa7dbe21eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871372"
---
# <span data-ttu-id="35d39-101">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="35d39-101">New-AzPrivateEndpoint</span></span>

## <span data-ttu-id="35d39-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="35d39-102">SYNOPSIS</span></span>
<span data-ttu-id="35d39-103">Umożliwia utworzenie prywatnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="35d39-103">Creates a private endpoint.</span></span>

## <span data-ttu-id="35d39-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="35d39-104">SYNTAX</span></span>

```
New-AzPrivateEndpoint -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
 -PrivateLinkServiceConnection <PSPrivateLinkServiceConnection[]> [-ByManualRequest] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35d39-105">Opis</span><span class="sxs-lookup"><span data-stu-id="35d39-105">DESCRIPTION</span></span>
<span data-ttu-id="35d39-106">Polecenie cmdlet **New-AzPrivateEndpoint** umożliwia utworzenie prywatnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="35d39-106">The **New-AzPrivateEndpoint** cmdlet creates a private endpoint.</span></span>

## <span data-ttu-id="35d39-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="35d39-107">EXAMPLES</span></span>

### <span data-ttu-id="35d39-108">1: Tworzenie prywatnego punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="35d39-108">1: Create a private endpoint</span></span>
```
$virtualNetwork = Get-AzVirtualNetwork -ResourceName MyVirtualNetwork -ResourceGroupName TestResourceGroup
$plsConnection= New-AzPrivateLinkServiceConnection -Name MyPLSConnections -PrivateLinkServiceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService" -RequestMessage "Please Approve my request"
New-AzPrivateEndpoint -Name MyPrivateEndpoint -ResourceGroup TestResourceGroup -Location centralus -PrivateLinkServiceConnection $plsConnection -Subnet $virtualNetwork.Subnets[0]
```

<span data-ttu-id="35d39-109">W tym przykładzie przedstawiono tworzenie prywatnego punktu końcowego z określonym identyfikatorem prywatnego łącza w określonej podsieci w sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="35d39-109">This example creates a private endpoint with specific private link service id in a specific subnet in a virtual network.</span></span>

## <span data-ttu-id="35d39-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="35d39-110">PARAMETERS</span></span>

### <span data-ttu-id="35d39-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35d39-111">-AsJob</span></span>
<span data-ttu-id="35d39-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="35d39-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="35d39-113">-ByManualRequest</span><span class="sxs-lookup"><span data-stu-id="35d39-113">-ByManualRequest</span></span>
<span data-ttu-id="35d39-114">Używanie ręcznego żądania.</span><span class="sxs-lookup"><span data-stu-id="35d39-114">Using manual request.</span></span>

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

### <span data-ttu-id="35d39-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35d39-115">-DefaultProfile</span></span>
<span data-ttu-id="35d39-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="35d39-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35d39-117">-Force</span><span class="sxs-lookup"><span data-stu-id="35d39-117">-Force</span></span>
<span data-ttu-id="35d39-118">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="35d39-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="35d39-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="35d39-119">-Location</span></span>
<span data-ttu-id="35d39-120">pozycję.</span><span class="sxs-lookup"><span data-stu-id="35d39-120">location.</span></span>

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

### <span data-ttu-id="35d39-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="35d39-121">-Name</span></span>
<span data-ttu-id="35d39-122">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="35d39-122">The resource name.</span></span>

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

### <span data-ttu-id="35d39-123">-PrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="35d39-123">-PrivateLinkServiceConnection</span></span>
<span data-ttu-id="35d39-124">Połączenie z usługą link prywatny.</span><span class="sxs-lookup"><span data-stu-id="35d39-124">The private link service connection.</span></span>

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

### <span data-ttu-id="35d39-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35d39-125">-ResourceGroupName</span></span>
<span data-ttu-id="35d39-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="35d39-126">The resource group name.</span></span>

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

### <span data-ttu-id="35d39-127">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="35d39-127">-Subnet</span></span>
<span data-ttu-id="35d39-128">Podsieć prywatnego punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="35d39-128">The subnet of the private endpoint</span></span>

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

### <span data-ttu-id="35d39-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="35d39-129">-Tag</span></span>
<span data-ttu-id="35d39-130">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="35d39-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="35d39-131">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="35d39-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="35d39-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="35d39-132">-Confirm</span></span>
<span data-ttu-id="35d39-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35d39-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35d39-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35d39-134">-WhatIf</span></span>
<span data-ttu-id="35d39-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35d39-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35d39-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="35d39-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35d39-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35d39-137">CommonParameters</span></span>
<span data-ttu-id="35d39-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35d39-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35d39-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35d39-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35d39-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="35d39-140">INPUTS</span></span>

### <span data-ttu-id="35d39-141">System. String</span><span class="sxs-lookup"><span data-stu-id="35d39-141">System.String</span></span>

### <span data-ttu-id="35d39-142">Microsoft. Azure. Commands. Network. models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="35d39-142">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="35d39-143">Microsoft. Azure. Commands. Network. models. PSPrivateLinkServiceConnection []</span><span class="sxs-lookup"><span data-stu-id="35d39-143">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection[]</span></span>

## <span data-ttu-id="35d39-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="35d39-144">OUTPUTS</span></span>

### <span data-ttu-id="35d39-145">Microsoft. Azure. Commands. Network. models. PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="35d39-145">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="35d39-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="35d39-146">NOTES</span></span>

## <span data-ttu-id="35d39-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="35d39-147">RELATED LINKS</span></span>

[<span data-ttu-id="35d39-148">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="35d39-148">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="35d39-149">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="35d39-149">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)

[<span data-ttu-id="35d39-150">Nowe — AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="35d39-150">New-AzPrivateLinkServiceConnection</span></span>](./New-AzPrivateLinkServiceConnection.md)