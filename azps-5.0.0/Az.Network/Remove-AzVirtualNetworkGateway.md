---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A35BB728-A7EF-4ADF-B1A9-25A156434E99
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGateway.md
ms.openlocfilehash: 7708202630b5c7797d9ec3eda77475c82e1c358a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319129"
---
# <span data-ttu-id="25b0a-101">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="25b0a-101">Remove-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="25b0a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="25b0a-102">SYNOPSIS</span></span>
<span data-ttu-id="25b0a-103">Usuwa bramę sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="25b0a-103">Deletes a Virtual Network Gateway</span></span>

## <span data-ttu-id="25b0a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="25b0a-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25b0a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="25b0a-105">DESCRIPTION</span></span>
<span data-ttu-id="25b0a-106">Brama sieci wirtualnej to obiekt reprezentujący bramę na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="25b0a-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="25b0a-107">Polecenie cmdlet **Get-AzVirtualNetworkGateway** zwraca obiekt bramy na platformie Azure na podstawie nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="25b0a-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="25b0a-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="25b0a-108">EXAMPLES</span></span>

### <span data-ttu-id="25b0a-109">Przykład 1: usuwanie bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="25b0a-109">Example 1: Delete a Virtual Network Gateway</span></span>
```powershell
Remove-AzVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="25b0a-110">Usuwa obiekt bramy sieci wirtualnej o nazwie "Moja brama" w grupie zasobów "myRG" Uwaga: musisz najpierw usunąć wszystkie połączenia z bramą sieci wirtualnej za pomocą polecenia cmdlet **Remove-AzVirtualNetworkGatewayConnection** .</span><span class="sxs-lookup"><span data-stu-id="25b0a-110">Deletes the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG" Note: You must first delete all connections to the Virtual Network Gateway using the **Remove-AzVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="25b0a-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="25b0a-111">PARAMETERS</span></span>

### <span data-ttu-id="25b0a-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="25b0a-112">-AsJob</span></span>
<span data-ttu-id="25b0a-113">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="25b0a-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="25b0a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25b0a-114">-DefaultProfile</span></span>
<span data-ttu-id="25b0a-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="25b0a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25b0a-116">-Force</span><span class="sxs-lookup"><span data-stu-id="25b0a-116">-Force</span></span>
<span data-ttu-id="25b0a-117">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="25b0a-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="25b0a-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="25b0a-118">-Name</span></span>
<span data-ttu-id="25b0a-119">Określa nazwę bramy sieci wirtualnej, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25b0a-119">Specifies the name of the virtual network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="25b0a-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25b0a-120">-PassThru</span></span>
<span data-ttu-id="25b0a-121">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="25b0a-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="25b0a-122">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="25b0a-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="25b0a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25b0a-123">-ResourceGroupName</span></span>
<span data-ttu-id="25b0a-124">Określa nazwę grupy zasobów zawierającej bramę sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="25b0a-124">Specifies the name of the resource group that contains the virtual network gateway.</span></span>

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

### <span data-ttu-id="25b0a-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="25b0a-125">-Confirm</span></span>
<span data-ttu-id="25b0a-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25b0a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25b0a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25b0a-127">-WhatIf</span></span>
<span data-ttu-id="25b0a-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25b0a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25b0a-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="25b0a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25b0a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25b0a-130">CommonParameters</span></span>
<span data-ttu-id="25b0a-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25b0a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25b0a-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25b0a-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25b0a-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="25b0a-133">INPUTS</span></span>

### <span data-ttu-id="25b0a-134">System. String</span><span class="sxs-lookup"><span data-stu-id="25b0a-134">System.String</span></span>

## <span data-ttu-id="25b0a-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="25b0a-135">OUTPUTS</span></span>

### <span data-ttu-id="25b0a-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="25b0a-136">System.Boolean</span></span>

## <span data-ttu-id="25b0a-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="25b0a-137">NOTES</span></span>

## <span data-ttu-id="25b0a-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="25b0a-138">RELATED LINKS</span></span>

[<span data-ttu-id="25b0a-139">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="25b0a-139">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="25b0a-140">Nowe — AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="25b0a-140">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="25b0a-141">Resetowanie — AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="25b0a-141">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="25b0a-142">Zmienianie rozmiaru — AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="25b0a-142">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="25b0a-143">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="25b0a-143">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
