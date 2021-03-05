---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5F8E11DF-D560-44D7-99CA-C425951A56D6
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 30b66350cffeae7fa42da7c9230a9f3976ab6cc2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993672"
---
# <span data-ttu-id="35dd2-101">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="35dd2-101">Remove-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="35dd2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35dd2-102">SYNOPSIS</span></span>
<span data-ttu-id="35dd2-103">Usuwa konfigurację frontoronu IP z urządzenia do równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="35dd2-103">Removes a front-end IP configuration from a load balancer.</span></span>

## <span data-ttu-id="35dd2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="35dd2-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35dd2-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="35dd2-105">DESCRIPTION</span></span>
<span data-ttu-id="35dd2-106">Polecenie **cmdlet Remove-AzLoadBalancerFrontendIpConfig** usuwa konfigurację frontoronu ip z narzędzia do równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="35dd2-106">The **Remove-AzLoadBalancerFrontendIpConfig** cmdlet removes a front-end IP configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="35dd2-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="35dd2-107">EXAMPLES</span></span>

### <span data-ttu-id="35dd2-108">Przykład 1. Usuwanie konfiguracji frontoronu ip z urządzenia do równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="35dd2-108">Example 1: Remove a front-end IP configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerFrontendIpConfig -Name "frontendName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="35dd2-109">Pierwsze polecenie pobiera równoważenie obciążenia skojarzone z konfiguracją frontonu adresu IP, którą chcesz usunąć, a następnie zapisuje je w $loadbalancer sieci.</span><span class="sxs-lookup"><span data-stu-id="35dd2-109">The first command gets the load balancer that is associated with the front-end IP configuration you want to remove, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="35dd2-110">Drugie polecenie usuwa skojarzoną konfigurację frontonu IP z równoważenia obciążenia w $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="35dd2-110">The second command removes the associated frontend IP configuration from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="35dd2-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35dd2-111">PARAMETERS</span></span>

### <span data-ttu-id="35dd2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35dd2-112">-DefaultProfile</span></span>
<span data-ttu-id="35dd2-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="35dd2-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35dd2-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="35dd2-114">-LoadBalancer</span></span>
<span data-ttu-id="35dd2-115">Określa równoważenie obciążenia zawierające konfigurację frontoronu IP do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="35dd2-115">Specifies the load balancer that contains the front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="35dd2-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="35dd2-116">-Name</span></span>
<span data-ttu-id="35dd2-117">Określa nazwę konfiguracji frontoronu adresu IP do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="35dd2-117">Specifies the name of the front-end IP address configuration to remove.</span></span>

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

### <span data-ttu-id="35dd2-118">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="35dd2-118">-Confirm</span></span>
<span data-ttu-id="35dd2-119">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="35dd2-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35dd2-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35dd2-120">-WhatIf</span></span>
<span data-ttu-id="35dd2-121">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35dd2-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="35dd2-122">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="35dd2-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35dd2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35dd2-123">CommonParameters</span></span>
<span data-ttu-id="35dd2-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35dd2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35dd2-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35dd2-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35dd2-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="35dd2-126">INPUTS</span></span>

### <span data-ttu-id="35dd2-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="35dd2-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="35dd2-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="35dd2-128">OUTPUTS</span></span>

### <span data-ttu-id="35dd2-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="35dd2-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="35dd2-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="35dd2-130">NOTES</span></span>

## <span data-ttu-id="35dd2-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="35dd2-131">RELATED LINKS</span></span>

[<span data-ttu-id="35dd2-132">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="35dd2-132">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="35dd2-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="35dd2-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="35dd2-134">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="35dd2-134">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="35dd2-135">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="35dd2-135">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="35dd2-136">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="35dd2-136">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


