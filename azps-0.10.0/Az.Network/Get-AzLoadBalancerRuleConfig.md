---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2CF11FC-520C-4C14-9A1B-13F06B250B5D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: a5d21e5a34727d0bc13730503d55be6ef604a245
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890762"
---
# <span data-ttu-id="ef9c1-101">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ef9c1-101">Get-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="ef9c1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ef9c1-102">SYNOPSIS</span></span>
<span data-ttu-id="ef9c1-103">Pobiera konfigurację reguły dla modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="ef9c1-103">Gets the rule configuration for a load balancer.</span></span>

## <span data-ttu-id="ef9c1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ef9c1-104">SYNTAX</span></span>

```
Get-AzLoadBalancerRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef9c1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ef9c1-105">DESCRIPTION</span></span>
<span data-ttu-id="ef9c1-106">Polecenie cmdlet **Get-AzLoadBalancerRuleConfig** pobiera co najmniej jeden wariant reguły dla modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="ef9c1-106">The **Get-AzLoadBalancerRuleConfig** cmdlet gets one or more rule configurations for a load balancer.</span></span>

## <span data-ttu-id="ef9c1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ef9c1-107">EXAMPLES</span></span>

### <span data-ttu-id="ef9c1-108">Przykład 1. Pobierz konfigurację reguły modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="ef9c1-108">Example 1: Get the rule configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerRuleConfig -Name "MyLBrulename" -LoadBalancer $slb
```

<span data-ttu-id="ef9c1-109">Pierwsze polecenie uzyskuje usługę równoważenia obciążenia o nazwie MyLoadBalancer, a następnie zapisuje ją w zmiennej $slb.</span><span class="sxs-lookup"><span data-stu-id="ef9c1-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="ef9c1-110">Drugie polecenie pobiera skojarzoną konfigurację reguły o nazwie MyLBrulename z modułu równoważenia obciążenia w $slb.</span><span class="sxs-lookup"><span data-stu-id="ef9c1-110">The second command gets the associated rule configuration named MyLBrulename from the load balancer in $slb.</span></span>

## <span data-ttu-id="ef9c1-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ef9c1-111">PARAMETERS</span></span>

### <span data-ttu-id="ef9c1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef9c1-112">-DefaultProfile</span></span>
<span data-ttu-id="ef9c1-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ef9c1-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef9c1-114">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="ef9c1-114">-LoadBalancer</span></span>
<span data-ttu-id="ef9c1-115">Określa moduł równoważenia obciążenia skojarzony z konfiguracją reguły do pobrania.</span><span class="sxs-lookup"><span data-stu-id="ef9c1-115">Specifies the load balancer that is associated with the rule configuration to get.</span></span>

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

### <span data-ttu-id="ef9c1-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ef9c1-116">-Name</span></span>
<span data-ttu-id="ef9c1-117">Określa nazwę konfiguracji reguły, którą należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="ef9c1-117">Specifies the name of the rule configuration to get.</span></span>

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

### <span data-ttu-id="ef9c1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef9c1-118">CommonParameters</span></span>
<span data-ttu-id="ef9c1-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef9c1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef9c1-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef9c1-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef9c1-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ef9c1-121">INPUTS</span></span>

### <span data-ttu-id="ef9c1-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ef9c1-122">PSLoadBalancer</span></span>
<span data-ttu-id="ef9c1-123">Parametr "równoważenia obciążenia" akceptuje wartość typu "PSLoadBalancer" z procesu</span><span class="sxs-lookup"><span data-stu-id="ef9c1-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="ef9c1-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ef9c1-124">OUTPUTS</span></span>

### <span data-ttu-id="ef9c1-125">Microsoft. Azure. Commands. Network. models. PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="ef9c1-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="ef9c1-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ef9c1-126">NOTES</span></span>

## <span data-ttu-id="ef9c1-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ef9c1-127">RELATED LINKS</span></span>

[<span data-ttu-id="ef9c1-128">Dodaj-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ef9c1-128">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="ef9c1-129">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ef9c1-129">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="ef9c1-130">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ef9c1-130">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="ef9c1-131">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ef9c1-131">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


