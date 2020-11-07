---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DEBD58A3-AFAF-485C-8708-53228625138F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: 38f6223fdf1dc230dbd34310b7eda2ab45e2d4b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716523"
---
# <span data-ttu-id="f298f-101">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f298f-101">Remove-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="f298f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f298f-102">SYNOPSIS</span></span>
<span data-ttu-id="f298f-103">Usuwa konfigurację reguły dla modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="f298f-103">Removes a rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f298f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f298f-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f298f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f298f-105">DESCRIPTION</span></span>
<span data-ttu-id="f298f-106">Polecenie cmdlet **Remove-AzureRmLoadBalancerRuleConfig** usuwa konfigurację reguły dla modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f298f-106">The **Remove-AzureRmLoadBalancerRuleConfig** cmdlet removes a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="f298f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f298f-107">EXAMPLES</span></span>

### <span data-ttu-id="f298f-108">Przykład 1: Usuwanie konfiguracji reguły z modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="f298f-108">Example 1: Remove a rule configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerRuleConfig -Name "MyLBruleName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="f298f-109">Pierwsze polecenie uzyskuje usługę równoważenia obciążenia o nazwie MyLoadBalancer, a następnie zapisuje ją w zmiennej $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="f298f-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="f298f-110">Drugie polecenie usuwa konfigurację reguły o nazwie MyLBruleName z modułu równoważenia obciążenia w $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="f298f-110">The second command removes the rule configuration named MyLBruleName from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="f298f-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f298f-111">PARAMETERS</span></span>

### <span data-ttu-id="f298f-112">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="f298f-112">-LoadBalancer</span></span>
<span data-ttu-id="f298f-113">Określa obiekt **modułu równoważenia obciążenia** , który zawiera konfigurację reguły, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f298f-113">Specifies the **LoadBalancer** object that contains the rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f298f-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f298f-114">-Name</span></span>
<span data-ttu-id="f298f-115">Określa nazwę konfiguracji reguły modułu równoważenia obciążenia, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f298f-115">Specifies the name of the load balancer rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f298f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f298f-116">-DefaultProfile</span></span>
<span data-ttu-id="f298f-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f298f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f298f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f298f-118">CommonParameters</span></span>
<span data-ttu-id="f298f-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f298f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f298f-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f298f-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f298f-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f298f-121">INPUTS</span></span>

### <span data-ttu-id="f298f-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f298f-122">PSLoadBalancer</span></span>
<span data-ttu-id="f298f-123">Parametr "równoważenia obciążenia" akceptuje wartość typu "PSLoadBalancer" z procesu</span><span class="sxs-lookup"><span data-stu-id="f298f-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="f298f-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f298f-124">OUTPUTS</span></span>

### <span data-ttu-id="f298f-125">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f298f-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f298f-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f298f-126">NOTES</span></span>

## <span data-ttu-id="f298f-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f298f-127">RELATED LINKS</span></span>

[<span data-ttu-id="f298f-128">Dodaj-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f298f-128">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="f298f-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f298f-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="f298f-130">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f298f-130">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="f298f-131">Nowe — AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f298f-131">New-AzureRmLoadBalancerRuleConfig</span></span>](./New-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="f298f-132">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f298f-132">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


