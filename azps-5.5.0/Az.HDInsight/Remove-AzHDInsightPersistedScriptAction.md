---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 08D1D6AC-D064-4E2D-9C22-0B65E7BE4DA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: 344c6fccd0f6c7db26110a94e2cacc53625df3d9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200202"
---
# <span data-ttu-id="49c21-101">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="49c21-101">Remove-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="49c21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49c21-102">SYNOPSIS</span></span>
<span data-ttu-id="49c21-103">Usuwa trwałą akcję skryptu z klastra HDInsight.</span><span class="sxs-lookup"><span data-stu-id="49c21-103">Removes an persisted script action from an HDInsight cluster.</span></span>

## <span data-ttu-id="49c21-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="49c21-104">SYNTAX</span></span>

```
Remove-AzHDInsightPersistedScriptAction [-ClusterName] <String> [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49c21-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="49c21-105">DESCRIPTION</span></span>
<span data-ttu-id="49c21-106">Polecenie cmdlet **Remove-AzHDInsightPersistedScriptAction** usuwa utrwaloną akcję skryptu z listy utrwalonych akcji skryptów określonego klastra usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="49c21-106">The **Remove-AzHDInsightPersistedScriptAction** cmdlet removes a persisted script action from the specified Azure HDInsight cluster's list of persisted script actions.</span></span>
<span data-ttu-id="49c21-107">Usunięty skrypt nie będzie już wykonywany, gdy klaster zostanie przeskalowany.</span><span class="sxs-lookup"><span data-stu-id="49c21-107">The removed script will no longer be executed when the cluster is scaled up.</span></span>

## <span data-ttu-id="49c21-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="49c21-108">EXAMPLES</span></span>

### <span data-ttu-id="49c21-109">Przykład 1. Usunięcie akcji skryptu z listy utrwalonych akcji skryptów w klastrze</span><span class="sxs-lookup"><span data-stu-id="49c21-109">Example 1: Remove a script action from the list of persisted script actions on a cluster</span></span>
```
PS C:\>Remove-AzHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "Scriptaction"
```

<span data-ttu-id="49c21-110">To polecenie usuwa akcję skryptu o nazwie Scriptaction z listy utrwalonych akcji skryptów w określonym klastrze.</span><span class="sxs-lookup"><span data-stu-id="49c21-110">This command removes the script action named Scriptaction from the list of persisted script actions on the specified cluster.</span></span>

## <span data-ttu-id="49c21-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49c21-111">PARAMETERS</span></span>

### <span data-ttu-id="49c21-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="49c21-112">-ClusterName</span></span>
<span data-ttu-id="49c21-113">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="49c21-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="49c21-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49c21-114">-DefaultProfile</span></span>
<span data-ttu-id="49c21-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="49c21-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="49c21-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="49c21-116">-Name</span></span>
<span data-ttu-id="49c21-117">Określa nazwę akcji utrwalonego skryptu do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="49c21-117">Specifies the name of the persisted script action to be removed.</span></span>

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

### <span data-ttu-id="49c21-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49c21-118">-ResourceGroupName</span></span>
<span data-ttu-id="49c21-119">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="49c21-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="49c21-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49c21-120">CommonParameters</span></span>
<span data-ttu-id="49c21-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49c21-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49c21-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49c21-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49c21-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="49c21-123">INPUTS</span></span>

### <span data-ttu-id="49c21-124">Brak</span><span class="sxs-lookup"><span data-stu-id="49c21-124">None</span></span>

## <span data-ttu-id="49c21-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="49c21-125">OUTPUTS</span></span>

### <span data-ttu-id="49c21-126">System.Void</span><span class="sxs-lookup"><span data-stu-id="49c21-126">System.Void</span></span>

## <span data-ttu-id="49c21-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="49c21-127">NOTES</span></span>

## <span data-ttu-id="49c21-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="49c21-128">RELATED LINKS</span></span>

[<span data-ttu-id="49c21-129">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="49c21-129">Get-AzHDInsightPersistedScriptAction</span></span>](./Get-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="49c21-130">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="49c21-130">Set-AzHDInsightPersistedScriptAction</span></span>](./Set-AzHDInsightPersistedScriptAction.md)


