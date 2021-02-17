---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkTap.md
ms.openlocfilehash: dc6ca5c41e5f819c8f1db3d0c601b48273e3d78e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184619"
---
# <span data-ttu-id="ef73b-101">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="ef73b-101">Get-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="ef73b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef73b-102">SYNOPSIS</span></span>
<span data-ttu-id="ef73b-103">Otrzymuje naciśnięcie w sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="ef73b-103">Gets a virtual network tap</span></span>

## <span data-ttu-id="ef73b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ef73b-104">SYNTAX</span></span>

### <span data-ttu-id="ef73b-105">ListParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="ef73b-105">ListParameterSet (Default)</span></span>
```
Get-AzVirtualNetworkTap [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef73b-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef73b-106">GetByResourceIdParameterSet</span></span>
```
Get-AzVirtualNetworkTap -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ef73b-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="ef73b-107">DESCRIPTION</span></span>
<span data-ttu-id="ef73b-108">Polecenie **cmdlet Get-AzVirtualNetworkTap** pobiera naciśnięcie sieci wirtualnej platformy Azure lub listę naciskanych sieci wirtualnych platformy Azure w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="ef73b-108">The **Get-AzVirtualNetworkTap** cmdlet gets an Azure virtual network tap or a list of Azure virtual network taps in a resource group.</span></span>

## <span data-ttu-id="ef73b-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ef73b-109">EXAMPLES</span></span>

### <span data-ttu-id="ef73b-110">Przykład 1. Uzyskiwanie dotknięcia sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="ef73b-110">Example 1: Get a virtual network tap</span></span>
```
PS C:\> Get-AzVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
```

<span data-ttu-id="ef73b-111">To polecenie pobiera odwołanie do naciśnięcia VirtualNetwork dla danego "VirtualTap1" w "ResourceGroup1".</span><span class="sxs-lookup"><span data-stu-id="ef73b-111">This command gets a VirtualNetwork tap reference for given "VirtualTap1" in "ResourceGroup1".</span></span>

### <span data-ttu-id="ef73b-112">Przykład 2. Uzyskiwanie wszystkich nacięć sieci wirtualnej przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="ef73b-112">Example 2: Get all virtual network taps using filtering</span></span>
```
PS C:\> Get-AzVirtualNetworkTap -Name "VirtualTap*"
```

<span data-ttu-id="ef73b-113">To polecenie pobiera wszystkie odwołania do naciśnięciem w virtualNetwork, które zaczynają się od "VirtualTap".</span><span class="sxs-lookup"><span data-stu-id="ef73b-113">This command gets all VirtualNetwork tap references that start with "VirtualTap".</span></span>

## <span data-ttu-id="ef73b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef73b-114">PARAMETERS</span></span>

### <span data-ttu-id="ef73b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef73b-115">-DefaultProfile</span></span>
<span data-ttu-id="ef73b-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ef73b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef73b-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ef73b-117">-Name</span></span>
<span data-ttu-id="ef73b-118">Nazwa naciśnięcia.</span><span class="sxs-lookup"><span data-stu-id="ef73b-118">The name of the tap.</span></span>

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

### <span data-ttu-id="ef73b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef73b-119">-ResourceGroupName</span></span>
<span data-ttu-id="ef73b-120">Nazwa grupy zasobów sieci wirtualnej naciśnij.</span><span class="sxs-lookup"><span data-stu-id="ef73b-120">The resource group name of the virtual network tap.</span></span>

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

### <span data-ttu-id="ef73b-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef73b-121">-ResourceId</span></span>
<span data-ttu-id="ef73b-122">ResourceId zasobu VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="ef73b-122">ResourceId of the VirtualNetworkTap resource</span></span>

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

### <span data-ttu-id="ef73b-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ef73b-123">-Confirm</span></span>
<span data-ttu-id="ef73b-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ef73b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef73b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef73b-125">-WhatIf</span></span>
<span data-ttu-id="ef73b-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef73b-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ef73b-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ef73b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef73b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef73b-128">CommonParameters</span></span>
<span data-ttu-id="ef73b-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef73b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef73b-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ef73b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef73b-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ef73b-131">INPUTS</span></span>

### <span data-ttu-id="ef73b-132">System.String</span><span class="sxs-lookup"><span data-stu-id="ef73b-132">System.String</span></span>

## <span data-ttu-id="ef73b-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ef73b-133">OUTPUTS</span></span>

### <span data-ttu-id="ef73b-134">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="ef73b-134">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="ef73b-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ef73b-135">NOTES</span></span>

## <span data-ttu-id="ef73b-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ef73b-136">RELATED LINKS</span></span>

[<span data-ttu-id="ef73b-137">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="ef73b-137">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="ef73b-138">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="ef73b-138">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)

[<span data-ttu-id="ef73b-139">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="ef73b-139">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)
