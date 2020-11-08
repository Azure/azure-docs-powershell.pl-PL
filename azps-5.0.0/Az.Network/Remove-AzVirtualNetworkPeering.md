---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
ms.openlocfilehash: 38530b5e4034286d623c82b841064760fe2e49e0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232769"
---
# <span data-ttu-id="d944d-101">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="d944d-101">Remove-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="d944d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d944d-102">SYNOPSIS</span></span>
<span data-ttu-id="d944d-103">Umożliwia usunięcie komunikacji równorzędnej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d944d-103">Removes a virtual network peering.</span></span>

## <span data-ttu-id="d944d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d944d-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String> [-Force]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d944d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d944d-105">DESCRIPTION</span></span>
<span data-ttu-id="d944d-106">Umożliwia usunięcie komunikacji równorzędnej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d944d-106">Removes a virtual network peering.</span></span>

## <span data-ttu-id="d944d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d944d-107">EXAMPLES</span></span>

### <span data-ttu-id="d944d-108">Przykład 1: usuwanie komunikacji równorzędnej sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="d944d-108">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="d944d-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d944d-109">PARAMETERS</span></span>

### <span data-ttu-id="d944d-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d944d-110">-AsJob</span></span>
<span data-ttu-id="d944d-111">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d944d-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d944d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d944d-112">-DefaultProfile</span></span>
<span data-ttu-id="d944d-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d944d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d944d-114">-Force</span><span class="sxs-lookup"><span data-stu-id="d944d-114">-Force</span></span>
<span data-ttu-id="d944d-115">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="d944d-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d944d-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d944d-116">-Name</span></span>
<span data-ttu-id="d944d-117">Nazwa elementu równorzędnego sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d944d-117">The virtual network peering name.</span></span>

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

### <span data-ttu-id="d944d-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d944d-118">-PassThru</span></span>
<span data-ttu-id="d944d-119">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="d944d-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d944d-120">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="d944d-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d944d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d944d-121">-ResourceGroupName</span></span>
<span data-ttu-id="d944d-122">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="d944d-122">The resource group name</span></span>

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

### <span data-ttu-id="d944d-123">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="d944d-123">-VirtualNetworkName</span></span>
<span data-ttu-id="d944d-124">Nazwa sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d944d-124">The virtual network name.</span></span>

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

### <span data-ttu-id="d944d-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d944d-125">-Confirm</span></span>
<span data-ttu-id="d944d-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d944d-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d944d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d944d-127">-WhatIf</span></span>
<span data-ttu-id="d944d-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d944d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d944d-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d944d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d944d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d944d-130">CommonParameters</span></span>
<span data-ttu-id="d944d-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d944d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d944d-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d944d-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d944d-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d944d-133">INPUTS</span></span>

### <span data-ttu-id="d944d-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d944d-134">System.String</span></span>

## <span data-ttu-id="d944d-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d944d-135">OUTPUTS</span></span>

### <span data-ttu-id="d944d-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d944d-136">System.Boolean</span></span>

## <span data-ttu-id="d944d-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d944d-137">NOTES</span></span>

## <span data-ttu-id="d944d-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d944d-138">RELATED LINKS</span></span>

[<span data-ttu-id="d944d-139">Dodaj-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="d944d-139">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="d944d-140">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="d944d-140">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="d944d-141">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="d944d-141">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)
