---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.CloudService/new-AzCloudServiceLoadBalancerFrontendIPConfigurationObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject.md
ms.openlocfilehash: cdd983e2ede5cd06c3b9b00805b337eac5b73a9b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195123"
---
# <span data-ttu-id="75b98-101">New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="75b98-101">New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject</span></span>

## <span data-ttu-id="75b98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75b98-102">SYNOPSIS</span></span>
<span data-ttu-id="75b98-103">Tworzenie obiektu w pamięci na karcie LoadBalancerFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="75b98-103">Create a in-memory object for LoadBalancerFrontendIPConfiguration</span></span>

## <span data-ttu-id="75b98-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="75b98-104">SYNTAX</span></span>

```
New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject [-Name <String>] [-PublicIPAddressId <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="75b98-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="75b98-105">DESCRIPTION</span></span>
<span data-ttu-id="75b98-106">Tworzenie obiektu w pamięci na karcie LoadBalancerFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="75b98-106">Create a in-memory object for LoadBalancerFrontendIPConfiguration</span></span>

## <span data-ttu-id="75b98-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="75b98-107">EXAMPLES</span></span>

### <span data-ttu-id="75b98-108">Przykład 1. Tworzenie obiektu konfiguracji frontendu IP równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="75b98-108">Example 1: Create load balancer frontend IP configuration object</span></span>
```powershell
PS C:\> $publicIP = Get-AzPublicIpAddress -ResourceGroupName 'ContosoOrg' -Name 'ContosoPublicIP'
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIp.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
```

<span data-ttu-id="75b98-109">To polecenie tworzy obiekt konfiguracji frontendu IP równoważenia obciążenia, który jest używany do tworzenia lub aktualizowania usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="75b98-109">This command creates load balancer frontend IP configuration object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="75b98-110">Aby uzyskać więcej szczegółowych informacji, zobacz New-AzCloudService.</span><span class="sxs-lookup"><span data-stu-id="75b98-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="75b98-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75b98-111">PARAMETERS</span></span>

### <span data-ttu-id="75b98-112">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="75b98-112">-Name</span></span>
<span data-ttu-id="75b98-113">Nazwa konfiguracji FrontendIpConfigration.</span><span class="sxs-lookup"><span data-stu-id="75b98-113">Name of FrontendIpConfigration.</span></span>

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

### <span data-ttu-id="75b98-114">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="75b98-114">-PublicIPAddressId</span></span>
<span data-ttu-id="75b98-115">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="75b98-115">Resource Id.</span></span>

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

### <span data-ttu-id="75b98-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75b98-116">CommonParameters</span></span>
<span data-ttu-id="75b98-117">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75b98-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75b98-118">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="75b98-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75b98-119">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="75b98-119">INPUTS</span></span>

## <span data-ttu-id="75b98-120">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="75b98-120">OUTPUTS</span></span>

### <span data-ttu-id="75b98-121">Microsoft.Azure.PowerShell.Cmdlet.CloudService.Models.Api20201001Preview.LoadBalancerFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="75b98-121">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.LoadBalancerFrontendIPConfiguration</span></span>

## <span data-ttu-id="75b98-122">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="75b98-122">NOTES</span></span>

<span data-ttu-id="75b98-123">ALIASY</span><span class="sxs-lookup"><span data-stu-id="75b98-123">ALIASES</span></span>

## <span data-ttu-id="75b98-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="75b98-124">RELATED LINKS</span></span>

