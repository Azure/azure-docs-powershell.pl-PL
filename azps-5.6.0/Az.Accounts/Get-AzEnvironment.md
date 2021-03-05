---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/get-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzEnvironment.md
ms.openlocfilehash: b3bccc5d538c8ce5e3a79b621b48d75556ed0189
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981338"
---
# <span data-ttu-id="e0e9b-101">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="e0e9b-101">Get-AzEnvironment</span></span>

## <span data-ttu-id="e0e9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0e9b-102">SYNOPSIS</span></span>
<span data-ttu-id="e0e9b-103">Uzyskaj punkty końcowe i metadane dla wystąpienia usług platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e0e9b-103">Get endpoints and metadata for an instance of Azure services.</span></span>

## <span data-ttu-id="e0e9b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e0e9b-104">SYNTAX</span></span>

```
Get-AzEnvironment [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0e9b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e0e9b-105">DESCRIPTION</span></span>
<span data-ttu-id="e0e9b-106">Polecenie Get-AzEnvironment pobiera punkty końcowe i metadane dla wystąpienia usług Azure.</span><span class="sxs-lookup"><span data-stu-id="e0e9b-106">The Get-AzEnvironment cmdlet gets endpoints and metadata for an instance of Azure services.</span></span>

## <span data-ttu-id="e0e9b-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e0e9b-107">EXAMPLES</span></span>

### <span data-ttu-id="e0e9b-108">Przykład 1. Uzyskiwanie środowiska usługi AzureCloud</span><span class="sxs-lookup"><span data-stu-id="e0e9b-108">Example 1: Getting the AzureCloud environment</span></span>
```
PS C:\> Get-AzEnvironment AzureCloud

Name       Resource Manager Url          ActiveDirectory Authority
----       --------------------          -------------------------
AzureCloud https://management.azure.com/ https://login.microsoftonline.com/
```

<span data-ttu-id="e0e9b-109">W tym przykładzie pokazano, jak uzyskać punkty końcowe i metadane dla środowiska usługi AzureCloud (domyślnego).</span><span class="sxs-lookup"><span data-stu-id="e0e9b-109">This example shows how to get the endpoints and metadata for the AzureCloud (default) environment.</span></span>

### <span data-ttu-id="e0e9b-110">Przykład 2. Uzyskiwanie środowiska AzureChinaCloud</span><span class="sxs-lookup"><span data-stu-id="e0e9b-110">Example 2: Getting the AzureChinaCloud environment</span></span>
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

<span data-ttu-id="e0e9b-111">W tym przykładzie pokazano, jak uzyskać punkty końcowe i metadane dla środowiska usługi AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="e0e9b-111">This example shows how to get the endpoints and metadata for the AzureChinaCloud environment.</span></span>

### <span data-ttu-id="e0e9b-112">Przykład 3. Uzyskiwanie środowiska AzureUSGovernment</span><span class="sxs-lookup"><span data-stu-id="e0e9b-112">Example 3: Getting the AzureUSGovernment environment</span></span>
```
PS C:\> Get-AzEnvironment AzureUSGovernment

Name              Resource Manager Url                  ActiveDirectory Authority
----              --------------------                  -------------------------
AzureUSGovernment https://management.usgovcloudapi.net/ https://login.microsoftonline.us/
```

<span data-ttu-id="e0e9b-113">W tym przykładzie pokazano, jak uzyskać punkty końcowe i metadane dla środowiska AzureUSGovernment.</span><span class="sxs-lookup"><span data-stu-id="e0e9b-113">This example shows how to get the endpoints and metadata for the AzureUSGovernment environment.</span></span>

## <span data-ttu-id="e0e9b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0e9b-114">PARAMETERS</span></span>

### <span data-ttu-id="e0e9b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0e9b-115">-DefaultProfile</span></span>
<span data-ttu-id="e0e9b-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e0e9b-116">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0e9b-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e0e9b-117">-Name</span></span>
<span data-ttu-id="e0e9b-118">Określa nazwę wystąpienia platformy Azure do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="e0e9b-118">Specifies the name of the Azure instance to get.</span></span>

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

### <span data-ttu-id="e0e9b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0e9b-119">CommonParameters</span></span>
<span data-ttu-id="e0e9b-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0e9b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0e9b-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0e9b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0e9b-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e0e9b-122">INPUTS</span></span>

### <span data-ttu-id="e0e9b-123">System.String</span><span class="sxs-lookup"><span data-stu-id="e0e9b-123">System.String</span></span>

## <span data-ttu-id="e0e9b-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e0e9b-124">OUTPUTS</span></span>

### <span data-ttu-id="e0e9b-125">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="e0e9b-125">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="e0e9b-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e0e9b-126">NOTES</span></span>

## <span data-ttu-id="e0e9b-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e0e9b-127">RELATED LINKS</span></span>

[<span data-ttu-id="e0e9b-128">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="e0e9b-128">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="e0e9b-129">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="e0e9b-129">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

[<span data-ttu-id="e0e9b-130">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="e0e9b-130">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

