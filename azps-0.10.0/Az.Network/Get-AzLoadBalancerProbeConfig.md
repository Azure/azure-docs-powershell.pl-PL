---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 278228EB-0126-4F27-A30F-51DC498C65FE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: bf106b9fbe4c8f069f2d7b5b1b2a9beae95cd51b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890765"
---
# <span data-ttu-id="f3774-101">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f3774-101">Get-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="f3774-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f3774-102">SYNOPSIS</span></span>
<span data-ttu-id="f3774-103">Pobiera konfigurację sondy dla modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="f3774-103">Gets a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="f3774-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f3774-104">SYNTAX</span></span>

```
Get-AzLoadBalancerProbeConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3774-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f3774-105">DESCRIPTION</span></span>
<span data-ttu-id="f3774-106">Polecenie cmdlet **Get-AzLoadBalancerProbeConfig** umożliwia pobranie co najmniej jednej konfiguracji sondy modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="f3774-106">The **Get-AzLoadBalancerProbeConfig** cmdlet gets one or more probe configurations for a load balancer.</span></span>

## <span data-ttu-id="f3774-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f3774-107">EXAMPLES</span></span>

### <span data-ttu-id="f3774-108">Przykład 1: Uzyskiwanie konfiguracji sondy modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="f3774-108">Example 1: Get the probe configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $slb
```

<span data-ttu-id="f3774-109">Pierwsze polecenie uzyskuje usługę równoważenia obciążenia o nazwie MyLoadBalancer, a następnie zapisuje ją w zmiennej $slb.</span><span class="sxs-lookup"><span data-stu-id="f3774-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="f3774-110">Drugie polecenie pobiera skojarzoną konfigurację sondy o nazwie Moja Sonda z modułu równoważenia obciążenia w $slb.</span><span class="sxs-lookup"><span data-stu-id="f3774-110">The second command gets the associated probe configuration named MyProbe from the load balancer in $slb.</span></span>

## <span data-ttu-id="f3774-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f3774-111">PARAMETERS</span></span>

### <span data-ttu-id="f3774-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3774-112">-DefaultProfile</span></span>
<span data-ttu-id="f3774-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f3774-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3774-114">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="f3774-114">-LoadBalancer</span></span>
<span data-ttu-id="f3774-115">Określa moduł równoważenia obciążenia skojarzony z konfiguracją sondy do pobrania.</span><span class="sxs-lookup"><span data-stu-id="f3774-115">Specifies the load balancer that is associated with the probe configuration to get.</span></span>

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

### <span data-ttu-id="f3774-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f3774-116">-Name</span></span>
<span data-ttu-id="f3774-117">Określa nazwę konfiguracji sondy, którą należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="f3774-117">Specifies the name of the probe configuration to get.</span></span>

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

### <span data-ttu-id="f3774-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3774-118">CommonParameters</span></span>
<span data-ttu-id="f3774-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3774-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3774-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3774-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3774-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f3774-121">INPUTS</span></span>

### <span data-ttu-id="f3774-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f3774-122">PSLoadBalancer</span></span>
<span data-ttu-id="f3774-123">Parametr "równoważenia obciążenia" akceptuje wartość typu "PSLoadBalancer" z procesu</span><span class="sxs-lookup"><span data-stu-id="f3774-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="f3774-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f3774-124">OUTPUTS</span></span>

### <span data-ttu-id="f3774-125">Microsoft. Azure. Commands. Network. models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="f3774-125">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="f3774-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f3774-126">NOTES</span></span>

## <span data-ttu-id="f3774-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f3774-127">RELATED LINKS</span></span>

[<span data-ttu-id="f3774-128">Dodaj-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f3774-128">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="f3774-129">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f3774-129">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="f3774-130">Nowe — AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f3774-130">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="f3774-131">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f3774-131">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="f3774-132">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f3774-132">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


