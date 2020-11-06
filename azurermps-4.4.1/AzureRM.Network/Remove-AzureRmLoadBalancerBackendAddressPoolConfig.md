---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F965A9DE-645C-471B-84E8-58D648B1CA57
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: eb7f7b85286d491d4168e08ef94c1a46ff9076ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525510"
---
# <span data-ttu-id="4c5a3-101">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="4c5a3-101">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="4c5a3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4c5a3-102">SYNOPSIS</span></span>
<span data-ttu-id="4c5a3-103">Usuwa konfigurację puli adresów zaplecza z modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="4c5a3-103">Removes a backend address pool configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c5a3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4c5a3-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerBackendAddressPoolConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c5a3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4c5a3-105">DESCRIPTION</span></span>
<span data-ttu-id="4c5a3-106">Polecenie cmdlet **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** usuwa pulę adresów zaplecza z modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="4c5a3-106">The **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** cmdlet removes a backend address pool from a load balancer.</span></span>

## <span data-ttu-id="4c5a3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4c5a3-107">EXAMPLES</span></span>

### <span data-ttu-id="4c5a3-108">Przykład 1: Usuwanie konfiguracji puli adresów zaplecza z modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="4c5a3-108">Example 1: Remove a backend address pool configuration from a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" | Remove-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzureRmLoadBalancer
```

<span data-ttu-id="4c5a3-109">To polecenie uzyskuje moduł równoważenia obciążenia o nazwie MyLoadBalancer i przekazuje go do pozycji **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** , co powoduje usunięcie konfiguracji BackendAddressPool02 z MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="4c5a3-109">This command gets the load balancer named MyLoadBalancer and passes it to **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** , which removes the BackendAddressPool02 configuration from MyLoadBalancer.</span></span>
<span data-ttu-id="4c5a3-110">Na koniec Set-AzureRmLoadBalancer polecenie cmdlet aktualizuje MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="4c5a3-110">Finally, the Set-AzureRmLoadBalancer cmdlet updates MyLoadBalancer.</span></span>
<span data-ttu-id="4c5a3-111">Należy pamiętać, że konfiguracja puli adresów zaplecza musi istnieć, aby można było ją usunąć.</span><span class="sxs-lookup"><span data-stu-id="4c5a3-111">Note that a backend address pool configuration must exist before you can delete it.</span></span>

## <span data-ttu-id="4c5a3-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4c5a3-112">PARAMETERS</span></span>

### <span data-ttu-id="4c5a3-113">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="4c5a3-113">-LoadBalancer</span></span>
<span data-ttu-id="4c5a3-114">Określa moduł równoważenia obciążenia zawierający pulę adresów zaplecza do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="4c5a3-114">Specifies the load balancer that contains the backend address pool to remove.</span></span>

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

### <span data-ttu-id="4c5a3-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4c5a3-115">-Name</span></span>
<span data-ttu-id="4c5a3-116">Określa nazwę puli adresów zaplecza, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c5a3-116">Specifies the name of the backend address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4c5a3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c5a3-117">-DefaultProfile</span></span>
<span data-ttu-id="4c5a3-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4c5a3-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c5a3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c5a3-119">CommonParameters</span></span>
<span data-ttu-id="4c5a3-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c5a3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c5a3-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c5a3-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c5a3-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4c5a3-122">INPUTS</span></span>

### <span data-ttu-id="4c5a3-123">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4c5a3-123">PSLoadBalancer</span></span>
<span data-ttu-id="4c5a3-124">Parametr "równoważenia obciążenia" akceptuje wartość typu "PSLoadBalancer" z procesu</span><span class="sxs-lookup"><span data-stu-id="4c5a3-124">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="4c5a3-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4c5a3-125">OUTPUTS</span></span>

### <span data-ttu-id="4c5a3-126">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4c5a3-126">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="4c5a3-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4c5a3-127">NOTES</span></span>

## <span data-ttu-id="4c5a3-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4c5a3-128">RELATED LINKS</span></span>

[<span data-ttu-id="4c5a3-129">Dodaj-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="4c5a3-129">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="4c5a3-130">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4c5a3-130">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="4c5a3-131">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="4c5a3-131">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="4c5a3-132">Nowe — AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="4c5a3-132">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzureRmLoadBalancerBackendAddressPoolConfig.md)


