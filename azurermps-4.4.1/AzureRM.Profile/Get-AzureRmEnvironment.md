---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmEnvironment.md
ms.openlocfilehash: 40aaec91fc33d28c6b32c0a058343439fd0f3020
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717168"
---
# <span data-ttu-id="66a05-101">Get-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="66a05-101">Get-AzureRmEnvironment</span></span>

## <span data-ttu-id="66a05-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="66a05-102">SYNOPSIS</span></span>
<span data-ttu-id="66a05-103">Uzyskiwanie punktów końcowych i metadanych dla wystąpienia usług platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="66a05-103">Get endpoints and metadata for an instance of Azure services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66a05-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="66a05-104">SYNTAX</span></span>

```
Get-AzureRmEnvironment [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66a05-105">Opis</span><span class="sxs-lookup"><span data-stu-id="66a05-105">DESCRIPTION</span></span>
<span data-ttu-id="66a05-106">Polecenie cmdlet Get-AzureRmEnvironment pobiera punkty końcowe i metadane wystąpienia usług platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="66a05-106">The Get-AzureRmEnvironment cmdlet gets endpoints and metadata for an instance of Azure services.</span></span>

## <span data-ttu-id="66a05-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="66a05-107">EXAMPLES</span></span>

### <span data-ttu-id="66a05-108">Przykład 1: uzyskiwanie środowiska AzureCloud</span><span class="sxs-lookup"><span data-stu-id="66a05-108">Example 1: Getting the AzureCloud environment</span></span>
```
PS C:\> Get-AzureRmEnvironment AzureCloud

Name                                              : AzureCloud
EnableAdfsAuthentication                          : False
ActiveDirectoryServiceEndpointResourceId          : https://management.core.windows.net/
AdTenant                                          :
GalleryUrl                                        : https://gallery.azure.com/
ManagementPortalUrl                               : https://go.microsoft.com/fwlink/?LinkId=254433
ServiceManagementUrl                              : https://management.core.windows.net/
PublishSettingsFileUrl                            : https://go.microsoft.com/fwlink/?LinkID=301775
ResourceManagerUrl                                : https://management.azure.com/
SqlDatabaseDnsSuffix                              : .database.windows.net
StorageEndpointSuffix                             : core.windows.net
ActiveDirectoryAuthority                          : https://login.microsoftonline.com/
GraphUrl                                          : https://graph.windows.net/
GraphEndpointResourceId                           : https://graph.windows.net/
TrafficManagerDnsSuffix                           : trafficmanager.net
AzureKeyVaultDnsSuffix                            : vault.azure.net
AzureDataLakeStoreFileSystemEndpointSuffix        : azuredatalakestore.net
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix : azuredatalakeanalytics.net
AzureKeyVaultServiceEndpointResourceId            : https://vault.azure.net
```

<span data-ttu-id="66a05-109">W tym przykładzie pokazano, jak uzyskać punkty końcowe i metadane dla środowiska AzureCloud (domyślnego).</span><span class="sxs-lookup"><span data-stu-id="66a05-109">This example shows how to get the endpoints and metadata for the AzureCloud (default) environment.</span></span>

### <span data-ttu-id="66a05-110">Przykład 2: uzyskiwanie środowiska AzureChinaCloud</span><span class="sxs-lookup"><span data-stu-id="66a05-110">Example 2: Getting the AzureChinaCloud environment</span></span>
```
PS C:\> Get-AzureRmEnvironment AzureChinaCloud

Name                                              : AzureChinaCloud
EnableAdfsAuthentication                          : False
ActiveDirectoryServiceEndpointResourceId          : https://management.core.chinacloudapi.cn/
AdTenant                                          :
GalleryUrl                                        : https://gallery.chinacloudapi.cn/
ManagementPortalUrl                               : https://go.microsoft.com/fwlink/?LinkId=301902
ServiceManagementUrl                              : https://management.core.chinacloudapi.cn/
PublishSettingsFileUrl                            : https://go.microsoft.com/fwlink/?LinkID=301776
ResourceManagerUrl                                : https://management.chinacloudapi.cn/
SqlDatabaseDnsSuffix                              : .database.chinacloudapi.cn
StorageEndpointSuffix                             : core.chinacloudapi.cn
ActiveDirectoryAuthority                          : https://login.chinacloudapi.cn/
GraphUrl                                          : https://graph.chinacloudapi.cn/
GraphEndpointResourceId                           : https://graph.chinacloudapi.cn/
TrafficManagerDnsSuffix                           : trafficmanager.cn
AzureKeyVaultDnsSuffix                            : vault.azure.cn
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            : https://vault.azure.cn
```

<span data-ttu-id="66a05-111">W tym przykładzie pokazano, jak uzyskać punkty końcowe i metadane środowiska AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="66a05-111">This example shows how to get the endpoints and metadata for the AzureChinaCloud environment.</span></span>

### <span data-ttu-id="66a05-112">Przykład 3: uzyskiwanie środowiska AzureUSGovernment</span><span class="sxs-lookup"><span data-stu-id="66a05-112">Example 3: Getting the AzureUSGovernment environment</span></span>
```
PS C:\> Get-AzureRmEnvironment AzureUSGovernment

Name                                              : AzureUSGovernment
EnableAdfsAuthentication                          : False
ActiveDirectoryServiceEndpointResourceId          : https://management.core.usgovcloudapi.net/
AdTenant                                          :
GalleryUrl                                        : https://gallery.usgovcloudapi.net/
ManagementPortalUrl                               : https://manage.windowsazure.us
ServiceManagementUrl                              : https://management.core.usgovcloudapi.net/
PublishSettingsFileUrl                            : https://manage.windowsazure.us/publishsettings/index
ResourceManagerUrl                                : https://management.usgovcloudapi.net/
SqlDatabaseDnsSuffix                              : .database.usgovcloudapi.net
StorageEndpointSuffix                             : core.usgovcloudapi.net
ActiveDirectoryAuthority                          : https://login-us.microsoftonline.com/
GraphUrl                                          : https://graph.windows.net/
GraphEndpointResourceId                           : https://graph.windows.net/
TrafficManagerDnsSuffix                           : usgovtrafficmanager.net
AzureKeyVaultDnsSuffix                            : vault.usgovcloudapi.net
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            : https://vault.usgovcloudapi.net
```

<span data-ttu-id="66a05-113">W tym przykładzie pokazano, jak uzyskać punkty końcowe i metadane środowiska AzureUSGovernment.</span><span class="sxs-lookup"><span data-stu-id="66a05-113">This example shows how to get the endpoints and metadata for the AzureUSGovernment environment.</span></span>

## <span data-ttu-id="66a05-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="66a05-114">PARAMETERS</span></span>

### <span data-ttu-id="66a05-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66a05-115">-DefaultProfile</span></span>
<span data-ttu-id="66a05-116">Poświadczenia, konto, dzierżawca i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="66a05-116">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66a05-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="66a05-117">-Name</span></span>
<span data-ttu-id="66a05-118">Określa nazwę wystąpienia platformy Azure, które ma zostać pozyskane.</span><span class="sxs-lookup"><span data-stu-id="66a05-118">Specifies the name of the Azure instance to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66a05-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66a05-119">CommonParameters</span></span>
<span data-ttu-id="66a05-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66a05-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66a05-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66a05-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66a05-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="66a05-122">INPUTS</span></span>

## <span data-ttu-id="66a05-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="66a05-123">OUTPUTS</span></span>

### <span data-ttu-id="66a05-124">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="66a05-124">PSAzureEnvironment</span></span>

## <span data-ttu-id="66a05-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="66a05-125">NOTES</span></span>

## <span data-ttu-id="66a05-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="66a05-126">RELATED LINKS</span></span>

[<span data-ttu-id="66a05-127">Dodaj-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="66a05-127">Add-AzureRMEnvironment</span></span>](./Add-AzureRMEnvironment.md)

[<span data-ttu-id="66a05-128">Remove-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="66a05-128">Remove-AzureRMEnvironment</span></span>](./Remove-AzureRMEnvironment.md)

[<span data-ttu-id="66a05-129">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="66a05-129">Set-AzureRMEnvironment</span></span>](./Set-AzureRMEnvironment.md)

