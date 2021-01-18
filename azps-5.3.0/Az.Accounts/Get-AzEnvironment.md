---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzEnvironment.md
ms.openlocfilehash: 176874b9d3fbf192597cd98659e45df800dc819c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98500586"
---
# <span data-ttu-id="6496c-101">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="6496c-101">Get-AzEnvironment</span></span>

## <span data-ttu-id="6496c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6496c-102">SYNOPSIS</span></span>
<span data-ttu-id="6496c-103">Uzyskiwanie punktów końcowych i metadanych dla wystąpienia usług platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6496c-103">Get endpoints and metadata for an instance of Azure services.</span></span>

## <span data-ttu-id="6496c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6496c-104">SYNTAX</span></span>

```
Get-AzEnvironment [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6496c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6496c-105">DESCRIPTION</span></span>
<span data-ttu-id="6496c-106">Polecenie cmdlet Get-AzEnvironment pobiera punkty końcowe i metadane wystąpienia usług platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6496c-106">The Get-AzEnvironment cmdlet gets endpoints and metadata for an instance of Azure services.</span></span>

## <span data-ttu-id="6496c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6496c-107">EXAMPLES</span></span>

### <span data-ttu-id="6496c-108">Przykład 1: uzyskiwanie środowiska AzureCloud</span><span class="sxs-lookup"><span data-stu-id="6496c-108">Example 1: Getting the AzureCloud environment</span></span>
```
PS C:\> Get-AzEnvironment AzureCloud

Name       Resource Manager Url          ActiveDirectory Authority
----       --------------------          -------------------------
AzureCloud https://management.azure.com/ https://login.microsoftonline.com/
```

<span data-ttu-id="6496c-109">W tym przykładzie pokazano, jak uzyskać punkty końcowe i metadane dla środowiska AzureCloud (domyślnego).</span><span class="sxs-lookup"><span data-stu-id="6496c-109">This example shows how to get the endpoints and metadata for the AzureCloud (default) environment.</span></span>

### <span data-ttu-id="6496c-110">Przykład 2: uzyskiwanie środowiska AzureChinaCloud</span><span class="sxs-lookup"><span data-stu-id="6496c-110">Example 2: Getting the AzureChinaCloud environment</span></span>
```
PS C:\> Get-AzEnvironment AzureChinaCloud | Format-List

Name                                              : AzureChinaCloud
EnableAdfsAuthentication                          : False
ActiveDirectoryServiceEndpointResourceId          : https://management.core.chinacloudapi.cn/
AdTenant                                          :
GalleryUrl                                        : https://gallery.chinacloudapi.cn/
ManagementPortalUrl                               : http://go.microsoft.com/fwlink/?LinkId=301902
ServiceManagementUrl                              : https://management.core.chinacloudapi.cn/
PublishSettingsFileUrl                            : http://go.microsoft.com/fwlink/?LinkID=301776
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

<span data-ttu-id="6496c-111">W tym przykładzie pokazano, jak uzyskać punkty końcowe i metadane środowiska AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="6496c-111">This example shows how to get the endpoints and metadata for the AzureChinaCloud environment.</span></span>

### <span data-ttu-id="6496c-112">Przykład 3: uzyskiwanie środowiska AzureUSGovernment</span><span class="sxs-lookup"><span data-stu-id="6496c-112">Example 3: Getting the AzureUSGovernment environment</span></span>
```
PS C:\> Get-AzEnvironment AzureUSGovernment

Name              Resource Manager Url                  ActiveDirectory Authority
----              --------------------                  -------------------------
AzureUSGovernment https://management.usgovcloudapi.net/ https://login.microsoftonline.us/
```

<span data-ttu-id="6496c-113">W tym przykładzie pokazano, jak uzyskać punkty końcowe i metadane środowiska AzureUSGovernment.</span><span class="sxs-lookup"><span data-stu-id="6496c-113">This example shows how to get the endpoints and metadata for the AzureUSGovernment environment.</span></span>

## <span data-ttu-id="6496c-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6496c-114">PARAMETERS</span></span>

### <span data-ttu-id="6496c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6496c-115">-DefaultProfile</span></span>
<span data-ttu-id="6496c-116">Poświadczenia, konto, dzierżawca i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6496c-116">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6496c-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6496c-117">-Name</span></span>
<span data-ttu-id="6496c-118">Określa nazwę wystąpienia platformy Azure, które ma zostać pozyskane.</span><span class="sxs-lookup"><span data-stu-id="6496c-118">Specifies the name of the Azure instance to get.</span></span>

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

### <span data-ttu-id="6496c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6496c-119">CommonParameters</span></span>
<span data-ttu-id="6496c-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6496c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6496c-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6496c-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6496c-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6496c-122">INPUTS</span></span>

### <span data-ttu-id="6496c-123">System. String</span><span class="sxs-lookup"><span data-stu-id="6496c-123">System.String</span></span>

## <span data-ttu-id="6496c-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6496c-124">OUTPUTS</span></span>

### <span data-ttu-id="6496c-125">Microsoft. Azure. Commands. profile. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="6496c-125">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="6496c-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6496c-126">NOTES</span></span>

## <span data-ttu-id="6496c-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6496c-127">RELATED LINKS</span></span>

[<span data-ttu-id="6496c-128">Dodaj-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="6496c-128">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="6496c-129">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="6496c-129">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

[<span data-ttu-id="6496c-130">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="6496c-130">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

