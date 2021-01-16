---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSparkPool.md
ms.openlocfilehash: 1ed539f6064d6f99aff632a43cee5f200d735b6d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356341"
---
# <span data-ttu-id="f80ef-101">Update-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="f80ef-101">Update-AzSynapseSparkPool</span></span>

## <span data-ttu-id="f80ef-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f80ef-102">SYNOPSIS</span></span>
<span data-ttu-id="f80ef-103">Umożliwia zaktualizowanie puli Synapse analiz Spark.</span><span class="sxs-lookup"><span data-stu-id="f80ef-103">Updates a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="f80ef-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f80ef-104">SYNTAX</span></span>

### <span data-ttu-id="f80ef-105">SetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f80ef-105">SetByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] [-EnableAutoScale <Boolean>] [-AutoScaleMinNodeCount <Int32>]
 [-AutoScaleMaxNodeCount <Int32>] [-EnableAutoPause <Boolean>] [-AutoPauseDelayInMinute <Int32>]
 [-NodeCount <Int32>] [-NodeSize <String>] [-SparkVersion <String>] [-LibraryRequirementsFilePath <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f80ef-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f80ef-106">SetByParentObjectParameterSet</span></span>
```
Update-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Tag <Hashtable>]
 [-EnableAutoScale <Boolean>] [-AutoScaleMinNodeCount <Int32>] [-AutoScaleMaxNodeCount <Int32>]
 [-EnableAutoPause <Boolean>] [-AutoPauseDelayInMinute <Int32>] [-NodeCount <Int32>] [-NodeSize <String>]
 [-SparkVersion <String>] [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f80ef-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f80ef-107">SetByInputObjectParameterSet</span></span>
```
Update-AzSynapseSparkPool -InputObject <PSSynapseSparkPool> [-Tag <Hashtable>] [-EnableAutoScale <Boolean>]
 [-AutoScaleMinNodeCount <Int32>] [-AutoScaleMaxNodeCount <Int32>] [-EnableAutoPause <Boolean>]
 [-AutoPauseDelayInMinute <Int32>] [-NodeCount <Int32>] [-NodeSize <String>] [-SparkVersion <String>]
 [-LibraryRequirementsFilePath <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f80ef-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f80ef-108">SetByResourceIdParameterSet</span></span>
```
Update-AzSynapseSparkPool -ResourceId <String> [-Tag <Hashtable>] [-EnableAutoScale <Boolean>]
 [-AutoScaleMinNodeCount <Int32>] [-AutoScaleMaxNodeCount <Int32>] [-EnableAutoPause <Boolean>]
 [-AutoPauseDelayInMinute <Int32>] [-NodeCount <Int32>] [-NodeSize <String>] [-SparkVersion <String>]
 [-LibraryRequirementsFilePath <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f80ef-109">Opis</span><span class="sxs-lookup"><span data-stu-id="f80ef-109">DESCRIPTION</span></span>
<span data-ttu-id="f80ef-110">Polecenie cmdlet **Update-AzSynapseSparkPool** aktualizuje pulę platformy Azure Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="f80ef-110">The **Update-AzSynapseSparkPool** cmdlet updates an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="f80ef-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f80ef-111">EXAMPLES</span></span>

### <span data-ttu-id="f80ef-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f80ef-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool -Tag @{"key" = "value"} -NodeCount 5 -NodeSize Medium
```

<span data-ttu-id="f80ef-113">To polecenie aktualizuje pulę platformy Azure Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="f80ef-113">This command updates an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="f80ef-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f80ef-114">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
$pool | Update-AzSynapseSparkPool -Tag @{"key" = "value1"}
```

<span data-ttu-id="f80ef-115">To polecenie aktualizuje pulę usługi Azure Synapse Analytics Spark za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="f80ef-115">This command updates an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="f80ef-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="f80ef-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseSparkPool -Name ContosoSparkPool -Tag @{"key" = "value2"}
```

<span data-ttu-id="f80ef-117">To polecenie aktualizuje pulę usługi Azure Synapse Analytics Spark za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="f80ef-117">This command updates an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="f80ef-118">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="f80ef-118">Example 4</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/bigDataPools/ContosoSparkPool -Tag @{"key" = "value3"}
```

<span data-ttu-id="f80ef-119">To polecenie aktualizuje pulę usługi Azure Synapse Analytics Spark z IDENTYFIKATORem zasobu.</span><span class="sxs-lookup"><span data-stu-id="f80ef-119">This command updates an Azure Synapse Analytics Spark pool with resource ID.</span></span>

### <span data-ttu-id="f80ef-120">Przykład 5</span><span class="sxs-lookup"><span data-stu-id="f80ef-120">Example 5</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoScale $true -AutoScaleMinNodeCount 3 -AutoScaleMaxNodeCount 7
```

<span data-ttu-id="f80ef-121">To polecenie umożliwia automatyczną skalowanie puli platformy Azure Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="f80ef-121">This command enables auto-scale for an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="f80ef-122">Przykład 6</span><span class="sxs-lookup"><span data-stu-id="f80ef-122">Example 6</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoScale $false
```

<span data-ttu-id="f80ef-123">To polecenie wyłącza automatyczną skalowanie puli platformy Azure Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="f80ef-123">This command disables auto-scale for an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="f80ef-124">Przykład 7</span><span class="sxs-lookup"><span data-stu-id="f80ef-124">Example 7</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoPause $true -AutoPauseDelayInMinute 15
```

<span data-ttu-id="f80ef-125">To polecenie umożliwia automatyczne wstrzymanie puli platformy Azure Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="f80ef-125">This command enables auto-pause for an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="f80ef-126">Przykład 8</span><span class="sxs-lookup"><span data-stu-id="f80ef-126">Example 8</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoPause $false
```

<span data-ttu-id="f80ef-127">To polecenie wyłącza automatyczne wstrzymywanie puli platformy Azure Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="f80ef-127">This command disables auto-pause for an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="f80ef-128">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f80ef-128">PARAMETERS</span></span>

### <span data-ttu-id="f80ef-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f80ef-129">-AsJob</span></span>
<span data-ttu-id="f80ef-130">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f80ef-130">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f80ef-131">-AutoPauseDelayInMinute</span><span class="sxs-lookup"><span data-stu-id="f80ef-131">-AutoPauseDelayInMinute</span></span>
<span data-ttu-id="f80ef-132">Liczba minut bezczynności.</span><span class="sxs-lookup"><span data-stu-id="f80ef-132">Number of minutes idle.</span></span> <span data-ttu-id="f80ef-133">Ten parametr należy określić, gdy funkcja automatycznego wstrzymywania jest włączona.</span><span class="sxs-lookup"><span data-stu-id="f80ef-133">This parameter must be specified when Auto-pause is enabled.</span></span>

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

### <span data-ttu-id="f80ef-134">-AutoScaleMaxNodeCount</span><span class="sxs-lookup"><span data-stu-id="f80ef-134">-AutoScaleMaxNodeCount</span></span>
<span data-ttu-id="f80ef-135">Maksymalna liczba węzłów do przydzielenia w określonej puli platformy Spark.</span><span class="sxs-lookup"><span data-stu-id="f80ef-135">Maximum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="f80ef-136">Ten parametr należy określić, gdy funkcja automatycznego skalowania jest włączona.</span><span class="sxs-lookup"><span data-stu-id="f80ef-136">This parameter must be specified when Auto-scale is enabled.</span></span>

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

### <span data-ttu-id="f80ef-137">-AutoScaleMinNodeCount</span><span class="sxs-lookup"><span data-stu-id="f80ef-137">-AutoScaleMinNodeCount</span></span>
<span data-ttu-id="f80ef-138">Minimalna liczba węzłów do przydzielenia w określonej puli platformy Spark.</span><span class="sxs-lookup"><span data-stu-id="f80ef-138">Minimum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="f80ef-139">Ten parametr należy określić, gdy funkcja automatycznego skalowania jest włączona.</span><span class="sxs-lookup"><span data-stu-id="f80ef-139">This parameter must be specified when Auto-scale is enabled.</span></span>

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

### <span data-ttu-id="f80ef-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f80ef-140">-DefaultProfile</span></span>
<span data-ttu-id="f80ef-141">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f80ef-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f80ef-142">-EnableAutoPause</span><span class="sxs-lookup"><span data-stu-id="f80ef-142">-EnableAutoPause</span></span>
<span data-ttu-id="f80ef-143">Wskazuje, czy funkcja automatycznego wstrzymywania ma być włączona.</span><span class="sxs-lookup"><span data-stu-id="f80ef-143">Indicates whether Auto-pause should be enabled.</span></span>

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

### <span data-ttu-id="f80ef-144">-EnableAutoScale</span><span class="sxs-lookup"><span data-stu-id="f80ef-144">-EnableAutoScale</span></span>
<span data-ttu-id="f80ef-145">Wskazuje, czy funkcja automatycznej skali ma być włączona</span><span class="sxs-lookup"><span data-stu-id="f80ef-145">Indicates whether Auto-scale should be enabled</span></span>

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

### <span data-ttu-id="f80ef-146">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f80ef-146">-InputObject</span></span>
<span data-ttu-id="f80ef-147">Obiekt wejściowy usługi Spark Pool, zazwyczaj przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="f80ef-147">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="f80ef-148">-LibraryRequirementsFilePath</span><span class="sxs-lookup"><span data-stu-id="f80ef-148">-LibraryRequirementsFilePath</span></span>
<span data-ttu-id="f80ef-149">Plik konfiguracji środowiska ("PIP Zablokuj").</span><span class="sxs-lookup"><span data-stu-id="f80ef-149">Environment configuration file ("PIP freeze" output).</span></span>

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

### <span data-ttu-id="f80ef-150">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f80ef-150">-Name</span></span>
<span data-ttu-id="f80ef-151">Nazwa puli Synapse Spark.</span><span class="sxs-lookup"><span data-stu-id="f80ef-151">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="f80ef-152">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="f80ef-152">-NodeCount</span></span>
<span data-ttu-id="f80ef-153">Liczba węzłów do przydzielenia w określonej puli platformy Spark.</span><span class="sxs-lookup"><span data-stu-id="f80ef-153">Number of nodes to be allocated in the specified Spark pool.</span></span>

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

### <span data-ttu-id="f80ef-154">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="f80ef-154">-NodeSize</span></span>
<span data-ttu-id="f80ef-155">Liczba nośników podstawowych i pamięci, które mają być używane dla węzłów przydzielonych w określonej puli platformy Spark.</span><span class="sxs-lookup"><span data-stu-id="f80ef-155">Number of core and memory to be used for nodes allocated in the specified Spark pool.</span></span>
<span data-ttu-id="f80ef-156">Ten parametr należy określić, gdy funkcja automatycznego skalowania jest wyłączona</span><span class="sxs-lookup"><span data-stu-id="f80ef-156">This parameter must be specified when Auto-scale is disabled</span></span>

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

### <span data-ttu-id="f80ef-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f80ef-157">-ResourceGroupName</span></span>
<span data-ttu-id="f80ef-158">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f80ef-158">Resource group name.</span></span>

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

### <span data-ttu-id="f80ef-159">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f80ef-159">-ResourceId</span></span>
<span data-ttu-id="f80ef-160">Identyfikator zasobu puli usługi Synapse Spark.</span><span class="sxs-lookup"><span data-stu-id="f80ef-160">Resource identifier of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="f80ef-161">-SparkVersion</span><span class="sxs-lookup"><span data-stu-id="f80ef-161">-SparkVersion</span></span>
<span data-ttu-id="f80ef-162">Wersja oprogramowania Apache Spark.</span><span class="sxs-lookup"><span data-stu-id="f80ef-162">Apache Spark version.</span></span>
<span data-ttu-id="f80ef-163">Dozwolone wartości: 2,4</span><span class="sxs-lookup"><span data-stu-id="f80ef-163">Allowed values: 2.4</span></span>

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

### <span data-ttu-id="f80ef-164">-Tag</span><span class="sxs-lookup"><span data-stu-id="f80ef-164">-Tag</span></span>
<span data-ttu-id="f80ef-165">Ciąg znaków, który jest ciągiem znaczników skojarzonych z zasobem.</span><span class="sxs-lookup"><span data-stu-id="f80ef-165">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="f80ef-166">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="f80ef-166">-WorkspaceName</span></span>
<span data-ttu-id="f80ef-167">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="f80ef-167">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="f80ef-168">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="f80ef-168">-WorkspaceObject</span></span>
<span data-ttu-id="f80ef-169">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="f80ef-169">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="f80ef-170">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f80ef-170">-Confirm</span></span>
<span data-ttu-id="f80ef-171">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f80ef-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f80ef-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f80ef-172">-WhatIf</span></span>
<span data-ttu-id="f80ef-173">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f80ef-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f80ef-174">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f80ef-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f80ef-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f80ef-175">CommonParameters</span></span>
<span data-ttu-id="f80ef-176">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f80ef-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f80ef-177">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f80ef-177">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f80ef-178">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f80ef-178">INPUTS</span></span>

### <span data-ttu-id="f80ef-179">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f80ef-179">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="f80ef-180">Microsoft. Azure. Commands. Synapse. models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="f80ef-180">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="f80ef-181">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f80ef-181">OUTPUTS</span></span>

### <span data-ttu-id="f80ef-182">Microsoft. Azure. Commands. Synapse. models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="f80ef-182">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="f80ef-183">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f80ef-183">NOTES</span></span>

## <span data-ttu-id="f80ef-184">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f80ef-184">RELATED LINKS</span></span>
