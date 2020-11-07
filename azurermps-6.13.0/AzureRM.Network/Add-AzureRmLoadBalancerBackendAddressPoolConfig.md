---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9EB11283-0189-4333-8142-DCC3F770F91A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 0cc210563046a0ff8ee0554eb479e5eb822157fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718821"
---
# <span data-ttu-id="4d21e-101">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="4d21e-101">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="4d21e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4d21e-102">SYNOPSIS</span></span>
<span data-ttu-id="4d21e-103">Umożliwia dodanie konfiguracji puli adresów zaplecza do modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="4d21e-103">Adds a backend address pool configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d21e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4d21e-104">SYNTAX</span></span>

```
Add-AzureRmLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d21e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4d21e-105">DESCRIPTION</span></span>
<span data-ttu-id="4d21e-106">Polecenie cmdlet **Add-AzureRmLoadBalancerBackend** umożliwia dodanie puli adresów zaplecza do modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4d21e-106">The **Add-AzureRmLoadBalancerBackend** cmdlet adds a backend address pool to an Azure load balancer.</span></span>

## <span data-ttu-id="4d21e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4d21e-107">EXAMPLES</span></span>

### <span data-ttu-id="4d21e-108">Przykład 1 Dodawanie konfiguracji puli adresów zaplecza do modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="4d21e-108">Example 1 Add a backend address pool configuration to a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myrg" | Add-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzureRmLoadBalancer
```

<span data-ttu-id="4d21e-109">To polecenie uzyskuje usługę równoważenia obciążenia o nazwie MyLoadBalancer, dodaje pulę adresów zaplecza o nazwie BackendAddressPool02 do MyLoadBalancer, a następnie używa polecenia cmdlet **Set-AzureRmLoadBalancer** w celu zaktualizowania MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="4d21e-109">This command gets the load balancer named MyLoadBalancer, adds the backend address pool named BackendAddressPool02 to MyLoadBalancer, and then uses the **Set-AzureRmLoadBalancer** cmdlet to update MyLoadBalancer.</span></span>

## <span data-ttu-id="4d21e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4d21e-110">PARAMETERS</span></span>

### <span data-ttu-id="4d21e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d21e-111">-DefaultProfile</span></span>
<span data-ttu-id="4d21e-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4d21e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d21e-113">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="4d21e-113">-LoadBalancer</span></span>
<span data-ttu-id="4d21e-114">Określa obiekt **modułu równoważenia obciążenia** .</span><span class="sxs-lookup"><span data-stu-id="4d21e-114">Specifies a **LoadBalancer** object.</span></span>

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

### <span data-ttu-id="4d21e-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4d21e-115">-Name</span></span>
<span data-ttu-id="4d21e-116">Określa nazwę konfiguracji puli adresów zaplecza, która ma zostać dodana.</span><span class="sxs-lookup"><span data-stu-id="4d21e-116">Specifies the name of the backend address pool configuration to add.</span></span>

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

### <span data-ttu-id="4d21e-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4d21e-117">-Confirm</span></span>
<span data-ttu-id="4d21e-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d21e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d21e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d21e-119">-WhatIf</span></span>
<span data-ttu-id="4d21e-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d21e-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4d21e-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4d21e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d21e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d21e-122">CommonParameters</span></span>
<span data-ttu-id="4d21e-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d21e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d21e-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d21e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d21e-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4d21e-125">INPUTS</span></span>

### <span data-ttu-id="4d21e-126">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4d21e-126">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="4d21e-127">Parametry: moduł równoważenia obciążenia (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4d21e-127">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="4d21e-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4d21e-128">OUTPUTS</span></span>

### <span data-ttu-id="4d21e-129">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4d21e-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="4d21e-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4d21e-130">NOTES</span></span>

## <span data-ttu-id="4d21e-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4d21e-131">RELATED LINKS</span></span>

[<span data-ttu-id="4d21e-132">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4d21e-132">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="4d21e-133">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="4d21e-133">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="4d21e-134">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="4d21e-134">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="4d21e-135">Nowe — AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="4d21e-135">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="4d21e-136">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="4d21e-136">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md)


