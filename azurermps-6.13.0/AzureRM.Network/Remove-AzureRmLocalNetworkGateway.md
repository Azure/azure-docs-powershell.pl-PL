---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 75E30205-97AD-44E3-A61F-62B81ADB532C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: c09e812762867dc6aa89945f50d9658bb61bf5a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527813"
---
# <span data-ttu-id="13130-101">Remove-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="13130-101">Remove-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="13130-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="13130-102">SYNOPSIS</span></span>
<span data-ttu-id="13130-103">Usuwa bramę sieci lokalnej</span><span class="sxs-lookup"><span data-stu-id="13130-103">Deletes a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13130-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="13130-104">SYNTAX</span></span>

```
Remove-AzureRmLocalNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13130-105">Opis</span><span class="sxs-lookup"><span data-stu-id="13130-105">DESCRIPTION</span></span>
<span data-ttu-id="13130-106">Lokalna Brama sieci to obiekt reprezentujący urządzenie VPN.</span><span class="sxs-lookup"><span data-stu-id="13130-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="13130-107">Polecenie cmdlet **Remove-AzureRmLocalNetworkGateway** usuwa obiekt reprezentujący bramę środowisku na podstawie nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="13130-107">The **Remove-AzureRmLocalNetworkGateway** cmdlet deletes the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="13130-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="13130-108">EXAMPLES</span></span>

### <span data-ttu-id="13130-109">1: usuwanie bramy sieci lokalnej</span><span class="sxs-lookup"><span data-stu-id="13130-109">1: Delete a Local Network Gateway</span></span>
```
Remove-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="13130-110">Usuwa obiekt bramy sieci lokalnej o nazwie "myLocalGW" w grupie zasobów "myRG" Uwaga: musisz najpierw usunąć wszystkie połączenia z bramą sieci lokalnej za pomocą polecenia cmdlet **Remove-AzureRmVirtualNetworkGatewayConnection** .</span><span class="sxs-lookup"><span data-stu-id="13130-110">Deletes the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" Note: You must first delete all connections to the Local Network Gateway using the **Remove-AzureRmVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="13130-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="13130-111">PARAMETERS</span></span>

### <span data-ttu-id="13130-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="13130-112">-AsJob</span></span>
<span data-ttu-id="13130-113">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="13130-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="13130-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13130-114">-DefaultProfile</span></span>
<span data-ttu-id="13130-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="13130-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13130-116">-Force</span><span class="sxs-lookup"><span data-stu-id="13130-116">-Force</span></span>
<span data-ttu-id="13130-117">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="13130-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="13130-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="13130-118">-Name</span></span>
<span data-ttu-id="13130-119">Określa nazwę bramy sieci lokalnej, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13130-119">Specifies the name of the local network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="13130-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="13130-120">-PassThru</span></span>
<span data-ttu-id="13130-121">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="13130-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="13130-122">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="13130-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="13130-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13130-123">-ResourceGroupName</span></span>
<span data-ttu-id="13130-124">Określa nazwę grupy zasobów zawierającej bramę sieci lokalnej.</span><span class="sxs-lookup"><span data-stu-id="13130-124">Specifies the name of the resource group that contains the local network gateway.</span></span>

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

### <span data-ttu-id="13130-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="13130-125">-Confirm</span></span>
<span data-ttu-id="13130-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13130-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13130-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13130-127">-WhatIf</span></span>
<span data-ttu-id="13130-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13130-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13130-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="13130-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13130-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13130-130">CommonParameters</span></span>
<span data-ttu-id="13130-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13130-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13130-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13130-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13130-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13130-133">INPUTS</span></span>

### <span data-ttu-id="13130-134">System. String</span><span class="sxs-lookup"><span data-stu-id="13130-134">System.String</span></span>

## <span data-ttu-id="13130-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="13130-135">OUTPUTS</span></span>

### <span data-ttu-id="13130-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="13130-136">System.Boolean</span></span>

## <span data-ttu-id="13130-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="13130-137">NOTES</span></span>

## <span data-ttu-id="13130-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="13130-138">RELATED LINKS</span></span>

[<span data-ttu-id="13130-139">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="13130-139">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="13130-140">Nowe — AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="13130-140">New-AzureRmLocalNetworkGateway</span></span>](./New-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="13130-141">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="13130-141">Set-AzureRmLocalNetworkGateway</span></span>](./Set-AzureRmLocalNetworkGateway.md)


