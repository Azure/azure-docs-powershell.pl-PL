---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6F9BAB0B-7DC7-4672-B2B5-8B139D652DDD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: 79e9d856825e174bc8667f99e7b25b301230dec3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549967"
---
# <span data-ttu-id="04ad3-101">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="04ad3-101">Add-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="04ad3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="04ad3-102">SYNOPSIS</span></span>
<span data-ttu-id="04ad3-103">Umożliwia dodanie konfiguracji sondy do modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="04ad3-103">Adds a probe configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04ad3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="04ad3-104">SYNTAX</span></span>

```
Add-AzureRmLoadBalancerProbeConfig -Name <String> -LoadBalancer <PSLoadBalancer> [-RequestPath <String>]
 [-Protocol <String>] -Port <Int32> -IntervalInSeconds <Int32> -ProbeCount <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04ad3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="04ad3-105">DESCRIPTION</span></span>
<span data-ttu-id="04ad3-106">Polecenie cmdlet **Add-AzureRmLoadBalancerProbeConfig** umożliwia dodanie konfiguracji sondy do modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="04ad3-106">The **Add-AzureRmLoadBalancerProbeConfig** cmdlet adds a probe configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="04ad3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="04ad3-107">EXAMPLES</span></span>

### <span data-ttu-id="04ad3-108">Przykład 1 Dodawanie konfiguracji sondy do modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="04ad3-108">Example 1 Add a probe configuration to a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "myLb" -ResourceGroupName "myRg" | Add-AzureRmLoadBalancerProbeConfig -Name "probeName" -RequestPath healthcheck2.aspx -Protocol http -Port 81 -IntervalInSeconds 16 -ProbeCount 3 | Set-AzureRmLoadBalancer
```

<span data-ttu-id="04ad3-109">To polecenie uzyskuje usługę równoważenia obciążenia o nazwie myLb, dodaje do niej określoną konfigurację sondy, a następnie używa polecenia cmdlet **Set-AzureRmLoadBalancer** w celu zaktualizowania modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="04ad3-109">This command gets the load balancer named myLb, adds the specified probe configuration to it, and then uses the **Set-AzureRmLoadBalancer** cmdlet to update the load balancer.</span></span>

## <span data-ttu-id="04ad3-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="04ad3-110">PARAMETERS</span></span>

### <span data-ttu-id="04ad3-111">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="04ad3-111">-IntervalInSeconds</span></span>
<span data-ttu-id="04ad3-112">Określa interwał (w sekundach) między sondami dla każdego wystąpienia usługi równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="04ad3-112">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04ad3-113">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="04ad3-113">-LoadBalancer</span></span>
<span data-ttu-id="04ad3-114">Określa obiekt **modułu równoważenia obciążenia** .</span><span class="sxs-lookup"><span data-stu-id="04ad3-114">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="04ad3-115">To polecenie cmdlet umożliwia dodanie konfiguracji sondy do modułu równoważenia obciążenia, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="04ad3-115">This cmdlet adds a probe configuration to the load balancer that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="04ad3-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="04ad3-116">-Name</span></span>
<span data-ttu-id="04ad3-117">Określa nazwę konfiguracji sondy, którą należy dodać.</span><span class="sxs-lookup"><span data-stu-id="04ad3-117">Specifies the name of the probe configuration to add.</span></span>

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

### <span data-ttu-id="04ad3-118">-Port</span><span class="sxs-lookup"><span data-stu-id="04ad3-118">-Port</span></span>
<span data-ttu-id="04ad3-119">Określa port, na którym sondy powinny być połączone z usługą równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="04ad3-119">Specifies the port on which probes should connect to a load-balanced service.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04ad3-120">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="04ad3-120">-ProbeCount</span></span>
<span data-ttu-id="04ad3-121">Określa liczbę kolejnych awarii dla wystąpienia, które można uznać za niezdrowe.</span><span class="sxs-lookup"><span data-stu-id="04ad3-121">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04ad3-122">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="04ad3-122">-Protocol</span></span>
<span data-ttu-id="04ad3-123">Określa protokół, który ma być używany do badania.</span><span class="sxs-lookup"><span data-stu-id="04ad3-123">Specifies the protocol to use for the probe.</span></span>
<span data-ttu-id="04ad3-124">Dopuszczalne wartości tego parametru to: TCP lub http.</span><span class="sxs-lookup"><span data-stu-id="04ad3-124">The acceptable values for this parameter are: Tcp or Http.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Http

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04ad3-125">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="04ad3-125">-RequestPath</span></span>
<span data-ttu-id="04ad3-126">Określa ścieżkę w usłudze równoważenia obciążenia do sondowania w celu określenia kondycji.</span><span class="sxs-lookup"><span data-stu-id="04ad3-126">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="04ad3-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04ad3-127">-DefaultProfile</span></span>
<span data-ttu-id="04ad3-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="04ad3-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04ad3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04ad3-129">CommonParameters</span></span>
<span data-ttu-id="04ad3-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04ad3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04ad3-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04ad3-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04ad3-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="04ad3-132">INPUTS</span></span>

### <span data-ttu-id="04ad3-133">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="04ad3-133">PSLoadBalancer</span></span>
<span data-ttu-id="04ad3-134">Parametr "równoważenia obciążenia" akceptuje wartość typu "PSLoadBalancer" z procesu</span><span class="sxs-lookup"><span data-stu-id="04ad3-134">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="04ad3-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="04ad3-135">OUTPUTS</span></span>

### <span data-ttu-id="04ad3-136">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="04ad3-136">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="04ad3-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="04ad3-137">NOTES</span></span>

## <span data-ttu-id="04ad3-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="04ad3-138">RELATED LINKS</span></span>

[<span data-ttu-id="04ad3-139">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="04ad3-139">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="04ad3-140">Nowe — AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="04ad3-140">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="04ad3-141">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="04ad3-141">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="04ad3-142">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="04ad3-142">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)

[<span data-ttu-id="04ad3-143">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="04ad3-143">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


