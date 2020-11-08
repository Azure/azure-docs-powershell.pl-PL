---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkTap.md
ms.openlocfilehash: dc6ca5c41e5f819c8f1db3d0c601b48273e3d78e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063390"
---
# <span data-ttu-id="3dcf4-101">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="3dcf4-101">Get-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="3dcf4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3dcf4-102">SYNOPSIS</span></span>
<span data-ttu-id="3dcf4-103">Umożliwia wybranie sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="3dcf4-103">Gets a virtual network tap</span></span>

## <span data-ttu-id="3dcf4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3dcf4-104">SYNTAX</span></span>

### <span data-ttu-id="3dcf4-105">ListParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3dcf4-105">ListParameterSet (Default)</span></span>
```
Get-AzVirtualNetworkTap [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3dcf4-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3dcf4-106">GetByResourceIdParameterSet</span></span>
```
Get-AzVirtualNetworkTap -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3dcf4-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3dcf4-107">DESCRIPTION</span></span>
<span data-ttu-id="3dcf4-108">Polecenie cmdlet **Get-AzVirtualNetworkTap umożliwia pobranie** wirtualnej sieci Azure w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="3dcf4-108">The **Get-AzVirtualNetworkTap** cmdlet gets an Azure virtual network tap or a list of Azure virtual network taps in a resource group.</span></span>

## <span data-ttu-id="3dcf4-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3dcf4-109">EXAMPLES</span></span>

### <span data-ttu-id="3dcf4-110">Przykład 1: Uzyskaj sieć wirtualną naciśnij</span><span class="sxs-lookup"><span data-stu-id="3dcf4-110">Example 1: Get a virtual network tap</span></span>
```
PS C:\> Get-AzVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
```

<span data-ttu-id="3dcf4-111">To polecenie pobiera VirtualNetwork, dla którego otrzymano odwołanie "VirtualTap1" w "ResourceGroup1".</span><span class="sxs-lookup"><span data-stu-id="3dcf4-111">This command gets a VirtualNetwork tap reference for given "VirtualTap1" in "ResourceGroup1".</span></span>

### <span data-ttu-id="3dcf4-112">Przykład 2: pobieranie wszystkich naciśnięć sieci wirtualnej za pomocą funkcji filtrowania</span><span class="sxs-lookup"><span data-stu-id="3dcf4-112">Example 2: Get all virtual network taps using filtering</span></span>
```
PS C:\> Get-AzVirtualNetworkTap -Name "VirtualTap*"
```

<span data-ttu-id="3dcf4-113">To polecenie pobiera wszystkie VirtualNetwork, które rozpoczynają się od "VirtualTap".</span><span class="sxs-lookup"><span data-stu-id="3dcf4-113">This command gets all VirtualNetwork tap references that start with "VirtualTap".</span></span>

## <span data-ttu-id="3dcf4-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3dcf4-114">PARAMETERS</span></span>

### <span data-ttu-id="3dcf4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dcf4-115">-DefaultProfile</span></span>
<span data-ttu-id="3dcf4-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3dcf4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3dcf4-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3dcf4-117">-Name</span></span>
<span data-ttu-id="3dcf4-118">Nazwa naciśnięcia przycisku.</span><span class="sxs-lookup"><span data-stu-id="3dcf4-118">The name of the tap.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="3dcf4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3dcf4-119">-ResourceGroupName</span></span>
<span data-ttu-id="3dcf4-120">Nazwa grupy zasobów naciśnięcie sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3dcf4-120">The resource group name of the virtual network tap.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="3dcf4-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3dcf4-121">-ResourceId</span></span>
<span data-ttu-id="3dcf4-122">Identyfikator zasobu VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="3dcf4-122">ResourceId of the VirtualNetworkTap resource</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dcf4-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3dcf4-123">-Confirm</span></span>
<span data-ttu-id="3dcf4-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3dcf4-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3dcf4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3dcf4-125">-WhatIf</span></span>
<span data-ttu-id="3dcf4-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3dcf4-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3dcf4-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3dcf4-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3dcf4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dcf4-128">CommonParameters</span></span>
<span data-ttu-id="3dcf4-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dcf4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dcf4-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3dcf4-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dcf4-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3dcf4-131">INPUTS</span></span>

### <span data-ttu-id="3dcf4-132">System. String</span><span class="sxs-lookup"><span data-stu-id="3dcf4-132">System.String</span></span>

## <span data-ttu-id="3dcf4-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3dcf4-133">OUTPUTS</span></span>

### <span data-ttu-id="3dcf4-134">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="3dcf4-134">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="3dcf4-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3dcf4-135">NOTES</span></span>

## <span data-ttu-id="3dcf4-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3dcf4-136">RELATED LINKS</span></span>

[<span data-ttu-id="3dcf4-137">Nowe — AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="3dcf4-137">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="3dcf4-138">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="3dcf4-138">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)

[<span data-ttu-id="3dcf4-139">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="3dcf4-139">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)
