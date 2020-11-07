---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/add-azurermenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Add-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Add-AzureRmEnvironment.md
ms.openlocfilehash: ef4f5128e92a319cb2b8ca021fc9b86f484d9b19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716485"
---
# <span data-ttu-id="b151f-101">Add-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="b151f-101">Add-AzureRmEnvironment</span></span>

## <span data-ttu-id="b151f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b151f-102">SYNOPSIS</span></span>
<span data-ttu-id="b151f-103">Dodaje punkty końcowe i metadane wystąpienia Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b151f-103">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b151f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b151f-104">SYNTAX</span></span>

### <span data-ttu-id="b151f-105">Nazwa (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="b151f-105">Name (Default)</span></span>
```
Add-AzureRmEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
 [[-ManagementPortalUrl] <String>] [[-StorageEndpoint] <String>] [[-ActiveDirectoryEndpoint] <String>]
 [[-ResourceManagerEndpoint] <String>] [[-GalleryEndpoint] <String>]
 [[-ActiveDirectoryServiceEndpointResourceId] <String>] [[-GraphEndpoint] <String>]
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-TrafficManagerDnsSuffix] <String>] [[-SqlDatabaseDnsSuffix] <String>]
 [[-AzureDataLakeStoreFileSystemEndpointSuffix] <String>]
 [[-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix] <String>] [-EnableAdfsAuthentication]
 [[-AdTenant] <String>] [[-GraphAudience] <String>] [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId <String>]]
 [[-AzureOperationalInsightsEndpoint] <String>] [[-AzureOperationalInsightsEndpointResourceId] <String>] 
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b151f-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="b151f-106">ARMEndpoint</span></span>
```
Add-AzureRmEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId <String>]]
 [[-AzureOperationalInsightsEndpoint] <String>] [[-AzureOperationalInsightsEndpointResourceId] <String>] 
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b151f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b151f-107">DESCRIPTION</span></span>
<span data-ttu-id="b151f-108">Polecenie cmdlet Add-AzureRmEnvironment umożliwia dodanie punktów końcowych i metadanych w celu włączenia poleceń cmdlet Menedżera zasobów platformy Azure w celu nawiązania połączenia z nowym wystąpieniem Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b151f-108">The Add-AzureRmEnvironment cmdlet adds endpoints and metadata to enable Azure Resource Manager cmdlets to connect with a new instance of Azure Resource Manager.</span></span>
<span data-ttu-id="b151f-109">Wbudowane środowiska AzureCloud i AzureChinaCloud mają miejsce docelowe istniejące wystąpienia publiczne Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b151f-109">The built-in environments AzureCloud and AzureChinaCloud target existing public instances of Azure Resource Manager.</span></span>

## <span data-ttu-id="b151f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b151f-110">EXAMPLES</span></span>

### <span data-ttu-id="b151f-111">Przykład 1: Tworzenie i modyfikowanie nowego środowiska</span><span class="sxs-lookup"><span data-stu-id="b151f-111">Example 1: Creating and modifying a new environment</span></span>
```
PS C:\> Add-AzureRmEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint TestADEndpoint `
        -ActiveDirectoryServiceEndpointResourceId TestADApplicationId `
        -ResourceManagerEndpoint TestRMEndpoint `
        -GalleryEndpoint TestGalleryEndpoint `
        -GraphEndpoint TestGraphEndpoint

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
ActiveDirectoryAuthority                          : TestADEndpoint
GraphUrl                                          : TestGraphEndpoint
GraphEndpointResourceId                           :
TrafficManagerDnsSuffix                           :
AzureKeyVaultDnsSuffix                            :
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            :

PS C:\> Set-AzureRmEnvironment -Name TestEnvironment
        -ActiveDirectoryEndpoint NewTestADEndpoint
        -GraphEndpoint NewTestGraphEndpoint

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
```

<span data-ttu-id="b151f-112">W tym przykładzie tworzymy nowe środowisko platformy Azure z przykładowymi punktami końcowymi przy użyciu polecenia Add-AzureRmEnvironment, a następnie zmieniamy wartość atrybutów ActiveDirectoryEndpoint i GraphEndpoint utworzonego środowiska za pomocą zestawu poleceń cmdlet Set-AzureRmEnvironment.</span><span class="sxs-lookup"><span data-stu-id="b151f-112">In this example we are creating a new Azure environment with sample endpoints using Add-AzureRmEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzureRmEnvironment.</span></span>

## <span data-ttu-id="b151f-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b151f-113">PARAMETERS</span></span>

### <span data-ttu-id="b151f-114">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="b151f-114">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="b151f-115">Określa podstawowy urząd uwierzytelniania usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b151f-115">Specifies the base authority for Azure Active Directory authentication.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: AdEndpointUrl, ActiveDirectory, ActiveDirectoryAuthority

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b151f-116">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="b151f-116">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="b151f-117">Określa odbiorców tokenów uwierzytelniających żądania do punktów końcowych Menedżera zasobów platformy Azure lub zarządzania usługami (REDDOG, Service Management Manager).</span><span class="sxs-lookup"><span data-stu-id="b151f-117">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b151f-118">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="b151f-118">-AdTenant</span></span>
<span data-ttu-id="b151f-119">Określa domyślną dzierżawę usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b151f-119">Specifies the default Active Directory tenant.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: 

Required: False
Position: 17
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b151f-120">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="b151f-120">-ARMEndpoint</span></span>
<span data-ttu-id="b151f-121">Punkt końcowy usługi Azure Resource Manager</span><span class="sxs-lookup"><span data-stu-id="b151f-121">The Azure Resource Manager endpoint</span></span>

```yaml
Type: String
Parameter Sets: ARMEndpoint
Aliases: ArmUrl

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b151f-122">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="b151f-122">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="b151f-123">Sufiks DNS dla zadań usługi Azure Data Lake Analytics i usług wykazu</span><span class="sxs-lookup"><span data-stu-id="b151f-123">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b151f-124">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="b151f-124">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="b151f-125">Sufiks DNS w systemie plików usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b151f-125">Dns Suffix of Azure Data Lake Store FileSystem.</span></span>
<span data-ttu-id="b151f-126">Przykład: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="b151f-126">Example: azuredatalake.net</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: 

Required: False
Position: 14
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b151f-127">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="b151f-127">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="b151f-128">Określa sufiks nazwy domeny dla usług magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="b151f-128">Specifies the domain name suffix for Key Vault services.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b151f-129">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="b151f-129">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="b151f-130">Określa odbiorców dla tokenów dostępu, które autoryzują żądania dotyczące usług magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="b151f-130">Specifies the audience for access tokens that authorize requests for Key Vault services.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b151f-131">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="b151f-131">-DataLakeAudience</span></span>
<span data-ttu-id="b151f-132">Odbiorca tokenów uwierzytelniających się za pomocą punktu końcowego usługi AD Data Lake Services.</span><span class="sxs-lookup"><span data-stu-id="b151f-132">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DataLakeEndpointResourceId, DataLakeResourceId

Required: False
Position: 19
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b151f-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b151f-133">-DefaultProfile</span></span>
<span data-ttu-id="b151f-134">Credeetnails, dzierżawa i subskrypcja używana do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b151f-134">The credeetnails, tenant and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b151f-135">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="b151f-135">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="b151f-136">Wskazuje, że dozwolone jest uwierzytelnianie lokalne usług federacyjnych Active Directory (ADFS).</span><span class="sxs-lookup"><span data-stu-id="b151f-136">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Name
Aliases: OnPremise

Required: False
Position: 16
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b151f-137">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="b151f-137">-GalleryEndpoint</span></span>
<span data-ttu-id="b151f-138">Określa punkt końcowy galerii szablonów wdrażania usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="b151f-138">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: Gallery, GalleryUrl

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b151f-139">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="b151f-139">-GraphAudience</span></span>
<span data-ttu-id="b151f-140">Odbiorca tokenów uwierzytelniających się za pomocą punktu końcowego grafu AD.</span><span class="sxs-lookup"><span data-stu-id="b151f-140">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: GraphEndpointResourceId, GraphResourceId

Required: False
Position: 18
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b151f-141">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="b151f-141">-GraphEndpoint</span></span>
<span data-ttu-id="b151f-142">Określa adres URL żądań wykresu (metadanych usługi Active Directory).</span><span class="sxs-lookup"><span data-stu-id="b151f-142">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: Graph, GraphUrl

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b151f-143">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="b151f-143">-ManagementPortalUrl</span></span>
<span data-ttu-id="b151f-144">Określa adres URL portalu zarządzania.</span><span class="sxs-lookup"><span data-stu-id="b151f-144">Specifies the URL for the Management Portal.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b151f-145">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b151f-145">-Name</span></span>
<span data-ttu-id="b151f-146">Określa nazwę środowiska, które ma zostać dodane.</span><span class="sxs-lookup"><span data-stu-id="b151f-146">Specifies the name of the environment to add.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b151f-147">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="b151f-147">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="b151f-148">Określa adres URL, z którego można pobrać pliki publishsettings.</span><span class="sxs-lookup"><span data-stu-id="b151f-148">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b151f-149">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b151f-149">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="b151f-150">Określa adres URL żądań usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="b151f-150">Specifies the URL for Azure Resource Manager requests.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: ResourceManager, ResourceManagerUrl

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b151f-151">-Zakres</span><span class="sxs-lookup"><span data-stu-id="b151f-151">-Scope</span></span>
<span data-ttu-id="b151f-152">Określa zakres zmian kontekstu, na przykład, czy zmiany są stosowane tylko do bieżącego procesu, czy do wszystkich sesji uruchomionych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="b151f-152">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b151f-153">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="b151f-153">-ServiceEndpoint</span></span>
<span data-ttu-id="b151f-154">Umożliwia określenie punktu końcowego dla żądań zarządzania usługami (REDDOG).</span><span class="sxs-lookup"><span data-stu-id="b151f-154">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: ServiceManagement, ServiceManagementUrl

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b151f-155">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="b151f-155">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="b151f-156">Określa sufiks nazwy domeny dla serwerów bazy danych platformy Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="b151f-156">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b151f-157">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="b151f-157">-StorageEndpoint</span></span>
<span data-ttu-id="b151f-158">Umożliwia określenie punktu końcowego dostępu (obiektu BLOB, tabeli, kolejki i pliku).</span><span class="sxs-lookup"><span data-stu-id="b151f-158">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageEndpointSuffix

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b151f-159">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="b151f-159">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="b151f-160">Określa sufiks nazwy domeny dla usług programu Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="b151f-160">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b151f-161">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="b151f-161">-BatchEndpointResourceId</span></span>
<span data-ttu-id="b151f-162">Identyfikator zasobu usługi Azure Batch, który jest odbiorcą żądanego tokenu</span><span class="sxs-lookup"><span data-stu-id="b151f-162">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 20
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b151f-163">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="b151f-163">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="b151f-164">Określa punkt końcowy dostępu do zapytań o szczegółowe dane.</span><span class="sxs-lookup"><span data-stu-id="b151f-164">Specifies the endpoint for the Operational Insights query access.</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 22
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b151f-165">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="b151f-165">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="b151f-166">Określa odbiorców dla tokenów dostępu, które autoryzują żądania dotyczące usług usługi Insights.</span><span class="sxs-lookup"><span data-stu-id="b151f-166">Specifies the audience for access tokens that authorize requests for Operational Insights services.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 21
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b151f-167">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b151f-167">-Confirm</span></span>
<span data-ttu-id="b151f-168">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b151f-168">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b151f-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b151f-169">-WhatIf</span></span>
<span data-ttu-id="b151f-170">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b151f-170">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b151f-171">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b151f-171">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b151f-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b151f-172">CommonParameters</span></span>
<span data-ttu-id="b151f-173">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b151f-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b151f-174">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b151f-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b151f-175">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b151f-175">INPUTS</span></span>

### <span data-ttu-id="b151f-176">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b151f-176">None</span></span>
<span data-ttu-id="b151f-177">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="b151f-177">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b151f-178">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b151f-178">OUTPUTS</span></span>

### <span data-ttu-id="b151f-179">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="b151f-179">PSAzureEnvironment</span></span>
<span data-ttu-id="b151f-180">To polecenie cmdlet zwraca zestaw punktów końcowych i metadanych wymaganych do komunikacji z wystąpieniem platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b151f-180">This cmdlet returns the set of endpoints and metadata needed to communicate with an instance of Azure.</span></span>

## <span data-ttu-id="b151f-181">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b151f-181">NOTES</span></span>

## <span data-ttu-id="b151f-182">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b151f-182">RELATED LINKS</span></span>

[<span data-ttu-id="b151f-183">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="b151f-183">Get-AzureRMEnvironment</span></span>](./Get-AzureRMEnvironment.md)

[<span data-ttu-id="b151f-184">Remove-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="b151f-184">Remove-AzureRMEnvironment</span></span>](./Remove-AzureRMEnvironment.md)

[<span data-ttu-id="b151f-185">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="b151f-185">Set-AzureRMEnvironment</span></span>](./Set-AzureRMEnvironment.md)

