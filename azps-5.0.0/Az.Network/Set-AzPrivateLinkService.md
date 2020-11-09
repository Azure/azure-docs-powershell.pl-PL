---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateLinkService.md
ms.openlocfilehash: a594e23505b9db1004a086ff4e0c168353c6bc28
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319092"
---
# <span data-ttu-id="84769-101">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="84769-101">Set-AzPrivateLinkService</span></span>

## <span data-ttu-id="84769-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="84769-102">SYNOPSIS</span></span>
<span data-ttu-id="84769-103">Umożliwia zaktualizowanie usługi linku prywatnego.</span><span class="sxs-lookup"><span data-stu-id="84769-103">Updates a private link service.</span></span>

## <span data-ttu-id="84769-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="84769-104">SYNTAX</span></span>

```
Set-AzPrivateLinkService -PrivateLinkService <PSPrivateLinkService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84769-105">Opis</span><span class="sxs-lookup"><span data-stu-id="84769-105">DESCRIPTION</span></span>
<span data-ttu-id="84769-106">Polecenie cmdlet **Set-AzPrivateLinkService** umożliwia zaktualizowanie usługi linku prywatnego.</span><span class="sxs-lookup"><span data-stu-id="84769-106">The **Set-AzPrivateLinkService** cmdlet updates a private link service.</span></span>

## <span data-ttu-id="84769-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="84769-107">EXAMPLES</span></span>

### <span data-ttu-id="84769-108">1: Tworzenie usługi linku prywatnego i aktualizowanie jej</span><span class="sxs-lookup"><span data-stu-id="84769-108">1: Creates a private link service and update its</span></span>
```
$vnet = Get-AzVirtualNetwork -ResourceName "myvnet" -ResourceGroupName "myresourcegroup"
$IPConfig = New-AzPrivateLinkServiceIpConfig -Name "IP-Config" -Subnet $vnet.subnets[1] -PrivateIpAddress "10.0.0.5"
$publicip = Get-AzPublicIpAddress -ResourceGroupName "myresourcegroup"
$frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
$lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myresourcegroup" -Location "West US" -FrontendIpConfiguration $frontend  
$privateLinkService = New-AzPrivateLinkService -ServiceName "mypls" -ResourceGroupName myresourcegroup -Location "West US" -LoadBalancerFrontendIpConfiguration $frontend -IpConfiguration $IPConfig

$newIPConfig = New-AzPrivateLinkServiceIpConfig -Name "New-IP-Config" -Subnet $vnet.subnets[0] 
$privateLinkService.IpConfigurations[0] = $newIPConfig
$privateLinkService | Set-AzPrivateLinkService
```

<span data-ttu-id="84769-109">W tym przykładzie jest tworzona usługa linku prywatnego o nazwie mypls.</span><span class="sxs-lookup"><span data-stu-id="84769-109">This example creates a private link service called mypls.</span></span> <span data-ttu-id="84769-110">Następnie zastępuje on swoje elementy Ipconfiguration z obiektu ipConfiguratiuon w pamięci.</span><span class="sxs-lookup"><span data-stu-id="84769-110">Then it replace its ipConfigurations from the in-memory ipConfiguratiuon object.</span></span> <span data-ttu-id="84769-111">Polecenie cmdlet Set-AzPrivateLinkService jest następnie używane do napisania zmodyfikowanego stanu usługi link prywatny po stronie usługi.</span><span class="sxs-lookup"><span data-stu-id="84769-111">The Set-AzPrivateLinkService cmdlet is then used to write the modified private link service state on the service side.</span></span> 

## <span data-ttu-id="84769-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="84769-112">PARAMETERS</span></span>

### <span data-ttu-id="84769-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="84769-113">-AsJob</span></span>
<span data-ttu-id="84769-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="84769-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84769-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84769-115">-DefaultProfile</span></span>
<span data-ttu-id="84769-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="84769-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84769-117">-PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="84769-117">-PrivateLinkService</span></span>
<span data-ttu-id="84769-118">Określa prywatny obiekt usługi linku reprezentujący stan, do którego powinna być ustawiona usługa linku prywatnego.</span><span class="sxs-lookup"><span data-stu-id="84769-118">Specifies a private link service object representing the state to which the private link service should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84769-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84769-119">CommonParameters</span></span>
<span data-ttu-id="84769-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84769-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84769-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="84769-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84769-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="84769-122">INPUTS</span></span>

### <span data-ttu-id="84769-123">Microsoft. Azure. Commands. Network. models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="84769-123">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="84769-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="84769-124">OUTPUTS</span></span>

### <span data-ttu-id="84769-125">Microsoft. Azure. Commands. Network. models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="84769-125">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="84769-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="84769-126">NOTES</span></span>

## <span data-ttu-id="84769-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="84769-127">RELATED LINKS</span></span>

[<span data-ttu-id="84769-128">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="84769-128">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="84769-129">Nowe — AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="84769-129">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)

[<span data-ttu-id="84769-130">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="84769-130">Remove-AzPrivateLinkService</span></span>](./Remove-AzPrivateLinkService.md)


