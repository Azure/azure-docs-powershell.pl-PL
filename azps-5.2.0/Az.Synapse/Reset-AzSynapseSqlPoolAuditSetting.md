---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/reset-azsynapsesqlpoolauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlPoolAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlPoolAuditSetting.md
ms.openlocfilehash: 77299e9424f0a194776b1114146b76ef2be3329f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329056"
---
# <span data-ttu-id="74a0b-101">Reset-AzSynapseSqlPoolAuditSetting</span><span class="sxs-lookup"><span data-stu-id="74a0b-101">Reset-AzSynapseSqlPoolAuditSetting</span></span>

## <span data-ttu-id="74a0b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="74a0b-102">SYNOPSIS</span></span>
<span data-ttu-id="74a0b-103">Usuwa ustawienia inspekcji puli SQL usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="74a0b-103">Removes the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="74a0b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="74a0b-104">SYNTAX</span></span>

### <span data-ttu-id="74a0b-105">RemoveByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="74a0b-105">RemoveByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlPoolAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74a0b-106">RemoveByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="74a0b-106">RemoveByParentObjectParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAuditSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74a0b-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="74a0b-107">RemoveByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAuditSetting -InputObject <PSSynapseSqlPool> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74a0b-108">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="74a0b-108">RemoveByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAuditSetting -ResourceId <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74a0b-109">Opis</span><span class="sxs-lookup"><span data-stu-id="74a0b-109">DESCRIPTION</span></span>
<span data-ttu-id="74a0b-110">Polecenie cmdlet **Reset-AzSynapseSqlPoolAuditSetting** usuwa ustawienia inspekcji puli SQL usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="74a0b-110">The **Reset-AzSynapseSqlPoolAuditSetting** cmdlet removes the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="74a0b-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="74a0b-111">EXAMPLES</span></span>

### <span data-ttu-id="74a0b-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="74a0b-112">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="74a0b-113">To polecenie usuwa ustawienia inspekcji puli SQL o nazwie ContosoSqlPool w obszarze roboczym ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="74a0b-113">This command removes the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="74a0b-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="74a0b-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Reset-AzSynapseSqlPoolAuditSetting
```

<span data-ttu-id="74a0b-115">To polecenie usuwa ustawienia inspekcji puli SQL o nazwie ContosoSqlPool w obszarze roboczym ContosoWorkspace za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="74a0b-115">This command removes the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="74a0b-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="74a0b-116">PARAMETERS</span></span>

### <span data-ttu-id="74a0b-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="74a0b-117">-AsJob</span></span>
<span data-ttu-id="74a0b-118">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="74a0b-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="74a0b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74a0b-119">-DefaultProfile</span></span>
<span data-ttu-id="74a0b-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="74a0b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74a0b-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="74a0b-121">-InputObject</span></span>
<span data-ttu-id="74a0b-122">Obiekt wejściowy zestawu SQL, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="74a0b-122">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="74a0b-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="74a0b-123">-Name</span></span>
<span data-ttu-id="74a0b-124">Nazwa puli SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="74a0b-124">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="74a0b-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="74a0b-125">-PassThru</span></span>
<span data-ttu-id="74a0b-126">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="74a0b-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="74a0b-127">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="74a0b-127">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="74a0b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74a0b-128">-ResourceGroupName</span></span>
<span data-ttu-id="74a0b-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="74a0b-129">Resource group name.</span></span>

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

### <span data-ttu-id="74a0b-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="74a0b-130">-ResourceId</span></span>
<span data-ttu-id="74a0b-131">Identyfikator zasobu puli SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="74a0b-131">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="74a0b-132">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="74a0b-132">-WorkspaceName</span></span>
<span data-ttu-id="74a0b-133">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="74a0b-133">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="74a0b-134">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="74a0b-134">-WorkspaceObject</span></span>
<span data-ttu-id="74a0b-135">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="74a0b-135">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="74a0b-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="74a0b-136">-Confirm</span></span>
<span data-ttu-id="74a0b-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74a0b-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74a0b-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74a0b-138">-WhatIf</span></span>
<span data-ttu-id="74a0b-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74a0b-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74a0b-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="74a0b-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74a0b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74a0b-141">CommonParameters</span></span>
<span data-ttu-id="74a0b-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74a0b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74a0b-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="74a0b-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74a0b-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="74a0b-144">INPUTS</span></span>

### <span data-ttu-id="74a0b-145">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="74a0b-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="74a0b-146">Microsoft. Azure. Commands. Synapse. models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="74a0b-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="74a0b-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="74a0b-147">OUTPUTS</span></span>

### <span data-ttu-id="74a0b-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="74a0b-148">System.Boolean</span></span>

## <span data-ttu-id="74a0b-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="74a0b-149">NOTES</span></span>

## <span data-ttu-id="74a0b-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="74a0b-150">RELATED LINKS</span></span>
