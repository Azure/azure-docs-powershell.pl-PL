---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2B7C1B83-EEEA-4BD1-9E9B-1F3070295995
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: b5d62e963bdd2f30ab0c5b821854ee46b391376b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489609"
---
# <span data-ttu-id="a14f4-101">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="a14f4-101">Get-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="a14f4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a14f4-102">SYNOPSIS</span></span>
<span data-ttu-id="a14f4-103">Pobiera akcje trwałego skryptu dla klastra i umieszcza je na liście w kolejności chronologicznej lub pobiera szczegóły określonego działania skryptu trwałego.</span><span class="sxs-lookup"><span data-stu-id="a14f4-103">Gets the persisted script actions for a cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="a14f4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a14f4-104">SYNTAX</span></span>

```
Get-AzHDInsightPersistedScriptAction [-ClusterName] <String> [[-Name] <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a14f4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a14f4-105">DESCRIPTION</span></span>
<span data-ttu-id="a14f4-106">Polecenie cmdlet **Get-AzHDInsightPersistedScriptAction** pobiera utrwalone akcje skryptu dla klastra usługi Azure HDInsight i wyświetla je w porządku chronologicznym lub pobiera szczegóły określonego działania skryptu trwałego.</span><span class="sxs-lookup"><span data-stu-id="a14f4-106">The **Get-AzHDInsightPersistedScriptAction** cmdlet gets the persisted script actions for an Azure HDInsight cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="a14f4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a14f4-107">EXAMPLES</span></span>

### <span data-ttu-id="a14f4-108">Przykład 1: uzyskiwanie akcji trwałego skryptu w klastrze</span><span class="sxs-lookup"><span data-stu-id="a14f4-108">Example 1: Get the persisted script actions on a cluster</span></span>
```
PS C:\>Get-AzHDInsightPersistedScriptAction -ClusterName "your-hadoop-001"
```

<span data-ttu-id="a14f4-109">To polecenie pobiera akcje trwałego skryptu w klastrze o nazwie Your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="a14f4-109">This command gets persisted script actions on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="a14f4-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a14f4-110">PARAMETERS</span></span>

### <span data-ttu-id="a14f4-111">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="a14f4-111">-ClusterName</span></span>
<span data-ttu-id="a14f4-112">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="a14f4-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="a14f4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a14f4-113">-DefaultProfile</span></span>
<span data-ttu-id="a14f4-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a14f4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a14f4-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a14f4-115">-Name</span></span>
<span data-ttu-id="a14f4-116">Określa nazwę akcji skryptu utrwalonego.</span><span class="sxs-lookup"><span data-stu-id="a14f4-116">Specifies the name of the persisted script action.</span></span>

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

### <span data-ttu-id="a14f4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a14f4-117">-ResourceGroupName</span></span>
<span data-ttu-id="a14f4-118">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a14f4-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="a14f4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a14f4-119">CommonParameters</span></span>
<span data-ttu-id="a14f4-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a14f4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a14f4-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a14f4-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a14f4-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a14f4-122">INPUTS</span></span>

### <span data-ttu-id="a14f4-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a14f4-123">None</span></span>

## <span data-ttu-id="a14f4-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a14f4-124">OUTPUTS</span></span>

### <span data-ttu-id="a14f4-125">Microsoft. Azure. Commands. HDInsight. models. Management. AzureHDInsightRuntimeScriptAction</span><span class="sxs-lookup"><span data-stu-id="a14f4-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptAction</span></span>

## <span data-ttu-id="a14f4-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a14f4-126">NOTES</span></span>

## <span data-ttu-id="a14f4-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a14f4-127">RELATED LINKS</span></span>

[<span data-ttu-id="a14f4-128">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="a14f4-128">Remove-AzHDInsightPersistedScriptAction</span></span>](./Remove-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="a14f4-129">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="a14f4-129">Set-AzHDInsightPersistedScriptAction</span></span>](./Set-AzHDInsightPersistedScriptAction.md)


