---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A35BB728-A7EF-4ADF-B1A9-25A156434E99
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 533eb9482c2e872c0b41552a5c59842a07fa0216
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719166"
---
# <span data-ttu-id="b1ce4-101">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b1ce4-101">Remove-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="b1ce4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b1ce4-102">SYNOPSIS</span></span>
<span data-ttu-id="b1ce4-103">Usuwa bramę sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="b1ce4-103">Deletes a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1ce4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b1ce4-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1ce4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b1ce4-105">DESCRIPTION</span></span>
<span data-ttu-id="b1ce4-106">Brama sieci wirtualnej to obiekt reprezentujący bramę na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="b1ce4-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="b1ce4-107">Polecenie cmdlet **Get-AzureRmVirtualNetworkGateway** zwraca obiekt bramy na platformie Azure na podstawie nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b1ce4-107">The **Get-AzureRmVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="b1ce4-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b1ce4-108">EXAMPLES</span></span>

### <span data-ttu-id="b1ce4-109">1: usuwanie bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="b1ce4-109">1: Delete a Virtual Network Gateway</span></span>
```
Remove-AzureRmVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="b1ce4-110">Usuwa obiekt bramy sieci wirtualnej o nazwie "Moja brama" w grupie zasobów "myRG".</span><span class="sxs-lookup"><span data-stu-id="b1ce4-110">Deletes the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

<span data-ttu-id="b1ce4-111">Uwaga: musisz najpierw usunąć wszystkie połączenia z bramą sieci wirtualnej za pomocą polecenia cmdlet **Remove-AzureRmVirtualNetworkGatewayConnection** .</span><span class="sxs-lookup"><span data-stu-id="b1ce4-111">Note: You must first delete all connections to the Virtual Network Gateway using the **Remove-AzureRmVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="b1ce4-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b1ce4-112">PARAMETERS</span></span>

### <span data-ttu-id="b1ce4-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b1ce4-113">-AsJob</span></span>
<span data-ttu-id="b1ce4-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b1ce4-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b1ce4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1ce4-115">-DefaultProfile</span></span>
<span data-ttu-id="b1ce4-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b1ce4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1ce4-117">-Force</span><span class="sxs-lookup"><span data-stu-id="b1ce4-117">-Force</span></span>
<span data-ttu-id="b1ce4-118">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="b1ce4-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b1ce4-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b1ce4-119">-Name</span></span>
<span data-ttu-id="b1ce4-120">Określa nazwę bramy sieci wirtualnej, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1ce4-120">Specifies the name of the virtual network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b1ce4-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b1ce4-121">-PassThru</span></span>
<span data-ttu-id="b1ce4-122">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="b1ce4-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b1ce4-123">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="b1ce4-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b1ce4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1ce4-124">-ResourceGroupName</span></span>
<span data-ttu-id="b1ce4-125">Określa nazwę grupy zasobów zawierającej bramę sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b1ce4-125">Specifies the name of the resource group that contains the virtual network gateway.</span></span>

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

### <span data-ttu-id="b1ce4-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b1ce4-126">-Confirm</span></span>
<span data-ttu-id="b1ce4-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1ce4-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1ce4-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1ce4-128">-WhatIf</span></span>
<span data-ttu-id="b1ce4-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1ce4-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1ce4-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b1ce4-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1ce4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1ce4-131">CommonParameters</span></span>
<span data-ttu-id="b1ce4-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1ce4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1ce4-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1ce4-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1ce4-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b1ce4-134">INPUTS</span></span>

### <span data-ttu-id="b1ce4-135">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b1ce4-135">None</span></span>
<span data-ttu-id="b1ce4-136">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="b1ce4-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b1ce4-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b1ce4-137">OUTPUTS</span></span>

## <span data-ttu-id="b1ce4-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b1ce4-138">NOTES</span></span>

## <span data-ttu-id="b1ce4-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b1ce4-139">RELATED LINKS</span></span>

