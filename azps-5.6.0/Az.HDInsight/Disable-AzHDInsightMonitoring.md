---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/disable-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Disable-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Disable-AzHDInsightMonitoring.md
ms.openlocfilehash: 04e4a2e45f799367060c76e30807f75eaedb0465
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968993"
---
# <span data-ttu-id="e7aa1-101">Disable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="e7aa1-101">Disable-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="e7aa1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7aa1-102">SYNOPSIS</span></span>
<span data-ttu-id="e7aa1-103">Wyłącza monitorowanie w klastrze HDInsight i odpowiednie dzienniki przestaną przepływać do obszaru roboczego monitorowania określonego podczas włączania.</span><span class="sxs-lookup"><span data-stu-id="e7aa1-103">Disables monitoring in a HDInsight cluster and relevant logs will stop flowing to the monitoring workspace specified during enable.</span></span>

## <span data-ttu-id="e7aa1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e7aa1-104">SYNTAX</span></span>

```
Disable-AzHDInsightMonitoring [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7aa1-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e7aa1-105">DESCRIPTION</span></span>
<span data-ttu-id="e7aa1-106">Polecenie **cmdlet Disable-AzHDInsightMonitoring** wyłącza monitorowanie w klastrze usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e7aa1-106">The **Disable-AzHDInsightMonitoring** cmdlet disables monitoring in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="e7aa1-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e7aa1-107">EXAMPLES</span></span>

### <span data-ttu-id="e7aa1-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e7aa1-108">Example 1</span></span>
```
PS C:\> Disable-AzHDInsightMonitoring -Name testcluster

True
```

<span data-ttu-id="e7aa1-109">Monitorowanie zostanie wyłączone w klastrze HDInsight, a odpowiednie dzienniki przestaną trafiać do obszaru roboczego monitorowania.</span><span class="sxs-lookup"><span data-stu-id="e7aa1-109">Monitoring will be disabled on the HDInsight cluster and relevant logs will stop flowing to the monitoring workspace.</span></span>

### <span data-ttu-id="e7aa1-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e7aa1-110">Example 2</span></span>
```
PS C:\> Disable-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

True
```

<span data-ttu-id="e7aa1-111">Monitorowanie zostanie wyłączone w klastrze HDInsight, a odpowiednie dzienniki przestaną trafiać do obszaru roboczego monitorowania.</span><span class="sxs-lookup"><span data-stu-id="e7aa1-111">Monitoring will be disabled on the HDInsight cluster and relevant logs will stop flowing to the monitoring workspace.</span></span>

## <span data-ttu-id="e7aa1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e7aa1-112">PARAMETERS</span></span>

### <span data-ttu-id="e7aa1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7aa1-113">-DefaultProfile</span></span>
<span data-ttu-id="e7aa1-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="e7aa1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e7aa1-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e7aa1-115">-Name</span></span>
<span data-ttu-id="e7aa1-116">Nazwa klastra, który ma być wyłączany podczas monitorowania.</span><span class="sxs-lookup"><span data-stu-id="e7aa1-116">The name of the cluster to disable Monitoring.</span></span>

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

### <span data-ttu-id="e7aa1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7aa1-117">-ResourceGroupName</span></span>
<span data-ttu-id="e7aa1-118">Grupa zasobów klastru.</span><span class="sxs-lookup"><span data-stu-id="e7aa1-118">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="e7aa1-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e7aa1-119">-Confirm</span></span>
<span data-ttu-id="e7aa1-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e7aa1-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7aa1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7aa1-121">-WhatIf</span></span>
<span data-ttu-id="e7aa1-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7aa1-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e7aa1-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e7aa1-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7aa1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7aa1-124">CommonParameters</span></span>
<span data-ttu-id="e7aa1-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7aa1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7aa1-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e7aa1-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7aa1-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e7aa1-127">INPUTS</span></span>

### <span data-ttu-id="e7aa1-128">System.String</span><span class="sxs-lookup"><span data-stu-id="e7aa1-128">System.String</span></span>

## <span data-ttu-id="e7aa1-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e7aa1-129">OUTPUTS</span></span>

### <span data-ttu-id="e7aa1-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e7aa1-130">System.Boolean</span></span>

## <span data-ttu-id="e7aa1-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e7aa1-131">NOTES</span></span>

## <span data-ttu-id="e7aa1-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e7aa1-132">RELATED LINKS</span></span>
