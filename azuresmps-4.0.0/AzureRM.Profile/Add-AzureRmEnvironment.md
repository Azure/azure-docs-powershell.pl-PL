---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 650b5e2c930577101337c4fe0f33db9c32160e1e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523062"
---
# <span data-ttu-id="26725-101">Add-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="26725-101">Add-AzureRmEnvironment</span></span>

## <span data-ttu-id="26725-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="26725-102">SYNOPSIS</span></span>
<span data-ttu-id="26725-103">Dodaje punkty końcowe i metadane wystąpienia Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="26725-103">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

## <span data-ttu-id="26725-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="26725-104">SYNTAX</span></span>

```
Add-AzureRmEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
 [[-ManagementPortalUrl] <String>] [[-StorageEndpoint] <String>] [[-ActiveDirectoryEndpoint] <String>]
 [[-ResourceManagerEndpoint] <String>] [[-GalleryEndpoint] <String>]
 [[-ActiveDirectoryServiceEndpointResourceId] <String>] [[-GraphEndpoint] <String>]
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-TrafficManagerDnsSuffix] <String>] [[-SqlDatabaseDnsSuffix] <String>]
 [[-AzureDataLakeStoreFileSystemEndpointSuffix] <String>]
 [[-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix] <String>] [-EnableAdfsAuthentication]
 [[-AdTenant] <String>] [[-GraphAudience] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26725-105">Opis</span><span class="sxs-lookup"><span data-stu-id="26725-105">DESCRIPTION</span></span>
<span data-ttu-id="26725-106">Polecenie cmdlet Add-AzureRmEnvironment umożliwia dodanie punktów końcowych i metadanych w celu włączenia poleceń cmdlet Menedżera zasobów platformy Azure w celu nawiązania połączenia z nowym wystąpieniem Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="26725-106">The Add-AzureRmEnvironment cmdlet adds endpoints and metadata to enable Azure Resource Manager cmdlets to connect with a new instance of Azure Resource Manager.</span></span>
<span data-ttu-id="26725-107">Wbudowane środowiska AzureCloud i AzureChinaCloud mają miejsce docelowe istniejące wystąpienia publiczne Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="26725-107">The built-in environments AzureCloud and AzureChinaCloud target existing public instances of Azure Resource Manager.</span></span>

## <span data-ttu-id="26725-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="26725-108">EXAMPLES</span></span>

### <span data-ttu-id="26725-109">Przykład 1: Tworzenie i modyfikowanie nowego środowiska</span><span class="sxs-lookup"><span data-stu-id="26725-109">Example 1: Creating and modifying a new environment</span></span>
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

<span data-ttu-id="26725-110">W tym przykładzie tworzymy nowe środowisko platformy Azure z przykładowymi punktami końcowymi przy użyciu polecenia Add-AzureRmEnvironment, a następnie zmieniamy wartość atrybutów ActiveDirectoryEndpoint i GraphEndpoint utworzonego środowiska za pomocą zestawu poleceń cmdlet Set-AzureRmEnvironment.</span><span class="sxs-lookup"><span data-stu-id="26725-110">In this example we are creating a new Azure environment with sample endpoints using Add-AzureRmEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzureRmEnvironment.</span></span>

## <span data-ttu-id="26725-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="26725-111">PARAMETERS</span></span>

### <span data-ttu-id="26725-112">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="26725-112">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="26725-113">Określa podstawowy urząd uwierzytelniania usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="26725-113">Specifies the base authority for Azure Active Directory authentication.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AdEndpointUrl, ActiveDirectory, ActiveDirectoryAuthority

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26725-114">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="26725-114">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="26725-115">Określa odbiorców tokenów uwierzytelniających żądania do punktów końcowych Menedżera zasobów platformy Azure lub zarządzania usługami (REDDOG, Service Management Manager).</span><span class="sxs-lookup"><span data-stu-id="26725-115">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26725-116">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="26725-116">-AdTenant</span></span>
<span data-ttu-id="26725-117">Określa domyślną dzierżawę usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="26725-117">Specifies the default Active Directory tenant.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 17
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26725-118">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="26725-118">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="26725-119">Sufiks DNS dla zadań usługi Azure Data Lake Analytics i usług wykazu</span><span class="sxs-lookup"><span data-stu-id="26725-119">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26725-120">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="26725-120">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="26725-121">Sufiks DNS w systemie plików usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="26725-121">Dns Suffix of Azure Data Lake Store FileSystem.</span></span>
<span data-ttu-id="26725-122">Przykład: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="26725-122">Example: azuredatalake.net</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 14
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26725-123">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="26725-123">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="26725-124">Określa sufiks nazwy domeny dla usług magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="26725-124">Specifies the domain name suffix for Key Vault services.</span></span>

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

### <span data-ttu-id="26725-125">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="26725-125">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="26725-126">Określa odbiorców dla tokenów dostępu, które autoryzują żądania dotyczące usług magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="26725-126">Specifies the audience for access tokens that authorize requests for Key Vault services.</span></span>

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

### <span data-ttu-id="26725-127">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="26725-127">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="26725-128">Wskazuje, że dozwolone jest uwierzytelnianie lokalne usług federacyjnych Active Directory (ADFS).</span><span class="sxs-lookup"><span data-stu-id="26725-128">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: OnPremise

Required: False
Position: 16
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26725-129">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="26725-129">-GalleryEndpoint</span></span>
<span data-ttu-id="26725-130">Określa punkt końcowy galerii szablonów wdrażania usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="26725-130">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Gallery, GalleryUrl

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26725-131">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="26725-131">-GraphAudience</span></span>
<span data-ttu-id="26725-132">Odbiorca tokenów uwierzytelniających się za pomocą punktu końcowego grafu AD.</span><span class="sxs-lookup"><span data-stu-id="26725-132">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: GraphEndpointResourceId, GraphResourceId

Required: False
Position: 18
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26725-133">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="26725-133">-GraphEndpoint</span></span>
<span data-ttu-id="26725-134">Określa adres URL żądań wykresu (metadanych usługi Active Directory).</span><span class="sxs-lookup"><span data-stu-id="26725-134">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Graph, GraphUrl

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26725-135">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="26725-135">-ManagementPortalUrl</span></span>
<span data-ttu-id="26725-136">Określa adres URL portalu zarządzania.</span><span class="sxs-lookup"><span data-stu-id="26725-136">Specifies the URL for the Management Portal.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26725-137">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="26725-137">-Name</span></span>
<span data-ttu-id="26725-138">Określa nazwę środowiska, które ma zostać dodane.</span><span class="sxs-lookup"><span data-stu-id="26725-138">Specifies the name of the environment to add.</span></span>

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

### <span data-ttu-id="26725-139">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="26725-139">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="26725-140">Określa adres URL, z którego można pobrać pliki publishsettings.</span><span class="sxs-lookup"><span data-stu-id="26725-140">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26725-141">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="26725-141">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="26725-142">Określa adres URL żądań usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="26725-142">Specifies the URL for Azure Resource Manager requests.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceManager, ResourceManagerUrl

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26725-143">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="26725-143">-ServiceEndpoint</span></span>
<span data-ttu-id="26725-144">Umożliwia określenie punktu końcowego dla żądań zarządzania usługami (REDDOG).</span><span class="sxs-lookup"><span data-stu-id="26725-144">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceManagement, ServiceManagementUrl

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26725-145">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="26725-145">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="26725-146">Określa sufiks nazwy domeny dla serwerów bazy danych platformy Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="26725-146">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26725-147">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="26725-147">-StorageEndpoint</span></span>
<span data-ttu-id="26725-148">Umożliwia określenie punktu końcowego dostępu (obiektu BLOB, tabeli, kolejki i pliku).</span><span class="sxs-lookup"><span data-stu-id="26725-148">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="26725-149">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="26725-149">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="26725-150">Określa sufiks nazwy domeny dla usług programu Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="26725-150">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26725-151">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="26725-151">-Confirm</span></span>
<span data-ttu-id="26725-152">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26725-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26725-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26725-153">-WhatIf</span></span>
<span data-ttu-id="26725-154">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26725-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="26725-155">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="26725-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26725-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26725-156">CommonParameters</span></span>
<span data-ttu-id="26725-157">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26725-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26725-158">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26725-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26725-159">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="26725-159">INPUTS</span></span>

## <span data-ttu-id="26725-160">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="26725-160">OUTPUTS</span></span>

### <span data-ttu-id="26725-161">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="26725-161">PSAzureEnvironment</span></span>
<span data-ttu-id="26725-162">To polecenie cmdlet zwraca zestaw punktów końcowych i metadanych wymaganych do komunikacji z wystąpieniem platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="26725-162">This cmdlet returns the set of endpoints and metadata needed to communicate with an instance of Azure.</span></span>

## <span data-ttu-id="26725-163">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="26725-163">NOTES</span></span>

## <span data-ttu-id="26725-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="26725-164">RELATED LINKS</span></span>

[<span data-ttu-id="26725-165">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="26725-165">Get-AzureRMEnvironment</span></span>]()

[<span data-ttu-id="26725-166">Remove-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="26725-166">Remove-AzureRMEnvironment</span></span>]()

[<span data-ttu-id="26725-167">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="26725-167">Set-AzureRMEnvironment</span></span>]()

