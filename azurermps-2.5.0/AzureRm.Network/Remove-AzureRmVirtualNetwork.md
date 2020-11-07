---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C48E204D-D7EC-4EFD-ADC5-C6F593313B9B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetwork
schema: 2.0.0
ms.openlocfilehash: 89f0be5dbb0ba6b4e24e76be1eb75c375f0ebcd5
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897870"
---
# <span data-ttu-id="d7e6c-101">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d7e6c-101">Remove-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="d7e6c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d7e6c-102">SYNOPSIS</span></span>
<span data-ttu-id="d7e6c-103">Usuwa sieć wirtualną.</span><span class="sxs-lookup"><span data-stu-id="d7e6c-103">Removes a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7e6c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d7e6c-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetwork -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7e6c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d7e6c-105">DESCRIPTION</span></span>
<span data-ttu-id="d7e6c-106">Polecenie cmdlet **Remove-AzureRmVirtualNetwork** usuwa sieć wirtualną Azure.</span><span class="sxs-lookup"><span data-stu-id="d7e6c-106">The **Remove-AzureRmVirtualNetwork** cmdlet removes an Azure virtual network.</span></span>

## <span data-ttu-id="d7e6c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d7e6c-107">EXAMPLES</span></span>

### <span data-ttu-id="d7e6c-108">1: Tworzenie i usuwanie sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="d7e6c-108">1: Create and delete a virtual network</span></span>
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

<span data-ttu-id="d7e6c-109">W tym przykładzie przedstawiono tworzenie sieci wirtualnej w grupie zasobów, a następnie natychmiastowe jej usunięcie.</span><span class="sxs-lookup"><span data-stu-id="d7e6c-109">This example creates a virtual network in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="d7e6c-110">Aby zapobiec wyświetlaniu monitu podczas usuwania sieci wirtualnej, Użyj flagi-Force.</span><span class="sxs-lookup"><span data-stu-id="d7e6c-110">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="d7e6c-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d7e6c-111">PARAMETERS</span></span>

### <span data-ttu-id="d7e6c-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d7e6c-112">-AsJob</span></span>
<span data-ttu-id="d7e6c-113">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d7e6c-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d7e6c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7e6c-114">-DefaultProfile</span></span>
<span data-ttu-id="d7e6c-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d7e6c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7e6c-116">-Force</span><span class="sxs-lookup"><span data-stu-id="d7e6c-116">-Force</span></span>
<span data-ttu-id="d7e6c-117">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="d7e6c-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d7e6c-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d7e6c-118">-Name</span></span>
<span data-ttu-id="d7e6c-119">Określa nazwę sieci wirtualnej, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7e6c-119">Specifies the name of the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d7e6c-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d7e6c-120">-PassThru</span></span>
<span data-ttu-id="d7e6c-121">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="d7e6c-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d7e6c-122">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="d7e6c-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d7e6c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7e6c-123">-ResourceGroupName</span></span>
<span data-ttu-id="d7e6c-124">Określa nazwę grupy zasobów zawierającej sieć wirtualną, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7e6c-124">Specifies the name of the resource group that contains the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d7e6c-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d7e6c-125">-Confirm</span></span>
<span data-ttu-id="d7e6c-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7e6c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7e6c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7e6c-127">-WhatIf</span></span>
<span data-ttu-id="d7e6c-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7e6c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7e6c-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d7e6c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7e6c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7e6c-130">CommonParameters</span></span>
<span data-ttu-id="d7e6c-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7e6c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7e6c-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7e6c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7e6c-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d7e6c-133">INPUTS</span></span>

## <span data-ttu-id="d7e6c-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d7e6c-134">OUTPUTS</span></span>

## <span data-ttu-id="d7e6c-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d7e6c-135">NOTES</span></span>

## <span data-ttu-id="d7e6c-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d7e6c-136">RELATED LINKS</span></span>

[<span data-ttu-id="d7e6c-137">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d7e6c-137">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="d7e6c-138">Nowe — AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d7e6c-138">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="d7e6c-139">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d7e6c-139">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)


