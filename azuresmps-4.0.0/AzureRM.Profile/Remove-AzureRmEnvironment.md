---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8d9c783d6fe4047aa1d179cd661c88d13e9c716b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710716"
---
# <span data-ttu-id="bea27-101">Remove-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="bea27-101">Remove-AzureRmEnvironment</span></span>

## <span data-ttu-id="bea27-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bea27-102">SYNOPSIS</span></span>
<span data-ttu-id="bea27-103">Umożliwia usunięcie punktów końcowych i metadanych w celu nawiązania połączenia z danym wystąpieniem platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bea27-103">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="bea27-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bea27-104">SYNTAX</span></span>

```
Remove-AzureRmEnvironment [-Name] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bea27-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bea27-105">DESCRIPTION</span></span>
<span data-ttu-id="bea27-106">Polecenie cmdlet Remove-AzureRmEnvironment powoduje usunięcie punktów końcowych i informacji o metadanych w celu nawiązania połączenia z danym wystąpieniem platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bea27-106">The Remove-AzureRmEnvironment cmdlet removes endpoints and metadata information for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="bea27-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bea27-107">EXAMPLES</span></span>

### <span data-ttu-id="bea27-108">Przykład 1: Tworzenie i usuwanie środowiska testowego</span><span class="sxs-lookup"><span data-stu-id="bea27-108">Example 1: Creating and removing a test environment</span></span>
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

<span data-ttu-id="bea27-109">W tym przykładzie pokazano, jak utworzyć środowisko przy użyciu dodatku Add-AzureRmEnvironment, a następnie jak usunąć środowisko przy użyciu polecenia Remove-AzureRmEnvironment.</span><span class="sxs-lookup"><span data-stu-id="bea27-109">This example shows how to create an environment using Add-AzureRmEnvironment, and then how to delete the environment using Remove-AzureRmEnvironment.</span></span>

## <span data-ttu-id="bea27-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bea27-110">PARAMETERS</span></span>

### <span data-ttu-id="bea27-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bea27-111">-Name</span></span>
<span data-ttu-id="bea27-112">Określa nazwę środowiska, które ma zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="bea27-112">Specifies the name of the environment to remove.</span></span>

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

### <span data-ttu-id="bea27-113">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bea27-113">-Confirm</span></span>
<span data-ttu-id="bea27-114">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bea27-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bea27-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bea27-115">-WhatIf</span></span>
<span data-ttu-id="bea27-116">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bea27-116">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bea27-117">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bea27-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bea27-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bea27-118">CommonParameters</span></span>
<span data-ttu-id="bea27-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bea27-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bea27-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bea27-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bea27-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bea27-121">INPUTS</span></span>

## <span data-ttu-id="bea27-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bea27-122">OUTPUTS</span></span>

### <span data-ttu-id="bea27-123">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="bea27-123">PSAzureEnvironment</span></span>

## <span data-ttu-id="bea27-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bea27-124">NOTES</span></span>

## <span data-ttu-id="bea27-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bea27-125">RELATED LINKS</span></span>

[<span data-ttu-id="bea27-126">Dodaj-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="bea27-126">Add-AzureRMEnvironment</span></span>]()

[<span data-ttu-id="bea27-127">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="bea27-127">Get-AzureRMEnvironment</span></span>]()

[<span data-ttu-id="bea27-128">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="bea27-128">Set-AzureRMEnvironment</span></span>]()

