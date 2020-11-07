---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/set-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Set-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Set-AzEnvironment.md
ms.openlocfilehash: 7ec08296fe88b7d5b7d7825c3a3078b1e85ce81c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890153"
---
# <span data-ttu-id="480b1-101">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="480b1-101">Set-AzEnvironment</span></span>

## <span data-ttu-id="480b1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="480b1-102">SYNOPSIS</span></span>
<span data-ttu-id="480b1-103">Ustawia właściwości dla środowiska platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="480b1-103">Sets properties for an Azure environment.</span></span>

## <span data-ttu-id="480b1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="480b1-104">SYNTAX</span></span>

### <span data-ttu-id="480b1-105">Nazwa (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="480b1-105">Name (Default)</span></span>
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
 [-AzureAttestationServiceEndpointResourceId <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="480b1-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="480b1-106">ARMEndpoint</span></span>
```
Set-AzEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-AzureAnalysisServicesEndpointSuffix <String>] [-AzureAnalysisServicesEndpointResourceId <String>]
 [-AzureAttestationServiceEndpointSuffix <String>] [-AzureAttestationServiceEndpointResourceId <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="480b1-107">Opis</span><span class="sxs-lookup"><span data-stu-id="480b1-107">DESCRIPTION</span></span>
<span data-ttu-id="480b1-108">Polecenie cmdlet Set-AzEnvironment ustawia punkty końcowe i metadane w celu nawiązania połączenia z wystąpieniem platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="480b1-108">The Set-AzEnvironment cmdlet sets endpoints and metadata for connecting to an instance of Azure.</span></span>

## <span data-ttu-id="480b1-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="480b1-109">EXAMPLES</span></span>

### <span data-ttu-id="480b1-110">Przykład 1: Tworzenie i modyfikowanie nowego środowiska</span><span class="sxs-lookup"><span data-stu-id="480b1-110">Example 1: Creating and modifying a new environment</span></span>
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
```

<span data-ttu-id="480b1-111">W tym przykładzie tworzymy nowe środowisko platformy Azure z przykładowymi punktami końcowymi przy użyciu polecenia Add-AzEnvironment, a następnie zmieniamy wartość atrybutów ActiveDirectoryEndpoint i GraphEndpoint utworzonego środowiska za pomocą zestawu poleceń cmdlet Set-AzEnvironment.</span><span class="sxs-lookup"><span data-stu-id="480b1-111">In this example we are creating a new Azure environment with sample endpoints using Add-AzEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzEnvironment.</span></span>

## <span data-ttu-id="480b1-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="480b1-112">PARAMETERS</span></span>

### <span data-ttu-id="480b1-113">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="480b1-113">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="480b1-114">Określa podstawowy urząd uwierzytelniania usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="480b1-114">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="480b1-115">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="480b1-115">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="480b1-116">Określa odbiorców tokenów uwierzytelniających żądania do punktów końcowych Menedżera zasobów platformy Azure lub zarządzania usługami (REDDOG, Service Management Manager).</span><span class="sxs-lookup"><span data-stu-id="480b1-116">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="480b1-117">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="480b1-117">-AdTenant</span></span>
<span data-ttu-id="480b1-118">Określa domyślną dzierżawę usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="480b1-118">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="480b1-119">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="480b1-119">-ARMEndpoint</span></span>
<span data-ttu-id="480b1-120">Punkt końcowy usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="480b1-120">The Azure Resource Manager endpoint.</span></span>

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

### <span data-ttu-id="480b1-121">-AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="480b1-121">-AzureAnalysisServicesEndpointResourceId</span></span>
<span data-ttu-id="480b1-122">Identyfikator zasobu zasobu usługi Azure Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="480b1-122">The resource identifier of the Azure Analysis Services resource.</span></span>

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

### <span data-ttu-id="480b1-123">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="480b1-123">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="480b1-124">Punkt końcowy, który ma być używany podczas komunikowania się z interfejsem API analizy dzienników Azure.</span><span class="sxs-lookup"><span data-stu-id="480b1-124">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="480b1-125">-AzureAttestationServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="480b1-125">-AzureAttestationServiceEndpointResourceId</span></span>
<span data-ttu-id="480b1-126">Identyfikator zasobu usługi zaświadczeń na platformie Azure, który jest odbiorcą żądanego tokenu.</span><span class="sxs-lookup"><span data-stu-id="480b1-126">The The resource identifier of the Azure Attestation service that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="480b1-127">-AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="480b1-127">-AzureAttestationServiceEndpointSuffix</span></span>
<span data-ttu-id="480b1-128">Sufiks DNS usługi zaświadczeń na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="480b1-128">Dns suffix of Azure Attestation service.</span></span>

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

### <span data-ttu-id="480b1-129">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="480b1-129">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="480b1-130">Sufiks DNS dla zadań usługi Azure Data Lake Analytics i usług wykazu</span><span class="sxs-lookup"><span data-stu-id="480b1-130">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="480b1-131">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="480b1-131">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="480b1-132">Sufiks DNS w systemie plików usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="480b1-132">Dns Suffix of Azure Data Lake Store FileSystem.</span></span> <span data-ttu-id="480b1-133">Przykład: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="480b1-133">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="480b1-134">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="480b1-134">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="480b1-135">Sufiks DNS usługi magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="480b1-135">Dns suffix of Azure Key Vault service.</span></span> <span data-ttu-id="480b1-136">Przykład to vault-int.azure-int.net</span><span class="sxs-lookup"><span data-stu-id="480b1-136">Example is vault-int.azure-int.net</span></span>

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

### <span data-ttu-id="480b1-137">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="480b1-137">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="480b1-138">Identyfikator zasobu usługi danych magazynu kluczy platformy Azure, który jest odbiorcą żądanego tokenu.</span><span class="sxs-lookup"><span data-stu-id="480b1-138">Resource identifier of Azure Key Vault data service that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="480b1-139">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="480b1-139">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="480b1-140">Punkt końcowy, który ma być używany podczas komunikowania się z interfejsem API analizy dzienników Azure.</span><span class="sxs-lookup"><span data-stu-id="480b1-140">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="480b1-141">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="480b1-141">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="480b1-142">Odbiorcy tokenów uwierzytelniających się przy użyciu interfejsu API analizy dzienników Azure.</span><span class="sxs-lookup"><span data-stu-id="480b1-142">The audience for tokens authenticating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="480b1-143">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="480b1-143">-BatchEndpointResourceId</span></span>
<span data-ttu-id="480b1-144">Identyfikator zasobu usługi Azure Batch, który jest odbiorcą żądanego tokenu</span><span class="sxs-lookup"><span data-stu-id="480b1-144">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

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

### <span data-ttu-id="480b1-145">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="480b1-145">-DataLakeAudience</span></span>
<span data-ttu-id="480b1-146">Odbiorca tokenów uwierzytelniających się za pomocą punktu końcowego usługi AD Data Lake Services.</span><span class="sxs-lookup"><span data-stu-id="480b1-146">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

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

### <span data-ttu-id="480b1-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="480b1-147">-DefaultProfile</span></span>
<span data-ttu-id="480b1-148">Poświadczenia, konto, dzierżawca i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="480b1-148">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="480b1-149">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="480b1-149">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="480b1-150">Wskazuje, że dozwolone jest uwierzytelnianie lokalne usług federacyjnych Active Directory (ADFS).</span><span class="sxs-lookup"><span data-stu-id="480b1-150">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="480b1-151">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="480b1-151">-GalleryEndpoint</span></span>
<span data-ttu-id="480b1-152">Określa punkt końcowy galerii szablonów wdrażania usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="480b1-152">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="480b1-153">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="480b1-153">-GraphAudience</span></span>
<span data-ttu-id="480b1-154">Odbiorca tokenów uwierzytelniających się za pomocą punktu końcowego grafu AD.</span><span class="sxs-lookup"><span data-stu-id="480b1-154">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="480b1-155">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="480b1-155">-GraphEndpoint</span></span>
<span data-ttu-id="480b1-156">Określa adres URL żądań wykresu (metadanych usługi Active Directory).</span><span class="sxs-lookup"><span data-stu-id="480b1-156">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="480b1-157">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="480b1-157">-ManagementPortalUrl</span></span>
<span data-ttu-id="480b1-158">Określa adres URL portalu zarządzania.</span><span class="sxs-lookup"><span data-stu-id="480b1-158">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="480b1-159">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="480b1-159">-Name</span></span>
<span data-ttu-id="480b1-160">Określa nazwę środowiska, które ma zostać zmodyfikowane.</span><span class="sxs-lookup"><span data-stu-id="480b1-160">Specifies the name of the environment to modify.</span></span>

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

### <span data-ttu-id="480b1-161">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="480b1-161">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="480b1-162">Określa adres URL, z którego można pobrać pliki publishsettings.</span><span class="sxs-lookup"><span data-stu-id="480b1-162">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="480b1-163">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="480b1-163">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="480b1-164">Określa adres URL żądań usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="480b1-164">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="480b1-165">-Zakres</span><span class="sxs-lookup"><span data-stu-id="480b1-165">-Scope</span></span>
<span data-ttu-id="480b1-166">Określa zakres zmian kontekstu, na przykład, czy zmiany są stosowane tylko do bieżącego procesu, czy do wszystkich sesji uruchomionych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="480b1-166">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="480b1-167">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="480b1-167">-ServiceEndpoint</span></span>
<span data-ttu-id="480b1-168">Umożliwia określenie punktu końcowego dla żądań zarządzania usługami (REDDOG).</span><span class="sxs-lookup"><span data-stu-id="480b1-168">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="480b1-169">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="480b1-169">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="480b1-170">Określa sufiks nazwy domeny dla serwerów bazy danych platformy Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="480b1-170">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="480b1-171">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="480b1-171">-StorageEndpoint</span></span>
<span data-ttu-id="480b1-172">Umożliwia określenie punktu końcowego dostępu (obiektu BLOB, tabeli, kolejki i pliku).</span><span class="sxs-lookup"><span data-stu-id="480b1-172">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="480b1-173">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="480b1-173">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="480b1-174">Określa sufiks nazwy domeny dla usług programu Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="480b1-174">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="480b1-175">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="480b1-175">-Confirm</span></span>
<span data-ttu-id="480b1-176">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="480b1-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="480b1-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="480b1-177">-WhatIf</span></span>
<span data-ttu-id="480b1-178">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="480b1-178">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="480b1-179">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="480b1-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="480b1-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="480b1-180">CommonParameters</span></span>
<span data-ttu-id="480b1-181">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="480b1-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="480b1-182">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="480b1-182">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="480b1-183">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="480b1-183">INPUTS</span></span>

### <span data-ttu-id="480b1-184">System. String</span><span class="sxs-lookup"><span data-stu-id="480b1-184">System.String</span></span>

### <span data-ttu-id="480b1-185">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="480b1-185">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="480b1-186">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="480b1-186">OUTPUTS</span></span>

### <span data-ttu-id="480b1-187">Microsoft. Azure. Commands. profile. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="480b1-187">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="480b1-188">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="480b1-188">NOTES</span></span>

## <span data-ttu-id="480b1-189">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="480b1-189">RELATED LINKS</span></span>

[<span data-ttu-id="480b1-190">Dodaj-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="480b1-190">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="480b1-191">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="480b1-191">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="480b1-192">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="480b1-192">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

