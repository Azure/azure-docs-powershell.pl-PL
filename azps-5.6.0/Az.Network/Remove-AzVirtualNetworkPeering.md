---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
ms.openlocfilehash: f47b1bcc571337de8a64c591383367568cf7d67e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993525"
---
# <span data-ttu-id="e0069-101">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="e0069-101">Remove-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="e0069-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0069-102">SYNOPSIS</span></span>
<span data-ttu-id="e0069-103">Usuwa wirtualną sieć równorzędną.</span><span class="sxs-lookup"><span data-stu-id="e0069-103">Removes a virtual network peering.</span></span>

## <span data-ttu-id="e0069-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e0069-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String> [-Force]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0069-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e0069-105">DESCRIPTION</span></span>
<span data-ttu-id="e0069-106">Usuwa wirtualną sieć równorzędną.</span><span class="sxs-lookup"><span data-stu-id="e0069-106">Removes a virtual network peering.</span></span>

## <span data-ttu-id="e0069-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e0069-107">EXAMPLES</span></span>

### <span data-ttu-id="e0069-108">Przykład 1. Usuwanie komunikacji równorzędnej w sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="e0069-108">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="e0069-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0069-109">PARAMETERS</span></span>

### <span data-ttu-id="e0069-110">— AsJob</span><span class="sxs-lookup"><span data-stu-id="e0069-110">-AsJob</span></span>
<span data-ttu-id="e0069-111">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e0069-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e0069-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0069-112">-DefaultProfile</span></span>
<span data-ttu-id="e0069-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e0069-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0069-114">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="e0069-114">-Force</span></span>
<span data-ttu-id="e0069-115">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e0069-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e0069-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e0069-116">-Name</span></span>
<span data-ttu-id="e0069-117">Nazwa komunikacji równorzędnej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e0069-117">The virtual network peering name.</span></span>

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

### <span data-ttu-id="e0069-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e0069-118">-PassThru</span></span>
<span data-ttu-id="e0069-119">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="e0069-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e0069-120">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="e0069-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e0069-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0069-121">-ResourceGroupName</span></span>
<span data-ttu-id="e0069-122">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="e0069-122">The resource group name</span></span>

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

### <span data-ttu-id="e0069-123">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="e0069-123">-VirtualNetworkName</span></span>
<span data-ttu-id="e0069-124">Nazwa sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e0069-124">The virtual network name.</span></span>

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

### <span data-ttu-id="e0069-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e0069-125">-Confirm</span></span>
<span data-ttu-id="e0069-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e0069-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0069-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0069-127">-WhatIf</span></span>
<span data-ttu-id="e0069-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0069-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0069-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e0069-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0069-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0069-130">CommonParameters</span></span>
<span data-ttu-id="e0069-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0069-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0069-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0069-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0069-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e0069-133">INPUTS</span></span>

### <span data-ttu-id="e0069-134">System.String</span><span class="sxs-lookup"><span data-stu-id="e0069-134">System.String</span></span>

## <span data-ttu-id="e0069-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e0069-135">OUTPUTS</span></span>

### <span data-ttu-id="e0069-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e0069-136">System.Boolean</span></span>

## <span data-ttu-id="e0069-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e0069-137">NOTES</span></span>

## <span data-ttu-id="e0069-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e0069-138">RELATED LINKS</span></span>

[<span data-ttu-id="e0069-139">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="e0069-139">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="e0069-140">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="e0069-140">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="e0069-141">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="e0069-141">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)
