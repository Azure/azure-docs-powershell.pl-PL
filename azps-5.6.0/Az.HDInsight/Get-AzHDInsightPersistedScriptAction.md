---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2B7C1B83-EEEA-4BD1-9E9B-1F3070295995
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/get-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: 136099b4fb37952825afbf82ba99a11695b901a9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009105"
---
# <span data-ttu-id="ceee6-101">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="ceee6-101">Get-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="ceee6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ceee6-102">SYNOPSIS</span></span>
<span data-ttu-id="ceee6-103">Pobiera utrwalone akcje skryptu dla klastra i wyświetla je w porządku chronologicznym lub pobiera szczegółowe informacje dotyczące określonej, utrwalonej akcji skryptu.</span><span class="sxs-lookup"><span data-stu-id="ceee6-103">Gets the persisted script actions for a cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="ceee6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ceee6-104">SYNTAX</span></span>

```
Get-AzHDInsightPersistedScriptAction [-ClusterName] <String> [[-Name] <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ceee6-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ceee6-105">DESCRIPTION</span></span>
<span data-ttu-id="ceee6-106">Polecenie **cmdlet Get-AzHDInsightPersistedScriptAction** pobiera utrwalone akcje skryptów dla klastru usługi Azure HDInsight i wyświetla je w porządku chronologicznym lub zawiera szczegółowe informacje dotyczące określonej utrwalonej akcji skryptu.</span><span class="sxs-lookup"><span data-stu-id="ceee6-106">The **Get-AzHDInsightPersistedScriptAction** cmdlet gets the persisted script actions for an Azure HDInsight cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="ceee6-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ceee6-107">EXAMPLES</span></span>

### <span data-ttu-id="ceee6-108">Przykład 1. Uzyskiwanie utrwalonych akcji skryptu w klastrze</span><span class="sxs-lookup"><span data-stu-id="ceee6-108">Example 1: Get the persisted script actions on a cluster</span></span>
```
PS C:\>Get-AzHDInsightPersistedScriptAction -ClusterName "your-hadoop-001"
```

<span data-ttu-id="ceee6-109">To polecenie jest zachowywane w ramach akcji skryptu w klastrze o nazwie Twoja-hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="ceee6-109">This command gets persisted script actions on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="ceee6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ceee6-110">PARAMETERS</span></span>

### <span data-ttu-id="ceee6-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ceee6-111">-ClusterName</span></span>
<span data-ttu-id="ceee6-112">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="ceee6-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="ceee6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ceee6-113">-DefaultProfile</span></span>
<span data-ttu-id="ceee6-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="ceee6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ceee6-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ceee6-115">-Name</span></span>
<span data-ttu-id="ceee6-116">Określa nazwę akcji utrwalonego skryptu.</span><span class="sxs-lookup"><span data-stu-id="ceee6-116">Specifies the name of the persisted script action.</span></span>

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

### <span data-ttu-id="ceee6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ceee6-117">-ResourceGroupName</span></span>
<span data-ttu-id="ceee6-118">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ceee6-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="ceee6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceee6-119">CommonParameters</span></span>
<span data-ttu-id="ceee6-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ceee6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceee6-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ceee6-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceee6-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ceee6-122">INPUTS</span></span>

### <span data-ttu-id="ceee6-123">Brak</span><span class="sxs-lookup"><span data-stu-id="ceee6-123">None</span></span>

## <span data-ttu-id="ceee6-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ceee6-124">OUTPUTS</span></span>

### <span data-ttu-id="ceee6-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptAction</span><span class="sxs-lookup"><span data-stu-id="ceee6-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptAction</span></span>

## <span data-ttu-id="ceee6-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ceee6-126">NOTES</span></span>

## <span data-ttu-id="ceee6-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ceee6-127">RELATED LINKS</span></span>

[<span data-ttu-id="ceee6-128">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="ceee6-128">Remove-AzHDInsightPersistedScriptAction</span></span>](./Remove-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="ceee6-129">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="ceee6-129">Set-AzHDInsightPersistedScriptAction</span></span>](./Set-AzHDInsightPersistedScriptAction.md)


