---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 37e8952ab7337ae69e5c23ed4ab09e651acfac8c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523170"
---
# <span data-ttu-id="88301-101">Set-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="88301-101">Set-AzureRmEnvironment</span></span>

## <span data-ttu-id="88301-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="88301-102">SYNOPSIS</span></span>
<span data-ttu-id="88301-103">Ustawia właściwości dla środowiska platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="88301-103">Sets properties for an Azure environment.</span></span>

## <span data-ttu-id="88301-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="88301-104">SYNTAX</span></span>

```
Set-AzureRmEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
 [[-ManagementPortalUrl] <String>] [[-StorageEndpoint] <String>] [[-ActiveDirectoryEndpoint] <String>]
 [[-ResourceManagerEndpoint] <String>] [[-GalleryEndpoint] <String>]
 [[-ActiveDirectoryServiceEndpointResourceId] <String>] [[-GraphEndpoint] <String>]
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-TrafficManagerDnsSuffix] <String>] [[-SqlDatabaseDnsSuffix] <String>]
 [[-AzureDataLakeStoreFileSystemEndpointSuffix] <String>]
 [[-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix] <String>] [-EnableAdfsAuthentication]
 [[-AdTenant] <String>] [[-GraphAudience] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88301-105">Opis</span><span class="sxs-lookup"><span data-stu-id="88301-105">DESCRIPTION</span></span>
<span data-ttu-id="88301-106">Polecenie cmdlet Set-AzureRMEnvironment ustawia punkty końcowe i metadane w celu nawiązania połączenia z wystąpieniem platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="88301-106">The Set-AzureRMEnvironment cmdlet sets endpoints and metadata for connecting to an instance of Azure.</span></span>

## <span data-ttu-id="88301-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="88301-107">EXAMPLES</span></span>

### <span data-ttu-id="88301-108">Przykład 1: Tworzenie i modyfikowanie nowego środowiska</span><span class="sxs-lookup"><span data-stu-id="88301-108">Example 1: Creating and modifying a new environment</span></span>
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

<span data-ttu-id="88301-109">W tym przykładzie tworzymy nowe środowisko platformy Azure z przykładowymi punktami końcowymi przy użyciu polecenia Add-AzureRmEnvironment, a następnie zmieniamy wartość atrybutów ActiveDirectoryEndpoint i GraphEndpoint utworzonego środowiska za pomocą zestawu poleceń cmdlet Set-AzureRmEnvironment.</span><span class="sxs-lookup"><span data-stu-id="88301-109">In this example we are creating a new Azure environment with sample endpoints using Add-AzureRmEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzureRmEnvironment.</span></span>

## <span data-ttu-id="88301-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="88301-110">PARAMETERS</span></span>

### <span data-ttu-id="88301-111">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="88301-111">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="88301-112">Określa podstawowy urząd uwierzytelniania usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="88301-112">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="88301-113">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="88301-113">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="88301-114">Określa odbiorców tokenów uwierzytelniających żądania do punktów końcowych Menedżera zasobów platformy Azure lub zarządzania usługami (REDDOG, Service Management Manager).</span><span class="sxs-lookup"><span data-stu-id="88301-114">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="88301-115">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="88301-115">-AdTenant</span></span>
<span data-ttu-id="88301-116">Określa domyślną dzierżawę usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="88301-116">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="88301-117">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="88301-117">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="88301-118">Sufiks DNS dla zadań usługi Azure Data Lake Analytics i usług wykazu</span><span class="sxs-lookup"><span data-stu-id="88301-118">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="88301-119">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="88301-119">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="88301-120">Sufiks DNS w systemie plików usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="88301-120">Dns Suffix of Azure Data Lake Store FileSystem.</span></span>
<span data-ttu-id="88301-121">Przykład: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="88301-121">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="88301-122">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="88301-122">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="88301-123">Określa sufiks nazwy domeny dla usług magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="88301-123">Specifies the domain name suffix for Key Vault services.</span></span>

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

### <span data-ttu-id="88301-124">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="88301-124">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="88301-125">Określa odbiorców dla tokenów dostępu, które autoryzują żądania dotyczące usług magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="88301-125">Specifies the audience for access tokens that authorize requests for Key Vault services.</span></span>

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

### <span data-ttu-id="88301-126">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="88301-126">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="88301-127">Wskazuje, że dozwolone jest uwierzytelnianie lokalne usług federacyjnych Active Directory (ADFS).</span><span class="sxs-lookup"><span data-stu-id="88301-127">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="88301-128">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="88301-128">-GalleryEndpoint</span></span>
<span data-ttu-id="88301-129">Określa punkt końcowy galerii szablonów wdrażania usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="88301-129">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="88301-130">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="88301-130">-GraphAudience</span></span>
<span data-ttu-id="88301-131">Odbiorca tokenów uwierzytelniających się za pomocą punktu końcowego grafu AD.</span><span class="sxs-lookup"><span data-stu-id="88301-131">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="88301-132">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="88301-132">-GraphEndpoint</span></span>
<span data-ttu-id="88301-133">Określa adres URL żądań wykresu (metadanych usługi Active Directory).</span><span class="sxs-lookup"><span data-stu-id="88301-133">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="88301-134">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="88301-134">-ManagementPortalUrl</span></span>
<span data-ttu-id="88301-135">Określa adres URL portalu zarządzania.</span><span class="sxs-lookup"><span data-stu-id="88301-135">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="88301-136">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="88301-136">-Name</span></span>
<span data-ttu-id="88301-137">Określa nazwę środowiska, które ma zostać zmodyfikowane.</span><span class="sxs-lookup"><span data-stu-id="88301-137">Specifies the name of the environment to modify.</span></span>

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

### <span data-ttu-id="88301-138">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="88301-138">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="88301-139">Określa adres URL, z którego można pobrać pliki publishsettings.</span><span class="sxs-lookup"><span data-stu-id="88301-139">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="88301-140">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="88301-140">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="88301-141">Określa adres URL żądań usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="88301-141">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="88301-142">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="88301-142">-ServiceEndpoint</span></span>
<span data-ttu-id="88301-143">Umożliwia określenie punktu końcowego dla żądań zarządzania usługami (REDDOG).</span><span class="sxs-lookup"><span data-stu-id="88301-143">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="88301-144">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="88301-144">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="88301-145">Określa sufiks nazwy domeny dla serwerów bazy danych platformy Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="88301-145">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="88301-146">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="88301-146">-StorageEndpoint</span></span>
<span data-ttu-id="88301-147">Umożliwia określenie punktu końcowego dostępu (obiektu BLOB, tabeli, kolejki i pliku).</span><span class="sxs-lookup"><span data-stu-id="88301-147">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="88301-148">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="88301-148">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="88301-149">Określa sufiks nazwy domeny dla usług programu Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="88301-149">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="88301-150">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="88301-150">-Confirm</span></span>
<span data-ttu-id="88301-151">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88301-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88301-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88301-152">-WhatIf</span></span>
<span data-ttu-id="88301-153">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88301-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="88301-154">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="88301-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88301-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88301-155">CommonParameters</span></span>
<span data-ttu-id="88301-156">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88301-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88301-157">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88301-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88301-158">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="88301-158">INPUTS</span></span>

## <span data-ttu-id="88301-159">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="88301-159">OUTPUTS</span></span>

### <span data-ttu-id="88301-160">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="88301-160">PSAzureEnvironment</span></span>

## <span data-ttu-id="88301-161">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="88301-161">NOTES</span></span>

## <span data-ttu-id="88301-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="88301-162">RELATED LINKS</span></span>

[<span data-ttu-id="88301-163">Dodaj-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="88301-163">Add-AzureRMEnvironment</span></span>]()

[<span data-ttu-id="88301-164">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="88301-164">Get-AzureRMEnvironment</span></span>]()

[<span data-ttu-id="88301-165">Remove-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="88301-165">Remove-AzureRMEnvironment</span></span>]()

