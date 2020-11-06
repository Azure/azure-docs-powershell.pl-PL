---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5F8E11DF-D560-44D7-99CA-C425951A56D6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: c4809371792a2add8510b1bf7f4db39dd344b037
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525509"
---
# <span data-ttu-id="86de0-101">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="86de0-101">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="86de0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="86de0-102">SYNOPSIS</span></span>
<span data-ttu-id="86de0-103">Usuwa konfigurację frontonu IP z modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="86de0-103">Removes a front-end IP configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86de0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="86de0-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerFrontendIpConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86de0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="86de0-105">DESCRIPTION</span></span>
<span data-ttu-id="86de0-106">Polecenie cmdlet **Remove-AzureRmLoadBalancerFrontendIpConfig** usuwa konfigurację adresu IP frontonu z modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="86de0-106">The **Remove-AzureRmLoadBalancerFrontendIpConfig** cmdlet removes a front-end IP configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="86de0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="86de0-107">EXAMPLES</span></span>

### <span data-ttu-id="86de0-108">Przykład 1: Usuwanie konfiguracji frontonu IP z modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="86de0-108">Example 1: Remove a front-end IP configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerFrontendIpConfig -Name "frontendName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="86de0-109">Pierwsze polecenie uzyskuje moduł równoważenia obciążenia skojarzony z konfiguracją frontonu IP, którą chcesz usunąć, a następnie zapisze ją w zmiennej $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="86de0-109">The first command gets the load balancer that is associated with the front-end IP configuration you want to remove, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="86de0-110">Drugie polecenie usuwa skojarzoną konfigurację adresu IP frontonu z modułu równoważenia obciążenia w $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="86de0-110">The second command removes the associated frontend IP configuration from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="86de0-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="86de0-111">PARAMETERS</span></span>

### <span data-ttu-id="86de0-112">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="86de0-112">-LoadBalancer</span></span>
<span data-ttu-id="86de0-113">Określa moduł równoważenia obciążenia zawierający konfigurację frontonu IP do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="86de0-113">Specifies the load balancer that contains the front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="86de0-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="86de0-114">-Name</span></span>
<span data-ttu-id="86de0-115">Określa nazwę konfiguracji frontonu adresu IP do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="86de0-115">Specifies the name of the front-end IP address configuration to remove.</span></span>

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

### <span data-ttu-id="86de0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86de0-116">-DefaultProfile</span></span>
<span data-ttu-id="86de0-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="86de0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86de0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86de0-118">CommonParameters</span></span>
<span data-ttu-id="86de0-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86de0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86de0-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86de0-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86de0-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="86de0-121">INPUTS</span></span>

### <span data-ttu-id="86de0-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="86de0-122">PSLoadBalancer</span></span>
<span data-ttu-id="86de0-123">Parametr "równoważenia obciążenia" akceptuje wartość typu "PSLoadBalancer" z procesu</span><span class="sxs-lookup"><span data-stu-id="86de0-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="86de0-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="86de0-124">OUTPUTS</span></span>

### <span data-ttu-id="86de0-125">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="86de0-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="86de0-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="86de0-126">NOTES</span></span>

## <span data-ttu-id="86de0-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="86de0-127">RELATED LINKS</span></span>

[<span data-ttu-id="86de0-128">Dodaj-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="86de0-128">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="86de0-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="86de0-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="86de0-130">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="86de0-130">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="86de0-131">Nowe — AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="86de0-131">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="86de0-132">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="86de0-132">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


