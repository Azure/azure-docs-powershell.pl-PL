---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/reset-azsynapsesqlauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAuditSetting.md
ms.openlocfilehash: b25ca2a026cf5d82aa25f69868ca8605fd75bced
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383266"
---
# <span data-ttu-id="89f50-101">Reset-AzSynapseSqlAuditSetting</span><span class="sxs-lookup"><span data-stu-id="89f50-101">Reset-AzSynapseSqlAuditSetting</span></span>

## <span data-ttu-id="89f50-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="89f50-102">SYNOPSIS</span></span>
<span data-ttu-id="89f50-103">Usuwa ustawienia inspekcji obszaru roboczego analizy usługi Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="89f50-103">Removes the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="89f50-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="89f50-104">SYNTAX</span></span>

### <span data-ttu-id="89f50-105">RemoveByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="89f50-105">RemoveByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89f50-106">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="89f50-106">RemoveByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlAuditSetting -InputObject <PSSynapseWorkspace> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89f50-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="89f50-107">RemoveByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlAuditSetting -ResourceId <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89f50-108">Opis</span><span class="sxs-lookup"><span data-stu-id="89f50-108">DESCRIPTION</span></span>
<span data-ttu-id="89f50-109">Polecenie cmdlet **Reset-AzSynapseSqlAuditSetting** usuwa ustawienia inspekcji obszaru roboczego funkcji Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="89f50-109">The **Reset-AzSynapseSqlAuditSetting** cmdlet removes the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="89f50-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="89f50-110">EXAMPLES</span></span>

### <span data-ttu-id="89f50-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="89f50-111">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="89f50-112">To polecenie usuwa ustawienia inspekcji obszaru roboczego usługi Azure Synapse analiza o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="89f50-112">This command removes the auditing settings of an Azure Synapse Analytics Workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="89f50-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="89f50-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Reset-AzSynapseSqlAuditSetting
```

<span data-ttu-id="89f50-114">To polecenie usuwa ustawienia inspekcji obszaru roboczego usługi Azure Synapse Analytics o nazwie ContosoWorkspace za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="89f50-114">This command removes the auditing settings of an Azure Synapse Analytics Workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="89f50-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="89f50-115">PARAMETERS</span></span>

### <span data-ttu-id="89f50-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="89f50-116">-AsJob</span></span>
<span data-ttu-id="89f50-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="89f50-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="89f50-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89f50-118">-DefaultProfile</span></span>
<span data-ttu-id="89f50-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="89f50-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89f50-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="89f50-120">-InputObject</span></span>
<span data-ttu-id="89f50-121">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="89f50-121">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="89f50-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="89f50-122">-PassThru</span></span>
<span data-ttu-id="89f50-123">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="89f50-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="89f50-124">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="89f50-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="89f50-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89f50-125">-ResourceGroupName</span></span>
<span data-ttu-id="89f50-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="89f50-126">Resource group name.</span></span>

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

### <span data-ttu-id="89f50-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="89f50-127">-ResourceId</span></span>
<span data-ttu-id="89f50-128">Identyfikator zasobu obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="89f50-128">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="89f50-129">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="89f50-129">-WorkspaceName</span></span>
<span data-ttu-id="89f50-130">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="89f50-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="89f50-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="89f50-131">-Confirm</span></span>
<span data-ttu-id="89f50-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89f50-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89f50-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89f50-133">-WhatIf</span></span>
<span data-ttu-id="89f50-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89f50-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89f50-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="89f50-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89f50-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89f50-136">CommonParameters</span></span>
<span data-ttu-id="89f50-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89f50-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89f50-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="89f50-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89f50-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="89f50-139">INPUTS</span></span>

### <span data-ttu-id="89f50-140">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="89f50-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="89f50-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="89f50-141">OUTPUTS</span></span>

### <span data-ttu-id="89f50-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="89f50-142">System.Boolean</span></span>

## <span data-ttu-id="89f50-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="89f50-143">NOTES</span></span>

## <span data-ttu-id="89f50-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="89f50-144">RELATED LINKS</span></span>
