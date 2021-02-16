---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9EB11283-0189-4333-8142-DCC3F770F91A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 39e388fbdb809f136942749a0d0585189155e32b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203192"
---
# <span data-ttu-id="33bf3-101">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="33bf3-101">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="33bf3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33bf3-102">SYNOPSIS</span></span>
<span data-ttu-id="33bf3-103">Dodaje konfigurację puli adresów zaplecza do równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="33bf3-103">Adds a backend address pool configuration to a load balancer.</span></span>

## <span data-ttu-id="33bf3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="33bf3-104">SYNTAX</span></span>

```
Add-AzLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33bf3-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="33bf3-105">DESCRIPTION</span></span>
<span data-ttu-id="33bf3-106">Polecenie **cmdlet Add-AzLoadBalancerBackend** dodaje pulę adresów zaplecza do narzędzia do równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="33bf3-106">The **Add-AzLoadBalancerBackend** cmdlet adds a backend address pool to an Azure load balancer.</span></span>

## <span data-ttu-id="33bf3-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="33bf3-107">EXAMPLES</span></span>

### <span data-ttu-id="33bf3-108">Przykład 1. Dodawanie konfiguracji puli adresów zaplecza do równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="33bf3-108">Example 1: Add a backend address pool configuration to a load balancer</span></span>
```powershell
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myrg" | Add-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

<span data-ttu-id="33bf3-109">To polecenie pobiera równoważenie obciążenia o nazwie MyLoadBalancer, dodaje pulę adresów zaplecza o nazwie BackendAddressPool02 do myLoadBalancer, a następnie używa polecenia cmdlet **Set-AzLoadBalancer** w celu zaktualizowania myLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="33bf3-109">This command gets the load balancer named MyLoadBalancer, adds the backend address pool named BackendAddressPool02 to MyLoadBalancer, and then uses the **Set-AzLoadBalancer** cmdlet to update MyLoadBalancer.</span></span>

## <span data-ttu-id="33bf3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="33bf3-110">PARAMETERS</span></span>

### <span data-ttu-id="33bf3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33bf3-111">-DefaultProfile</span></span>
<span data-ttu-id="33bf3-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="33bf3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33bf3-113">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="33bf3-113">-LoadBalancer</span></span>
<span data-ttu-id="33bf3-114">Określa obiekt **LoadBalancer.**</span><span class="sxs-lookup"><span data-stu-id="33bf3-114">Specifies a **LoadBalancer** object.</span></span>

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

### <span data-ttu-id="33bf3-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="33bf3-115">-Name</span></span>
<span data-ttu-id="33bf3-116">Określa nazwę konfiguracji puli adresów zaplecza do dodania.</span><span class="sxs-lookup"><span data-stu-id="33bf3-116">Specifies the name of the backend address pool configuration to add.</span></span>

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

### <span data-ttu-id="33bf3-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="33bf3-117">-Confirm</span></span>
<span data-ttu-id="33bf3-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="33bf3-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33bf3-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33bf3-119">-WhatIf</span></span>
<span data-ttu-id="33bf3-120">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33bf3-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="33bf3-121">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="33bf3-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33bf3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33bf3-122">CommonParameters</span></span>
<span data-ttu-id="33bf3-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33bf3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33bf3-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33bf3-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33bf3-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="33bf3-125">INPUTS</span></span>

### <span data-ttu-id="33bf3-126">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="33bf3-126">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="33bf3-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="33bf3-127">OUTPUTS</span></span>

### <span data-ttu-id="33bf3-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="33bf3-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="33bf3-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="33bf3-129">NOTES</span></span>

## <span data-ttu-id="33bf3-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="33bf3-130">RELATED LINKS</span></span>

[<span data-ttu-id="33bf3-131">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="33bf3-131">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="33bf3-132">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="33bf3-132">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="33bf3-133">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="33bf3-133">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="33bf3-134">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="33bf3-134">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="33bf3-135">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="33bf3-135">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


