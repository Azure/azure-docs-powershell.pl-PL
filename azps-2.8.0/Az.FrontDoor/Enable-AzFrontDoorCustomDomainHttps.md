---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/enable-azfrontdoorcustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Enable-AzFrontDoorCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Enable-AzFrontDoorCustomDomainHttps.md
ms.openlocfilehash: 6edf891d693e0c1cb2143236d12e623fdd2b4a3f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705405"
---
# <span data-ttu-id="d73fc-101">Enable-AzFrontDoorCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="d73fc-101">Enable-AzFrontDoorCustomDomainHttps</span></span>

## <span data-ttu-id="d73fc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d73fc-102">SYNOPSIS</span></span>
<span data-ttu-id="d73fc-103">Włączanie protokołu HTTPS dla domeny niestandardowej przy użyciu certyfikatu z zarządzanym Drzwiczką drzwi lub z użyciem własnego certyfikatu w magazynie kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d73fc-103">Enable HTTPS for a custom domain using Front Door managed certificate or using own certificate from Azure Key Vault.</span></span>

## <span data-ttu-id="d73fc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d73fc-104">SYNTAX</span></span>

### <span data-ttu-id="d73fc-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d73fc-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d73fc-106">ByFieldsWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="d73fc-106">ByFieldsWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> -VaultId <String> -SecretName <String> -SecretVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d73fc-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d73fc-107">ByResourceIdParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d73fc-108">ByResourceIdWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="d73fc-108">ByResourceIdWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceId <String> -VaultId <String> -SecretName <String>
 -SecretVersion <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d73fc-109">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d73fc-109">ByObjectParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d73fc-110">ByObjectWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="d73fc-110">ByObjectWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint> -VaultId <String> -SecretName <String>
 -SecretVersion <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d73fc-111">Opis</span><span class="sxs-lookup"><span data-stu-id="d73fc-111">DESCRIPTION</span></span>
<span data-ttu-id="d73fc-112">**Enable-AzFrontDoorCustomDomainHttps** włącza HTTPS dla domeny niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="d73fc-112">The **Enable-AzFrontDoorCustomDomainHttps** enables HTTPS for a custom domain.</span></span>

## <span data-ttu-id="d73fc-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d73fc-113">EXAMPLES</span></span>

### <span data-ttu-id="d73fc-114">Przykład 1: Włączanie protokołu HTTPS dla domeny niestandardowej z FrontDoorName i ResourceGroupName przy użyciu certyfikatu z zarządzanym drzwiami przednimi.</span><span class="sxs-lookup"><span data-stu-id="d73fc-114">Example 1: Enable HTTPS for a custom domain with FrontDoorName and ResourceGroupName using Front Door managed certificate.</span></span>
```powershell
PS C:\> Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz"


HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Enabling
CustomHttpsProvisioningSubstate  : SubmittingDomainControlValidationRequest
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

<span data-ttu-id="d73fc-115">Włącz protokół HTTPS dla domeny niestandardowej "frontendpointname1-Custom-XYZ", która jest częścią przednich drzwi "frontdoor1" w grupie zasobów "resourcegroup1" przy użyciu certyfikatu z zarządzanym drzwiczkami.</span><span class="sxs-lookup"><span data-stu-id="d73fc-115">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" that is part of Front Door "frontdoor1" in resource group "resourcegroup1" using Front Door managed certificate.</span></span>

### <span data-ttu-id="d73fc-116">Przykład 2: Włączanie protokołu HTTPS dla domeny niestandardowej z FrontDoorName i ResourceGroupName przy użyciu certyfikatu własnego w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="d73fc-116">Example 2: Enable HTTPS for a custom domain with FrontDoorName and ResourceGroupName using own certificate in Key Vault.</span></span>
```powershell
PS C:\> $vaultId = (Get-AzKeyVault -VaultName $vaultName).ResourceId
PS C:\> Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz" -Vault $vaultId -secretName $secretName -SecretVersion $secretVersion


HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Enabling
CustomHttpsProvisioningSubstate  : SubmittingDomainControlValidationRequest
CertificateSource                : AzureKeyVault
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

<span data-ttu-id="d73fc-117">Włącz protokół HTTPS dla domeny niestandardowej "frontendpointname1-Custom-XYZ", która jest częścią przednich drzwi "frontdoor1" w grupie zasobów "resourcegroup1" przy użyciu certyfikatu z zarządzanym drzwiczkami.</span><span class="sxs-lookup"><span data-stu-id="d73fc-117">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" that is part of Front Door "frontdoor1" in resource group "resourcegroup1" using Front Door managed certificate.</span></span>

### <span data-ttu-id="d73fc-118">Przykład 3: Włączanie protokołu HTTPS dla domeny niestandardowej z obiektem PSFrontendEndpoint przy użyciu certyfikatu z zarządzanym drzwiami przednimi.</span><span class="sxs-lookup"><span data-stu-id="d73fc-118">Example 3: Enable HTTPS for a custom domain with PSFrontendEndpoint object using Front Door managed certificate.</span></span>
```powershell
PS C:\> Get-AzFrontDoorFrontendEndpoint -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz" | Enable-AzFrontDoorCustomDomainHttps 


HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Enabling
CustomHttpsProvisioningSubstate  : SubmittingDomainControlValidationRequest
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

<span data-ttu-id="d73fc-119">Włączanie protokołu HTTPS dla domeny niestandardowej z obiektem PSFrontendEndpoint przy użyciu certyfikatu z zarządzanym drzwiami przednimi.</span><span class="sxs-lookup"><span data-stu-id="d73fc-119">Enable HTTPS for a custom domain with PSFrontendEndpoint object using Front Door managed certificate.</span></span>

### <span data-ttu-id="d73fc-120">Przykład 4: Włączanie protokołu HTTPS dla domeny niestandardowej z identyfikatorem zasobu przy użyciu certyfikatu zarządzanego drzwi przednich.</span><span class="sxs-lookup"><span data-stu-id="d73fc-120">Example 4: Enable HTTPS for a custom domain with resource id using Front Door managed certificate.</span></span>
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

<span data-ttu-id="d73fc-121">Włączanie protokołu HTTPS dla domeny niestandardowej "frontendpointname1-Custom-XYZ" z identyfikatorem zasobu $resourceId użyciu certyfikatu z zarządzanym drzwiami przednimi.</span><span class="sxs-lookup"><span data-stu-id="d73fc-121">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" with resource id $resourceId using Front Door managed certificate.</span></span>

## <span data-ttu-id="d73fc-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d73fc-122">PARAMETERS</span></span>

### <span data-ttu-id="d73fc-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d73fc-123">-DefaultProfile</span></span>
<span data-ttu-id="d73fc-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d73fc-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d73fc-125">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="d73fc-125">-FrontDoorName</span></span>
<span data-ttu-id="d73fc-126">Nazwa przednich drzwi.</span><span class="sxs-lookup"><span data-stu-id="d73fc-126">The name of the Front Door.</span></span>

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

### <span data-ttu-id="d73fc-127">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="d73fc-127">-FrontendEndpointName</span></span>
<span data-ttu-id="d73fc-128">Nazwa punktu końcowego frontonu.</span><span class="sxs-lookup"><span data-stu-id="d73fc-128">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="d73fc-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d73fc-129">-InputObject</span></span>
<span data-ttu-id="d73fc-130">Obiekt punktu końcowego frontonu do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="d73fc-130">The Frontend endpoint object to update.</span></span>

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

### <span data-ttu-id="d73fc-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d73fc-131">-ResourceGroupName</span></span>
<span data-ttu-id="d73fc-132">Grupa zasobów, do której należą przednia drzwi.</span><span class="sxs-lookup"><span data-stu-id="d73fc-132">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="d73fc-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d73fc-133">-ResourceId</span></span>
<span data-ttu-id="d73fc-134">Identyfikator zasobu punktu końcowego z przednim Drzwiem w celu włączenia protokołu https</span><span class="sxs-lookup"><span data-stu-id="d73fc-134">Resource Id of the Front Door endpoint to enable https</span></span>

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

### <span data-ttu-id="d73fc-135">-Secretname</span><span class="sxs-lookup"><span data-stu-id="d73fc-135">-SecretName</span></span>
<span data-ttu-id="d73fc-136">Nazwa tajnego magazynu kluczy reprezentującego pełny certyfikat PFX</span><span class="sxs-lookup"><span data-stu-id="d73fc-136">The name of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="d73fc-137">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="d73fc-137">-SecretVersion</span></span>
<span data-ttu-id="d73fc-138">Wersja tajnego magazynu kluczy reprezentującego pełną PFX certyfikatu</span><span class="sxs-lookup"><span data-stu-id="d73fc-138">The version of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="d73fc-139">-VaultId</span><span class="sxs-lookup"><span data-stu-id="d73fc-139">-VaultId</span></span>
<span data-ttu-id="d73fc-140">Identyfikator magazynu kluczy zawierający certyfikat SSL</span><span class="sxs-lookup"><span data-stu-id="d73fc-140">The Key Vault id containing the SSL certificate</span></span>

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

### <span data-ttu-id="d73fc-141">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d73fc-141">-Confirm</span></span>
<span data-ttu-id="d73fc-142">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d73fc-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d73fc-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d73fc-143">-WhatIf</span></span>
<span data-ttu-id="d73fc-144">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d73fc-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d73fc-145">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d73fc-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d73fc-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d73fc-146">CommonParameters</span></span>
<span data-ttu-id="d73fc-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d73fc-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d73fc-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d73fc-148">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d73fc-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d73fc-149">INPUTS</span></span>

### <span data-ttu-id="d73fc-150">System. String</span><span class="sxs-lookup"><span data-stu-id="d73fc-150">System.String</span></span>

## <span data-ttu-id="d73fc-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d73fc-151">OUTPUTS</span></span>

### <span data-ttu-id="d73fc-152">Microsoft. Azure. Commands. FrontDoor. models. PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="d73fc-152">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="d73fc-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d73fc-153">NOTES</span></span>

## <span data-ttu-id="d73fc-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d73fc-154">RELATED LINKS</span></span>
