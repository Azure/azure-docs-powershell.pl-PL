---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9EB11283-0189-4333-8142-DCC3F770F91A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: e97e8f3ed5769e4f81175b29f097aa4946d28881
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890989"
---
# <span data-ttu-id="46a20-101">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="46a20-101">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="46a20-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="46a20-102">SYNOPSIS</span></span>
<span data-ttu-id="46a20-103">Umożliwia dodanie konfiguracji puli adresów zaplecza do modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="46a20-103">Adds a backend address pool configuration to a load balancer.</span></span>

## <span data-ttu-id="46a20-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="46a20-104">SYNTAX</span></span>

```
Add-AzLoadBalancerBackendAddressPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46a20-105">Opis</span><span class="sxs-lookup"><span data-stu-id="46a20-105">DESCRIPTION</span></span>
<span data-ttu-id="46a20-106">Polecenie cmdlet **Add-AzLoadBalancerBackend** umożliwia dodanie puli adresów zaplecza do modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="46a20-106">The **Add-AzLoadBalancerBackend** cmdlet adds a backend address pool to an Azure load balancer.</span></span>

## <span data-ttu-id="46a20-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="46a20-107">EXAMPLES</span></span>

### <span data-ttu-id="46a20-108">Przykład 1 Dodawanie konfiguracji puli adresów zaplecza do modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="46a20-108">Example 1 Add a backend address pool configuration to a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myrg" | Add-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

<span data-ttu-id="46a20-109">To polecenie uzyskuje usługę równoważenia obciążenia o nazwie MyLoadBalancer, dodaje pulę adresów zaplecza o nazwie BackendAddressPool02 do MyLoadBalancer, a następnie używa polecenia cmdlet **Set-AzLoadBalancer** w celu zaktualizowania MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="46a20-109">This command gets the load balancer named MyLoadBalancer, adds the backend address pool named BackendAddressPool02 to MyLoadBalancer, and then uses the **Set-AzLoadBalancer** cmdlet to update MyLoadBalancer.</span></span>

## <span data-ttu-id="46a20-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="46a20-110">PARAMETERS</span></span>

### <span data-ttu-id="46a20-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46a20-111">-DefaultProfile</span></span>
<span data-ttu-id="46a20-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="46a20-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46a20-113">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="46a20-113">-LoadBalancer</span></span>
<span data-ttu-id="46a20-114">Określa obiekt **modułu równoważenia obciążenia** .</span><span class="sxs-lookup"><span data-stu-id="46a20-114">Specifies a **LoadBalancer** object.</span></span>

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

### <span data-ttu-id="46a20-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="46a20-115">-Name</span></span>
<span data-ttu-id="46a20-116">Określa nazwę konfiguracji puli adresów zaplecza, która ma zostać dodana.</span><span class="sxs-lookup"><span data-stu-id="46a20-116">Specifies the name of the backend address pool configuration to add.</span></span>

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

### <span data-ttu-id="46a20-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46a20-117">CommonParameters</span></span>
<span data-ttu-id="46a20-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46a20-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46a20-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46a20-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46a20-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="46a20-120">INPUTS</span></span>

### <span data-ttu-id="46a20-121">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="46a20-121">PSLoadBalancer</span></span>
<span data-ttu-id="46a20-122">Parametr "równoważenia obciążenia" akceptuje wartość typu "PSLoadBalancer" z procesu</span><span class="sxs-lookup"><span data-stu-id="46a20-122">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="46a20-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="46a20-123">OUTPUTS</span></span>

### <span data-ttu-id="46a20-124">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="46a20-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="46a20-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="46a20-125">NOTES</span></span>

## <span data-ttu-id="46a20-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="46a20-126">RELATED LINKS</span></span>

[<span data-ttu-id="46a20-127">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="46a20-127">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="46a20-128">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="46a20-128">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="46a20-129">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="46a20-129">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="46a20-130">Nowe — AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="46a20-130">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="46a20-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="46a20-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


