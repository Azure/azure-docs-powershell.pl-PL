---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2B7C1B83-EEEA-4BD1-9E9B-1F3070295995
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: 56056e2933254401645a30e190a3a181b0c4514f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338245"
---
# <span data-ttu-id="e2ca7-101">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="e2ca7-101">Get-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="e2ca7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e2ca7-102">SYNOPSIS</span></span>
<span data-ttu-id="e2ca7-103">Pobiera akcje trwałego skryptu dla klastra i umieszcza je na liście w kolejności chronologicznej lub pobiera szczegóły określonego działania skryptu trwałego.</span><span class="sxs-lookup"><span data-stu-id="e2ca7-103">Gets the persisted script actions for a cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="e2ca7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e2ca7-104">SYNTAX</span></span>

```
Get-AzHDInsightPersistedScriptAction [-ClusterName] <String> [[-Name] <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2ca7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e2ca7-105">DESCRIPTION</span></span>
<span data-ttu-id="e2ca7-106">Polecenie cmdlet **Get-AzHDInsightPersistedScriptAction** pobiera utrwalone akcje skryptu dla klastra usługi Azure HDInsight i wyświetla je w porządku chronologicznym lub pobiera szczegóły określonego działania skryptu trwałego.</span><span class="sxs-lookup"><span data-stu-id="e2ca7-106">The **Get-AzHDInsightPersistedScriptAction** cmdlet gets the persisted script actions for an Azure HDInsight cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="e2ca7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e2ca7-107">EXAMPLES</span></span>

### <span data-ttu-id="e2ca7-108">Przykład 1: uzyskiwanie akcji trwałego skryptu w klastrze</span><span class="sxs-lookup"><span data-stu-id="e2ca7-108">Example 1: Get the persisted script actions on a cluster</span></span>
```
PS C:\>Get-AzHDInsightPersistedScriptAction -ClusterName "your-hadoop-001"
```

<span data-ttu-id="e2ca7-109">To polecenie pobiera akcje trwałego skryptu w klastrze o nazwie Your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="e2ca7-109">This command gets persisted script actions on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="e2ca7-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e2ca7-110">PARAMETERS</span></span>

### <span data-ttu-id="e2ca7-111">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="e2ca7-111">-ClusterName</span></span>
<span data-ttu-id="e2ca7-112">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="e2ca7-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="e2ca7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2ca7-113">-DefaultProfile</span></span>
<span data-ttu-id="e2ca7-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e2ca7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e2ca7-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e2ca7-115">-Name</span></span>
<span data-ttu-id="e2ca7-116">Określa nazwę akcji skryptu utrwalonego.</span><span class="sxs-lookup"><span data-stu-id="e2ca7-116">Specifies the name of the persisted script action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2ca7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2ca7-117">-ResourceGroupName</span></span>
<span data-ttu-id="e2ca7-118">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e2ca7-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="e2ca7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2ca7-119">CommonParameters</span></span>
<span data-ttu-id="e2ca7-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2ca7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2ca7-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2ca7-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2ca7-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e2ca7-122">INPUTS</span></span>

### <span data-ttu-id="e2ca7-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e2ca7-123">None</span></span>

## <span data-ttu-id="e2ca7-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e2ca7-124">OUTPUTS</span></span>

### <span data-ttu-id="e2ca7-125">Microsoft. Azure. Commands. HDInsight. models. Management. AzureHDInsightRuntimeScriptAction</span><span class="sxs-lookup"><span data-stu-id="e2ca7-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptAction</span></span>

## <span data-ttu-id="e2ca7-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e2ca7-126">NOTES</span></span>

## <span data-ttu-id="e2ca7-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e2ca7-127">RELATED LINKS</span></span>

[<span data-ttu-id="e2ca7-128">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="e2ca7-128">Remove-AzHDInsightPersistedScriptAction</span></span>](./Remove-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="e2ca7-129">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="e2ca7-129">Set-AzHDInsightPersistedScriptAction</span></span>](./Set-AzHDInsightPersistedScriptAction.md)


