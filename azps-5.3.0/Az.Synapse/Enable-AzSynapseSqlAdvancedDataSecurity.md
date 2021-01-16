---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/enable-azsynapsesqladvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Enable-AzSynapseSqlAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Enable-AzSynapseSqlAdvancedDataSecurity.md
ms.openlocfilehash: dea0770af8cca14ebd523f67b69d7a12931183ec
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384134"
---
# <span data-ttu-id="f3035-101">Enable-AzSynapseSqlAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="f3035-101">Enable-AzSynapseSqlAdvancedDataSecurity</span></span>

## <span data-ttu-id="f3035-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f3035-102">SYNOPSIS</span></span>
<span data-ttu-id="f3035-103">Włączanie zaawansowanych zabezpieczeń danych w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="f3035-103">Enables Advanced Data Security on a workspace.</span></span>

## <span data-ttu-id="f3035-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f3035-104">SYNTAX</span></span>

### <span data-ttu-id="f3035-105">EnableByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f3035-105">EnableByNameParameterSet (Default)</span></span>
```
Enable-AzSynapseSqlAdvancedDataSecurity [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DoNotConfigureVulnerabilityAssessment] [-DeploymentName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3035-106">EnableByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3035-106">EnableByInputObjectParameterSet</span></span>
```
Enable-AzSynapseSqlAdvancedDataSecurity -InputObject <PSSynapseWorkspace>
 [-DoNotConfigureVulnerabilityAssessment] [-DeploymentName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3035-107">EnableByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3035-107">EnableByResourceIdParameterSet</span></span>
```
Enable-AzSynapseSqlAdvancedDataSecurity -ResourceId <String> [-DoNotConfigureVulnerabilityAssessment]
 [-DeploymentName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f3035-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f3035-108">DESCRIPTION</span></span>
<span data-ttu-id="f3035-109">Polecenie cmdlet **enable-AzSynapseSqlAdvancedDataSecurity** włącza zaawansowane zabezpieczenia danych w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="f3035-109">The **Enable-AzSynapseSqlAdvancedDataSecurity** cmdlet enables Advanced Data Security on a workspace.</span></span> <span data-ttu-id="f3035-110">Zaawansowane zabezpieczenia danych to ujednolicony pakiet zabezpieczeń, który obejmuje klasyfikację danych, ocenę luk w zabezpieczeniach i zaawansowaną ochronę przed zagrożeniami dla obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="f3035-110">Advanced Data Security is a unified security package that includes Data Classification, Vulnerability Assessment and Advanced Threat Protection for your workspace.</span></span> <span data-ttu-id="f3035-111">(Nowe konto magazynu zostanie automatycznie utworzone w celu zapisania ocen dotyczących luk.</span><span class="sxs-lookup"><span data-stu-id="f3035-111">(A new storage account will automatically be created for saving vulnerability assessments.</span></span> <span data-ttu-id="f3035-112">Jeśli w tym celu utworzono wcześniej konto magazynu, zamiast tego zostanie użyte to polecenie.</span><span class="sxs-lookup"><span data-stu-id="f3035-112">If a storage account was previously created for this purpose, it will be used instead)</span></span>

## <span data-ttu-id="f3035-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f3035-113">EXAMPLES</span></span>

### <span data-ttu-id="f3035-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f3035-114">Example 1</span></span>
```powershell
PS C:\> Enable-AzSynapseSqlAdvancedDataSecurity -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="f3035-115">To polecenie włącza zaawansowane zabezpieczenia danych w obszarze przestrzeń robocza.</span><span class="sxs-lookup"><span data-stu-id="f3035-115">This command enables workspace Advanced Data Security.</span></span>

### <span data-ttu-id="f3035-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f3035-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Enable-AzSynapseSqlAdvancedDataSecurity
```

<span data-ttu-id="f3035-117">To polecenie umożliwia zaawansowane bezpieczeństwo danych w obszarze roboczym za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="f3035-117">This command enables workspace Advanced Data Security through pipeline.</span></span>

### <span data-ttu-id="f3035-118">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="f3035-118">Example 3</span></span>
```powershell
PS C:\> Enable-AzSynapseSqlAdvancedDataSecurity -WorkspaceName ContosoWorkspace -DoNotConfigureVulnerabilityAssessment
```

<span data-ttu-id="f3035-119">To polecenie umożliwia zaawansowane zabezpieczenie danych w obszarze roboczym za pośrednictwem rurociągu i nie powoduje automatycznego włączenia oceny luki w zabezpieczeniach.</span><span class="sxs-lookup"><span data-stu-id="f3035-119">This command enables workspace Advanced Data Security through pipeline and does not auto enable Vulnerability Assessment.</span></span>

## <span data-ttu-id="f3035-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f3035-120">PARAMETERS</span></span>

### <span data-ttu-id="f3035-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f3035-121">-AsJob</span></span>
<span data-ttu-id="f3035-122">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f3035-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f3035-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3035-123">-DefaultProfile</span></span>
<span data-ttu-id="f3035-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f3035-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3035-125">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="f3035-125">-DeploymentName</span></span>
<span data-ttu-id="f3035-126">Podaj nazwę niestandardową dla zaawansowanego wdrożenia zabezpieczeń danych.</span><span class="sxs-lookup"><span data-stu-id="f3035-126">Supply a custom name for Advanced Data Security deployment.</span></span>

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

### <span data-ttu-id="f3035-127">-DoNotConfigureVulnerabilityAssessment</span><span class="sxs-lookup"><span data-stu-id="f3035-127">-DoNotConfigureVulnerabilityAssessment</span></span>
<span data-ttu-id="f3035-128">Nie włączaj automatycznie oceny luki (nie spowoduje to utworzenia konta magazynu).</span><span class="sxs-lookup"><span data-stu-id="f3035-128">Do not auto enable Vulnerability Assessment (This will not create a storage account).</span></span>

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

### <span data-ttu-id="f3035-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f3035-129">-InputObject</span></span>
<span data-ttu-id="f3035-130">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="f3035-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: EnableByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3035-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3035-131">-ResourceGroupName</span></span>
<span data-ttu-id="f3035-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f3035-132">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3035-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3035-133">-ResourceId</span></span>
<span data-ttu-id="f3035-134">Identyfikator zasobu obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="f3035-134">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3035-135">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="f3035-135">-WorkspaceName</span></span>
<span data-ttu-id="f3035-136">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="f3035-136">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3035-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f3035-137">-Confirm</span></span>
<span data-ttu-id="f3035-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3035-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3035-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3035-139">-WhatIf</span></span>
<span data-ttu-id="f3035-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3035-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3035-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f3035-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3035-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3035-142">CommonParameters</span></span>
<span data-ttu-id="f3035-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3035-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3035-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f3035-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3035-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f3035-145">INPUTS</span></span>

### <span data-ttu-id="f3035-146">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f3035-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="f3035-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f3035-147">OUTPUTS</span></span>

### <span data-ttu-id="f3035-148">Microsoft. Azure. Commands. Synapse. models. WorkspaceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="f3035-148">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="f3035-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f3035-149">NOTES</span></span>

## <span data-ttu-id="f3035-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f3035-150">RELATED LINKS</span></span>
