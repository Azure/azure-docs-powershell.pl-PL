---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorfrontendendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFrontendEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFrontendEndpoint.md
ms.openlocfilehash: f685bb7bdad663e84a67397c89568d2263d0ed9a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705399"
---
# <span data-ttu-id="ea0b8-101">Get-AzFrontDoorFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="ea0b8-101">Get-AzFrontDoorFrontendEndpoint</span></span>

## <span data-ttu-id="ea0b8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ea0b8-102">SYNOPSIS</span></span>
<span data-ttu-id="ea0b8-103">Pobierz przedni punkt końcowy frontonu dla drzwi.</span><span class="sxs-lookup"><span data-stu-id="ea0b8-103">Get a front door frontend endpoint.</span></span>

## <span data-ttu-id="ea0b8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ea0b8-104">SYNTAX</span></span>

### <span data-ttu-id="ea0b8-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ea0b8-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzFrontDoorFrontendEndpoint -ResourceGroupName <String> -FrontDoorName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea0b8-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea0b8-106">ByObjectParameterSet</span></span>
```
Get-AzFrontDoorFrontendEndpoint [-Name <String>] -FrontDoorObject <PSFrontDoor>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea0b8-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea0b8-107">ByResourceIdParameterSet</span></span>
```
Get-AzFrontDoorFrontendEndpoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ea0b8-108">Opis</span><span class="sxs-lookup"><span data-stu-id="ea0b8-108">DESCRIPTION</span></span>
<span data-ttu-id="ea0b8-109">Polecenie cmdlet **Get-AzFrontDoorFrontendEndpoint** pobiera wszystkie istniejące punkty końcowe frontonu w bieżącym zasobie z przodu, które pasują do podanych informacji.</span><span class="sxs-lookup"><span data-stu-id="ea0b8-109">The **Get-AzFrontDoorFrontendEndpoint** cmdlet gets all existing frontend endpoints in the current Front Door resource that matches provided information.</span></span>

## <span data-ttu-id="ea0b8-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ea0b8-110">EXAMPLES</span></span>

### <span data-ttu-id="ea0b8-111">Przykład 1: uzyskiwanie wszystkich punktów końcowych frontonu w przednich drzwiach "frontdoor1", które są częścią grupy zasobów "RG1".</span><span class="sxs-lookup"><span data-stu-id="ea0b8-111">Example 1: Get all frontend endpoints in Front Door "frontdoor1" which is part of resource group "rg1".</span></span>
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

<span data-ttu-id="ea0b8-112">Pobierz wszystkie punkty końcowe frontonu w przód "frontdoor1", który jest częścią grupy zasobów "RG1".</span><span class="sxs-lookup"><span data-stu-id="ea0b8-112">Get all frontend endpoints in Front Door "frontdoor1" which is part of resource group "rg1".</span></span>

### <span data-ttu-id="ea0b8-113">Przykład 2: pobieranie punktu końcowego frontonu o nazwie "frontdoor1-azurefd-NET" w przednich drzwiach "frontdoor1", który jest częścią grupy zasobów "RG1"</span><span class="sxs-lookup"><span data-stu-id="ea0b8-113">Example 2: Get frontend endpoint with name "frontdoor1-azurefd-net" in Front Door "frontdoor1" which is part of resource group "rg1"</span></span>
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

<span data-ttu-id="ea0b8-114">Pobierz punkt końcowy frontonu o nazwie "frontdoor1-azurefd-NET" w przednich drzwiach "frontdoor1", który jest częścią grupy zasobów "RG1"</span><span class="sxs-lookup"><span data-stu-id="ea0b8-114">Get frontend endpoint with name "frontdoor1-azurefd-net" in Front Door "frontdoor1" which is part of resource group "rg1"</span></span>

## <span data-ttu-id="ea0b8-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ea0b8-115">PARAMETERS</span></span>

### <span data-ttu-id="ea0b8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea0b8-116">-DefaultProfile</span></span>
<span data-ttu-id="ea0b8-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ea0b8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea0b8-118">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="ea0b8-118">-FrontDoorName</span></span>
<span data-ttu-id="ea0b8-119">Imię i nazwisko drzwi przednie.</span><span class="sxs-lookup"><span data-stu-id="ea0b8-119">Front Door name.</span></span>

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

### <span data-ttu-id="ea0b8-120">-FrontDoorObject</span><span class="sxs-lookup"><span data-stu-id="ea0b8-120">-FrontDoorObject</span></span>
<span data-ttu-id="ea0b8-121">Obiekt FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="ea0b8-121">The FrontDoor object.</span></span>

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

### <span data-ttu-id="ea0b8-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ea0b8-122">-Name</span></span>
<span data-ttu-id="ea0b8-123">Nazwa punktu końcowego frontonu.</span><span class="sxs-lookup"><span data-stu-id="ea0b8-123">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="ea0b8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea0b8-124">-ResourceGroupName</span></span>
<span data-ttu-id="ea0b8-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ea0b8-125">The resource group name.</span></span>

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

### <span data-ttu-id="ea0b8-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea0b8-126">-ResourceId</span></span>
<span data-ttu-id="ea0b8-127">Identyfikator zasobu Przednie drzwi</span><span class="sxs-lookup"><span data-stu-id="ea0b8-127">Resource Id of the Front Door</span></span>

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

### <span data-ttu-id="ea0b8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea0b8-128">CommonParameters</span></span>
<span data-ttu-id="ea0b8-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea0b8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea0b8-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ea0b8-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea0b8-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ea0b8-131">INPUTS</span></span>

### <span data-ttu-id="ea0b8-132">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="ea0b8-132">None</span></span>

## <span data-ttu-id="ea0b8-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ea0b8-133">OUTPUTS</span></span>

### <span data-ttu-id="ea0b8-134">Microsoft. Azure. Commands. FrontDoor. models. PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="ea0b8-134">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="ea0b8-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ea0b8-135">NOTES</span></span>

## <span data-ttu-id="ea0b8-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ea0b8-136">RELATED LINKS</span></span>
