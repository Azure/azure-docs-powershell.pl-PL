---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F421174A-B138-45EB-AF84-CB3CE5870F27
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerbackendaddresspoolconfig
schema: 2.0.0
ms.openlocfilehash: 4bfae8947661f21441d67d6d82dbc8751f3128d2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898365"
---
# <span data-ttu-id="788ea-101">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="788ea-101">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="788ea-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="788ea-102">SYNOPSIS</span></span>
<span data-ttu-id="788ea-103">Pobiera konfigurację puli adresów zaplecza modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="788ea-103">Gets a backend address pool configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="788ea-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="788ea-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerBackendAddressPoolConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="788ea-105">Opis</span><span class="sxs-lookup"><span data-stu-id="788ea-105">DESCRIPTION</span></span>
<span data-ttu-id="788ea-106">Polecenie cmdlet **Get-AzureRmLoadBalancerBackendAddressPoolConfig** pobiera pojedynczą pulę adresów zaplecza lub listę pul adresów zaplecza w ramach modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="788ea-106">The **Get-AzureRmLoadBalancerBackendAddressPoolConfig** cmdlet gets a single backend address pool or a list of backend address pools within a load balancer.</span></span>

## <span data-ttu-id="788ea-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="788ea-107">EXAMPLES</span></span>

### <span data-ttu-id="788ea-108">Przykład 1: pobieranie puli adresów zaplecza</span><span class="sxs-lookup"><span data-stu-id="788ea-108">Example 1: Get the backend address pool</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" -LoadBalancer $loadbalancer
```

<span data-ttu-id="788ea-109">Pierwsze polecenie uzyskuje istniejące Równoważenie obciążenia o nazwie MyLoadBalancer w grupie zasób o nazwie moja grupa, a następnie zapisuje je w zmiennej $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="788ea-109">The first command gets an existing load balancer named MyLoadBalancer in the resource group named MyResourceGroup, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="788ea-110">Drugie polecenie pobiera skojarzoną konfigurację puli adresów zaplecza o nazwie BackendAddressPool02 dla modułu równoważenia obciążenia w $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="788ea-110">The second command gets the associated backend address pool configuration named BackendAddressPool02 for the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="788ea-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="788ea-111">PARAMETERS</span></span>

### <span data-ttu-id="788ea-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="788ea-112">-DefaultProfile</span></span>
<span data-ttu-id="788ea-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="788ea-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="788ea-114">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="788ea-114">-LoadBalancer</span></span>
<span data-ttu-id="788ea-115">Określa moduł równoważenia obciążenia skojarzony z pulą adresów zaplecza, aby uzyskać dostęp.</span><span class="sxs-lookup"><span data-stu-id="788ea-115">Specifies the load balancer that is associated with the backend address pool to get.</span></span>

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

### <span data-ttu-id="788ea-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="788ea-116">-Name</span></span>
<span data-ttu-id="788ea-117">Określa nazwę modułu równoważenia obciążenia zawierającego pulę adresów zaplecza, która ma zostać pozyskana.</span><span class="sxs-lookup"><span data-stu-id="788ea-117">Specifies the name of the load balancer that contains the backend address pool to get.</span></span>

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

### <span data-ttu-id="788ea-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="788ea-118">CommonParameters</span></span>
<span data-ttu-id="788ea-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="788ea-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="788ea-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="788ea-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="788ea-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="788ea-121">INPUTS</span></span>

### <span data-ttu-id="788ea-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="788ea-122">PSLoadBalancer</span></span>
<span data-ttu-id="788ea-123">Parametr "równoważenia obciążenia" akceptuje wartość typu "PSLoadBalancer" z procesu</span><span class="sxs-lookup"><span data-stu-id="788ea-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="788ea-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="788ea-124">OUTPUTS</span></span>

### <span data-ttu-id="788ea-125">Microsoft. Azure. Commands. Network. models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="788ea-125">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="788ea-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="788ea-126">NOTES</span></span>

## <span data-ttu-id="788ea-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="788ea-127">RELATED LINKS</span></span>

[<span data-ttu-id="788ea-128">Dodaj-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="788ea-128">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="788ea-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="788ea-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="788ea-130">Nowe — AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="788ea-130">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="788ea-131">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="788ea-131">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md)


