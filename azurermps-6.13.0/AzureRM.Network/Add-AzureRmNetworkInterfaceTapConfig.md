---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermnetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmNetworkInterfaceTapConfig.md
ms.openlocfilehash: 10d51bd2e70db0d2b1d06b907769fb6842e413cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554077"
---
# <span data-ttu-id="a0a48-101">Add-AzureRmNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="a0a48-101">Add-AzureRmNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="a0a48-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a0a48-102">SYNOPSIS</span></span>
<span data-ttu-id="a0a48-103">Tworzy zasób TapConfiguration skojarzony z NetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="a0a48-103">Creates a TapConfiguration resource associated to a NetworkInterface.</span></span> <span data-ttu-id="a0a48-104">Będzie to miało odwołanie do istniejącego zasobu VirtualNetworkTap.</span><span class="sxs-lookup"><span data-stu-id="a0a48-104">This will reference to an existing VirtualNetworkTap resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0a48-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a0a48-105">SYNTAX</span></span>

### <span data-ttu-id="a0a48-106">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a0a48-106">SetByResource (Default)</span></span>
```
Add-AzureRmNetworkInterfaceTapConfig -NetworkInterface <PSNetworkInterface> -Name <String>
 [-VirtualNetworkTap <PSVirtualNetworkTap>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a0a48-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a0a48-107">SetByResourceId</span></span>
```
Add-AzureRmNetworkInterfaceTapConfig -NetworkInterface <PSNetworkInterface> -Name <String>
 [-VirtualNetworkTapId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a0a48-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a0a48-108">DESCRIPTION</span></span>
<span data-ttu-id="a0a48-109">Polecenie cmdlet **Add-AzureRmNetworkInterfaceTapConfig** tworzy zasób TapConfiguration skojarzony z NetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="a0a48-109">The **Add-AzureRmNetworkInterfaceTapConfig** cmdlet creates a TapConfiguration resource associated to a NetworkInterface.</span></span> <span data-ttu-id="a0a48-110">Będzie to miało odwołanie do istniejącego zasobu VirtualNetworkTap.</span><span class="sxs-lookup"><span data-stu-id="a0a48-110">This will reference to an existing VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="a0a48-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a0a48-111">EXAMPLES</span></span>

### <span data-ttu-id="a0a48-112">Przykład 1: Dodawanie TapConfiguration do danego NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a0a48-112">Example 1: Add TapConfiguration to a given NetworkInterface</span></span>
```
PS C:\>Add-AzureRmNetworkInterfaceTapConfig -NetworkInterface $sourceNic -VirtualNetworkTap $vVirtualNetworkTap -Name 'myTapConfig'
```

<span data-ttu-id="a0a48-113">Dodaj TapConfiguration do sourceNic.</span><span class="sxs-lookup"><span data-stu-id="a0a48-113">Add the TapConfiguration to a sourceNic.</span></span> <span data-ttu-id="a0a48-114">Ruch z maszyny wirtualnej sourceNic będzie dublowany na docelowej maszynie wirtualnej określonej w zasobie vVirtualNetworkTap.</span><span class="sxs-lookup"><span data-stu-id="a0a48-114">The traffic from sourceNic VM will be mirrored to destination VM referred in vVirtualNetworkTap resource.</span></span>

## <span data-ttu-id="a0a48-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a0a48-115">PARAMETERS</span></span>

### <span data-ttu-id="a0a48-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0a48-116">-DefaultProfile</span></span>
<span data-ttu-id="a0a48-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a0a48-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0a48-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a0a48-118">-Name</span></span>
<span data-ttu-id="a0a48-119">Nazwa konfiguracji stuknij.</span><span class="sxs-lookup"><span data-stu-id="a0a48-119">Name of the tap configuration.</span></span>

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

### <span data-ttu-id="a0a48-120">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a0a48-120">-NetworkInterface</span></span>
<span data-ttu-id="a0a48-121">Odwołanie do zasobu interfejs sieciowy.</span><span class="sxs-lookup"><span data-stu-id="a0a48-121">The reference of the network interface resource.</span></span>

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

### <span data-ttu-id="a0a48-122">-VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="a0a48-122">-VirtualNetworkTap</span></span>
<span data-ttu-id="a0a48-123">Odwołanie do zasobu sieci wirtualnej TAP.</span><span class="sxs-lookup"><span data-stu-id="a0a48-123">The reference of the virtual network tap resource.</span></span>

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

### <span data-ttu-id="a0a48-124">-VirtualNetworkTapId</span><span class="sxs-lookup"><span data-stu-id="a0a48-124">-VirtualNetworkTapId</span></span>
<span data-ttu-id="a0a48-125">Odwołanie do zasobu sieci wirtualnej TAP.</span><span class="sxs-lookup"><span data-stu-id="a0a48-125">The reference of the virtual network tap resource.</span></span>

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

### <span data-ttu-id="a0a48-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a0a48-126">-Confirm</span></span>
<span data-ttu-id="a0a48-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0a48-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0a48-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0a48-128">-WhatIf</span></span>
<span data-ttu-id="a0a48-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0a48-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0a48-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a0a48-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0a48-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0a48-131">CommonParameters</span></span>
<span data-ttu-id="a0a48-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0a48-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0a48-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0a48-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0a48-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a0a48-134">INPUTS</span></span>

### <span data-ttu-id="a0a48-135">Microsoft. Azure. Commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a0a48-135">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="a0a48-136">System. String</span><span class="sxs-lookup"><span data-stu-id="a0a48-136">System.String</span></span>

### <span data-ttu-id="a0a48-137">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="a0a48-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="a0a48-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a0a48-138">OUTPUTS</span></span>

### <span data-ttu-id="a0a48-139">Microsoft. Azure. Commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a0a48-139">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="a0a48-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a0a48-140">NOTES</span></span>

## <span data-ttu-id="a0a48-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a0a48-141">RELATED LINKS</span></span>
