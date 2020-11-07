---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5F8E11DF-D560-44D7-99CA-C425951A56D6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerfrontendipconfig
schema: 2.0.0
ms.openlocfilehash: 192eb5ebfa21c97aa7043c4d4719831def08d93e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899240"
---
# <span data-ttu-id="8332b-101">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8332b-101">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="8332b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8332b-102">SYNOPSIS</span></span>
<span data-ttu-id="8332b-103">Usuwa konfigurację frontonu IP z modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="8332b-103">Removes a front-end IP configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8332b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8332b-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerFrontendIpConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8332b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8332b-105">DESCRIPTION</span></span>
<span data-ttu-id="8332b-106">Polecenie cmdlet **Remove-AzureRmLoadBalancerFrontendIpConfig** usuwa konfigurację adresu IP frontonu z modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8332b-106">The **Remove-AzureRmLoadBalancerFrontendIpConfig** cmdlet removes a front-end IP configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="8332b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8332b-107">EXAMPLES</span></span>

### <span data-ttu-id="8332b-108">Przykład 1: Usuwanie konfiguracji frontonu IP z modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="8332b-108">Example 1: Remove a front-end IP configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerFrontendIpConfig -Name "frontendName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="8332b-109">Pierwsze polecenie uzyskuje moduł równoważenia obciążenia skojarzony z konfiguracją frontonu IP, którą chcesz usunąć, a następnie zapisze ją w zmiennej $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="8332b-109">The first command gets the load balancer that is associated with the front-end IP configuration you want to remove, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="8332b-110">Drugie polecenie usuwa skojarzoną konfigurację adresu IP frontonu z modułu równoważenia obciążenia w $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="8332b-110">The second command removes the associated frontend IP configuration from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="8332b-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8332b-111">PARAMETERS</span></span>

### <span data-ttu-id="8332b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8332b-112">-DefaultProfile</span></span>
<span data-ttu-id="8332b-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8332b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8332b-114">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="8332b-114">-LoadBalancer</span></span>
<span data-ttu-id="8332b-115">Określa moduł równoważenia obciążenia zawierający konfigurację frontonu IP do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="8332b-115">Specifies the load balancer that contains the front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="8332b-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8332b-116">-Name</span></span>
<span data-ttu-id="8332b-117">Określa nazwę konfiguracji frontonu adresu IP do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="8332b-117">Specifies the name of the front-end IP address configuration to remove.</span></span>

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

### <span data-ttu-id="8332b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8332b-118">CommonParameters</span></span>
<span data-ttu-id="8332b-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8332b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8332b-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8332b-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8332b-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8332b-121">INPUTS</span></span>

### <span data-ttu-id="8332b-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8332b-122">PSLoadBalancer</span></span>
<span data-ttu-id="8332b-123">Parametr "równoważenia obciążenia" akceptuje wartość typu "PSLoadBalancer" z procesu</span><span class="sxs-lookup"><span data-stu-id="8332b-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="8332b-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8332b-124">OUTPUTS</span></span>

### <span data-ttu-id="8332b-125">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8332b-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="8332b-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8332b-126">NOTES</span></span>

## <span data-ttu-id="8332b-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8332b-127">RELATED LINKS</span></span>

[<span data-ttu-id="8332b-128">Dodaj-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8332b-128">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="8332b-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8332b-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="8332b-130">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8332b-130">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="8332b-131">Nowe — AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8332b-131">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="8332b-132">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8332b-132">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


