---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
ms.openlocfilehash: 608be77335c0201b8ae1d17b34057025392f1072
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978250"
---
# <span data-ttu-id="782aa-101">New-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="782aa-101">New-AzVirtualRouter</span></span>

## <span data-ttu-id="782aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="782aa-102">SYNOPSIS</span></span>
<span data-ttu-id="782aa-103">Tworzy wirtualny program Azure VirtualRouter.</span><span class="sxs-lookup"><span data-stu-id="782aa-103">Creates an Azure VirtualRouter.</span></span>

## <span data-ttu-id="782aa-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="782aa-104">SYNTAX</span></span>

```
New-AzVirtualRouter -ResourceGroupName <String> -Name <String> -HostedSubnet <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="782aa-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="782aa-105">DESCRIPTION</span></span>
<span data-ttu-id="782aa-106">Polecenie **cmdlet New-AzVirtualRouter** tworzy narzędzie Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="782aa-106">The **New-AzVirtualRouter** cmdlet creates an Azure VirtualRouter</span></span>

## <span data-ttu-id="782aa-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="782aa-107">EXAMPLES</span></span>

### <span data-ttu-id="782aa-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="782aa-108">Example 1</span></span>
```powershell
$subnet = New-AzVirtualNetworkSubnetConfig -Name $subnetName -AddressPrefix 10.0.0.0/24
$vnet = New-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroupName -Location $resourceGroupLocation -AddressPrefix 10.0.0.0/16 -Subnet $subnet
$subnetId = (Get-AzVirtualNetworkSubnetConfig -Name $subnetName -VirtualNetwork $vnet).Id
New-AzVirtualRouter -Name $virtualRouterName -ResourceGroupName $resourceGroupName -Location $resourceGroupLocation -HostedSubnet $subnetId
```

## <span data-ttu-id="782aa-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="782aa-109">PARAMETERS</span></span>

### <span data-ttu-id="782aa-110">— AsJob</span><span class="sxs-lookup"><span data-stu-id="782aa-110">-AsJob</span></span>
<span data-ttu-id="782aa-111">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="782aa-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="782aa-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="782aa-112">-DefaultProfile</span></span>
<span data-ttu-id="782aa-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="782aa-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="782aa-114">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="782aa-114">-Force</span></span>
<span data-ttu-id="782aa-115">Nie pytaj o potwierdzenie, jeśli chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="782aa-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="782aa-116">-HostedSubnet</span><span class="sxs-lookup"><span data-stu-id="782aa-116">-HostedSubnet</span></span>
<span data-ttu-id="782aa-117">Podsieci, w której jest hostowany router wirtualny.</span><span class="sxs-lookup"><span data-stu-id="782aa-117">The subnet where the virtual router is hosted.</span></span>

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

### <span data-ttu-id="782aa-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="782aa-118">-Location</span></span>
<span data-ttu-id="782aa-119">Lokalizacja.</span><span class="sxs-lookup"><span data-stu-id="782aa-119">The location.</span></span>

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

### <span data-ttu-id="782aa-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="782aa-120">-Name</span></span>
<span data-ttu-id="782aa-121">Nazwa routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="782aa-121">The name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="782aa-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="782aa-122">-ResourceGroupName</span></span>
<span data-ttu-id="782aa-123">Nazwa grupy zasobów routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="782aa-123">The resource group name of the virtual router.</span></span>

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

### <span data-ttu-id="782aa-124">— Tag</span><span class="sxs-lookup"><span data-stu-id="782aa-124">-Tag</span></span>
<span data-ttu-id="782aa-125">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="782aa-125">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="782aa-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="782aa-126">-Confirm</span></span>
<span data-ttu-id="782aa-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="782aa-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="782aa-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="782aa-128">-WhatIf</span></span>
<span data-ttu-id="782aa-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="782aa-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="782aa-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="782aa-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="782aa-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="782aa-131">CommonParameters</span></span>
<span data-ttu-id="782aa-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="782aa-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="782aa-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="782aa-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="782aa-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="782aa-134">INPUTS</span></span>

### <span data-ttu-id="782aa-135">System.String</span><span class="sxs-lookup"><span data-stu-id="782aa-135">System.String</span></span>

### <span data-ttu-id="782aa-136">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="782aa-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="782aa-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="782aa-137">OUTPUTS</span></span>

### <span data-ttu-id="782aa-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="782aa-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="782aa-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="782aa-139">NOTES</span></span>

## <span data-ttu-id="782aa-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="782aa-140">RELATED LINKS</span></span>
