---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 75E30205-97AD-44E3-A61F-62B81ADB532C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermlocalnetworkgateway
schema: 2.0.0
ms.openlocfilehash: 7b3fde5feb5dae1ca064b8f5e31bbdfe03e12c7a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899087"
---
# <span data-ttu-id="b5306-101">Remove-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b5306-101">Remove-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="b5306-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b5306-102">SYNOPSIS</span></span>
<span data-ttu-id="b5306-103">Usuwa bramę sieci lokalnej</span><span class="sxs-lookup"><span data-stu-id="b5306-103">Deletes a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5306-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b5306-104">SYNTAX</span></span>

```
Remove-AzureRmLocalNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5306-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b5306-105">DESCRIPTION</span></span>
<span data-ttu-id="b5306-106">Lokalna Brama sieci to obiekt reprezentujący urządzenie VPN.</span><span class="sxs-lookup"><span data-stu-id="b5306-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="b5306-107">Polecenie cmdlet **Remove-AzureRmLocalNetworkGateway** usuwa obiekt reprezentujący bramę środowisku na podstawie nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b5306-107">The **Remove-AzureRmLocalNetworkGateway** cmdlet deletes the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="b5306-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b5306-108">EXAMPLES</span></span>

### <span data-ttu-id="b5306-109">1: usuwanie bramy sieci lokalnej</span><span class="sxs-lookup"><span data-stu-id="b5306-109">1: Delete a Local Network Gateway</span></span>
```
Remove-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="b5306-110">Usuwa obiekt bramy sieci lokalnej o nazwie "myLocalGW" w grupie zasobów "myRG".</span><span class="sxs-lookup"><span data-stu-id="b5306-110">Deletes the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG"</span></span>

<span data-ttu-id="b5306-111">Uwaga: musisz najpierw usunąć wszystkie połączenia z bramą sieci lokalnej przy użyciu polecenia cmdlet **Remove-AzureRmVirtualNetworkGatewayConnection** .</span><span class="sxs-lookup"><span data-stu-id="b5306-111">Note: You must first delete all connections to the Local Network Gateway using the **Remove-AzureRmVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="b5306-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b5306-112">PARAMETERS</span></span>

### <span data-ttu-id="b5306-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b5306-113">-AsJob</span></span>
<span data-ttu-id="b5306-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b5306-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5306-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5306-115">-DefaultProfile</span></span>
<span data-ttu-id="b5306-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b5306-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5306-117">-Force</span><span class="sxs-lookup"><span data-stu-id="b5306-117">-Force</span></span>
<span data-ttu-id="b5306-118">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="b5306-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5306-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b5306-119">-Name</span></span>
<span data-ttu-id="b5306-120">Określa nazwę bramy sieci lokalnej, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5306-120">Specifies the name of the local network gateway that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5306-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b5306-121">-PassThru</span></span>
<span data-ttu-id="b5306-122">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="b5306-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b5306-123">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="b5306-123">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5306-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5306-124">-ResourceGroupName</span></span>
<span data-ttu-id="b5306-125">Określa nazwę grupy zasobów zawierającej bramę sieci lokalnej.</span><span class="sxs-lookup"><span data-stu-id="b5306-125">Specifies the name of the resource group that contains the local network gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5306-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b5306-126">-Confirm</span></span>
<span data-ttu-id="b5306-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5306-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5306-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5306-128">-WhatIf</span></span>
<span data-ttu-id="b5306-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5306-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5306-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b5306-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5306-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5306-131">CommonParameters</span></span>
<span data-ttu-id="b5306-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5306-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5306-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5306-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5306-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b5306-134">INPUTS</span></span>

## <span data-ttu-id="b5306-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b5306-135">OUTPUTS</span></span>

## <span data-ttu-id="b5306-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b5306-136">NOTES</span></span>

## <span data-ttu-id="b5306-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b5306-137">RELATED LINKS</span></span>

[<span data-ttu-id="b5306-138">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b5306-138">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="b5306-139">Nowe — AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b5306-139">New-AzureRmLocalNetworkGateway</span></span>](./New-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="b5306-140">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b5306-140">Set-AzureRmLocalNetworkGateway</span></span>](./Set-AzureRmLocalNetworkGateway.md)


