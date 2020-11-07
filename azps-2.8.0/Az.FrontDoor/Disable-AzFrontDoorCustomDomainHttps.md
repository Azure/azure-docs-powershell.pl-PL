---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/disable-azfrontdoorcustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Disable-AzFrontDoorCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Disable-AzFrontDoorCustomDomainHttps.md
ms.openlocfilehash: 2f6b5635b029548f8d92917e0abfca18d5c0c415
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705407"
---
# <span data-ttu-id="c2b64-101">Disable-AzFrontDoorCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="c2b64-101">Disable-AzFrontDoorCustomDomainHttps</span></span>

## <span data-ttu-id="c2b64-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c2b64-102">SYNOPSIS</span></span>
<span data-ttu-id="c2b64-103">Wyłączanie protokołu HTTPS dla domeny niestandardowej</span><span class="sxs-lookup"><span data-stu-id="c2b64-103">Disable HTTPS for a custom domain</span></span>

## <span data-ttu-id="c2b64-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c2b64-104">SYNTAX</span></span>

### <span data-ttu-id="c2b64-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c2b64-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c2b64-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2b64-106">ByResourceIdParameterSet</span></span>
```
Disable-AzFrontDoorCustomDomainHttps -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2b64-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2b64-107">ByObjectParameterSet</span></span>
```
Disable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2b64-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c2b64-108">DESCRIPTION</span></span>
<span data-ttu-id="c2b64-109">**Element Disable-AzFrontDoorCustomDomainHttps** wyłącza HTTPS dla domeny niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="c2b64-109">The **Disable-AzFrontDoorCustomDomainHttps** disables HTTPS for a custom domain.</span></span>

## <span data-ttu-id="c2b64-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c2b64-110">EXAMPLES</span></span>

### <span data-ttu-id="c2b64-111">Przykład 1: wyłączanie protokołu HTTPS dla domeny niestandardowej z FrontDoorName i ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="c2b64-111">Example 1: Disable HTTPS for a custom domain with FrontDoorName and ResourceGroupName.</span></span>
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

<span data-ttu-id="c2b64-112">Wyłącz protokół HTTPS dla domeny niestandardowej "frontendpointname1-Custom-XYZ" z FrontDoorName jako "frontdoor1" i ResourceGroupName jako "resourcegroup1".</span><span class="sxs-lookup"><span data-stu-id="c2b64-112">Disable HTTPS for a custom domain "frontendpointname1-custom-xyz" with FrontDoorName as "frontdoor1" and ResourceGroupName as "resourcegroup1".</span></span>

### <span data-ttu-id="c2b64-113">Przykład 2: wyłączanie protokołu HTTPS dla domeny niestandardowej z obiektem PSFrontendEndpoint.</span><span class="sxs-lookup"><span data-stu-id="c2b64-113">Example 2: Disable HTTPS for a custom domain with PSFrontendEndpoint object.</span></span>
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

<span data-ttu-id="c2b64-114">Wyłącz protokół HTTPS dla domeny niestandardowej z obiektem PSFrontendEndpoint.</span><span class="sxs-lookup"><span data-stu-id="c2b64-114">Disable HTTPS for a custom domain with PSFrontendEndpoint object.</span></span>

### <span data-ttu-id="c2b64-115">Przykład 3: wyłączanie protokołu HTTPS dla domeny niestandardowej z identyfikatorem zasobu ResourceId.</span><span class="sxs-lookup"><span data-stu-id="c2b64-115">Example 3: Disable HTTPS for a custom domain with ResourceId.</span></span>
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

<span data-ttu-id="c2b64-116">Wyłącz protokół HTTPS dla domeny niestandardowej "frontendpointname1-Custom-XYZ" z identyfikatorem ResourceId jako $resourceId.</span><span class="sxs-lookup"><span data-stu-id="c2b64-116">Disable HTTPS for a custom domain "frontendpointname1-custom-xyz" with ResourceId as $resourceId.</span></span>

## <span data-ttu-id="c2b64-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c2b64-117">PARAMETERS</span></span>

### <span data-ttu-id="c2b64-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2b64-118">-DefaultProfile</span></span>
<span data-ttu-id="c2b64-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c2b64-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2b64-120">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="c2b64-120">-FrontDoorName</span></span>
<span data-ttu-id="c2b64-121">Nazwa przednich drzwi.</span><span class="sxs-lookup"><span data-stu-id="c2b64-121">The name of the Front Door.</span></span>

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

### <span data-ttu-id="c2b64-122">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="c2b64-122">-FrontendEndpointName</span></span>
<span data-ttu-id="c2b64-123">Nazwa punktu końcowego frontonu.</span><span class="sxs-lookup"><span data-stu-id="c2b64-123">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="c2b64-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c2b64-124">-InputObject</span></span>
<span data-ttu-id="c2b64-125">Obiekt punktu końcowego frontonu do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="c2b64-125">The Frontend endpoint object to update.</span></span>

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

### <span data-ttu-id="c2b64-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2b64-126">-ResourceGroupName</span></span>
<span data-ttu-id="c2b64-127">Grupa zasobów, do której należą przednia drzwi.</span><span class="sxs-lookup"><span data-stu-id="c2b64-127">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="c2b64-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2b64-128">-ResourceId</span></span>
<span data-ttu-id="c2b64-129">Identyfikator zasobu punktu końcowego z przednim Drzwiczkeniem w celu wyłączenia protokołu https</span><span class="sxs-lookup"><span data-stu-id="c2b64-129">Resource Id of the Front Door endpoint to disable https</span></span>

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

### <span data-ttu-id="c2b64-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c2b64-130">-Confirm</span></span>
<span data-ttu-id="c2b64-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2b64-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2b64-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2b64-132">-WhatIf</span></span>
<span data-ttu-id="c2b64-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2b64-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c2b64-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c2b64-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2b64-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2b64-135">CommonParameters</span></span>
<span data-ttu-id="c2b64-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2b64-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2b64-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2b64-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2b64-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c2b64-138">INPUTS</span></span>

### <span data-ttu-id="c2b64-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c2b64-139">System.String</span></span>

## <span data-ttu-id="c2b64-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c2b64-140">OUTPUTS</span></span>

### <span data-ttu-id="c2b64-141">Microsoft. Azure. Commands. FrontDoor. models. PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="c2b64-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="c2b64-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c2b64-142">NOTES</span></span>

## <span data-ttu-id="c2b64-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c2b64-143">RELATED LINKS</span></span>
