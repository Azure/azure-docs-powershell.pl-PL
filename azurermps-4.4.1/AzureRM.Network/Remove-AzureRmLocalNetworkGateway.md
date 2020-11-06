---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 75E30205-97AD-44E3-A61F-62B81ADB532C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: ddc269ecd6f5cb4d1a1d377f656d47b0d18c6c00
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525502"
---
# <span data-ttu-id="6acfe-101">Remove-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6acfe-101">Remove-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="6acfe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6acfe-102">SYNOPSIS</span></span>
<span data-ttu-id="6acfe-103">Usuwa bramę sieci lokalnej</span><span class="sxs-lookup"><span data-stu-id="6acfe-103">Deletes a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6acfe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6acfe-104">SYNTAX</span></span>

```
Remove-AzureRmLocalNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6acfe-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6acfe-105">DESCRIPTION</span></span>
<span data-ttu-id="6acfe-106">Lokalna Brama sieci to obiekt reprezentujący urządzenie VPN.</span><span class="sxs-lookup"><span data-stu-id="6acfe-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="6acfe-107">Polecenie cmdlet **Remove-AzureRmLocalNetworkGateway** usuwa obiekt reprezentujący bramę środowisku na podstawie nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6acfe-107">The **Remove-AzureRmLocalNetworkGateway** cmdlet deletes the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="6acfe-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6acfe-108">EXAMPLES</span></span>

### <span data-ttu-id="6acfe-109">1: usuwanie bramy sieci lokalnej</span><span class="sxs-lookup"><span data-stu-id="6acfe-109">1: Delete a Local Network Gateway</span></span>
```
Remove-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="6acfe-110">Usuwa obiekt bramy sieci lokalnej o nazwie "myLocalGW" w grupie zasobów "myRG".</span><span class="sxs-lookup"><span data-stu-id="6acfe-110">Deletes the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG"</span></span>

<span data-ttu-id="6acfe-111">Uwaga: musisz najpierw usunąć wszystkie połączenia z bramą sieci lokalnej przy użyciu polecenia cmdlet **Remove-AzureRmVirtualNetworkGatewayConnection** .</span><span class="sxs-lookup"><span data-stu-id="6acfe-111">Note: You must first delete all connections to the Local Network Gateway using the **Remove-AzureRmVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="6acfe-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6acfe-112">PARAMETERS</span></span>

### <span data-ttu-id="6acfe-113">-Force</span><span class="sxs-lookup"><span data-stu-id="6acfe-113">-Force</span></span>
<span data-ttu-id="6acfe-114">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="6acfe-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6acfe-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6acfe-115">-Name</span></span>
<span data-ttu-id="6acfe-116">Określa nazwę bramy sieci lokalnej, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6acfe-116">Specifies the name of the local network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6acfe-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6acfe-117">-PassThru</span></span>
<span data-ttu-id="6acfe-118">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="6acfe-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6acfe-119">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="6acfe-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6acfe-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6acfe-120">-ResourceGroupName</span></span>
<span data-ttu-id="6acfe-121">Określa nazwę grupy zasobów zawierającej bramę sieci lokalnej.</span><span class="sxs-lookup"><span data-stu-id="6acfe-121">Specifies the name of the resource group that contains the local network gateway.</span></span>

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

### <span data-ttu-id="6acfe-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6acfe-122">-Confirm</span></span>
<span data-ttu-id="6acfe-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6acfe-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6acfe-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6acfe-124">-WhatIf</span></span>
<span data-ttu-id="6acfe-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6acfe-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6acfe-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6acfe-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6acfe-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6acfe-127">-DefaultProfile</span></span>
<span data-ttu-id="6acfe-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6acfe-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6acfe-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6acfe-129">CommonParameters</span></span>
<span data-ttu-id="6acfe-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6acfe-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6acfe-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6acfe-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6acfe-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6acfe-132">INPUTS</span></span>

## <span data-ttu-id="6acfe-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6acfe-133">OUTPUTS</span></span>

## <span data-ttu-id="6acfe-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6acfe-134">NOTES</span></span>

## <span data-ttu-id="6acfe-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6acfe-135">RELATED LINKS</span></span>

[<span data-ttu-id="6acfe-136">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6acfe-136">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="6acfe-137">Nowe — AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6acfe-137">New-AzureRmLocalNetworkGateway</span></span>](./New-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="6acfe-138">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6acfe-138">Set-AzureRmLocalNetworkGateway</span></span>](./Set-AzureRmLocalNetworkGateway.md)


