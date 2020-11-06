---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A35BB728-A7EF-4ADF-B1A9-25A156434E99
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 65e4259b7b530c7ea003860ab30c9f0c0baa7250
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552648"
---
# <span data-ttu-id="b6594-101">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b6594-101">Remove-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="b6594-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b6594-102">SYNOPSIS</span></span>
<span data-ttu-id="b6594-103">Usuwa bramę sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="b6594-103">Deletes a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6594-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b6594-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6594-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b6594-105">DESCRIPTION</span></span>
<span data-ttu-id="b6594-106">Brama sieci wirtualnej to obiekt reprezentujący bramę na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="b6594-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="b6594-107">Polecenie cmdlet **Get-AzureRmVirtualNetworkGateway** zwraca obiekt bramy na platformie Azure na podstawie nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b6594-107">The **Get-AzureRmVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="b6594-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b6594-108">EXAMPLES</span></span>

### <span data-ttu-id="b6594-109">1: usuwanie bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="b6594-109">1: Delete a Virtual Network Gateway</span></span>
```
Remove-AzureRmVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="b6594-110">Usuwa obiekt bramy sieci wirtualnej o nazwie "Moja brama" w grupie zasobów "myRG" Uwaga: musisz najpierw usunąć wszystkie połączenia z bramą sieci wirtualnej za pomocą polecenia cmdlet **Remove-AzureRmVirtualNetworkGatewayConnection** .</span><span class="sxs-lookup"><span data-stu-id="b6594-110">Deletes the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG" Note: You must first delete all connections to the Virtual Network Gateway using the **Remove-AzureRmVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="b6594-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b6594-111">PARAMETERS</span></span>

### <span data-ttu-id="b6594-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b6594-112">-AsJob</span></span>
<span data-ttu-id="b6594-113">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b6594-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b6594-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6594-114">-DefaultProfile</span></span>
<span data-ttu-id="b6594-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b6594-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6594-116">-Force</span><span class="sxs-lookup"><span data-stu-id="b6594-116">-Force</span></span>
<span data-ttu-id="b6594-117">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="b6594-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b6594-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b6594-118">-Name</span></span>
<span data-ttu-id="b6594-119">Określa nazwę bramy sieci wirtualnej, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6594-119">Specifies the name of the virtual network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b6594-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b6594-120">-PassThru</span></span>
<span data-ttu-id="b6594-121">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="b6594-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b6594-122">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="b6594-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b6594-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6594-123">-ResourceGroupName</span></span>
<span data-ttu-id="b6594-124">Określa nazwę grupy zasobów zawierającej bramę sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b6594-124">Specifies the name of the resource group that contains the virtual network gateway.</span></span>

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

### <span data-ttu-id="b6594-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b6594-125">-Confirm</span></span>
<span data-ttu-id="b6594-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6594-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6594-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6594-127">-WhatIf</span></span>
<span data-ttu-id="b6594-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6594-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6594-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b6594-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6594-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6594-130">CommonParameters</span></span>
<span data-ttu-id="b6594-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6594-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6594-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6594-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6594-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b6594-133">INPUTS</span></span>

### <span data-ttu-id="b6594-134">System. String</span><span class="sxs-lookup"><span data-stu-id="b6594-134">System.String</span></span>

## <span data-ttu-id="b6594-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b6594-135">OUTPUTS</span></span>

### <span data-ttu-id="b6594-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b6594-136">System.Boolean</span></span>

## <span data-ttu-id="b6594-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b6594-137">NOTES</span></span>

## <span data-ttu-id="b6594-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b6594-138">RELATED LINKS</span></span>
