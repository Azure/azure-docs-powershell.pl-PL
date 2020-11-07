---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 278228EB-0126-4F27-A30F-51DC498C65FE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: 3d8d80f8f8de0c1a0dedd50e7f4c6a93ce414b48
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717732"
---
# <span data-ttu-id="ad8af-101">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ad8af-101">Get-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="ad8af-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ad8af-102">SYNOPSIS</span></span>
<span data-ttu-id="ad8af-103">Pobiera konfigurację sondy dla modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="ad8af-103">Gets a probe configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad8af-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ad8af-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerProbeConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad8af-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ad8af-105">DESCRIPTION</span></span>
<span data-ttu-id="ad8af-106">Polecenie cmdlet **Get-AzureRmLoadBalancerProbeConfig** umożliwia pobranie co najmniej jednej konfiguracji sondy modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="ad8af-106">The **Get-AzureRmLoadBalancerProbeConfig** cmdlet gets one or more probe configurations for a load balancer.</span></span>

## <span data-ttu-id="ad8af-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ad8af-107">EXAMPLES</span></span>

### <span data-ttu-id="ad8af-108">Przykład 1: Uzyskiwanie konfiguracji sondy modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="ad8af-108">Example 1: Get the probe configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $slb
```

<span data-ttu-id="ad8af-109">Pierwsze polecenie uzyskuje usługę równoważenia obciążenia o nazwie MyLoadBalancer, a następnie zapisuje ją w zmiennej $slb.</span><span class="sxs-lookup"><span data-stu-id="ad8af-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="ad8af-110">Drugie polecenie pobiera skojarzoną konfigurację sondy o nazwie Moja Sonda z modułu równoważenia obciążenia w $slb.</span><span class="sxs-lookup"><span data-stu-id="ad8af-110">The second command gets the associated probe configuration named MyProbe from the load balancer in $slb.</span></span>

## <span data-ttu-id="ad8af-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ad8af-111">PARAMETERS</span></span>

### <span data-ttu-id="ad8af-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad8af-112">-DefaultProfile</span></span>
<span data-ttu-id="ad8af-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ad8af-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad8af-114">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="ad8af-114">-LoadBalancer</span></span>
<span data-ttu-id="ad8af-115">Określa moduł równoważenia obciążenia skojarzony z konfiguracją sondy do pobrania.</span><span class="sxs-lookup"><span data-stu-id="ad8af-115">Specifies the load balancer that is associated with the probe configuration to get.</span></span>

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

### <span data-ttu-id="ad8af-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ad8af-116">-Name</span></span>
<span data-ttu-id="ad8af-117">Określa nazwę konfiguracji sondy, którą należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="ad8af-117">Specifies the name of the probe configuration to get.</span></span>

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

### <span data-ttu-id="ad8af-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad8af-118">CommonParameters</span></span>
<span data-ttu-id="ad8af-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad8af-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad8af-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad8af-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad8af-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ad8af-121">INPUTS</span></span>

### <span data-ttu-id="ad8af-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ad8af-122">PSLoadBalancer</span></span>
<span data-ttu-id="ad8af-123">Parametr "równoważenia obciążenia" akceptuje wartość typu "PSLoadBalancer" z procesu</span><span class="sxs-lookup"><span data-stu-id="ad8af-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="ad8af-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ad8af-124">OUTPUTS</span></span>

### <span data-ttu-id="ad8af-125">Microsoft. Azure. Commands. Network. models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="ad8af-125">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="ad8af-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ad8af-126">NOTES</span></span>

## <span data-ttu-id="ad8af-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ad8af-127">RELATED LINKS</span></span>

[<span data-ttu-id="ad8af-128">Dodaj-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ad8af-128">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="ad8af-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ad8af-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="ad8af-130">Nowe — AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ad8af-130">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="ad8af-131">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ad8af-131">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="ad8af-132">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ad8af-132">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)

