---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/update-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSparkPool.md
ms.openlocfilehash: f8657a8a9b8f4c4c15606e70f632e6ad0b29a33c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991929"
---
# <span data-ttu-id="acc6a-101">Update-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="acc6a-101">Update-AzSynapseSparkPool</span></span>

## <span data-ttu-id="acc6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="acc6a-102">SYNOPSIS</span></span>
<span data-ttu-id="acc6a-103">Aktualizuje pulę przebiegu w czasie analizy Synapse.</span><span class="sxs-lookup"><span data-stu-id="acc6a-103">Updates a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="acc6a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="acc6a-104">SYNTAX</span></span>

### <span data-ttu-id="acc6a-105">SetByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="acc6a-105">SetByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] [-EnableAutoScale <Boolean>] [-AutoScaleMinNodeCount <Int32>]
 [-AutoScaleMaxNodeCount <Int32>] [-EnableAutoPause <Boolean>] [-AutoPauseDelayInMinute <Int32>]
 [-NodeCount <Int32>] [-NodeSize <String>] [-SparkVersion <String>] [-LibraryRequirementsFilePath <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acc6a-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="acc6a-106">SetByParentObjectParameterSet</span></span>
```
Update-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Tag <Hashtable>]
 [-EnableAutoScale <Boolean>] [-AutoScaleMinNodeCount <Int32>] [-AutoScaleMaxNodeCount <Int32>]
 [-EnableAutoPause <Boolean>] [-AutoPauseDelayInMinute <Int32>] [-NodeCount <Int32>] [-NodeSize <String>]
 [-SparkVersion <String>] [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acc6a-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="acc6a-107">SetByInputObjectParameterSet</span></span>
```
Update-AzSynapseSparkPool -InputObject <PSSynapseSparkPool> [-Tag <Hashtable>] [-EnableAutoScale <Boolean>]
 [-AutoScaleMinNodeCount <Int32>] [-AutoScaleMaxNodeCount <Int32>] [-EnableAutoPause <Boolean>]
 [-AutoPauseDelayInMinute <Int32>] [-NodeCount <Int32>] [-NodeSize <String>] [-SparkVersion <String>]
 [-LibraryRequirementsFilePath <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acc6a-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="acc6a-108">SetByResourceIdParameterSet</span></span>
```
Update-AzSynapseSparkPool -ResourceId <String> [-Tag <Hashtable>] [-EnableAutoScale <Boolean>]
 [-AutoScaleMinNodeCount <Int32>] [-AutoScaleMaxNodeCount <Int32>] [-EnableAutoPause <Boolean>]
 [-AutoPauseDelayInMinute <Int32>] [-NodeCount <Int32>] [-NodeSize <String>] [-SparkVersion <String>]
 [-LibraryRequirementsFilePath <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="acc6a-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="acc6a-109">DESCRIPTION</span></span>
<span data-ttu-id="acc6a-110">Polecenie **cmdlet Update-AzSynapseSparkPool** aktualizuje pulę przebiegu w czasie analizy Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="acc6a-110">The **Update-AzSynapseSparkPool** cmdlet updates an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="acc6a-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="acc6a-111">EXAMPLES</span></span>

### <span data-ttu-id="acc6a-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="acc6a-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool -Tag @{"key" = "value"} -NodeCount 5 -NodeSize Medium
```

<span data-ttu-id="acc6a-113">To polecenie aktualizuje pulę przebiegu w czasie analizy Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="acc6a-113">This command updates an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="acc6a-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="acc6a-114">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
$pool | Update-AzSynapseSparkPool -Tag @{"key" = "value1"}
```

<span data-ttu-id="acc6a-115">To polecenie aktualizuje pulę przebiegu w czasie analizy Azure Synapse w potoku.</span><span class="sxs-lookup"><span data-stu-id="acc6a-115">This command updates an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="acc6a-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="acc6a-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseSparkPool -Name ContosoSparkPool -Tag @{"key" = "value2"}
```

<span data-ttu-id="acc6a-117">To polecenie aktualizuje pulę przebiegu w czasie analizy Azure Synapse w potoku.</span><span class="sxs-lookup"><span data-stu-id="acc6a-117">This command updates an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="acc6a-118">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="acc6a-118">Example 4</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/bigDataPools/ContosoSparkPool -Tag @{"key" = "value3"}
```

<span data-ttu-id="acc6a-119">To polecenie aktualizuje pulę przebiegu w czasie analizy Synapse Azure o identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="acc6a-119">This command updates an Azure Synapse Analytics Spark pool with resource ID.</span></span>

### <span data-ttu-id="acc6a-120">Przykład 5</span><span class="sxs-lookup"><span data-stu-id="acc6a-120">Example 5</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoScale $true -AutoScaleMinNodeCount 3 -AutoScaleMaxNodeCount 7
```

<span data-ttu-id="acc6a-121">To polecenie umożliwia automatyczne skalowanie puli przebiegu w czasie analizy Azure Synpsy.</span><span class="sxs-lookup"><span data-stu-id="acc6a-121">This command enables auto-scale for an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="acc6a-122">Przykład 6</span><span class="sxs-lookup"><span data-stu-id="acc6a-122">Example 6</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoScale $false
```

<span data-ttu-id="acc6a-123">To polecenie wyłącza automatyczne skalowanie dla puli przebiegu w czasie usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="acc6a-123">This command disables auto-scale for an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="acc6a-124">Przykład 7</span><span class="sxs-lookup"><span data-stu-id="acc6a-124">Example 7</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoPause $true -AutoPauseDelayInMinute 15
```

<span data-ttu-id="acc6a-125">To polecenie umożliwia automatyczne wstrzymywanie dla puli przebiegu w czasie usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="acc6a-125">This command enables auto-pause for an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="acc6a-126">Przykład 8</span><span class="sxs-lookup"><span data-stu-id="acc6a-126">Example 8</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoPause $false
```

<span data-ttu-id="acc6a-127">To polecenie wyłącza automatyczne wstrzymywanie dla puli przebiegu w czasie analizy Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="acc6a-127">This command disables auto-pause for an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="acc6a-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="acc6a-128">PARAMETERS</span></span>

### <span data-ttu-id="acc6a-129">— AsJob</span><span class="sxs-lookup"><span data-stu-id="acc6a-129">-AsJob</span></span>
<span data-ttu-id="acc6a-130">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="acc6a-130">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="acc6a-131">-AutoPauseDelayInMinute</span><span class="sxs-lookup"><span data-stu-id="acc6a-131">-AutoPauseDelayInMinute</span></span>
<span data-ttu-id="acc6a-132">Liczba minut bezczynności.</span><span class="sxs-lookup"><span data-stu-id="acc6a-132">Number of minutes idle.</span></span> <span data-ttu-id="acc6a-133">Ten parametr musi zostać określony, gdy jest włączona funkcja automatycznego wstrzymywania.</span><span class="sxs-lookup"><span data-stu-id="acc6a-133">This parameter must be specified when Auto-pause is enabled.</span></span>

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

### <span data-ttu-id="acc6a-134">-AutoScaleMaxNodeCount</span><span class="sxs-lookup"><span data-stu-id="acc6a-134">-AutoScaleMaxNodeCount</span></span>
<span data-ttu-id="acc6a-135">Maksymalna liczba węzłów, które mają zostać przydzielone w określonej puli przebiegu w czasie.</span><span class="sxs-lookup"><span data-stu-id="acc6a-135">Maximum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="acc6a-136">Ten parametr musi zostać określony, gdy jest włączona funkcja skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="acc6a-136">This parameter must be specified when Auto-scale is enabled.</span></span>

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

### <span data-ttu-id="acc6a-137">-AutoScaleMinNodeCount</span><span class="sxs-lookup"><span data-stu-id="acc6a-137">-AutoScaleMinNodeCount</span></span>
<span data-ttu-id="acc6a-138">Minimalna liczba węzłów, które mają zostać przydzielone w określonej puli przebiegu w czasie.</span><span class="sxs-lookup"><span data-stu-id="acc6a-138">Minimum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="acc6a-139">Ten parametr musi zostać określony, gdy jest włączona funkcja skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="acc6a-139">This parameter must be specified when Auto-scale is enabled.</span></span>

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

### <span data-ttu-id="acc6a-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acc6a-140">-DefaultProfile</span></span>
<span data-ttu-id="acc6a-141">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="acc6a-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="acc6a-142">-EnableAutoPause</span><span class="sxs-lookup"><span data-stu-id="acc6a-142">-EnableAutoPause</span></span>
<span data-ttu-id="acc6a-143">Wskazuje, czy funkcja automatycznego wstrzymywania powinna być włączona.</span><span class="sxs-lookup"><span data-stu-id="acc6a-143">Indicates whether Auto-pause should be enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acc6a-144">-EnableAutoScale</span><span class="sxs-lookup"><span data-stu-id="acc6a-144">-EnableAutoScale</span></span>
<span data-ttu-id="acc6a-145">Wskazuje, czy należy włączyć automatyczne skalowanie.</span><span class="sxs-lookup"><span data-stu-id="acc6a-145">Indicates whether Auto-scale should be enabled</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acc6a-146">-InputObject</span><span class="sxs-lookup"><span data-stu-id="acc6a-146">-InputObject</span></span>
<span data-ttu-id="acc6a-147">Obiekt wejściowy puli przebiegu w przebiegu w przebiegu, który zwykle przeszedł przez potok.</span><span class="sxs-lookup"><span data-stu-id="acc6a-147">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="acc6a-148">-LibraryRequirementsFilePath</span><span class="sxs-lookup"><span data-stu-id="acc6a-148">-LibraryRequirementsFilePath</span></span>
<span data-ttu-id="acc6a-149">Plik konfiguracji środowiska (plik wyjściowy zawieszania się pliku PIP).</span><span class="sxs-lookup"><span data-stu-id="acc6a-149">Environment configuration file ("PIP freeze" output).</span></span>

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

### <span data-ttu-id="acc6a-150">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="acc6a-150">-Name</span></span>
<span data-ttu-id="acc6a-151">Nazwa puli przebiegu w czasie synpsy.</span><span class="sxs-lookup"><span data-stu-id="acc6a-151">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet, SetByParentObjectParameterSet
Aliases: SparkPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acc6a-152">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="acc6a-152">-NodeCount</span></span>
<span data-ttu-id="acc6a-153">Liczba węzłów do przydzielenia w określonej puli przebiegu w czasie.</span><span class="sxs-lookup"><span data-stu-id="acc6a-153">Number of nodes to be allocated in the specified Spark pool.</span></span>

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

### <span data-ttu-id="acc6a-154">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="acc6a-154">-NodeSize</span></span>
<span data-ttu-id="acc6a-155">Liczba rdzeni i pamięci, które mają być używane dla węzłów przydzielonych do określonej puli przebiegu w czasie.</span><span class="sxs-lookup"><span data-stu-id="acc6a-155">Number of core and memory to be used for nodes allocated in the specified Spark pool.</span></span>
<span data-ttu-id="acc6a-156">Ten parametr musi zostać określony, gdy funkcja automatycznego skalowania jest wyłączona</span><span class="sxs-lookup"><span data-stu-id="acc6a-156">This parameter must be specified when Auto-scale is disabled</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Small, Medium, Large

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acc6a-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acc6a-157">-ResourceGroupName</span></span>
<span data-ttu-id="acc6a-158">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="acc6a-158">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acc6a-159">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="acc6a-159">-ResourceId</span></span>
<span data-ttu-id="acc6a-160">Identyfikator zasobu puli synpsy przebiegu w czasie.</span><span class="sxs-lookup"><span data-stu-id="acc6a-160">Resource identifier of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acc6a-161">— SparkVersion</span><span class="sxs-lookup"><span data-stu-id="acc6a-161">-SparkVersion</span></span>
<span data-ttu-id="acc6a-162">Spark w wersji.</span><span class="sxs-lookup"><span data-stu-id="acc6a-162">Apache Spark version.</span></span>
<span data-ttu-id="acc6a-163">Dozwolone wartości: 2,4</span><span class="sxs-lookup"><span data-stu-id="acc6a-163">Allowed values: 2.4</span></span>

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

### <span data-ttu-id="acc6a-164">— Tag</span><span class="sxs-lookup"><span data-stu-id="acc6a-164">-Tag</span></span>
<span data-ttu-id="acc6a-165">A string,string dictionary of tags associated with the resource.</span><span class="sxs-lookup"><span data-stu-id="acc6a-165">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="acc6a-166">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="acc6a-166">-WorkspaceName</span></span>
<span data-ttu-id="acc6a-167">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="acc6a-167">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acc6a-168">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="acc6a-168">-WorkspaceObject</span></span>
<span data-ttu-id="acc6a-169">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="acc6a-169">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="acc6a-170">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="acc6a-170">-Confirm</span></span>
<span data-ttu-id="acc6a-171">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="acc6a-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="acc6a-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acc6a-172">-WhatIf</span></span>
<span data-ttu-id="acc6a-173">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="acc6a-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="acc6a-174">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="acc6a-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="acc6a-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acc6a-175">CommonParameters</span></span>
<span data-ttu-id="acc6a-176">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acc6a-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acc6a-177">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="acc6a-177">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acc6a-178">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="acc6a-178">INPUTS</span></span>

### <span data-ttu-id="acc6a-179">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="acc6a-179">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="acc6a-180">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="acc6a-180">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="acc6a-181">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="acc6a-181">OUTPUTS</span></span>

### <span data-ttu-id="acc6a-182">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="acc6a-182">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="acc6a-183">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="acc6a-183">NOTES</span></span>

## <span data-ttu-id="acc6a-184">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="acc6a-184">RELATED LINKS</span></span>
