---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateLinkService.md
ms.openlocfilehash: a594e23505b9db1004a086ff4e0c168353c6bc28
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184170"
---
# <span data-ttu-id="ec4f6-101">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ec4f6-101">Set-AzPrivateLinkService</span></span>

## <span data-ttu-id="ec4f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec4f6-102">SYNOPSIS</span></span>
<span data-ttu-id="ec4f6-103">Aktualizuje prywatną usługę linków.</span><span class="sxs-lookup"><span data-stu-id="ec4f6-103">Updates a private link service.</span></span>

## <span data-ttu-id="ec4f6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ec4f6-104">SYNTAX</span></span>

```
Set-AzPrivateLinkService -PrivateLinkService <PSPrivateLinkService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec4f6-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ec4f6-105">DESCRIPTION</span></span>
<span data-ttu-id="ec4f6-106">Polecenie **cmdlet Set-AzPrivateLinkService** aktualizuje prywatną usługę linków.</span><span class="sxs-lookup"><span data-stu-id="ec4f6-106">The **Set-AzPrivateLinkService** cmdlet updates a private link service.</span></span>

## <span data-ttu-id="ec4f6-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ec4f6-107">EXAMPLES</span></span>

### <span data-ttu-id="ec4f6-108">1. Tworzy prywatną usługę linków i aktualizuje</span><span class="sxs-lookup"><span data-stu-id="ec4f6-108">1: Creates a private link service and update its</span></span>
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

<span data-ttu-id="ec4f6-109">W tym przykładzie jest wana prywatna usługa linków o nazwie mojepls.</span><span class="sxs-lookup"><span data-stu-id="ec4f6-109">This example creates a private link service called mypls.</span></span> <span data-ttu-id="ec4f6-110">Następnie zamienia swoje konfiguracje ipConfigurations z obiektu ipConfiguratiuon w pamięci.</span><span class="sxs-lookup"><span data-stu-id="ec4f6-110">Then it replace its ipConfigurations from the in-memory ipConfiguratiuon object.</span></span> <span data-ttu-id="ec4f6-111">Polecenie Set-AzPrivateLinkService cmdlet służy następnie do pisania zmodyfikowanego stanu usługi prywatnego linku po stronie usługi.</span><span class="sxs-lookup"><span data-stu-id="ec4f6-111">The Set-AzPrivateLinkService cmdlet is then used to write the modified private link service state on the service side.</span></span> 

## <span data-ttu-id="ec4f6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ec4f6-112">PARAMETERS</span></span>

### <span data-ttu-id="ec4f6-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="ec4f6-113">-AsJob</span></span>
<span data-ttu-id="ec4f6-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="ec4f6-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ec4f6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec4f6-115">-DefaultProfile</span></span>
<span data-ttu-id="ec4f6-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ec4f6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec4f6-117">-PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ec4f6-117">-PrivateLinkService</span></span>
<span data-ttu-id="ec4f6-118">Określa obiekt usługi łączenia prywatnego reprezentujący stan, dla którego należy ustawić prywatną usługę łączenia.</span><span class="sxs-lookup"><span data-stu-id="ec4f6-118">Specifies a private link service object representing the state to which the private link service should be set.</span></span>

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

### <span data-ttu-id="ec4f6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec4f6-119">CommonParameters</span></span>
<span data-ttu-id="ec4f6-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec4f6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec4f6-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ec4f6-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec4f6-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ec4f6-122">INPUTS</span></span>

### <span data-ttu-id="ec4f6-123">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ec4f6-123">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="ec4f6-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ec4f6-124">OUTPUTS</span></span>

### <span data-ttu-id="ec4f6-125">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ec4f6-125">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="ec4f6-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ec4f6-126">NOTES</span></span>

## <span data-ttu-id="ec4f6-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ec4f6-127">RELATED LINKS</span></span>

[<span data-ttu-id="ec4f6-128">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ec4f6-128">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="ec4f6-129">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ec4f6-129">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)

[<span data-ttu-id="ec4f6-130">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ec4f6-130">Remove-AzPrivateLinkService</span></span>](./Remove-AzPrivateLinkService.md)


