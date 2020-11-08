---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
ms.openlocfilehash: 75315de4e6ca2cf799f6cefb1d3b9c143631f5a3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052188"
---
# <span data-ttu-id="1f804-101">New-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="1f804-101">New-AzVirtualRouter</span></span>

## <span data-ttu-id="1f804-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1f804-102">SYNOPSIS</span></span>
<span data-ttu-id="1f804-103">Tworzy usługę Azure VirtualRouter.</span><span class="sxs-lookup"><span data-stu-id="1f804-103">Creates an Azure VirtualRouter.</span></span>

## <span data-ttu-id="1f804-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1f804-104">SYNTAX</span></span>

### <span data-ttu-id="1f804-105">HostedGatewayParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1f804-105">HostedGatewayParameterSet (Default)</span></span>
```
New-AzVirtualRouter -ResourceGroupName <String> -Name <String> -HostedGateway <PSVirtualNetworkGateway>
 -Location <String> [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f804-106">HostedGatewayIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f804-106">HostedGatewayIdParameterSet</span></span>
```
New-AzVirtualRouter -ResourceGroupName <String> -Name <String> -HostedGatewayId <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1f804-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1f804-107">DESCRIPTION</span></span>
<span data-ttu-id="1f804-108">Polecenie cmdlet **New-AzVirtualRouter** tworzy składnik Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="1f804-108">The **New-AzVirtualRouter** cmdlet creates an Azure VirtualRouter</span></span>


## <span data-ttu-id="1f804-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1f804-109">EXAMPLES</span></span>

### <span data-ttu-id="1f804-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1f804-110">Example 1</span></span>
```powershell
$gatewayId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualNetworkGateways/erGateway'
New-AzVirtualRouter -RouterName virtualRouter -ResourceGroupName virtualRouterRG -Location 'West US'  -HostedGatewayId $gatewayId
```

### <span data-ttu-id="1f804-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="1f804-111">Example 2</span></span>
```powershell
$gateway = Get-AzVirtualNetworkGateway -Name erGateway -ResourceGroupName virtualRouterRG
New-AzVirtualRouter -RouterName virtualRouter -ResourceGroupName virtualRouterRG -Location 'West US'  -HostedGateway $gateway
```

## <span data-ttu-id="1f804-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1f804-112">PARAMETERS</span></span>

### <span data-ttu-id="1f804-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1f804-113">-AsJob</span></span>
<span data-ttu-id="1f804-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="1f804-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1f804-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f804-115">-DefaultProfile</span></span>
<span data-ttu-id="1f804-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1f804-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f804-117">-Force</span><span class="sxs-lookup"><span data-stu-id="1f804-117">-Force</span></span>
<span data-ttu-id="1f804-118">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="1f804-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="1f804-119">-HostedGateway</span><span class="sxs-lookup"><span data-stu-id="1f804-119">-HostedGateway</span></span>
<span data-ttu-id="1f804-120">Brama, w której router wirtualny musi być hostowany.</span><span class="sxs-lookup"><span data-stu-id="1f804-120">The gateway where Virtual Router needs to be hosted.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: HostedGatewayParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f804-121">-HostedGatewayId</span><span class="sxs-lookup"><span data-stu-id="1f804-121">-HostedGatewayId</span></span>
<span data-ttu-id="1f804-122">Identyfikator bramy, w której router wirtualny musi być hostowany.</span><span class="sxs-lookup"><span data-stu-id="1f804-122">The id of gateway where Virtual Router needs to be hosted.</span></span>

```yaml
Type: String
Parameter Sets: HostedGatewayIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f804-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="1f804-123">-Location</span></span>
<span data-ttu-id="1f804-124">Lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="1f804-124">The location.</span></span>

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

### <span data-ttu-id="1f804-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1f804-125">-Name</span></span>
<span data-ttu-id="1f804-126">Nazwa routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="1f804-126">The name of the virtual router.</span></span>

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

### <span data-ttu-id="1f804-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f804-127">-ResourceGroupName</span></span>
<span data-ttu-id="1f804-128">Nazwa grupy zasobów routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="1f804-128">The resource group name of the virtual router.</span></span>

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

### <span data-ttu-id="1f804-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="1f804-129">-Tag</span></span>
<span data-ttu-id="1f804-130">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="1f804-130">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="1f804-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1f804-131">-Confirm</span></span>
<span data-ttu-id="1f804-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f804-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f804-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f804-133">-WhatIf</span></span>
<span data-ttu-id="1f804-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f804-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f804-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1f804-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f804-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f804-136">CommonParameters</span></span>
<span data-ttu-id="1f804-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f804-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="1f804-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f804-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f804-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1f804-139">INPUTS</span></span>

### <span data-ttu-id="1f804-140">System. String</span><span class="sxs-lookup"><span data-stu-id="1f804-140">System.String</span></span>

### <span data-ttu-id="1f804-141">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1f804-141">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="1f804-142">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1f804-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1f804-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1f804-143">OUTPUTS</span></span>

### <span data-ttu-id="1f804-144">Microsoft. Azure. Commands. Network. models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="1f804-144">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="1f804-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1f804-145">NOTES</span></span>

## <span data-ttu-id="1f804-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1f804-146">RELATED LINKS</span></span>
