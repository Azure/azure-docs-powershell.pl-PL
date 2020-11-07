---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6BEED413-E2E4-4557-BD31-2A655E790C1D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerfrontendipconfig
schema: 2.0.0
ms.openlocfilehash: a80fa84beaaea0307447f25767d665c465e8c2aa
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897325"
---
# <span data-ttu-id="cdee0-101">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="cdee0-101">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="cdee0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cdee0-102">SYNOPSIS</span></span>
<span data-ttu-id="cdee0-103">Pobiera konfigurację IP frontonu w usłudze równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="cdee0-103">Gets a front-end IP configuration in a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cdee0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cdee0-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerFrontendIpConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cdee0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cdee0-105">DESCRIPTION</span></span>
<span data-ttu-id="cdee0-106">Polecenie cmdlet **Get-AzureRmLoadBalancerFrontendIpConfig** Pobiera konfigurację adresu IP frontonu lub listy konfiguracji adresów IP frontonu w usłudze równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="cdee0-106">The **Get-AzureRmLoadBalancerFrontendIpConfig** cmdlet gets a front-end IP configuration or a list of front-end IP configurations in a load balancer.</span></span>

## <span data-ttu-id="cdee0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cdee0-107">EXAMPLES</span></span>

### <span data-ttu-id="cdee0-108">Przykład 1: Uzyskiwanie konfiguracji frontonu IP w usłudze równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="cdee0-108">Example 1: Get a front-end IP configuration in a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -LoadBalancer $slb
```

<span data-ttu-id="cdee0-109">Pierwsze polecenie uzyskuje usługę równoważenia obciążenia o nazwie MyLoadBalancer, a następnie zapisuje ją w zmiennej $slb.</span><span class="sxs-lookup"><span data-stu-id="cdee0-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="cdee0-110">Drugie polecenie pobiera konfigurację IP front-end skojarzoną z modułem równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="cdee0-110">The second command gets the front end IP configuration associated with that load balancer.</span></span>

## <span data-ttu-id="cdee0-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cdee0-111">PARAMETERS</span></span>

### <span data-ttu-id="cdee0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdee0-112">-DefaultProfile</span></span>
<span data-ttu-id="cdee0-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cdee0-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cdee0-114">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="cdee0-114">-LoadBalancer</span></span>
<span data-ttu-id="cdee0-115">Umożliwia określenie modułu równoważenia obciążenia skojarzonego z konfiguracją IP frontonu w celu uzyskania.</span><span class="sxs-lookup"><span data-stu-id="cdee0-115">Specifies the load balancer that is associated with the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="cdee0-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cdee0-116">-Name</span></span>
<span data-ttu-id="cdee0-117">Określa nazwę modułu równoważenia obciążenia zawierającego konfigurację frontonu IP do pobrania.</span><span class="sxs-lookup"><span data-stu-id="cdee0-117">Specifies the name of the load balancer that contains the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="cdee0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdee0-118">CommonParameters</span></span>
<span data-ttu-id="cdee0-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdee0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdee0-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdee0-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdee0-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cdee0-121">INPUTS</span></span>

### <span data-ttu-id="cdee0-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="cdee0-122">PSLoadBalancer</span></span>
<span data-ttu-id="cdee0-123">Parametr "równoważenia obciążenia" akceptuje wartość typu "PSLoadBalancer" z procesu</span><span class="sxs-lookup"><span data-stu-id="cdee0-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="cdee0-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cdee0-124">OUTPUTS</span></span>

### <span data-ttu-id="cdee0-125">Microsoft. Azure. Commands. Network. models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="cdee0-125">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="cdee0-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cdee0-126">NOTES</span></span>

## <span data-ttu-id="cdee0-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cdee0-127">RELATED LINKS</span></span>

[<span data-ttu-id="cdee0-128">Dodaj-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="cdee0-128">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="cdee0-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="cdee0-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="cdee0-130">Nowe — AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="cdee0-130">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="cdee0-131">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="cdee0-131">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="cdee0-132">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="cdee0-132">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


