---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/enable-azfrontdoorcustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Enable-AzFrontDoorCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Enable-AzFrontDoorCustomDomainHttps.md
ms.openlocfilehash: 6d3eb8d4cbeb2a8c40e3fc6fbf0f54e8973e8f79
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243602"
---
# <span data-ttu-id="ae032-101">Enable-AzFrontDoorCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="ae032-101">Enable-AzFrontDoorCustomDomainHttps</span></span>

## <span data-ttu-id="ae032-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae032-102">SYNOPSIS</span></span>
<span data-ttu-id="ae032-103">Włącz protokół HTTPS dla domeny niestandardowej przy użyciu certyfikatu zarządzanego frontem drzwi lub własnego certyfikatu z magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ae032-103">Enable HTTPS for a custom domain using Front Door managed certificate or using own certificate from Azure Key Vault.</span></span>

## <span data-ttu-id="ae032-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ae032-104">SYNTAX</span></span>

### <span data-ttu-id="ae032-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="ae032-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae032-106">ByFieldsWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae032-106">ByFieldsWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> -VaultId <String> -SecretName <String> -SecretVersion <String>
 [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ae032-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae032-107">ByResourceIdParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceId <String> [-MinimumTlsVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae032-108">ByResourceIdWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae032-108">ByResourceIdWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceId <String> -VaultId <String> -SecretName <String>
 -SecretVersion <String> [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae032-109">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae032-109">ByObjectParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint> [-MinimumTlsVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae032-110">ByObjectWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae032-110">ByObjectWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint> -VaultId <String> -SecretName <String>
 -SecretVersion <String> [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae032-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="ae032-111">DESCRIPTION</span></span>
<span data-ttu-id="ae032-112">Funkcja **Enable-AzFrontDoorCustomDomainHttps** włącza protokół HTTPS dla domeny niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="ae032-112">The **Enable-AzFrontDoorCustomDomainHttps** enables HTTPS for a custom domain.</span></span>

## <span data-ttu-id="ae032-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ae032-113">EXAMPLES</span></span>

### <span data-ttu-id="ae032-114">Przykład 1. Włączanie protokołu HTTPS dla domeny niestandardowej za pomocą właściwości FrontDoorName i ResourceGroupName przy użyciu certyfikatu zarządzanego front door.</span><span class="sxs-lookup"><span data-stu-id="ae032-114">Example 1: Enable HTTPS for a custom domain with FrontDoorName and ResourceGroupName using Front Door managed certificate.</span></span>
```powershell
PS C:\> Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz" -MinimumTlsVersion "1.2"


HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Enabling
CustomHttpsProvisioningSubstate  : SubmittingDomainControlValidationRequest
CertificateSource                : FrontDoor
ProtocolType                     : ServerNameIndication
MinimumTlsVersion                : 1.2
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

<span data-ttu-id="ae032-115">Włącz protokół HTTPS dla domeny niestandardowej "frontendpointname1-custom-xyz", która jest częścią frontdooru "frontdoor1" w grupie zasobów "resourcegroup1" przy użyciu certyfikatu zarządzanego front door.</span><span class="sxs-lookup"><span data-stu-id="ae032-115">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" that is part of Front Door "frontdoor1" in resource group "resourcegroup1" using Front Door managed certificate.</span></span>

### <span data-ttu-id="ae032-116">Przykład 2. Włączanie protokołu HTTPS dla domeny niestandardowej za pomocą właściwości FrontDoorName i ResourceGroupName przy użyciu własnego certyfikatu w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="ae032-116">Example 2: Enable HTTPS for a custom domain with FrontDoorName and ResourceGroupName using own certificate in Key Vault.</span></span>
```powershell
PS C:\> $vaultId = (Get-AzKeyVault -VaultName $vaultName).ResourceId
PS C:\> Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz" -Vault $vaultId -secretName $secretName -SecretVersion $secretVersion -MinimumTlsVersion "1.0"


HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Enabling
CustomHttpsProvisioningSubstate  : SubmittingDomainControlValidationRequest
CertificateSource                : AzureKeyVault
ProtocolType                     : ServerNameIndication
MinimumTlsVersion                : 1.0
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

<span data-ttu-id="ae032-117">Włącz protokół HTTPS dla domeny niestandardowej "frontendpointname1-custom-xyz", która jest częścią frontdooru "frontdoor1" w grupie zasobów "resourcegroup1" przy użyciu certyfikatu zarządzanego front door.</span><span class="sxs-lookup"><span data-stu-id="ae032-117">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" that is part of Front Door "frontdoor1" in resource group "resourcegroup1" using Front Door managed certificate.</span></span>

### <span data-ttu-id="ae032-118">Przykład 3. Włączanie protokołu HTTPS dla domeny niestandardowej przy użyciu obiektu PSFrontendEndpoint przy użyciu certyfikatu zarządzanego front door.</span><span class="sxs-lookup"><span data-stu-id="ae032-118">Example 3: Enable HTTPS for a custom domain with PSFrontendEndpoint object using Front Door managed certificate.</span></span>
```powershell
PS C:\> Get-AzFrontDoorFrontendEndpoint -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -Name "frontendpointname1-custom-xyz" | Enable-AzFrontDoorCustomDomainHttps 


HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Enabling
CustomHttpsProvisioningSubstate  : SubmittingDomainControlValidationRequest
CertificateSource                : FrontDoor
ProtocolType                     : ServerNameIndication
MinimumTlsVersion                : 1.2
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

<span data-ttu-id="ae032-119">Włącz protokół HTTPS dla domeny niestandardowej za pomocą obiektu PSFrontendEndpoint przy użyciu certyfikatu zarządzanego przez front door.</span><span class="sxs-lookup"><span data-stu-id="ae032-119">Enable HTTPS for a custom domain with PSFrontendEndpoint object using Front Door managed certificate.</span></span>

### <span data-ttu-id="ae032-120">Przykład 4. Włączanie protokołu HTTPS dla domeny niestandardowej z identyfikatorem zasobu przy użyciu certyfikatu zarządzanego przez front door.</span><span class="sxs-lookup"><span data-stu-id="ae032-120">Example 4: Enable HTTPS for a custom domain with resource id using Front Door managed certificate.</span></span>
```powershell
PS C:\> Enable-AzFrontDoorCustomDomainHttps -ResourceId $resourceId


HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Enabling
CustomHttpsProvisioningSubstate  : SubmittingDomainControlValidationRequest
CertificateSource                : FrontDoor
ProtocolType                     : ServerNameIndication
MinimumTlsVersion                : 1.2
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

<span data-ttu-id="ae032-121">Włącz protokół HTTPS dla domeny niestandardowej "frontendpointname1-custom-xyz" przy użyciu identyfikatora zasobu $resourceId użyciu certyfikatu zarządzanego front door.</span><span class="sxs-lookup"><span data-stu-id="ae032-121">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" with resource id $resourceId using Front Door managed certificate.</span></span>

## <span data-ttu-id="ae032-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae032-122">PARAMETERS</span></span>

### <span data-ttu-id="ae032-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae032-123">-DefaultProfile</span></span>
<span data-ttu-id="ae032-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ae032-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae032-125">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="ae032-125">-FrontDoorName</span></span>
<span data-ttu-id="ae032-126">Nazwa drzwi frontowych.</span><span class="sxs-lookup"><span data-stu-id="ae032-126">The name of the Front Door.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae032-127">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="ae032-127">-FrontendEndpointName</span></span>
<span data-ttu-id="ae032-128">Nazwa punktu końcowego frontendu.</span><span class="sxs-lookup"><span data-stu-id="ae032-128">Frontend endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae032-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae032-129">-InputObject</span></span>
<span data-ttu-id="ae032-130">Obiekt punktu końcowego frontendu do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="ae032-130">The Frontend endpoint object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint
Parameter Sets: ByObjectParameterSet, ByObjectWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae032-131">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="ae032-131">-MinimumTlsVersion</span></span>
<span data-ttu-id="ae032-132">Minimalna wersja TLS wymagana przez klientów do nawiązania uścisku SSL z drzwiami przednimi.</span><span class="sxs-lookup"><span data-stu-id="ae032-132">The minimum TLS version required from the clients to establish an SSL handshake with Front Door.</span></span>

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

### <span data-ttu-id="ae032-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae032-133">-ResourceGroupName</span></span>
<span data-ttu-id="ae032-134">Grupa zasobów, do której należy drzwi przednie.</span><span class="sxs-lookup"><span data-stu-id="ae032-134">The resource group to which the Front Door belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae032-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae032-135">-ResourceId</span></span>
<span data-ttu-id="ae032-136">Identyfikator zasobu punktu końcowego drzwi frontowych w celu włączenia https</span><span class="sxs-lookup"><span data-stu-id="ae032-136">Resource Id of the Front Door endpoint to enable https</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet, ByResourceIdWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae032-137">-SecretName</span><span class="sxs-lookup"><span data-stu-id="ae032-137">-SecretName</span></span>
<span data-ttu-id="ae032-138">Nazwa klucza magazynu kluczy reprezentująca pełny certyfikat PFX</span><span class="sxs-lookup"><span data-stu-id="ae032-138">The name of the Key Vault secret representing the full certificate PFX</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithVaultParameterSet, ByResourceIdWithVaultParameterSet, ByObjectWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae032-139">- SecretVersion</span><span class="sxs-lookup"><span data-stu-id="ae032-139">-SecretVersion</span></span>
<span data-ttu-id="ae032-140">Wersja klucza klucza o kluczu tajnym reprezentująca pełny certyfikat PFX</span><span class="sxs-lookup"><span data-stu-id="ae032-140">The version of the Key Vault secret representing the full certificate PFX</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithVaultParameterSet, ByResourceIdWithVaultParameterSet, ByObjectWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae032-141">-VaultId</span><span class="sxs-lookup"><span data-stu-id="ae032-141">-VaultId</span></span>
<span data-ttu-id="ae032-142">Identyfikator magazynu kluczy zawierający certyfikat SSL</span><span class="sxs-lookup"><span data-stu-id="ae032-142">The Key Vault id containing the SSL certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithVaultParameterSet, ByResourceIdWithVaultParameterSet, ByObjectWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae032-143">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ae032-143">-Confirm</span></span>
<span data-ttu-id="ae032-144">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ae032-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae032-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae032-145">-WhatIf</span></span>
<span data-ttu-id="ae032-146">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae032-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ae032-147">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ae032-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae032-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae032-148">CommonParameters</span></span>
<span data-ttu-id="ae032-149">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae032-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae032-150">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ae032-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae032-151">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae032-151">INPUTS</span></span>

### <span data-ttu-id="ae032-152">System.String</span><span class="sxs-lookup"><span data-stu-id="ae032-152">System.String</span></span>
## <span data-ttu-id="ae032-153">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ae032-153">OUTPUTS</span></span>

### <span data-ttu-id="ae032-154">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="ae032-154">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>
## <span data-ttu-id="ae032-155">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ae032-155">NOTES</span></span>

## <span data-ttu-id="ae032-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ae032-156">RELATED LINKS</span></span>
