---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataFlow.md
ms.openlocfilehash: 2d0bec0c86f51771e971ca2c6b5a22c32f8ee687
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501318"
---
# <span data-ttu-id="b0490-101">Remove-AzSynapseDataFlow</span><span class="sxs-lookup"><span data-stu-id="b0490-101">Remove-AzSynapseDataFlow</span></span>

## <span data-ttu-id="b0490-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b0490-102">SYNOPSIS</span></span>
<span data-ttu-id="b0490-103">Usuwa przepływ danych z obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="b0490-103">Removes a data flow from workspace.</span></span>

## <span data-ttu-id="b0490-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b0490-104">SYNTAX</span></span>

### <span data-ttu-id="b0490-105">RemoveByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b0490-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseDataFlow -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0490-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="b0490-106">RemoveByObject</span></span>
```
Remove-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0490-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="b0490-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseDataFlow -InputObject <PSDataFlowResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0490-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b0490-108">DESCRIPTION</span></span>
<span data-ttu-id="b0490-109">Polecenie cmdlet **Remove-AzSynapseDataFlow** usuwa przepływ danych z obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="b0490-109">The **Remove-AzSynapseDataFlow** cmdlet removes a data flow from workspace.</span></span>

## <span data-ttu-id="b0490-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b0490-110">EXAMPLES</span></span>

### <span data-ttu-id="b0490-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b0490-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow
```

<span data-ttu-id="b0490-112">To polecenie usuwa przepływ danych o nazwie ContosoDataFlow z obszaru roboczego o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="b0490-112">This command removes the data flow named ContosoDataFlow from the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="b0490-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b0490-113">PARAMETERS</span></span>

### <span data-ttu-id="b0490-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b0490-114">-AsJob</span></span>
<span data-ttu-id="b0490-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b0490-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b0490-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0490-116">-DefaultProfile</span></span>
<span data-ttu-id="b0490-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b0490-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0490-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b0490-118">-Force</span></span>
<span data-ttu-id="b0490-119">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b0490-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b0490-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b0490-120">-InputObject</span></span>
<span data-ttu-id="b0490-121">Obiekt przepływu danych.</span><span class="sxs-lookup"><span data-stu-id="b0490-121">The data flow object.</span></span>

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

### <span data-ttu-id="b0490-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b0490-122">-Name</span></span>
<span data-ttu-id="b0490-123">Nazwa przepływu danych.</span><span class="sxs-lookup"><span data-stu-id="b0490-123">The data flow name.</span></span>

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

### <span data-ttu-id="b0490-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b0490-124">-PassThru</span></span>
<span data-ttu-id="b0490-125">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="b0490-125">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="b0490-126">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="b0490-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="b0490-127">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="b0490-127">-WorkspaceName</span></span>
<span data-ttu-id="b0490-128">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="b0490-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="b0490-129">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="b0490-129">-WorkspaceObject</span></span>
<span data-ttu-id="b0490-130">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="b0490-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="b0490-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b0490-131">-Confirm</span></span>
<span data-ttu-id="b0490-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0490-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0490-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0490-133">-WhatIf</span></span>
<span data-ttu-id="b0490-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0490-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0490-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b0490-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0490-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0490-136">CommonParameters</span></span>
<span data-ttu-id="b0490-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0490-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0490-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b0490-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0490-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b0490-139">INPUTS</span></span>

### <span data-ttu-id="b0490-140">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b0490-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="b0490-141">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span><span class="sxs-lookup"><span data-stu-id="b0490-141">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span></span>

## <span data-ttu-id="b0490-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b0490-142">OUTPUTS</span></span>

### <span data-ttu-id="b0490-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b0490-143">System.Boolean</span></span>

## <span data-ttu-id="b0490-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b0490-144">NOTES</span></span>

## <span data-ttu-id="b0490-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b0490-145">RELATED LINKS</span></span>
