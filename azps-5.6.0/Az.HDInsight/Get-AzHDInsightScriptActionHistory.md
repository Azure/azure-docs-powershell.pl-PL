---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: CE690DB0-0CD4-4841-B219-C208173D4730
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/get-azhdinsightscriptactionhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightScriptActionHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightScriptActionHistory.md
ms.openlocfilehash: 8273ad77091d008bead41e568f6c9d2de0e0d6f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983121"
---
# <span data-ttu-id="5f8f0-101">Get-AzHDInsightScriptActionHistory</span><span class="sxs-lookup"><span data-stu-id="5f8f0-101">Get-AzHDInsightScriptActionHistory</span></span>

## <span data-ttu-id="5f8f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f8f0-102">SYNOPSIS</span></span>
<span data-ttu-id="5f8f0-103">Pobiera historię akcji skryptu dla klastra i wyświetla ją w odwrotnej kolejności chronologicznej lub zawiera szczegóły wcześniej wykonanej akcji skryptu.</span><span class="sxs-lookup"><span data-stu-id="5f8f0-103">Gets the script action history for a cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

## <span data-ttu-id="5f8f0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5f8f0-104">SYNTAX</span></span>

```
Get-AzHDInsightScriptActionHistory [-ClusterName] <String> [[-ScriptExecutionId] <Int64>]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f8f0-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="5f8f0-105">DESCRIPTION</span></span>
<span data-ttu-id="5f8f0-106">Polecenie **cmdlet Get-AzHDInsightScriptActionHistory** pobiera historię akcji skryptów dla klastru usługi Azure HDInsight i wyświetla go w odwrotnej kolejności chronologicznej lub zawiera szczegóły wcześniej wykonanej akcji skryptu.</span><span class="sxs-lookup"><span data-stu-id="5f8f0-106">The **Get-AzHDInsightScriptActionHistory** cmdlet gets the script action history for an Azure HDInsight cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

## <span data-ttu-id="5f8f0-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5f8f0-107">EXAMPLES</span></span>

### <span data-ttu-id="5f8f0-108">Przykład 1. Uzyskiwanie historii wykonywania akcji skryptów dla klastra</span><span class="sxs-lookup"><span data-stu-id="5f8f0-108">Example 1: Get the history of script actions executions for a cluster</span></span>
```
PS C:\>Get-AzHDInsightScriptActionHistory -ClusterName "your-hadoop-001"
```

<span data-ttu-id="5f8f0-109">To polecenie pobiera historię akcji skryptów dla twojego-hadoop-001 klastra.</span><span class="sxs-lookup"><span data-stu-id="5f8f0-109">This command gets the history of script actions for the cluster your-hadoop-001.</span></span>

## <span data-ttu-id="5f8f0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5f8f0-110">PARAMETERS</span></span>

### <span data-ttu-id="5f8f0-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="5f8f0-111">-ClusterName</span></span>
<span data-ttu-id="5f8f0-112">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="5f8f0-112">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f8f0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f8f0-113">-DefaultProfile</span></span>
<span data-ttu-id="5f8f0-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="5f8f0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5f8f0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f8f0-115">-ResourceGroupName</span></span>
<span data-ttu-id="5f8f0-116">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5f8f0-116">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f8f0-117">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="5f8f0-117">-ScriptExecutionId</span></span>
<span data-ttu-id="5f8f0-118">Określa identyfikator wykonywania wykonanej akcji skryptu.</span><span class="sxs-lookup"><span data-stu-id="5f8f0-118">Specifies the execution ID of the executed script action.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f8f0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f8f0-119">CommonParameters</span></span>
<span data-ttu-id="5f8f0-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f8f0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f8f0-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5f8f0-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f8f0-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5f8f0-122">INPUTS</span></span>

### <span data-ttu-id="5f8f0-123">Brak</span><span class="sxs-lookup"><span data-stu-id="5f8f0-123">None</span></span>

## <span data-ttu-id="5f8f0-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5f8f0-124">OUTPUTS</span></span>

### <span data-ttu-id="5f8f0-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionDetail</span><span class="sxs-lookup"><span data-stu-id="5f8f0-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionDetail</span></span>

## <span data-ttu-id="5f8f0-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5f8f0-126">NOTES</span></span>

## <span data-ttu-id="5f8f0-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5f8f0-127">RELATED LINKS</span></span>
