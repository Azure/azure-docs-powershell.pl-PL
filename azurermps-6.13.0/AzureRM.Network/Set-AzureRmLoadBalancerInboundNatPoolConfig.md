---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 355DF798-6233-45C6-9416-8AB0E0D7DC02
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 3d2110b4d8f4caf75751745ef996cb18094ae7e6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551151"
---
# <span data-ttu-id="79e7b-101">Set-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="79e7b-101">Set-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="79e7b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="79e7b-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79e7b-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="79e7b-103">SYNTAX</span></span>

### <span data-ttu-id="79e7b-104">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="79e7b-104">SetByResource (Default)</span></span>
```
Set-AzureRmLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79e7b-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="79e7b-105">SetByResourceId</span></span>
```
Set-AzureRmLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset] [-FrontendIpConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79e7b-106">Opis</span><span class="sxs-lookup"><span data-stu-id="79e7b-106">DESCRIPTION</span></span>

## <span data-ttu-id="79e7b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="79e7b-107">EXAMPLES</span></span>

### <span data-ttu-id="79e7b-108">1: Ustaw</span><span class="sxs-lookup"><span data-stu-id="79e7b-108">1: Set</span></span>
```
PS C:\> $slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $feIpConfig = Get-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -LoadBalancer $slb
PS C:\> Set-AzureRmLoadBalancerInboundNatPoolConfig -Name "myInboundNatPool" -LoadBalancer $slb -FrontendIpConfigurationId $inboundNatPoolConfig.FrontendIPConfiguration -Protocol TCP -FrontendPortRangeStart 2001 -FrontendPortRangeEnd 3000 -BackendPort 2001
```

## <span data-ttu-id="79e7b-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="79e7b-109">PARAMETERS</span></span>

### <span data-ttu-id="79e7b-110">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="79e7b-110">-BackendPort</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79e7b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79e7b-111">-DefaultProfile</span></span>
<span data-ttu-id="79e7b-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="79e7b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79e7b-113">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="79e7b-113">-EnableFloatingIP</span></span>
<span data-ttu-id="79e7b-114">Umożliwia skonfigurowanie punktu końcowego maszyny wirtualnej dla przestawnego adresu IP wymaganego do skonfigurowania grupy dostępności funkcji SQL AlwaysOn.</span><span class="sxs-lookup"><span data-stu-id="79e7b-114">Configures a virtual machine's endpoint for the floating IP capability required to configure a SQL AlwaysOn Availability Group.</span></span> <span data-ttu-id="79e7b-115">To ustawienie jest wymagane w przypadku używania grup dostępności funkcji SQL AlwaysOn w programie SQL Server.</span><span class="sxs-lookup"><span data-stu-id="79e7b-115">This setting is required when using the SQL AlwaysOn Availability Groups in SQL server.</span></span> <span data-ttu-id="79e7b-116">Tego ustawienia nie można zmienić po utworzeniu punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="79e7b-116">This setting can't be changed after you create the endpoint.</span></span>

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

### <span data-ttu-id="79e7b-117">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="79e7b-117">-EnableTcpReset</span></span>
<span data-ttu-id="79e7b-118">Odbieraj dwukierunkowe Resetowanie protokołu TCP na limicie czasu bezczynności przepływu TCP lub nieoczekiwane zakończenie połączenia.</span><span class="sxs-lookup"><span data-stu-id="79e7b-118">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="79e7b-119">Ten element jest wykorzystywany tylko wtedy, gdy protokół jest ustawiony na protokół TCP.</span><span class="sxs-lookup"><span data-stu-id="79e7b-119">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="79e7b-120">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="79e7b-120">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="79e7b-121">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="79e7b-121">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="79e7b-122">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="79e7b-122">-FrontendPortRangeEnd</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79e7b-123">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="79e7b-123">-FrontendPortRangeStart</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79e7b-124">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="79e7b-124">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="79e7b-125">Limit czasu bezczynności połączenia TCP.</span><span class="sxs-lookup"><span data-stu-id="79e7b-125">The timeout for the TCP idle connection.</span></span> <span data-ttu-id="79e7b-126">Wartość może być ustawiona między 4 a 30 minut.</span><span class="sxs-lookup"><span data-stu-id="79e7b-126">The value can be set between 4 and 30 minutes.</span></span> <span data-ttu-id="79e7b-127">Wartość domyślna to 4 minuty.</span><span class="sxs-lookup"><span data-stu-id="79e7b-127">The default value is 4 minutes.</span></span> <span data-ttu-id="79e7b-128">Ten element jest wykorzystywany tylko wtedy, gdy protokół jest ustawiony na protokół TCP.</span><span class="sxs-lookup"><span data-stu-id="79e7b-128">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="79e7b-129">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="79e7b-129">-LoadBalancer</span></span>
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

### <span data-ttu-id="79e7b-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="79e7b-130">-Name</span></span>
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

### <span data-ttu-id="79e7b-131">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="79e7b-131">-Protocol</span></span>
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

### <span data-ttu-id="79e7b-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="79e7b-132">-Confirm</span></span>
<span data-ttu-id="79e7b-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79e7b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79e7b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79e7b-134">-WhatIf</span></span>
<span data-ttu-id="79e7b-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79e7b-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="79e7b-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="79e7b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79e7b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79e7b-137">CommonParameters</span></span>
<span data-ttu-id="79e7b-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79e7b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79e7b-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79e7b-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79e7b-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="79e7b-140">INPUTS</span></span>

### <span data-ttu-id="79e7b-141">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="79e7b-141">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="79e7b-142">Parametry: moduł równoważenia obciążenia (ByValue)</span><span class="sxs-lookup"><span data-stu-id="79e7b-142">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="79e7b-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="79e7b-143">OUTPUTS</span></span>

### <span data-ttu-id="79e7b-144">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="79e7b-144">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="79e7b-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="79e7b-145">NOTES</span></span>

## <span data-ttu-id="79e7b-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="79e7b-146">RELATED LINKS</span></span>

[<span data-ttu-id="79e7b-147">Dodaj-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="79e7b-147">Add-AzureRmLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzureRmLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="79e7b-148">Get-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="79e7b-148">Get-AzureRmLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="79e7b-149">Nowe — AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="79e7b-149">New-AzureRmLoadBalancerInboundNatPoolConfig</span></span>](./New-AzureRmLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="79e7b-150">Remove-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="79e7b-150">Remove-AzureRmLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatPoolConfig.md)


