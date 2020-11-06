---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6BEED413-E2E4-4557-BD31-2A655E790C1D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 070680c1dc1c9fd091b311888867cda3f844ce4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545091"
---
# <span data-ttu-id="44158-101">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="44158-101">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="44158-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="44158-102">SYNOPSIS</span></span>
<span data-ttu-id="44158-103">Pobiera konfigurację IP frontonu w usłudze równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="44158-103">Gets a front-end IP configuration in a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44158-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="44158-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44158-105">Opis</span><span class="sxs-lookup"><span data-stu-id="44158-105">DESCRIPTION</span></span>
<span data-ttu-id="44158-106">Polecenie cmdlet **Get-AzureRmLoadBalancerFrontendIpConfig** Pobiera konfigurację adresu IP frontonu lub listy konfiguracji adresów IP frontonu w usłudze równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="44158-106">The **Get-AzureRmLoadBalancerFrontendIpConfig** cmdlet gets a front-end IP configuration or a list of front-end IP configurations in a load balancer.</span></span>

## <span data-ttu-id="44158-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="44158-107">EXAMPLES</span></span>

### <span data-ttu-id="44158-108">Przykład 1: Uzyskiwanie konfiguracji frontonu IP w usłudze równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="44158-108">Example 1: Get a front-end IP configuration in a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -LoadBalancer $slb
```

<span data-ttu-id="44158-109">Pierwsze polecenie uzyskuje usługę równoważenia obciążenia o nazwie MyLoadBalancer, a następnie zapisuje ją w zmiennej $slb.</span><span class="sxs-lookup"><span data-stu-id="44158-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="44158-110">Drugie polecenie pobiera konfigurację IP front-end skojarzoną z modułem równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="44158-110">The second command gets the front end IP configuration associated with that load balancer.</span></span>

## <span data-ttu-id="44158-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="44158-111">PARAMETERS</span></span>

### <span data-ttu-id="44158-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44158-112">-DefaultProfile</span></span>
<span data-ttu-id="44158-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="44158-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44158-114">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="44158-114">-LoadBalancer</span></span>
<span data-ttu-id="44158-115">Umożliwia określenie modułu równoważenia obciążenia skojarzonego z konfiguracją IP frontonu w celu uzyskania.</span><span class="sxs-lookup"><span data-stu-id="44158-115">Specifies the load balancer that is associated with the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="44158-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="44158-116">-Name</span></span>
<span data-ttu-id="44158-117">Określa nazwę modułu równoważenia obciążenia zawierającego konfigurację frontonu IP do pobrania.</span><span class="sxs-lookup"><span data-stu-id="44158-117">Specifies the name of the load balancer that contains the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="44158-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44158-118">CommonParameters</span></span>
<span data-ttu-id="44158-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44158-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44158-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44158-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44158-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="44158-121">INPUTS</span></span>

### <span data-ttu-id="44158-122">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="44158-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="44158-123">Parametry: moduł równoważenia obciążenia (ByValue)</span><span class="sxs-lookup"><span data-stu-id="44158-123">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="44158-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="44158-124">OUTPUTS</span></span>

### <span data-ttu-id="44158-125">Microsoft. Azure. Commands. Network. models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="44158-125">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="44158-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="44158-126">NOTES</span></span>

## <span data-ttu-id="44158-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="44158-127">RELATED LINKS</span></span>

[<span data-ttu-id="44158-128">Dodaj-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="44158-128">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="44158-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="44158-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="44158-130">Nowe — AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="44158-130">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="44158-131">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="44158-131">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="44158-132">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="44158-132">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


