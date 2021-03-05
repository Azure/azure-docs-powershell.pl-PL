---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkTap.md
ms.openlocfilehash: 154cededf20ceb88fdbc851b96189282e1b6123a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003594"
---
# <span data-ttu-id="10912-101">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="10912-101">Get-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="10912-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10912-102">SYNOPSIS</span></span>
<span data-ttu-id="10912-103">Otrzymuje dotknięcie sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="10912-103">Gets a virtual network tap</span></span>

## <span data-ttu-id="10912-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="10912-104">SYNTAX</span></span>

### <span data-ttu-id="10912-105">ListParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="10912-105">ListParameterSet (Default)</span></span>
```
Get-AzVirtualNetworkTap [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10912-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="10912-106">GetByResourceIdParameterSet</span></span>
```
Get-AzVirtualNetworkTap -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="10912-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="10912-107">DESCRIPTION</span></span>
<span data-ttu-id="10912-108">Polecenie **cmdlet Get-AzVirtualNetworkTap** pobiera naciśnięcie sieci wirtualnej platformy Azure lub listę naciskanych sieci wirtualnych platformy Azure w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="10912-108">The **Get-AzVirtualNetworkTap** cmdlet gets an Azure virtual network tap or a list of Azure virtual network taps in a resource group.</span></span>

## <span data-ttu-id="10912-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="10912-109">EXAMPLES</span></span>

### <span data-ttu-id="10912-110">Przykład 1. Uzyskiwanie naciśnięcia sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="10912-110">Example 1: Get a virtual network tap</span></span>
```
PS C:\> Get-AzVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
```

<span data-ttu-id="10912-111">To polecenie pobiera odwołanie do naciśnięcia VirtualNetwork dla danego "VirtualTap1" w "ResourceGroup1".</span><span class="sxs-lookup"><span data-stu-id="10912-111">This command gets a VirtualNetwork tap reference for given "VirtualTap1" in "ResourceGroup1".</span></span>

### <span data-ttu-id="10912-112">Przykład 2. Uzyskiwanie wszystkich nacięć sieci wirtualnej za pomocą filtrowania</span><span class="sxs-lookup"><span data-stu-id="10912-112">Example 2: Get all virtual network taps using filtering</span></span>
```
PS C:\> Get-AzVirtualNetworkTap -Name "VirtualTap*"
```

<span data-ttu-id="10912-113">To polecenie pobiera wszystkie odwołania do naciśnięciem w virtualNetwork, które zaczynają się od "VirtualTap".</span><span class="sxs-lookup"><span data-stu-id="10912-113">This command gets all VirtualNetwork tap references that start with "VirtualTap".</span></span>

## <span data-ttu-id="10912-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10912-114">PARAMETERS</span></span>

### <span data-ttu-id="10912-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10912-115">-DefaultProfile</span></span>
<span data-ttu-id="10912-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="10912-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10912-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="10912-117">-Name</span></span>
<span data-ttu-id="10912-118">Nazwa naciśnięcia.</span><span class="sxs-lookup"><span data-stu-id="10912-118">The name of the tap.</span></span>

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

### <span data-ttu-id="10912-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10912-119">-ResourceGroupName</span></span>
<span data-ttu-id="10912-120">Nazwa grupy zasobów sieci wirtualnej naciśnij.</span><span class="sxs-lookup"><span data-stu-id="10912-120">The resource group name of the virtual network tap.</span></span>

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

### <span data-ttu-id="10912-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="10912-121">-ResourceId</span></span>
<span data-ttu-id="10912-122">ResourceId zasobu VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="10912-122">ResourceId of the VirtualNetworkTap resource</span></span>

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

### <span data-ttu-id="10912-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="10912-123">-Confirm</span></span>
<span data-ttu-id="10912-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="10912-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10912-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10912-125">-WhatIf</span></span>
<span data-ttu-id="10912-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10912-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="10912-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="10912-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10912-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10912-128">CommonParameters</span></span>
<span data-ttu-id="10912-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10912-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10912-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="10912-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10912-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10912-131">INPUTS</span></span>

### <span data-ttu-id="10912-132">System.String</span><span class="sxs-lookup"><span data-stu-id="10912-132">System.String</span></span>

## <span data-ttu-id="10912-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10912-133">OUTPUTS</span></span>

### <span data-ttu-id="10912-134">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="10912-134">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="10912-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="10912-135">NOTES</span></span>

## <span data-ttu-id="10912-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="10912-136">RELATED LINKS</span></span>

[<span data-ttu-id="10912-137">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="10912-137">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="10912-138">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="10912-138">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)

[<span data-ttu-id="10912-139">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="10912-139">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)
