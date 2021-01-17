---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataFlow.md
ms.openlocfilehash: 2d0bec0c86f51771e971ca2c6b5a22c32f8ee687
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340141"
---
# <span data-ttu-id="3c6c5-101">Remove-AzSynapseDataFlow</span><span class="sxs-lookup"><span data-stu-id="3c6c5-101">Remove-AzSynapseDataFlow</span></span>

## <span data-ttu-id="3c6c5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3c6c5-102">SYNOPSIS</span></span>
<span data-ttu-id="3c6c5-103">Usuwa przepływ danych z obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="3c6c5-103">Removes a data flow from workspace.</span></span>

## <span data-ttu-id="3c6c5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3c6c5-104">SYNTAX</span></span>

### <span data-ttu-id="3c6c5-105">RemoveByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3c6c5-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseDataFlow -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c6c5-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="3c6c5-106">RemoveByObject</span></span>
```
Remove-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c6c5-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="3c6c5-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseDataFlow -InputObject <PSDataFlowResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c6c5-108">Opis</span><span class="sxs-lookup"><span data-stu-id="3c6c5-108">DESCRIPTION</span></span>
<span data-ttu-id="3c6c5-109">Polecenie cmdlet **Remove-AzSynapseDataFlow** usuwa przepływ danych z obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="3c6c5-109">The **Remove-AzSynapseDataFlow** cmdlet removes a data flow from workspace.</span></span>

## <span data-ttu-id="3c6c5-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3c6c5-110">EXAMPLES</span></span>

### <span data-ttu-id="3c6c5-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3c6c5-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow
```

<span data-ttu-id="3c6c5-112">To polecenie usuwa przepływ danych o nazwie ContosoDataFlow z obszaru roboczego o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="3c6c5-112">This command removes the data flow named ContosoDataFlow from the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="3c6c5-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3c6c5-113">PARAMETERS</span></span>

### <span data-ttu-id="3c6c5-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3c6c5-114">-AsJob</span></span>
<span data-ttu-id="3c6c5-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="3c6c5-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3c6c5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c6c5-116">-DefaultProfile</span></span>
<span data-ttu-id="3c6c5-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3c6c5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c6c5-118">-Force</span><span class="sxs-lookup"><span data-stu-id="3c6c5-118">-Force</span></span>
<span data-ttu-id="3c6c5-119">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3c6c5-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="3c6c5-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3c6c5-120">-InputObject</span></span>
<span data-ttu-id="3c6c5-121">Obiekt przepływu danych.</span><span class="sxs-lookup"><span data-stu-id="3c6c5-121">The data flow object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c6c5-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3c6c5-122">-Name</span></span>
<span data-ttu-id="3c6c5-123">Nazwa przepływu danych.</span><span class="sxs-lookup"><span data-stu-id="3c6c5-123">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: DataFlowName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c6c5-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3c6c5-124">-PassThru</span></span>
<span data-ttu-id="3c6c5-125">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="3c6c5-125">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="3c6c5-126">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="3c6c5-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="3c6c5-127">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="3c6c5-127">-WorkspaceName</span></span>
<span data-ttu-id="3c6c5-128">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="3c6c5-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c6c5-129">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="3c6c5-129">-WorkspaceObject</span></span>
<span data-ttu-id="3c6c5-130">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="3c6c5-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c6c5-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3c6c5-131">-Confirm</span></span>
<span data-ttu-id="3c6c5-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c6c5-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c6c5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c6c5-133">-WhatIf</span></span>
<span data-ttu-id="3c6c5-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c6c5-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c6c5-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3c6c5-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c6c5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c6c5-136">CommonParameters</span></span>
<span data-ttu-id="3c6c5-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c6c5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c6c5-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3c6c5-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c6c5-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3c6c5-139">INPUTS</span></span>

### <span data-ttu-id="3c6c5-140">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="3c6c5-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="3c6c5-141">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span><span class="sxs-lookup"><span data-stu-id="3c6c5-141">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span></span>

## <span data-ttu-id="3c6c5-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3c6c5-142">OUTPUTS</span></span>

### <span data-ttu-id="3c6c5-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3c6c5-143">System.Boolean</span></span>

## <span data-ttu-id="3c6c5-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3c6c5-144">NOTES</span></span>

## <span data-ttu-id="3c6c5-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3c6c5-145">RELATED LINKS</span></span>
