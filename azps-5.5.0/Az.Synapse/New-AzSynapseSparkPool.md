---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSparkPool.md
ms.openlocfilehash: c931bff1ba95ee1be185b5fe4dfdc2256d2cafec
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197338"
---
# <span data-ttu-id="94d0a-101">New-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="94d0a-101">New-AzSynapseSparkPool</span></span>

## <span data-ttu-id="94d0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94d0a-102">SYNOPSIS</span></span>
<span data-ttu-id="94d0a-103">Tworzy pulę przebiegu w czasie analizy Synapse.</span><span class="sxs-lookup"><span data-stu-id="94d0a-103">Creates a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="94d0a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="94d0a-104">SYNTAX</span></span>

### <span data-ttu-id="94d0a-105">CreateByNameAndEnableAutoScaleParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="94d0a-105">CreateByNameAndEnableAutoScaleParameterSet (Default)</span></span>
```
New-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Tag <Hashtable>]
 -NodeSize <String> -AutoScaleMinNodeCount <Int32> -AutoScaleMaxNodeCount <Int32> [-EnableAutoPause]
 [-AutoPauseDelayInMinute <Int32>] -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94d0a-106">CreateByNameAndDisableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="94d0a-106">CreateByNameAndDisableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Tag <Hashtable>]
 -NodeCount <Int32> -NodeSize <String> [-EnableAutoPause] [-AutoPauseDelayInMinute <Int32>]
 -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94d0a-107">CreateByParentObjectAndEnableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="94d0a-107">CreateByParentObjectAndEnableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 -NodeSize <String> -AutoScaleMinNodeCount <Int32> -AutoScaleMaxNodeCount <Int32> [-EnableAutoPause]
 [-AutoPauseDelayInMinute <Int32>] -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94d0a-108">CreateByParentObjectAndDisableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="94d0a-108">CreateByParentObjectAndDisableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 -NodeCount <Int32> -NodeSize <String> [-EnableAutoPause] [-AutoPauseDelayInMinute <Int32>]
 -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94d0a-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="94d0a-109">DESCRIPTION</span></span>
<span data-ttu-id="94d0a-110">Polecenie **cmdlet New-AzSynapseSparkPool** tworzy pulę przebiegu w czasie usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="94d0a-110">The **New-AzSynapseSparkPool** cmdlet creates an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="94d0a-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="94d0a-111">EXAMPLES</span></span>

### <span data-ttu-id="94d0a-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="94d0a-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool -NodeCount 3 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="94d0a-113">To polecenie tworzy pulę przebiegu w czasie analizy Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="94d0a-113">This command creates an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="94d0a-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="94d0a-114">Example 2</span></span>
```powershell
PS C:\> New-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool -AutoScaleMinNodeCount 3 -AutoScaleMaxNodeCount 10 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="94d0a-115">To polecenie tworzy pulę przebiegu w czasie analizy Synapse Azure z włączoną automatyczną skalą.</span><span class="sxs-lookup"><span data-stu-id="94d0a-115">This command creates an Azure Synapse Analytics Spark pool with auto-scale enabled.</span></span>

### <span data-ttu-id="94d0a-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="94d0a-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseSparkPool -Name ContosoSparkPool -NodeCount 3 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="94d0a-117">To polecenie tworzy pulę przebiegu w czasie analizy Azure Synapse Analytics za pośrednictwem potoku.</span><span class="sxs-lookup"><span data-stu-id="94d0a-117">This command creates an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="94d0a-118">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="94d0a-118">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseSparkPool -Name ContosoSparkPool -AutoScaleMinNodeCount 3 -AutoScaleMaxNodeCount 10 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="94d0a-119">To polecenie tworzy pulę przebiegu w czasie analizy Synapse Azure z włączoną automatyczną skalą za pośrednictwem potoku.</span><span class="sxs-lookup"><span data-stu-id="94d0a-119">This command creates an Azure Synapse Analytics Spark pool with auto-scale enabled through pipeline.</span></span>

## <span data-ttu-id="94d0a-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94d0a-120">PARAMETERS</span></span>

### <span data-ttu-id="94d0a-121">— AsJob</span><span class="sxs-lookup"><span data-stu-id="94d0a-121">-AsJob</span></span>
<span data-ttu-id="94d0a-122">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="94d0a-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="94d0a-123">-AutoPauseDelayInMinute</span><span class="sxs-lookup"><span data-stu-id="94d0a-123">-AutoPauseDelayInMinute</span></span>
<span data-ttu-id="94d0a-124">Liczba minut bezczynności.</span><span class="sxs-lookup"><span data-stu-id="94d0a-124">Number of minutes idle.</span></span> <span data-ttu-id="94d0a-125">Ten parametr musi zostać określony, gdy jest włączona funkcja automatycznego wstrzymywania.</span><span class="sxs-lookup"><span data-stu-id="94d0a-125">This parameter must be specified when Auto-pause is enabled.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94d0a-126">-AutoScaleMaxNodeCount</span><span class="sxs-lookup"><span data-stu-id="94d0a-126">-AutoScaleMaxNodeCount</span></span>
<span data-ttu-id="94d0a-127">Maksymalna liczba węzłów, które mają zostać przydzielone w określonej puli przebiegu w czasie.</span><span class="sxs-lookup"><span data-stu-id="94d0a-127">Maximum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="94d0a-128">Ten parametr musi zostać określony, gdy jest włączona funkcja skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="94d0a-128">This parameter must be specified when Auto-scale is enabled.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateByNameAndEnableAutoScaleParameterSet, CreateByParentObjectAndEnableAutoScaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94d0a-129">-AutoScaleMinNodeCount</span><span class="sxs-lookup"><span data-stu-id="94d0a-129">-AutoScaleMinNodeCount</span></span>
<span data-ttu-id="94d0a-130">Minimalna liczba węzłów, które mają zostać przydzielone w określonej puli przebiegu w czasie.</span><span class="sxs-lookup"><span data-stu-id="94d0a-130">Minimum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="94d0a-131">Ten parametr musi zostać określony, gdy jest włączona funkcja skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="94d0a-131">This parameter must be specified when Auto-scale is enabled.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateByNameAndEnableAutoScaleParameterSet, CreateByParentObjectAndEnableAutoScaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94d0a-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94d0a-132">-DefaultProfile</span></span>
<span data-ttu-id="94d0a-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="94d0a-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94d0a-134">-EnableAutoPause</span><span class="sxs-lookup"><span data-stu-id="94d0a-134">-EnableAutoPause</span></span>
<span data-ttu-id="94d0a-135">Wskazuje, czy funkcja automatycznego wstrzymywania powinna być włączona.</span><span class="sxs-lookup"><span data-stu-id="94d0a-135">Indicates whether Auto-pause should be enabled.</span></span>

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

### <span data-ttu-id="94d0a-136">-LibraryRequirementsFilePath</span><span class="sxs-lookup"><span data-stu-id="94d0a-136">-LibraryRequirementsFilePath</span></span>
<span data-ttu-id="94d0a-137">Plik konfiguracji środowiska (plik wyjściowy zawieszania się pliku PIP).</span><span class="sxs-lookup"><span data-stu-id="94d0a-137">Environment configuration file ("PIP freeze" output).</span></span>

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

### <span data-ttu-id="94d0a-138">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="94d0a-138">-Name</span></span>
<span data-ttu-id="94d0a-139">Nazwa puli przebiegu w czasie synpsy.</span><span class="sxs-lookup"><span data-stu-id="94d0a-139">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SparkPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94d0a-140">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="94d0a-140">-NodeCount</span></span>
<span data-ttu-id="94d0a-141">Liczba węzłów do przydzielenia w określonej puli przebiegu w czasie.</span><span class="sxs-lookup"><span data-stu-id="94d0a-141">Number of nodes to be allocated in the specified Spark pool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateByNameAndDisableAutoScaleParameterSet, CreateByParentObjectAndDisableAutoScaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94d0a-142">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="94d0a-142">-NodeSize</span></span>
<span data-ttu-id="94d0a-143">Liczba rdzeni i pamięci, które mają być używane dla węzłów przydzielonych do określonej puli przebiegu w czasie.</span><span class="sxs-lookup"><span data-stu-id="94d0a-143">Number of core and memory to be used for nodes allocated in the specified Spark pool.</span></span>
<span data-ttu-id="94d0a-144">Ten parametr musi zostać określony, gdy funkcja automatycznego skalowania jest wyłączona</span><span class="sxs-lookup"><span data-stu-id="94d0a-144">This parameter must be specified when Auto-scale is disabled</span></span>

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

### <span data-ttu-id="94d0a-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94d0a-145">-ResourceGroupName</span></span>
<span data-ttu-id="94d0a-146">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="94d0a-146">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameAndEnableAutoScaleParameterSet, CreateByNameAndDisableAutoScaleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94d0a-147">— SparkVersion</span><span class="sxs-lookup"><span data-stu-id="94d0a-147">-SparkVersion</span></span>
<span data-ttu-id="94d0a-148">Spark w wersji.</span><span class="sxs-lookup"><span data-stu-id="94d0a-148">Apache Spark version.</span></span>
<span data-ttu-id="94d0a-149">Dozwolone wartości: 2,4</span><span class="sxs-lookup"><span data-stu-id="94d0a-149">Allowed values: 2.4</span></span>

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

### <span data-ttu-id="94d0a-150">— Tag</span><span class="sxs-lookup"><span data-stu-id="94d0a-150">-Tag</span></span>
<span data-ttu-id="94d0a-151">A string,string dictionary of tags associated with the resource.</span><span class="sxs-lookup"><span data-stu-id="94d0a-151">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="94d0a-152">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="94d0a-152">-WorkspaceName</span></span>
<span data-ttu-id="94d0a-153">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="94d0a-153">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameAndEnableAutoScaleParameterSet, CreateByNameAndDisableAutoScaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94d0a-154">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="94d0a-154">-WorkspaceObject</span></span>
<span data-ttu-id="94d0a-155">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="94d0a-155">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: CreateByParentObjectAndEnableAutoScaleParameterSet, CreateByParentObjectAndDisableAutoScaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94d0a-156">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="94d0a-156">-Confirm</span></span>
<span data-ttu-id="94d0a-157">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="94d0a-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94d0a-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94d0a-158">-WhatIf</span></span>
<span data-ttu-id="94d0a-159">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94d0a-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94d0a-160">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="94d0a-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94d0a-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94d0a-161">CommonParameters</span></span>
<span data-ttu-id="94d0a-162">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94d0a-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94d0a-163">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="94d0a-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94d0a-164">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="94d0a-164">INPUTS</span></span>

### <span data-ttu-id="94d0a-165">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="94d0a-165">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="94d0a-166">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="94d0a-166">OUTPUTS</span></span>

### <span data-ttu-id="94d0a-167">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="94d0a-167">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="94d0a-168">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="94d0a-168">NOTES</span></span>

## <span data-ttu-id="94d0a-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="94d0a-169">RELATED LINKS</span></span>
