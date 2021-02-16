---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddressconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressConfig.md
ms.openlocfilehash: 3c3cc0e5da1cc8afbc6160acf13c3ef94eb02e34
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179667"
---
# <span data-ttu-id="65cb9-101">New-AzLoadBalancerBackendAddressConfig</span><span class="sxs-lookup"><span data-stu-id="65cb9-101">New-AzLoadBalancerBackendAddressConfig</span></span>

## <span data-ttu-id="65cb9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65cb9-102">SYNOPSIS</span></span>
<span data-ttu-id="65cb9-103">Zwraca adres zaplecza równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="65cb9-103">Returns a load balancer backend address config.</span></span> 

## <span data-ttu-id="65cb9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="65cb9-104">SYNTAX</span></span>

### <span data-ttu-id="65cb9-105">SetByResourcePublicIpAddress (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="65cb9-105">SetByResourcePublicIpAddress (Default)</span></span>
```
New-AzLoadBalancerBackendAddressConfig -IpAddress <String> -Name <String> -VirtualNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65cb9-106">SetByResourceFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="65cb9-106">SetByResourceFrontendIPConfiguration</span></span>
```
New-AzLoadBalancerBackendAddressConfig -Name <String> -LoadBalancerFrontendIPConfigurationId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65cb9-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="65cb9-107">DESCRIPTION</span></span>
<span data-ttu-id="65cb9-108">Zwraca adres zaplecza równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="65cb9-108">Returns a load balancer backend address config.</span></span> 

## <span data-ttu-id="65cb9-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="65cb9-109">EXAMPLES</span></span>

### <span data-ttu-id="65cb9-110">Przykład 1. Nowy konfiguracja adresu równoważenia obciążenia z odwołaniem do sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="65cb9-110">Example 1: New loadbalancer address config with virtual network reference</span></span>
```powershell
PS C:\> $virtualNetwork = Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroup
New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.5" -Name "TestVNetRef" -VirtualNetworkId $virtualNetwork.Id
```

### <span data-ttu-id="65cb9-111">Przykład 2. Nowy adres konfiguracji równoważenia obciążenia z odwołaniem do konfiguracji frontendu ip loadbalancer</span><span class="sxs-lookup"><span data-stu-id="65cb9-111">Example 2: New loadbalancer address config with loadbalancer frontend ip configuration reference</span></span>
```powershell
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name $frontendName -PublicIpAddress $publicip
New-AzLoadBalancerBackendAddressConfig -LoadBalancerFrontendIPConfigurationId $frontend.Id -Name "TestLBFERef"
```

## <span data-ttu-id="65cb9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="65cb9-112">PARAMETERS</span></span>

### <span data-ttu-id="65cb9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65cb9-113">-DefaultProfile</span></span>
<span data-ttu-id="65cb9-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="65cb9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65cb9-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="65cb9-115">-IpAddress</span></span>
<span data-ttu-id="65cb9-116">Adres IPAddress, który należy dodać do puli zaplecza</span><span class="sxs-lookup"><span data-stu-id="65cb9-116">The IPAddress to add to the backend pool</span></span>

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

### <span data-ttu-id="65cb9-117">-LoadBalancerFrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="65cb9-117">-LoadBalancerFrontendIPConfigurationId</span></span>
<span data-ttu-id="65cb9-118">Konfiguracja frontendu adresu IP równoważenia obciążenia skojarzona z konfiguracją adresu zaplecza</span><span class="sxs-lookup"><span data-stu-id="65cb9-118">The load balancer frontend ip configuration associated with Backend Address config</span></span>

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

### <span data-ttu-id="65cb9-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="65cb9-119">-Name</span></span>
<span data-ttu-id="65cb9-120">Nazwa konfiguracji adresu zaplecza</span><span class="sxs-lookup"><span data-stu-id="65cb9-120">The name of the Backend Address config</span></span>

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

### <span data-ttu-id="65cb9-121">- VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="65cb9-121">-VirtualNetworkId</span></span>
<span data-ttu-id="65cb9-122">Sieć wirtualna skojarzona z konfiguracją adresu zaplecza</span><span class="sxs-lookup"><span data-stu-id="65cb9-122">The virtual network associated with Backend Address config</span></span>

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

### <span data-ttu-id="65cb9-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="65cb9-123">-Confirm</span></span>
<span data-ttu-id="65cb9-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="65cb9-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65cb9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65cb9-125">-WhatIf</span></span>
<span data-ttu-id="65cb9-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65cb9-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="65cb9-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="65cb9-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65cb9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65cb9-128">CommonParameters</span></span>
<span data-ttu-id="65cb9-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65cb9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65cb9-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="65cb9-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65cb9-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="65cb9-131">INPUTS</span></span>

### <span data-ttu-id="65cb9-132">System.String</span><span class="sxs-lookup"><span data-stu-id="65cb9-132">System.String</span></span>

### <span data-ttu-id="65cb9-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="65cb9-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="65cb9-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="65cb9-134">OUTPUTS</span></span>

### <span data-ttu-id="65cb9-135">Microsoft.Azure.Commands.Network.Models.PSLoadBalancerBackendAddress</span><span class="sxs-lookup"><span data-stu-id="65cb9-135">Microsoft.Azure.Commands.Network.Models.PSLoadBalancerBackendAddress</span></span>

## <span data-ttu-id="65cb9-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="65cb9-136">NOTES</span></span>

## <span data-ttu-id="65cb9-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="65cb9-137">RELATED LINKS</span></span>
