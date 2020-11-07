---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 1bcaab526ac2fbb82d696db7197bbc8d69c0078f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719570"
---
# <span data-ttu-id="1ae95-101">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1ae95-101">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="1ae95-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1ae95-102">SYNOPSIS</span></span>
<span data-ttu-id="1ae95-103">Pobiera konfigurację reguły ruchu wychodzącego w usłudze równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="1ae95-103">Gets an outbound rule configuration in a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ae95-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1ae95-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ae95-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1ae95-105">DESCRIPTION</span></span>
<span data-ttu-id="1ae95-106">Polecenie cmdlet **Get-AzureRmLoadBalancerOutboundRuleConfig** Pobiera konfigurację reguły ruchu wychodzącego lub listę konfiguracji reguł ruchu wychodzącego w ramach modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="1ae95-106">The **Get-AzureRmLoadBalancerOutboundRuleConfig** cmdlet gets an outbound rule configuration or a list of outbound rule configurations in a load balancer.</span></span>

## <span data-ttu-id="1ae95-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1ae95-107">EXAMPLES</span></span>

### <span data-ttu-id="1ae95-108">Przykład 1: Pobieranie konfiguracji reguły ruchu wychodzącego w usłudze równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="1ae95-108">Example 1: Get an outbound rule configuration in a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzureRmLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Get-AzureRmLoadBalancerOutboundRuleConfig -LoadBalancer $slb -Name "MyRule"
```

<span data-ttu-id="1ae95-109">Pierwsze polecenie uzyskuje usługę równoważenia obciążenia o nazwie MyLoadBalancer, a następnie zapisuje ją w zmiennej $slb.</span><span class="sxs-lookup"><span data-stu-id="1ae95-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="1ae95-110">Drugie polecenie pobiera konfigurację reguły ruchu wychodzącego o nazwie Moja reguła skojarzona z tym modułem równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="1ae95-110">The second command gets the outbound rule configuration named MyRule associated with that load balancer.</span></span>

## <span data-ttu-id="1ae95-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1ae95-111">PARAMETERS</span></span>

### <span data-ttu-id="1ae95-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ae95-112">-DefaultProfile</span></span>
<span data-ttu-id="1ae95-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1ae95-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ae95-114">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="1ae95-114">-LoadBalancer</span></span>
<span data-ttu-id="1ae95-115">Odwołanie do zasobu modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="1ae95-115">The reference of the load balancer resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ae95-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1ae95-116">-Name</span></span>
<span data-ttu-id="1ae95-117">Nazwa reguły ruchu wychodzącego.</span><span class="sxs-lookup"><span data-stu-id="1ae95-117">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="1ae95-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ae95-118">CommonParameters</span></span>
<span data-ttu-id="1ae95-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ae95-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ae95-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ae95-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ae95-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1ae95-121">INPUTS</span></span>

### <span data-ttu-id="1ae95-122">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1ae95-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="1ae95-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1ae95-123">OUTPUTS</span></span>

### <span data-ttu-id="1ae95-124">Microsoft. Azure. Commands. Network. models. PSOutboundRule</span><span class="sxs-lookup"><span data-stu-id="1ae95-124">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span></span>

## <span data-ttu-id="1ae95-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1ae95-125">NOTES</span></span>

## <span data-ttu-id="1ae95-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1ae95-126">RELATED LINKS</span></span>
