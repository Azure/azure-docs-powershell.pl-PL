---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2049CB74-E3CB-4294-B97C-B41E91209A1E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: 8a4889190e58edd896d1a93222a35688dd5884c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545056"
---
# <span data-ttu-id="11ede-101">New-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="11ede-101">New-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="11ede-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="11ede-102">SYNOPSIS</span></span>
<span data-ttu-id="11ede-103">Umożliwia utworzenie konfiguracji sondy dla modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="11ede-103">Creates a probe configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11ede-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="11ede-104">SYNTAX</span></span>

```
New-AzureRmLoadBalancerProbeConfig -Name <String> [-Protocol <String>] -Port <Int32> -IntervalInSeconds <Int32>
 -ProbeCount <Int32> [-RequestPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="11ede-105">Opis</span><span class="sxs-lookup"><span data-stu-id="11ede-105">DESCRIPTION</span></span>
<span data-ttu-id="11ede-106">Polecenie cmdlet **New-AzureRmLoadBalancerProbeConfig** umożliwia utworzenie konfiguracji sondy modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="11ede-106">The **New-AzureRmLoadBalancerProbeConfig** cmdlet creates a probe configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="11ede-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="11ede-107">EXAMPLES</span></span>

### <span data-ttu-id="11ede-108">Przykład 1. Tworzenie konfiguracji sondy</span><span class="sxs-lookup"><span data-stu-id="11ede-108">Example 1: Create a probe configuration</span></span>
```
PS C:\>New-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 15
```

<span data-ttu-id="11ede-109">To polecenie umożliwia utworzenie konfiguracji sondy o nazwie Moja sonda przy użyciu protokołu HTTP.</span><span class="sxs-lookup"><span data-stu-id="11ede-109">This command creates a probe configuration named MyProbe using the HTTP protocol.</span></span>
<span data-ttu-id="11ede-110">Nowa sonda połączy się z usługą równoważenia obciążenia na porcie 80.</span><span class="sxs-lookup"><span data-stu-id="11ede-110">The new probe will connect to a load-balanced service on port 80.</span></span>

## <span data-ttu-id="11ede-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="11ede-111">PARAMETERS</span></span>

### <span data-ttu-id="11ede-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11ede-112">-DefaultProfile</span></span>
<span data-ttu-id="11ede-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="11ede-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11ede-114">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="11ede-114">-IntervalInSeconds</span></span>
<span data-ttu-id="11ede-115">Określa interwał (w sekundach) między sondami dla każdego wystąpienia usługi równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="11ede-115">Specifies the interval, in seconds, between probes to each instance of a load-balanced service.</span></span>

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

### <span data-ttu-id="11ede-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="11ede-116">-Name</span></span>
<span data-ttu-id="11ede-117">Określa nazwę konfiguracji sondy, którą należy utworzyć.</span><span class="sxs-lookup"><span data-stu-id="11ede-117">Specifies the name of the probe configuration to create.</span></span>

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

### <span data-ttu-id="11ede-118">-Port</span><span class="sxs-lookup"><span data-stu-id="11ede-118">-Port</span></span>
<span data-ttu-id="11ede-119">Określa port, na którym nowe sondy powinny łączyć się z usługą równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="11ede-119">Specifies the port on which the new probe should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="11ede-120">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="11ede-120">-ProbeCount</span></span>
<span data-ttu-id="11ede-121">Określa liczbę kolejnych awarii dla wystąpienia, które można uznać za niezdrowe.</span><span class="sxs-lookup"><span data-stu-id="11ede-121">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="11ede-122">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="11ede-122">-Protocol</span></span>
<span data-ttu-id="11ede-123">Określa protokół, który ma być używany do konfiguracji sondy.</span><span class="sxs-lookup"><span data-stu-id="11ede-123">Specifies the protocol to use for the probe configuration.</span></span>
<span data-ttu-id="11ede-124">Dopuszczalne wartości tego parametru to: TCP lub http.</span><span class="sxs-lookup"><span data-stu-id="11ede-124">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="11ede-125">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="11ede-125">-RequestPath</span></span>
<span data-ttu-id="11ede-126">Określa ścieżkę w usłudze równoważenia obciążenia do sondowania w celu określenia kondycji.</span><span class="sxs-lookup"><span data-stu-id="11ede-126">Specifies the path in a load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="11ede-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="11ede-127">-Confirm</span></span>
<span data-ttu-id="11ede-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11ede-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11ede-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11ede-129">-WhatIf</span></span>
<span data-ttu-id="11ede-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11ede-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="11ede-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="11ede-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11ede-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11ede-132">CommonParameters</span></span>
<span data-ttu-id="11ede-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11ede-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11ede-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11ede-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11ede-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11ede-135">INPUTS</span></span>

### <span data-ttu-id="11ede-136">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="11ede-136">None</span></span>

## <span data-ttu-id="11ede-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="11ede-137">OUTPUTS</span></span>

### <span data-ttu-id="11ede-138">Microsoft. Azure. Commands. Network. models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="11ede-138">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="11ede-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="11ede-139">NOTES</span></span>

## <span data-ttu-id="11ede-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="11ede-140">RELATED LINKS</span></span>

[<span data-ttu-id="11ede-141">Dodaj-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="11ede-141">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="11ede-142">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="11ede-142">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="11ede-143">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="11ede-143">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="11ede-144">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="11ede-144">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


