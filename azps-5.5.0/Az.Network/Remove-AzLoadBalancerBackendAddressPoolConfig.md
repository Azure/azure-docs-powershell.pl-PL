---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F965A9DE-645C-471B-84E8-58D648B1CA57
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 26f7e0dde825305e888d598a23af0b2fbaff81cd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189602"
---
# <span data-ttu-id="51dbe-101">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="51dbe-101">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="51dbe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51dbe-102">SYNOPSIS</span></span>
<span data-ttu-id="51dbe-103">Usuwa konfigurację puli adresów zaplecza z urządzenia do równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="51dbe-103">Removes a backend address pool configuration from a load balancer.</span></span>

## <span data-ttu-id="51dbe-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="51dbe-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51dbe-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="51dbe-105">DESCRIPTION</span></span>
<span data-ttu-id="51dbe-106">Polecenie **cmdlet Remove-AzLoadBalancerBackendAddressPoolConfig** usuwa pulę adresów zaplecza z równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="51dbe-106">The **Remove-AzLoadBalancerBackendAddressPoolConfig** cmdlet removes a backend address pool from a load balancer.</span></span>

## <span data-ttu-id="51dbe-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="51dbe-107">EXAMPLES</span></span>

### <span data-ttu-id="51dbe-108">Przykład 1. Usuwanie konfiguracji puli adresów zaplecza z równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="51dbe-108">Example 1: Remove a backend address pool configuration from a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" | Remove-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

<span data-ttu-id="51dbe-109">To polecenie pobiera równoważenie obciążenia o nazwie MyLoadBalancer i przekazuje je do **remove-AzLoadBalancerBackendAddressPoolConfig,** co usuwa konfigurację BackendAddressPool02 z myLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="51dbe-109">This command gets the load balancer named MyLoadBalancer and passes it to **Remove-AzLoadBalancerBackendAddressPoolConfig**, which removes the BackendAddressPool02 configuration from MyLoadBalancer.</span></span>
<span data-ttu-id="51dbe-110">Na koniec polecenie Set-AzLoadBalancer aktualizuje polecenie MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="51dbe-110">Finally, the Set-AzLoadBalancer cmdlet updates MyLoadBalancer.</span></span>
<span data-ttu-id="51dbe-111">Pamiętaj, że aby można było usunąć pulę adresów zaplecza, musi istnieć konfiguracja puli adresów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="51dbe-111">Note that a backend address pool configuration must exist before you can delete it.</span></span>

## <span data-ttu-id="51dbe-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="51dbe-112">PARAMETERS</span></span>

### <span data-ttu-id="51dbe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51dbe-113">-DefaultProfile</span></span>
<span data-ttu-id="51dbe-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="51dbe-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51dbe-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="51dbe-115">-LoadBalancer</span></span>
<span data-ttu-id="51dbe-116">Określa równoważenie obciążenia zawierające pulę adresów zaplecza do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="51dbe-116">Specifies the load balancer that contains the backend address pool to remove.</span></span>

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

### <span data-ttu-id="51dbe-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="51dbe-117">-Name</span></span>
<span data-ttu-id="51dbe-118">Określa nazwę puli adresów zaplecza, która jest usuwana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51dbe-118">Specifies the name of the backend address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="51dbe-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="51dbe-119">-Confirm</span></span>
<span data-ttu-id="51dbe-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="51dbe-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51dbe-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51dbe-121">-WhatIf</span></span>
<span data-ttu-id="51dbe-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51dbe-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="51dbe-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="51dbe-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51dbe-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51dbe-124">CommonParameters</span></span>
<span data-ttu-id="51dbe-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51dbe-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51dbe-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51dbe-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51dbe-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="51dbe-127">INPUTS</span></span>

### <span data-ttu-id="51dbe-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="51dbe-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="51dbe-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="51dbe-129">OUTPUTS</span></span>

### <span data-ttu-id="51dbe-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="51dbe-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="51dbe-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="51dbe-131">NOTES</span></span>

## <span data-ttu-id="51dbe-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="51dbe-132">RELATED LINKS</span></span>

[<span data-ttu-id="51dbe-133">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="51dbe-133">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="51dbe-134">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="51dbe-134">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="51dbe-135">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="51dbe-135">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="51dbe-136">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="51dbe-136">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)


