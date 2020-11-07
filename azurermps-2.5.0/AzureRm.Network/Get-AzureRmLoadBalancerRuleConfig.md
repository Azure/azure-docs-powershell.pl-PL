---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B2CF11FC-520C-4C14-9A1B-13F06B250B5D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerruleconfig
schema: 2.0.0
ms.openlocfilehash: bd834351322f3141685538ea80a89e689d70c74f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899278"
---
# <span data-ttu-id="4a253-101">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4a253-101">Get-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="4a253-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4a253-102">SYNOPSIS</span></span>
<span data-ttu-id="4a253-103">Pobiera konfigurację reguły dla modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="4a253-103">Gets the rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a253-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4a253-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a253-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4a253-105">DESCRIPTION</span></span>
<span data-ttu-id="4a253-106">Polecenie cmdlet **Get-AzureRmLoadBalancerRuleConfig** pobiera co najmniej jeden wariant reguły dla modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="4a253-106">The **Get-AzureRmLoadBalancerRuleConfig** cmdlet gets one or more rule configurations for a load balancer.</span></span>

## <span data-ttu-id="4a253-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4a253-107">EXAMPLES</span></span>

### <span data-ttu-id="4a253-108">Przykład 1. Pobierz konfigurację reguły modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="4a253-108">Example 1: Get the rule configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerRuleConfig -Name "MyLBrulename" -LoadBalancer $slb
```

<span data-ttu-id="4a253-109">Pierwsze polecenie uzyskuje usługę równoważenia obciążenia o nazwie MyLoadBalancer, a następnie zapisuje ją w zmiennej $slb.</span><span class="sxs-lookup"><span data-stu-id="4a253-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="4a253-110">Drugie polecenie pobiera skojarzoną konfigurację reguły o nazwie MyLBrulename z modułu równoważenia obciążenia w $slb.</span><span class="sxs-lookup"><span data-stu-id="4a253-110">The second command gets the associated rule configuration named MyLBrulename from the load balancer in $slb.</span></span>

## <span data-ttu-id="4a253-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4a253-111">PARAMETERS</span></span>

### <span data-ttu-id="4a253-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a253-112">-DefaultProfile</span></span>
<span data-ttu-id="4a253-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4a253-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a253-114">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="4a253-114">-LoadBalancer</span></span>
<span data-ttu-id="4a253-115">Określa moduł równoważenia obciążenia skojarzony z konfiguracją reguły do pobrania.</span><span class="sxs-lookup"><span data-stu-id="4a253-115">Specifies the load balancer that is associated with the rule configuration to get.</span></span>

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

### <span data-ttu-id="4a253-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4a253-116">-Name</span></span>
<span data-ttu-id="4a253-117">Określa nazwę konfiguracji reguły, którą należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="4a253-117">Specifies the name of the rule configuration to get.</span></span>

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

### <span data-ttu-id="4a253-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a253-118">CommonParameters</span></span>
<span data-ttu-id="4a253-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a253-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a253-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a253-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a253-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4a253-121">INPUTS</span></span>

### <span data-ttu-id="4a253-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4a253-122">PSLoadBalancer</span></span>
<span data-ttu-id="4a253-123">Parametr "równoważenia obciążenia" akceptuje wartość typu "PSLoadBalancer" z procesu</span><span class="sxs-lookup"><span data-stu-id="4a253-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="4a253-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4a253-124">OUTPUTS</span></span>

### <span data-ttu-id="4a253-125">Microsoft. Azure. Commands. Network. models. PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="4a253-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="4a253-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4a253-126">NOTES</span></span>

## <span data-ttu-id="4a253-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4a253-127">RELATED LINKS</span></span>

[<span data-ttu-id="4a253-128">Dodaj-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4a253-128">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="4a253-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4a253-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="4a253-130">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4a253-130">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="4a253-131">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4a253-131">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


