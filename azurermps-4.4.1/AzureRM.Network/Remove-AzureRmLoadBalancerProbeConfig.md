---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2B15B224-E36C-454B-B6C2-F2BE032AE962
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: 132ec5259a6d03591860dceaaa215f8db57c27dd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716525"
---
# <span data-ttu-id="7ea8e-101">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7ea8e-101">Remove-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="7ea8e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7ea8e-102">SYNOPSIS</span></span>
<span data-ttu-id="7ea8e-103">Umożliwia usunięcie konfiguracji sondy z modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="7ea8e-103">Removes a probe configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ea8e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7ea8e-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerProbeConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ea8e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7ea8e-105">DESCRIPTION</span></span>
<span data-ttu-id="7ea8e-106">Polecenie cmdlet **Remove-AzureRmLoadBalancerProbeConfig** umożliwia usunięcie konfiguracji sondy z modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="7ea8e-106">The **Remove-AzureRmLoadBalancerProbeConfig** cmdlet removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="7ea8e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7ea8e-107">EXAMPLES</span></span>

### <span data-ttu-id="7ea8e-108">Przykład 1: Usuwanie konfiguracji sondy z modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="7ea8e-108">Example 1: Remove a probe configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $loadbalancer
```

<span data-ttu-id="7ea8e-109">Pierwsze polecenie uzyskuje usługę równoważenia obciążenia o nazwie MyLoadBalancer, a następnie zapisuje ją w zmiennej $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="7ea8e-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="7ea8e-110">Drugie polecenie usuwa konfigurację o nazwie Moja Sonda z modułu równoważenia obciążenia w $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="7ea8e-110">The second command deletes the configuration named MyProbe from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="7ea8e-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7ea8e-111">PARAMETERS</span></span>

### <span data-ttu-id="7ea8e-112">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="7ea8e-112">-LoadBalancer</span></span>
<span data-ttu-id="7ea8e-113">Umożliwia określenie modułu równoważenia obciążenia zawierającego konfigurację sondy, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ea8e-113">Specifies the load balancer that contains the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7ea8e-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7ea8e-114">-Name</span></span>
<span data-ttu-id="7ea8e-115">Określa nazwę konfiguracji sondy, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ea8e-115">Specifies the name of the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7ea8e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ea8e-116">-DefaultProfile</span></span>
<span data-ttu-id="7ea8e-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7ea8e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ea8e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ea8e-118">CommonParameters</span></span>
<span data-ttu-id="7ea8e-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ea8e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ea8e-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ea8e-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ea8e-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7ea8e-121">INPUTS</span></span>

### <span data-ttu-id="7ea8e-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7ea8e-122">PSLoadBalancer</span></span>
<span data-ttu-id="7ea8e-123">Parametr "równoważenia obciążenia" akceptuje wartość typu "PSLoadBalancer" z procesu</span><span class="sxs-lookup"><span data-stu-id="7ea8e-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="7ea8e-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7ea8e-124">OUTPUTS</span></span>

### <span data-ttu-id="7ea8e-125">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7ea8e-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="7ea8e-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7ea8e-126">NOTES</span></span>

## <span data-ttu-id="7ea8e-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7ea8e-127">RELATED LINKS</span></span>

[<span data-ttu-id="7ea8e-128">Dodaj-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7ea8e-128">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="7ea8e-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7ea8e-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="7ea8e-130">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7ea8e-130">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="7ea8e-131">Nowe — AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7ea8e-131">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="7ea8e-132">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7ea8e-132">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


