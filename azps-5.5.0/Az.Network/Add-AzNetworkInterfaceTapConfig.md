---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 1b51b7d086af738e356d7a6b65c17bdb45cbb518
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203182"
---
# <span data-ttu-id="8dc48-101">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="8dc48-101">Add-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="8dc48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8dc48-102">SYNOPSIS</span></span>
<span data-ttu-id="8dc48-103">Tworzy zasób TapConfiguration skojarzony z krojem NetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="8dc48-103">Creates a TapConfiguration resource associated to a NetworkInterface.</span></span> <span data-ttu-id="8dc48-104">Będzie to odwołanie do istniejącego zasobu VirtualNetworkTap.</span><span class="sxs-lookup"><span data-stu-id="8dc48-104">This will reference to an existing VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="8dc48-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8dc48-105">SYNTAX</span></span>

### <span data-ttu-id="8dc48-106">SetByResource (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="8dc48-106">SetByResource (Default)</span></span>
```
Add-AzNetworkInterfaceTapConfig -NetworkInterface <PSNetworkInterface> -Name <String>
 [-VirtualNetworkTap <PSVirtualNetworkTap>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8dc48-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="8dc48-107">SetByResourceId</span></span>
```
Add-AzNetworkInterfaceTapConfig -NetworkInterface <PSNetworkInterface> -Name <String>
 [-VirtualNetworkTapId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8dc48-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="8dc48-108">DESCRIPTION</span></span>
<span data-ttu-id="8dc48-109">Polecenie **cmdlet Add-AzNetworkInterfaceTapConfig** tworzy zasób TapConfiguration skojarzony z krojem NetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="8dc48-109">The **Add-AzNetworkInterfaceTapConfig** cmdlet creates a TapConfiguration resource associated to a NetworkInterface.</span></span> <span data-ttu-id="8dc48-110">Będzie to odwołanie do istniejącego zasobu VirtualNetworkTap.</span><span class="sxs-lookup"><span data-stu-id="8dc48-110">This will reference to an existing VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="8dc48-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8dc48-111">EXAMPLES</span></span>

### <span data-ttu-id="8dc48-112">Przykład 1. Dodawanie ustawienia TapConfiguration do danej czcionki NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="8dc48-112">Example 1: Add TapConfiguration to a given NetworkInterface</span></span>
```
PS C:\>Add-AzNetworkInterfaceTapConfig -NetworkInterface $sourceNic -VirtualNetworkTap $vVirtualNetworkTap -Name 'myTapConfig'
```

<span data-ttu-id="8dc48-113">Dodaj konfigurację TapConfiguration do sourceNic.</span><span class="sxs-lookup"><span data-stu-id="8dc48-113">Add the TapConfiguration to a sourceNic.</span></span> <span data-ttu-id="8dc48-114">Ruch z maszyny wirtualnej sourceNic będzie lustrzany do docelowej maszyny wirtualnej, o której mowa w zasobie vVirtualNetworkTap.</span><span class="sxs-lookup"><span data-stu-id="8dc48-114">The traffic from sourceNic VM will be mirrored to destination VM referred in vVirtualNetworkTap resource.</span></span>

## <span data-ttu-id="8dc48-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8dc48-115">PARAMETERS</span></span>

### <span data-ttu-id="8dc48-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dc48-116">-DefaultProfile</span></span>
<span data-ttu-id="8dc48-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8dc48-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8dc48-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8dc48-118">-Name</span></span>
<span data-ttu-id="8dc48-119">Nazwa konfiguracji naciśnięcia.</span><span class="sxs-lookup"><span data-stu-id="8dc48-119">Name of the tap configuration.</span></span>

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

### <span data-ttu-id="8dc48-120">- NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="8dc48-120">-NetworkInterface</span></span>
<span data-ttu-id="8dc48-121">Odwołanie do zasobu interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="8dc48-121">The reference of the network interface resource.</span></span>

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

### <span data-ttu-id="8dc48-122">— VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="8dc48-122">-VirtualNetworkTap</span></span>
<span data-ttu-id="8dc48-123">Odwołanie do zasobu sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8dc48-123">The reference of the virtual network tap resource.</span></span>

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

### <span data-ttu-id="8dc48-124">- VirtualNetworkTapId</span><span class="sxs-lookup"><span data-stu-id="8dc48-124">-VirtualNetworkTapId</span></span>
<span data-ttu-id="8dc48-125">Odwołanie do zasobu sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8dc48-125">The reference of the virtual network tap resource.</span></span>

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

### <span data-ttu-id="8dc48-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8dc48-126">-Confirm</span></span>
<span data-ttu-id="8dc48-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8dc48-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8dc48-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dc48-128">-WhatIf</span></span>
<span data-ttu-id="8dc48-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8dc48-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8dc48-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8dc48-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8dc48-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dc48-131">CommonParameters</span></span>
<span data-ttu-id="8dc48-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8dc48-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dc48-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8dc48-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dc48-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8dc48-134">INPUTS</span></span>

### <span data-ttu-id="8dc48-135">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="8dc48-135">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="8dc48-136">System.String</span><span class="sxs-lookup"><span data-stu-id="8dc48-136">System.String</span></span>

### <span data-ttu-id="8dc48-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="8dc48-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="8dc48-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8dc48-138">OUTPUTS</span></span>

### <span data-ttu-id="8dc48-139">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="8dc48-139">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="8dc48-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8dc48-140">NOTES</span></span>

## <span data-ttu-id="8dc48-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8dc48-141">RELATED LINKS</span></span>

[<span data-ttu-id="8dc48-142">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="8dc48-142">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="8dc48-143">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="8dc48-143">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="8dc48-144">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="8dc48-144">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)
