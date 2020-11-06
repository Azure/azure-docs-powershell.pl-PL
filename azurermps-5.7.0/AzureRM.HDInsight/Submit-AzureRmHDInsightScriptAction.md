---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 15C5D659-472B-41DD-806A-A0A175434EE3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/submit-azurermhdinsightscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Submit-AzureRmHDInsightScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Submit-AzureRmHDInsightScriptAction.md
ms.openlocfilehash: 866bd8c8189ca727b3893f09370bcca1136e827b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553678"
---
# <span data-ttu-id="2f459-101">Submit-AzureRmHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="2f459-101">Submit-AzureRmHDInsightScriptAction</span></span>

## <span data-ttu-id="2f459-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2f459-102">SYNOPSIS</span></span>
<span data-ttu-id="2f459-103">Wysyła nową akcję skryptu do klastra usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2f459-103">Submits a new script action to an Azure HDInsight cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f459-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2f459-104">SYNTAX</span></span>

```
Submit-AzureRmHDInsightScriptAction [-ClusterName] <String> [-Name] <String> [-Uri] <Uri>
 [-NodeTypes] <RuntimeScriptActionClusterNodeType[]> [[-Parameters] <String>] [[-ApplicationName] <String>]
 [-PersistOnSuccess] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2f459-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2f459-105">DESCRIPTION</span></span>
<span data-ttu-id="2f459-106">Polecenie cmdlet **Submit-AzureRmHDInsightScriptAction** umożliwia przesłanie nowej akcji skryptu do klastra usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2f459-106">The **Submit-AzureRmHDInsightScriptAction** cmdlet submits a new script action to an Azure HDInsight cluster.</span></span>
<span data-ttu-id="2f459-107">Użyj *PersistOnSuccess* , aby akcja skryptu była uruchamiana za każdym razem, gdy klaster jest skalowany, o ile akcja skryptu jest początkowo zakończona.</span><span class="sxs-lookup"><span data-stu-id="2f459-107">Use *PersistOnSuccess* to have the script action run each time the cluster is scaled up, as long as the script action initially succeeds.</span></span>

## <span data-ttu-id="2f459-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2f459-108">EXAMPLES</span></span>

### <span data-ttu-id="2f459-109">Przykład 1: przesyłanie nowej akcji skryptu do uruchomionego klastra usługi HDInsight</span><span class="sxs-lookup"><span data-stu-id="2f459-109">Example 1: Submit a new script action to a running HDInsight cluster</span></span>
```
PS C:\>Submit-AzureRmHDInsightScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "scriptaction" `
            -Uri "<script action URI>" `
            -NodeTypes Worker -PersistOnSuccess
```

<span data-ttu-id="2f459-110">To polecenie przesyła akcję skryptu do uruchomionego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2f459-110">This command submits a script action to a running HDInsight cluster.</span></span>

## <span data-ttu-id="2f459-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2f459-111">PARAMETERS</span></span>

### <span data-ttu-id="2f459-112">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="2f459-112">-ApplicationName</span></span>
<span data-ttu-id="2f459-113">Określa nazwę aplikacji dla akcji skryptu.</span><span class="sxs-lookup"><span data-stu-id="2f459-113">Specifies the application name for the script action.</span></span>
<span data-ttu-id="2f459-114">Gdy właściwość *ApplicationName* jest określona, *PersistOnSuccess* powinna mieć wartość false, węzły muszą zawierać tylko edgenode, a liczba akcji skryptu powinna być równa 1.</span><span class="sxs-lookup"><span data-stu-id="2f459-114">When *ApplicationName* is specified, *PersistOnSuccess* should be set to False, nodes must contain only edgenode, and script action count should equal 1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f459-115">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="2f459-115">-ClusterName</span></span>
<span data-ttu-id="2f459-116">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="2f459-116">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f459-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f459-117">-DefaultProfile</span></span>
<span data-ttu-id="2f459-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="2f459-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f459-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2f459-119">-Name</span></span>
<span data-ttu-id="2f459-120">Określa nazwę akcji skryptu.</span><span class="sxs-lookup"><span data-stu-id="2f459-120">Specifies the name of the script action.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f459-121">-NodeTypes</span><span class="sxs-lookup"><span data-stu-id="2f459-121">-NodeTypes</span></span>
<span data-ttu-id="2f459-122">Określa typy węzłów, na których ma zostać uruchomiona akcja skryptu.</span><span class="sxs-lookup"><span data-stu-id="2f459-122">Specifies the node types on which to run the script action.</span></span>

```yaml
Type: RuntimeScriptActionClusterNodeType[]
Parameter Sets: (All)
Aliases: 
Accepted values: HeadNode, WorkerNode, ZookeeperNode, EdgeNode

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f459-123">— Parametry</span><span class="sxs-lookup"><span data-stu-id="2f459-123">-Parameters</span></span>
<span data-ttu-id="2f459-124">Określa parametry akcji skryptu.</span><span class="sxs-lookup"><span data-stu-id="2f459-124">Specifies the parameters for the script action.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f459-125">-PersistOnSuccess</span><span class="sxs-lookup"><span data-stu-id="2f459-125">-PersistOnSuccess</span></span>
<span data-ttu-id="2f459-126">Wskazuje, że akcja skryptu powinna być uruchamiana za każdym razem, gdy klaster jest skalowany.</span><span class="sxs-lookup"><span data-stu-id="2f459-126">Indicates that the script action should run each time the cluster is scaled up.</span></span>
<span data-ttu-id="2f459-127">Ten parametr przełącznika jest ignorowany, jeśli akcja skryptu jest początkowo niepowodzenie.</span><span class="sxs-lookup"><span data-stu-id="2f459-127">This switch parameter is ignored if the script action initially fails.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f459-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f459-128">-ResourceGroupName</span></span>
<span data-ttu-id="2f459-129">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2f459-129">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f459-130">-URI</span><span class="sxs-lookup"><span data-stu-id="2f459-130">-Uri</span></span>
<span data-ttu-id="2f459-131">Określa publiczny identyfikator URI akcji skryptu (programu PowerShell lub skryptu bash).</span><span class="sxs-lookup"><span data-stu-id="2f459-131">Specifies the public URI for the script action (a PowerShell or Bash script).</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f459-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f459-132">CommonParameters</span></span>
<span data-ttu-id="2f459-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f459-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f459-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f459-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f459-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2f459-135">INPUTS</span></span>

### <span data-ttu-id="2f459-136">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="2f459-136">None</span></span>
<span data-ttu-id="2f459-137">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="2f459-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2f459-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2f459-138">OUTPUTS</span></span>

### <span data-ttu-id="2f459-139">Microsoft. Azure. Commands. HDInsight. models. Management. AzureHDInsightRuntimeScriptActionOperationResource</span><span class="sxs-lookup"><span data-stu-id="2f459-139">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionOperationResource</span></span>

## <span data-ttu-id="2f459-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2f459-140">NOTES</span></span>

## <span data-ttu-id="2f459-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2f459-141">RELATED LINKS</span></span>

[<span data-ttu-id="2f459-142">Dodaj-AzureRmHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="2f459-142">Add-AzureRmHDInsightScriptAction</span></span>](./Add-AzureRmHDInsightScriptAction.md)


