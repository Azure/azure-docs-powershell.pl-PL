---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 75E30205-97AD-44E3-A61F-62B81ADB532C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLocalNetworkGateway.md
ms.openlocfilehash: 3f09656caaccb103afa096ca0995489b3768e40e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871220"
---
# <span data-ttu-id="802a1-101">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="802a1-101">Remove-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="802a1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="802a1-102">SYNOPSIS</span></span>
<span data-ttu-id="802a1-103">Usuwa bramę sieci lokalnej</span><span class="sxs-lookup"><span data-stu-id="802a1-103">Deletes a Local Network Gateway</span></span>

## <span data-ttu-id="802a1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="802a1-104">SYNTAX</span></span>

```
Remove-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="802a1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="802a1-105">DESCRIPTION</span></span>
<span data-ttu-id="802a1-106">Lokalna Brama sieci to obiekt reprezentujący urządzenie VPN.</span><span class="sxs-lookup"><span data-stu-id="802a1-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="802a1-107">Polecenie cmdlet **Remove-AzLocalNetworkGateway** usuwa obiekt reprezentujący bramę środowisku na podstawie nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="802a1-107">The **Remove-AzLocalNetworkGateway** cmdlet deletes the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="802a1-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="802a1-108">EXAMPLES</span></span>

### <span data-ttu-id="802a1-109">1: usuwanie bramy sieci lokalnej</span><span class="sxs-lookup"><span data-stu-id="802a1-109">1: Delete a Local Network Gateway</span></span>
```
Remove-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="802a1-110">Usuwa obiekt bramy sieci lokalnej o nazwie "myLocalGW" w grupie zasobów "myRG" Uwaga: musisz najpierw usunąć wszystkie połączenia z bramą sieci lokalnej za pomocą polecenia cmdlet **Remove-AzVirtualNetworkGatewayConnection** .</span><span class="sxs-lookup"><span data-stu-id="802a1-110">Deletes the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" Note: You must first delete all connections to the Local Network Gateway using the **Remove-AzVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="802a1-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="802a1-111">PARAMETERS</span></span>

### <span data-ttu-id="802a1-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="802a1-112">-AsJob</span></span>
<span data-ttu-id="802a1-113">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="802a1-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="802a1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="802a1-114">-DefaultProfile</span></span>
<span data-ttu-id="802a1-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="802a1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="802a1-116">-Force</span><span class="sxs-lookup"><span data-stu-id="802a1-116">-Force</span></span>
<span data-ttu-id="802a1-117">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="802a1-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="802a1-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="802a1-118">-Name</span></span>
<span data-ttu-id="802a1-119">Określa nazwę bramy sieci lokalnej, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="802a1-119">Specifies the name of the local network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="802a1-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="802a1-120">-PassThru</span></span>
<span data-ttu-id="802a1-121">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="802a1-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="802a1-122">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="802a1-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="802a1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="802a1-123">-ResourceGroupName</span></span>
<span data-ttu-id="802a1-124">Określa nazwę grupy zasobów zawierającej bramę sieci lokalnej.</span><span class="sxs-lookup"><span data-stu-id="802a1-124">Specifies the name of the resource group that contains the local network gateway.</span></span>

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

### <span data-ttu-id="802a1-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="802a1-125">-Confirm</span></span>
<span data-ttu-id="802a1-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="802a1-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="802a1-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="802a1-127">-WhatIf</span></span>
<span data-ttu-id="802a1-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="802a1-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="802a1-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="802a1-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="802a1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="802a1-130">CommonParameters</span></span>
<span data-ttu-id="802a1-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="802a1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="802a1-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="802a1-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="802a1-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="802a1-133">INPUTS</span></span>

### <span data-ttu-id="802a1-134">System. String</span><span class="sxs-lookup"><span data-stu-id="802a1-134">System.String</span></span>

## <span data-ttu-id="802a1-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="802a1-135">OUTPUTS</span></span>

### <span data-ttu-id="802a1-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="802a1-136">System.Boolean</span></span>

## <span data-ttu-id="802a1-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="802a1-137">NOTES</span></span>

## <span data-ttu-id="802a1-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="802a1-138">RELATED LINKS</span></span>

[<span data-ttu-id="802a1-139">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="802a1-139">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="802a1-140">Nowe — AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="802a1-140">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="802a1-141">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="802a1-141">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
