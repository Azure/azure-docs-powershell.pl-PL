---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 2da755a4ac3044c6499faee82a74e2c9ec7d9f6e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982449"
---
# <span data-ttu-id="a82a5-101">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="a82a5-101">Add-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="a82a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a82a5-102">SYNOPSIS</span></span>
<span data-ttu-id="a82a5-103">Tworzy zasób TapConfiguration skojarzony z krojem NetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="a82a5-103">Creates a TapConfiguration resource associated to a NetworkInterface.</span></span> <span data-ttu-id="a82a5-104">Będzie to odwołanie do istniejącego zasobu VirtualNetworkTap.</span><span class="sxs-lookup"><span data-stu-id="a82a5-104">This will reference to an existing VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="a82a5-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a82a5-105">SYNTAX</span></span>

### <span data-ttu-id="a82a5-106">SetByResource (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="a82a5-106">SetByResource (Default)</span></span>
```
Add-AzNetworkInterfaceTapConfig -NetworkInterface <PSNetworkInterface> -Name <String>
 [-VirtualNetworkTap <PSVirtualNetworkTap>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a82a5-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a82a5-107">SetByResourceId</span></span>
```
Add-AzNetworkInterfaceTapConfig -NetworkInterface <PSNetworkInterface> -Name <String>
 [-VirtualNetworkTapId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a82a5-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="a82a5-108">DESCRIPTION</span></span>
<span data-ttu-id="a82a5-109">Polecenie **cmdlet Add-AzNetworkInterfaceTapConfig** tworzy zasób TapConfiguration skojarzony z krojem NetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="a82a5-109">The **Add-AzNetworkInterfaceTapConfig** cmdlet creates a TapConfiguration resource associated to a NetworkInterface.</span></span> <span data-ttu-id="a82a5-110">Będzie to odwołanie do istniejącego zasobu VirtualNetworkTap.</span><span class="sxs-lookup"><span data-stu-id="a82a5-110">This will reference to an existing VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="a82a5-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a82a5-111">EXAMPLES</span></span>

### <span data-ttu-id="a82a5-112">Przykład 1. Dodawanie ustawienia TapConfiguration do danej czcionki NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a82a5-112">Example 1: Add TapConfiguration to a given NetworkInterface</span></span>
```
PS C:\>Add-AzNetworkInterfaceTapConfig -NetworkInterface $sourceNic -VirtualNetworkTap $vVirtualNetworkTap -Name 'myTapConfig'
```

<span data-ttu-id="a82a5-113">Dodaj konfigurację TapConfiguration do sourceNic.</span><span class="sxs-lookup"><span data-stu-id="a82a5-113">Add the TapConfiguration to a sourceNic.</span></span> <span data-ttu-id="a82a5-114">Ruch z maszyny wirtualnej sourceNic będzie dublowany do docelowej maszyny wirtualnej, która jest określana w zasobie vVirtualNetworkTap.</span><span class="sxs-lookup"><span data-stu-id="a82a5-114">The traffic from sourceNic VM will be mirrored to destination VM referred in vVirtualNetworkTap resource.</span></span>

## <span data-ttu-id="a82a5-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a82a5-115">PARAMETERS</span></span>

### <span data-ttu-id="a82a5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a82a5-116">-DefaultProfile</span></span>
<span data-ttu-id="a82a5-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a82a5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a82a5-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a82a5-118">-Name</span></span>
<span data-ttu-id="a82a5-119">Nazwa konfiguracji naciśnięcia.</span><span class="sxs-lookup"><span data-stu-id="a82a5-119">Name of the tap configuration.</span></span>

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

### <span data-ttu-id="a82a5-120">- NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a82a5-120">-NetworkInterface</span></span>
<span data-ttu-id="a82a5-121">Odwołanie do zasobu interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="a82a5-121">The reference of the network interface resource.</span></span>

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

### <span data-ttu-id="a82a5-122">— VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="a82a5-122">-VirtualNetworkTap</span></span>
<span data-ttu-id="a82a5-123">Odwołanie do zasobu sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a82a5-123">The reference of the virtual network tap resource.</span></span>

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

### <span data-ttu-id="a82a5-124">- VirtualNetworkTapId</span><span class="sxs-lookup"><span data-stu-id="a82a5-124">-VirtualNetworkTapId</span></span>
<span data-ttu-id="a82a5-125">Odwołanie do zasobu sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a82a5-125">The reference of the virtual network tap resource.</span></span>

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

### <span data-ttu-id="a82a5-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a82a5-126">-Confirm</span></span>
<span data-ttu-id="a82a5-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a82a5-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a82a5-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a82a5-128">-WhatIf</span></span>
<span data-ttu-id="a82a5-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a82a5-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a82a5-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a82a5-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a82a5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a82a5-131">CommonParameters</span></span>
<span data-ttu-id="a82a5-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a82a5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a82a5-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a82a5-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a82a5-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a82a5-134">INPUTS</span></span>

### <span data-ttu-id="a82a5-135">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a82a5-135">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="a82a5-136">System.String</span><span class="sxs-lookup"><span data-stu-id="a82a5-136">System.String</span></span>

### <span data-ttu-id="a82a5-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="a82a5-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="a82a5-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a82a5-138">OUTPUTS</span></span>

### <span data-ttu-id="a82a5-139">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a82a5-139">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="a82a5-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a82a5-140">NOTES</span></span>

## <span data-ttu-id="a82a5-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a82a5-141">RELATED LINKS</span></span>

[<span data-ttu-id="a82a5-142">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="a82a5-142">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="a82a5-143">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="a82a5-143">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="a82a5-144">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="a82a5-144">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)
