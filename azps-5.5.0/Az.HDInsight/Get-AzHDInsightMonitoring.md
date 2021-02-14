---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightMonitoring.md
ms.openlocfilehash: 2d91c96d20797988a7def2d11d633f36b08cb8cb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100237760"
---
# <span data-ttu-id="a685f-101">Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="a685f-101">Get-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="a685f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a685f-102">SYNOPSIS</span></span>
<span data-ttu-id="a685f-103">Pobiera stan instalacji monitorowania w klastrze.</span><span class="sxs-lookup"><span data-stu-id="a685f-103">Gets the status of monitoring installation on the cluster.</span></span>

## <span data-ttu-id="a685f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a685f-104">SYNTAX</span></span>

```
Get-AzHDInsightMonitoring [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a685f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a685f-105">DESCRIPTION</span></span>
<span data-ttu-id="a685f-106">Polecenie **cmdlet Get-AzHDInsightMonitoring** otrzymuje stan instalacji monitorowania w klastrze usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="a685f-106">The **Get-AzHDInsightMonitoring** cmdlet gets the status of monitoring installation in an Azure HDInsight cluster.</span></span> <span data-ttu-id="a685f-107">Jeśli monitorowanie jest włączone, zwracany jest również identyfikator obszaru roboczego analizy dziennika.</span><span class="sxs-lookup"><span data-stu-id="a685f-107">If monitoring is enabled then it will also return the log analytics workspace id.</span></span>

## <span data-ttu-id="a685f-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a685f-108">EXAMPLES</span></span>

### <span data-ttu-id="a685f-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a685f-109">Example 1</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="a685f-110">Monitorowanie jest włączone w klastrze, ponieważ właściwość ClusterMonitoringEnabled jest prawdziwa.</span><span class="sxs-lookup"><span data-stu-id="a685f-110">Monitoring is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="a685f-111">Identyfikator obszaru roboczego monitorowania, w którym przepływają dzienniki, to 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="a685f-111">The monitoring workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="a685f-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a685f-112">Example 2</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="a685f-113">Monitorowanie jest włączone w klastrze, ponieważ właściwość ClusterMonitoringEnabled jest prawdziwa.</span><span class="sxs-lookup"><span data-stu-id="a685f-113">Monitoring is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="a685f-114">Identyfikator obszaru roboczego monitorowania, w którym przepływają dzienniki, to 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="a685f-114">The monitoring workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="a685f-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="a685f-115">Example 3</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster

{'ClusterMonitoringEnabled':'false', 'workspaceId': null}
```

<span data-ttu-id="a685f-116">Monitorowanie jest wyłączone w klastrze, ponieważ właściwość ClusterMonitoringEnabled ma wartość fałszywą.</span><span class="sxs-lookup"><span data-stu-id="a685f-116">Monitoring is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

### <span data-ttu-id="a685f-117">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="a685f-117">Example 4</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

{'ClusterMonitoringEnabled':'false', 'workspaceId': null}
```

<span data-ttu-id="a685f-118">Monitorowanie jest wyłączone w klastrze, ponieważ właściwość ClusterMonitoringEnabled ma wartość fałszywą.</span><span class="sxs-lookup"><span data-stu-id="a685f-118">Monitoring is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

## <span data-ttu-id="a685f-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a685f-119">PARAMETERS</span></span>

### <span data-ttu-id="a685f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a685f-120">-DefaultProfile</span></span>
<span data-ttu-id="a685f-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="a685f-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a685f-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a685f-122">-Name</span></span>
<span data-ttu-id="a685f-123">Nazwa klastra, który ma być w stanie monitorowania.</span><span class="sxs-lookup"><span data-stu-id="a685f-123">The name of the cluster to get the status of monitoring.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a685f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a685f-124">-ResourceGroupName</span></span>
<span data-ttu-id="a685f-125">Grupa zasobów klastrów.</span><span class="sxs-lookup"><span data-stu-id="a685f-125">The resource group of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a685f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a685f-126">CommonParameters</span></span>
<span data-ttu-id="a685f-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a685f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a685f-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a685f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a685f-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a685f-129">INPUTS</span></span>

### <span data-ttu-id="a685f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="a685f-130">System.String</span></span>

## <span data-ttu-id="a685f-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a685f-131">OUTPUTS</span></span>

### <span data-ttu-id="a685f-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="a685f-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightMonitoring</span></span>

## <span data-ttu-id="a685f-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a685f-133">NOTES</span></span>

## <span data-ttu-id="a685f-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a685f-134">RELATED LINKS</span></span>
