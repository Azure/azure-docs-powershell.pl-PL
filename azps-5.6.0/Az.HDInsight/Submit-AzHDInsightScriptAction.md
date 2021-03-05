---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 15C5D659-472B-41DD-806A-A0A175434EE3
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/submit-azhdinsightscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Submit-AzHDInsightScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Submit-AzHDInsightScriptAction.md
ms.openlocfilehash: 9481c16db393a9147a4730b4c5f496e86c94eb0e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992685"
---
# <span data-ttu-id="6b53d-101">Submit-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="6b53d-101">Submit-AzHDInsightScriptAction</span></span>

## <span data-ttu-id="6b53d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b53d-102">SYNOPSIS</span></span>
<span data-ttu-id="6b53d-103">Przesyła nową akcję skryptu do klastrów usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="6b53d-103">Submits a new script action to an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="6b53d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6b53d-104">SYNTAX</span></span>

```
Submit-AzHDInsightScriptAction [-ClusterName] <String> [-Name] <String> [-Uri] <Uri>
 [-NodeTypes] <RuntimeScriptActionClusterNodeType[]> [[-Parameters] <String>] [[-ApplicationName] <String>]
 [-PersistOnSuccess] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6b53d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="6b53d-105">DESCRIPTION</span></span>
<span data-ttu-id="6b53d-106">Polecenie **cmdlet Submit-AzHDInsightScriptAction** przesyła nową akcję skryptu do klastru usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="6b53d-106">The **Submit-AzHDInsightScriptAction** cmdlet submits a new script action to an Azure HDInsight cluster.</span></span>
<span data-ttu-id="6b53d-107">Użyj *funkcji PersistOnSuccess,* aby akcja skryptu była uruchamiana za każdym razem, gdy klaster jest skalowany w górę, o ile akcja skryptu początkowo się powiedzie.</span><span class="sxs-lookup"><span data-stu-id="6b53d-107">Use *PersistOnSuccess* to have the script action run each time the cluster is scaled up, as long as the script action initially succeeds.</span></span>

## <span data-ttu-id="6b53d-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6b53d-108">EXAMPLES</span></span>

### <span data-ttu-id="6b53d-109">Przykład 1. Przesyłanie nowej akcji skryptu do uruchomionego klastra usługi HDInsight</span><span class="sxs-lookup"><span data-stu-id="6b53d-109">Example 1: Submit a new script action to a running HDInsight cluster</span></span>
```
PS C:\>Submit-AzHDInsightScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "scriptaction" `
            -Uri "<script action URI>" `
            -NodeTypes Worker -PersistOnSuccess
```

<span data-ttu-id="6b53d-110">To polecenie przesyła akcję skryptu do uruchomionego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="6b53d-110">This command submits a script action to a running HDInsight cluster.</span></span>

## <span data-ttu-id="6b53d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b53d-111">PARAMETERS</span></span>

### <span data-ttu-id="6b53d-112">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="6b53d-112">-ApplicationName</span></span>
<span data-ttu-id="6b53d-113">Określa nazwę aplikacji dla akcji skryptu.</span><span class="sxs-lookup"><span data-stu-id="6b53d-113">Specifies the application name for the script action.</span></span>
<span data-ttu-id="6b53d-114">Gdy *jest określona* nazwa_aplikacji, *wartość PersistOnSuccess* powinna być ustawiona na Fałsz, węzły muszą zawierać tylko edgenode, a liczba akcji skryptów powinna być równa 1.</span><span class="sxs-lookup"><span data-stu-id="6b53d-114">When *ApplicationName* is specified, *PersistOnSuccess* should be set to False, nodes must contain only edgenode, and script action count should equal 1.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b53d-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="6b53d-115">-ClusterName</span></span>
<span data-ttu-id="6b53d-116">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="6b53d-116">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="6b53d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b53d-117">-DefaultProfile</span></span>
<span data-ttu-id="6b53d-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="6b53d-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6b53d-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6b53d-119">-Name</span></span>
<span data-ttu-id="6b53d-120">Określa nazwę akcji skryptu.</span><span class="sxs-lookup"><span data-stu-id="6b53d-120">Specifies the name of the script action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b53d-121">-NodeTypes</span><span class="sxs-lookup"><span data-stu-id="6b53d-121">-NodeTypes</span></span>
<span data-ttu-id="6b53d-122">Określa typy węzła, na których ma być uruchamiana akcja skryptu.</span><span class="sxs-lookup"><span data-stu-id="6b53d-122">Specifies the node types on which to run the script action.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Management.RuntimeScriptActionClusterNodeType[]
Parameter Sets: (All)
Aliases:
Accepted values: HeadNode, WorkerNode, ZookeeperNode, EdgeNode

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b53d-123">— Parametry</span><span class="sxs-lookup"><span data-stu-id="6b53d-123">-Parameters</span></span>
<span data-ttu-id="6b53d-124">Określa parametry akcji skryptu.</span><span class="sxs-lookup"><span data-stu-id="6b53d-124">Specifies the parameters for the script action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b53d-125">- PersistOnSuccess</span><span class="sxs-lookup"><span data-stu-id="6b53d-125">-PersistOnSuccess</span></span>
<span data-ttu-id="6b53d-126">Wskazuje, że akcja skryptu powinna być uruchamiana za każdym razem, gdy klaster jest skalowany w górę.</span><span class="sxs-lookup"><span data-stu-id="6b53d-126">Indicates that the script action should run each time the cluster is scaled up.</span></span>
<span data-ttu-id="6b53d-127">Ten parametr przełącznika jest ignorowany, jeśli akcja skryptu na początku zakończy się niepowodzeniem.</span><span class="sxs-lookup"><span data-stu-id="6b53d-127">This switch parameter is ignored if the script action initially fails.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b53d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b53d-128">-ResourceGroupName</span></span>
<span data-ttu-id="6b53d-129">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6b53d-129">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="6b53d-130">-Uri</span><span class="sxs-lookup"><span data-stu-id="6b53d-130">-Uri</span></span>
<span data-ttu-id="6b53d-131">Określa publiczny URI dla akcji skryptu (skryptu PowerShell lub Bash).</span><span class="sxs-lookup"><span data-stu-id="6b53d-131">Specifies the public URI for the script action (a PowerShell or Bash script).</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b53d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b53d-132">CommonParameters</span></span>
<span data-ttu-id="6b53d-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b53d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b53d-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6b53d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b53d-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6b53d-135">INPUTS</span></span>

### <span data-ttu-id="6b53d-136">System.String</span><span class="sxs-lookup"><span data-stu-id="6b53d-136">System.String</span></span>

### <span data-ttu-id="6b53d-137">System.Uri</span><span class="sxs-lookup"><span data-stu-id="6b53d-137">System.Uri</span></span>

### <span data-ttu-id="6b53d-138">Microsoft.Azure.Commands.HDInsight.Models.Management.RuntimeScriptActionClusterNodeType[]</span><span class="sxs-lookup"><span data-stu-id="6b53d-138">Microsoft.Azure.Commands.HDInsight.Models.Management.RuntimeScriptActionClusterNodeType[]</span></span>

## <span data-ttu-id="6b53d-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6b53d-139">OUTPUTS</span></span>

### <span data-ttu-id="6b53d-140">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionOperationResource</span><span class="sxs-lookup"><span data-stu-id="6b53d-140">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionOperationResource</span></span>

## <span data-ttu-id="6b53d-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6b53d-141">NOTES</span></span>

## <span data-ttu-id="6b53d-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6b53d-142">RELATED LINKS</span></span>

[<span data-ttu-id="6b53d-143">Add-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="6b53d-143">Add-AzHDInsightScriptAction</span></span>](./Add-AzHDInsightScriptAction.md)


