---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/start-azsynapsesparksession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseSparkSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseSparkSession.md
ms.openlocfilehash: b066807d812fc9a74b36b2826cc978589d39ea49
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182658"
---
# <span data-ttu-id="1db70-101">Start-AzSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="1db70-101">Start-AzSynapseSparkSession</span></span>

## <span data-ttu-id="1db70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1db70-102">SYNOPSIS</span></span>
<span data-ttu-id="1db70-103">Rozpoczyna sesję analizy Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="1db70-103">Starts a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="1db70-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1db70-104">SYNTAX</span></span>

### <span data-ttu-id="1db70-105">CreateByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="1db70-105">CreateByNameParameterSet (Default)</span></span>
```
Start-AzSynapseSparkSession -WorkspaceName <String> -SparkPoolName <String> [-Language <String>] -Name <String>
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1db70-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1db70-106">CreateByParentObjectParameterSet</span></span>
```
Start-AzSynapseSparkSession -SparkPoolObject <PSSynapseSparkPool> [-Language <String>] -Name <String>
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1db70-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="1db70-107">DESCRIPTION</span></span>
<span data-ttu-id="1db70-108">Polecenie **cmdlet Start-AzSynapseSparkSession** uruchamia sesję analizy Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="1db70-108">The **Start-AzSynapseSparkSession** cmdlet starts a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="1db70-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1db70-109">EXAMPLES</span></span>

### <span data-ttu-id="1db70-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1db70-110">Example 1</span></span>
```powershell
PS C:\> Start-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
```

<span data-ttu-id="1db70-111">To polecenie uruchamia sesję Azure Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="1db70-111">This command starts an Azure Synapse Analytics Spark session.</span></span>

### <span data-ttu-id="1db70-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="1db70-112">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Start-AzSynapseSparkSession -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
```

<span data-ttu-id="1db70-113">To polecenie uruchamia sesję przebiegu w czasie analizy Azure Synapse Analytics za pośrednictwem potoku.</span><span class="sxs-lookup"><span data-stu-id="1db70-113">This command starts an Azure Synapse Analytics Spark session through pipeline.</span></span>

## <span data-ttu-id="1db70-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1db70-114">PARAMETERS</span></span>

### <span data-ttu-id="1db70-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="1db70-115">-AsJob</span></span>
<span data-ttu-id="1db70-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="1db70-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1db70-117">— Konfiguracja</span><span class="sxs-lookup"><span data-stu-id="1db70-117">-Configuration</span></span>
<span data-ttu-id="1db70-118">Właściwości konfiguracji przebiegu w przebiegu w sieci.</span><span class="sxs-lookup"><span data-stu-id="1db70-118">Spark configuration properties.</span></span>

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

### <span data-ttu-id="1db70-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1db70-119">-DefaultProfile</span></span>
<span data-ttu-id="1db70-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1db70-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1db70-121">-ExecutorCount</span><span class="sxs-lookup"><span data-stu-id="1db70-121">-ExecutorCount</span></span>
<span data-ttu-id="1db70-122">Liczba wykonawców, którzy mają zostać przydzieleni w określonej puli przebiegu w czasie dla zadania.</span><span class="sxs-lookup"><span data-stu-id="1db70-122">Number of executors to be allocated in the specified Spark pool for the job.</span></span>

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

### <span data-ttu-id="1db70-123">-ExecutorSize</span><span class="sxs-lookup"><span data-stu-id="1db70-123">-ExecutorSize</span></span>
<span data-ttu-id="1db70-124">Liczba rdzeni i pamięci, które mają być używane dla executorów przydzielonych do określonej puli przebiegu w czasie dla zadania.</span><span class="sxs-lookup"><span data-stu-id="1db70-124">Number of core and memory to be used for executors allocated in the specified Spark pool for the job.</span></span>

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

### <span data-ttu-id="1db70-125">— język</span><span class="sxs-lookup"><span data-stu-id="1db70-125">-Language</span></span>
<span data-ttu-id="1db70-126">Język kodu wykonywania.</span><span class="sxs-lookup"><span data-stu-id="1db70-126">Language of the execution code.</span></span>

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

### <span data-ttu-id="1db70-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1db70-127">-Name</span></span>
<span data-ttu-id="1db70-128">Nazwa sesji przebiegu w przebiegu w trakcie.</span><span class="sxs-lookup"><span data-stu-id="1db70-128">Name of Spark session.</span></span>

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

### <span data-ttu-id="1db70-129">-ReferenceFile</span><span class="sxs-lookup"><span data-stu-id="1db70-129">-ReferenceFile</span></span>
<span data-ttu-id="1db70-130">Dodatkowe pliki używane w celach referencyjnych w głównym pliku definicji.</span><span class="sxs-lookup"><span data-stu-id="1db70-130">Additional files used for reference in the main definition file.</span></span> <span data-ttu-id="1db70-131">Lista URI magazynu rozdzielana przecinkami.</span><span class="sxs-lookup"><span data-stu-id="1db70-131">Comma-separated storage URI list.</span></span> <span data-ttu-id="1db70-132">np. " abfss://filesystem@account.dfs.core.windows.net/file1.txt , abfss://filesystem@account.dfs.core.windows.net/result/ "</span><span class="sxs-lookup"><span data-stu-id="1db70-132">e.g. "abfss://filesystem@account.dfs.core.windows.net/file1.txt,abfss://filesystem@account.dfs.core.windows.net/result/"</span></span>

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

### <span data-ttu-id="1db70-133">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="1db70-133">-SparkPoolName</span></span>
<span data-ttu-id="1db70-134">Nazwa puli przebiegu w czasie synpsy.</span><span class="sxs-lookup"><span data-stu-id="1db70-134">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="1db70-135">— SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="1db70-135">-SparkPoolObject</span></span>
<span data-ttu-id="1db70-136">Obiekt wejściowy puli przebiegu w przebiegu w przebiegu w uścisce, który zwykle przeszedł przez potok.</span><span class="sxs-lookup"><span data-stu-id="1db70-136">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="1db70-137">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1db70-137">-WorkspaceName</span></span>
<span data-ttu-id="1db70-138">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="1db70-138">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="1db70-139">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1db70-139">-Confirm</span></span>
<span data-ttu-id="1db70-140">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1db70-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1db70-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1db70-141">-WhatIf</span></span>
<span data-ttu-id="1db70-142">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1db70-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1db70-143">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1db70-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1db70-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1db70-144">CommonParameters</span></span>
<span data-ttu-id="1db70-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1db70-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1db70-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1db70-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1db70-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1db70-147">INPUTS</span></span>

### <span data-ttu-id="1db70-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="1db70-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="1db70-149">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1db70-149">OUTPUTS</span></span>

### <span data-ttu-id="1db70-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="1db70-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="1db70-151">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1db70-151">NOTES</span></span>

## <span data-ttu-id="1db70-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1db70-152">RELATED LINKS</span></span>
