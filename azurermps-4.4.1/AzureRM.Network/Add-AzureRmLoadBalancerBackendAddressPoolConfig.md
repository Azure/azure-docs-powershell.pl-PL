---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9EB11283-0189-4333-8142-DCC3F770F91A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: ef5071ff0127c34d9ae8c41ea12e2465e83c98d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717829"
---
# <span data-ttu-id="3d894-101">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="3d894-101">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="3d894-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3d894-102">SYNOPSIS</span></span>
<span data-ttu-id="3d894-103">Umożliwia dodanie konfiguracji puli adresów zaplecza do modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="3d894-103">Adds a backend address pool configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d894-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3d894-104">SYNTAX</span></span>

```
Add-AzureRmLoadBalancerBackendAddressPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d894-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3d894-105">DESCRIPTION</span></span>
<span data-ttu-id="3d894-106">Polecenie cmdlet **Add-AzureRmLoadBalancerBackend** umożliwia dodanie puli adresów zaplecza do modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3d894-106">The **Add-AzureRmLoadBalancerBackend** cmdlet adds a backend address pool to an Azure load balancer.</span></span>

## <span data-ttu-id="3d894-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3d894-107">EXAMPLES</span></span>

### <span data-ttu-id="3d894-108">Przykład 1 Dodawanie konfiguracji puli adresów zaplecza do modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="3d894-108">Example 1 Add a backend address pool configuration to a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myrg" | Add-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzureRmLoadBalancer
```

<span data-ttu-id="3d894-109">To polecenie uzyskuje usługę równoważenia obciążenia o nazwie MyLoadBalancer, dodaje pulę adresów zaplecza o nazwie BackendAddressPool02 do MyLoadBalancer, a następnie używa polecenia cmdlet **Set-AzureRmLoadBalancer** w celu zaktualizowania MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="3d894-109">This command gets the load balancer named MyLoadBalancer, adds the backend address pool named BackendAddressPool02 to MyLoadBalancer, and then uses the **Set-AzureRmLoadBalancer** cmdlet to update MyLoadBalancer.</span></span>

## <span data-ttu-id="3d894-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3d894-110">PARAMETERS</span></span>

### <span data-ttu-id="3d894-111">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="3d894-111">-LoadBalancer</span></span>
<span data-ttu-id="3d894-112">Określa obiekt **modułu równoważenia obciążenia** .</span><span class="sxs-lookup"><span data-stu-id="3d894-112">Specifies a **LoadBalancer** object.</span></span>

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

### <span data-ttu-id="3d894-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3d894-113">-Name</span></span>
<span data-ttu-id="3d894-114">Określa nazwę konfiguracji puli adresów zaplecza, która ma zostać dodana.</span><span class="sxs-lookup"><span data-stu-id="3d894-114">Specifies the name of the backend address pool configuration to add.</span></span>

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

### <span data-ttu-id="3d894-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d894-115">-DefaultProfile</span></span>
<span data-ttu-id="3d894-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3d894-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d894-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d894-117">CommonParameters</span></span>
<span data-ttu-id="3d894-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d894-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d894-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d894-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d894-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3d894-120">INPUTS</span></span>

### <span data-ttu-id="3d894-121">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3d894-121">PSLoadBalancer</span></span>
<span data-ttu-id="3d894-122">Parametr "równoważenia obciążenia" akceptuje wartość typu "PSLoadBalancer" z procesu</span><span class="sxs-lookup"><span data-stu-id="3d894-122">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="3d894-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3d894-123">OUTPUTS</span></span>

### <span data-ttu-id="3d894-124">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3d894-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="3d894-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3d894-125">NOTES</span></span>

## <span data-ttu-id="3d894-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3d894-126">RELATED LINKS</span></span>

[<span data-ttu-id="3d894-127">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3d894-127">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="3d894-128">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="3d894-128">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="3d894-129">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="3d894-129">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="3d894-130">Nowe — AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="3d894-130">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="3d894-131">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="3d894-131">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md)


