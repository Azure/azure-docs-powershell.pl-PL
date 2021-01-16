---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightMonitoring.md
ms.openlocfilehash: 2d91c96d20797988a7def2d11d633f36b08cb8cb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338233"
---
# <span data-ttu-id="b6951-101">Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="b6951-101">Get-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="b6951-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b6951-102">SYNOPSIS</span></span>
<span data-ttu-id="b6951-103">Pobiera stan instalacji monitorowania w klastrze.</span><span class="sxs-lookup"><span data-stu-id="b6951-103">Gets the status of monitoring installation on the cluster.</span></span>

## <span data-ttu-id="b6951-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b6951-104">SYNTAX</span></span>

```
Get-AzHDInsightMonitoring [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6951-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b6951-105">DESCRIPTION</span></span>
<span data-ttu-id="b6951-106">Polecenie cmdlet **Get-AzHDInsightMonitoring** Pobiera stan instalacji monitorowania w klastrze usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="b6951-106">The **Get-AzHDInsightMonitoring** cmdlet gets the status of monitoring installation in an Azure HDInsight cluster.</span></span> <span data-ttu-id="b6951-107">Jeśli monitorowanie jest włączone, zostanie również zwrócony identyfikator obszaru roboczego Analiza dzienników.</span><span class="sxs-lookup"><span data-stu-id="b6951-107">If monitoring is enabled then it will also return the log analytics workspace id.</span></span>

## <span data-ttu-id="b6951-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b6951-108">EXAMPLES</span></span>

### <span data-ttu-id="b6951-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b6951-109">Example 1</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="b6951-110">Monitorowanie jest włączone w klastrze, ponieważ właściwość ClusterMonitoringEnabled ma wartość PRAWDA.</span><span class="sxs-lookup"><span data-stu-id="b6951-110">Monitoring is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="b6951-111">Identyfikator obszaru roboczego monitorowania, w którym są nalewane dzienniki, to 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="b6951-111">The monitoring workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="b6951-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b6951-112">Example 2</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="b6951-113">Monitorowanie jest włączone w klastrze, ponieważ właściwość ClusterMonitoringEnabled ma wartość PRAWDA.</span><span class="sxs-lookup"><span data-stu-id="b6951-113">Monitoring is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="b6951-114">Identyfikator obszaru roboczego monitorowania, w którym są nalewane dzienniki, to 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="b6951-114">The monitoring workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="b6951-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="b6951-115">Example 3</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster

{'ClusterMonitoringEnabled':'false', 'workspaceId': null}
```

<span data-ttu-id="b6951-116">Monitorowanie jest wyłączone w klastrze, ponieważ właściwość ClusterMonitoringEnabled ma wartość false.</span><span class="sxs-lookup"><span data-stu-id="b6951-116">Monitoring is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

### <span data-ttu-id="b6951-117">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="b6951-117">Example 4</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

{'ClusterMonitoringEnabled':'false', 'workspaceId': null}
```

<span data-ttu-id="b6951-118">Monitorowanie jest wyłączone w klastrze, ponieważ właściwość ClusterMonitoringEnabled ma wartość false.</span><span class="sxs-lookup"><span data-stu-id="b6951-118">Monitoring is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

## <span data-ttu-id="b6951-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b6951-119">PARAMETERS</span></span>

### <span data-ttu-id="b6951-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6951-120">-DefaultProfile</span></span>
<span data-ttu-id="b6951-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b6951-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b6951-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b6951-122">-Name</span></span>
<span data-ttu-id="b6951-123">Nazwa klastra, aby uzyskać stan monitorowania.</span><span class="sxs-lookup"><span data-stu-id="b6951-123">The name of the cluster to get the status of monitoring.</span></span>

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

### <span data-ttu-id="b6951-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6951-124">-ResourceGroupName</span></span>
<span data-ttu-id="b6951-125">Grupa zasobów klastra.</span><span class="sxs-lookup"><span data-stu-id="b6951-125">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="b6951-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6951-126">CommonParameters</span></span>
<span data-ttu-id="b6951-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6951-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6951-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b6951-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6951-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b6951-129">INPUTS</span></span>

### <span data-ttu-id="b6951-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b6951-130">System.String</span></span>

## <span data-ttu-id="b6951-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b6951-131">OUTPUTS</span></span>

### <span data-ttu-id="b6951-132">Microsoft. Azure. Commands. HDInsight. models. Management. AzureHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="b6951-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightMonitoring</span></span>

## <span data-ttu-id="b6951-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b6951-133">NOTES</span></span>

## <span data-ttu-id="b6951-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b6951-134">RELATED LINKS</span></span>
