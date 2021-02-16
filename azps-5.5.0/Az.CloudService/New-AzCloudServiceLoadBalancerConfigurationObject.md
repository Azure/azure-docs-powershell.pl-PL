---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.CloudService/new-AzCloudServiceLoadBalancerConfigurationObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceLoadBalancerConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceLoadBalancerConfigurationObject.md
ms.openlocfilehash: 6afabb94ae006cec122d7e89997be17c20e85b05
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199427"
---
# <span data-ttu-id="fd9d5-101">New-AzCloudServiceLoadBalancerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="fd9d5-101">New-AzCloudServiceLoadBalancerConfigurationObject</span></span>

## <span data-ttu-id="fd9d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd9d5-102">SYNOPSIS</span></span>
<span data-ttu-id="fd9d5-103">Tworzenie obiektu w pamięci na karcie LoadBalancerConfiguration</span><span class="sxs-lookup"><span data-stu-id="fd9d5-103">Create a in-memory object for LoadBalancerConfiguration</span></span>

## <span data-ttu-id="fd9d5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fd9d5-104">SYNTAX</span></span>

```
New-AzCloudServiceLoadBalancerConfigurationObject
 [-FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>] [-Name <String>] [<CommonParameters>]
```

## <span data-ttu-id="fd9d5-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="fd9d5-105">DESCRIPTION</span></span>
<span data-ttu-id="fd9d5-106">Tworzenie obiektu w pamięci na karcie LoadBalancerConfiguration</span><span class="sxs-lookup"><span data-stu-id="fd9d5-106">Create a in-memory object for LoadBalancerConfiguration</span></span>

## <span data-ttu-id="fd9d5-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fd9d5-107">EXAMPLES</span></span>

### <span data-ttu-id="fd9d5-108">Przykład 1. Tworzenie obiektu konfiguracji równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="fd9d5-108">Example 1: Create load balancer configuration object</span></span>
```powershell
PS C:\> $publicIP = Get-AzPublicIpAddress -ResourceGroupName 'ContosoOrg' -Name 'ContosoPublicIP'
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIP.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
```

<span data-ttu-id="fd9d5-109">To polecenie tworzy obiekt konfiguracji równoważenia obciążenia, który jest używany do tworzenia lub aktualizowania usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="fd9d5-109">This command creates load balancer configuration object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="fd9d5-110">Aby uzyskać więcej szczegółowych informacji, zobacz New-AzCloudService.</span><span class="sxs-lookup"><span data-stu-id="fd9d5-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="fd9d5-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd9d5-111">PARAMETERS</span></span>

### <span data-ttu-id="fd9d5-112">- FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="fd9d5-112">-FrontendIPConfiguration</span></span>
<span data-ttu-id="fd9d5-113">FrontendIPConfiguration.</span><span class="sxs-lookup"><span data-stu-id="fd9d5-113">FrontendIPConfiguration.</span></span>
<span data-ttu-id="fd9d5-114">Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach FRONTENDIPCONFIGURATION i utworzyć tabelę skrótów.</span><span class="sxs-lookup"><span data-stu-id="fd9d5-114">To construct, see NOTES section for FRONTENDIPCONFIGURATION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ILoadBalancerFrontendIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd9d5-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="fd9d5-115">-Name</span></span>
<span data-ttu-id="fd9d5-116">Nazwa konfiguracji LoadBalancerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="fd9d5-116">Name of LoadBalancerConfiguration.</span></span>

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

### <span data-ttu-id="fd9d5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd9d5-117">CommonParameters</span></span>
<span data-ttu-id="fd9d5-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd9d5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd9d5-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd9d5-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd9d5-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fd9d5-120">INPUTS</span></span>

## <span data-ttu-id="fd9d5-121">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fd9d5-121">OUTPUTS</span></span>

### <span data-ttu-id="fd9d5-122">Microsoft.Azure.PowerShell.cmdlet.CloudService.Models.Api20201001Preview.LoadBalancerConfiguration</span><span class="sxs-lookup"><span data-stu-id="fd9d5-122">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.LoadBalancerConfiguration</span></span>

## <span data-ttu-id="fd9d5-123">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fd9d5-123">NOTES</span></span>

<span data-ttu-id="fd9d5-124">ALIASY</span><span class="sxs-lookup"><span data-stu-id="fd9d5-124">ALIASES</span></span>

<span data-ttu-id="fd9d5-125">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fd9d5-125">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fd9d5-126">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="fd9d5-126">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fd9d5-127">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fd9d5-127">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fd9d5-128">FRONTENDIPCONFIGURATION <ILoadBalancerFrontendIPConfiguration[]>: FrontendIPConfiguration.</span><span class="sxs-lookup"><span data-stu-id="fd9d5-128">FRONTENDIPCONFIGURATION <ILoadBalancerFrontendIPConfiguration[]>: FrontendIPConfiguration.</span></span>
  - <span data-ttu-id="fd9d5-129">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="fd9d5-129">`[Name <String>]`:</span></span> 
  - <span data-ttu-id="fd9d5-130">`[PrivateIPAddress <String>]`: prywatny adres IP, do których odwołuje się usługa w chmurze.</span><span class="sxs-lookup"><span data-stu-id="fd9d5-130">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
  - <span data-ttu-id="fd9d5-131">`[PublicIPAddressId <String>]`: Identyfikator zasobu</span><span class="sxs-lookup"><span data-stu-id="fd9d5-131">`[PublicIPAddressId <String>]`: Resource Id</span></span>
  - <span data-ttu-id="fd9d5-132">`[SubnetId <String>]`: Identyfikator zasobu</span><span class="sxs-lookup"><span data-stu-id="fd9d5-132">`[SubnetId <String>]`: Resource Id</span></span>

## <span data-ttu-id="fd9d5-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fd9d5-133">RELATED LINKS</span></span>

