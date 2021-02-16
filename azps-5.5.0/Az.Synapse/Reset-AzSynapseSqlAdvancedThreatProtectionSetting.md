---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/reset-azsynapsesqladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 420b95d8d20d21758e4f42db6c31e2d1ead557ac
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243074"
---
# <span data-ttu-id="a23f9-101">Reset-AzSynapseSqlAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="a23f9-101">Reset-AzSynapseSqlAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="a23f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a23f9-102">SYNOPSIS</span></span>
<span data-ttu-id="a23f9-103">Usuwa z obszaru roboczego zaawansowane ustawienia ochrony przed zagrożeniami.</span><span class="sxs-lookup"><span data-stu-id="a23f9-103">Removes the advanced threat protection settings from a workspace.</span></span>

## <span data-ttu-id="a23f9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a23f9-104">SYNTAX</span></span>

### <span data-ttu-id="a23f9-105">ClearByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="a23f9-105">ClearByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a23f9-106">ClearByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a23f9-106">ClearByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting -InputObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a23f9-107">ClearByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a23f9-107">ClearByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a23f9-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="a23f9-108">DESCRIPTION</span></span>
<span data-ttu-id="a23f9-109">Polecenie cmdlet **Reset-AzSynapseSqlAdvancedThreatProtectionSetting** usuwa zaawansowane ustawienia ochrony przed zagrożeniami z obszaru roboczego usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="a23f9-109">The **Reset-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet removes the advanced threat protection settings from an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="a23f9-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a23f9-110">EXAMPLES</span></span>

### <span data-ttu-id="a23f9-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a23f9-111">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="a23f9-112">To polecenie usuwa zaawansowane ustawienia ochrony przed zagrożeniami z obszaru roboczego o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="a23f9-112">This command removes the advanced threat protection settings from a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="a23f9-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a23f9-113">PARAMETERS</span></span>

### <span data-ttu-id="a23f9-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="a23f9-114">-AsJob</span></span>
<span data-ttu-id="a23f9-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a23f9-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a23f9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a23f9-116">-DefaultProfile</span></span>
<span data-ttu-id="a23f9-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a23f9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a23f9-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a23f9-118">-InputObject</span></span>
<span data-ttu-id="a23f9-119">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="a23f9-119">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: ClearByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a23f9-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a23f9-120">-PassThru</span></span>
<span data-ttu-id="a23f9-121">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="a23f9-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="a23f9-122">Jeśli ten przełącznik zostanie określony, zostanie on podany jako prawda, jeśli zostanie pomyślnie określony.</span><span class="sxs-lookup"><span data-stu-id="a23f9-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="a23f9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a23f9-123">-ResourceGroupName</span></span>
<span data-ttu-id="a23f9-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a23f9-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ClearByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a23f9-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a23f9-125">-ResourceId</span></span>
<span data-ttu-id="a23f9-126">Identyfikator zasobu obszaru roboczego programu Synapse.</span><span class="sxs-lookup"><span data-stu-id="a23f9-126">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ClearByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a23f9-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a23f9-127">-WorkspaceName</span></span>
<span data-ttu-id="a23f9-128">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="a23f9-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ClearByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a23f9-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a23f9-129">-Confirm</span></span>
<span data-ttu-id="a23f9-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a23f9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a23f9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a23f9-131">-WhatIf</span></span>
<span data-ttu-id="a23f9-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a23f9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a23f9-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a23f9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a23f9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a23f9-134">CommonParameters</span></span>
<span data-ttu-id="a23f9-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a23f9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a23f9-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a23f9-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a23f9-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a23f9-137">INPUTS</span></span>

### <span data-ttu-id="a23f9-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a23f9-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="a23f9-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a23f9-139">OUTPUTS</span></span>

### <span data-ttu-id="a23f9-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a23f9-140">System.Boolean</span></span>

## <span data-ttu-id="a23f9-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a23f9-141">NOTES</span></span>

## <span data-ttu-id="a23f9-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a23f9-142">RELATED LINKS</span></span>
