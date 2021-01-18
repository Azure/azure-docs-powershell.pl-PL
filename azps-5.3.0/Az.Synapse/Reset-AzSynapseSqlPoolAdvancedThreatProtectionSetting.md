---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/reset-azsynapsesqlpooladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
ms.openlocfilehash: c5f1c3f2d1a23a06286cdbf7fb54915d33b1e3d3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501312"
---
# <span data-ttu-id="1bcb2-101">Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="1bcb2-101">Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="1bcb2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1bcb2-102">SYNOPSIS</span></span>
<span data-ttu-id="1bcb2-103">Usuwa zaawansowane ustawienia ochrony przed zagrożeniami z puli SQL.</span><span class="sxs-lookup"><span data-stu-id="1bcb2-103">Removes the advanced threat protection settings from a SQL pool.</span></span>

## <span data-ttu-id="1bcb2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1bcb2-104">SYNTAX</span></span>

### <span data-ttu-id="1bcb2-105">ClearByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1bcb2-105">ClearByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1bcb2-106">ClearByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1bcb2-106">ClearByParentObjectParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bcb2-107">ClearByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1bcb2-107">ClearByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bcb2-108">ClearByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1bcb2-108">ClearByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1bcb2-109">Opis</span><span class="sxs-lookup"><span data-stu-id="1bcb2-109">DESCRIPTION</span></span>
<span data-ttu-id="1bcb2-110">Polecenie cmdlet **Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting** usuwa zaawansowane ustawienia ochrony przed zagrożeniami z puli SQL usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="1bcb2-110">The **Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting** cmdlet removes the advanced threat protection settings from an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="1bcb2-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1bcb2-111">EXAMPLES</span></span>

### <span data-ttu-id="1bcb2-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1bcb2-112">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="1bcb2-113">To polecenie usuwa zaawansowane ustawienia ochrony przed zagrożeniami z puli SQL o nazwie ContosoSqlPool w obszarze roboczym o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="1bcb2-113">This command removes the advanced threat protection settings from a SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="1bcb2-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1bcb2-114">PARAMETERS</span></span>

### <span data-ttu-id="1bcb2-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1bcb2-115">-AsJob</span></span>
<span data-ttu-id="1bcb2-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="1bcb2-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1bcb2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bcb2-117">-DefaultProfile</span></span>
<span data-ttu-id="1bcb2-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1bcb2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1bcb2-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1bcb2-119">-InputObject</span></span>
<span data-ttu-id="1bcb2-120">Obiekt wejściowy zestawu SQL, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="1bcb2-120">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="1bcb2-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1bcb2-121">-Name</span></span>
<span data-ttu-id="1bcb2-122">Nazwa puli SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="1bcb2-122">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="1bcb2-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1bcb2-123">-PassThru</span></span>
<span data-ttu-id="1bcb2-124">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="1bcb2-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="1bcb2-125">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="1bcb2-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="1bcb2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bcb2-126">-ResourceGroupName</span></span>
<span data-ttu-id="1bcb2-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1bcb2-127">Resource group name.</span></span>

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

### <span data-ttu-id="1bcb2-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1bcb2-128">-ResourceId</span></span>
<span data-ttu-id="1bcb2-129">Identyfikator zasobu puli SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="1bcb2-129">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="1bcb2-130">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="1bcb2-130">-WorkspaceName</span></span>
<span data-ttu-id="1bcb2-131">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="1bcb2-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="1bcb2-132">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="1bcb2-132">-WorkspaceObject</span></span>
<span data-ttu-id="1bcb2-133">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="1bcb2-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="1bcb2-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1bcb2-134">-Confirm</span></span>
<span data-ttu-id="1bcb2-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1bcb2-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bcb2-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bcb2-136">-WhatIf</span></span>
<span data-ttu-id="1bcb2-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1bcb2-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1bcb2-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1bcb2-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bcb2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bcb2-139">CommonParameters</span></span>
<span data-ttu-id="1bcb2-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bcb2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bcb2-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1bcb2-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bcb2-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1bcb2-142">INPUTS</span></span>

### <span data-ttu-id="1bcb2-143">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="1bcb2-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="1bcb2-144">Microsoft. Azure. Commands. Synapse. models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="1bcb2-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="1bcb2-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1bcb2-145">OUTPUTS</span></span>

### <span data-ttu-id="1bcb2-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1bcb2-146">System.Boolean</span></span>

## <span data-ttu-id="1bcb2-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1bcb2-147">NOTES</span></span>

## <span data-ttu-id="1bcb2-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1bcb2-148">RELATED LINKS</span></span>
