---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C48E204D-D7EC-4EFD-ADC5-C6F593313B9B
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetwork.md
ms.openlocfilehash: 18d73d317b1bf2056fdefdfbc112c56bc4ebdfec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006049"
---
# <span data-ttu-id="448af-101">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="448af-101">Remove-AzVirtualNetwork</span></span>

## <span data-ttu-id="448af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="448af-102">SYNOPSIS</span></span>
<span data-ttu-id="448af-103">Usuwa sieć wirtualną.</span><span class="sxs-lookup"><span data-stu-id="448af-103">Removes a virtual network.</span></span>

## <span data-ttu-id="448af-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="448af-104">SYNTAX</span></span>

```
Remove-AzVirtualNetwork -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="448af-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="448af-105">DESCRIPTION</span></span>
<span data-ttu-id="448af-106">Polecenie **cmdlet Remove-AzVirtualNetwork** usuwa sieć wirtualną platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="448af-106">The **Remove-AzVirtualNetwork** cmdlet removes an Azure virtual network.</span></span>

## <span data-ttu-id="448af-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="448af-107">EXAMPLES</span></span>

### <span data-ttu-id="448af-108">1. Tworzenie i usuwanie sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="448af-108">1: Create and delete a virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix 
    "10.0.2.0/24"

New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
    
Remove-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="448af-109">W tym przykładzie jest grupę zasobów, która jest siecią wirtualną, a następnie natychmiast usuwana.</span><span class="sxs-lookup"><span data-stu-id="448af-109">This example creates a virtual network in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="448af-110">Aby pominąć monit podczas usuwania sieci wirtualnej, użyj flagi -Force.</span><span class="sxs-lookup"><span data-stu-id="448af-110">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="448af-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="448af-111">PARAMETERS</span></span>

### <span data-ttu-id="448af-112">— AsJob</span><span class="sxs-lookup"><span data-stu-id="448af-112">-AsJob</span></span>
<span data-ttu-id="448af-113">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="448af-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="448af-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="448af-114">-DefaultProfile</span></span>
<span data-ttu-id="448af-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="448af-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="448af-116">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="448af-116">-Force</span></span>
<span data-ttu-id="448af-117">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="448af-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="448af-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="448af-118">-Name</span></span>
<span data-ttu-id="448af-119">Określa nazwę sieci wirtualnej, która jest usuwana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="448af-119">Specifies the name of the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="448af-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="448af-120">-PassThru</span></span>
<span data-ttu-id="448af-121">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="448af-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="448af-122">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="448af-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="448af-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="448af-123">-ResourceGroupName</span></span>
<span data-ttu-id="448af-124">Określa nazwę grupy zasobów zawierającej sieć wirtualną, która jest usuwana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="448af-124">Specifies the name of the resource group that contains the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="448af-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="448af-125">-Confirm</span></span>
<span data-ttu-id="448af-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="448af-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="448af-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="448af-127">-WhatIf</span></span>
<span data-ttu-id="448af-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="448af-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="448af-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="448af-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="448af-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="448af-130">CommonParameters</span></span>
<span data-ttu-id="448af-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="448af-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="448af-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="448af-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="448af-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="448af-133">INPUTS</span></span>

### <span data-ttu-id="448af-134">System.String</span><span class="sxs-lookup"><span data-stu-id="448af-134">System.String</span></span>

## <span data-ttu-id="448af-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="448af-135">OUTPUTS</span></span>

### <span data-ttu-id="448af-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="448af-136">System.Boolean</span></span>

## <span data-ttu-id="448af-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="448af-137">NOTES</span></span>

## <span data-ttu-id="448af-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="448af-138">RELATED LINKS</span></span>

[<span data-ttu-id="448af-139">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="448af-139">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="448af-140">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="448af-140">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="448af-141">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="448af-141">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)


