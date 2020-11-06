---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2B15B224-E36C-454B-B6C2-F2BE032AE962
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: c52546ba0477a2911ac34533060d7a47df0b0698
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527818"
---
# <span data-ttu-id="a63d9-101">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a63d9-101">Remove-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="a63d9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a63d9-102">SYNOPSIS</span></span>
<span data-ttu-id="a63d9-103">Umożliwia usunięcie konfiguracji sondy z modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="a63d9-103">Removes a probe configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a63d9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a63d9-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a63d9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a63d9-105">DESCRIPTION</span></span>
<span data-ttu-id="a63d9-106">Polecenie cmdlet **Remove-AzureRmLoadBalancerProbeConfig** umożliwia usunięcie konfiguracji sondy z modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="a63d9-106">The **Remove-AzureRmLoadBalancerProbeConfig** cmdlet removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="a63d9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a63d9-107">EXAMPLES</span></span>

### <span data-ttu-id="a63d9-108">Przykład 1: Usuwanie konfiguracji sondy z modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="a63d9-108">Example 1: Remove a probe configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $loadbalancer
```

<span data-ttu-id="a63d9-109">Pierwsze polecenie uzyskuje usługę równoważenia obciążenia o nazwie MyLoadBalancer, a następnie zapisuje ją w zmiennej $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="a63d9-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="a63d9-110">Drugie polecenie usuwa konfigurację o nazwie Moja Sonda z modułu równoważenia obciążenia w $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="a63d9-110">The second command deletes the configuration named MyProbe from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="a63d9-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a63d9-111">PARAMETERS</span></span>

### <span data-ttu-id="a63d9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a63d9-112">-DefaultProfile</span></span>
<span data-ttu-id="a63d9-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a63d9-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a63d9-114">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="a63d9-114">-LoadBalancer</span></span>
<span data-ttu-id="a63d9-115">Umożliwia określenie modułu równoważenia obciążenia zawierającego konfigurację sondy, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a63d9-115">Specifies the load balancer that contains the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a63d9-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a63d9-116">-Name</span></span>
<span data-ttu-id="a63d9-117">Określa nazwę konfiguracji sondy, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a63d9-117">Specifies the name of the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a63d9-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a63d9-118">-Confirm</span></span>
<span data-ttu-id="a63d9-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a63d9-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a63d9-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a63d9-120">-WhatIf</span></span>
<span data-ttu-id="a63d9-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a63d9-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a63d9-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a63d9-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a63d9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a63d9-123">CommonParameters</span></span>
<span data-ttu-id="a63d9-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a63d9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a63d9-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a63d9-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a63d9-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a63d9-126">INPUTS</span></span>

### <span data-ttu-id="a63d9-127">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a63d9-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="a63d9-128">Parametry: moduł równoważenia obciążenia (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a63d9-128">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="a63d9-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a63d9-129">OUTPUTS</span></span>

### <span data-ttu-id="a63d9-130">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a63d9-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a63d9-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a63d9-131">NOTES</span></span>

## <span data-ttu-id="a63d9-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a63d9-132">RELATED LINKS</span></span>

[<span data-ttu-id="a63d9-133">Dodaj-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a63d9-133">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="a63d9-134">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a63d9-134">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="a63d9-135">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a63d9-135">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="a63d9-136">Nowe — AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a63d9-136">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="a63d9-137">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a63d9-137">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


