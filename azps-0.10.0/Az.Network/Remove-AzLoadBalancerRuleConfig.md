---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DEBD58A3-AFAF-485C-8708-53228625138F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 9c50452acd832c7ac7ca0c4bc2827b8f320115b4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890282"
---
# <span data-ttu-id="70c88-101">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="70c88-101">Remove-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="70c88-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="70c88-102">SYNOPSIS</span></span>
<span data-ttu-id="70c88-103">Usuwa konfigurację reguły dla modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="70c88-103">Removes a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="70c88-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="70c88-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70c88-105">Opis</span><span class="sxs-lookup"><span data-stu-id="70c88-105">DESCRIPTION</span></span>
<span data-ttu-id="70c88-106">Polecenie cmdlet **Remove-AzLoadBalancerRuleConfig** usuwa konfigurację reguły dla modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="70c88-106">The **Remove-AzLoadBalancerRuleConfig** cmdlet removes a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="70c88-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="70c88-107">EXAMPLES</span></span>

### <span data-ttu-id="70c88-108">Przykład 1: Usuwanie konfiguracji reguły z modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="70c88-108">Example 1: Remove a rule configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerRuleConfig -Name "MyLBruleName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="70c88-109">Pierwsze polecenie uzyskuje usługę równoważenia obciążenia o nazwie MyLoadBalancer, a następnie zapisuje ją w zmiennej $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="70c88-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="70c88-110">Drugie polecenie usuwa konfigurację reguły o nazwie MyLBruleName z modułu równoważenia obciążenia w $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="70c88-110">The second command removes the rule configuration named MyLBruleName from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="70c88-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="70c88-111">PARAMETERS</span></span>

### <span data-ttu-id="70c88-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70c88-112">-DefaultProfile</span></span>
<span data-ttu-id="70c88-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="70c88-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70c88-114">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="70c88-114">-LoadBalancer</span></span>
<span data-ttu-id="70c88-115">Określa obiekt **modułu równoważenia obciążenia** , który zawiera konfigurację reguły, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70c88-115">Specifies the **LoadBalancer** object that contains the rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="70c88-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="70c88-116">-Name</span></span>
<span data-ttu-id="70c88-117">Określa nazwę konfiguracji reguły modułu równoważenia obciążenia, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70c88-117">Specifies the name of the load balancer rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="70c88-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70c88-118">CommonParameters</span></span>
<span data-ttu-id="70c88-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70c88-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70c88-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70c88-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70c88-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="70c88-121">INPUTS</span></span>

### <span data-ttu-id="70c88-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="70c88-122">PSLoadBalancer</span></span>
<span data-ttu-id="70c88-123">Parametr "równoważenia obciążenia" akceptuje wartość typu "PSLoadBalancer" z procesu</span><span class="sxs-lookup"><span data-stu-id="70c88-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="70c88-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="70c88-124">OUTPUTS</span></span>

### <span data-ttu-id="70c88-125">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="70c88-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="70c88-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="70c88-126">NOTES</span></span>

## <span data-ttu-id="70c88-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="70c88-127">RELATED LINKS</span></span>

[<span data-ttu-id="70c88-128">Dodaj-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="70c88-128">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="70c88-129">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="70c88-129">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="70c88-130">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="70c88-130">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="70c88-131">Nowe — AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="70c88-131">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="70c88-132">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="70c88-132">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


