---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9EB11283-0189-4333-8142-DCC3F770F91A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 9e353eb6682e4985ff278ddc8c0207bf0f1ab45b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709680"
---
# <span data-ttu-id="f653f-101">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f653f-101">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="f653f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f653f-102">SYNOPSIS</span></span>
<span data-ttu-id="f653f-103">Umożliwia dodanie konfiguracji puli adresów zaplecza do modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="f653f-103">Adds a backend address pool configuration to a load balancer.</span></span>

## <span data-ttu-id="f653f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f653f-104">SYNTAX</span></span>

```
Add-AzLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f653f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f653f-105">DESCRIPTION</span></span>
<span data-ttu-id="f653f-106">Polecenie cmdlet **Add-AzLoadBalancerBackend** umożliwia dodanie puli adresów zaplecza do modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f653f-106">The **Add-AzLoadBalancerBackend** cmdlet adds a backend address pool to an Azure load balancer.</span></span>

## <span data-ttu-id="f653f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f653f-107">EXAMPLES</span></span>

### <span data-ttu-id="f653f-108">Przykład 1 Dodawanie konfiguracji puli adresów zaplecza do modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="f653f-108">Example 1 Add a backend address pool configuration to a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myrg" | Add-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

<span data-ttu-id="f653f-109">To polecenie uzyskuje usługę równoważenia obciążenia o nazwie MyLoadBalancer, dodaje pulę adresów zaplecza o nazwie BackendAddressPool02 do MyLoadBalancer, a następnie używa polecenia cmdlet **Set-AzLoadBalancer** w celu zaktualizowania MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="f653f-109">This command gets the load balancer named MyLoadBalancer, adds the backend address pool named BackendAddressPool02 to MyLoadBalancer, and then uses the **Set-AzLoadBalancer** cmdlet to update MyLoadBalancer.</span></span>

## <span data-ttu-id="f653f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f653f-110">PARAMETERS</span></span>

### <span data-ttu-id="f653f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f653f-111">-DefaultProfile</span></span>
<span data-ttu-id="f653f-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f653f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f653f-113">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="f653f-113">-LoadBalancer</span></span>
<span data-ttu-id="f653f-114">Określa obiekt **modułu równoważenia obciążenia** .</span><span class="sxs-lookup"><span data-stu-id="f653f-114">Specifies a **LoadBalancer** object.</span></span>

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

### <span data-ttu-id="f653f-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f653f-115">-Name</span></span>
<span data-ttu-id="f653f-116">Określa nazwę konfiguracji puli adresów zaplecza, która ma zostać dodana.</span><span class="sxs-lookup"><span data-stu-id="f653f-116">Specifies the name of the backend address pool configuration to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f653f-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f653f-117">-Confirm</span></span>
<span data-ttu-id="f653f-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f653f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f653f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f653f-119">-WhatIf</span></span>
<span data-ttu-id="f653f-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f653f-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f653f-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f653f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f653f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f653f-122">CommonParameters</span></span>
<span data-ttu-id="f653f-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f653f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f653f-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f653f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f653f-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f653f-125">INPUTS</span></span>

### <span data-ttu-id="f653f-126">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f653f-126">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f653f-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f653f-127">OUTPUTS</span></span>

### <span data-ttu-id="f653f-128">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f653f-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f653f-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f653f-129">NOTES</span></span>

## <span data-ttu-id="f653f-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f653f-130">RELATED LINKS</span></span>

[<span data-ttu-id="f653f-131">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f653f-131">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="f653f-132">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f653f-132">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="f653f-133">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f653f-133">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="f653f-134">Nowe — AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f653f-134">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="f653f-135">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f653f-135">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


