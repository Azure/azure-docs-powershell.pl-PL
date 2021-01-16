---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/resume-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Resume-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Resume-AzSynapseSqlPool.md
ms.openlocfilehash: ea27b23174d9555e4153dc5ef8c4d053ef5a49b3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368944"
---
# <span data-ttu-id="e9648-101">Resume-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="e9648-101">Resume-AzSynapseSqlPool</span></span>

## <span data-ttu-id="e9648-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e9648-102">SYNOPSIS</span></span>
<span data-ttu-id="e9648-103">Wznawia pulę Synapse analizy SQL.</span><span class="sxs-lookup"><span data-stu-id="e9648-103">Resumes a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="e9648-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e9648-104">SYNTAX</span></span>

### <span data-ttu-id="e9648-105">ResumeByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e9648-105">ResumeByNameParameterSet (Default)</span></span>
```
Resume-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9648-106">ResumeByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9648-106">ResumeByParentObjectParameterSet</span></span>
```
Resume-AzSynapseSqlPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9648-107">ResumeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9648-107">ResumeByInputObjectParameterSet</span></span>
```
Resume-AzSynapseSqlPool -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9648-108">ResumeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9648-108">ResumeByResourceIdParameterSet</span></span>
```
Resume-AzSynapseSqlPool -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9648-109">Opis</span><span class="sxs-lookup"><span data-stu-id="e9648-109">DESCRIPTION</span></span>
<span data-ttu-id="e9648-110">Polecenie cmdlet **Resume-AzSynapseSqlPool** WZNAWIA pulę SQL usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="e9648-110">The **Resume-AzSynapseSqlPool** cmdlet resumes an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="e9648-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e9648-111">EXAMPLES</span></span>

### <span data-ttu-id="e9648-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e9648-112">Example 1</span></span>
```powershell
PS C:\> Resume-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="e9648-113">To polecenie wznawia zawieszoną pulę platformy Azure Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="e9648-113">This command resumes a suspended Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="e9648-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e9648-114">PARAMETERS</span></span>

### <span data-ttu-id="e9648-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e9648-115">-AsJob</span></span>
<span data-ttu-id="e9648-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e9648-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e9648-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9648-117">-DefaultProfile</span></span>
<span data-ttu-id="e9648-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e9648-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9648-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e9648-119">-InputObject</span></span>
<span data-ttu-id="e9648-120">Obiekt wejściowy zestawu SQL, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="e9648-120">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: ResumeByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9648-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e9648-121">-Name</span></span>
<span data-ttu-id="e9648-122">Nazwa puli SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="e9648-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ResumeByNameParameterSet, ResumeByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9648-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e9648-123">-PassThru</span></span>
<span data-ttu-id="e9648-124">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="e9648-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="e9648-125">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="e9648-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="e9648-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9648-126">-ResourceGroupName</span></span>
<span data-ttu-id="e9648-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e9648-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResumeByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9648-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e9648-128">-ResourceId</span></span>
<span data-ttu-id="e9648-129">Identyfikator zasobu puli SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="e9648-129">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ResumeByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9648-130">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="e9648-130">-WorkspaceName</span></span>
<span data-ttu-id="e9648-131">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="e9648-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ResumeByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9648-132">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="e9648-132">-WorkspaceObject</span></span>
<span data-ttu-id="e9648-133">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="e9648-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: ResumeByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9648-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e9648-134">-Confirm</span></span>
<span data-ttu-id="e9648-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9648-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9648-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9648-136">-WhatIf</span></span>
<span data-ttu-id="e9648-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9648-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9648-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e9648-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9648-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9648-139">CommonParameters</span></span>
<span data-ttu-id="e9648-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9648-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9648-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e9648-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9648-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e9648-142">INPUTS</span></span>

### <span data-ttu-id="e9648-143">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e9648-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="e9648-144">Microsoft. Azure. Commands. Synapse. models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="e9648-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="e9648-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e9648-145">OUTPUTS</span></span>

### <span data-ttu-id="e9648-146">Microsoft. Azure. Commands. Synapse. models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="e9648-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="e9648-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e9648-147">NOTES</span></span>

## <span data-ttu-id="e9648-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e9648-148">RELATED LINKS</span></span>
