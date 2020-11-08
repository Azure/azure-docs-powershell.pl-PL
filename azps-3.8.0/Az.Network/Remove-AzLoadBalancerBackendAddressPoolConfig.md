---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F965A9DE-645C-471B-84E8-58D648B1CA57
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 26f7e0dde825305e888d598a23af0b2fbaff81cd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053003"
---
# <span data-ttu-id="41887-101">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="41887-101">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="41887-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="41887-102">SYNOPSIS</span></span>
<span data-ttu-id="41887-103">Usuwa konfigurację puli adresów zaplecza z modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="41887-103">Removes a backend address pool configuration from a load balancer.</span></span>

## <span data-ttu-id="41887-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="41887-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41887-105">Opis</span><span class="sxs-lookup"><span data-stu-id="41887-105">DESCRIPTION</span></span>
<span data-ttu-id="41887-106">Polecenie cmdlet **Remove-AzLoadBalancerBackendAddressPoolConfig** usuwa pulę adresów zaplecza z modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="41887-106">The **Remove-AzLoadBalancerBackendAddressPoolConfig** cmdlet removes a backend address pool from a load balancer.</span></span>

## <span data-ttu-id="41887-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="41887-107">EXAMPLES</span></span>

### <span data-ttu-id="41887-108">Przykład 1: Usuwanie konfiguracji puli adresów zaplecza z modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="41887-108">Example 1: Remove a backend address pool configuration from a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" | Remove-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

<span data-ttu-id="41887-109">To polecenie uzyskuje moduł równoważenia obciążenia o nazwie MyLoadBalancer i przekazuje go do pozycji **Remove-AzLoadBalancerBackendAddressPoolConfig** , co powoduje usunięcie konfiguracji BackendAddressPool02 z MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="41887-109">This command gets the load balancer named MyLoadBalancer and passes it to **Remove-AzLoadBalancerBackendAddressPoolConfig** , which removes the BackendAddressPool02 configuration from MyLoadBalancer.</span></span>
<span data-ttu-id="41887-110">Na koniec Set-AzLoadBalancer polecenie cmdlet aktualizuje MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="41887-110">Finally, the Set-AzLoadBalancer cmdlet updates MyLoadBalancer.</span></span>
<span data-ttu-id="41887-111">Należy pamiętać, że konfiguracja puli adresów zaplecza musi istnieć, aby można było ją usunąć.</span><span class="sxs-lookup"><span data-stu-id="41887-111">Note that a backend address pool configuration must exist before you can delete it.</span></span>

## <span data-ttu-id="41887-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="41887-112">PARAMETERS</span></span>

### <span data-ttu-id="41887-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41887-113">-DefaultProfile</span></span>
<span data-ttu-id="41887-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="41887-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41887-115">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="41887-115">-LoadBalancer</span></span>
<span data-ttu-id="41887-116">Określa moduł równoważenia obciążenia zawierający pulę adresów zaplecza do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="41887-116">Specifies the load balancer that contains the backend address pool to remove.</span></span>

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

### <span data-ttu-id="41887-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="41887-117">-Name</span></span>
<span data-ttu-id="41887-118">Określa nazwę puli adresów zaplecza, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41887-118">Specifies the name of the backend address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="41887-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="41887-119">-Confirm</span></span>
<span data-ttu-id="41887-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41887-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41887-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41887-121">-WhatIf</span></span>
<span data-ttu-id="41887-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41887-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="41887-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="41887-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41887-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41887-124">CommonParameters</span></span>
<span data-ttu-id="41887-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41887-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41887-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41887-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41887-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="41887-127">INPUTS</span></span>

### <span data-ttu-id="41887-128">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="41887-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="41887-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="41887-129">OUTPUTS</span></span>

### <span data-ttu-id="41887-130">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="41887-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="41887-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="41887-131">NOTES</span></span>

## <span data-ttu-id="41887-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="41887-132">RELATED LINKS</span></span>

[<span data-ttu-id="41887-133">Dodaj-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="41887-133">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="41887-134">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="41887-134">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="41887-135">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="41887-135">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="41887-136">Nowe — AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="41887-136">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)


