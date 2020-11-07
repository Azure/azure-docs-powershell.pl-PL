---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2049CB74-E3CB-4294-B97C-B41E91209A1E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 6e647cbc20e74c5c473fe91b2ec592177c0713ba
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890478"
---
# <span data-ttu-id="89dec-101">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="89dec-101">New-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="89dec-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="89dec-102">SYNOPSIS</span></span>
<span data-ttu-id="89dec-103">Umożliwia utworzenie konfiguracji sondy dla modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="89dec-103">Creates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="89dec-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="89dec-104">SYNTAX</span></span>

```
New-AzLoadBalancerProbeConfig -Name <String> [-RequestPath <String>] [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89dec-105">Opis</span><span class="sxs-lookup"><span data-stu-id="89dec-105">DESCRIPTION</span></span>
<span data-ttu-id="89dec-106">Polecenie cmdlet **New-AzLoadBalancerProbeConfig** umożliwia utworzenie konfiguracji sondy modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="89dec-106">The **New-AzLoadBalancerProbeConfig** cmdlet creates a probe configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="89dec-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="89dec-107">EXAMPLES</span></span>

### <span data-ttu-id="89dec-108">Przykład 1. Tworzenie konfiguracji sondy</span><span class="sxs-lookup"><span data-stu-id="89dec-108">Example 1: Create a probe configuration</span></span>
```
PS C:\>New-AzLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 15
```

<span data-ttu-id="89dec-109">To polecenie umożliwia utworzenie konfiguracji sondy o nazwie Moja sonda przy użyciu protokołu HTTP.</span><span class="sxs-lookup"><span data-stu-id="89dec-109">This command creates a probe configuration named MyProbe using the HTTP protocol.</span></span>
<span data-ttu-id="89dec-110">Nowa sonda połączy się z usługą równoważenia obciążenia na porcie 80.</span><span class="sxs-lookup"><span data-stu-id="89dec-110">The new probe will connect to a load-balanced service on port 80.</span></span>

## <span data-ttu-id="89dec-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="89dec-111">PARAMETERS</span></span>

### <span data-ttu-id="89dec-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89dec-112">-DefaultProfile</span></span>
<span data-ttu-id="89dec-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="89dec-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89dec-114">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="89dec-114">-IntervalInSeconds</span></span>
<span data-ttu-id="89dec-115">Określa interwał (w sekundach) między sondami dla każdego wystąpienia usługi równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="89dec-115">Specifies the interval, in seconds, between probes to each instance of a load-balanced service.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89dec-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="89dec-116">-Name</span></span>
<span data-ttu-id="89dec-117">Określa nazwę konfiguracji sondy, którą należy utworzyć.</span><span class="sxs-lookup"><span data-stu-id="89dec-117">Specifies the name of the probe configuration to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89dec-118">-Port</span><span class="sxs-lookup"><span data-stu-id="89dec-118">-Port</span></span>
<span data-ttu-id="89dec-119">Określa port, na którym nowe sondy powinny łączyć się z usługą równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="89dec-119">Specifies the port on which the new probe should connect to a load-balanced service.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89dec-120">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="89dec-120">-ProbeCount</span></span>
<span data-ttu-id="89dec-121">Określa liczbę kolejnych awarii dla wystąpienia, które można uznać za niezdrowe.</span><span class="sxs-lookup"><span data-stu-id="89dec-121">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89dec-122">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="89dec-122">-Protocol</span></span>
<span data-ttu-id="89dec-123">Określa protokół, który ma być używany do konfiguracji sondy.</span><span class="sxs-lookup"><span data-stu-id="89dec-123">Specifies the protocol to use for the probe configuration.</span></span>
<span data-ttu-id="89dec-124">Dopuszczalne wartości tego parametru to: TCP lub http.</span><span class="sxs-lookup"><span data-stu-id="89dec-124">The acceptable values for this parameter are: Tcp or Http.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Http

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89dec-125">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="89dec-125">-RequestPath</span></span>
<span data-ttu-id="89dec-126">Określa ścieżkę w usłudze równoważenia obciążenia do sondowania w celu określenia kondycji.</span><span class="sxs-lookup"><span data-stu-id="89dec-126">Specifies the path in a load-balanced service to probe to determine health.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89dec-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89dec-127">CommonParameters</span></span>
<span data-ttu-id="89dec-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89dec-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89dec-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89dec-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89dec-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="89dec-130">INPUTS</span></span>

## <span data-ttu-id="89dec-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="89dec-131">OUTPUTS</span></span>

### <span data-ttu-id="89dec-132">Microsoft. Azure. Commands. Network. models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="89dec-132">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="89dec-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="89dec-133">NOTES</span></span>

## <span data-ttu-id="89dec-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="89dec-134">RELATED LINKS</span></span>

[<span data-ttu-id="89dec-135">Dodaj-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="89dec-135">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="89dec-136">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="89dec-136">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="89dec-137">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="89dec-137">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="89dec-138">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="89dec-138">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


