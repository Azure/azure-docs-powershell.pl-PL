---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F965A9DE-645C-471B-84E8-58D648B1CA57
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 065aa3718f1a66949265e7dca39880c1eff21fa0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716940"
---
# <span data-ttu-id="9b786-101">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="9b786-101">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="9b786-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9b786-102">SYNOPSIS</span></span>
<span data-ttu-id="9b786-103">Usuwa konfigurację puli adresów zaplecza z modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="9b786-103">Removes a backend address pool configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b786-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9b786-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b786-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9b786-105">DESCRIPTION</span></span>
<span data-ttu-id="9b786-106">Polecenie cmdlet **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** usuwa pulę adresów zaplecza z modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="9b786-106">The **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** cmdlet removes a backend address pool from a load balancer.</span></span>

## <span data-ttu-id="9b786-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9b786-107">EXAMPLES</span></span>

### <span data-ttu-id="9b786-108">Przykład 1: Usuwanie konfiguracji puli adresów zaplecza z modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="9b786-108">Example 1: Remove a backend address pool configuration from a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" | Remove-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzureRmLoadBalancer
```

<span data-ttu-id="9b786-109">To polecenie uzyskuje moduł równoważenia obciążenia o nazwie MyLoadBalancer i przekazuje go do pozycji **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** , co powoduje usunięcie konfiguracji BackendAddressPool02 z MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="9b786-109">This command gets the load balancer named MyLoadBalancer and passes it to **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** , which removes the BackendAddressPool02 configuration from MyLoadBalancer.</span></span>
<span data-ttu-id="9b786-110">Na koniec Set-AzureRmLoadBalancer polecenie cmdlet aktualizuje MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="9b786-110">Finally, the Set-AzureRmLoadBalancer cmdlet updates MyLoadBalancer.</span></span>
<span data-ttu-id="9b786-111">Należy pamiętać, że konfiguracja puli adresów zaplecza musi istnieć, aby można było ją usunąć.</span><span class="sxs-lookup"><span data-stu-id="9b786-111">Note that a backend address pool configuration must exist before you can delete it.</span></span>

## <span data-ttu-id="9b786-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9b786-112">PARAMETERS</span></span>

### <span data-ttu-id="9b786-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b786-113">-DefaultProfile</span></span>
<span data-ttu-id="9b786-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9b786-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b786-115">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="9b786-115">-LoadBalancer</span></span>
<span data-ttu-id="9b786-116">Określa moduł równoważenia obciążenia zawierający pulę adresów zaplecza do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="9b786-116">Specifies the load balancer that contains the backend address pool to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b786-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9b786-117">-Name</span></span>
<span data-ttu-id="9b786-118">Określa nazwę puli adresów zaplecza, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b786-118">Specifies the name of the backend address pool that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b786-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9b786-119">-Confirm</span></span>
<span data-ttu-id="9b786-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b786-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b786-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b786-121">-WhatIf</span></span>
<span data-ttu-id="9b786-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b786-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9b786-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9b786-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b786-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b786-124">CommonParameters</span></span>
<span data-ttu-id="9b786-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b786-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b786-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b786-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b786-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9b786-127">INPUTS</span></span>

### <span data-ttu-id="9b786-128">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9b786-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="9b786-129">Parametry: moduł równoważenia obciążenia (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9b786-129">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="9b786-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9b786-130">OUTPUTS</span></span>

### <span data-ttu-id="9b786-131">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9b786-131">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="9b786-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9b786-132">NOTES</span></span>

## <span data-ttu-id="9b786-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9b786-133">RELATED LINKS</span></span>

[<span data-ttu-id="9b786-134">Dodaj-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="9b786-134">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="9b786-135">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9b786-135">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="9b786-136">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="9b786-136">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="9b786-137">Nowe — AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="9b786-137">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzureRmLoadBalancerBackendAddressPoolConfig.md)


