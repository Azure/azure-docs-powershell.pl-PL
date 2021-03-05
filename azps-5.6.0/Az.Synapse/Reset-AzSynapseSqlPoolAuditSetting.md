---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/reset-azsynapsesqlpoolauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlPoolAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlPoolAuditSetting.md
ms.openlocfilehash: 8b47466c2f40ff769c1755ea1d59873a120e5d5e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010145"
---
# <span data-ttu-id="a970a-101">Reset-AzSynapseSqlPoolAuditSetting</span><span class="sxs-lookup"><span data-stu-id="a970a-101">Reset-AzSynapseSqlPoolAuditSetting</span></span>

## <span data-ttu-id="a970a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a970a-102">SYNOPSIS</span></span>
<span data-ttu-id="a970a-103">Usuwa ustawienia inspekcji puli sql usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="a970a-103">Removes the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="a970a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a970a-104">SYNTAX</span></span>

### <span data-ttu-id="a970a-105">RemoveByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="a970a-105">RemoveByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlPoolAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a970a-106">RemoveByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a970a-106">RemoveByParentObjectParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAuditSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a970a-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a970a-107">RemoveByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAuditSetting -InputObject <PSSynapseSqlPool> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a970a-108">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a970a-108">RemoveByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAuditSetting -ResourceId <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a970a-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="a970a-109">DESCRIPTION</span></span>
<span data-ttu-id="a970a-110">Polecenie cmdlet **Reset-AzSynapseSqlPoolAuditSetting** usuwa ustawienia inspekcji puli SQL Synapse Analytics platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a970a-110">The **Reset-AzSynapseSqlPoolAuditSetting** cmdlet removes the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="a970a-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a970a-111">EXAMPLES</span></span>

### <span data-ttu-id="a970a-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a970a-112">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="a970a-113">To polecenie usuwa ustawienia inspekcji puli języka SQL o nazwie ContosoSqlPool w obszarze roboczym ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="a970a-113">This command removes the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="a970a-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a970a-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Reset-AzSynapseSqlPoolAuditSetting
```

<span data-ttu-id="a970a-115">To polecenie usuwa ustawienia inspekcji puli języka SQL o nazwie ContosoSqlPool w obszarze roboczym ContosoWorkspace za pośrednictwem potoku.</span><span class="sxs-lookup"><span data-stu-id="a970a-115">This command removes the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="a970a-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a970a-116">PARAMETERS</span></span>

### <span data-ttu-id="a970a-117">— AsJob</span><span class="sxs-lookup"><span data-stu-id="a970a-117">-AsJob</span></span>
<span data-ttu-id="a970a-118">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a970a-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a970a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a970a-119">-DefaultProfile</span></span>
<span data-ttu-id="a970a-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a970a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a970a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a970a-121">-InputObject</span></span>
<span data-ttu-id="a970a-122">Obiekt wejściowy puli SQL, który zwykle przechodził przez potok.</span><span class="sxs-lookup"><span data-stu-id="a970a-122">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a970a-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a970a-123">-Name</span></span>
<span data-ttu-id="a970a-124">Nazwa puli sql Synapse.</span><span class="sxs-lookup"><span data-stu-id="a970a-124">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet, RemoveByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a970a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a970a-125">-PassThru</span></span>
<span data-ttu-id="a970a-126">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="a970a-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="a970a-127">Jeśli ten przełącznik zostanie określony, zostanie on podany jako prawda, jeśli zostanie pomyślnie określony.</span><span class="sxs-lookup"><span data-stu-id="a970a-127">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="a970a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a970a-128">-ResourceGroupName</span></span>
<span data-ttu-id="a970a-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a970a-129">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a970a-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a970a-130">-ResourceId</span></span>
<span data-ttu-id="a970a-131">Identyfikator zasobu synapse SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="a970a-131">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a970a-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a970a-132">-WorkspaceName</span></span>
<span data-ttu-id="a970a-133">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="a970a-133">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a970a-134">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a970a-134">-WorkspaceObject</span></span>
<span data-ttu-id="a970a-135">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="a970a-135">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a970a-136">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a970a-136">-Confirm</span></span>
<span data-ttu-id="a970a-137">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a970a-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a970a-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a970a-138">-WhatIf</span></span>
<span data-ttu-id="a970a-139">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a970a-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a970a-140">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a970a-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a970a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a970a-141">CommonParameters</span></span>
<span data-ttu-id="a970a-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a970a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a970a-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a970a-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a970a-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a970a-144">INPUTS</span></span>

### <span data-ttu-id="a970a-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a970a-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="a970a-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="a970a-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="a970a-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a970a-147">OUTPUTS</span></span>

### <span data-ttu-id="a970a-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a970a-148">System.Boolean</span></span>

## <span data-ttu-id="a970a-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a970a-149">NOTES</span></span>

## <span data-ttu-id="a970a-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a970a-150">RELATED LINKS</span></span>
