---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/start-azsynapsesparksession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseSparkSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseSparkSession.md
ms.openlocfilehash: b066807d812fc9a74b36b2826cc978589d39ea49
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383145"
---
# <span data-ttu-id="d7ac3-101">Start-AzSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="d7ac3-101">Start-AzSynapseSparkSession</span></span>

## <span data-ttu-id="d7ac3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d7ac3-102">SYNOPSIS</span></span>
<span data-ttu-id="d7ac3-103">Rozpoczyna sesję Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="d7ac3-103">Starts a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="d7ac3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d7ac3-104">SYNTAX</span></span>

### <span data-ttu-id="d7ac3-105">CreateByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d7ac3-105">CreateByNameParameterSet (Default)</span></span>
```
Start-AzSynapseSparkSession -WorkspaceName <String> -SparkPoolName <String> [-Language <String>] -Name <String>
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7ac3-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7ac3-106">CreateByParentObjectParameterSet</span></span>
```
Start-AzSynapseSparkSession -SparkPoolObject <PSSynapseSparkPool> [-Language <String>] -Name <String>
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7ac3-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d7ac3-107">DESCRIPTION</span></span>
<span data-ttu-id="d7ac3-108">Polecenie cmdlet **Start-AzSynapseSparkSession** rozpoczyna sesję usługi Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="d7ac3-108">The **Start-AzSynapseSparkSession** cmdlet starts a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="d7ac3-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d7ac3-109">EXAMPLES</span></span>

### <span data-ttu-id="d7ac3-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d7ac3-110">Example 1</span></span>
```powershell
PS C:\> Start-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
```

<span data-ttu-id="d7ac3-111">To polecenie uruchamia sesję usługi Azure Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="d7ac3-111">This command starts an Azure Synapse Analytics Spark session.</span></span>

### <span data-ttu-id="d7ac3-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d7ac3-112">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Start-AzSynapseSparkSession -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
```

<span data-ttu-id="d7ac3-113">To polecenie uruchamia sesję usługi Azure Synapse Analytics Spark za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="d7ac3-113">This command starts an Azure Synapse Analytics Spark session through pipeline.</span></span>

## <span data-ttu-id="d7ac3-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d7ac3-114">PARAMETERS</span></span>

### <span data-ttu-id="d7ac3-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d7ac3-115">-AsJob</span></span>
<span data-ttu-id="d7ac3-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d7ac3-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7ac3-117">— Konfiguracja</span><span class="sxs-lookup"><span data-stu-id="d7ac3-117">-Configuration</span></span>
<span data-ttu-id="d7ac3-118">Właściwości konfiguracji platformy Spark.</span><span class="sxs-lookup"><span data-stu-id="d7ac3-118">Spark configuration properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7ac3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7ac3-119">-DefaultProfile</span></span>
<span data-ttu-id="d7ac3-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d7ac3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7ac3-121">-ExecutorCount</span><span class="sxs-lookup"><span data-stu-id="d7ac3-121">-ExecutorCount</span></span>
<span data-ttu-id="d7ac3-122">Liczba wykonawców, które mają zostać przydzielone w określonej puli platformy Spark dla zadania.</span><span class="sxs-lookup"><span data-stu-id="d7ac3-122">Number of executors to be allocated in the specified Spark pool for the job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7ac3-123">-ExecutorSize</span><span class="sxs-lookup"><span data-stu-id="d7ac3-123">-ExecutorSize</span></span>
<span data-ttu-id="d7ac3-124">Liczba podstawowych i pamięci, które mają być używane w przypadku modułów wykonujących zadania, przydzielonych w określonej puli platformy Spark.</span><span class="sxs-lookup"><span data-stu-id="d7ac3-124">Number of core and memory to be used for executors allocated in the specified Spark pool for the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Small, Medium, Large

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7ac3-125">-Language</span><span class="sxs-lookup"><span data-stu-id="d7ac3-125">-Language</span></span>
<span data-ttu-id="d7ac3-126">Język kodu wykonania.</span><span class="sxs-lookup"><span data-stu-id="d7ac3-126">Language of the execution code.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Spark, Scala, PySpark, Python, SparkDotNet, CSharp, SQL

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7ac3-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d7ac3-127">-Name</span></span>
<span data-ttu-id="d7ac3-128">Nazwa sesji usługi Spark.</span><span class="sxs-lookup"><span data-stu-id="d7ac3-128">Name of Spark session.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7ac3-129">-ReferenceFile</span><span class="sxs-lookup"><span data-stu-id="d7ac3-129">-ReferenceFile</span></span>
<span data-ttu-id="d7ac3-130">Dodatkowe pliki używane w celu odwołania w pliku definicji głównej.</span><span class="sxs-lookup"><span data-stu-id="d7ac3-130">Additional files used for reference in the main definition file.</span></span> <span data-ttu-id="d7ac3-131">Lista identyfikatorów URI magazynu rozdzielonych przecinkami.</span><span class="sxs-lookup"><span data-stu-id="d7ac3-131">Comma-separated storage URI list.</span></span> <span data-ttu-id="d7ac3-132">na przykład " abfss://filesystem@account.dfs.core.windows.net/file1.txt , abfss://filesystem@account.dfs.core.windows.net/result/ "</span><span class="sxs-lookup"><span data-stu-id="d7ac3-132">e.g. "abfss://filesystem@account.dfs.core.windows.net/file1.txt,abfss://filesystem@account.dfs.core.windows.net/result/"</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7ac3-133">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="d7ac3-133">-SparkPoolName</span></span>
<span data-ttu-id="d7ac3-134">Nazwa puli Synapse Spark.</span><span class="sxs-lookup"><span data-stu-id="d7ac3-134">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7ac3-135">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="d7ac3-135">-SparkPoolObject</span></span>
<span data-ttu-id="d7ac3-136">Obiekt wejściowy usługi Spark Pool, zazwyczaj przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="d7ac3-136">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7ac3-137">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="d7ac3-137">-WorkspaceName</span></span>
<span data-ttu-id="d7ac3-138">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="d7ac3-138">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7ac3-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d7ac3-139">-Confirm</span></span>
<span data-ttu-id="d7ac3-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7ac3-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7ac3-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7ac3-141">-WhatIf</span></span>
<span data-ttu-id="d7ac3-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7ac3-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d7ac3-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d7ac3-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7ac3-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7ac3-144">CommonParameters</span></span>
<span data-ttu-id="d7ac3-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7ac3-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7ac3-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d7ac3-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7ac3-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d7ac3-147">INPUTS</span></span>

### <span data-ttu-id="d7ac3-148">Microsoft. Azure. Commands. Synapse. models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="d7ac3-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="d7ac3-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d7ac3-149">OUTPUTS</span></span>

### <span data-ttu-id="d7ac3-150">Microsoft. Azure. Commands. Synapse. models. PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="d7ac3-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="d7ac3-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d7ac3-151">NOTES</span></span>

## <span data-ttu-id="d7ac3-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d7ac3-152">RELATED LINKS</span></span>
