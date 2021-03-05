---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/start-azsynapsesparksession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseSparkSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseSparkSession.md
ms.openlocfilehash: e7e873638e38ed8c0c561fce5c4cd425be7bafbb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992027"
---
# <span data-ttu-id="23087-101">Start-AzSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="23087-101">Start-AzSynapseSparkSession</span></span>

## <span data-ttu-id="23087-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23087-102">SYNOPSIS</span></span>
<span data-ttu-id="23087-103">Rozpoczyna sesję analizy Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="23087-103">Starts a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="23087-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="23087-104">SYNTAX</span></span>

### <span data-ttu-id="23087-105">CreateByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="23087-105">CreateByNameParameterSet (Default)</span></span>
```
Start-AzSynapseSparkSession -WorkspaceName <String> -SparkPoolName <String> [-Language <String>] -Name <String>
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23087-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="23087-106">CreateByParentObjectParameterSet</span></span>
```
Start-AzSynapseSparkSession -SparkPoolObject <PSSynapseSparkPool> [-Language <String>] -Name <String>
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23087-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="23087-107">DESCRIPTION</span></span>
<span data-ttu-id="23087-108">Polecenie **cmdlet Start-AzSynapseSparkSession** uruchamia sesję przebiegu w czasie analizy Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="23087-108">The **Start-AzSynapseSparkSession** cmdlet starts a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="23087-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="23087-109">EXAMPLES</span></span>

### <span data-ttu-id="23087-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="23087-110">Example 1</span></span>
```powershell
PS C:\> Start-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
```

<span data-ttu-id="23087-111">To polecenie uruchamia sesję azure Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="23087-111">This command starts an Azure Synapse Analytics Spark session.</span></span>

### <span data-ttu-id="23087-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="23087-112">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Start-AzSynapseSparkSession -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
```

<span data-ttu-id="23087-113">To polecenie uruchamia sesję azure Synapse Analytics Spark za pośrednictwem potoku.</span><span class="sxs-lookup"><span data-stu-id="23087-113">This command starts an Azure Synapse Analytics Spark session through pipeline.</span></span>

## <span data-ttu-id="23087-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="23087-114">PARAMETERS</span></span>

### <span data-ttu-id="23087-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="23087-115">-AsJob</span></span>
<span data-ttu-id="23087-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="23087-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="23087-117">— Konfiguracja</span><span class="sxs-lookup"><span data-stu-id="23087-117">-Configuration</span></span>
<span data-ttu-id="23087-118">Właściwości konfiguracji przebiegu w przebiegu w sieci.</span><span class="sxs-lookup"><span data-stu-id="23087-118">Spark configuration properties.</span></span>

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

### <span data-ttu-id="23087-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23087-119">-DefaultProfile</span></span>
<span data-ttu-id="23087-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="23087-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23087-121">-ExecutorCount</span><span class="sxs-lookup"><span data-stu-id="23087-121">-ExecutorCount</span></span>
<span data-ttu-id="23087-122">Liczba executorów, którzy mają zostać przydzieleni w określonej puli przebiegu w czasie dla zadania.</span><span class="sxs-lookup"><span data-stu-id="23087-122">Number of executors to be allocated in the specified Spark pool for the job.</span></span>

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

### <span data-ttu-id="23087-123">-ExecutorSize</span><span class="sxs-lookup"><span data-stu-id="23087-123">-ExecutorSize</span></span>
<span data-ttu-id="23087-124">Liczba rdzeni i pamięci, które mają być używane dla executorów przydzielonych do określonej puli przebiegu w czasie dla zadania.</span><span class="sxs-lookup"><span data-stu-id="23087-124">Number of core and memory to be used for executors allocated in the specified Spark pool for the job.</span></span>

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

### <span data-ttu-id="23087-125">— język</span><span class="sxs-lookup"><span data-stu-id="23087-125">-Language</span></span>
<span data-ttu-id="23087-126">Język kodu wykonywania.</span><span class="sxs-lookup"><span data-stu-id="23087-126">Language of the execution code.</span></span>

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

### <span data-ttu-id="23087-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="23087-127">-Name</span></span>
<span data-ttu-id="23087-128">Nazwa sesji przebiegu w przebiegu w trakcie.</span><span class="sxs-lookup"><span data-stu-id="23087-128">Name of Spark session.</span></span>

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

### <span data-ttu-id="23087-129">-ReferenceFile</span><span class="sxs-lookup"><span data-stu-id="23087-129">-ReferenceFile</span></span>
<span data-ttu-id="23087-130">Dodatkowe pliki używane w celach referencyjnych w głównym pliku definicji.</span><span class="sxs-lookup"><span data-stu-id="23087-130">Additional files used for reference in the main definition file.</span></span> <span data-ttu-id="23087-131">Lista URI magazynu rozdzielana przecinkami.</span><span class="sxs-lookup"><span data-stu-id="23087-131">Comma-separated storage URI list.</span></span> <span data-ttu-id="23087-132">np. " abfss://filesystem@account.dfs.core.windows.net/file1.txt , abfss://filesystem@account.dfs.core.windows.net/result/ "</span><span class="sxs-lookup"><span data-stu-id="23087-132">e.g. "abfss://filesystem@account.dfs.core.windows.net/file1.txt,abfss://filesystem@account.dfs.core.windows.net/result/"</span></span>

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

### <span data-ttu-id="23087-133">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="23087-133">-SparkPoolName</span></span>
<span data-ttu-id="23087-134">Nazwa puli przebiegu w czasie synpsy.</span><span class="sxs-lookup"><span data-stu-id="23087-134">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="23087-135">— SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="23087-135">-SparkPoolObject</span></span>
<span data-ttu-id="23087-136">Obiekt wejściowy puli przebiegu w przebiegu w przebiegu, który zwykle przeszedł przez potok.</span><span class="sxs-lookup"><span data-stu-id="23087-136">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="23087-137">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="23087-137">-WorkspaceName</span></span>
<span data-ttu-id="23087-138">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="23087-138">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="23087-139">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="23087-139">-Confirm</span></span>
<span data-ttu-id="23087-140">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="23087-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23087-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23087-141">-WhatIf</span></span>
<span data-ttu-id="23087-142">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23087-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="23087-143">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="23087-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23087-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23087-144">CommonParameters</span></span>
<span data-ttu-id="23087-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23087-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23087-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="23087-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23087-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="23087-147">INPUTS</span></span>

### <span data-ttu-id="23087-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="23087-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="23087-149">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="23087-149">OUTPUTS</span></span>

### <span data-ttu-id="23087-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="23087-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="23087-151">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="23087-151">NOTES</span></span>

## <span data-ttu-id="23087-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="23087-152">RELATED LINKS</span></span>
