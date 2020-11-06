---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/remove-azurermenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmEnvironment.md
ms.openlocfilehash: 2916a4048987d703bc1cbb44653eae2cfb066a29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551680"
---
# <span data-ttu-id="eba53-101">Remove-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="eba53-101">Remove-AzureRmEnvironment</span></span>

## <span data-ttu-id="eba53-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eba53-102">SYNOPSIS</span></span>
<span data-ttu-id="eba53-103">Umożliwia usunięcie punktów końcowych i metadanych w celu nawiązania połączenia z danym wystąpieniem platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="eba53-103">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eba53-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eba53-104">SYNTAX</span></span>

```
Remove-AzureRmEnvironment [-Name] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eba53-105">Opis</span><span class="sxs-lookup"><span data-stu-id="eba53-105">DESCRIPTION</span></span>
<span data-ttu-id="eba53-106">Polecenie cmdlet Remove-AzureRmEnvironment powoduje usunięcie punktów końcowych i informacji o metadanych w celu nawiązania połączenia z danym wystąpieniem platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="eba53-106">The Remove-AzureRmEnvironment cmdlet removes endpoints and metadata information for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="eba53-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eba53-107">EXAMPLES</span></span>

### <span data-ttu-id="eba53-108">Przykład 1: Tworzenie i usuwanie środowiska testowego</span><span class="sxs-lookup"><span data-stu-id="eba53-108">Example 1: Creating and removing a test environment</span></span>
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

PS C:\> Remove-AzureRmEnvironment -Name TestEnvironment

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
```

<span data-ttu-id="eba53-109">W tym przykładzie pokazano, jak utworzyć środowisko przy użyciu dodatku Add-AzureRmEnvironment, a następnie jak usunąć środowisko przy użyciu polecenia Remove-AzureRmEnvironment.</span><span class="sxs-lookup"><span data-stu-id="eba53-109">This example shows how to create an environment using Add-AzureRmEnvironment, and then how to delete the environment using Remove-AzureRmEnvironment.</span></span>

## <span data-ttu-id="eba53-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eba53-110">PARAMETERS</span></span>

### <span data-ttu-id="eba53-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eba53-111">-DefaultProfile</span></span>
<span data-ttu-id="eba53-112">Poświadczenia, dzierżawca i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="eba53-112">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eba53-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="eba53-113">-Name</span></span>
<span data-ttu-id="eba53-114">Określa nazwę środowiska, które ma zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="eba53-114">Specifies the name of the environment to remove.</span></span>

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

### <span data-ttu-id="eba53-115">-Zakres</span><span class="sxs-lookup"><span data-stu-id="eba53-115">-Scope</span></span>
<span data-ttu-id="eba53-116">Określa zakres zmian kontekstu, na przykład, czy zmiany są stosowane tylko do bieżącego procesu, czy do wszystkich sesji uruchomionych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="eba53-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="eba53-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="eba53-117">-Confirm</span></span>
<span data-ttu-id="eba53-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eba53-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eba53-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eba53-119">-WhatIf</span></span>
<span data-ttu-id="eba53-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eba53-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eba53-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="eba53-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eba53-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eba53-122">CommonParameters</span></span>
<span data-ttu-id="eba53-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eba53-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eba53-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eba53-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eba53-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eba53-125">INPUTS</span></span>

### <span data-ttu-id="eba53-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="eba53-126">None</span></span>
<span data-ttu-id="eba53-127">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="eba53-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="eba53-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eba53-128">OUTPUTS</span></span>

### <span data-ttu-id="eba53-129">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="eba53-129">PSAzureEnvironment</span></span>

## <span data-ttu-id="eba53-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eba53-130">NOTES</span></span>

## <span data-ttu-id="eba53-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eba53-131">RELATED LINKS</span></span>

[<span data-ttu-id="eba53-132">Dodaj-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="eba53-132">Add-AzureRMEnvironment</span></span>](./Add-AzureRMEnvironment.md)

[<span data-ttu-id="eba53-133">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="eba53-133">Get-AzureRMEnvironment</span></span>](./Get-AzureRMEnvironment.md)

[<span data-ttu-id="eba53-134">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="eba53-134">Set-AzureRMEnvironment</span></span>](./Set-AzureRMEnvironment.md)

