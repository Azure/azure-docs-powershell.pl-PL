---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/reset-azsynapsesqlauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAuditSetting.md
ms.openlocfilehash: b25ca2a026cf5d82aa25f69868ca8605fd75bced
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243066"
---
# <span data-ttu-id="a4fd6-101">Reset-AzSynapseSqlAuditSetting</span><span class="sxs-lookup"><span data-stu-id="a4fd6-101">Reset-AzSynapseSqlAuditSetting</span></span>

## <span data-ttu-id="a4fd6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4fd6-102">SYNOPSIS</span></span>
<span data-ttu-id="a4fd6-103">Usuwa ustawienia inspekcji obszaru roboczego analizy Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="a4fd6-103">Removes the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="a4fd6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a4fd6-104">SYNTAX</span></span>

### <span data-ttu-id="a4fd6-105">RemoveByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="a4fd6-105">RemoveByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4fd6-106">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4fd6-106">RemoveByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlAuditSetting -InputObject <PSSynapseWorkspace> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4fd6-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4fd6-107">RemoveByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlAuditSetting -ResourceId <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4fd6-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="a4fd6-108">DESCRIPTION</span></span>
<span data-ttu-id="a4fd6-109">Polecenie cmdlet **Reset-AzSynapseSqlAuditSetting** usuwa ustawienia inspekcji obszaru roboczego analizy Synapse Analytics platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a4fd6-109">The **Reset-AzSynapseSqlAuditSetting** cmdlet removes the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="a4fd6-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a4fd6-110">EXAMPLES</span></span>

### <span data-ttu-id="a4fd6-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a4fd6-111">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="a4fd6-112">To polecenie usuwa ustawienia inspekcji obszaru roboczego analizy Azure Synapse Analytics o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="a4fd6-112">This command removes the auditing settings of an Azure Synapse Analytics Workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="a4fd6-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a4fd6-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Reset-AzSynapseSqlAuditSetting
```

<span data-ttu-id="a4fd6-114">To polecenie usuwa z potoku ustawienia inspekcji obszaru roboczego analizy Azure Synapse Analytics o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="a4fd6-114">This command removes the auditing settings of an Azure Synapse Analytics Workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="a4fd6-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4fd6-115">PARAMETERS</span></span>

### <span data-ttu-id="a4fd6-116">— AsJob</span><span class="sxs-lookup"><span data-stu-id="a4fd6-116">-AsJob</span></span>
<span data-ttu-id="a4fd6-117">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a4fd6-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a4fd6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4fd6-118">-DefaultProfile</span></span>
<span data-ttu-id="a4fd6-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a4fd6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4fd6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4fd6-120">-InputObject</span></span>
<span data-ttu-id="a4fd6-121">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="a4fd6-121">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4fd6-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a4fd6-122">-PassThru</span></span>
<span data-ttu-id="a4fd6-123">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="a4fd6-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="a4fd6-124">Jeśli ten przełącznik zostanie określony, zostanie on podany jako prawda, jeśli zostanie pomyślnie określony.</span><span class="sxs-lookup"><span data-stu-id="a4fd6-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="a4fd6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4fd6-125">-ResourceGroupName</span></span>
<span data-ttu-id="a4fd6-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a4fd6-126">Resource group name.</span></span>

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

### <span data-ttu-id="a4fd6-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4fd6-127">-ResourceId</span></span>
<span data-ttu-id="a4fd6-128">Identyfikator zasobu obszaru roboczego programu Synapse.</span><span class="sxs-lookup"><span data-stu-id="a4fd6-128">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="a4fd6-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a4fd6-129">-WorkspaceName</span></span>
<span data-ttu-id="a4fd6-130">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="a4fd6-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a4fd6-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a4fd6-131">-Confirm</span></span>
<span data-ttu-id="a4fd6-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a4fd6-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4fd6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4fd6-133">-WhatIf</span></span>
<span data-ttu-id="a4fd6-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4fd6-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4fd6-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a4fd6-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4fd6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4fd6-136">CommonParameters</span></span>
<span data-ttu-id="a4fd6-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4fd6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4fd6-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a4fd6-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4fd6-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a4fd6-139">INPUTS</span></span>

### <span data-ttu-id="a4fd6-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a4fd6-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="a4fd6-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a4fd6-141">OUTPUTS</span></span>

### <span data-ttu-id="a4fd6-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a4fd6-142">System.Boolean</span></span>

## <span data-ttu-id="a4fd6-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a4fd6-143">NOTES</span></span>

## <span data-ttu-id="a4fd6-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a4fd6-144">RELATED LINKS</span></span>
