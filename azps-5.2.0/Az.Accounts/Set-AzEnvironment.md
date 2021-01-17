---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/set-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzEnvironment.md
ms.openlocfilehash: 7764a40f71b689835d340e8061616e6e5a548621
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342634"
---
# <span data-ttu-id="819c8-101">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="819c8-101">Set-AzEnvironment</span></span>

## <span data-ttu-id="819c8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="819c8-102">SYNOPSIS</span></span>
<span data-ttu-id="819c8-103">Ustawia właściwości dla środowiska platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="819c8-103">Sets properties for an Azure environment.</span></span>

## <span data-ttu-id="819c8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="819c8-104">SYNTAX</span></span>

### <span data-ttu-id="819c8-105">Nazwa (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="819c8-105">Name (Default)</span></span>
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

### <span data-ttu-id="819c8-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="819c8-106">ARMEndpoint</span></span>
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

## <span data-ttu-id="819c8-107">Opis</span><span class="sxs-lookup"><span data-stu-id="819c8-107">DESCRIPTION</span></span>
<span data-ttu-id="819c8-108">Polecenie cmdlet Set-AzEnvironment ustawia punkty końcowe i metadane w celu nawiązania połączenia z wystąpieniem platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="819c8-108">The Set-AzEnvironment cmdlet sets endpoints and metadata for connecting to an instance of Azure.</span></span>

## <span data-ttu-id="819c8-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="819c8-109">EXAMPLES</span></span>

### <span data-ttu-id="819c8-110">Przykład 1: Tworzenie i modyfikowanie nowego środowiska</span><span class="sxs-lookup"><span data-stu-id="819c8-110">Example 1: Creating and modifying a new environment</span></span>
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

<span data-ttu-id="819c8-111">W tym przykładzie tworzymy nowe środowisko platformy Azure z przykładowymi punktami końcowymi przy użyciu polecenia Add-AzEnvironment, a następnie zmieniamy wartość atrybutów ActiveDirectoryEndpoint i GraphEndpoint utworzonego środowiska za pomocą zestawu poleceń cmdlet Set-AzEnvironment.</span><span class="sxs-lookup"><span data-stu-id="819c8-111">In this example we are creating a new Azure environment with sample endpoints using Add-AzEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzEnvironment.</span></span>

## <span data-ttu-id="819c8-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="819c8-112">PARAMETERS</span></span>

### <span data-ttu-id="819c8-113">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="819c8-113">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="819c8-114">Określa podstawowy urząd uwierzytelniania usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="819c8-114">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="819c8-115">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="819c8-115">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="819c8-116">Określa odbiorców tokenów uwierzytelniających żądania do punktów końcowych Menedżera zasobów platformy Azure lub zarządzania usługami (REDDOG, Service Management Manager).</span><span class="sxs-lookup"><span data-stu-id="819c8-116">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="819c8-117">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="819c8-117">-AdTenant</span></span>
<span data-ttu-id="819c8-118">Określa domyślną dzierżawę usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="819c8-118">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="819c8-119">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="819c8-119">-ARMEndpoint</span></span>
<span data-ttu-id="819c8-120">Punkt końcowy usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="819c8-120">The Azure Resource Manager endpoint.</span></span>

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

### <span data-ttu-id="819c8-121">-AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="819c8-121">-AzureAnalysisServicesEndpointResourceId</span></span>
<span data-ttu-id="819c8-122">Identyfikator zasobu zasobu usługi Azure Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="819c8-122">The resource identifier of the Azure Analysis Services resource.</span></span>

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

### <span data-ttu-id="819c8-123">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="819c8-123">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="819c8-124">Punkt końcowy, który ma być używany podczas komunikowania się z interfejsem API analizy dzienników Azure.</span><span class="sxs-lookup"><span data-stu-id="819c8-124">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="819c8-125">-AzureAttestationServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="819c8-125">-AzureAttestationServiceEndpointResourceId</span></span>
<span data-ttu-id="819c8-126">Identyfikator zasobu usługi zaświadczeń na platformie Azure, który jest odbiorcą żądanego tokenu.</span><span class="sxs-lookup"><span data-stu-id="819c8-126">The The resource identifier of the Azure Attestation service that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="819c8-127">-AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="819c8-127">-AzureAttestationServiceEndpointSuffix</span></span>
<span data-ttu-id="819c8-128">Sufiks DNS usługi zaświadczeń na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="819c8-128">Dns suffix of Azure Attestation service.</span></span>

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

### <span data-ttu-id="819c8-129">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="819c8-129">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="819c8-130">Sufiks DNS dla zadań usługi Azure Data Lake Analytics i usług wykazu</span><span class="sxs-lookup"><span data-stu-id="819c8-130">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="819c8-131">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="819c8-131">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="819c8-132">Sufiks DNS w systemie plików usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="819c8-132">Dns Suffix of Azure Data Lake Store FileSystem.</span></span> <span data-ttu-id="819c8-133">Przykład: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="819c8-133">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="819c8-134">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="819c8-134">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="819c8-135">Sufiks DNS usługi magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="819c8-135">Dns suffix of Azure Key Vault service.</span></span> <span data-ttu-id="819c8-136">Przykład to vault-int.azure-int.net</span><span class="sxs-lookup"><span data-stu-id="819c8-136">Example is vault-int.azure-int.net</span></span>

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

### <span data-ttu-id="819c8-137">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="819c8-137">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="819c8-138">Identyfikator zasobu usługi danych magazynu kluczy platformy Azure, który jest odbiorcą żądanego tokenu.</span><span class="sxs-lookup"><span data-stu-id="819c8-138">Resource identifier of Azure Key Vault data service that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="819c8-139">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="819c8-139">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="819c8-140">Punkt końcowy, który ma być używany podczas komunikowania się z interfejsem API analizy dzienników Azure.</span><span class="sxs-lookup"><span data-stu-id="819c8-140">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="819c8-141">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="819c8-141">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="819c8-142">Odbiorcy tokenów uwierzytelniających się przy użyciu interfejsu API analizy dzienników Azure.</span><span class="sxs-lookup"><span data-stu-id="819c8-142">The audience for tokens authenticating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="819c8-143">-AzureSynapseAnalyticsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="819c8-143">-AzureSynapseAnalyticsEndpointResourceId</span></span>
<span data-ttu-id="819c8-144">Identyfikator zasobu analizy usługi Azure Synapse, który jest odbiorcą żądanego tokenu.</span><span class="sxs-lookup"><span data-stu-id="819c8-144">The The resource identifier of the Azure Synapse Analytics that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="819c8-145">-AzureSynapseAnalyticsEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="819c8-145">-AzureSynapseAnalyticsEndpointSuffix</span></span>
<span data-ttu-id="819c8-146">Sufiks DNS na platformie Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="819c8-146">Dns suffix of Azure Synapse Analytics.</span></span>

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

### <span data-ttu-id="819c8-147">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="819c8-147">-BatchEndpointResourceId</span></span>
<span data-ttu-id="819c8-148">Identyfikator zasobu usługi Azure Batch, który jest odbiorcą żądanego tokenu</span><span class="sxs-lookup"><span data-stu-id="819c8-148">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

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

### <span data-ttu-id="819c8-149">-ContainerRegistryEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="819c8-149">-ContainerRegistryEndpointSuffix</span></span>
<span data-ttu-id="819c8-150">Sufiks rejestru kontenera platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="819c8-150">Suffix of Azure Container Registry.</span></span>

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

### <span data-ttu-id="819c8-151">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="819c8-151">-DataLakeAudience</span></span>
<span data-ttu-id="819c8-152">Odbiorca tokenów uwierzytelniających się za pomocą punktu końcowego usługi AD Data Lake Services.</span><span class="sxs-lookup"><span data-stu-id="819c8-152">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

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

### <span data-ttu-id="819c8-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="819c8-153">-DefaultProfile</span></span>
<span data-ttu-id="819c8-154">Poświadczenia, konto, dzierżawca i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="819c8-154">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="819c8-155">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="819c8-155">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="819c8-156">Wskazuje, że dozwolone jest uwierzytelnianie lokalne usług federacyjnych Active Directory (ADFS).</span><span class="sxs-lookup"><span data-stu-id="819c8-156">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="819c8-157">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="819c8-157">-GalleryEndpoint</span></span>
<span data-ttu-id="819c8-158">Określa punkt końcowy galerii szablonów wdrażania usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="819c8-158">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="819c8-159">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="819c8-159">-GraphAudience</span></span>
<span data-ttu-id="819c8-160">Odbiorca tokenów uwierzytelniających się za pomocą punktu końcowego grafu AD.</span><span class="sxs-lookup"><span data-stu-id="819c8-160">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="819c8-161">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="819c8-161">-GraphEndpoint</span></span>
<span data-ttu-id="819c8-162">Określa adres URL żądań wykresu (metadanych usługi Active Directory).</span><span class="sxs-lookup"><span data-stu-id="819c8-162">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="819c8-163">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="819c8-163">-ManagementPortalUrl</span></span>
<span data-ttu-id="819c8-164">Określa adres URL portalu zarządzania.</span><span class="sxs-lookup"><span data-stu-id="819c8-164">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="819c8-165">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="819c8-165">-Name</span></span>
<span data-ttu-id="819c8-166">Określa nazwę środowiska, które ma zostać zmodyfikowane.</span><span class="sxs-lookup"><span data-stu-id="819c8-166">Specifies the name of the environment to modify.</span></span>

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

### <span data-ttu-id="819c8-167">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="819c8-167">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="819c8-168">Określa adres URL, z którego można pobrać pliki publishsettings.</span><span class="sxs-lookup"><span data-stu-id="819c8-168">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="819c8-169">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="819c8-169">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="819c8-170">Określa adres URL żądań usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="819c8-170">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="819c8-171">-Zakres</span><span class="sxs-lookup"><span data-stu-id="819c8-171">-Scope</span></span>
<span data-ttu-id="819c8-172">Określa zakres zmian kontekstu, na przykład, czy zmiany są stosowane tylko do bieżącego procesu, czy do wszystkich sesji uruchomionych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="819c8-172">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="819c8-173">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="819c8-173">-ServiceEndpoint</span></span>
<span data-ttu-id="819c8-174">Umożliwia określenie punktu końcowego dla żądań zarządzania usługami (REDDOG).</span><span class="sxs-lookup"><span data-stu-id="819c8-174">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="819c8-175">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="819c8-175">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="819c8-176">Określa sufiks nazwy domeny dla serwerów bazy danych platformy Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="819c8-176">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="819c8-177">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="819c8-177">-StorageEndpoint</span></span>
<span data-ttu-id="819c8-178">Umożliwia określenie punktu końcowego dostępu (obiektu BLOB, tabeli, kolejki i pliku).</span><span class="sxs-lookup"><span data-stu-id="819c8-178">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="819c8-179">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="819c8-179">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="819c8-180">Określa sufiks nazwy domeny dla usług programu Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="819c8-180">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="819c8-181">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="819c8-181">-Confirm</span></span>
<span data-ttu-id="819c8-182">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="819c8-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="819c8-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="819c8-183">-WhatIf</span></span>
<span data-ttu-id="819c8-184">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="819c8-184">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="819c8-185">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="819c8-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="819c8-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="819c8-186">CommonParameters</span></span>
<span data-ttu-id="819c8-187">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="819c8-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="819c8-188">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="819c8-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="819c8-189">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="819c8-189">INPUTS</span></span>

### <span data-ttu-id="819c8-190">System. String</span><span class="sxs-lookup"><span data-stu-id="819c8-190">System.String</span></span>

### <span data-ttu-id="819c8-191">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="819c8-191">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="819c8-192">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="819c8-192">OUTPUTS</span></span>

### <span data-ttu-id="819c8-193">Microsoft. Azure. Commands. profile. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="819c8-193">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="819c8-194">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="819c8-194">NOTES</span></span>

## <span data-ttu-id="819c8-195">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="819c8-195">RELATED LINKS</span></span>

[<span data-ttu-id="819c8-196">Dodaj-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="819c8-196">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="819c8-197">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="819c8-197">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="819c8-198">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="819c8-198">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

