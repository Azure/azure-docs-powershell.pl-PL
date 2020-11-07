---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmEnvironment.md
ms.openlocfilehash: c39b61ab51296231b0952d1f12bd18e6d3aa13d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553795"
---
# <span data-ttu-id="497f8-101">Set-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="497f8-101">Set-AzureRmEnvironment</span></span>

## <span data-ttu-id="497f8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="497f8-102">SYNOPSIS</span></span>
<span data-ttu-id="497f8-103">Ustawia właściwości dla środowiska platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="497f8-103">Sets properties for an Azure environment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="497f8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="497f8-104">SYNTAX</span></span>

### <span data-ttu-id="497f8-105">Nazwa (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="497f8-105">Name (Default)</span></span>
```
Set-AzureRmEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
 [[-ManagementPortalUrl] <String>] [[-StorageEndpoint] <String>] [[-ActiveDirectoryEndpoint] <String>]
 [[-ResourceManagerEndpoint] <String>] [[-GalleryEndpoint] <String>]
 [[-ActiveDirectoryServiceEndpointResourceId] <String>] [[-GraphEndpoint] <String>]
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-TrafficManagerDnsSuffix] <String>] [[-SqlDatabaseDnsSuffix] <String>]
 [[-AzureDataLakeStoreFileSystemEndpointSuffix] <String>]
 [[-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix] <String>] [-EnableAdfsAuthentication]
 [[-AdTenant] <String>] [[-GraphAudience] <String>] [[-DataLakeAudience] <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="497f8-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="497f8-106">ARMEndpoint</span></span>
```
Set-AzureRmEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-DataLakeAudience] <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="497f8-107">Opis</span><span class="sxs-lookup"><span data-stu-id="497f8-107">DESCRIPTION</span></span>
<span data-ttu-id="497f8-108">Polecenie cmdlet Set-AzureRMEnvironment ustawia punkty końcowe i metadane w celu nawiązania połączenia z wystąpieniem platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="497f8-108">The Set-AzureRMEnvironment cmdlet sets endpoints and metadata for connecting to an instance of Azure.</span></span>

## <span data-ttu-id="497f8-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="497f8-109">EXAMPLES</span></span>

### <span data-ttu-id="497f8-110">Przykład 1: Tworzenie i modyfikowanie nowego środowiska</span><span class="sxs-lookup"><span data-stu-id="497f8-110">Example 1: Creating and modifying a new environment</span></span>
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

<span data-ttu-id="497f8-111">W tym przykładzie tworzymy nowe środowisko platformy Azure z przykładowymi punktami końcowymi przy użyciu polecenia Add-AzureRmEnvironment, a następnie zmieniamy wartość atrybutów ActiveDirectoryEndpoint i GraphEndpoint utworzonego środowiska za pomocą zestawu poleceń cmdlet Set-AzureRmEnvironment.</span><span class="sxs-lookup"><span data-stu-id="497f8-111">In this example we are creating a new Azure environment with sample endpoints using Add-AzureRmEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzureRmEnvironment.</span></span>

## <span data-ttu-id="497f8-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="497f8-112">PARAMETERS</span></span>

### <span data-ttu-id="497f8-113">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="497f8-113">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="497f8-114">Określa podstawowy urząd uwierzytelniania usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="497f8-114">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="497f8-115">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="497f8-115">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="497f8-116">Określa odbiorców tokenów uwierzytelniających żądania do punktów końcowych Menedżera zasobów platformy Azure lub zarządzania usługami (REDDOG, Service Management Manager).</span><span class="sxs-lookup"><span data-stu-id="497f8-116">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="497f8-117">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="497f8-117">-AdTenant</span></span>
<span data-ttu-id="497f8-118">Określa domyślną dzierżawę usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="497f8-118">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="497f8-119">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="497f8-119">-ARMEndpoint</span></span>
<span data-ttu-id="497f8-120">Punkt końcowy usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="497f8-120">The Azure Resource Manager endpoint.</span></span>

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

### <span data-ttu-id="497f8-121">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="497f8-121">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="497f8-122">Sufiks DNS dla zadań usługi Azure Data Lake Analytics i usług wykazu</span><span class="sxs-lookup"><span data-stu-id="497f8-122">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="497f8-123">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="497f8-123">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="497f8-124">Sufiks DNS w systemie plików usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="497f8-124">Dns Suffix of Azure Data Lake Store FileSystem.</span></span>
<span data-ttu-id="497f8-125">Przykład: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="497f8-125">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="497f8-126">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="497f8-126">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="497f8-127">Określa sufiks nazwy domeny dla usług magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="497f8-127">Specifies the domain name suffix for Key Vault services.</span></span>

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

### <span data-ttu-id="497f8-128">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="497f8-128">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="497f8-129">Określa odbiorców dla tokenów dostępu, które autoryzują żądania dotyczące usług magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="497f8-129">Specifies the audience for access tokens that authorize requests for Key Vault services.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="497f8-130">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="497f8-130">-DataLakeAudience</span></span>
<span data-ttu-id="497f8-131">Odbiorca tokenów uwierzytelniających się za pomocą punktu końcowego usługi AD Data Lake Services.</span><span class="sxs-lookup"><span data-stu-id="497f8-131">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

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

### <span data-ttu-id="497f8-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="497f8-132">-DefaultProfile</span></span>
<span data-ttu-id="497f8-133">Poświadczenia, konto, dzierżawca i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="497f8-133">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="497f8-134">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="497f8-134">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="497f8-135">Wskazuje, że dozwolone jest uwierzytelnianie lokalne usług federacyjnych Active Directory (ADFS).</span><span class="sxs-lookup"><span data-stu-id="497f8-135">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="497f8-136">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="497f8-136">-GalleryEndpoint</span></span>
<span data-ttu-id="497f8-137">Określa punkt końcowy galerii szablonów wdrażania usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="497f8-137">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="497f8-138">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="497f8-138">-GraphAudience</span></span>
<span data-ttu-id="497f8-139">Odbiorca tokenów uwierzytelniających się za pomocą punktu końcowego grafu AD.</span><span class="sxs-lookup"><span data-stu-id="497f8-139">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="497f8-140">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="497f8-140">-GraphEndpoint</span></span>
<span data-ttu-id="497f8-141">Określa adres URL żądań wykresu (metadanych usługi Active Directory).</span><span class="sxs-lookup"><span data-stu-id="497f8-141">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="497f8-142">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="497f8-142">-ManagementPortalUrl</span></span>
<span data-ttu-id="497f8-143">Określa adres URL portalu zarządzania.</span><span class="sxs-lookup"><span data-stu-id="497f8-143">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="497f8-144">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="497f8-144">-Name</span></span>
<span data-ttu-id="497f8-145">Określa nazwę środowiska, które ma zostać zmodyfikowane.</span><span class="sxs-lookup"><span data-stu-id="497f8-145">Specifies the name of the environment to modify.</span></span>

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

### <span data-ttu-id="497f8-146">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="497f8-146">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="497f8-147">Określa adres URL, z którego można pobrać pliki publishsettings.</span><span class="sxs-lookup"><span data-stu-id="497f8-147">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="497f8-148">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="497f8-148">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="497f8-149">Określa adres URL żądań usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="497f8-149">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="497f8-150">-Zakres</span><span class="sxs-lookup"><span data-stu-id="497f8-150">-Scope</span></span>
<span data-ttu-id="497f8-151">Określa zakres zmian kontekstu, na przykład wheher zmiany dotyczą tylko procesu cusrrent lub wszystkich sesji uruchomionych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="497f8-151">Determines the scope of context changes, for example, wheher changes apply only to the cusrrent process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="497f8-152">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="497f8-152">-ServiceEndpoint</span></span>
<span data-ttu-id="497f8-153">Umożliwia określenie punktu końcowego dla żądań zarządzania usługami (REDDOG).</span><span class="sxs-lookup"><span data-stu-id="497f8-153">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="497f8-154">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="497f8-154">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="497f8-155">Określa sufiks nazwy domeny dla serwerów bazy danych platformy Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="497f8-155">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="497f8-156">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="497f8-156">-StorageEndpoint</span></span>
<span data-ttu-id="497f8-157">Umożliwia określenie punktu końcowego dostępu (obiektu BLOB, tabeli, kolejki i pliku).</span><span class="sxs-lookup"><span data-stu-id="497f8-157">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="497f8-158">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="497f8-158">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="497f8-159">Określa sufiks nazwy domeny dla usług programu Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="497f8-159">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="497f8-160">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="497f8-160">-Confirm</span></span>
<span data-ttu-id="497f8-161">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="497f8-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="497f8-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="497f8-162">-WhatIf</span></span>
<span data-ttu-id="497f8-163">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="497f8-163">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="497f8-164">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="497f8-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="497f8-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="497f8-165">CommonParameters</span></span>
<span data-ttu-id="497f8-166">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="497f8-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="497f8-167">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="497f8-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="497f8-168">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="497f8-168">INPUTS</span></span>

## <span data-ttu-id="497f8-169">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="497f8-169">OUTPUTS</span></span>

### <span data-ttu-id="497f8-170">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="497f8-170">PSAzureEnvironment</span></span>

## <span data-ttu-id="497f8-171">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="497f8-171">NOTES</span></span>

## <span data-ttu-id="497f8-172">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="497f8-172">RELATED LINKS</span></span>

[<span data-ttu-id="497f8-173">Dodaj-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="497f8-173">Add-AzureRMEnvironment</span></span>](./Add-AzureRMEnvironment.md)

[<span data-ttu-id="497f8-174">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="497f8-174">Get-AzureRMEnvironment</span></span>](./Get-AzureRMEnvironment.md)

[<span data-ttu-id="497f8-175">Remove-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="497f8-175">Remove-AzureRMEnvironment</span></span>](./Remove-AzureRMEnvironment.md)
