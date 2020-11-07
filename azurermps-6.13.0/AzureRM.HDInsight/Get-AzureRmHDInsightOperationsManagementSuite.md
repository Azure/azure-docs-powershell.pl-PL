---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightoperationsmanagementsuite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightOperationsManagementSuite.md
ms.openlocfilehash: 5fbc34f3a5a2a7b87c0e7319c5d6243e1207dc61
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717078"
---
# <span data-ttu-id="a0b29-101">Get-AzureRmHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="a0b29-101">Get-AzureRmHDInsightOperationsManagementSuite</span></span>

## <span data-ttu-id="a0b29-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a0b29-102">SYNOPSIS</span></span>
<span data-ttu-id="a0b29-103">Pobiera stan instalacji usługi Operations Management Suite (OMS) w klastrze.</span><span class="sxs-lookup"><span data-stu-id="a0b29-103">Gets the status of Operations Management Suite (OMS) installation on the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0b29-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a0b29-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightOperationsManagementSuite [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0b29-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a0b29-105">DESCRIPTION</span></span>
<span data-ttu-id="a0b29-106">Polecenie cmdlet **Get-AzureRmHDInsightOperationsManagementSuite** Pobiera stan instalacji OMS w klastrze usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="a0b29-106">The **Get-AzureRmHDInsightOperationsManagementSuite** cmdlet gets the status of OMS installation in an Azure HDInsight cluster.</span></span> <span data-ttu-id="a0b29-107">Jeśli funkcja OMS jest włączona, zostanie również zwrócony identyfikator obszaru roboczego OMS.</span><span class="sxs-lookup"><span data-stu-id="a0b29-107">If OMS is enabled then it will also return the OMS workspace id.</span></span>

## <span data-ttu-id="a0b29-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a0b29-108">EXAMPLES</span></span>

### <span data-ttu-id="a0b29-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a0b29-109">Example 1</span></span>
```
PS C:\> Get-AzureRmHDInsightOMS -Name testcluster

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="a0b29-110">Pakiet Operations Management Suite (OMS) jest włączony w klastrze, ponieważ właściwość ClusterMonitoringEnabled ma wartość PRAWDA.</span><span class="sxs-lookup"><span data-stu-id="a0b29-110">Operations Management Suite (OMS) is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="a0b29-111">Identyfikator obszaru roboczego OMS, w którym są nalewane dzienniki, to 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="a0b29-111">The OMS workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="a0b29-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a0b29-112">Example 2</span></span>
```
PS C:\> Get-AzureRmHDInsightOMS -Name testcluster -ResourceGroupName testrg

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="a0b29-113">Pakiet Operations Management Suite (OMS) jest włączony w klastrze, ponieważ właściwość ClusterMonitoringEnabled ma wartość PRAWDA.</span><span class="sxs-lookup"><span data-stu-id="a0b29-113">Operations Management Suite (OMS) is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="a0b29-114">Identyfikator obszaru roboczego OMS, w którym są nalewane dzienniki, to 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="a0b29-114">The OMS workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="a0b29-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="a0b29-115">Example 3</span></span>
```
PS C:\> Get-AzureRmHDInsightOMS -Name testcluster

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'false'}
```

<span data-ttu-id="a0b29-116">Pakiet Operations Management Suite (OMS) jest wyłączony w klastrze, ponieważ właściwość ClusterMonitoringEnabled ma wartość false.</span><span class="sxs-lookup"><span data-stu-id="a0b29-116">Operations Management Suite (OMS) is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

### <span data-ttu-id="a0b29-117">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="a0b29-117">Example 4</span></span>
```
PS C:\> Get-AzureRmHDInsightOMS -Name testcluster -ResourceGroupName testrg

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'false'}
```

<span data-ttu-id="a0b29-118">Pakiet Operations Management Suite (OMS) jest wyłączony w klastrze, ponieważ właściwość ClusterMonitoringEnabled ma wartość false.</span><span class="sxs-lookup"><span data-stu-id="a0b29-118">Operations Management Suite (OMS) is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

## <span data-ttu-id="a0b29-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a0b29-119">PARAMETERS</span></span>

### <span data-ttu-id="a0b29-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0b29-120">-DefaultProfile</span></span>
<span data-ttu-id="a0b29-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a0b29-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0b29-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a0b29-122">-Name</span></span>
<span data-ttu-id="a0b29-123">Nazwa klastra, aby uzyskać stan pakietu Operations Management Suite (OMS).</span><span class="sxs-lookup"><span data-stu-id="a0b29-123">The name of the cluster to get the status of Operations Management Suite(OMS).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0b29-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0b29-124">-ResourceGroupName</span></span>
<span data-ttu-id="a0b29-125">Grupa zasobów klastra.</span><span class="sxs-lookup"><span data-stu-id="a0b29-125">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="a0b29-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0b29-126">CommonParameters</span></span>
<span data-ttu-id="a0b29-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0b29-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0b29-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0b29-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0b29-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a0b29-129">INPUTS</span></span>

### <span data-ttu-id="a0b29-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a0b29-130">System.String</span></span>

## <span data-ttu-id="a0b29-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a0b29-131">OUTPUTS</span></span>

### <span data-ttu-id="a0b29-132">Microsoft. Azure. Commands. HDInsight. models. Management. AzureHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="a0b29-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightOMS</span></span>

## <span data-ttu-id="a0b29-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a0b29-133">NOTES</span></span>

## <span data-ttu-id="a0b29-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a0b29-134">RELATED LINKS</span></span>