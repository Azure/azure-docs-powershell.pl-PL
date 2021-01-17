---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkTap.md
ms.openlocfilehash: 0ac64d9b1aee363a1681b8d62da2ecf73574f7cd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379024"
---
# <span data-ttu-id="03011-101">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="03011-101">New-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="03011-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="03011-102">SYNOPSIS</span></span>
<span data-ttu-id="03011-103">Tworzy zasób VirtualNetworkTap.</span><span class="sxs-lookup"><span data-stu-id="03011-103">Creates a VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="03011-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="03011-104">SYNTAX</span></span>

### <span data-ttu-id="03011-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="03011-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-DestinationPort <Int32>]
 [-Location <String>] [-Tag <Hashtable>]
 [-DestinationNetworkInterfaceIPConfiguration <PSNetworkInterfaceIPConfiguration>]
 [-DestinationLoadBalancerFrontEndIPConfiguration <PSFrontendIPConfiguration>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03011-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="03011-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-DestinationPort <Int32>]
 [-Location <String>] [-Tag <Hashtable>] [-DestinationNetworkInterfaceIPConfigurationId <String>]
 [-DestinationLoadBalancerFrontEndIPConfigurationId <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03011-107">Opis</span><span class="sxs-lookup"><span data-stu-id="03011-107">DESCRIPTION</span></span>
<span data-ttu-id="03011-108">Polecenie cmdlet **New-AzVirtualNetworkTap** umożliwia utworzenie zasobu sieci wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="03011-108">The **New-AzVirtualNetworkTap** cmdlet creates an Azure virtual network tap resource.</span></span>

## <span data-ttu-id="03011-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="03011-109">EXAMPLES</span></span>

### <span data-ttu-id="03011-110">Przykład 1. Naciśnij pozycję Utwórz sieć wirtualną Azure</span><span class="sxs-lookup"><span data-stu-id="03011-110">Example 1: Create an Azure virtual network tap</span></span>
```
PS C:\>New-AzVirtualNetworkTap -Name "VirtualNetworkTap1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -DestinationPort 8888 -DestinationNetworkInterfaceIPConfiguration $destinationNic.IpConfigurations[0]
```

<span data-ttu-id="03011-111">To polecenie tworzy sieć wirtualną, wybierając nazwę "VirtualNetworkTap1", która ma dane konfiguracji docelowej maszyny wirtualnej (DestinationIpConfiguration, DestinationPort).</span><span class="sxs-lookup"><span data-stu-id="03011-111">This command creates a virtual network tap named "VirtualNetworkTap1" which has destination VM configuration details (DestinationIpConfiguration, DestinationPort).</span></span>
<span data-ttu-id="03011-112">Wszystkie źródła, które skonfigurowano w celu nakierowania ruchu maszyny wirtualnej, będą przekierowywane do tego docelowego adresu IP + portu.</span><span class="sxs-lookup"><span data-stu-id="03011-112">All the source tap configured VM's traffic will be routed to this Destination IP + Port.</span></span>

### <span data-ttu-id="03011-113">Przykład 2: tworzenie sieci wirtualnej platformy Azure naciśnij przy użyciu protokołu równoważenia adresu IP</span><span class="sxs-lookup"><span data-stu-id="03011-113">Example 2: Create an Azure virtual network tap using LoadBalancer IP</span></span>
```
# Create LoadBalancer
PS C:\>$frontend = New-AzLoadBalancerFrontendIpConfig -Name $frontendName -PublicIpAddress $publicip
PS C:\>New-AzVirtualNetworkTap -Name "VirtualNetworkTap1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -DestinationLoadBalancerFrontEndIPConfiguration $frontend
```

<span data-ttu-id="03011-114">To polecenie tworzy sieć wirtualną, wybierając nazwę "VirtualNetworkTap1", która ma docelowe dane konfiguracji maszyny wirtualnej (FrontEndIpConfiguration).</span><span class="sxs-lookup"><span data-stu-id="03011-114">This command creates a virtual network tap named "VirtualNetworkTap1" which has destination VM configuration details (FrontEndIpConfiguration).</span></span>
<span data-ttu-id="03011-115">Wszystkie dane źródłowe skonfigurowanej maszyny wirtualnej z maszyną wirtualną zostaną przekierowane do tego elementu IpConfiguration modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="03011-115">All the source tap configured VM's traffic will be routed to this LoadBalancer IpConfiguration.</span></span> <span data-ttu-id="03011-116">Domyślnym portem docelowym jest 4789.</span><span class="sxs-lookup"><span data-stu-id="03011-116">Default Destination Port is 4789.</span></span>

## <span data-ttu-id="03011-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="03011-117">PARAMETERS</span></span>

### <span data-ttu-id="03011-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="03011-118">-AsJob</span></span>
<span data-ttu-id="03011-119">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="03011-119">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03011-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03011-120">-DefaultProfile</span></span>
<span data-ttu-id="03011-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="03011-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03011-122">-DestinationLoadBalancerFrontEndIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="03011-122">-DestinationLoadBalancerFrontEndIPConfiguration</span></span>
<span data-ttu-id="03011-123">Odwołanie do zasobu konfiguracji IP frontonu modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="03011-123">The reference of the destination load balancer front end IP configuration resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03011-124">-DestinationLoadBalancerFrontEndIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="03011-124">-DestinationLoadBalancerFrontEndIPConfigurationId</span></span>
<span data-ttu-id="03011-125">Odwołanie do zasobu konfiguracji IP frontonu modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="03011-125">The reference of the destination load balancer front end IP configuration resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03011-126">-DestinationNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="03011-126">-DestinationNetworkInterfaceIPConfiguration</span></span>
<span data-ttu-id="03011-127">Odwołanie do zasobu konfiguracji IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="03011-127">The reference of the destination network interface IP configuration resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03011-128">-DestinationNetworkInterfaceIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="03011-128">-DestinationNetworkInterfaceIPConfigurationId</span></span>
<span data-ttu-id="03011-129">Odwołanie do zasobu konfiguracji IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="03011-129">The reference of the destination network interface IP configuration resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03011-130">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="03011-130">-DestinationPort</span></span>
<span data-ttu-id="03011-131">Port docelowy modułu zbierającego pakiety</span><span class="sxs-lookup"><span data-stu-id="03011-131">The Destination Port of the packet collector</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03011-132">-Force</span><span class="sxs-lookup"><span data-stu-id="03011-132">-Force</span></span>
<span data-ttu-id="03011-133">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="03011-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03011-134">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="03011-134">-Location</span></span>
<span data-ttu-id="03011-135">Lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="03011-135">The location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03011-136">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="03011-136">-Name</span></span>
<span data-ttu-id="03011-137">Nazwa naciśnięcia przycisku.</span><span class="sxs-lookup"><span data-stu-id="03011-137">The name of the tap.</span></span>

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

### <span data-ttu-id="03011-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03011-138">-ResourceGroupName</span></span>
<span data-ttu-id="03011-139">Nazwa grupy zasobów naciśnięcie sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="03011-139">The resource group name of the virtual network tap.</span></span>

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

### <span data-ttu-id="03011-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="03011-140">-Tag</span></span>
<span data-ttu-id="03011-141">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="03011-141">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03011-142">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="03011-142">-Confirm</span></span>
<span data-ttu-id="03011-143">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03011-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03011-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03011-144">-WhatIf</span></span>
<span data-ttu-id="03011-145">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03011-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03011-146">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="03011-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03011-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03011-147">CommonParameters</span></span>
<span data-ttu-id="03011-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03011-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03011-149">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03011-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03011-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="03011-150">INPUTS</span></span>

### <span data-ttu-id="03011-151">System. String</span><span class="sxs-lookup"><span data-stu-id="03011-151">System.String</span></span>

### <span data-ttu-id="03011-152">System. Int32</span><span class="sxs-lookup"><span data-stu-id="03011-152">System.Int32</span></span>

### <span data-ttu-id="03011-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="03011-153">System.Collections.Hashtable</span></span>

### <span data-ttu-id="03011-154">Microsoft. Azure. Commands. Network. models. PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="03011-154">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

### <span data-ttu-id="03011-155">Microsoft. Azure. Commands. Network. models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="03011-155">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="03011-156">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="03011-156">OUTPUTS</span></span>

### <span data-ttu-id="03011-157">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="03011-157">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="03011-158">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="03011-158">NOTES</span></span>

## <span data-ttu-id="03011-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="03011-159">RELATED LINKS</span></span>

[<span data-ttu-id="03011-160">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="03011-160">Get-AzVirtualNetworkTap</span></span>](./Get-AzVirtualNetworkTap.md)

[<span data-ttu-id="03011-161">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="03011-161">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)

[<span data-ttu-id="03011-162">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="03011-162">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)
