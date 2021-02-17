---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorfrontendendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFrontendEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFrontendEndpoint.md
ms.openlocfilehash: cc07dd366d5c82705a23e3b9276ee9d681c6ae2c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243587"
---
# <span data-ttu-id="de92c-101">Get-AzFrontDoorFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="de92c-101">Get-AzFrontDoorFrontendEndpoint</span></span>

## <span data-ttu-id="de92c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de92c-102">SYNOPSIS</span></span>
<span data-ttu-id="de92c-103">Uzyskaj punkt końcowy frontendu drzwi przednich.</span><span class="sxs-lookup"><span data-stu-id="de92c-103">Get a front door frontend endpoint.</span></span>

## <span data-ttu-id="de92c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="de92c-104">SYNTAX</span></span>

### <span data-ttu-id="de92c-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="de92c-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzFrontDoorFrontendEndpoint -ResourceGroupName <String> -FrontDoorName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de92c-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="de92c-106">ByObjectParameterSet</span></span>
```
Get-AzFrontDoorFrontendEndpoint [-Name <String>] -FrontDoorObject <PSFrontDoor>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de92c-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="de92c-107">ByResourceIdParameterSet</span></span>
```
Get-AzFrontDoorFrontendEndpoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="de92c-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="de92c-108">DESCRIPTION</span></span>
<span data-ttu-id="de92c-109">Polecenie **cmdlet Get-AzFrontDoorFrontendEndpoint** pobiera wszystkie istniejące punkty końcowe frontendu w bieżącym zasobie front door, który odpowiada podano informacje.</span><span class="sxs-lookup"><span data-stu-id="de92c-109">The **Get-AzFrontDoorFrontendEndpoint** cmdlet gets all existing frontend endpoints in the current Front Door resource that matches provided information.</span></span>

## <span data-ttu-id="de92c-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="de92c-110">EXAMPLES</span></span>

### <span data-ttu-id="de92c-111">Przykład 1. Uzyskaj wszystkie punkty końcowe frontendu w frontonie "frontdoor1", który jest częścią grupy zasobów "rg1".</span><span class="sxs-lookup"><span data-stu-id="de92c-111">Example 1: Get all frontend endpoints in Front Door "frontdoor1" which is part of resource group "rg1".</span></span>
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

<span data-ttu-id="de92c-112">Uzyskaj wszystkie punkty końcowe frontendu w frontonie "frontdoor1", który jest częścią grupy zasobów "rg1".</span><span class="sxs-lookup"><span data-stu-id="de92c-112">Get all frontend endpoints in Front Door "frontdoor1" which is part of resource group "rg1".</span></span>

### <span data-ttu-id="de92c-113">Przykład 2. Uzyskiwanie punktu końcowego frontendu o nazwie "frontdoor1-azurefd-net" w front dooru "frontdoor1", który jest częścią grupy zasobów "rg1"</span><span class="sxs-lookup"><span data-stu-id="de92c-113">Example 2: Get frontend endpoint with name "frontdoor1-azurefd-net" in Front Door "frontdoor1" which is part of resource group "rg1"</span></span>
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

<span data-ttu-id="de92c-114">Uzyskaj punkt końcowy frontendu o nazwie "frontdoor1-azurefd-net" w front dooru "frontdoor1", który jest częścią grupy zasobów "rg1"</span><span class="sxs-lookup"><span data-stu-id="de92c-114">Get frontend endpoint with name "frontdoor1-azurefd-net" in Front Door "frontdoor1" which is part of resource group "rg1"</span></span>

## <span data-ttu-id="de92c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="de92c-115">PARAMETERS</span></span>

### <span data-ttu-id="de92c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de92c-116">-DefaultProfile</span></span>
<span data-ttu-id="de92c-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="de92c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de92c-118">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="de92c-118">-FrontDoorName</span></span>
<span data-ttu-id="de92c-119">Nazwa drzwi przednich.</span><span class="sxs-lookup"><span data-stu-id="de92c-119">Front Door name.</span></span>

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

### <span data-ttu-id="de92c-120">-FrontDoorObject</span><span class="sxs-lookup"><span data-stu-id="de92c-120">-FrontDoorObject</span></span>
<span data-ttu-id="de92c-121">Obiekt FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="de92c-121">The FrontDoor object.</span></span>

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

### <span data-ttu-id="de92c-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="de92c-122">-Name</span></span>
<span data-ttu-id="de92c-123">Nazwa punktu końcowego frontendu.</span><span class="sxs-lookup"><span data-stu-id="de92c-123">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="de92c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de92c-124">-ResourceGroupName</span></span>
<span data-ttu-id="de92c-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="de92c-125">The resource group name.</span></span>

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

### <span data-ttu-id="de92c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="de92c-126">-ResourceId</span></span>
<span data-ttu-id="de92c-127">Identyfikator zasobu drzwi frontowych</span><span class="sxs-lookup"><span data-stu-id="de92c-127">Resource Id of the Front Door</span></span>

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

### <span data-ttu-id="de92c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de92c-128">CommonParameters</span></span>
<span data-ttu-id="de92c-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de92c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de92c-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="de92c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de92c-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="de92c-131">INPUTS</span></span>

### <span data-ttu-id="de92c-132">Brak</span><span class="sxs-lookup"><span data-stu-id="de92c-132">None</span></span>

## <span data-ttu-id="de92c-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="de92c-133">OUTPUTS</span></span>

### <span data-ttu-id="de92c-134">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="de92c-134">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="de92c-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="de92c-135">NOTES</span></span>

## <span data-ttu-id="de92c-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="de92c-136">RELATED LINKS</span></span>
