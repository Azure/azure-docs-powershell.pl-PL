---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/add-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Add-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Add-AzEnvironment.md
ms.openlocfilehash: 2db2e90dc1292bdfe67907e5a180b08a09a54718
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100406013"
---
# <span data-ttu-id="50286-101">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="50286-101">Add-AzEnvironment</span></span>

## <span data-ttu-id="50286-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50286-102">SYNOPSIS</span></span>
<span data-ttu-id="50286-103">Dodaje punkty końcowe i metadane dla wystąpienia usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="50286-103">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

## <span data-ttu-id="50286-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="50286-104">SYNTAX</span></span>

### <span data-ttu-id="50286-105">Nazwa (domyślna)</span><span class="sxs-lookup"><span data-stu-id="50286-105">Name (Default)</span></span>
```
Add-AzEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
 [[-ManagementPortalUrl] <String>] [[-StorageEndpoint] <String>] [[-ActiveDirectoryEndpoint] <String>]
 [[-ResourceManagerEndpoint] <String>] [[-GalleryEndpoint] <String>]
 [[-ActiveDirectoryServiceEndpointResourceId] <String>] [[-GraphEndpoint] <String>]
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-TrafficManagerDnsSuffix] <String>] [[-SqlDatabaseDnsSuffix] <String>]
 [[-AzureDataLakeStoreFileSystemEndpointSuffix] <String>]
 [[-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix] <String>] [-EnableAdfsAuthentication]
 [[-AdTenant] <String>] [[-GraphAudience] <String>] [[-DataLakeAudience] <String>]
 [[-BatchEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpoint] <String>] [-AzureAnalysisServicesEndpointSuffix <String>]
 [-AzureAnalysisServicesEndpointResourceId <String>] [-AzureAttestationServiceEndpointSuffix <String>]
 [-AzureAttestationServiceEndpointResourceId <String>] [-AzureSynapseAnalyticsEndpointSuffix <String>]
 [-AzureSynapseAnalyticsEndpointResourceId <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50286-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="50286-106">ARMEndpoint</span></span>
```
Add-AzEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-AzureAnalysisServicesEndpointSuffix <String>] [-AzureAnalysisServicesEndpointResourceId <String>]
 [-AzureAttestationServiceEndpointSuffix <String>] [-AzureAttestationServiceEndpointResourceId <String>]
 [-AzureSynapseAnalyticsEndpointSuffix <String>] [-AzureSynapseAnalyticsEndpointResourceId <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="50286-107">Odnajdowanie</span><span class="sxs-lookup"><span data-stu-id="50286-107">Discovery</span></span>
```
Add-AzEnvironment -AutoDiscover [-Uri <Uri>] [-Scope {Process | CurrentUser}]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50286-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="50286-108">DESCRIPTION</span></span>
<span data-ttu-id="50286-109">Polecenie Add-AzEnvironment cmdlet dodaje punkty końcowe i metadane w celu umożliwienia polecenia cmdlet usługi Azure Resource Manager na łączenie się za pomocą nowego wystąpienia usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="50286-109">The Add-AzEnvironment cmdlet adds endpoints and metadata to enable Azure Resource Manager cmdlets to connect with a new instance of Azure Resource Manager.</span></span>
<span data-ttu-id="50286-110">Środowiska wbudowane AzureCloud i AzureChinaCloud są kierowane do istniejących wystąpień publicznych usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="50286-110">The built-in environments AzureCloud and AzureChinaCloud target existing public instances of Azure Resource Manager.</span></span>

## <span data-ttu-id="50286-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="50286-111">EXAMPLES</span></span>

### <span data-ttu-id="50286-112">Przykład 1. Tworzenie i modyfikowanie nowego środowiska</span><span class="sxs-lookup"><span data-stu-id="50286-112">Example 1: Creating and modifying a new environment</span></span>
```
PS C:\> Add-AzEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint TestADEndpoint `
        -ActiveDirectoryServiceEndpointResourceId TestADApplicationId `
        -ResourceManagerEndpoint TestRMEndpoint `
        -GalleryEndpoint TestGalleryEndpoint `
        -GraphEndpoint TestGraphEndpoint

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/

PS C:\> Set-AzEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint NewTestADEndpoint `
        -GraphEndpoint NewTestGraphEndpoint | Format-List

Name                                              : TestEnvironment
EnableAdfsAuthentication                          : False
OnPremise                                         : False
ActiveDirectoryServiceEndpointResourceId          : TestADApplicationId
AdTenant                                          :
GalleryUrl                                        : TestGalleryEndpoint
ManagementPortalUrl                               :
ServiceManagementUrl                              :
PublishSettingsFileUrl                            :
ResourceManagerUrl                                : TestRMEndpoint
SqlDatabaseDnsSuffix                              :
StorageEndpointSuffix                             :
ActiveDirectoryAuthority                          : NewTestADEndpoint
GraphUrl                                          : NewTestGraphEndpoint
GraphEndpointResourceId                           :
TrafficManagerDnsSuffix                           :
AzureKeyVaultDnsSuffix                            :
DataLakeEndpointResourceId                        :
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            :
AzureOperationalInsightsEndpointResourceId        :
AzureOperationalInsightsEndpoint                  :
AzureAnalysisServicesEndpointSuffix               :
AzureAttestationServiceEndpointSuffix             :
AzureAttestationServiceEndpointResourceId         :
AzureSynapseAnalyticsEndpointSuffix               :
AzureSynapseAnalyticsEndpointResourceId           :
VersionProfiles                                   : {}
ExtendedProperties                                : {}
BatchEndpointResourceId                           :
```

<span data-ttu-id="50286-113">W tym przykładzie tworzymy nowe środowisko platformy Azure z przykładowymi punktami końcowymi przy użyciu dodatku AzEnvironment, a następnie zmieniamy wartość atrybutów ActiveDirectoryEndpoint i GraphEndpoint utworzonego środowiska przy użyciu polecenia cmdlet Set-AzEnvironment.</span><span class="sxs-lookup"><span data-stu-id="50286-113">In this example we are creating a new Azure environment with sample endpoints using Add-AzEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzEnvironment.</span></span>

### <span data-ttu-id="50286-114">Przykład 2. Odnajdowanie nowego środowiska za pośrednictwem Uri</span><span class="sxs-lookup"><span data-stu-id="50286-114">Example 2: Discovering a new environment via Uri</span></span>
```
<#
Uri https://configuredmetadata.net returns an array of environment metadata. The following example contains a payload for the AzureCloud default environment.

[
  {
    "portal": "https://portal.azure.com",
    "authentication": {
      "loginEndpoint": "https://login.microsoftonline.com/",
      "audiences": [
        "https://management.core.windows.net/"
      ],
      "tenant": "common",
      "identityProvider": "AAD"
    },
    "media": "https://rest.media.azure.net",
    "graphAudience": "https://graph.windows.net/",
    "graph": "https://graph.windows.net/",
    "name": "AzureCloud",
    "suffixes": {
      "azureDataLakeStoreFileSystem": "azuredatalakestore.net",
      "acrLoginServer": "azurecr.io",
      "sqlServerHostname": ".database.windows.net",
      "azureDataLakeAnalyticsCatalogAndJob": "azuredatalakeanalytics.net",
      "keyVaultDns": "vault.azure.net",
      "storage": "core.windows.net",
      "azureFrontDoorEndpointSuffix": "azurefd.net"
    },
    "batch": "https://batch.core.windows.net/",
    "resourceManager": "https://management.azure.com/",
    "vmImageAliasDoc": "https://raw.githubusercontent.com/Azure/azure-rest-api-specs/master/arm-compute/quickstart-templates/aliases.json",
    "activeDirectoryDataLake": "https://datalake.azure.net/",
    "sqlManagement": "https://management.core.windows.net:8443/",
    "gallery": "https://gallery.azure.com/"
  },
……
]
#>

PS C:\> Add-AzEnvironment -AutoDiscover -Uri https://configuredmetadata.net

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/
```

<span data-ttu-id="50286-115">W tym przykładzie odkrywamy nowe środowisko platformy Azure na stronie `https://configuredmetadata.net` Uri.</span><span class="sxs-lookup"><span data-stu-id="50286-115">In this example, we are discovering a new Azure environment from the `https://configuredmetadata.net` Uri.</span></span>

## <span data-ttu-id="50286-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50286-116">PARAMETERS</span></span>

### <span data-ttu-id="50286-117">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="50286-117">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="50286-118">Określa podstawowy urząd uwierzytelniania usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="50286-118">Specifies the base authority for Azure Active Directory authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: AdEndpointUrl, ActiveDirectory, ActiveDirectoryAuthority

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50286-119">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="50286-119">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="50286-120">Określa grupę odbiorców tokenów uwierzytelniania żądań do punktów końcowych usługi Azure Resource Manager lub zarządzania usługami (RDFE).</span><span class="sxs-lookup"><span data-stu-id="50286-120">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50286-121">—AdTenant</span><span class="sxs-lookup"><span data-stu-id="50286-121">-AdTenant</span></span>
<span data-ttu-id="50286-122">Określa domyślną dzierżawę usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="50286-122">Specifies the default Active Directory tenant.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 17
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50286-123">- ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="50286-123">-ARMEndpoint</span></span>
<span data-ttu-id="50286-124">Punkt końcowy usługi Azure Resource Manager</span><span class="sxs-lookup"><span data-stu-id="50286-124">The Azure Resource Manager endpoint</span></span>

```yaml
Type: System.String
Parameter Sets: ARMEndpoint
Aliases: ArmUrl

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50286-125">— Autodiscover</span><span class="sxs-lookup"><span data-stu-id="50286-125">-AutoDiscover</span></span>
<span data-ttu-id="50286-126">Wykrywa środowiska za pośrednictwem domyślnego lub skonfigurowanego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="50286-126">Discovers environments via default or configured endpoint.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Discovery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50286-127">-AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="50286-127">-AzureAnalysisServicesEndpointResourceId</span></span>
<span data-ttu-id="50286-128">Identyfikator zasobu zasobu usług Azure Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="50286-128">The resource identifier of the Azure Analysis Services resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50286-129">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="50286-129">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="50286-130">Punkt końcowy do użycia podczas komunikowania się z interfejsem API Azure Log Analytics.</span><span class="sxs-lookup"><span data-stu-id="50286-130">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50286-131">-AzureAttastationServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="50286-131">-AzureAttestationServiceEndpointResourceId</span></span>
<span data-ttu-id="50286-132">Identyfikator zasobu usługi Azure Attestation, który jest adresatem żądanego tokenu.</span><span class="sxs-lookup"><span data-stu-id="50286-132">The The resource identifier of the Azure Attestation service that is the recipient of the requested token.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50286-133">-AzureAttastationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="50286-133">-AzureAttestationServiceEndpointSuffix</span></span>
<span data-ttu-id="50286-134">Sufiks DNS usługi Azure Attestation.</span><span class="sxs-lookup"><span data-stu-id="50286-134">Dns suffix of Azure Attestation service.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50286-135">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="50286-135">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="50286-136">Sufiks DNS zadania i usług wykazu usługi Azure Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="50286-136">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 15
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50286-137">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="50286-137">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="50286-138">Sufiks DNS systemu plików Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="50286-138">Dns Suffix of Azure Data Lake Store FileSystem.</span></span> <span data-ttu-id="50286-139">Przykład: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="50286-139">Example: azuredatalake.net</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 14
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50286-140">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="50286-140">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="50286-141">Sufiks DNS usługi magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="50286-141">Dns suffix of Azure Key Vault service.</span></span> <span data-ttu-id="50286-142">Przykład: vault-int.azure-int.net</span><span class="sxs-lookup"><span data-stu-id="50286-142">Example is vault-int.azure-int.net</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50286-143">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="50286-143">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="50286-144">Identyfikator zasobu usługi danych magazynu kluczy platformy Azure, który jest adresatem żądanego tokenu.</span><span class="sxs-lookup"><span data-stu-id="50286-144">Resource identifier of Azure Key Vault data service that is the recipient of the requested token.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50286-145">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="50286-145">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="50286-146">Punkt końcowy do użycia podczas komunikowania się z interfejsem API Azure Log Analytics.</span><span class="sxs-lookup"><span data-stu-id="50286-146">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: 22
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50286-147">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="50286-147">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="50286-148">Odbiorcy tokenów uwierzytelniający za pomocą interfejsu API Azure Log Analytics.</span><span class="sxs-lookup"><span data-stu-id="50286-148">The audience for tokens authenticating with the Azure Log Analytics API.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: 21
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50286-149">-AzureSynapseAnalyticsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="50286-149">-AzureSynapseAnalyticsEndpointResourceId</span></span>
<span data-ttu-id="50286-150">Identyfikator zasobu usługi Azure Synapse Analytics, który jest adresatem żądanego tokenu.</span><span class="sxs-lookup"><span data-stu-id="50286-150">The The resource identifier of the Azure Synapse Analytics that is the recipient of the requested token.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50286-151">-AzureSynapseAnalyticsEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="50286-151">-AzureSynapseAnalyticsEndpointSuffix</span></span>
<span data-ttu-id="50286-152">Sufiks dns usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="50286-152">Dns suffix of Azure Synapse Analytics.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50286-153">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="50286-153">-BatchEndpointResourceId</span></span>
<span data-ttu-id="50286-154">Identyfikator zasobu usługi Azure Batch, który jest adresatem żądanego tokenu</span><span class="sxs-lookup"><span data-stu-id="50286-154">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases: BatchResourceId, BatchAudience

Required: False
Position: 20
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50286-155">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="50286-155">-DataLakeAudience</span></span>
<span data-ttu-id="50286-156">Odbiorcy tokenów uwierzytelniania za pomocą punktu końcowego usług AD Data Lake.</span><span class="sxs-lookup"><span data-stu-id="50286-156">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases: DataLakeEndpointResourceId, DataLakeResourceId

Required: False
Position: 19
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50286-157">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50286-157">-DefaultProfile</span></span>
<span data-ttu-id="50286-158">Poświadczenia, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="50286-158">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="50286-159">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="50286-159">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="50286-160">Wskazuje, że lokalne uwierzytelnianie usług federowych Active Directory (ADFS) jest dozwolone.</span><span class="sxs-lookup"><span data-stu-id="50286-160">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Name
Aliases: OnPremise

Required: False
Position: 16
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50286-161">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="50286-161">-GalleryEndpoint</span></span>
<span data-ttu-id="50286-162">Określa punkt końcowy galerii szablonów wdrażania usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="50286-162">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: Gallery, GalleryUrl

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50286-163">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="50286-163">-GraphAudience</span></span>
<span data-ttu-id="50286-164">Grupa odbiorców tokenów uwierzytelniających się za pomocą punktu końcowego programu AD Graph.</span><span class="sxs-lookup"><span data-stu-id="50286-164">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: GraphEndpointResourceId, GraphResourceId

Required: False
Position: 18
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50286-165">- GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="50286-165">-GraphEndpoint</span></span>
<span data-ttu-id="50286-166">Określa adres URL żądań usługi Graph (metadanych usługi Active Directory).</span><span class="sxs-lookup"><span data-stu-id="50286-166">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: Graph, GraphUrl

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50286-167">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="50286-167">-ManagementPortalUrl</span></span>
<span data-ttu-id="50286-168">Określa adres URL portalu zarządzania.</span><span class="sxs-lookup"><span data-stu-id="50286-168">Specifies the URL for the Management Portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50286-169">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="50286-169">-Name</span></span>
<span data-ttu-id="50286-170">Określa nazwę środowiska do dodania.</span><span class="sxs-lookup"><span data-stu-id="50286-170">Specifies the name of the environment to add.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50286-171">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="50286-171">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="50286-172">Określa adres URL, z którego można pobierać pliki .publishsettings.</span><span class="sxs-lookup"><span data-stu-id="50286-172">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50286-173">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="50286-173">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="50286-174">Określa adres URL żądań usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="50286-174">Specifies the URL for Azure Resource Manager requests.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: ResourceManager, ResourceManagerUrl

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50286-175">— Zakres</span><span class="sxs-lookup"><span data-stu-id="50286-175">-Scope</span></span>
<span data-ttu-id="50286-176">Określa zakres zmian kontekstu, na przykład tego, czy zmiany mają zastosowanie tylko do bieżącego procesu, czy do wszystkich sesji rozpoczętych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="50286-176">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50286-177">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="50286-177">-ServiceEndpoint</span></span>
<span data-ttu-id="50286-178">Określa punkt końcowy żądań zarządzania usługami (RDFE).</span><span class="sxs-lookup"><span data-stu-id="50286-178">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: ServiceManagement, ServiceManagementUrl

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50286-179">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="50286-179">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="50286-180">Określa sufiks nazwy domeny dla serwerów usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="50286-180">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50286-181">- StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="50286-181">-StorageEndpoint</span></span>
<span data-ttu-id="50286-182">Określa punkt końcowy dla dostępu do magazynu (obiektu blob, tabeli, kolejki i pliku).</span><span class="sxs-lookup"><span data-stu-id="50286-182">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases: StorageEndpointSuffix

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50286-183">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="50286-183">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="50286-184">Określa sufiks nazwy domeny dla usług Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="50286-184">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50286-185">-Uri</span><span class="sxs-lookup"><span data-stu-id="50286-185">-Uri</span></span>
<span data-ttu-id="50286-186">Określa URI zasobu internetowego w celu zdalnego dostępu do środowisk.</span><span class="sxs-lookup"><span data-stu-id="50286-186">Specifies URI of the internet resource to fetch environments.</span></span>

```yaml
Type: System.Uri
Parameter Sets: Discovery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50286-187">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="50286-187">-Confirm</span></span>
<span data-ttu-id="50286-188">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="50286-188">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50286-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50286-189">-WhatIf</span></span>
<span data-ttu-id="50286-190">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50286-190">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="50286-191">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="50286-191">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50286-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50286-192">CommonParameters</span></span>
<span data-ttu-id="50286-193">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50286-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50286-194">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="50286-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50286-195">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="50286-195">INPUTS</span></span>

### <span data-ttu-id="50286-196">System.String</span><span class="sxs-lookup"><span data-stu-id="50286-196">System.String</span></span>

### <span data-ttu-id="50286-197">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="50286-197">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="50286-198">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="50286-198">OUTPUTS</span></span>

### <span data-ttu-id="50286-199">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="50286-199">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="50286-200">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="50286-200">NOTES</span></span>

## <span data-ttu-id="50286-201">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="50286-201">RELATED LINKS</span></span>

[<span data-ttu-id="50286-202">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="50286-202">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="50286-203">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="50286-203">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

[<span data-ttu-id="50286-204">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="50286-204">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

