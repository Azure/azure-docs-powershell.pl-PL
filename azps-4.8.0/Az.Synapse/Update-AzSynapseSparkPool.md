---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSparkPool.md
ms.openlocfilehash: 1ed539f6064d6f99aff632a43cee5f200d735b6d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94061927"
---
# <span data-ttu-id="1d769-101">Update-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="1d769-101">Update-AzSynapseSparkPool</span></span>

## <span data-ttu-id="1d769-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1d769-102">SYNOPSIS</span></span>
<span data-ttu-id="1d769-103">Umożliwia zaktualizowanie puli Synapse analiz Spark.</span><span class="sxs-lookup"><span data-stu-id="1d769-103">Updates a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="1d769-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1d769-104">SYNTAX</span></span>

### <span data-ttu-id="1d769-105">SetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1d769-105">SetByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] [-EnableAutoScale <Boolean>] [-AutoScaleMinNodeCount <Int32>]
 [-AutoScaleMaxNodeCount <Int32>] [-EnableAutoPause <Boolean>] [-AutoPauseDelayInMinute <Int32>]
 [-NodeCount <Int32>] [-NodeSize <String>] [-SparkVersion <String>] [-LibraryRequirementsFilePath <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d769-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d769-106">SetByParentObjectParameterSet</span></span>
```
Update-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Tag <Hashtable>]
 [-EnableAutoScale <Boolean>] [-AutoScaleMinNodeCount <Int32>] [-AutoScaleMaxNodeCount <Int32>]
 [-EnableAutoPause <Boolean>] [-AutoPauseDelayInMinute <Int32>] [-NodeCount <Int32>] [-NodeSize <String>]
 [-SparkVersion <String>] [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d769-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d769-107">SetByInputObjectParameterSet</span></span>
```
Update-AzSynapseSparkPool -InputObject <PSSynapseSparkPool> [-Tag <Hashtable>] [-EnableAutoScale <Boolean>]
 [-AutoScaleMinNodeCount <Int32>] [-AutoScaleMaxNodeCount <Int32>] [-EnableAutoPause <Boolean>]
 [-AutoPauseDelayInMinute <Int32>] [-NodeCount <Int32>] [-NodeSize <String>] [-SparkVersion <String>]
 [-LibraryRequirementsFilePath <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d769-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d769-108">SetByResourceIdParameterSet</span></span>
```
Update-AzSynapseSparkPool -ResourceId <String> [-Tag <Hashtable>] [-EnableAutoScale <Boolean>]
 [-AutoScaleMinNodeCount <Int32>] [-AutoScaleMaxNodeCount <Int32>] [-EnableAutoPause <Boolean>]
 [-AutoPauseDelayInMinute <Int32>] [-NodeCount <Int32>] [-NodeSize <String>] [-SparkVersion <String>]
 [-LibraryRequirementsFilePath <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d769-109">Opis</span><span class="sxs-lookup"><span data-stu-id="1d769-109">DESCRIPTION</span></span>
<span data-ttu-id="1d769-110">Polecenie cmdlet **Update-AzSynapseSparkPool** aktualizuje pulę platformy Azure Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="1d769-110">The **Update-AzSynapseSparkPool** cmdlet updates an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="1d769-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1d769-111">EXAMPLES</span></span>

### <span data-ttu-id="1d769-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1d769-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool -Tag @{"key" = "value"} -NodeCount 5 -NodeSize Medium
```

<span data-ttu-id="1d769-113">To polecenie aktualizuje pulę platformy Azure Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="1d769-113">This command updates an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="1d769-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="1d769-114">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
$pool | Update-AzSynapseSparkPool -Tag @{"key" = "value1"}
```

<span data-ttu-id="1d769-115">To polecenie aktualizuje pulę usługi Azure Synapse Analytics Spark za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="1d769-115">This command updates an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="1d769-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="1d769-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseSparkPool -Name ContosoSparkPool -Tag @{"key" = "value2"}
```

<span data-ttu-id="1d769-117">To polecenie aktualizuje pulę usługi Azure Synapse Analytics Spark za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="1d769-117">This command updates an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="1d769-118">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="1d769-118">Example 4</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/bigDataPools/ContosoSparkPool -Tag @{"key" = "value3"}
```

<span data-ttu-id="1d769-119">To polecenie aktualizuje pulę usługi Azure Synapse Analytics Spark z IDENTYFIKATORem zasobu.</span><span class="sxs-lookup"><span data-stu-id="1d769-119">This command updates an Azure Synapse Analytics Spark pool with resource ID.</span></span>

### <span data-ttu-id="1d769-120">Przykład 5</span><span class="sxs-lookup"><span data-stu-id="1d769-120">Example 5</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoScale $true -AutoScaleMinNodeCount 3 -AutoScaleMaxNodeCount 7
```

<span data-ttu-id="1d769-121">To polecenie umożliwia automatyczną skalowanie puli platformy Azure Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="1d769-121">This command enables auto-scale for an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="1d769-122">Przykład 6</span><span class="sxs-lookup"><span data-stu-id="1d769-122">Example 6</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoScale $false
```

<span data-ttu-id="1d769-123">To polecenie wyłącza automatyczną skalowanie puli platformy Azure Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="1d769-123">This command disables auto-scale for an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="1d769-124">Przykład 7</span><span class="sxs-lookup"><span data-stu-id="1d769-124">Example 7</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoPause $true -AutoPauseDelayInMinute 15
```

<span data-ttu-id="1d769-125">To polecenie umożliwia automatyczne wstrzymanie puli platformy Azure Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="1d769-125">This command enables auto-pause for an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="1d769-126">Przykład 8</span><span class="sxs-lookup"><span data-stu-id="1d769-126">Example 8</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoPause $false
```

<span data-ttu-id="1d769-127">To polecenie wyłącza automatyczne wstrzymywanie puli platformy Azure Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="1d769-127">This command disables auto-pause for an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="1d769-128">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1d769-128">PARAMETERS</span></span>

### <span data-ttu-id="1d769-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1d769-129">-AsJob</span></span>
<span data-ttu-id="1d769-130">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="1d769-130">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1d769-131">-AutoPauseDelayInMinute</span><span class="sxs-lookup"><span data-stu-id="1d769-131">-AutoPauseDelayInMinute</span></span>
<span data-ttu-id="1d769-132">Liczba minut bezczynności.</span><span class="sxs-lookup"><span data-stu-id="1d769-132">Number of minutes idle.</span></span> <span data-ttu-id="1d769-133">Ten parametr należy określić, gdy funkcja automatycznego wstrzymywania jest włączona.</span><span class="sxs-lookup"><span data-stu-id="1d769-133">This parameter must be specified when Auto-pause is enabled.</span></span>

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

### <span data-ttu-id="1d769-134">-AutoScaleMaxNodeCount</span><span class="sxs-lookup"><span data-stu-id="1d769-134">-AutoScaleMaxNodeCount</span></span>
<span data-ttu-id="1d769-135">Maksymalna liczba węzłów do przydzielenia w określonej puli platformy Spark.</span><span class="sxs-lookup"><span data-stu-id="1d769-135">Maximum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="1d769-136">Ten parametr należy określić, gdy funkcja automatycznego skalowania jest włączona.</span><span class="sxs-lookup"><span data-stu-id="1d769-136">This parameter must be specified when Auto-scale is enabled.</span></span>

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

### <span data-ttu-id="1d769-137">-AutoScaleMinNodeCount</span><span class="sxs-lookup"><span data-stu-id="1d769-137">-AutoScaleMinNodeCount</span></span>
<span data-ttu-id="1d769-138">Minimalna liczba węzłów do przydzielenia w określonej puli platformy Spark.</span><span class="sxs-lookup"><span data-stu-id="1d769-138">Minimum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="1d769-139">Ten parametr należy określić, gdy funkcja automatycznego skalowania jest włączona.</span><span class="sxs-lookup"><span data-stu-id="1d769-139">This parameter must be specified when Auto-scale is enabled.</span></span>

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

### <span data-ttu-id="1d769-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d769-140">-DefaultProfile</span></span>
<span data-ttu-id="1d769-141">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1d769-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d769-142">-EnableAutoPause</span><span class="sxs-lookup"><span data-stu-id="1d769-142">-EnableAutoPause</span></span>
<span data-ttu-id="1d769-143">Wskazuje, czy funkcja automatycznego wstrzymywania ma być włączona.</span><span class="sxs-lookup"><span data-stu-id="1d769-143">Indicates whether Auto-pause should be enabled.</span></span>

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

### <span data-ttu-id="1d769-144">-EnableAutoScale</span><span class="sxs-lookup"><span data-stu-id="1d769-144">-EnableAutoScale</span></span>
<span data-ttu-id="1d769-145">Wskazuje, czy funkcja automatycznej skali ma być włączona</span><span class="sxs-lookup"><span data-stu-id="1d769-145">Indicates whether Auto-scale should be enabled</span></span>

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

### <span data-ttu-id="1d769-146">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1d769-146">-InputObject</span></span>
<span data-ttu-id="1d769-147">Obiekt wejściowy usługi Spark Pool, zazwyczaj przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="1d769-147">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="1d769-148">-LibraryRequirementsFilePath</span><span class="sxs-lookup"><span data-stu-id="1d769-148">-LibraryRequirementsFilePath</span></span>
<span data-ttu-id="1d769-149">Plik konfiguracji środowiska ("PIP Zablokuj").</span><span class="sxs-lookup"><span data-stu-id="1d769-149">Environment configuration file ("PIP freeze" output).</span></span>

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

### <span data-ttu-id="1d769-150">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1d769-150">-Name</span></span>
<span data-ttu-id="1d769-151">Nazwa puli Synapse Spark.</span><span class="sxs-lookup"><span data-stu-id="1d769-151">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="1d769-152">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="1d769-152">-NodeCount</span></span>
<span data-ttu-id="1d769-153">Liczba węzłów do przydzielenia w określonej puli platformy Spark.</span><span class="sxs-lookup"><span data-stu-id="1d769-153">Number of nodes to be allocated in the specified Spark pool.</span></span>

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

### <span data-ttu-id="1d769-154">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="1d769-154">-NodeSize</span></span>
<span data-ttu-id="1d769-155">Liczba nośników podstawowych i pamięci, które mają być używane dla węzłów przydzielonych w określonej puli platformy Spark.</span><span class="sxs-lookup"><span data-stu-id="1d769-155">Number of core and memory to be used for nodes allocated in the specified Spark pool.</span></span>
<span data-ttu-id="1d769-156">Ten parametr należy określić, gdy funkcja automatycznego skalowania jest wyłączona</span><span class="sxs-lookup"><span data-stu-id="1d769-156">This parameter must be specified when Auto-scale is disabled</span></span>

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

### <span data-ttu-id="1d769-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d769-157">-ResourceGroupName</span></span>
<span data-ttu-id="1d769-158">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1d769-158">Resource group name.</span></span>

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

### <span data-ttu-id="1d769-159">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1d769-159">-ResourceId</span></span>
<span data-ttu-id="1d769-160">Identyfikator zasobu puli usługi Synapse Spark.</span><span class="sxs-lookup"><span data-stu-id="1d769-160">Resource identifier of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="1d769-161">-SparkVersion</span><span class="sxs-lookup"><span data-stu-id="1d769-161">-SparkVersion</span></span>
<span data-ttu-id="1d769-162">Wersja oprogramowania Apache Spark.</span><span class="sxs-lookup"><span data-stu-id="1d769-162">Apache Spark version.</span></span>
<span data-ttu-id="1d769-163">Dozwolone wartości: 2,4</span><span class="sxs-lookup"><span data-stu-id="1d769-163">Allowed values: 2.4</span></span>

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

### <span data-ttu-id="1d769-164">-Tag</span><span class="sxs-lookup"><span data-stu-id="1d769-164">-Tag</span></span>
<span data-ttu-id="1d769-165">Ciąg znaków, który jest ciągiem znaczników skojarzonych z zasobem.</span><span class="sxs-lookup"><span data-stu-id="1d769-165">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="1d769-166">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="1d769-166">-WorkspaceName</span></span>
<span data-ttu-id="1d769-167">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="1d769-167">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="1d769-168">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="1d769-168">-WorkspaceObject</span></span>
<span data-ttu-id="1d769-169">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="1d769-169">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="1d769-170">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1d769-170">-Confirm</span></span>
<span data-ttu-id="1d769-171">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d769-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d769-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d769-172">-WhatIf</span></span>
<span data-ttu-id="1d769-173">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d769-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d769-174">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1d769-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d769-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d769-175">CommonParameters</span></span>
<span data-ttu-id="1d769-176">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d769-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d769-177">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1d769-177">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d769-178">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1d769-178">INPUTS</span></span>

### <span data-ttu-id="1d769-179">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="1d769-179">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="1d769-180">Microsoft. Azure. Commands. Synapse. models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="1d769-180">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="1d769-181">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1d769-181">OUTPUTS</span></span>

### <span data-ttu-id="1d769-182">Microsoft. Azure. Commands. Synapse. models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="1d769-182">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="1d769-183">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1d769-183">NOTES</span></span>

## <span data-ttu-id="1d769-184">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1d769-184">RELATED LINKS</span></span>
