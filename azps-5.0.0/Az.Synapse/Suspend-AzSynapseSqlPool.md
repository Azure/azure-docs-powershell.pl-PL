---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/suspend-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Suspend-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Suspend-AzSynapseSqlPool.md
ms.openlocfilehash: fef045417a9c6cb22cd3ec3651a5b27b127b3b9f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224129"
---
# <span data-ttu-id="a9246-101">Suspend-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="a9246-101">Suspend-AzSynapseSqlPool</span></span>

## <span data-ttu-id="a9246-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a9246-102">SYNOPSIS</span></span>
<span data-ttu-id="a9246-103">Wstrzymuje pulę Synapse analizy SQL.</span><span class="sxs-lookup"><span data-stu-id="a9246-103">Suspends a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="a9246-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a9246-104">SYNTAX</span></span>

### <span data-ttu-id="a9246-105">SuspendByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a9246-105">SuspendByNameParameterSet (Default)</span></span>
```
Suspend-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9246-106">SuspendByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9246-106">SuspendByParentObjectParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9246-107">SuspendByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9246-107">SuspendByInputObjectParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9246-108">SuspendByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9246-108">SuspendByResourceIdParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9246-109">Opis</span><span class="sxs-lookup"><span data-stu-id="a9246-109">DESCRIPTION</span></span>
<span data-ttu-id="a9246-110">Polecenie cmdlet **Suspend-AzSynapseSqlPool** wstrzymuje pulę SQL usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="a9246-110">The **Suspend-AzSynapseSqlPool** cmdlet suspends an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="a9246-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a9246-111">EXAMPLES</span></span>

### <span data-ttu-id="a9246-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a9246-112">Example 1</span></span>
```powershell
PS C:\> Suspend-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="a9246-113">To polecenie zawiesza aktywną pulę SQL usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="a9246-113">This command suspends an active Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="a9246-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a9246-114">PARAMETERS</span></span>

### <span data-ttu-id="a9246-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a9246-115">-AsJob</span></span>
<span data-ttu-id="a9246-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a9246-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a9246-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9246-117">-DefaultProfile</span></span>
<span data-ttu-id="a9246-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a9246-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9246-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a9246-119">-InputObject</span></span>
<span data-ttu-id="a9246-120">Obiekt wejściowy zestawu SQL, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="a9246-120">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SuspendByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9246-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a9246-121">-Name</span></span>
<span data-ttu-id="a9246-122">Nazwa puli SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="a9246-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByNameParameterSet, SuspendByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9246-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a9246-123">-PassThru</span></span>
<span data-ttu-id="a9246-124">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="a9246-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="a9246-125">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="a9246-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="a9246-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9246-126">-ResourceGroupName</span></span>
<span data-ttu-id="a9246-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a9246-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9246-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9246-128">-ResourceId</span></span>
<span data-ttu-id="a9246-129">Identyfikator zasobu puli SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="a9246-129">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9246-130">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="a9246-130">-WorkspaceName</span></span>
<span data-ttu-id="a9246-131">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="a9246-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9246-132">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="a9246-132">-WorkspaceObject</span></span>
<span data-ttu-id="a9246-133">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="a9246-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SuspendByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9246-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a9246-134">-Confirm</span></span>
<span data-ttu-id="a9246-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9246-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9246-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9246-136">-WhatIf</span></span>
<span data-ttu-id="a9246-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9246-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9246-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a9246-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9246-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9246-139">CommonParameters</span></span>
<span data-ttu-id="a9246-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9246-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9246-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a9246-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9246-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a9246-142">INPUTS</span></span>

### <span data-ttu-id="a9246-143">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a9246-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="a9246-144">Microsoft. Azure. Commands. Synapse. models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="a9246-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="a9246-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a9246-145">OUTPUTS</span></span>

### <span data-ttu-id="a9246-146">Microsoft. Azure. Commands. Synapse. models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="a9246-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="a9246-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a9246-147">NOTES</span></span>

## <span data-ttu-id="a9246-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a9246-148">RELATED LINKS</span></span>
