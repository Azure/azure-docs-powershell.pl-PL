---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 15C5D659-472B-41DD-806A-A0A175434EE3
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/submit-azhdinsightscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Submit-AzHDInsightScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Submit-AzHDInsightScriptAction.md
ms.openlocfilehash: ef1c06c475b5de4984abf7859f033d68ad7d9dfa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705290"
---
# <span data-ttu-id="e566a-101">Submit-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="e566a-101">Submit-AzHDInsightScriptAction</span></span>

## <span data-ttu-id="e566a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e566a-102">SYNOPSIS</span></span>
<span data-ttu-id="e566a-103">Wysyła nową akcję skryptu do klastra usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e566a-103">Submits a new script action to an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="e566a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e566a-104">SYNTAX</span></span>

```
Submit-AzHDInsightScriptAction [-ClusterName] <String> [-Name] <String> [-Uri] <Uri>
 [-NodeTypes] <RuntimeScriptActionClusterNodeType[]> [[-Parameters] <String>] [[-ApplicationName] <String>]
 [-PersistOnSuccess] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e566a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e566a-105">DESCRIPTION</span></span>
<span data-ttu-id="e566a-106">Polecenie cmdlet **Submit-AzHDInsightScriptAction** umożliwia przesłanie nowej akcji skryptu do klastra usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e566a-106">The **Submit-AzHDInsightScriptAction** cmdlet submits a new script action to an Azure HDInsight cluster.</span></span>
<span data-ttu-id="e566a-107">Użyj *PersistOnSuccess* , aby akcja skryptu była uruchamiana za każdym razem, gdy klaster jest skalowany, o ile akcja skryptu jest początkowo zakończona.</span><span class="sxs-lookup"><span data-stu-id="e566a-107">Use *PersistOnSuccess* to have the script action run each time the cluster is scaled up, as long as the script action initially succeeds.</span></span>

## <span data-ttu-id="e566a-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e566a-108">EXAMPLES</span></span>

### <span data-ttu-id="e566a-109">Przykład 1: przesyłanie nowej akcji skryptu do uruchomionego klastra usługi HDInsight</span><span class="sxs-lookup"><span data-stu-id="e566a-109">Example 1: Submit a new script action to a running HDInsight cluster</span></span>
```
PS C:\>Submit-AzHDInsightScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "scriptaction" `
            -Uri "<script action URI>" `
            -NodeTypes Worker -PersistOnSuccess
```

<span data-ttu-id="e566a-110">To polecenie przesyła akcję skryptu do uruchomionego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e566a-110">This command submits a script action to a running HDInsight cluster.</span></span>

## <span data-ttu-id="e566a-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e566a-111">PARAMETERS</span></span>

### <span data-ttu-id="e566a-112">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="e566a-112">-ApplicationName</span></span>
<span data-ttu-id="e566a-113">Określa nazwę aplikacji dla akcji skryptu.</span><span class="sxs-lookup"><span data-stu-id="e566a-113">Specifies the application name for the script action.</span></span>
<span data-ttu-id="e566a-114">Gdy właściwość *ApplicationName* jest określona, *PersistOnSuccess* powinna mieć wartość false, węzły muszą zawierać tylko edgenode, a liczba akcji skryptu powinna być równa 1.</span><span class="sxs-lookup"><span data-stu-id="e566a-114">When *ApplicationName* is specified, *PersistOnSuccess* should be set to False, nodes must contain only edgenode, and script action count should equal 1.</span></span>

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

### <span data-ttu-id="e566a-115">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="e566a-115">-ClusterName</span></span>
<span data-ttu-id="e566a-116">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="e566a-116">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="e566a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e566a-117">-DefaultProfile</span></span>
<span data-ttu-id="e566a-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e566a-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e566a-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e566a-119">-Name</span></span>
<span data-ttu-id="e566a-120">Określa nazwę akcji skryptu.</span><span class="sxs-lookup"><span data-stu-id="e566a-120">Specifies the name of the script action.</span></span>

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

### <span data-ttu-id="e566a-121">-NodeTypes</span><span class="sxs-lookup"><span data-stu-id="e566a-121">-NodeTypes</span></span>
<span data-ttu-id="e566a-122">Określa typy węzłów, na których ma zostać uruchomiona akcja skryptu.</span><span class="sxs-lookup"><span data-stu-id="e566a-122">Specifies the node types on which to run the script action.</span></span>

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

### <span data-ttu-id="e566a-123">— Parametry</span><span class="sxs-lookup"><span data-stu-id="e566a-123">-Parameters</span></span>
<span data-ttu-id="e566a-124">Określa parametry akcji skryptu.</span><span class="sxs-lookup"><span data-stu-id="e566a-124">Specifies the parameters for the script action.</span></span>

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

### <span data-ttu-id="e566a-125">-PersistOnSuccess</span><span class="sxs-lookup"><span data-stu-id="e566a-125">-PersistOnSuccess</span></span>
<span data-ttu-id="e566a-126">Wskazuje, że akcja skryptu powinna być uruchamiana za każdym razem, gdy klaster jest skalowany.</span><span class="sxs-lookup"><span data-stu-id="e566a-126">Indicates that the script action should run each time the cluster is scaled up.</span></span>
<span data-ttu-id="e566a-127">Ten parametr przełącznika jest ignorowany, jeśli akcja skryptu jest początkowo niepowodzenie.</span><span class="sxs-lookup"><span data-stu-id="e566a-127">This switch parameter is ignored if the script action initially fails.</span></span>

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

### <span data-ttu-id="e566a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e566a-128">-ResourceGroupName</span></span>
<span data-ttu-id="e566a-129">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e566a-129">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="e566a-130">-URI</span><span class="sxs-lookup"><span data-stu-id="e566a-130">-Uri</span></span>
<span data-ttu-id="e566a-131">Określa publiczny identyfikator URI akcji skryptu (programu PowerShell lub skryptu bash).</span><span class="sxs-lookup"><span data-stu-id="e566a-131">Specifies the public URI for the script action (a PowerShell or Bash script).</span></span>

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

### <span data-ttu-id="e566a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e566a-132">CommonParameters</span></span>
<span data-ttu-id="e566a-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e566a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e566a-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e566a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e566a-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e566a-135">INPUTS</span></span>

### <span data-ttu-id="e566a-136">System. String</span><span class="sxs-lookup"><span data-stu-id="e566a-136">System.String</span></span>

### <span data-ttu-id="e566a-137">System. URI</span><span class="sxs-lookup"><span data-stu-id="e566a-137">System.Uri</span></span>

### <span data-ttu-id="e566a-138">Microsoft. Azure. Commands. HDInsight. models. Management. RuntimeScriptActionClusterNodeType []</span><span class="sxs-lookup"><span data-stu-id="e566a-138">Microsoft.Azure.Commands.HDInsight.Models.Management.RuntimeScriptActionClusterNodeType[]</span></span>

## <span data-ttu-id="e566a-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e566a-139">OUTPUTS</span></span>

### <span data-ttu-id="e566a-140">Microsoft. Azure. Commands. HDInsight. models. Management. AzureHDInsightRuntimeScriptActionOperationResource</span><span class="sxs-lookup"><span data-stu-id="e566a-140">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionOperationResource</span></span>

## <span data-ttu-id="e566a-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e566a-141">NOTES</span></span>

## <span data-ttu-id="e566a-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e566a-142">RELATED LINKS</span></span>

[<span data-ttu-id="e566a-143">Dodaj-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="e566a-143">Add-AzHDInsightScriptAction</span></span>](./Add-AzHDInsightScriptAction.md)


