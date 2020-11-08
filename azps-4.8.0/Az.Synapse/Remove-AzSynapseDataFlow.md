---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataFlow.md
ms.openlocfilehash: dcfcd391d1103b0755a3ffae481e4f1bd5fde2c7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064387"
---
# <span data-ttu-id="a3c1d-101">Remove-AzSynapseDataFlow</span><span class="sxs-lookup"><span data-stu-id="a3c1d-101">Remove-AzSynapseDataFlow</span></span>

## <span data-ttu-id="a3c1d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a3c1d-102">SYNOPSIS</span></span>
<span data-ttu-id="a3c1d-103">Usuwa przepływ danych z obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="a3c1d-103">Removes a data flow from workspace.</span></span>

## <span data-ttu-id="a3c1d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a3c1d-104">SYNTAX</span></span>

### <span data-ttu-id="a3c1d-105">RemoveByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a3c1d-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseDataFlow -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3c1d-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="a3c1d-106">RemoveByObject</span></span>
```
Remove-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3c1d-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="a3c1d-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseDataFlow -InputObject <PSDataFlowResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3c1d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a3c1d-108">DESCRIPTION</span></span>
<span data-ttu-id="a3c1d-109">Polecenie cmdlet **Remove-AzSynapseDataFlow** usuwa przepływ danych z obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="a3c1d-109">The **Remove-AzSynapseDataFlow** cmdlet removes a data flow from workspace.</span></span>

## <span data-ttu-id="a3c1d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a3c1d-110">EXAMPLES</span></span>

### <span data-ttu-id="a3c1d-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a3c1d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow
```

<span data-ttu-id="a3c1d-112">To polecenie usuwa przepływ danych o nazwie ContosoDataFlow z obszaru roboczego o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="a3c1d-112">This command removes the data flow named ContosoDataFlow from the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="a3c1d-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a3c1d-113">PARAMETERS</span></span>

### <span data-ttu-id="a3c1d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a3c1d-114">-AsJob</span></span>
<span data-ttu-id="a3c1d-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a3c1d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a3c1d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3c1d-116">-DefaultProfile</span></span>
<span data-ttu-id="a3c1d-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a3c1d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3c1d-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a3c1d-118">-InputObject</span></span>
<span data-ttu-id="a3c1d-119">Obiekt przepływu danych.</span><span class="sxs-lookup"><span data-stu-id="a3c1d-119">The data flow object.</span></span>

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

### <span data-ttu-id="a3c1d-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a3c1d-120">-Name</span></span>
<span data-ttu-id="a3c1d-121">Nazwa przepływu danych.</span><span class="sxs-lookup"><span data-stu-id="a3c1d-121">The data flow name.</span></span>

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

### <span data-ttu-id="a3c1d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a3c1d-122">-PassThru</span></span>
<span data-ttu-id="a3c1d-123">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="a3c1d-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="a3c1d-124">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="a3c1d-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="a3c1d-125">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="a3c1d-125">-WorkspaceName</span></span>
<span data-ttu-id="a3c1d-126">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="a3c1d-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a3c1d-127">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="a3c1d-127">-WorkspaceObject</span></span>
<span data-ttu-id="a3c1d-128">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="a3c1d-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a3c1d-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a3c1d-129">-Confirm</span></span>
<span data-ttu-id="a3c1d-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3c1d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3c1d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3c1d-131">-WhatIf</span></span>
<span data-ttu-id="a3c1d-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3c1d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3c1d-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a3c1d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3c1d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3c1d-134">CommonParameters</span></span>
<span data-ttu-id="a3c1d-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3c1d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3c1d-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a3c1d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3c1d-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a3c1d-137">INPUTS</span></span>

### <span data-ttu-id="a3c1d-138">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a3c1d-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="a3c1d-139">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span><span class="sxs-lookup"><span data-stu-id="a3c1d-139">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span></span>

## <span data-ttu-id="a3c1d-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a3c1d-140">OUTPUTS</span></span>

### <span data-ttu-id="a3c1d-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a3c1d-141">System.Boolean</span></span>

## <span data-ttu-id="a3c1d-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a3c1d-142">NOTES</span></span>

## <span data-ttu-id="a3c1d-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a3c1d-143">RELATED LINKS</span></span>
