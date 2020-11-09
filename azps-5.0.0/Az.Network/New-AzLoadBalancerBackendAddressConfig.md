---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddressconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressConfig.md
ms.openlocfilehash: 7d373092f850dd25abe5b6d913ddcf2572d4be94
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317953"
---
# <span data-ttu-id="79ae6-101">New-AzLoadBalancerBackendAddressConfig</span><span class="sxs-lookup"><span data-stu-id="79ae6-101">New-AzLoadBalancerBackendAddressConfig</span></span>

## <span data-ttu-id="79ae6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="79ae6-102">SYNOPSIS</span></span>
<span data-ttu-id="79ae6-103">Zwraca konfigurację adresu zaplecza modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="79ae6-103">Returns a load balancer backend address config.</span></span> 

## <span data-ttu-id="79ae6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="79ae6-104">SYNTAX</span></span>

```
New-AzLoadBalancerBackendAddressConfig -IpAddress <String> -Name <String> -VirtualNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79ae6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="79ae6-105">DESCRIPTION</span></span>
<span data-ttu-id="79ae6-106">Zwraca konfigurację adresu zaplecza modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="79ae6-106">Returns a load balancer backend address config.</span></span> 

## <span data-ttu-id="79ae6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="79ae6-107">EXAMPLES</span></span>

### <span data-ttu-id="79ae6-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="79ae6-108">Example 1</span></span>
### <span data-ttu-id="79ae6-109">Przykład 2: Nowa konfiguracja adresu usługi równoważenia obciążenia z odwołaniem do sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="79ae6-109">Example 2: New loadbalancer address config with virtual network reference</span></span>
```powershell
PS C:\> $virtualNetwork = Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroup
New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.5" -Name "TestVNetRef" -VirtualNetworkId $virtualNetwork.Id
```

## <span data-ttu-id="79ae6-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="79ae6-110">PARAMETERS</span></span>

### <span data-ttu-id="79ae6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79ae6-111">-DefaultProfile</span></span>
<span data-ttu-id="79ae6-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="79ae6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79ae6-113">-Adres_IP</span><span class="sxs-lookup"><span data-stu-id="79ae6-113">-IpAddress</span></span>
<span data-ttu-id="79ae6-114">Adres IP dodawany do puli zaplecza</span><span class="sxs-lookup"><span data-stu-id="79ae6-114">The IPAddress to add to the backend pool</span></span>

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

### <span data-ttu-id="79ae6-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="79ae6-115">-Name</span></span>
<span data-ttu-id="79ae6-116">Nazwa konfiguracji adresu zaplecza</span><span class="sxs-lookup"><span data-stu-id="79ae6-116">The name of the Backend Address config</span></span>

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

### <span data-ttu-id="79ae6-117">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="79ae6-117">-VirtualNetworkId</span></span>
<span data-ttu-id="79ae6-118">Sieć wirtualna skojarzona z konfiguracją adresu zaplecza</span><span class="sxs-lookup"><span data-stu-id="79ae6-118">The virtual network associated with Backend Address config</span></span>

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

### <span data-ttu-id="79ae6-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="79ae6-119">-Confirm</span></span>
<span data-ttu-id="79ae6-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79ae6-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79ae6-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79ae6-121">-WhatIf</span></span>
<span data-ttu-id="79ae6-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79ae6-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="79ae6-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="79ae6-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79ae6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79ae6-124">CommonParameters</span></span>
<span data-ttu-id="79ae6-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79ae6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79ae6-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="79ae6-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79ae6-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="79ae6-127">INPUTS</span></span>

### <span data-ttu-id="79ae6-128">System. String</span><span class="sxs-lookup"><span data-stu-id="79ae6-128">System.String</span></span>

### <span data-ttu-id="79ae6-129">Microsoft. Azure. Commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="79ae6-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="79ae6-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="79ae6-130">OUTPUTS</span></span>

### <span data-ttu-id="79ae6-131">Microsoft. Azure. Commands. Network. models. PSLoadBalancerBackendAddress</span><span class="sxs-lookup"><span data-stu-id="79ae6-131">Microsoft.Azure.Commands.Network.Models.PSLoadBalancerBackendAddress</span></span>

## <span data-ttu-id="79ae6-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="79ae6-132">NOTES</span></span>

## <span data-ttu-id="79ae6-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="79ae6-133">RELATED LINKS</span></span>
