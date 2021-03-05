---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/set-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzEnvironment.md
ms.openlocfilehash: 502a15c4d102932e32fb103a80f55c8b3acfee3f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967114"
---
# <span data-ttu-id="dcd6e-101">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="dcd6e-101">Set-AzEnvironment</span></span>

## <span data-ttu-id="dcd6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dcd6e-102">SYNOPSIS</span></span>
<span data-ttu-id="dcd6e-103">Ustawia właściwości środowiska platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-103">Sets properties for an Azure environment.</span></span>

## <span data-ttu-id="dcd6e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="dcd6e-104">SYNTAX</span></span>

### <span data-ttu-id="dcd6e-105">Nazwa (domyślna)</span><span class="sxs-lookup"><span data-stu-id="dcd6e-105">Name (Default)</span></span>
```
Set-AzEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
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
 [-ContainerRegistryEndpointSuffix <String>] [-AzureSynapseAnalyticsEndpointResourceId <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dcd6e-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="dcd6e-106">ARMEndpoint</span></span>
```
Set-AzEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-AzureAnalysisServicesEndpointSuffix <String>] [-AzureAnalysisServicesEndpointResourceId <String>]
 [-AzureAttestationServiceEndpointSuffix <String>] [-AzureAttestationServiceEndpointResourceId <String>]
 [-AzureSynapseAnalyticsEndpointSuffix <String>] [-ContainerRegistryEndpointSuffix <String>]
 [-AzureSynapseAnalyticsEndpointResourceId <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcd6e-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="dcd6e-107">DESCRIPTION</span></span>
<span data-ttu-id="dcd6e-108">Polecenie Set-AzEnvironment ustawia punkty końcowe i metadane do łączenia się z wystąpieniem platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-108">The Set-AzEnvironment cmdlet sets endpoints and metadata for connecting to an instance of Azure.</span></span>

## <span data-ttu-id="dcd6e-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="dcd6e-109">EXAMPLES</span></span>

### <span data-ttu-id="dcd6e-110">Przykład 1. Tworzenie i modyfikowanie nowego środowiska</span><span class="sxs-lookup"><span data-stu-id="dcd6e-110">Example 1: Creating and modifying a new environment</span></span>
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

PS C:\> Set-AzEnvironment -Name TestEnvironment
        -ActiveDirectoryEndpoint NewTestADEndpoint
        -GraphEndpoint NewTestGraphEndpoint | Format-List

Name                                              : TestEnvironment
EnableAdfsAuthentication                          : False
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
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            :
BatchEndpointResourceId                           :
AzureOperationalInsightsEndpoint                  :
AzureOperationalInsightsEndpointResourceId        :
AzureAttestationServiceEndpointSuffix             :
AzureAttestationServiceEndpointResourceId         :
AzureSynapseAnalyticsEndpointSuffix               :
AzureSynapseAnalyticsEndpointResourceId           :
```

<span data-ttu-id="dcd6e-111">W tym przykładzie tworzymy nowe środowisko platformy Azure z przykładowymi punktami końcowymi przy użyciu dodatku AzEnvironment, a następnie zmieniamy wartość atrybutów ActiveDirectoryEndpoint i GraphEndpoint utworzonego środowiska przy użyciu polecenia cmdlet Set-AzEnvironment.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-111">In this example we are creating a new Azure environment with sample endpoints using Add-AzEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzEnvironment.</span></span>

## <span data-ttu-id="dcd6e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dcd6e-112">PARAMETERS</span></span>

### <span data-ttu-id="dcd6e-113">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="dcd6e-113">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="dcd6e-114">Określa podstawowy urząd uwierzytelniania usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-114">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="dcd6e-115">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="dcd6e-115">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="dcd6e-116">Określa grupę odbiorców tokenów uwierzytelniania żądań do punktów końcowych usługi Azure Resource Manager lub zarządzania usługami (RDFE).</span><span class="sxs-lookup"><span data-stu-id="dcd6e-116">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="dcd6e-117">—AdTenant</span><span class="sxs-lookup"><span data-stu-id="dcd6e-117">-AdTenant</span></span>
<span data-ttu-id="dcd6e-118">Określa domyślną dzierżawę usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-118">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="dcd6e-119">- ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="dcd6e-119">-ARMEndpoint</span></span>
<span data-ttu-id="dcd6e-120">Punkt końcowy usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-120">The Azure Resource Manager endpoint.</span></span>

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

### <span data-ttu-id="dcd6e-121">-AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="dcd6e-121">-AzureAnalysisServicesEndpointResourceId</span></span>
<span data-ttu-id="dcd6e-122">Identyfikator zasobu zasobu usług Azure Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-122">The resource identifier of the Azure Analysis Services resource.</span></span>

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

### <span data-ttu-id="dcd6e-123">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="dcd6e-123">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="dcd6e-124">Punkt końcowy do użycia podczas komunikowania się z interfejsem API Azure Log Analytics.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-124">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="dcd6e-125">-AzureAttastationServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="dcd6e-125">-AzureAttestationServiceEndpointResourceId</span></span>
<span data-ttu-id="dcd6e-126">Identyfikator zasobu usługi Azure Attestation, który jest adresatem żądanego tokenu.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-126">The The resource identifier of the Azure Attestation service that is the recipient of the requested token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcd6e-127">-AzureAttastationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="dcd6e-127">-AzureAttestationServiceEndpointSuffix</span></span>
<span data-ttu-id="dcd6e-128">Sufiks DNS usługi Azure Attestation.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-128">Dns suffix of Azure Attestation service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcd6e-129">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="dcd6e-129">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="dcd6e-130">Sufiks DNS zadania i usług wykazu usługi Azure Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="dcd6e-130">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="dcd6e-131">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="dcd6e-131">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="dcd6e-132">Sufiks DNS systemu plików Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-132">Dns Suffix of Azure Data Lake Store FileSystem.</span></span> <span data-ttu-id="dcd6e-133">Przykład: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="dcd6e-133">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="dcd6e-134">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="dcd6e-134">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="dcd6e-135">Sufiks DNS usługi magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-135">Dns suffix of Azure Key Vault service.</span></span> <span data-ttu-id="dcd6e-136">Przykład: vault-int.azure-int.net</span><span class="sxs-lookup"><span data-stu-id="dcd6e-136">Example is vault-int.azure-int.net</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcd6e-137">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="dcd6e-137">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="dcd6e-138">Identyfikator zasobu usługi danych magazynu kluczy platformy Azure, który jest adresatem żądanego tokenu.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-138">Resource identifier of Azure Key Vault data service that is the recipient of the requested token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcd6e-139">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="dcd6e-139">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="dcd6e-140">Punkt końcowy do użycia podczas komunikowania się z interfejsem API Azure Log Analytics.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-140">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 22
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcd6e-141">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="dcd6e-141">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="dcd6e-142">Odbiorcy tokenów uwierzytelniający za pomocą interfejsu API Azure Log Analytics.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-142">The audience for tokens authenticating with the Azure Log Analytics API.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 21
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcd6e-143">-AzureSynapseAnalyticsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="dcd6e-143">-AzureSynapseAnalyticsEndpointResourceId</span></span>
<span data-ttu-id="dcd6e-144">Identyfikator zasobu usługi Azure Synapse Analytics, który jest adresatem żądanego tokenu.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-144">The The resource identifier of the Azure Synapse Analytics that is the recipient of the requested token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcd6e-145">-AzureSynapseAnalyticsEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="dcd6e-145">-AzureSynapseAnalyticsEndpointSuffix</span></span>
<span data-ttu-id="dcd6e-146">Sufiks dns usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-146">Dns suffix of Azure Synapse Analytics.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcd6e-147">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="dcd6e-147">-BatchEndpointResourceId</span></span>
<span data-ttu-id="dcd6e-148">Identyfikator zasobu usługi Azure Batch, który jest adresatem żądanego tokenu</span><span class="sxs-lookup"><span data-stu-id="dcd6e-148">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BatchResourceId, BatchAudience

Required: False
Position: 20
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcd6e-149">-ContainerRegistryEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="dcd6e-149">-ContainerRegistryEndpointSuffix</span></span>
<span data-ttu-id="dcd6e-150">Sufiks rejestru azure container.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-150">Suffix of Azure Container Registry.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcd6e-151">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="dcd6e-151">-DataLakeAudience</span></span>
<span data-ttu-id="dcd6e-152">Odbiorcy tokenów uwierzytelniania za pomocą punktu końcowego usług AD Data Lake.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-152">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataLakeEndpointResourceId, DataLakeResourceId

Required: False
Position: 19
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcd6e-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcd6e-153">-DefaultProfile</span></span>
<span data-ttu-id="dcd6e-154">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-154">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dcd6e-155">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="dcd6e-155">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="dcd6e-156">Wskazuje, że lokalne uwierzytelnianie usług federowych Active Directory (ADFS) jest dozwolone.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-156">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="dcd6e-157">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="dcd6e-157">-GalleryEndpoint</span></span>
<span data-ttu-id="dcd6e-158">Określa punkt końcowy galerii szablonów wdrażania usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-158">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="dcd6e-159">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="dcd6e-159">-GraphAudience</span></span>
<span data-ttu-id="dcd6e-160">Grupa odbiorców tokenów uwierzytelniających się za pomocą punktu końcowego programu AD Graph.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-160">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="dcd6e-161">- GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="dcd6e-161">-GraphEndpoint</span></span>
<span data-ttu-id="dcd6e-162">Określa adres URL żądań usługi Graph (metadanych usługi Active Directory).</span><span class="sxs-lookup"><span data-stu-id="dcd6e-162">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="dcd6e-163">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="dcd6e-163">-ManagementPortalUrl</span></span>
<span data-ttu-id="dcd6e-164">Określa adres URL portalu zarządzania.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-164">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="dcd6e-165">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="dcd6e-165">-Name</span></span>
<span data-ttu-id="dcd6e-166">Określa nazwę środowiska do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-166">Specifies the name of the environment to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcd6e-167">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="dcd6e-167">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="dcd6e-168">Określa adres URL, z którego można pobierać pliki .publishsettings.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-168">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="dcd6e-169">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="dcd6e-169">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="dcd6e-170">Określa adres URL żądań usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-170">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="dcd6e-171">— Zakres</span><span class="sxs-lookup"><span data-stu-id="dcd6e-171">-Scope</span></span>
<span data-ttu-id="dcd6e-172">Określa zakres zmian kontekstu, na przykład tego, czy zmiany mają zastosowanie tylko do bieżącego procesu, czy do wszystkich sesji rozpoczętych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-172">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="dcd6e-173">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="dcd6e-173">-ServiceEndpoint</span></span>
<span data-ttu-id="dcd6e-174">Określa punkt końcowy żądań zarządzania usługami (RDFE).</span><span class="sxs-lookup"><span data-stu-id="dcd6e-174">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="dcd6e-175">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="dcd6e-175">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="dcd6e-176">Określa sufiks nazwy domeny dla serwerów usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-176">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="dcd6e-177">- StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="dcd6e-177">-StorageEndpoint</span></span>
<span data-ttu-id="dcd6e-178">Określa punkt końcowy dla dostępu do magazynu (obiektu blob, tabeli, kolejki i pliku).</span><span class="sxs-lookup"><span data-stu-id="dcd6e-178">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageEndpointSuffix

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcd6e-179">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="dcd6e-179">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="dcd6e-180">Określa sufiks nazwy domeny dla usług Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-180">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="dcd6e-181">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dcd6e-181">-Confirm</span></span>
<span data-ttu-id="dcd6e-182">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcd6e-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcd6e-183">-WhatIf</span></span>
<span data-ttu-id="dcd6e-184">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-184">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dcd6e-185">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcd6e-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcd6e-186">CommonParameters</span></span>
<span data-ttu-id="dcd6e-187">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcd6e-188">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dcd6e-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcd6e-189">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dcd6e-189">INPUTS</span></span>

### <span data-ttu-id="dcd6e-190">System.String</span><span class="sxs-lookup"><span data-stu-id="dcd6e-190">System.String</span></span>

### <span data-ttu-id="dcd6e-191">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="dcd6e-191">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="dcd6e-192">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dcd6e-192">OUTPUTS</span></span>

### <span data-ttu-id="dcd6e-193">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="dcd6e-193">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="dcd6e-194">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="dcd6e-194">NOTES</span></span>

## <span data-ttu-id="dcd6e-195">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dcd6e-195">RELATED LINKS</span></span>

[<span data-ttu-id="dcd6e-196">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="dcd6e-196">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="dcd6e-197">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="dcd6e-197">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="dcd6e-198">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="dcd6e-198">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

