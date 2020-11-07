---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoCluster.md
ms.openlocfilehash: a68604e9701a6ae2c251edf3f2a0935df5ffa94f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705076"
---
# <span data-ttu-id="dbe8f-101">Get-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="dbe8f-101">Get-AzKustoCluster</span></span>

## <span data-ttu-id="dbe8f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dbe8f-102">SYNOPSIS</span></span>
<span data-ttu-id="dbe8f-103">Wyświetlanie wszystkich klastrów Kusto w grupie zasobów lub uzyskiwanie określonego klastra Kusto.</span><span class="sxs-lookup"><span data-stu-id="dbe8f-103">List all Kusto clusters in a resource group or get a specific Kusto cluster.</span></span>

## <span data-ttu-id="dbe8f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dbe8f-104">SYNTAX</span></span>

### <span data-ttu-id="dbe8f-105">ByClusterOrResourceGroupOrSubscription (domyślny)</span><span class="sxs-lookup"><span data-stu-id="dbe8f-105">ByClusterOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzKustoCluster -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dbe8f-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="dbe8f-106">ByResourceId</span></span>
```
Get-AzKustoCluster -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dbe8f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="dbe8f-107">DESCRIPTION</span></span>
<span data-ttu-id="dbe8f-108">Wyświetlanie wszystkich klastrów Kusto w grupie zasobów lub uzyskiwanie określonego klastra Kusto.</span><span class="sxs-lookup"><span data-stu-id="dbe8f-108">List all Kusto clusters in a resource group or get a specific Kusto cluster.</span></span>

## <span data-ttu-id="dbe8f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dbe8f-109">EXAMPLES</span></span>

### <span data-ttu-id="dbe8f-110">Przykład 1-Wyświetlanie wszystkich klastrów Kusto w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="dbe8f-110">Example 1 - List all Kusto clusters in a resource group</span></span>

<span data-ttu-id="dbe8f-111">Typ: Microsoft. Kusto/klastry ID:/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster1 resourceName: testrg Name: mykustocluster1 lokalizacja: Centralna pojemność w Stanach Zjednoczonych: 3 SKU: D13_v2 ProvisioningState: powodzenie, stan: uruchomiony Tag: {} Identyfikator URI: https://mykustocluster1.centralus.kusto.windows.net DataIngestionUri: https://ingest-mykustocluster1.centralus.kusto.windows.net</span><span class="sxs-lookup"><span data-stu-id="dbe8f-111">Type              : Microsoft.Kusto/Clusters Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster1 ResourceGroup     : testrg Name              : mykustocluster1 Location          : Central US Capacity          : 3 Sku               : D13_v2 ProvisioningState : Succeeded State             : Running Tag               : {} Uri               : https://mykustocluster1.centralus.kusto.windows.net DataIngestionUri  : https://ingest-mykustocluster1.centralus.kusto.windows.net</span></span>

<span data-ttu-id="dbe8f-112">Type: Microsoft. Kusto/klastrów ID:/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster2 resourceName: testrg Nazwa: mykustocluster2 lokalizacja: Centralna pojemność w Stanach Zjednoczonych: 5 SKU: D13_v2 ProvisioningState: stan zakończony pomyślnie: uruchomiony Tag: {} Identyfikator URI: https://mykustocluster2.centralus.kusto.windows.net DataIngestionUri: https://ingest-mykustocluster2.centralus.kusto.windows.net</span><span class="sxs-lookup"><span data-stu-id="dbe8f-112">Type              : Microsoft.Kusto/Clusters Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster2 ResourceGroup     : testrg Name              : mykustocluster2 Location          : Central US Capacity          : 5 Sku               : D13_v2 ProvisioningState : Succeeded State             : Running Tag               : {} Uri               : https://mykustocluster2.centralus.kusto.windows.net DataIngestionUri  : https://ingest-mykustocluster2.centralus.kusto.windows.net</span></span>


```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg
```

<span data-ttu-id="dbe8f-113">Powyższe polecenie wyświetla listę wszystkich Kustoych klastrów w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="dbe8f-113">The above command lists all Kusto clusters in the resource group "testrg".</span></span>

### <span data-ttu-id="dbe8f-114">Przykład 2 — uzyskiwanie określonego klastra Kusto według nazwy</span><span class="sxs-lookup"><span data-stu-id="dbe8f-114">Example 2 - Get a specific Kusto cluster by name</span></span>

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

<span data-ttu-id="dbe8f-115">Powyższe polecenie zwraca klaster Kusto o nazwie "mykustocluster" w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="dbe8f-115">The above command returns the Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

### <span data-ttu-id="dbe8f-116">Przykład 3-uzyskiwanie określonego klastra Kusto według identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="dbe8f-116">Example 3 - Get a specific Kusto cluster by resource id</span></span>

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

<span data-ttu-id="dbe8f-117">Powyższe polecenie zwraca klaster Kusto o nazwie "mykustocluster" w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="dbe8f-117">The above command returns the Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="dbe8f-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dbe8f-118">PARAMETERS</span></span>

### <span data-ttu-id="dbe8f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbe8f-119">-DefaultProfile</span></span>
<span data-ttu-id="dbe8f-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dbe8f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbe8f-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dbe8f-121">-Name</span></span>
<span data-ttu-id="dbe8f-122">Nazwa określonego klastra.</span><span class="sxs-lookup"><span data-stu-id="dbe8f-122">Name of a specific cluster.</span></span>

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

### <span data-ttu-id="dbe8f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbe8f-123">-ResourceGroupName</span></span>
<span data-ttu-id="dbe8f-124">Nazwa grupy zasobów, pod którą użytkownik chce pobrać klaster.</span><span class="sxs-lookup"><span data-stu-id="dbe8f-124">Name of resource group under which the user wants to retrieve the cluster.</span></span>

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

### <span data-ttu-id="dbe8f-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dbe8f-125">-ResourceId</span></span>
<span data-ttu-id="dbe8f-126">Kusto identyfikator zasobu klastra.</span><span class="sxs-lookup"><span data-stu-id="dbe8f-126">Kusto cluster ResourceID.</span></span>

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

### <span data-ttu-id="dbe8f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbe8f-127">CommonParameters</span></span>
<span data-ttu-id="dbe8f-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbe8f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbe8f-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbe8f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbe8f-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dbe8f-130">INPUTS</span></span>

### <span data-ttu-id="dbe8f-131">System. String</span><span class="sxs-lookup"><span data-stu-id="dbe8f-131">System.String</span></span>

## <span data-ttu-id="dbe8f-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dbe8f-132">OUTPUTS</span></span>

### <span data-ttu-id="dbe8f-133">Microsoft. Azure. Commands. Kusto. models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="dbe8f-133">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="dbe8f-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dbe8f-134">NOTES</span></span>

## <span data-ttu-id="dbe8f-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dbe8f-135">RELATED LINKS</span></span>
