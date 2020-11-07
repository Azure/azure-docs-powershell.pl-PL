---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C48E204D-D7EC-4EFD-ADC5-C6F593313B9B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetwork.md
ms.openlocfilehash: 945f1d8d12b4a493ca361c04ae14cd899f91956f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719167"
---
# <span data-ttu-id="c8317-101">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c8317-101">Remove-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="c8317-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c8317-102">SYNOPSIS</span></span>
<span data-ttu-id="c8317-103">Usuwa sieć wirtualną.</span><span class="sxs-lookup"><span data-stu-id="c8317-103">Removes a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8317-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c8317-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetwork -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8317-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c8317-105">DESCRIPTION</span></span>
<span data-ttu-id="c8317-106">Polecenie cmdlet **Remove-AzureRmVirtualNetwork** usuwa sieć wirtualną Azure.</span><span class="sxs-lookup"><span data-stu-id="c8317-106">The **Remove-AzureRmVirtualNetwork** cmdlet removes an Azure virtual network.</span></span>

## <span data-ttu-id="c8317-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c8317-107">EXAMPLES</span></span>

### <span data-ttu-id="c8317-108">1: Tworzenie i usuwanie sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="c8317-108">1: Create and delete a virtual network</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix 
    "10.0.2.0/24"

New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
    
Remove-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="c8317-109">W tym przykładzie przedstawiono tworzenie sieci wirtualnej w grupie zasobów, a następnie natychmiastowe jej usunięcie.</span><span class="sxs-lookup"><span data-stu-id="c8317-109">This example creates a virtual network in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="c8317-110">Aby zapobiec wyświetlaniu monitu podczas usuwania sieci wirtualnej, Użyj flagi-Force.</span><span class="sxs-lookup"><span data-stu-id="c8317-110">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="c8317-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c8317-111">PARAMETERS</span></span>

### <span data-ttu-id="c8317-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c8317-112">-AsJob</span></span>
<span data-ttu-id="c8317-113">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="c8317-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c8317-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8317-114">-DefaultProfile</span></span>
<span data-ttu-id="c8317-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c8317-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8317-116">-Force</span><span class="sxs-lookup"><span data-stu-id="c8317-116">-Force</span></span>
<span data-ttu-id="c8317-117">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="c8317-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c8317-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c8317-118">-Name</span></span>
<span data-ttu-id="c8317-119">Określa nazwę sieci wirtualnej, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8317-119">Specifies the name of the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c8317-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c8317-120">-PassThru</span></span>
<span data-ttu-id="c8317-121">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="c8317-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c8317-122">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="c8317-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c8317-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8317-123">-ResourceGroupName</span></span>
<span data-ttu-id="c8317-124">Określa nazwę grupy zasobów zawierającej sieć wirtualną, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8317-124">Specifies the name of the resource group that contains the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c8317-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c8317-125">-Confirm</span></span>
<span data-ttu-id="c8317-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8317-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8317-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8317-127">-WhatIf</span></span>
<span data-ttu-id="c8317-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8317-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8317-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c8317-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8317-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8317-130">CommonParameters</span></span>
<span data-ttu-id="c8317-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8317-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8317-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8317-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8317-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c8317-133">INPUTS</span></span>

### <span data-ttu-id="c8317-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="c8317-134">None</span></span>
<span data-ttu-id="c8317-135">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="c8317-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c8317-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c8317-136">OUTPUTS</span></span>

## <span data-ttu-id="c8317-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c8317-137">NOTES</span></span>

## <span data-ttu-id="c8317-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c8317-138">RELATED LINKS</span></span>

[<span data-ttu-id="c8317-139">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c8317-139">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="c8317-140">Nowe — AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c8317-140">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="c8317-141">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c8317-141">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)


