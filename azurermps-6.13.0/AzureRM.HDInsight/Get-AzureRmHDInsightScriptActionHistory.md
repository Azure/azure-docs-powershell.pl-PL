---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: CE690DB0-0CD4-4841-B219-C208173D4730
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightscriptactionhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightScriptActionHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightScriptActionHistory.md
ms.openlocfilehash: cadedd6441d45065344d2bf1998552b693a01301
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545291"
---
# <span data-ttu-id="53f04-101">Get-AzureRmHDInsightScriptActionHistory</span><span class="sxs-lookup"><span data-stu-id="53f04-101">Get-AzureRmHDInsightScriptActionHistory</span></span>

## <span data-ttu-id="53f04-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="53f04-102">SYNOPSIS</span></span>
<span data-ttu-id="53f04-103">Pobiera historię akcji skryptów dla klastra i wyświetla ją w odwrotnej kolejności chronologicznej lub zawiera szczegółowe informacje o wykonanej akcji skryptu.</span><span class="sxs-lookup"><span data-stu-id="53f04-103">Gets the script action history for a cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53f04-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="53f04-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightScriptActionHistory [-ClusterName] <String> [[-ScriptExecutionId] <Int64>]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53f04-105">Opis</span><span class="sxs-lookup"><span data-stu-id="53f04-105">DESCRIPTION</span></span>
<span data-ttu-id="53f04-106">Polecenie cmdlet **Get-AzureRmHDInsightScriptActionHistory** pobiera historię akcji skryptów dla klastra usługi Azure HDInsight i wyświetla listę w odwrotnym porządku chronologicznym lub pobiera szczegóły akcji skryptu.</span><span class="sxs-lookup"><span data-stu-id="53f04-106">The **Get-AzureRmHDInsightScriptActionHistory** cmdlet gets the script action history for an Azure HDInsight cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

## <span data-ttu-id="53f04-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="53f04-107">EXAMPLES</span></span>

### <span data-ttu-id="53f04-108">Przykład 1: uzyskiwanie historii wykonania akcji skryptu dla klastra</span><span class="sxs-lookup"><span data-stu-id="53f04-108">Example 1: Get the history of script actions executions for a cluster</span></span>
```
PS C:\>Get-AzureRmHDInsightScriptActionHistory -ClusterName "your-hadoop-001"
```

<span data-ttu-id="53f04-109">To polecenie umożliwia wyświetlenie historii akcji skryptów dla klastra-usługi Hadoop-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="53f04-109">This command gets the history of script actions for the cluster your-hadoop-001.</span></span>

## <span data-ttu-id="53f04-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="53f04-110">PARAMETERS</span></span>

### <span data-ttu-id="53f04-111">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="53f04-111">-ClusterName</span></span>
<span data-ttu-id="53f04-112">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="53f04-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="53f04-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53f04-113">-DefaultProfile</span></span>
<span data-ttu-id="53f04-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="53f04-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="53f04-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53f04-115">-ResourceGroupName</span></span>
<span data-ttu-id="53f04-116">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="53f04-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="53f04-117">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="53f04-117">-ScriptExecutionId</span></span>
<span data-ttu-id="53f04-118">Określa identyfikator wykonania akcji wykonanego skryptu.</span><span class="sxs-lookup"><span data-stu-id="53f04-118">Specifies the execution ID of the executed script action.</span></span>

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

### <span data-ttu-id="53f04-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53f04-119">CommonParameters</span></span>
<span data-ttu-id="53f04-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53f04-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53f04-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53f04-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53f04-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="53f04-122">INPUTS</span></span>

### <span data-ttu-id="53f04-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="53f04-123">None</span></span>

## <span data-ttu-id="53f04-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="53f04-124">OUTPUTS</span></span>

### <span data-ttu-id="53f04-125">Microsoft. Azure. Commands. HDInsight. models. Management. AzureHDInsightRuntimeScriptActionDetail</span><span class="sxs-lookup"><span data-stu-id="53f04-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionDetail</span></span>

## <span data-ttu-id="53f04-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="53f04-126">NOTES</span></span>

## <span data-ttu-id="53f04-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="53f04-127">RELATED LINKS</span></span>