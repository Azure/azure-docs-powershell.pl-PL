---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddressconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressConfig.md
ms.openlocfilehash: 3c3cc0e5da1cc8afbc6160acf13c3ef94eb02e34
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98500345"
---
# <span data-ttu-id="ba11a-101">New-AzLoadBalancerBackendAddressConfig</span><span class="sxs-lookup"><span data-stu-id="ba11a-101">New-AzLoadBalancerBackendAddressConfig</span></span>

## <span data-ttu-id="ba11a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ba11a-102">SYNOPSIS</span></span>
<span data-ttu-id="ba11a-103">Zwraca konfigurację adresu zaplecza modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="ba11a-103">Returns a load balancer backend address config.</span></span> 

## <span data-ttu-id="ba11a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ba11a-104">SYNTAX</span></span>

### <span data-ttu-id="ba11a-105">SetByResourcePublicIpAddress (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ba11a-105">SetByResourcePublicIpAddress (Default)</span></span>
```
New-AzLoadBalancerBackendAddressConfig -IpAddress <String> -Name <String> -VirtualNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba11a-106">SetByResourceFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ba11a-106">SetByResourceFrontendIPConfiguration</span></span>
```
New-AzLoadBalancerBackendAddressConfig -Name <String> -LoadBalancerFrontendIPConfigurationId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba11a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ba11a-107">DESCRIPTION</span></span>
<span data-ttu-id="ba11a-108">Zwraca konfigurację adresu zaplecza modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="ba11a-108">Returns a load balancer backend address config.</span></span> 

## <span data-ttu-id="ba11a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ba11a-109">EXAMPLES</span></span>

### <span data-ttu-id="ba11a-110">Przykład 1: Nowa konfiguracja adresu usługi równoważenia obciążenia z odwołaniem do sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="ba11a-110">Example 1: New loadbalancer address config with virtual network reference</span></span>
```powershell
PS C:\> $virtualNetwork = Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroup
New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.5" -Name "TestVNetRef" -VirtualNetworkId $virtualNetwork.Id
```

### <span data-ttu-id="ba11a-111">Przykład 2: Nowa konfiguracja adresu usługi równoważenia obciążenia z adresem IP frontonu modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="ba11a-111">Example 2: New loadbalancer address config with loadbalancer frontend ip configuration reference</span></span>
```powershell
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name $frontendName -PublicIpAddress $publicip
New-AzLoadBalancerBackendAddressConfig -LoadBalancerFrontendIPConfigurationId $frontend.Id -Name "TestLBFERef"
```

## <span data-ttu-id="ba11a-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ba11a-112">PARAMETERS</span></span>

### <span data-ttu-id="ba11a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba11a-113">-DefaultProfile</span></span>
<span data-ttu-id="ba11a-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ba11a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba11a-115">-Adres_IP</span><span class="sxs-lookup"><span data-stu-id="ba11a-115">-IpAddress</span></span>
<span data-ttu-id="ba11a-116">Adres IP dodawany do puli zaplecza</span><span class="sxs-lookup"><span data-stu-id="ba11a-116">The IPAddress to add to the backend pool</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourcePublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba11a-117">-LoadBalancerFrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="ba11a-117">-LoadBalancerFrontendIPConfigurationId</span></span>
<span data-ttu-id="ba11a-118">Konfiguracja adresu IP frontonu modułu równoważenia obciążenia skojarzona z konfiguracją adresów zaplecza</span><span class="sxs-lookup"><span data-stu-id="ba11a-118">The load balancer frontend ip configuration associated with Backend Address config</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceFrontendIPConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba11a-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ba11a-119">-Name</span></span>
<span data-ttu-id="ba11a-120">Nazwa konfiguracji adresu zaplecza</span><span class="sxs-lookup"><span data-stu-id="ba11a-120">The name of the Backend Address config</span></span>

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

### <span data-ttu-id="ba11a-121">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="ba11a-121">-VirtualNetworkId</span></span>
<span data-ttu-id="ba11a-122">Sieć wirtualna skojarzona z konfiguracją adresu zaplecza</span><span class="sxs-lookup"><span data-stu-id="ba11a-122">The virtual network associated with Backend Address config</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourcePublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba11a-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ba11a-123">-Confirm</span></span>
<span data-ttu-id="ba11a-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba11a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba11a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba11a-125">-WhatIf</span></span>
<span data-ttu-id="ba11a-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba11a-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ba11a-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ba11a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba11a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba11a-128">CommonParameters</span></span>
<span data-ttu-id="ba11a-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba11a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba11a-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ba11a-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba11a-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ba11a-131">INPUTS</span></span>

### <span data-ttu-id="ba11a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ba11a-132">System.String</span></span>

### <span data-ttu-id="ba11a-133">Microsoft. Azure. Commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ba11a-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="ba11a-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ba11a-134">OUTPUTS</span></span>

### <span data-ttu-id="ba11a-135">Microsoft. Azure. Commands. Network. models. PSLoadBalancerBackendAddress</span><span class="sxs-lookup"><span data-stu-id="ba11a-135">Microsoft.Azure.Commands.Network.Models.PSLoadBalancerBackendAddress</span></span>

## <span data-ttu-id="ba11a-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ba11a-136">NOTES</span></span>

## <span data-ttu-id="ba11a-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ba11a-137">RELATED LINKS</span></span>
