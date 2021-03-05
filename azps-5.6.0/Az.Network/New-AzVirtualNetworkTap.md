---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkTap.md
ms.openlocfilehash: 93bc2a622d2bba077b5176c67df4d7894a95d4ae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978257"
---
# <span data-ttu-id="99611-101">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="99611-101">New-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="99611-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99611-102">SYNOPSIS</span></span>
<span data-ttu-id="99611-103">Tworzy zasób VirtualNetworkTap.</span><span class="sxs-lookup"><span data-stu-id="99611-103">Creates a VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="99611-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="99611-104">SYNTAX</span></span>

### <span data-ttu-id="99611-105">SetByResource (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="99611-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-DestinationPort <Int32>]
 [-Location <String>] [-Tag <Hashtable>]
 [-DestinationNetworkInterfaceIPConfiguration <PSNetworkInterfaceIPConfiguration>]
 [-DestinationLoadBalancerFrontEndIPConfiguration <PSFrontendIPConfiguration>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99611-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="99611-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-DestinationPort <Int32>]
 [-Location <String>] [-Tag <Hashtable>] [-DestinationNetworkInterfaceIPConfigurationId <String>]
 [-DestinationLoadBalancerFrontEndIPConfigurationId <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99611-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="99611-107">DESCRIPTION</span></span>
<span data-ttu-id="99611-108">Polecenie **cmdlet New-AzVirtualNetworkTap** tworzy zasób usługi Azure Virtual Network Tap.</span><span class="sxs-lookup"><span data-stu-id="99611-108">The **New-AzVirtualNetworkTap** cmdlet creates an Azure virtual network tap resource.</span></span>

## <span data-ttu-id="99611-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="99611-109">EXAMPLES</span></span>

### <span data-ttu-id="99611-110">Przykład 1. Tworzenie dotknięcia sieci wirtualnej platformy Azure</span><span class="sxs-lookup"><span data-stu-id="99611-110">Example 1: Create an Azure virtual network tap</span></span>
```
PS C:\>New-AzVirtualNetworkTap -Name "VirtualNetworkTap1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -DestinationPort 8888 -DestinationNetworkInterfaceIPConfiguration $destinationNic.IpConfigurations[0]
```

<span data-ttu-id="99611-111">To polecenie tworzy naciśnięcie sieci wirtualnej o nazwie "VirtualNetworkTap1", które ma szczegóły konfiguracji docelowej maszyny wirtualnej (DestinationIpConfiguration, DestinationPort).</span><span class="sxs-lookup"><span data-stu-id="99611-111">This command creates a virtual network tap named "VirtualNetworkTap1" which has destination VM configuration details (DestinationIpConfiguration, DestinationPort).</span></span>
<span data-ttu-id="99611-112">Cały ruch maszyny wirtualnej skonfigurowany do naciśnięcia źródła zostanie rozsyłany do tego adresu IP + portu miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="99611-112">All the source tap configured VM's traffic will be routed to this Destination IP + Port.</span></span>

### <span data-ttu-id="99611-113">Przykład 2. Tworzenie naciśnięcia sieci wirtualnej platformy Azure przy użyciu adresu IP narzędzia LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="99611-113">Example 2: Create an Azure virtual network tap using LoadBalancer IP</span></span>
```
# Create LoadBalancer
PS C:\>$frontend = New-AzLoadBalancerFrontendIpConfig -Name $frontendName -PublicIpAddress $publicip
PS C:\>New-AzVirtualNetworkTap -Name "VirtualNetworkTap1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -DestinationLoadBalancerFrontEndIPConfiguration $frontend
```

<span data-ttu-id="99611-114">To polecenie tworzy naciśnięcie sieci wirtualnej o nazwie "VirtualNetworkTap1", które ma szczegóły konfiguracji docelowej maszyny wirtualnej (FrontEndIpConfiguration).</span><span class="sxs-lookup"><span data-stu-id="99611-114">This command creates a virtual network tap named "VirtualNetworkTap1" which has destination VM configuration details (FrontEndIpConfiguration).</span></span>
<span data-ttu-id="99611-115">Cały ruch maszyny wirtualnej skonfigurowany przez naciśnięcie źródła zostanie przekierowyny do tej konfiguracji IpConfiguration protokołu LoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="99611-115">All the source tap configured VM's traffic will be routed to this LoadBalancer IpConfiguration.</span></span> <span data-ttu-id="99611-116">Domyślny port docelowy to 4789.</span><span class="sxs-lookup"><span data-stu-id="99611-116">Default Destination Port is 4789.</span></span>

## <span data-ttu-id="99611-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99611-117">PARAMETERS</span></span>

### <span data-ttu-id="99611-118">— AsJob</span><span class="sxs-lookup"><span data-stu-id="99611-118">-AsJob</span></span>
<span data-ttu-id="99611-119">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="99611-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="99611-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99611-120">-DefaultProfile</span></span>
<span data-ttu-id="99611-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="99611-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99611-122">-DestinationLoadBalancerFrontEndIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="99611-122">-DestinationLoadBalancerFrontEndIPConfiguration</span></span>
<span data-ttu-id="99611-123">Odwołanie do docelowego zasobu konfiguracji frontoronu IP równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="99611-123">The reference of the destination load balancer front end IP configuration resource.</span></span>

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

### <span data-ttu-id="99611-124">-DestinationLoadBalancerFrontEndIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="99611-124">-DestinationLoadBalancerFrontEndIPConfigurationId</span></span>
<span data-ttu-id="99611-125">Odwołanie do docelowego zasobu konfiguracji frontoronu IP równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="99611-125">The reference of the destination load balancer front end IP configuration resource.</span></span>

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

### <span data-ttu-id="99611-126">-DestinationNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="99611-126">-DestinationNetworkInterfaceIPConfiguration</span></span>
<span data-ttu-id="99611-127">Odwołanie do docelowego zasobu konfiguracji protokołu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="99611-127">The reference of the destination network interface IP configuration resource.</span></span>

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

### <span data-ttu-id="99611-128">-DestinationNetworkInterfaceIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="99611-128">-DestinationNetworkInterfaceIPConfigurationId</span></span>
<span data-ttu-id="99611-129">Odwołanie do docelowego zasobu konfiguracji protokołu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="99611-129">The reference of the destination network interface IP configuration resource.</span></span>

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

### <span data-ttu-id="99611-130">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="99611-130">-DestinationPort</span></span>
<span data-ttu-id="99611-131">Port docelowy pakietu</span><span class="sxs-lookup"><span data-stu-id="99611-131">The Destination Port of the packet collector</span></span>

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

### <span data-ttu-id="99611-132">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="99611-132">-Force</span></span>
<span data-ttu-id="99611-133">Nie pytaj o potwierdzenie, jeśli chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="99611-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="99611-134">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="99611-134">-Location</span></span>
<span data-ttu-id="99611-135">Lokalizacja.</span><span class="sxs-lookup"><span data-stu-id="99611-135">The location.</span></span>

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

### <span data-ttu-id="99611-136">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="99611-136">-Name</span></span>
<span data-ttu-id="99611-137">Nazwa naciśnięcia.</span><span class="sxs-lookup"><span data-stu-id="99611-137">The name of the tap.</span></span>

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

### <span data-ttu-id="99611-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99611-138">-ResourceGroupName</span></span>
<span data-ttu-id="99611-139">Nazwa grupy zasobów sieci wirtualnej naciśnij.</span><span class="sxs-lookup"><span data-stu-id="99611-139">The resource group name of the virtual network tap.</span></span>

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

### <span data-ttu-id="99611-140">— Tag</span><span class="sxs-lookup"><span data-stu-id="99611-140">-Tag</span></span>
<span data-ttu-id="99611-141">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="99611-141">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="99611-142">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="99611-142">-Confirm</span></span>
<span data-ttu-id="99611-143">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="99611-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99611-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99611-144">-WhatIf</span></span>
<span data-ttu-id="99611-145">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99611-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99611-146">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="99611-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99611-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99611-147">CommonParameters</span></span>
<span data-ttu-id="99611-148">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99611-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99611-149">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99611-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99611-150">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="99611-150">INPUTS</span></span>

### <span data-ttu-id="99611-151">System.String</span><span class="sxs-lookup"><span data-stu-id="99611-151">System.String</span></span>

### <span data-ttu-id="99611-152">System.Int32</span><span class="sxs-lookup"><span data-stu-id="99611-152">System.Int32</span></span>

### <span data-ttu-id="99611-153">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="99611-153">System.Collections.Hashtable</span></span>

### <span data-ttu-id="99611-154">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="99611-154">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

### <span data-ttu-id="99611-155">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="99611-155">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="99611-156">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="99611-156">OUTPUTS</span></span>

### <span data-ttu-id="99611-157">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="99611-157">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="99611-158">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="99611-158">NOTES</span></span>

## <span data-ttu-id="99611-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="99611-159">RELATED LINKS</span></span>

[<span data-ttu-id="99611-160">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="99611-160">Get-AzVirtualNetworkTap</span></span>](./Get-AzVirtualNetworkTap.md)

[<span data-ttu-id="99611-161">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="99611-161">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)

[<span data-ttu-id="99611-162">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="99611-162">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)
