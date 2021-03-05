---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 08D1D6AC-D064-4E2D-9C22-0B65E7BE4DA7
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/remove-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: a7c5c9c2008839d4e90dd5f393fbe4acea0f78a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965889"
---
# <span data-ttu-id="17c6c-101">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="17c6c-101">Remove-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="17c6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17c6c-102">SYNOPSIS</span></span>
<span data-ttu-id="17c6c-103">Usuwa trwałą akcję skryptu z klastra HDInsight.</span><span class="sxs-lookup"><span data-stu-id="17c6c-103">Removes an persisted script action from an HDInsight cluster.</span></span>

## <span data-ttu-id="17c6c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="17c6c-104">SYNTAX</span></span>

```
Remove-AzHDInsightPersistedScriptAction [-ClusterName] <String> [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17c6c-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="17c6c-105">DESCRIPTION</span></span>
<span data-ttu-id="17c6c-106">Polecenie cmdlet **Remove-AzHDInsightPersistedScriptAction** usuwa utrwaloną akcję skryptu z listy utrwalonych akcji skryptów określonego klastra usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="17c6c-106">The **Remove-AzHDInsightPersistedScriptAction** cmdlet removes a persisted script action from the specified Azure HDInsight cluster's list of persisted script actions.</span></span>
<span data-ttu-id="17c6c-107">Usunięty skrypt nie będzie już wykonywany, gdy klaster zostanie przeskalowany.</span><span class="sxs-lookup"><span data-stu-id="17c6c-107">The removed script will no longer be executed when the cluster is scaled up.</span></span>

## <span data-ttu-id="17c6c-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="17c6c-108">EXAMPLES</span></span>

### <span data-ttu-id="17c6c-109">Przykład 1. Usunięcie akcji skryptu z listy utrwalonych akcji skryptu w klastrze</span><span class="sxs-lookup"><span data-stu-id="17c6c-109">Example 1: Remove a script action from the list of persisted script actions on a cluster</span></span>
```
PS C:\>Remove-AzHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "Scriptaction"
```

<span data-ttu-id="17c6c-110">To polecenie usuwa akcję skryptu o nazwie Scriptaction z listy utrwalonych akcji skryptów w określonym klastrze.</span><span class="sxs-lookup"><span data-stu-id="17c6c-110">This command removes the script action named Scriptaction from the list of persisted script actions on the specified cluster.</span></span>

## <span data-ttu-id="17c6c-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17c6c-111">PARAMETERS</span></span>

### <span data-ttu-id="17c6c-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="17c6c-112">-ClusterName</span></span>
<span data-ttu-id="17c6c-113">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="17c6c-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="17c6c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17c6c-114">-DefaultProfile</span></span>
<span data-ttu-id="17c6c-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="17c6c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="17c6c-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="17c6c-116">-Name</span></span>
<span data-ttu-id="17c6c-117">Określa nazwę akcji utrwalonego skryptu do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="17c6c-117">Specifies the name of the persisted script action to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17c6c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17c6c-118">-ResourceGroupName</span></span>
<span data-ttu-id="17c6c-119">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="17c6c-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="17c6c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17c6c-120">CommonParameters</span></span>
<span data-ttu-id="17c6c-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17c6c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17c6c-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="17c6c-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17c6c-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="17c6c-123">INPUTS</span></span>

### <span data-ttu-id="17c6c-124">Brak</span><span class="sxs-lookup"><span data-stu-id="17c6c-124">None</span></span>

## <span data-ttu-id="17c6c-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="17c6c-125">OUTPUTS</span></span>

### <span data-ttu-id="17c6c-126">System.Void</span><span class="sxs-lookup"><span data-stu-id="17c6c-126">System.Void</span></span>

## <span data-ttu-id="17c6c-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="17c6c-127">NOTES</span></span>

## <span data-ttu-id="17c6c-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="17c6c-128">RELATED LINKS</span></span>

[<span data-ttu-id="17c6c-129">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="17c6c-129">Get-AzHDInsightPersistedScriptAction</span></span>](./Get-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="17c6c-130">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="17c6c-130">Set-AzHDInsightPersistedScriptAction</span></span>](./Set-AzHDInsightPersistedScriptAction.md)


