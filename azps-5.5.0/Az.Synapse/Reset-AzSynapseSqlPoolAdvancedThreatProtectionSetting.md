---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/reset-azsynapsesqlpooladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
ms.openlocfilehash: c5f1c3f2d1a23a06286cdbf7fb54915d33b1e3d3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243051"
---
# <span data-ttu-id="8c0f8-101">Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="8c0f8-101">Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="8c0f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c0f8-102">SYNOPSIS</span></span>
<span data-ttu-id="8c0f8-103">Usuwa zaawansowane ustawienia ochrony przed zagrożeniami z puli SQL.</span><span class="sxs-lookup"><span data-stu-id="8c0f8-103">Removes the advanced threat protection settings from a SQL pool.</span></span>

## <span data-ttu-id="8c0f8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8c0f8-104">SYNTAX</span></span>

### <span data-ttu-id="8c0f8-105">ClearByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="8c0f8-105">ClearByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8c0f8-106">ClearByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c0f8-106">ClearByParentObjectParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c0f8-107">ClearByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c0f8-107">ClearByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c0f8-108">ClearByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c0f8-108">ClearByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c0f8-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="8c0f8-109">DESCRIPTION</span></span>
<span data-ttu-id="8c0f8-110">Polecenie cmdlet **Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting** usuwa zaawansowane ustawienia ochrony przed zagrożeniami z puli sql usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="8c0f8-110">The **Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting** cmdlet removes the advanced threat protection settings from an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="8c0f8-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8c0f8-111">EXAMPLES</span></span>

### <span data-ttu-id="8c0f8-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8c0f8-112">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="8c0f8-113">To polecenie usuwa zaawansowane ustawienia ochrony przed zagrożeniami z puli sql o nazwie ContosoSqlPool w obszarze roboczym o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="8c0f8-113">This command removes the advanced threat protection settings from a SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="8c0f8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c0f8-114">PARAMETERS</span></span>

### <span data-ttu-id="8c0f8-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="8c0f8-115">-AsJob</span></span>
<span data-ttu-id="8c0f8-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="8c0f8-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8c0f8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c0f8-117">-DefaultProfile</span></span>
<span data-ttu-id="8c0f8-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8c0f8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c0f8-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8c0f8-119">-InputObject</span></span>
<span data-ttu-id="8c0f8-120">Obiekt wejściowy puli SQL, który zwykle przechodził przez potok.</span><span class="sxs-lookup"><span data-stu-id="8c0f8-120">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: ClearByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c0f8-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8c0f8-121">-Name</span></span>
<span data-ttu-id="8c0f8-122">Nazwa puli sql Synapse.</span><span class="sxs-lookup"><span data-stu-id="8c0f8-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ClearByNameParameterSet, ClearByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c0f8-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8c0f8-123">-PassThru</span></span>
<span data-ttu-id="8c0f8-124">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="8c0f8-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="8c0f8-125">Jeśli ten przełącznik zostanie określony, zostanie on podany jako prawda, jeśli zostanie pomyślnie określony.</span><span class="sxs-lookup"><span data-stu-id="8c0f8-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="8c0f8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c0f8-126">-ResourceGroupName</span></span>
<span data-ttu-id="8c0f8-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8c0f8-127">Resource group name.</span></span>

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

### <span data-ttu-id="8c0f8-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c0f8-128">-ResourceId</span></span>
<span data-ttu-id="8c0f8-129">Identyfikator zasobu synapse SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="8c0f8-129">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="8c0f8-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8c0f8-130">-WorkspaceName</span></span>
<span data-ttu-id="8c0f8-131">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="8c0f8-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="8c0f8-132">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="8c0f8-132">-WorkspaceObject</span></span>
<span data-ttu-id="8c0f8-133">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="8c0f8-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: ClearByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c0f8-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8c0f8-134">-Confirm</span></span>
<span data-ttu-id="8c0f8-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8c0f8-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c0f8-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c0f8-136">-WhatIf</span></span>
<span data-ttu-id="8c0f8-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c0f8-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c0f8-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8c0f8-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c0f8-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c0f8-139">CommonParameters</span></span>
<span data-ttu-id="8c0f8-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c0f8-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c0f8-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8c0f8-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c0f8-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8c0f8-142">INPUTS</span></span>

### <span data-ttu-id="8c0f8-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="8c0f8-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="8c0f8-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="8c0f8-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="8c0f8-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8c0f8-145">OUTPUTS</span></span>

### <span data-ttu-id="8c0f8-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8c0f8-146">System.Boolean</span></span>

## <span data-ttu-id="8c0f8-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8c0f8-147">NOTES</span></span>

## <span data-ttu-id="8c0f8-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8c0f8-148">RELATED LINKS</span></span>
