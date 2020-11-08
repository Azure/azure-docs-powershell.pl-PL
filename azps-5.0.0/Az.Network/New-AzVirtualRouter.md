---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
ms.openlocfilehash: 9bfaea690ab23df6e7ba5480aaeb28ca00dfa20c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225366"
---
# <span data-ttu-id="485a4-101">New-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="485a4-101">New-AzVirtualRouter</span></span>

## <span data-ttu-id="485a4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="485a4-102">SYNOPSIS</span></span>
<span data-ttu-id="485a4-103">Tworzy usługę Azure VirtualRouter.</span><span class="sxs-lookup"><span data-stu-id="485a4-103">Creates an Azure VirtualRouter.</span></span>

## <span data-ttu-id="485a4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="485a4-104">SYNTAX</span></span>

```
New-AzVirtualRouter -ResourceGroupName <String> -Name <String> -HostedSubnet <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="485a4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="485a4-105">DESCRIPTION</span></span>
<span data-ttu-id="485a4-106">Polecenie cmdlet **New-AzVirtualRouter** tworzy składnik Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="485a4-106">The **New-AzVirtualRouter** cmdlet creates an Azure VirtualRouter</span></span>

## <span data-ttu-id="485a4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="485a4-107">EXAMPLES</span></span>

### <span data-ttu-id="485a4-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="485a4-108">Example 1</span></span>
```powershell
$subnet = New-AzVirtualNetworkSubnetConfig -Name $subnetName -AddressPrefix 10.0.0.0/24
$vnet = New-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroupName -Location $resourceGroupLocation -AddressPrefix 10.0.0.0/16 -Subnet $subnet
$subnetId = (Get-AzVirtualNetworkSubnetConfig -Name $subnetName -VirtualNetwork $vnet).Id
New-AzVirtualRouter -Name $virtualRouterName -ResourceGroupName $resourceGroupName -Location $resourceGroupLocation -HostedSubnet $subnetId
```

## <span data-ttu-id="485a4-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="485a4-109">PARAMETERS</span></span>

### <span data-ttu-id="485a4-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="485a4-110">-AsJob</span></span>
<span data-ttu-id="485a4-111">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="485a4-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="485a4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="485a4-112">-DefaultProfile</span></span>
<span data-ttu-id="485a4-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="485a4-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="485a4-114">-Force</span><span class="sxs-lookup"><span data-stu-id="485a4-114">-Force</span></span>
<span data-ttu-id="485a4-115">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="485a4-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="485a4-116">-HostedSubnet</span><span class="sxs-lookup"><span data-stu-id="485a4-116">-HostedSubnet</span></span>
<span data-ttu-id="485a4-117">Podsieć, w której jest hostowany router wirtualny.</span><span class="sxs-lookup"><span data-stu-id="485a4-117">The subnet where the virtual router is hosted.</span></span>

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

### <span data-ttu-id="485a4-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="485a4-118">-Location</span></span>
<span data-ttu-id="485a4-119">Lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="485a4-119">The location.</span></span>

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

### <span data-ttu-id="485a4-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="485a4-120">-Name</span></span>
<span data-ttu-id="485a4-121">Nazwa routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="485a4-121">The name of the virtual router.</span></span>

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

### <span data-ttu-id="485a4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="485a4-122">-ResourceGroupName</span></span>
<span data-ttu-id="485a4-123">Nazwa grupy zasobów routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="485a4-123">The resource group name of the virtual router.</span></span>

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

### <span data-ttu-id="485a4-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="485a4-124">-Tag</span></span>
<span data-ttu-id="485a4-125">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="485a4-125">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="485a4-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="485a4-126">-Confirm</span></span>
<span data-ttu-id="485a4-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="485a4-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="485a4-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="485a4-128">-WhatIf</span></span>
<span data-ttu-id="485a4-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="485a4-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="485a4-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="485a4-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="485a4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="485a4-131">CommonParameters</span></span>
<span data-ttu-id="485a4-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="485a4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="485a4-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="485a4-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="485a4-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="485a4-134">INPUTS</span></span>

### <span data-ttu-id="485a4-135">System. String</span><span class="sxs-lookup"><span data-stu-id="485a4-135">System.String</span></span>

### <span data-ttu-id="485a4-136">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="485a4-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="485a4-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="485a4-137">OUTPUTS</span></span>

### <span data-ttu-id="485a4-138">Microsoft. Azure. Commands. Network. models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="485a4-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="485a4-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="485a4-139">NOTES</span></span>

## <span data-ttu-id="485a4-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="485a4-140">RELATED LINKS</span></span>
