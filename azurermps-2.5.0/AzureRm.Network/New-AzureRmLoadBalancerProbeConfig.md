---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2049CB74-E3CB-4294-B97C-B41E91209A1E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerprobeconfig
schema: 2.0.0
ms.openlocfilehash: f1d5ac87cc237e5a8ec92262255e996741346613
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899250"
---
# <span data-ttu-id="40209-101">New-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="40209-101">New-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="40209-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="40209-102">SYNOPSIS</span></span>
<span data-ttu-id="40209-103">Umożliwia utworzenie konfiguracji sondy dla modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="40209-103">Creates a probe configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40209-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="40209-104">SYNTAX</span></span>

```
New-AzureRmLoadBalancerProbeConfig -Name <String> [-RequestPath <String>] [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40209-105">Opis</span><span class="sxs-lookup"><span data-stu-id="40209-105">DESCRIPTION</span></span>
<span data-ttu-id="40209-106">Polecenie cmdlet **New-AzureRmLoadBalancerProbeConfig** umożliwia utworzenie konfiguracji sondy modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="40209-106">The **New-AzureRmLoadBalancerProbeConfig** cmdlet creates a probe configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="40209-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="40209-107">EXAMPLES</span></span>

### <span data-ttu-id="40209-108">Przykład 1. Tworzenie konfiguracji sondy</span><span class="sxs-lookup"><span data-stu-id="40209-108">Example 1: Create a probe configuration</span></span>
```
PS C:\>New-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 15
```

<span data-ttu-id="40209-109">To polecenie umożliwia utworzenie konfiguracji sondy o nazwie Moja sonda przy użyciu protokołu HTTP.</span><span class="sxs-lookup"><span data-stu-id="40209-109">This command creates a probe configuration named MyProbe using the HTTP protocol.</span></span>
<span data-ttu-id="40209-110">Nowa sonda połączy się z usługą równoważenia obciążenia na porcie 80.</span><span class="sxs-lookup"><span data-stu-id="40209-110">The new probe will connect to a load-balanced service on port 80.</span></span>

## <span data-ttu-id="40209-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="40209-111">PARAMETERS</span></span>

### <span data-ttu-id="40209-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40209-112">-DefaultProfile</span></span>
<span data-ttu-id="40209-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="40209-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40209-114">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="40209-114">-IntervalInSeconds</span></span>
<span data-ttu-id="40209-115">Określa interwał (w sekundach) między sondami dla każdego wystąpienia usługi równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="40209-115">Specifies the interval, in seconds, between probes to each instance of a load-balanced service.</span></span>

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

### <span data-ttu-id="40209-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="40209-116">-Name</span></span>
<span data-ttu-id="40209-117">Określa nazwę konfiguracji sondy, którą należy utworzyć.</span><span class="sxs-lookup"><span data-stu-id="40209-117">Specifies the name of the probe configuration to create.</span></span>

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

### <span data-ttu-id="40209-118">-Port</span><span class="sxs-lookup"><span data-stu-id="40209-118">-Port</span></span>
<span data-ttu-id="40209-119">Określa port, na którym nowe sondy powinny łączyć się z usługą równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="40209-119">Specifies the port on which the new probe should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="40209-120">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="40209-120">-ProbeCount</span></span>
<span data-ttu-id="40209-121">Określa liczbę kolejnych awarii dla wystąpienia, które można uznać za niezdrowe.</span><span class="sxs-lookup"><span data-stu-id="40209-121">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="40209-122">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="40209-122">-Protocol</span></span>
<span data-ttu-id="40209-123">Określa protokół, który ma być używany do konfiguracji sondy.</span><span class="sxs-lookup"><span data-stu-id="40209-123">Specifies the protocol to use for the probe configuration.</span></span>
<span data-ttu-id="40209-124">Dopuszczalne wartości tego parametru to: TCP lub http.</span><span class="sxs-lookup"><span data-stu-id="40209-124">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="40209-125">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="40209-125">-RequestPath</span></span>
<span data-ttu-id="40209-126">Określa ścieżkę w usłudze równoważenia obciążenia do sondowania w celu określenia kondycji.</span><span class="sxs-lookup"><span data-stu-id="40209-126">Specifies the path in a load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="40209-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40209-127">CommonParameters</span></span>
<span data-ttu-id="40209-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40209-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40209-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40209-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40209-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="40209-130">INPUTS</span></span>

## <span data-ttu-id="40209-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="40209-131">OUTPUTS</span></span>

### <span data-ttu-id="40209-132">Microsoft. Azure. Commands. Network. models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="40209-132">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="40209-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="40209-133">NOTES</span></span>

## <span data-ttu-id="40209-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="40209-134">RELATED LINKS</span></span>

[<span data-ttu-id="40209-135">Dodaj-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="40209-135">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="40209-136">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="40209-136">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="40209-137">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="40209-137">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="40209-138">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="40209-138">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


