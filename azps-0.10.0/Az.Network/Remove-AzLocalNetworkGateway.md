---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 75E30205-97AD-44E3-A61F-62B81ADB532C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLocalNetworkGateway.md
ms.openlocfilehash: 0589fa3f5dd806149c243557b547455af35178b2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890281"
---
# <span data-ttu-id="ed13c-101">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ed13c-101">Remove-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="ed13c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ed13c-102">SYNOPSIS</span></span>
<span data-ttu-id="ed13c-103">Usuwa bramę sieci lokalnej</span><span class="sxs-lookup"><span data-stu-id="ed13c-103">Deletes a Local Network Gateway</span></span>

## <span data-ttu-id="ed13c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ed13c-104">SYNTAX</span></span>

```
Remove-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed13c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ed13c-105">DESCRIPTION</span></span>
<span data-ttu-id="ed13c-106">Lokalna Brama sieci to obiekt reprezentujący urządzenie VPN.</span><span class="sxs-lookup"><span data-stu-id="ed13c-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="ed13c-107">Polecenie cmdlet **Remove-AzLocalNetworkGateway** usuwa obiekt reprezentujący bramę środowisku na podstawie nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ed13c-107">The **Remove-AzLocalNetworkGateway** cmdlet deletes the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="ed13c-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ed13c-108">EXAMPLES</span></span>

### <span data-ttu-id="ed13c-109">1: usuwanie bramy sieci lokalnej</span><span class="sxs-lookup"><span data-stu-id="ed13c-109">1: Delete a Local Network Gateway</span></span>
```
Remove-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="ed13c-110">Usuwa obiekt bramy sieci lokalnej o nazwie "myLocalGW" w grupie zasobów "myRG".</span><span class="sxs-lookup"><span data-stu-id="ed13c-110">Deletes the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG"</span></span>

<span data-ttu-id="ed13c-111">Uwaga: musisz najpierw usunąć wszystkie połączenia z bramą sieci lokalnej przy użyciu polecenia cmdlet **Remove-AzVirtualNetworkGatewayConnection** .</span><span class="sxs-lookup"><span data-stu-id="ed13c-111">Note: You must first delete all connections to the Local Network Gateway using the **Remove-AzVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="ed13c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ed13c-112">PARAMETERS</span></span>

### <span data-ttu-id="ed13c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ed13c-113">-AsJob</span></span>
<span data-ttu-id="ed13c-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="ed13c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ed13c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed13c-115">-DefaultProfile</span></span>
<span data-ttu-id="ed13c-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ed13c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed13c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ed13c-117">-Force</span></span>
<span data-ttu-id="ed13c-118">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="ed13c-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ed13c-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ed13c-119">-Name</span></span>
<span data-ttu-id="ed13c-120">Określa nazwę bramy sieci lokalnej, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed13c-120">Specifies the name of the local network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ed13c-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ed13c-121">-PassThru</span></span>
<span data-ttu-id="ed13c-122">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="ed13c-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ed13c-123">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="ed13c-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ed13c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed13c-124">-ResourceGroupName</span></span>
<span data-ttu-id="ed13c-125">Określa nazwę grupy zasobów zawierającej bramę sieci lokalnej.</span><span class="sxs-lookup"><span data-stu-id="ed13c-125">Specifies the name of the resource group that contains the local network gateway.</span></span>

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

### <span data-ttu-id="ed13c-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ed13c-126">-Confirm</span></span>
<span data-ttu-id="ed13c-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed13c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed13c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed13c-128">-WhatIf</span></span>
<span data-ttu-id="ed13c-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed13c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed13c-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ed13c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed13c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed13c-131">CommonParameters</span></span>
<span data-ttu-id="ed13c-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed13c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed13c-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed13c-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed13c-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ed13c-134">INPUTS</span></span>

## <span data-ttu-id="ed13c-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ed13c-135">OUTPUTS</span></span>

## <span data-ttu-id="ed13c-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ed13c-136">NOTES</span></span>

## <span data-ttu-id="ed13c-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ed13c-137">RELATED LINKS</span></span>

[<span data-ttu-id="ed13c-138">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ed13c-138">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="ed13c-139">Nowe — AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ed13c-139">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="ed13c-140">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ed13c-140">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)


