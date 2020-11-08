---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: CE690DB0-0CD4-4841-B219-C208173D4730
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightscriptactionhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightScriptActionHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightScriptActionHistory.md
ms.openlocfilehash: 4f73c58ee709e53e1337c161b698aa31cc38ca43
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062210"
---
# <span data-ttu-id="b0be5-101">Get-AzHDInsightScriptActionHistory</span><span class="sxs-lookup"><span data-stu-id="b0be5-101">Get-AzHDInsightScriptActionHistory</span></span>

## <span data-ttu-id="b0be5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b0be5-102">SYNOPSIS</span></span>
<span data-ttu-id="b0be5-103">Pobiera historię akcji skryptów dla klastra i wyświetla ją w odwrotnej kolejności chronologicznej lub zawiera szczegółowe informacje o wykonanej akcji skryptu.</span><span class="sxs-lookup"><span data-stu-id="b0be5-103">Gets the script action history for a cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

## <span data-ttu-id="b0be5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b0be5-104">SYNTAX</span></span>

```
Get-AzHDInsightScriptActionHistory [-ClusterName] <String> [[-ScriptExecutionId] <Int64>]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0be5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b0be5-105">DESCRIPTION</span></span>
<span data-ttu-id="b0be5-106">Polecenie cmdlet **Get-AzHDInsightScriptActionHistory** pobiera historię akcji skryptów dla klastra usługi Azure HDInsight i wyświetla listę w odwrotnym porządku chronologicznym lub pobiera szczegóły akcji skryptu.</span><span class="sxs-lookup"><span data-stu-id="b0be5-106">The **Get-AzHDInsightScriptActionHistory** cmdlet gets the script action history for an Azure HDInsight cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

## <span data-ttu-id="b0be5-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b0be5-107">EXAMPLES</span></span>

### <span data-ttu-id="b0be5-108">Przykład 1: uzyskiwanie historii wykonania akcji skryptu dla klastra</span><span class="sxs-lookup"><span data-stu-id="b0be5-108">Example 1: Get the history of script actions executions for a cluster</span></span>
```
PS C:\>Get-AzHDInsightScriptActionHistory -ClusterName "your-hadoop-001"
```

<span data-ttu-id="b0be5-109">To polecenie umożliwia wyświetlenie historii akcji skryptów dla klastra-usługi Hadoop-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="b0be5-109">This command gets the history of script actions for the cluster your-hadoop-001.</span></span>

## <span data-ttu-id="b0be5-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b0be5-110">PARAMETERS</span></span>

### <span data-ttu-id="b0be5-111">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="b0be5-111">-ClusterName</span></span>
<span data-ttu-id="b0be5-112">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="b0be5-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="b0be5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0be5-113">-DefaultProfile</span></span>
<span data-ttu-id="b0be5-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b0be5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b0be5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0be5-115">-ResourceGroupName</span></span>
<span data-ttu-id="b0be5-116">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b0be5-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="b0be5-117">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="b0be5-117">-ScriptExecutionId</span></span>
<span data-ttu-id="b0be5-118">Określa identyfikator wykonania akcji wykonanego skryptu.</span><span class="sxs-lookup"><span data-stu-id="b0be5-118">Specifies the execution ID of the executed script action.</span></span>

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

### <span data-ttu-id="b0be5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0be5-119">CommonParameters</span></span>
<span data-ttu-id="b0be5-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0be5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0be5-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0be5-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0be5-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b0be5-122">INPUTS</span></span>

### <span data-ttu-id="b0be5-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b0be5-123">None</span></span>

## <span data-ttu-id="b0be5-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b0be5-124">OUTPUTS</span></span>

### <span data-ttu-id="b0be5-125">Microsoft. Azure. Commands. HDInsight. models. Management. AzureHDInsightRuntimeScriptActionDetail</span><span class="sxs-lookup"><span data-stu-id="b0be5-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionDetail</span></span>

## <span data-ttu-id="b0be5-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b0be5-126">NOTES</span></span>

## <span data-ttu-id="b0be5-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b0be5-127">RELATED LINKS</span></span>
