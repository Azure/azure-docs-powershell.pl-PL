---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5F8E11DF-D560-44D7-99CA-C425951A56D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: bde16a6f3ecd68307574ae5eac7760a177101cc1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053004"
---
# <span data-ttu-id="21347-101">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="21347-101">Remove-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="21347-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="21347-102">SYNOPSIS</span></span>
<span data-ttu-id="21347-103">Usuwa konfigurację frontonu IP z modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="21347-103">Removes a front-end IP configuration from a load balancer.</span></span>

## <span data-ttu-id="21347-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="21347-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21347-105">Opis</span><span class="sxs-lookup"><span data-stu-id="21347-105">DESCRIPTION</span></span>
<span data-ttu-id="21347-106">Polecenie cmdlet **Remove-AzLoadBalancerFrontendIpConfig** usuwa konfigurację adresu IP frontonu z modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="21347-106">The **Remove-AzLoadBalancerFrontendIpConfig** cmdlet removes a front-end IP configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="21347-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="21347-107">EXAMPLES</span></span>

### <span data-ttu-id="21347-108">Przykład 1: Usuwanie konfiguracji frontonu IP z modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="21347-108">Example 1: Remove a front-end IP configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerFrontendIpConfig -Name "frontendName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="21347-109">Pierwsze polecenie uzyskuje moduł równoważenia obciążenia skojarzony z konfiguracją frontonu IP, którą chcesz usunąć, a następnie zapisze ją w zmiennej $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="21347-109">The first command gets the load balancer that is associated with the front-end IP configuration you want to remove, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="21347-110">Drugie polecenie usuwa skojarzoną konfigurację adresu IP frontonu z modułu równoważenia obciążenia w $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="21347-110">The second command removes the associated frontend IP configuration from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="21347-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="21347-111">PARAMETERS</span></span>

### <span data-ttu-id="21347-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21347-112">-DefaultProfile</span></span>
<span data-ttu-id="21347-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="21347-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21347-114">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="21347-114">-LoadBalancer</span></span>
<span data-ttu-id="21347-115">Określa moduł równoważenia obciążenia zawierający konfigurację frontonu IP do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="21347-115">Specifies the load balancer that contains the front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="21347-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="21347-116">-Name</span></span>
<span data-ttu-id="21347-117">Określa nazwę konfiguracji frontonu adresu IP do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="21347-117">Specifies the name of the front-end IP address configuration to remove.</span></span>

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

### <span data-ttu-id="21347-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="21347-118">-Confirm</span></span>
<span data-ttu-id="21347-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21347-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21347-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21347-120">-WhatIf</span></span>
<span data-ttu-id="21347-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21347-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="21347-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="21347-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21347-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21347-123">CommonParameters</span></span>
<span data-ttu-id="21347-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21347-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21347-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21347-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21347-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="21347-126">INPUTS</span></span>

### <span data-ttu-id="21347-127">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="21347-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="21347-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="21347-128">OUTPUTS</span></span>

### <span data-ttu-id="21347-129">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="21347-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="21347-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="21347-130">NOTES</span></span>

## <span data-ttu-id="21347-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="21347-131">RELATED LINKS</span></span>

[<span data-ttu-id="21347-132">Dodaj-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="21347-132">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="21347-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="21347-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="21347-134">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="21347-134">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="21347-135">Nowe — AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="21347-135">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="21347-136">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="21347-136">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


