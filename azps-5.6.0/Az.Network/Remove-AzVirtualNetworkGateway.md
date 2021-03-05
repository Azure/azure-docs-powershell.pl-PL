---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A35BB728-A7EF-4ADF-B1A9-25A156434E99
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGateway.md
ms.openlocfilehash: c4841678a1e1f318da36b506cc56e586244c233f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006033"
---
# <span data-ttu-id="2a287-101">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2a287-101">Remove-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="2a287-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a287-102">SYNOPSIS</span></span>
<span data-ttu-id="2a287-103">Usuwanie bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="2a287-103">Deletes a Virtual Network Gateway</span></span>

## <span data-ttu-id="2a287-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2a287-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a287-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2a287-105">DESCRIPTION</span></span>
<span data-ttu-id="2a287-106">Wirtualna brama sieciowa to obiekt reprezentujący bramę na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="2a287-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="2a287-107">Polecenie **cmdlet Get-AzVirtualNetworkGateway** zwraca obiekt bramy na platformie Azure na podstawie nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2a287-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="2a287-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2a287-108">EXAMPLES</span></span>

### <span data-ttu-id="2a287-109">Przykład 1. Usuwanie bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="2a287-109">Example 1: Delete a Virtual Network Gateway</span></span>
```powershell
Remove-AzVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="2a287-110">Usuwa obiekt bramy sieci wirtualnej o nazwie "myGateway" w grupie zasobów "myRG" Uwaga: Należy najpierw usunąć wszystkie połączenia z wirtualną bramą sieciową przy użyciu polecenia cmdlet **Remove-AzVirtualNetworkGatewayConnection.**</span><span class="sxs-lookup"><span data-stu-id="2a287-110">Deletes the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG" Note: You must first delete all connections to the Virtual Network Gateway using the **Remove-AzVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="2a287-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a287-111">PARAMETERS</span></span>

### <span data-ttu-id="2a287-112">— AsJob</span><span class="sxs-lookup"><span data-stu-id="2a287-112">-AsJob</span></span>
<span data-ttu-id="2a287-113">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="2a287-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2a287-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a287-114">-DefaultProfile</span></span>
<span data-ttu-id="2a287-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2a287-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a287-116">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="2a287-116">-Force</span></span>
<span data-ttu-id="2a287-117">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="2a287-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2a287-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="2a287-118">-Name</span></span>
<span data-ttu-id="2a287-119">Określa nazwę bramy sieci wirtualnej, która jest usuwana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a287-119">Specifies the name of the virtual network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2a287-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2a287-120">-PassThru</span></span>
<span data-ttu-id="2a287-121">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="2a287-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2a287-122">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="2a287-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2a287-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a287-123">-ResourceGroupName</span></span>
<span data-ttu-id="2a287-124">Określa nazwę grupy zasobów zawierającej bramę sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2a287-124">Specifies the name of the resource group that contains the virtual network gateway.</span></span>

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

### <span data-ttu-id="2a287-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2a287-125">-Confirm</span></span>
<span data-ttu-id="2a287-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2a287-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a287-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a287-127">-WhatIf</span></span>
<span data-ttu-id="2a287-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a287-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a287-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2a287-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a287-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a287-130">CommonParameters</span></span>
<span data-ttu-id="2a287-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a287-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a287-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a287-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a287-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2a287-133">INPUTS</span></span>

### <span data-ttu-id="2a287-134">System.String</span><span class="sxs-lookup"><span data-stu-id="2a287-134">System.String</span></span>

## <span data-ttu-id="2a287-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2a287-135">OUTPUTS</span></span>

### <span data-ttu-id="2a287-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2a287-136">System.Boolean</span></span>

## <span data-ttu-id="2a287-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2a287-137">NOTES</span></span>

## <span data-ttu-id="2a287-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2a287-138">RELATED LINKS</span></span>

[<span data-ttu-id="2a287-139">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2a287-139">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="2a287-140">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2a287-140">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="2a287-141">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2a287-141">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="2a287-142">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2a287-142">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="2a287-143">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2a287-143">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
