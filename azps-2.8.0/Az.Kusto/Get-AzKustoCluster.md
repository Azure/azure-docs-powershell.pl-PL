---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoCluster.md
ms.openlocfilehash: c5c7cdffc8b329fdff426f48f60869ca6821f32d
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401355"
---
# <span data-ttu-id="6fb65-101">Get-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="6fb65-101">Get-AzKustoCluster</span></span>

## <span data-ttu-id="6fb65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fb65-102">SYNOPSIS</span></span>
<span data-ttu-id="6fb65-103">Lista wszystkich klastrów Kusto w grupie zasobów lub uzyskiwanie określonego klastra Kusto.</span><span class="sxs-lookup"><span data-stu-id="6fb65-103">List all Kusto clusters in a resource group or get a specific Kusto cluster.</span></span>

## <span data-ttu-id="6fb65-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6fb65-104">SYNTAX</span></span>

### <span data-ttu-id="6fb65-105">ByClusterOrResourceGroupOrSubscription (Default)</span><span class="sxs-lookup"><span data-stu-id="6fb65-105">ByClusterOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzKustoCluster -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6fb65-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6fb65-106">ByResourceId</span></span>
```
Get-AzKustoCluster -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6fb65-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="6fb65-107">DESCRIPTION</span></span>
<span data-ttu-id="6fb65-108">Lista wszystkich klastrów Kusto w grupie zasobów lub uzyskiwanie określonego klastra Kusto.</span><span class="sxs-lookup"><span data-stu-id="6fb65-108">List all Kusto clusters in a resource group or get a specific Kusto cluster.</span></span>

## <span data-ttu-id="6fb65-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6fb65-109">EXAMPLES</span></span>

### <span data-ttu-id="6fb65-110">Przykład 1. Lista wszystkich klastrów Kusto w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="6fb65-110">Example 1 - List all Kusto clusters in a resource group</span></span>

<span data-ttu-id="6fb65-111">Typ: Microsoft.Kusto/Clusters Id: /subscriptions/xxxxxxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster1 ResourceGroup : testrg Name : mykustocluster1 Location: Central US Capacity : 3 SKU: D13_v2 ProvisioningState: Succeeded State: Running Tag: {} Uri: `https://mykustocluster1.centralus.kusto.windows.net` DataIngestionUri: `https://ingest-mykustocluster1.centralus.kusto.windows.net`</span><span class="sxs-lookup"><span data-stu-id="6fb65-111">Type              : Microsoft.Kusto/Clusters Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster1 ResourceGroup     : testrg Name              : mykustocluster1 Location          : Central US Capacity          : 3 Sku               : D13_v2 ProvisioningState : Succeeded State             : Running Tag               : {} Uri               : `https://mykustocluster1.centralus.kusto.windows.net` DataIngestionUri  : `https://ingest-mykustocluster1.centralus.kusto.windows.net`</span></span>

<span data-ttu-id="6fb65-112">Typ: Microsoft.Kusto/Clusters Id: /subscriptions/xxxxxxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster2 ResourceGroup : testrg Name: mykustocluster2 Location: Central US Capacity : 5 SKU : D13_v2 ProvisioningState: Succeeded State: Running Tag: {} Uri: `https://mykustocluster2.centralus.kusto.windows.net` DataIngestionUri: `https://ingest-mykustocluster2.centralus.kusto.windows.net`</span><span class="sxs-lookup"><span data-stu-id="6fb65-112">Type              : Microsoft.Kusto/Clusters Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster2 ResourceGroup     : testrg Name              : mykustocluster2 Location          : Central US Capacity          : 5 Sku               : D13_v2 ProvisioningState : Succeeded State             : Running Tag               : {} Uri               : `https://mykustocluster2.centralus.kusto.windows.net` DataIngestionUri  : `https://ingest-mykustocluster2.centralus.kusto.windows.net`</span></span>


```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg
```

<span data-ttu-id="6fb65-113">Powyższe polecenie wyświetla listę wszystkich klastrów Kusto w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="6fb65-113">The above command lists all Kusto clusters in the resource group "testrg".</span></span>

### <span data-ttu-id="6fb65-114">Przykład 2. Uzyskiwanie określonego klastru Kusto według nazwy</span><span class="sxs-lookup"><span data-stu-id="6fb65-114">Example 2 - Get a specific Kusto cluster by name</span></span>

```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster

Type              : Microsoft.Kusto/Clusters
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster
ResourceGroup     : testrg
Name              : mykustocluster
Location          : Central US
Capacity          : 5
Sku               : D13_v2
ProvisioningState : Succeeded
State             : Running
Tag               : {}
Uri               : https://mykustocluster.centralus.kusto.windows.net
DataIngestionUri  : https://ingest-mykustocluster.centralus.kusto.windows.net
```

<span data-ttu-id="6fb65-115">Powyższe polecenie zwraca klaster Kusto o nazwie "mykustocluster" w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="6fb65-115">The above command returns the Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

### <span data-ttu-id="6fb65-116">Przykład 3. Uzyskiwanie określonego klastru Kusto według identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="6fb65-116">Example 3 - Get a specific Kusto cluster by resource id</span></span>

```
PS C:\> Get-AzKustoCluster -ResourceId /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/clusters/mykustocluster
Type              : Microsoft.Kusto/Clusters
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster
ResourceGroup     : testrg
Name              : mykustocluster
Location          : Central US
Capacity          : 5
Sku               : D13_v2
ProvisioningState : Succeeded
State             : Running
Tag               : {}
Uri               : https://mykustocluster.centralus.kusto.windows.net
DataIngestionUri  : https://ingest-mykustocluster.centralus.kusto.windows.net
```

<span data-ttu-id="6fb65-117">Powyższe polecenie zwraca klaster Kusto o nazwie "mykustocluster" w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="6fb65-117">The above command returns the Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="6fb65-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6fb65-118">PARAMETERS</span></span>

### <span data-ttu-id="6fb65-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fb65-119">-DefaultProfile</span></span>
<span data-ttu-id="6fb65-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6fb65-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fb65-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6fb65-121">-Name</span></span>
<span data-ttu-id="6fb65-122">Nazwa określonego klastra.</span><span class="sxs-lookup"><span data-stu-id="6fb65-122">Name of a specific cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByClusterOrResourceGroupOrSubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fb65-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fb65-123">-ResourceGroupName</span></span>
<span data-ttu-id="6fb65-124">Nazwa grupy zasobów, w ramach której użytkownik chce pobrać klaster.</span><span class="sxs-lookup"><span data-stu-id="6fb65-124">Name of resource group under which the user wants to retrieve the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByClusterOrResourceGroupOrSubscription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fb65-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6fb65-125">-ResourceId</span></span>
<span data-ttu-id="6fb65-126">Kusto cluster ResourceID.</span><span class="sxs-lookup"><span data-stu-id="6fb65-126">Kusto cluster ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fb65-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fb65-127">CommonParameters</span></span>
<span data-ttu-id="6fb65-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fb65-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fb65-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fb65-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fb65-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6fb65-130">INPUTS</span></span>

### <span data-ttu-id="6fb65-131">System.String</span><span class="sxs-lookup"><span data-stu-id="6fb65-131">System.String</span></span>

## <span data-ttu-id="6fb65-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6fb65-132">OUTPUTS</span></span>

### <span data-ttu-id="6fb65-133">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="6fb65-133">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="6fb65-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6fb65-134">NOTES</span></span>

## <span data-ttu-id="6fb65-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6fb65-135">RELATED LINKS</span></span>
