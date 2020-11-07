---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/add-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Add-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Add-AzEnvironment.md
ms.openlocfilehash: b6616da9f357a02f91584c3388e3bdbc08d91b42
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707247"
---
# <span data-ttu-id="1a9c3-101">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="1a9c3-101">Add-AzEnvironment</span></span>

## <span data-ttu-id="1a9c3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1a9c3-102">SYNOPSIS</span></span>
<span data-ttu-id="1a9c3-103">Dodaje punkty końcowe i metadane wystąpienia Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1a9c3-103">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

## <span data-ttu-id="1a9c3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1a9c3-104">SYNTAX</span></span>

### <span data-ttu-id="1a9c3-105">Nazwa (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="1a9c3-105">Name (Default)</span></span>
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
 [-AzureAnalysisServicesEndpointResourceId <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a9c3-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="1a9c3-106">ARMEndpoint</span></span>
```
Add-AzEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-AzureAnalysisServicesEndpointSuffix <String>] [-AzureAnalysisServicesEndpointResourceId <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1a9c3-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1a9c3-107">DESCRIPTION</span></span>
<span data-ttu-id="1a9c3-108">Polecenie cmdlet Add-AzEnvironment umożliwia dodanie punktów końcowych i metadanych w celu włączenia poleceń cmdlet Menedżera zasobów platformy Azure w celu nawiązania połączenia z nowym wystąpieniem Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1a9c3-108">The Add-AzEnvironment cmdlet adds endpoints and metadata to enable Azure Resource Manager cmdlets to connect with a new instance of Azure Resource Manager.</span></span>
<span data-ttu-id="1a9c3-109">Wbudowane środowiska AzureCloud i AzureChinaCloud mają miejsce docelowe istniejące wystąpienia publiczne Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1a9c3-109">The built-in environments AzureCloud and AzureChinaCloud target existing public instances of Azure Resource Manager.</span></span>

## <span data-ttu-id="1a9c3-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1a9c3-110">EXAMPLES</span></span>

### <span data-ttu-id="1a9c3-111">Przykład 1: Tworzenie i modyfikowanie nowego środowiska</span><span class="sxs-lookup"><span data-stu-id="1a9c3-111">Example 1: Creating and modifying a new environment</span></span>
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
VersionProfiles                                   : {}
ExtendedProperties                                : {}
BatchEndpointResourceId                           :

In this example we are creating a new Azure environment with sample endpoints using Add-AzEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzEnvironment.
```

## <span data-ttu-id="1a9c3-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1a9c3-112">PARAMETERS</span></span>

### <span data-ttu-id="1a9c3-113">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="1a9c3-113">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="1a9c3-114">Określa podstawowy urząd uwierzytelniania usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1a9c3-114">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="1a9c3-115">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="1a9c3-115">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="1a9c3-116">Określa odbiorców tokenów uwierzytelniających żądania do punktów końcowych Menedżera zasobów platformy Azure lub zarządzania usługami (REDDOG, Service Management Manager).</span><span class="sxs-lookup"><span data-stu-id="1a9c3-116">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="1a9c3-117">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="1a9c3-117">-AdTenant</span></span>
<span data-ttu-id="1a9c3-118">Określa domyślną dzierżawę usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1a9c3-118">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="1a9c3-119">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="1a9c3-119">-ARMEndpoint</span></span>
<span data-ttu-id="1a9c3-120">Punkt końcowy usługi Azure Resource Manager</span><span class="sxs-lookup"><span data-stu-id="1a9c3-120">The Azure Resource Manager endpoint</span></span>

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

### <span data-ttu-id="1a9c3-121">-AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="1a9c3-121">-AzureAnalysisServicesEndpointResourceId</span></span>
<span data-ttu-id="1a9c3-122">Identyfikator zasobu zasobu usługi Azure Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="1a9c3-122">The resource identifier of the Azure Analysis Services resource.</span></span>

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

### <span data-ttu-id="1a9c3-123">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="1a9c3-123">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="1a9c3-124">Punkt końcowy, który ma być używany podczas komunikowania się z interfejsem API analizy dzienników Azure.</span><span class="sxs-lookup"><span data-stu-id="1a9c3-124">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="1a9c3-125">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="1a9c3-125">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="1a9c3-126">Sufiks DNS dla zadań usługi Azure Data Lake Analytics i usług wykazu</span><span class="sxs-lookup"><span data-stu-id="1a9c3-126">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="1a9c3-127">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="1a9c3-127">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="1a9c3-128">Sufiks DNS w systemie plików usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1a9c3-128">Dns Suffix of Azure Data Lake Store FileSystem.</span></span> <span data-ttu-id="1a9c3-129">Przykład: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="1a9c3-129">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="1a9c3-130">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="1a9c3-130">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="1a9c3-131">Sufiks DNS usługi magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1a9c3-131">Dns suffix of Azure Key Vault service.</span></span> <span data-ttu-id="1a9c3-132">Przykład to vault-int.azure-int.net</span><span class="sxs-lookup"><span data-stu-id="1a9c3-132">Example is vault-int.azure-int.net</span></span>

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

### <span data-ttu-id="1a9c3-133">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="1a9c3-133">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="1a9c3-134">Identyfikator zasobu usługi danych magazynu kluczy platformy Azure, który jest odbiorcą żądanego tokenu.</span><span class="sxs-lookup"><span data-stu-id="1a9c3-134">Resource identifier of Azure Key Vault data service that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="1a9c3-135">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="1a9c3-135">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="1a9c3-136">Punkt końcowy, który ma być używany podczas komunikowania się z interfejsem API analizy dzienników Azure.</span><span class="sxs-lookup"><span data-stu-id="1a9c3-136">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="1a9c3-137">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="1a9c3-137">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="1a9c3-138">Odbiorcy tokenów uwierzytelniających się przy użyciu interfejsu API analizy dzienników Azure.</span><span class="sxs-lookup"><span data-stu-id="1a9c3-138">The audience for tokens authenticating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="1a9c3-139">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="1a9c3-139">-BatchEndpointResourceId</span></span>
<span data-ttu-id="1a9c3-140">Identyfikator zasobu usługi Azure Batch, który jest odbiorcą żądanego tokenu</span><span class="sxs-lookup"><span data-stu-id="1a9c3-140">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

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

### <span data-ttu-id="1a9c3-141">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="1a9c3-141">-DataLakeAudience</span></span>
<span data-ttu-id="1a9c3-142">Odbiorca tokenów uwierzytelniających się za pomocą punktu końcowego usługi AD Data Lake Services.</span><span class="sxs-lookup"><span data-stu-id="1a9c3-142">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

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

### <span data-ttu-id="1a9c3-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a9c3-143">-DefaultProfile</span></span>
<span data-ttu-id="1a9c3-144">Poświadczenia, dzierżawca i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="1a9c3-144">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1a9c3-145">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="1a9c3-145">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="1a9c3-146">Wskazuje, że dozwolone jest uwierzytelnianie lokalne usług federacyjnych Active Directory (ADFS).</span><span class="sxs-lookup"><span data-stu-id="1a9c3-146">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="1a9c3-147">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="1a9c3-147">-GalleryEndpoint</span></span>
<span data-ttu-id="1a9c3-148">Określa punkt końcowy galerii szablonów wdrażania usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="1a9c3-148">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="1a9c3-149">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="1a9c3-149">-GraphAudience</span></span>
<span data-ttu-id="1a9c3-150">Odbiorca tokenów uwierzytelniających się za pomocą punktu końcowego grafu AD.</span><span class="sxs-lookup"><span data-stu-id="1a9c3-150">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="1a9c3-151">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="1a9c3-151">-GraphEndpoint</span></span>
<span data-ttu-id="1a9c3-152">Określa adres URL żądań wykresu (metadanych usługi Active Directory).</span><span class="sxs-lookup"><span data-stu-id="1a9c3-152">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="1a9c3-153">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="1a9c3-153">-ManagementPortalUrl</span></span>
<span data-ttu-id="1a9c3-154">Określa adres URL portalu zarządzania.</span><span class="sxs-lookup"><span data-stu-id="1a9c3-154">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="1a9c3-155">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1a9c3-155">-Name</span></span>
<span data-ttu-id="1a9c3-156">Określa nazwę środowiska, które ma zostać dodane.</span><span class="sxs-lookup"><span data-stu-id="1a9c3-156">Specifies the name of the environment to add.</span></span>

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

### <span data-ttu-id="1a9c3-157">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="1a9c3-157">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="1a9c3-158">Określa adres URL, z którego można pobrać pliki publishsettings.</span><span class="sxs-lookup"><span data-stu-id="1a9c3-158">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="1a9c3-159">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1a9c3-159">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="1a9c3-160">Określa adres URL żądań usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="1a9c3-160">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="1a9c3-161">-Zakres</span><span class="sxs-lookup"><span data-stu-id="1a9c3-161">-Scope</span></span>
<span data-ttu-id="1a9c3-162">Określa zakres zmian kontekstu, na przykład, czy zmiany są stosowane tylko do bieżącego procesu, czy do wszystkich sesji uruchomionych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="1a9c3-162">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="1a9c3-163">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="1a9c3-163">-ServiceEndpoint</span></span>
<span data-ttu-id="1a9c3-164">Umożliwia określenie punktu końcowego dla żądań zarządzania usługami (REDDOG).</span><span class="sxs-lookup"><span data-stu-id="1a9c3-164">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="1a9c3-165">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="1a9c3-165">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="1a9c3-166">Określa sufiks nazwy domeny dla serwerów bazy danych platformy Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="1a9c3-166">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="1a9c3-167">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="1a9c3-167">-StorageEndpoint</span></span>
<span data-ttu-id="1a9c3-168">Umożliwia określenie punktu końcowego dostępu (obiektu BLOB, tabeli, kolejki i pliku).</span><span class="sxs-lookup"><span data-stu-id="1a9c3-168">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="1a9c3-169">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="1a9c3-169">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="1a9c3-170">Określa sufiks nazwy domeny dla usług programu Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="1a9c3-170">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="1a9c3-171">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1a9c3-171">-Confirm</span></span>
<span data-ttu-id="1a9c3-172">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a9c3-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a9c3-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a9c3-173">-WhatIf</span></span>
<span data-ttu-id="1a9c3-174">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a9c3-174">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1a9c3-175">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1a9c3-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a9c3-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a9c3-176">CommonParameters</span></span>
<span data-ttu-id="1a9c3-177">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a9c3-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a9c3-178">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a9c3-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a9c3-179">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1a9c3-179">INPUTS</span></span>

### <span data-ttu-id="1a9c3-180">System. String</span><span class="sxs-lookup"><span data-stu-id="1a9c3-180">System.String</span></span>

### <span data-ttu-id="1a9c3-181">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1a9c3-181">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1a9c3-182">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1a9c3-182">OUTPUTS</span></span>

### <span data-ttu-id="1a9c3-183">Microsoft. Azure. Commands. profile. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="1a9c3-183">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="1a9c3-184">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1a9c3-184">NOTES</span></span>

## <span data-ttu-id="1a9c3-185">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1a9c3-185">RELATED LINKS</span></span>

[<span data-ttu-id="1a9c3-186">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="1a9c3-186">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="1a9c3-187">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="1a9c3-187">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

[<span data-ttu-id="1a9c3-188">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="1a9c3-188">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

