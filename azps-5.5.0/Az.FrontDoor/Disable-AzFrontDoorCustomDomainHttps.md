---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/disable-azfrontdoorcustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Disable-AzFrontDoorCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Disable-AzFrontDoorCustomDomainHttps.md
ms.openlocfilehash: 65c9bca6eb678ff3f3cb0a61d815f8415c715e43
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200347"
---
# <span data-ttu-id="73462-101">Disable-AzFrontDoorCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="73462-101">Disable-AzFrontDoorCustomDomainHttps</span></span>

## <span data-ttu-id="73462-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73462-102">SYNOPSIS</span></span>
<span data-ttu-id="73462-103">Wyłączanie protokołu HTTPS dla domeny niestandardowej</span><span class="sxs-lookup"><span data-stu-id="73462-103">Disable HTTPS for a custom domain</span></span>

## <span data-ttu-id="73462-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="73462-104">SYNTAX</span></span>

### <span data-ttu-id="73462-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="73462-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="73462-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="73462-106">ByResourceIdParameterSet</span></span>
```
Disable-AzFrontDoorCustomDomainHttps -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73462-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="73462-107">ByObjectParameterSet</span></span>
```
Disable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73462-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="73462-108">DESCRIPTION</span></span>
<span data-ttu-id="73462-109">Ustawienie **Disable-AzFrontDoorCustomDomainHttps** wyłącza protokół HTTPS dla domeny niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="73462-109">The **Disable-AzFrontDoorCustomDomainHttps** disables HTTPS for a custom domain.</span></span>

## <span data-ttu-id="73462-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="73462-110">EXAMPLES</span></span>

### <span data-ttu-id="73462-111">Przykład 1. Wyłączenie protokołu HTTPS dla domeny niestandardowej z wartościami FrontDoorName i ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="73462-111">Example 1: Disable HTTPS for a custom domain with FrontDoorName and ResourceGroupName.</span></span>
```powershell
PS C:\> Disable-AzFrontDoorCustomDomainHttps -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz"

HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabling
CustomHttpsProvisioningSubstate  : DeletingCertificate
CertificateSource                : FrontDoor
ProtocolType                     : ServerNameIndication
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

<span data-ttu-id="73462-112">Wyłącz protokół HTTPS dla domeny niestandardowej "frontendpointname1-custom-xyz" z nazwą FrontDoorName jako "frontdoor1" i ResourceGroupName jako "resourcegroup1".</span><span class="sxs-lookup"><span data-stu-id="73462-112">Disable HTTPS for a custom domain "frontendpointname1-custom-xyz" with FrontDoorName as "frontdoor1" and ResourceGroupName as "resourcegroup1".</span></span>

### <span data-ttu-id="73462-113">Przykład 2. Wyłączenie protokołu HTTPS dla domeny niestandardowej z obiektem PSFrontendEndpoint.</span><span class="sxs-lookup"><span data-stu-id="73462-113">Example 2: Disable HTTPS for a custom domain with PSFrontendEndpoint object.</span></span>
```powershell
PS C:\> Get-AzFrontDoorFrontendEndpoint -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz" | Disable-AzFrontDoorCustomDomainHttps -InputObject $frontendEndpointObj 

HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabling
CustomHttpsProvisioningSubstate  : DeletingCertificate
CertificateSource                : FrontDoor
ProtocolType                     : ServerNameIndication
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

<span data-ttu-id="73462-114">Wyłącz protokół HTTPS dla domeny niestandardowej za pomocą obiektu PSFrontendEndpoint.</span><span class="sxs-lookup"><span data-stu-id="73462-114">Disable HTTPS for a custom domain with PSFrontendEndpoint object.</span></span>

### <span data-ttu-id="73462-115">Przykład 3. Wyłączenie protokołu HTTPS dla domeny niestandardowej przy użyciu pola ResourceId.</span><span class="sxs-lookup"><span data-stu-id="73462-115">Example 3: Disable HTTPS for a custom domain with ResourceId.</span></span>
```powershell
PS C:\> Disable-AzFrontDoorCustomDomainHttps -ResourceId $resourceId 

HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabling
CustomHttpsProvisioningSubstate  : DeletingCertificate
CertificateSource                : FrontDoor
ProtocolType                     : ServerNameIndication
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

<span data-ttu-id="73462-116">Wyłącz protokół HTTPS dla domeny niestandardowej "frontendpointname1-custom-xyz" przy użyciu parametru ResourceId jako $resourceId.</span><span class="sxs-lookup"><span data-stu-id="73462-116">Disable HTTPS for a custom domain "frontendpointname1-custom-xyz" with ResourceId as $resourceId.</span></span>

## <span data-ttu-id="73462-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73462-117">PARAMETERS</span></span>

### <span data-ttu-id="73462-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73462-118">-DefaultProfile</span></span>
<span data-ttu-id="73462-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="73462-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73462-120">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="73462-120">-FrontDoorName</span></span>
<span data-ttu-id="73462-121">Nazwa drzwi frontowych.</span><span class="sxs-lookup"><span data-stu-id="73462-121">The name of the Front Door.</span></span>

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

### <span data-ttu-id="73462-122">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="73462-122">-FrontendEndpointName</span></span>
<span data-ttu-id="73462-123">Nazwa punktu końcowego frontendu.</span><span class="sxs-lookup"><span data-stu-id="73462-123">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="73462-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73462-124">-InputObject</span></span>
<span data-ttu-id="73462-125">Obiekt punktu końcowego frontendu do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="73462-125">The Frontend endpoint object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73462-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73462-126">-ResourceGroupName</span></span>
<span data-ttu-id="73462-127">Grupa zasobów, do której należy drzwi przednie.</span><span class="sxs-lookup"><span data-stu-id="73462-127">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="73462-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="73462-128">-ResourceId</span></span>
<span data-ttu-id="73462-129">Identyfikator zasobu punktu końcowego drzwi frontowych w celu wyłączenia https</span><span class="sxs-lookup"><span data-stu-id="73462-129">Resource Id of the Front Door endpoint to disable https</span></span>

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

### <span data-ttu-id="73462-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="73462-130">-Confirm</span></span>
<span data-ttu-id="73462-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="73462-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73462-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73462-132">-WhatIf</span></span>
<span data-ttu-id="73462-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73462-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="73462-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="73462-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73462-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73462-135">CommonParameters</span></span>
<span data-ttu-id="73462-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73462-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73462-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="73462-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73462-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="73462-138">INPUTS</span></span>

### <span data-ttu-id="73462-139">System.String</span><span class="sxs-lookup"><span data-stu-id="73462-139">System.String</span></span>

## <span data-ttu-id="73462-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="73462-140">OUTPUTS</span></span>

### <span data-ttu-id="73462-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="73462-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="73462-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="73462-142">NOTES</span></span>

## <span data-ttu-id="73462-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="73462-143">RELATED LINKS</span></span>
