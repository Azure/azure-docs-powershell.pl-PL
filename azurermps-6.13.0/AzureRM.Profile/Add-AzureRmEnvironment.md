---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/add-azurermenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Add-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Add-AzureRmEnvironment.md
ms.openlocfilehash: ed50d8e25dca0998e7e3e026783fe4ec78e6ce7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524337"
---
# <span data-ttu-id="f527d-101">Add-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="f527d-101">Add-AzureRmEnvironment</span></span>

## <span data-ttu-id="f527d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f527d-102">SYNOPSIS</span></span>
<span data-ttu-id="f527d-103">Dodaje punkty końcowe i metadane wystąpienia Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f527d-103">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f527d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f527d-104">SYNTAX</span></span>

### <span data-ttu-id="f527d-105">Nazwa (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="f527d-105">Name (Default)</span></span>
```
Add-AzureRmEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
 [[-ManagementPortalUrl] <String>] [[-StorageEndpoint] <String>] [[-ActiveDirectoryEndpoint] <String>]
 [[-ResourceManagerEndpoint] <String>] [[-GalleryEndpoint] <String>]
 [[-ActiveDirectoryServiceEndpointResourceId] <String>] [[-GraphEndpoint] <String>]
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-TrafficManagerDnsSuffix] <String>] [[-SqlDatabaseDnsSuffix] <String>]
 [[-AzureDataLakeStoreFileSystemEndpointSuffix] <String>]
 [[-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix] <String>] [-EnableAdfsAuthentication]
 [[-AdTenant] <String>] [[-GraphAudience] <String>] [[-DataLakeAudience] <String>]
 [[-BatchEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpoint] <String>] [-AzureAnalysisServicesEndpointSuffix <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f527d-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="f527d-106">ARMEndpoint</span></span>
```
Add-AzureRmEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f527d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f527d-107">DESCRIPTION</span></span>
<span data-ttu-id="f527d-108">Polecenie cmdlet Add-AzureRmEnvironment umożliwia dodanie punktów końcowych i metadanych w celu włączenia poleceń cmdlet Menedżera zasobów platformy Azure w celu nawiązania połączenia z nowym wystąpieniem Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f527d-108">The Add-AzureRmEnvironment cmdlet adds endpoints and metadata to enable Azure Resource Manager cmdlets to connect with a new instance of Azure Resource Manager.</span></span>
<span data-ttu-id="f527d-109">Wbudowane środowiska AzureCloud i AzureChinaCloud mają miejsce docelowe istniejące wystąpienia publiczne Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f527d-109">The built-in environments AzureCloud and AzureChinaCloud target existing public instances of Azure Resource Manager.</span></span>

## <span data-ttu-id="f527d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f527d-110">EXAMPLES</span></span>

### <span data-ttu-id="f527d-111">Przykład 1: Tworzenie i modyfikowanie nowego środowiska</span><span class="sxs-lookup"><span data-stu-id="f527d-111">Example 1: Creating and modifying a new environment</span></span>
```
PS C:\> Add-AzureRmEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint TestADEndpoint `
        -ActiveDirectoryServiceEndpointResourceId TestADApplicationId `
        -ResourceManagerEndpoint TestRMEndpoint `
        -GalleryEndpoint TestGalleryEndpoint `
        -GraphEndpoint TestGraphEndpoint

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/

PS C:\> Set-AzureRmEnvironment -Name TestEnvironment `
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

In this example we are creating a new Azure environment with sample endpoints using Add-AzureRmEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzureRmEnvironment.
```

## <span data-ttu-id="f527d-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f527d-112">PARAMETERS</span></span>

### <span data-ttu-id="f527d-113">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="f527d-113">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="f527d-114">Określa podstawowy urząd uwierzytelniania usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f527d-114">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="f527d-115">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="f527d-115">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="f527d-116">Określa odbiorców tokenów uwierzytelniających żądania do punktów końcowych Menedżera zasobów platformy Azure lub zarządzania usługami (REDDOG, Service Management Manager).</span><span class="sxs-lookup"><span data-stu-id="f527d-116">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="f527d-117">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="f527d-117">-AdTenant</span></span>
<span data-ttu-id="f527d-118">Określa domyślną dzierżawę usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f527d-118">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="f527d-119">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="f527d-119">-ARMEndpoint</span></span>
<span data-ttu-id="f527d-120">Punkt końcowy usługi Azure Resource Manager</span><span class="sxs-lookup"><span data-stu-id="f527d-120">The Azure Resource Manager endpoint</span></span>

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

### <span data-ttu-id="f527d-121">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="f527d-121">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="f527d-122">Sufiks DNS punktów końcowych usługi Azure Analysis Services</span><span class="sxs-lookup"><span data-stu-id="f527d-122">Dns Suffix of Azure Analysis Services service endpoints</span></span>

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


### <span data-ttu-id="f527d-123">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="f527d-123">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="f527d-124">Sufiks DNS dla zadań usługi Azure Data Lake Analytics i usług wykazu</span><span class="sxs-lookup"><span data-stu-id="f527d-124">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="f527d-125">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="f527d-125">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="f527d-126">Sufiks DNS w systemie plików usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f527d-126">Dns Suffix of Azure Data Lake Store FileSystem.</span></span>
<span data-ttu-id="f527d-127">Przykład: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="f527d-127">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="f527d-128">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="f527d-128">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="f527d-129">Określa sufiks nazwy domeny dla usług magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="f527d-129">Specifies the domain name suffix for Key Vault services.</span></span>

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

### <span data-ttu-id="f527d-130">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="f527d-130">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="f527d-131">Określa odbiorców dla tokenów dostępu, które autoryzują żądania dotyczące usług magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="f527d-131">Specifies the audience for access tokens that authorize requests for Key Vault services.</span></span>

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

### <span data-ttu-id="f527d-132">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="f527d-132">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="f527d-133">Określa punkt końcowy dostępu do zapytań o szczegółowe dane.</span><span class="sxs-lookup"><span data-stu-id="f527d-133">Specifies the endpoint for the Operational Insights query access.</span></span> 

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

### <span data-ttu-id="f527d-134">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="f527d-134">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="f527d-135">Określa odbiorców dla tokenów dostępu, które autoryzują żądania dotyczące usług usługi Insights.</span><span class="sxs-lookup"><span data-stu-id="f527d-135">Specifies the audience for access tokens that authorize requests for Operational Insights services.</span></span>

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

### <span data-ttu-id="f527d-136">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="f527d-136">-BatchEndpointResourceId</span></span>
<span data-ttu-id="f527d-137">Identyfikator zasobu usługi Azure Batch, który jest odbiorcą żądanego tokenu</span><span class="sxs-lookup"><span data-stu-id="f527d-137">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

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

### <span data-ttu-id="f527d-138">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="f527d-138">-DataLakeAudience</span></span>
<span data-ttu-id="f527d-139">Odbiorca tokenów uwierzytelniających się za pomocą punktu końcowego usługi AD Data Lake Services.</span><span class="sxs-lookup"><span data-stu-id="f527d-139">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

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

### <span data-ttu-id="f527d-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f527d-140">-DefaultProfile</span></span>
<span data-ttu-id="f527d-141">Credeetnails, dzierżawa i subskrypcja używana do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f527d-141">The credeetnails, tenant and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f527d-142">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="f527d-142">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="f527d-143">Wskazuje, że dozwolone jest uwierzytelnianie lokalne usług federacyjnych Active Directory (ADFS).</span><span class="sxs-lookup"><span data-stu-id="f527d-143">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="f527d-144">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="f527d-144">-GalleryEndpoint</span></span>
<span data-ttu-id="f527d-145">Określa punkt końcowy galerii szablonów wdrażania usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="f527d-145">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="f527d-146">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="f527d-146">-GraphAudience</span></span>
<span data-ttu-id="f527d-147">Odbiorca tokenów uwierzytelniających się za pomocą punktu końcowego grafu AD.</span><span class="sxs-lookup"><span data-stu-id="f527d-147">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="f527d-148">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="f527d-148">-GraphEndpoint</span></span>
<span data-ttu-id="f527d-149">Określa adres URL żądań wykresu (metadanych usługi Active Directory).</span><span class="sxs-lookup"><span data-stu-id="f527d-149">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="f527d-150">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="f527d-150">-ManagementPortalUrl</span></span>
<span data-ttu-id="f527d-151">Określa adres URL portalu zarządzania.</span><span class="sxs-lookup"><span data-stu-id="f527d-151">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="f527d-152">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f527d-152">-Name</span></span>
<span data-ttu-id="f527d-153">Określa nazwę środowiska, które ma zostać dodane.</span><span class="sxs-lookup"><span data-stu-id="f527d-153">Specifies the name of the environment to add.</span></span>

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

### <span data-ttu-id="f527d-154">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="f527d-154">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="f527d-155">Określa adres URL, z którego można pobrać pliki publishsettings.</span><span class="sxs-lookup"><span data-stu-id="f527d-155">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="f527d-156">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f527d-156">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="f527d-157">Określa adres URL żądań usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="f527d-157">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="f527d-158">-Zakres</span><span class="sxs-lookup"><span data-stu-id="f527d-158">-Scope</span></span>
<span data-ttu-id="f527d-159">Określa zakres zmian kontekstu, na przykład, czy zmiany są stosowane tylko do bieżącego procesu, czy do wszystkich sesji uruchomionych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f527d-159">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="f527d-160">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="f527d-160">-ServiceEndpoint</span></span>
<span data-ttu-id="f527d-161">Umożliwia określenie punktu końcowego dla żądań zarządzania usługami (REDDOG).</span><span class="sxs-lookup"><span data-stu-id="f527d-161">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="f527d-162">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="f527d-162">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="f527d-163">Określa sufiks nazwy domeny dla serwerów bazy danych platformy Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="f527d-163">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="f527d-164">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="f527d-164">-StorageEndpoint</span></span>
<span data-ttu-id="f527d-165">Umożliwia określenie punktu końcowego dostępu (obiektu BLOB, tabeli, kolejki i pliku).</span><span class="sxs-lookup"><span data-stu-id="f527d-165">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="f527d-166">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="f527d-166">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="f527d-167">Określa sufiks nazwy domeny dla usług programu Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="f527d-167">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="f527d-168">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f527d-168">-Confirm</span></span>
<span data-ttu-id="f527d-169">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f527d-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f527d-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f527d-170">-WhatIf</span></span>
<span data-ttu-id="f527d-171">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f527d-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f527d-172">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f527d-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f527d-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f527d-173">CommonParameters</span></span>
<span data-ttu-id="f527d-174">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f527d-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f527d-175">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f527d-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f527d-176">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f527d-176">INPUTS</span></span>

### <span data-ttu-id="f527d-177">System. String</span><span class="sxs-lookup"><span data-stu-id="f527d-177">System.String</span></span>

### <span data-ttu-id="f527d-178">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f527d-178">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f527d-179">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f527d-179">OUTPUTS</span></span>

### <span data-ttu-id="f527d-180">Microsoft. Azure. Commands. profile. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="f527d-180">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="f527d-181">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f527d-181">NOTES</span></span>

## <span data-ttu-id="f527d-182">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f527d-182">RELATED LINKS</span></span>

[<span data-ttu-id="f527d-183">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="f527d-183">Get-AzureRMEnvironment</span></span>](./Get-AzureRMEnvironment.md)

[<span data-ttu-id="f527d-184">Remove-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="f527d-184">Remove-AzureRMEnvironment</span></span>](./Remove-AzureRMEnvironment.md)

[<span data-ttu-id="f527d-185">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="f527d-185">Set-AzureRMEnvironment</span></span>](./Set-AzureRMEnvironment.md)

