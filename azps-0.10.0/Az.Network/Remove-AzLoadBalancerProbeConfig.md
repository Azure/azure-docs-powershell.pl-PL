---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B15B224-E36C-454B-B6C2-F2BE032AE962
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 11de4e8966b5e57e817b6c5d829536deacf229f8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890289"
---
# <span data-ttu-id="e651f-101">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e651f-101">Remove-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="e651f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e651f-102">SYNOPSIS</span></span>
<span data-ttu-id="e651f-103">Umożliwia usunięcie konfiguracji sondy z modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="e651f-103">Removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="e651f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e651f-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerProbeConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e651f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e651f-105">DESCRIPTION</span></span>
<span data-ttu-id="e651f-106">Polecenie cmdlet **Remove-AzLoadBalancerProbeConfig** umożliwia usunięcie konfiguracji sondy z modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="e651f-106">The **Remove-AzLoadBalancerProbeConfig** cmdlet removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="e651f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e651f-107">EXAMPLES</span></span>

### <span data-ttu-id="e651f-108">Przykład 1: Usuwanie konfiguracji sondy z modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="e651f-108">Example 1: Remove a probe configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $loadbalancer
```

<span data-ttu-id="e651f-109">Pierwsze polecenie uzyskuje usługę równoważenia obciążenia o nazwie MyLoadBalancer, a następnie zapisuje ją w zmiennej $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="e651f-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="e651f-110">Drugie polecenie usuwa konfigurację o nazwie Moja Sonda z modułu równoważenia obciążenia w $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="e651f-110">The second command deletes the configuration named MyProbe from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="e651f-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e651f-111">PARAMETERS</span></span>

### <span data-ttu-id="e651f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e651f-112">-DefaultProfile</span></span>
<span data-ttu-id="e651f-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e651f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e651f-114">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="e651f-114">-LoadBalancer</span></span>
<span data-ttu-id="e651f-115">Umożliwia określenie modułu równoważenia obciążenia zawierającego konfigurację sondy, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e651f-115">Specifies the load balancer that contains the probe configuration that this cmdlet removes.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e651f-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e651f-116">-Name</span></span>
<span data-ttu-id="e651f-117">Określa nazwę konfiguracji sondy, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e651f-117">Specifies the name of the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e651f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e651f-118">CommonParameters</span></span>
<span data-ttu-id="e651f-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e651f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e651f-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e651f-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e651f-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e651f-121">INPUTS</span></span>

### <span data-ttu-id="e651f-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e651f-122">PSLoadBalancer</span></span>
<span data-ttu-id="e651f-123">Parametr "równoważenia obciążenia" akceptuje wartość typu "PSLoadBalancer" z procesu</span><span class="sxs-lookup"><span data-stu-id="e651f-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="e651f-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e651f-124">OUTPUTS</span></span>

### <span data-ttu-id="e651f-125">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e651f-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="e651f-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e651f-126">NOTES</span></span>

## <span data-ttu-id="e651f-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e651f-127">RELATED LINKS</span></span>

[<span data-ttu-id="e651f-128">Dodaj-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e651f-128">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="e651f-129">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e651f-129">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="e651f-130">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e651f-130">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="e651f-131">Nowe — AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e651f-131">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="e651f-132">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e651f-132">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


