---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 92F21752-4FB6-4162-B542-DA25ACA3340B
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/set-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: 573bb9534107a4df020e21269b5bdb2ec12db125
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984607"
---
# <span data-ttu-id="91af7-101">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="91af7-101">Set-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="91af7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91af7-102">SYNOPSIS</span></span>
<span data-ttu-id="91af7-103">Ustawia wcześniej wykonaną akcję skryptu jako trwałą akcję skryptu.</span><span class="sxs-lookup"><span data-stu-id="91af7-103">Sets a previously executed script action to be a persisted script action.</span></span>

## <span data-ttu-id="91af7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="91af7-104">SYNTAX</span></span>

```
Set-AzHDInsightPersistedScriptAction [-ClusterName] <String> [-ScriptExecutionId] <Int64>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91af7-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="91af7-105">DESCRIPTION</span></span>
<span data-ttu-id="91af7-106">Polecenie **cmdlet Set-AzHDInsightPersistedScriptAction** ustawia wcześniej wykonaną akcję skryptu jako akcję skryptu trwałą.</span><span class="sxs-lookup"><span data-stu-id="91af7-106">The **Set-AzHDInsightPersistedScriptAction** cmdlet sets a previously executed script action to be a persisted script action.</span></span>
<span data-ttu-id="91af7-107">Określona akcja skryptu musi wcześniej zakończyć się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="91af7-107">The specified script action must have previously succeeded.</span></span>
<span data-ttu-id="91af7-108">Akcja skryptu będzie uruchamiana za każdym razem, gdy klaster usługi Azure HDInsight zostanie skalowany.</span><span class="sxs-lookup"><span data-stu-id="91af7-108">The script action will run each time the Azure HDInsight cluster is scaled up.</span></span>

## <span data-ttu-id="91af7-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="91af7-109">EXAMPLES</span></span>

### <span data-ttu-id="91af7-110">Przykład 1. Ustawianie wcześniej pomyślnej akcji skryptu, która ma zostać utrwalona lub uruchamiana na skali klastrów w górę</span><span class="sxs-lookup"><span data-stu-id="91af7-110">Example 1: Set a previously successful script action to be persisted, or run on cluster scale up</span></span>
```
PS C:\>Set-AzHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -ScriptExecutionId "<id>"
```

<span data-ttu-id="91af7-111">To polecenie ustawia wcześniej pomyślną akcję skryptu jako trwałą akcję skryptu.</span><span class="sxs-lookup"><span data-stu-id="91af7-111">This command sets a previously successful script action to be a persisted script action.</span></span>

## <span data-ttu-id="91af7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91af7-112">PARAMETERS</span></span>

### <span data-ttu-id="91af7-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="91af7-113">-ClusterName</span></span>
<span data-ttu-id="91af7-114">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="91af7-114">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="91af7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91af7-115">-DefaultProfile</span></span>
<span data-ttu-id="91af7-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="91af7-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="91af7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91af7-117">-ResourceGroupName</span></span>
<span data-ttu-id="91af7-118">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="91af7-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="91af7-119">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="91af7-119">-ScriptExecutionId</span></span>
<span data-ttu-id="91af7-120">Określa identyfikator wykonywania akcji skryptu, która ma być zachowywana.</span><span class="sxs-lookup"><span data-stu-id="91af7-120">Specifies the execution ID of the script action to promote to persisted.</span></span>
<span data-ttu-id="91af7-121">Aby można było promować tę akcję skryptu, musi się ona zakończyć powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="91af7-121">This script action must have succeeded in order to be promoted.</span></span>
<span data-ttu-id="91af7-122">Identyfikator wykonywania akcji skryptu możesz znaleźć przy użyciu polecenia Get-AzHDInsightScriptActionHistory.</span><span class="sxs-lookup"><span data-stu-id="91af7-122">You can find the script action execution ID using Get-AzHDInsightScriptActionHistory.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91af7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91af7-123">CommonParameters</span></span>
<span data-ttu-id="91af7-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91af7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91af7-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="91af7-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91af7-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="91af7-126">INPUTS</span></span>

### <span data-ttu-id="91af7-127">Brak</span><span class="sxs-lookup"><span data-stu-id="91af7-127">None</span></span>

## <span data-ttu-id="91af7-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="91af7-128">OUTPUTS</span></span>

### <span data-ttu-id="91af7-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="91af7-129">System.Void</span></span>

## <span data-ttu-id="91af7-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="91af7-130">NOTES</span></span>

## <span data-ttu-id="91af7-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="91af7-131">RELATED LINKS</span></span>

[<span data-ttu-id="91af7-132">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="91af7-132">Get-AzHDInsightPersistedScriptAction</span></span>](./Get-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="91af7-133">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="91af7-133">Remove-AzHDInsightPersistedScriptAction</span></span>](./Remove-AzHDInsightPersistedScriptAction.md)


