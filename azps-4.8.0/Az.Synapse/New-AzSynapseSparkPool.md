---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSparkPool.md
ms.openlocfilehash: c931bff1ba95ee1be185b5fe4dfdc2256d2cafec
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219686"
---
# <span data-ttu-id="c601b-101">New-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="c601b-101">New-AzSynapseSparkPool</span></span>

## <span data-ttu-id="c601b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c601b-102">SYNOPSIS</span></span>
<span data-ttu-id="c601b-103">Tworzy pulę Synapse analizy Spark.</span><span class="sxs-lookup"><span data-stu-id="c601b-103">Creates a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="c601b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c601b-104">SYNTAX</span></span>

### <span data-ttu-id="c601b-105">CreateByNameAndEnableAutoScaleParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c601b-105">CreateByNameAndEnableAutoScaleParameterSet (Default)</span></span>
```
New-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Tag <Hashtable>]
 -NodeSize <String> -AutoScaleMinNodeCount <Int32> -AutoScaleMaxNodeCount <Int32> [-EnableAutoPause]
 [-AutoPauseDelayInMinute <Int32>] -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c601b-106">CreateByNameAndDisableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="c601b-106">CreateByNameAndDisableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Tag <Hashtable>]
 -NodeCount <Int32> -NodeSize <String> [-EnableAutoPause] [-AutoPauseDelayInMinute <Int32>]
 -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c601b-107">CreateByParentObjectAndEnableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="c601b-107">CreateByParentObjectAndEnableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 -NodeSize <String> -AutoScaleMinNodeCount <Int32> -AutoScaleMaxNodeCount <Int32> [-EnableAutoPause]
 [-AutoPauseDelayInMinute <Int32>] -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c601b-108">CreateByParentObjectAndDisableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="c601b-108">CreateByParentObjectAndDisableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 -NodeCount <Int32> -NodeSize <String> [-EnableAutoPause] [-AutoPauseDelayInMinute <Int32>]
 -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c601b-109">Opis</span><span class="sxs-lookup"><span data-stu-id="c601b-109">DESCRIPTION</span></span>
<span data-ttu-id="c601b-110">Polecenie cmdlet **New-AzSynapseSparkPool** tworzy pulę platformy Azure Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="c601b-110">The **New-AzSynapseSparkPool** cmdlet creates an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="c601b-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c601b-111">EXAMPLES</span></span>

### <span data-ttu-id="c601b-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c601b-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool -NodeCount 3 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="c601b-113">To polecenie tworzy pulę platformy Azure Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="c601b-113">This command creates an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="c601b-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c601b-114">Example 2</span></span>
```powershell
PS C:\> New-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool -AutoScaleMinNodeCount 3 -AutoScaleMaxNodeCount 10 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="c601b-115">To polecenie tworzy pulę usługi Azure Synapse Analytics Spark z włączoną funkcją automatycznej skali.</span><span class="sxs-lookup"><span data-stu-id="c601b-115">This command creates an Azure Synapse Analytics Spark pool with auto-scale enabled.</span></span>

### <span data-ttu-id="c601b-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="c601b-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseSparkPool -Name ContosoSparkPool -NodeCount 3 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="c601b-117">To polecenie tworzy pulę usługi Azure Synapse Analytics Spark za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="c601b-117">This command creates an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="c601b-118">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="c601b-118">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseSparkPool -Name ContosoSparkPool -AutoScaleMinNodeCount 3 -AutoScaleMaxNodeCount 10 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="c601b-119">To polecenie tworzy pulę usługi Azure Synapse Analytics Spark z włączoną funkcją automatycznego skalowania za pomocą potoku.</span><span class="sxs-lookup"><span data-stu-id="c601b-119">This command creates an Azure Synapse Analytics Spark pool with auto-scale enabled through pipeline.</span></span>

## <span data-ttu-id="c601b-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c601b-120">PARAMETERS</span></span>

### <span data-ttu-id="c601b-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c601b-121">-AsJob</span></span>
<span data-ttu-id="c601b-122">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="c601b-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c601b-123">-AutoPauseDelayInMinute</span><span class="sxs-lookup"><span data-stu-id="c601b-123">-AutoPauseDelayInMinute</span></span>
<span data-ttu-id="c601b-124">Liczba minut bezczynności.</span><span class="sxs-lookup"><span data-stu-id="c601b-124">Number of minutes idle.</span></span> <span data-ttu-id="c601b-125">Ten parametr należy określić, gdy funkcja automatycznego wstrzymywania jest włączona.</span><span class="sxs-lookup"><span data-stu-id="c601b-125">This parameter must be specified when Auto-pause is enabled.</span></span>

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

### <span data-ttu-id="c601b-126">-AutoScaleMaxNodeCount</span><span class="sxs-lookup"><span data-stu-id="c601b-126">-AutoScaleMaxNodeCount</span></span>
<span data-ttu-id="c601b-127">Maksymalna liczba węzłów do przydzielenia w określonej puli platformy Spark.</span><span class="sxs-lookup"><span data-stu-id="c601b-127">Maximum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="c601b-128">Ten parametr należy określić, gdy funkcja automatycznego skalowania jest włączona.</span><span class="sxs-lookup"><span data-stu-id="c601b-128">This parameter must be specified when Auto-scale is enabled.</span></span>

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

### <span data-ttu-id="c601b-129">-AutoScaleMinNodeCount</span><span class="sxs-lookup"><span data-stu-id="c601b-129">-AutoScaleMinNodeCount</span></span>
<span data-ttu-id="c601b-130">Minimalna liczba węzłów do przydzielenia w określonej puli platformy Spark.</span><span class="sxs-lookup"><span data-stu-id="c601b-130">Minimum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="c601b-131">Ten parametr należy określić, gdy funkcja automatycznego skalowania jest włączona.</span><span class="sxs-lookup"><span data-stu-id="c601b-131">This parameter must be specified when Auto-scale is enabled.</span></span>

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

### <span data-ttu-id="c601b-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c601b-132">-DefaultProfile</span></span>
<span data-ttu-id="c601b-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c601b-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c601b-134">-EnableAutoPause</span><span class="sxs-lookup"><span data-stu-id="c601b-134">-EnableAutoPause</span></span>
<span data-ttu-id="c601b-135">Wskazuje, czy funkcja automatycznego wstrzymywania ma być włączona.</span><span class="sxs-lookup"><span data-stu-id="c601b-135">Indicates whether Auto-pause should be enabled.</span></span>

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

### <span data-ttu-id="c601b-136">-LibraryRequirementsFilePath</span><span class="sxs-lookup"><span data-stu-id="c601b-136">-LibraryRequirementsFilePath</span></span>
<span data-ttu-id="c601b-137">Plik konfiguracji środowiska ("PIP Zablokuj").</span><span class="sxs-lookup"><span data-stu-id="c601b-137">Environment configuration file ("PIP freeze" output).</span></span>

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

### <span data-ttu-id="c601b-138">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c601b-138">-Name</span></span>
<span data-ttu-id="c601b-139">Nazwa puli Synapse Spark.</span><span class="sxs-lookup"><span data-stu-id="c601b-139">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="c601b-140">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="c601b-140">-NodeCount</span></span>
<span data-ttu-id="c601b-141">Liczba węzłów do przydzielenia w określonej puli platformy Spark.</span><span class="sxs-lookup"><span data-stu-id="c601b-141">Number of nodes to be allocated in the specified Spark pool.</span></span>

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

### <span data-ttu-id="c601b-142">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="c601b-142">-NodeSize</span></span>
<span data-ttu-id="c601b-143">Liczba nośników podstawowych i pamięci, które mają być używane dla węzłów przydzielonych w określonej puli platformy Spark.</span><span class="sxs-lookup"><span data-stu-id="c601b-143">Number of core and memory to be used for nodes allocated in the specified Spark pool.</span></span>
<span data-ttu-id="c601b-144">Ten parametr należy określić, gdy funkcja automatycznego skalowania jest wyłączona</span><span class="sxs-lookup"><span data-stu-id="c601b-144">This parameter must be specified when Auto-scale is disabled</span></span>

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

### <span data-ttu-id="c601b-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c601b-145">-ResourceGroupName</span></span>
<span data-ttu-id="c601b-146">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c601b-146">Resource group name.</span></span>

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

### <span data-ttu-id="c601b-147">-SparkVersion</span><span class="sxs-lookup"><span data-stu-id="c601b-147">-SparkVersion</span></span>
<span data-ttu-id="c601b-148">Wersja oprogramowania Apache Spark.</span><span class="sxs-lookup"><span data-stu-id="c601b-148">Apache Spark version.</span></span>
<span data-ttu-id="c601b-149">Dozwolone wartości: 2,4</span><span class="sxs-lookup"><span data-stu-id="c601b-149">Allowed values: 2.4</span></span>

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

### <span data-ttu-id="c601b-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="c601b-150">-Tag</span></span>
<span data-ttu-id="c601b-151">Ciąg znaków, który jest ciągiem znaczników skojarzonych z zasobem.</span><span class="sxs-lookup"><span data-stu-id="c601b-151">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="c601b-152">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="c601b-152">-WorkspaceName</span></span>
<span data-ttu-id="c601b-153">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="c601b-153">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="c601b-154">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="c601b-154">-WorkspaceObject</span></span>
<span data-ttu-id="c601b-155">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="c601b-155">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="c601b-156">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c601b-156">-Confirm</span></span>
<span data-ttu-id="c601b-157">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c601b-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c601b-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c601b-158">-WhatIf</span></span>
<span data-ttu-id="c601b-159">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c601b-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c601b-160">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c601b-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c601b-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c601b-161">CommonParameters</span></span>
<span data-ttu-id="c601b-162">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c601b-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c601b-163">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c601b-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c601b-164">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c601b-164">INPUTS</span></span>

### <span data-ttu-id="c601b-165">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c601b-165">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="c601b-166">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c601b-166">OUTPUTS</span></span>

### <span data-ttu-id="c601b-167">Microsoft. Azure. Commands. Synapse. models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="c601b-167">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="c601b-168">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c601b-168">NOTES</span></span>

## <span data-ttu-id="c601b-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c601b-169">RELATED LINKS</span></span>
