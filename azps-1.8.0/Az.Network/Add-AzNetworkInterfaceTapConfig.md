---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: c5c2481244de752a76eb1a1863d1fcc49d93ddb2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709666"
---
# <span data-ttu-id="2cf80-101">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="2cf80-101">Add-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="2cf80-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2cf80-102">SYNOPSIS</span></span>
<span data-ttu-id="2cf80-103">Tworzy zasób TapConfiguration skojarzony z NetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="2cf80-103">Creates a TapConfiguration resource associated to a NetworkInterface.</span></span> <span data-ttu-id="2cf80-104">Będzie to miało odwołanie do istniejącego zasobu VirtualNetworkTap.</span><span class="sxs-lookup"><span data-stu-id="2cf80-104">This will reference to an existing VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="2cf80-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2cf80-105">SYNTAX</span></span>

### <span data-ttu-id="2cf80-106">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2cf80-106">SetByResource (Default)</span></span>
```
Add-AzNetworkInterfaceTapConfig -NetworkInterface <PSNetworkInterface> -Name <String>
 [-VirtualNetworkTap <PSVirtualNetworkTap>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2cf80-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2cf80-107">SetByResourceId</span></span>
```
Add-AzNetworkInterfaceTapConfig -NetworkInterface <PSNetworkInterface> -Name <String>
 [-VirtualNetworkTapId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2cf80-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2cf80-108">DESCRIPTION</span></span>
<span data-ttu-id="2cf80-109">Polecenie cmdlet **Add-AzNetworkInterfaceTapConfig** tworzy zasób TapConfiguration skojarzony z NetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="2cf80-109">The **Add-AzNetworkInterfaceTapConfig** cmdlet creates a TapConfiguration resource associated to a NetworkInterface.</span></span> <span data-ttu-id="2cf80-110">Będzie to miało odwołanie do istniejącego zasobu VirtualNetworkTap.</span><span class="sxs-lookup"><span data-stu-id="2cf80-110">This will reference to an existing VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="2cf80-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2cf80-111">EXAMPLES</span></span>

### <span data-ttu-id="2cf80-112">Przykład 1: Dodawanie TapConfiguration do danego NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="2cf80-112">Example 1: Add TapConfiguration to a given NetworkInterface</span></span>
```
PS C:\>Add-AzNetworkInterfaceTapConfig -NetworkInterface $sourceNic -VirtualNetworkTap $vVirtualNetworkTap -Name 'myTapConfig'
```

<span data-ttu-id="2cf80-113">Dodaj TapConfiguration do sourceNic.</span><span class="sxs-lookup"><span data-stu-id="2cf80-113">Add the TapConfiguration to a sourceNic.</span></span> <span data-ttu-id="2cf80-114">Ruch z maszyny wirtualnej sourceNic będzie dublowany na docelowej maszynie wirtualnej określonej w zasobie vVirtualNetworkTap.</span><span class="sxs-lookup"><span data-stu-id="2cf80-114">The traffic from sourceNic VM will be mirrored to destination VM referred in vVirtualNetworkTap resource.</span></span>

## <span data-ttu-id="2cf80-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2cf80-115">PARAMETERS</span></span>

### <span data-ttu-id="2cf80-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cf80-116">-DefaultProfile</span></span>
<span data-ttu-id="2cf80-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2cf80-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2cf80-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2cf80-118">-Name</span></span>
<span data-ttu-id="2cf80-119">Nazwa konfiguracji stuknij.</span><span class="sxs-lookup"><span data-stu-id="2cf80-119">Name of the tap configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cf80-120">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="2cf80-120">-NetworkInterface</span></span>
<span data-ttu-id="2cf80-121">Odwołanie do zasobu interfejs sieciowy.</span><span class="sxs-lookup"><span data-stu-id="2cf80-121">The reference of the network interface resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2cf80-122">-VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="2cf80-122">-VirtualNetworkTap</span></span>
<span data-ttu-id="2cf80-123">Odwołanie do zasobu sieci wirtualnej TAP.</span><span class="sxs-lookup"><span data-stu-id="2cf80-123">The reference of the virtual network tap resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cf80-124">-VirtualNetworkTapId</span><span class="sxs-lookup"><span data-stu-id="2cf80-124">-VirtualNetworkTapId</span></span>
<span data-ttu-id="2cf80-125">Odwołanie do zasobu sieci wirtualnej TAP.</span><span class="sxs-lookup"><span data-stu-id="2cf80-125">The reference of the virtual network tap resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cf80-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2cf80-126">-Confirm</span></span>
<span data-ttu-id="2cf80-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2cf80-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cf80-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cf80-128">-WhatIf</span></span>
<span data-ttu-id="2cf80-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2cf80-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2cf80-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2cf80-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cf80-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cf80-131">CommonParameters</span></span>
<span data-ttu-id="2cf80-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cf80-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cf80-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cf80-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cf80-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2cf80-134">INPUTS</span></span>

### <span data-ttu-id="2cf80-135">Microsoft. Azure. Commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="2cf80-135">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="2cf80-136">System. String</span><span class="sxs-lookup"><span data-stu-id="2cf80-136">System.String</span></span>

### <span data-ttu-id="2cf80-137">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="2cf80-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="2cf80-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2cf80-138">OUTPUTS</span></span>

### <span data-ttu-id="2cf80-139">Microsoft. Azure. Commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="2cf80-139">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="2cf80-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2cf80-140">NOTES</span></span>

## <span data-ttu-id="2cf80-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2cf80-141">RELATED LINKS</span></span>

[<span data-ttu-id="2cf80-142">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="2cf80-142">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="2cf80-143">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="2cf80-143">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="2cf80-144">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="2cf80-144">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)