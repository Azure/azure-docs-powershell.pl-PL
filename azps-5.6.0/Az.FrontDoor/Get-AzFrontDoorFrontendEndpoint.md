---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/get-azfrontdoorfrontendendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFrontendEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFrontendEndpoint.md
ms.openlocfilehash: 2887c343c9498eb2b8bde51b51226bffc5795ff3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954705"
---
# <span data-ttu-id="9fb2d-101">Get-AzFrontDoorFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="9fb2d-101">Get-AzFrontDoorFrontendEndpoint</span></span>

## <span data-ttu-id="9fb2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9fb2d-102">SYNOPSIS</span></span>
<span data-ttu-id="9fb2d-103">Uzyskaj punkt końcowy frontendu drzwi przednich.</span><span class="sxs-lookup"><span data-stu-id="9fb2d-103">Get a front door frontend endpoint.</span></span>

## <span data-ttu-id="9fb2d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9fb2d-104">SYNTAX</span></span>

### <span data-ttu-id="9fb2d-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="9fb2d-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzFrontDoorFrontendEndpoint -ResourceGroupName <String> -FrontDoorName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9fb2d-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9fb2d-106">ByObjectParameterSet</span></span>
```
Get-AzFrontDoorFrontendEndpoint [-Name <String>] -FrontDoorObject <PSFrontDoor>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9fb2d-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9fb2d-107">ByResourceIdParameterSet</span></span>
```
Get-AzFrontDoorFrontendEndpoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9fb2d-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="9fb2d-108">DESCRIPTION</span></span>
<span data-ttu-id="9fb2d-109">Polecenie **cmdlet Get-AzFrontDoorFrontendEndpoint** pobiera wszystkie istniejące punkty końcowe frontendu w bieżącym zasobie front door, który odpowiada podano informacje.</span><span class="sxs-lookup"><span data-stu-id="9fb2d-109">The **Get-AzFrontDoorFrontendEndpoint** cmdlet gets all existing frontend endpoints in the current Front Door resource that matches provided information.</span></span>

## <span data-ttu-id="9fb2d-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9fb2d-110">EXAMPLES</span></span>

### <span data-ttu-id="9fb2d-111">Przykład 1. Uzyskiwanie wszystkich punktów końcowych frontendu w front dooru "frontdoor1", który jest częścią grupy zasobów "rg1".</span><span class="sxs-lookup"><span data-stu-id="9fb2d-111">Example 1: Get all frontend endpoints in Front Door "frontdoor1" which is part of resource group "rg1".</span></span>
```powershell
PS C:\> Get-AzFrontDoorFrontendEndpoint -ResourceGroupName "rg1" -FrontDoorName "frontdoor1"


HostName                         : frontdoor1.azurefd.net
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabled
CustomHttpsProvisioningSubstate  : None
CertificateSource                :
ProtocolType                     :
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    : Enabled
Id                               : /subscriptions/{guid}/resourcegroups/resourcegroup1
                                   /providers/Microsoft.Network/frontdoors/frontdoor1/frontendendpoints/frontdoor1-azurefd-net
Name                             : frontdoor1-azurefd-net
Type                             : Microsoft.Network/frontdoors/frontendendpoints

HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabled
CustomHttpsProvisioningSubstate  : None
CertificateSource                :
ProtocolType                     :
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    : Enabled
Id                               : /subscriptions/{guid}/resourcegroups/resourcegroup1
                                   /providers/Microsoft.Network/frontdoors/frontdoor1/frontendendpoints/frontendpointname1-custom-xyz
Name                             : frontendpointname1-custom-xyz
Type                             : Microsoft.Network/frontdoors/frontendendpoints
```

<span data-ttu-id="9fb2d-112">Uzyskaj wszystkie punkty końcowe frontendu w frontonie "frontdoor1", który jest częścią grupy zasobów "rg1".</span><span class="sxs-lookup"><span data-stu-id="9fb2d-112">Get all frontend endpoints in Front Door "frontdoor1" which is part of resource group "rg1".</span></span>

### <span data-ttu-id="9fb2d-113">Przykład 2. Uzyskiwanie punktu końcowego frontendu o nazwie "frontdoor1-azurefd-net" w front dooru "frontdoor1", który jest częścią grupy zasobów "rg1"</span><span class="sxs-lookup"><span data-stu-id="9fb2d-113">Example 2: Get frontend endpoint with name "frontdoor1-azurefd-net" in Front Door "frontdoor1" which is part of resource group "rg1"</span></span>
```powershell
PS C:\> Get-AzFrontDoorFrontendEndpoint -ResourceGroupName "rg1" -FrontDoorName "frontdoor1" -Name "frontdoor1-azurefd-net"


HostName                         : frontdoor1.azurefd.net
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabled
CustomHttpsProvisioningSubstate  : None
CertificateSource                :
ProtocolType                     :
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    : Enabled
Id                               : /subscriptions/{guid}/resourcegroups/resourcegroup1
                                   /providers/Microsoft.Network/frontdoors/frontdoor1/frontendendpoints/frontdoor1-azurefd-net
Name                             : frontdoor1-azurefd-net
Type                             : Microsoft.Network/frontdoors/frontendendpoints
```

<span data-ttu-id="9fb2d-114">Uzyskaj punkt końcowy frontendu o nazwie "frontdoor1-azurefd-net" w front dooru "frontdoor1", który jest częścią grupy zasobów "rg1"</span><span class="sxs-lookup"><span data-stu-id="9fb2d-114">Get frontend endpoint with name "frontdoor1-azurefd-net" in Front Door "frontdoor1" which is part of resource group "rg1"</span></span>

## <span data-ttu-id="9fb2d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9fb2d-115">PARAMETERS</span></span>

### <span data-ttu-id="9fb2d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fb2d-116">-DefaultProfile</span></span>
<span data-ttu-id="9fb2d-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9fb2d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9fb2d-118">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="9fb2d-118">-FrontDoorName</span></span>
<span data-ttu-id="9fb2d-119">Nazwa drzwi przednich.</span><span class="sxs-lookup"><span data-stu-id="9fb2d-119">Front Door name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb2d-120">-FrontDoorObject</span><span class="sxs-lookup"><span data-stu-id="9fb2d-120">-FrontDoorObject</span></span>
<span data-ttu-id="9fb2d-121">Obiekt FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="9fb2d-121">The FrontDoor object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9fb2d-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9fb2d-122">-Name</span></span>
<span data-ttu-id="9fb2d-123">Nazwa punktu końcowego frontendu.</span><span class="sxs-lookup"><span data-stu-id="9fb2d-123">Frontend endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb2d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fb2d-124">-ResourceGroupName</span></span>
<span data-ttu-id="9fb2d-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9fb2d-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb2d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9fb2d-126">-ResourceId</span></span>
<span data-ttu-id="9fb2d-127">Identyfikator zasobu drzwi frontowych</span><span class="sxs-lookup"><span data-stu-id="9fb2d-127">Resource Id of the Front Door</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fb2d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fb2d-128">CommonParameters</span></span>
<span data-ttu-id="9fb2d-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fb2d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fb2d-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9fb2d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fb2d-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9fb2d-131">INPUTS</span></span>

### <span data-ttu-id="9fb2d-132">Brak</span><span class="sxs-lookup"><span data-stu-id="9fb2d-132">None</span></span>

## <span data-ttu-id="9fb2d-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9fb2d-133">OUTPUTS</span></span>

### <span data-ttu-id="9fb2d-134">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="9fb2d-134">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="9fb2d-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9fb2d-135">NOTES</span></span>

## <span data-ttu-id="9fb2d-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9fb2d-136">RELATED LINKS</span></span>
