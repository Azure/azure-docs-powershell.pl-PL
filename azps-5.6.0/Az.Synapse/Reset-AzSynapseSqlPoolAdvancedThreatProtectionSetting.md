---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/reset-azsynapsesqlpooladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 425b9c74fac1cd17b8e2c86045fbb4fcd8875b67
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979089"
---
# <span data-ttu-id="605c9-101">Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="605c9-101">Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="605c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="605c9-102">SYNOPSIS</span></span>
<span data-ttu-id="605c9-103">Usuwa zaawansowane ustawienia ochrony przed zagrożeniami z puli SQL.</span><span class="sxs-lookup"><span data-stu-id="605c9-103">Removes the advanced threat protection settings from a SQL pool.</span></span>

## <span data-ttu-id="605c9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="605c9-104">SYNTAX</span></span>

### <span data-ttu-id="605c9-105">ClearByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="605c9-105">ClearByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="605c9-106">ClearByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="605c9-106">ClearByParentObjectParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="605c9-107">ClearByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="605c9-107">ClearByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="605c9-108">ClearByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="605c9-108">ClearByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="605c9-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="605c9-109">DESCRIPTION</span></span>
<span data-ttu-id="605c9-110">Polecenie cmdlet **Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting** usuwa zaawansowane ustawienia ochrony przed zagrożeniami z puli sql usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="605c9-110">The **Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting** cmdlet removes the advanced threat protection settings from an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="605c9-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="605c9-111">EXAMPLES</span></span>

### <span data-ttu-id="605c9-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="605c9-112">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="605c9-113">To polecenie usuwa zaawansowane ustawienia ochrony przed zagrożeniami z puli SQL o nazwie ContosoSqlPool w obszarze roboczym o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="605c9-113">This command removes the advanced threat protection settings from a SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="605c9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="605c9-114">PARAMETERS</span></span>

### <span data-ttu-id="605c9-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="605c9-115">-AsJob</span></span>
<span data-ttu-id="605c9-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="605c9-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="605c9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="605c9-117">-DefaultProfile</span></span>
<span data-ttu-id="605c9-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="605c9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="605c9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="605c9-119">-InputObject</span></span>
<span data-ttu-id="605c9-120">Obiekt wejściowy puli SQL, który zwykle przechodził przez potok.</span><span class="sxs-lookup"><span data-stu-id="605c9-120">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="605c9-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="605c9-121">-Name</span></span>
<span data-ttu-id="605c9-122">Nazwa puli sql Synapse.</span><span class="sxs-lookup"><span data-stu-id="605c9-122">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="605c9-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="605c9-123">-PassThru</span></span>
<span data-ttu-id="605c9-124">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="605c9-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="605c9-125">Jeśli ten przełącznik zostanie określony, zostanie on podany jako prawda, jeśli zostanie pomyślnie określony.</span><span class="sxs-lookup"><span data-stu-id="605c9-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="605c9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="605c9-126">-ResourceGroupName</span></span>
<span data-ttu-id="605c9-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="605c9-127">Resource group name.</span></span>

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

### <span data-ttu-id="605c9-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="605c9-128">-ResourceId</span></span>
<span data-ttu-id="605c9-129">Identyfikator zasobu synapse SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="605c9-129">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="605c9-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="605c9-130">-WorkspaceName</span></span>
<span data-ttu-id="605c9-131">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="605c9-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="605c9-132">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="605c9-132">-WorkspaceObject</span></span>
<span data-ttu-id="605c9-133">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="605c9-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="605c9-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="605c9-134">-Confirm</span></span>
<span data-ttu-id="605c9-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="605c9-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="605c9-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="605c9-136">-WhatIf</span></span>
<span data-ttu-id="605c9-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="605c9-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="605c9-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="605c9-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="605c9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="605c9-139">CommonParameters</span></span>
<span data-ttu-id="605c9-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="605c9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="605c9-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="605c9-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="605c9-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="605c9-142">INPUTS</span></span>

### <span data-ttu-id="605c9-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="605c9-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="605c9-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="605c9-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="605c9-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="605c9-145">OUTPUTS</span></span>

### <span data-ttu-id="605c9-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="605c9-146">System.Boolean</span></span>

## <span data-ttu-id="605c9-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="605c9-147">NOTES</span></span>

## <span data-ttu-id="605c9-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="605c9-148">RELATED LINKS</span></span>
