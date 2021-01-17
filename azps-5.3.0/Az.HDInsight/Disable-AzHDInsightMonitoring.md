---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/disable-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Disable-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Disable-AzHDInsightMonitoring.md
ms.openlocfilehash: 9a65a82808c78fe878ba4a61f8be01f37fc11771
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489633"
---
# <span data-ttu-id="18dab-101">Disable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="18dab-101">Disable-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="18dab-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="18dab-102">SYNOPSIS</span></span>
<span data-ttu-id="18dab-103">Wyłącza monitorowanie w klastrze usługi HDInsight, a odpowiednie dzienniki będą przelewane do obszaru roboczego monitorowania określonego podczas włączania.</span><span class="sxs-lookup"><span data-stu-id="18dab-103">Disables monitoring in a HDInsight cluster and relevant logs will stop flowing to the monitoring workspace specified during enable.</span></span>

## <span data-ttu-id="18dab-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="18dab-104">SYNTAX</span></span>

```
Disable-AzHDInsightMonitoring [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18dab-105">Opis</span><span class="sxs-lookup"><span data-stu-id="18dab-105">DESCRIPTION</span></span>
<span data-ttu-id="18dab-106">Polecenie cmdlet **disable-AzHDInsightMonitoring** wyłącza monitorowanie w klastrze usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="18dab-106">The **Disable-AzHDInsightMonitoring** cmdlet disables monitoring in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="18dab-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="18dab-107">EXAMPLES</span></span>

### <span data-ttu-id="18dab-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="18dab-108">Example 1</span></span>
```
PS C:\> Disable-AzHDInsightMonitoring -Name testcluster

True
```

<span data-ttu-id="18dab-109">Monitorowanie zostanie wyłączone w klastrze usługi HDInsight, a odpowiednie dzienniki przestaną przepływ na obszar roboczy monitorowania.</span><span class="sxs-lookup"><span data-stu-id="18dab-109">Monitoring will be disabled on the HDInsight cluster and relevant logs will stop flowing to the monitoring workspace.</span></span>

### <span data-ttu-id="18dab-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="18dab-110">Example 2</span></span>
```
PS C:\> Disable-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

True
```

<span data-ttu-id="18dab-111">Monitorowanie zostanie wyłączone w klastrze usługi HDInsight, a odpowiednie dzienniki przestaną przepływ na obszar roboczy monitorowania.</span><span class="sxs-lookup"><span data-stu-id="18dab-111">Monitoring will be disabled on the HDInsight cluster and relevant logs will stop flowing to the monitoring workspace.</span></span>

## <span data-ttu-id="18dab-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="18dab-112">PARAMETERS</span></span>

### <span data-ttu-id="18dab-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18dab-113">-DefaultProfile</span></span>
<span data-ttu-id="18dab-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="18dab-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="18dab-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="18dab-115">-Name</span></span>
<span data-ttu-id="18dab-116">Nazwa klastra, aby wyłączyć monitorowanie.</span><span class="sxs-lookup"><span data-stu-id="18dab-116">The name of the cluster to disable Monitoring.</span></span>

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

### <span data-ttu-id="18dab-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18dab-117">-ResourceGroupName</span></span>
<span data-ttu-id="18dab-118">Grupa zasobów klastra.</span><span class="sxs-lookup"><span data-stu-id="18dab-118">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="18dab-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="18dab-119">-Confirm</span></span>
<span data-ttu-id="18dab-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18dab-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18dab-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18dab-121">-WhatIf</span></span>
<span data-ttu-id="18dab-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18dab-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="18dab-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="18dab-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18dab-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18dab-124">CommonParameters</span></span>
<span data-ttu-id="18dab-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18dab-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18dab-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="18dab-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18dab-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="18dab-127">INPUTS</span></span>

### <span data-ttu-id="18dab-128">System. String</span><span class="sxs-lookup"><span data-stu-id="18dab-128">System.String</span></span>

## <span data-ttu-id="18dab-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="18dab-129">OUTPUTS</span></span>

### <span data-ttu-id="18dab-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="18dab-130">System.Boolean</span></span>

## <span data-ttu-id="18dab-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="18dab-131">NOTES</span></span>

## <span data-ttu-id="18dab-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="18dab-132">RELATED LINKS</span></span>
