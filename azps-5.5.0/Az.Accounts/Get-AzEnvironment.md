---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzEnvironment.md
ms.openlocfilehash: 176874b9d3fbf192597cd98659e45df800dc819c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190483"
---
# <span data-ttu-id="c6c48-101">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="c6c48-101">Get-AzEnvironment</span></span>

## <span data-ttu-id="c6c48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6c48-102">SYNOPSIS</span></span>
<span data-ttu-id="c6c48-103">Uzyskaj punkty końcowe i metadane dla wystąpienia usług Platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c6c48-103">Get endpoints and metadata for an instance of Azure services.</span></span>

## <span data-ttu-id="c6c48-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c6c48-104">SYNTAX</span></span>

```
Get-AzEnvironment [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6c48-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="c6c48-105">DESCRIPTION</span></span>
<span data-ttu-id="c6c48-106">Polecenie Get-AzEnvironment pobiera punkty końcowe i metadane dla wystąpienia usług Azure.</span><span class="sxs-lookup"><span data-stu-id="c6c48-106">The Get-AzEnvironment cmdlet gets endpoints and metadata for an instance of Azure services.</span></span>

## <span data-ttu-id="c6c48-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c6c48-107">EXAMPLES</span></span>

### <span data-ttu-id="c6c48-108">Przykład 1. Uzyskiwanie środowiska usługi AzureCloud</span><span class="sxs-lookup"><span data-stu-id="c6c48-108">Example 1: Getting the AzureCloud environment</span></span>
```
PS C:\> Get-AzEnvironment AzureCloud

Name       Resource Manager Url          ActiveDirectory Authority
----       --------------------          -------------------------
AzureCloud https://management.azure.com/ https://login.microsoftonline.com/
```

<span data-ttu-id="c6c48-109">W tym przykładzie pokazano, jak uzyskać punkty końcowe i metadane dla środowiska usługi AzureCloud (domyślnego).</span><span class="sxs-lookup"><span data-stu-id="c6c48-109">This example shows how to get the endpoints and metadata for the AzureCloud (default) environment.</span></span>

### <span data-ttu-id="c6c48-110">Przykład 2. Uzyskiwanie środowiska AzureChinaCloud</span><span class="sxs-lookup"><span data-stu-id="c6c48-110">Example 2: Getting the AzureChinaCloud environment</span></span>
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

<span data-ttu-id="c6c48-111">W tym przykładzie pokazano, jak uzyskać punkty końcowe i metadane dla środowiska usługi AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="c6c48-111">This example shows how to get the endpoints and metadata for the AzureChinaCloud environment.</span></span>

### <span data-ttu-id="c6c48-112">Przykład 3. Uzyskiwanie środowiska AzureUSGovernment</span><span class="sxs-lookup"><span data-stu-id="c6c48-112">Example 3: Getting the AzureUSGovernment environment</span></span>
```
PS C:\> Get-AzEnvironment AzureUSGovernment

Name              Resource Manager Url                  ActiveDirectory Authority
----              --------------------                  -------------------------
AzureUSGovernment https://management.usgovcloudapi.net/ https://login.microsoftonline.us/
```

<span data-ttu-id="c6c48-113">W tym przykładzie pokazano, jak uzyskać punkty końcowe i metadane dla środowiska AzureUSGovernment.</span><span class="sxs-lookup"><span data-stu-id="c6c48-113">This example shows how to get the endpoints and metadata for the AzureUSGovernment environment.</span></span>

## <span data-ttu-id="c6c48-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c6c48-114">PARAMETERS</span></span>

### <span data-ttu-id="c6c48-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6c48-115">-DefaultProfile</span></span>
<span data-ttu-id="c6c48-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c6c48-116">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6c48-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c6c48-117">-Name</span></span>
<span data-ttu-id="c6c48-118">Określa nazwę wystąpienia platformy Azure do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="c6c48-118">Specifies the name of the Azure instance to get.</span></span>

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

### <span data-ttu-id="c6c48-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6c48-119">CommonParameters</span></span>
<span data-ttu-id="c6c48-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6c48-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6c48-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6c48-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6c48-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c6c48-122">INPUTS</span></span>

### <span data-ttu-id="c6c48-123">System.String</span><span class="sxs-lookup"><span data-stu-id="c6c48-123">System.String</span></span>

## <span data-ttu-id="c6c48-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c6c48-124">OUTPUTS</span></span>

### <span data-ttu-id="c6c48-125">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="c6c48-125">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="c6c48-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c6c48-126">NOTES</span></span>

## <span data-ttu-id="c6c48-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c6c48-127">RELATED LINKS</span></span>

[<span data-ttu-id="c6c48-128">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="c6c48-128">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="c6c48-129">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="c6c48-129">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

[<span data-ttu-id="c6c48-130">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="c6c48-130">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

