---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/enable-azsynapsesqladvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Enable-AzSynapseSqlAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Enable-AzSynapseSqlAdvancedDataSecurity.md
ms.openlocfilehash: dea0770af8cca14ebd523f67b69d7a12931183ec
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197403"
---
# <span data-ttu-id="d67de-101">Enable-AzSynapseSqlAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="d67de-101">Enable-AzSynapseSqlAdvancedDataSecurity</span></span>

## <span data-ttu-id="d67de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d67de-102">SYNOPSIS</span></span>
<span data-ttu-id="d67de-103">Włącza zaawansowane zabezpieczenia danych w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="d67de-103">Enables Advanced Data Security on a workspace.</span></span>

## <span data-ttu-id="d67de-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d67de-104">SYNTAX</span></span>

### <span data-ttu-id="d67de-105">EnableByNameParameterSet (Ustawienie domyślne)</span><span class="sxs-lookup"><span data-stu-id="d67de-105">EnableByNameParameterSet (Default)</span></span>
```
Enable-AzSynapseSqlAdvancedDataSecurity [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DoNotConfigureVulnerabilityAssessment] [-DeploymentName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d67de-106">EnableByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d67de-106">EnableByInputObjectParameterSet</span></span>
```
Enable-AzSynapseSqlAdvancedDataSecurity -InputObject <PSSynapseWorkspace>
 [-DoNotConfigureVulnerabilityAssessment] [-DeploymentName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d67de-107">EnableByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d67de-107">EnableByResourceIdParameterSet</span></span>
```
Enable-AzSynapseSqlAdvancedDataSecurity -ResourceId <String> [-DoNotConfigureVulnerabilityAssessment]
 [-DeploymentName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d67de-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="d67de-108">DESCRIPTION</span></span>
<span data-ttu-id="d67de-109">Polecenie **cmdlet Enable-AzSynapseSqlAdvancedDataSecurity** włącza zaawansowane zabezpieczenia danych w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="d67de-109">The **Enable-AzSynapseSqlAdvancedDataSecurity** cmdlet enables Advanced Data Security on a workspace.</span></span> <span data-ttu-id="d67de-110">Advanced Data Security to ujednolicony pakiet zabezpieczeń, który zawiera klasyfikację danych, ocenę luk i zaawansowaną ochronę przed zagrożeniami dla obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="d67de-110">Advanced Data Security is a unified security package that includes Data Classification, Vulnerability Assessment and Advanced Threat Protection for your workspace.</span></span> <span data-ttu-id="d67de-111">(Zostanie automatycznie utworzone nowe konto magazynu w celu zapisania oceny luk w zabezpieczeniach.</span><span class="sxs-lookup"><span data-stu-id="d67de-111">(A new storage account will automatically be created for saving vulnerability assessments.</span></span> <span data-ttu-id="d67de-112">Jeśli do tego celu wcześniej utworzono konto magazynu, będzie ono używane zamiast tego)</span><span class="sxs-lookup"><span data-stu-id="d67de-112">If a storage account was previously created for this purpose, it will be used instead)</span></span>

## <span data-ttu-id="d67de-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d67de-113">EXAMPLES</span></span>

### <span data-ttu-id="d67de-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d67de-114">Example 1</span></span>
```powershell
PS C:\> Enable-AzSynapseSqlAdvancedDataSecurity -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="d67de-115">To polecenie umożliwia obszarowi roboczemu zaawansowane zabezpieczenia danych.</span><span class="sxs-lookup"><span data-stu-id="d67de-115">This command enables workspace Advanced Data Security.</span></span>

### <span data-ttu-id="d67de-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d67de-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Enable-AzSynapseSqlAdvancedDataSecurity
```

<span data-ttu-id="d67de-117">To polecenie umożliwia obszarowi roboczemu zaawansowane zabezpieczenia danych za pośrednictwem potoku.</span><span class="sxs-lookup"><span data-stu-id="d67de-117">This command enables workspace Advanced Data Security through pipeline.</span></span>

### <span data-ttu-id="d67de-118">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="d67de-118">Example 3</span></span>
```powershell
PS C:\> Enable-AzSynapseSqlAdvancedDataSecurity -WorkspaceName ContosoWorkspace -DoNotConfigureVulnerabilityAssessment
```

<span data-ttu-id="d67de-119">To polecenie umożliwia obszarowi roboczemu zaawansowane zabezpieczenia danych za pośrednictwem potoku i nie umożliwia automatycznego oceniania luk.</span><span class="sxs-lookup"><span data-stu-id="d67de-119">This command enables workspace Advanced Data Security through pipeline and does not auto enable Vulnerability Assessment.</span></span>

## <span data-ttu-id="d67de-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d67de-120">PARAMETERS</span></span>

### <span data-ttu-id="d67de-121">— AsJob</span><span class="sxs-lookup"><span data-stu-id="d67de-121">-AsJob</span></span>
<span data-ttu-id="d67de-122">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d67de-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d67de-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d67de-123">-DefaultProfile</span></span>
<span data-ttu-id="d67de-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d67de-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d67de-125">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="d67de-125">-DeploymentName</span></span>
<span data-ttu-id="d67de-126">Nadaj niestandardową nazwę zaawansowanego wdrożenia zabezpieczeń danych.</span><span class="sxs-lookup"><span data-stu-id="d67de-126">Supply a custom name for Advanced Data Security deployment.</span></span>

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

### <span data-ttu-id="d67de-127">-DoNotConfigureVulnerabilityAssessment</span><span class="sxs-lookup"><span data-stu-id="d67de-127">-DoNotConfigureVulnerabilityAssessment</span></span>
<span data-ttu-id="d67de-128">Nie włączaj automatycznie oceny luk (nie spowoduje to utworzenia konta magazynu).</span><span class="sxs-lookup"><span data-stu-id="d67de-128">Do not auto enable Vulnerability Assessment (This will not create a storage account).</span></span>

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

### <span data-ttu-id="d67de-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d67de-129">-InputObject</span></span>
<span data-ttu-id="d67de-130">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="d67de-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="d67de-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d67de-131">-ResourceGroupName</span></span>
<span data-ttu-id="d67de-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d67de-132">Resource group name.</span></span>

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

### <span data-ttu-id="d67de-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d67de-133">-ResourceId</span></span>
<span data-ttu-id="d67de-134">Identyfikator zasobu obszaru roboczego programu Synapse.</span><span class="sxs-lookup"><span data-stu-id="d67de-134">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="d67de-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d67de-135">-WorkspaceName</span></span>
<span data-ttu-id="d67de-136">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="d67de-136">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="d67de-137">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d67de-137">-Confirm</span></span>
<span data-ttu-id="d67de-138">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d67de-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d67de-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d67de-139">-WhatIf</span></span>
<span data-ttu-id="d67de-140">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d67de-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d67de-141">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d67de-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d67de-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d67de-142">CommonParameters</span></span>
<span data-ttu-id="d67de-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d67de-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d67de-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d67de-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d67de-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d67de-145">INPUTS</span></span>

### <span data-ttu-id="d67de-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d67de-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="d67de-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d67de-147">OUTPUTS</span></span>

### <span data-ttu-id="d67de-148">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="d67de-148">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="d67de-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d67de-149">NOTES</span></span>

## <span data-ttu-id="d67de-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d67de-150">RELATED LINKS</span></span>
