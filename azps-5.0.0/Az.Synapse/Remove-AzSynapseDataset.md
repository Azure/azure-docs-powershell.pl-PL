---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataset.md
ms.openlocfilehash: 712aa1012269c6207b078fefa3a04a46bea4c573
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233759"
---
# <span data-ttu-id="7387d-101">Remove-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="7387d-101">Remove-AzSynapseDataset</span></span>

## <span data-ttu-id="7387d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7387d-102">SYNOPSIS</span></span>
<span data-ttu-id="7387d-103">Umożliwia usunięcie zestawu danych z obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="7387d-103">Removes a dataset from workspace.</span></span>

## <span data-ttu-id="7387d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7387d-104">SYNTAX</span></span>

### <span data-ttu-id="7387d-105">RemoveByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7387d-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseDataset -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7387d-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="7387d-106">RemoveByObject</span></span>
```
Remove-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7387d-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="7387d-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseDataset -InputObject <PSDatasetResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7387d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="7387d-108">DESCRIPTION</span></span>
<span data-ttu-id="7387d-109">Polecenie cmdlet **Remove-AzSynapseDataset** umożliwia usunięcie zestawu danych z obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="7387d-109">The **Remove-AzSynapseDataset** cmdlet removes a dataset from workspace.</span></span>

## <span data-ttu-id="7387d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7387d-110">EXAMPLES</span></span>

### <span data-ttu-id="7387d-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7387d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset
```

<span data-ttu-id="7387d-112">To polecenie usuwa zestaw danych o nazwie ContosoDataset z obszaru roboczego o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="7387d-112">This command removes the dataset named ContosoDataset from the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="7387d-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7387d-113">PARAMETERS</span></span>

### <span data-ttu-id="7387d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7387d-114">-AsJob</span></span>
<span data-ttu-id="7387d-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="7387d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7387d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7387d-116">-DefaultProfile</span></span>
<span data-ttu-id="7387d-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7387d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7387d-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7387d-118">-InputObject</span></span>
<span data-ttu-id="7387d-119">Obiekt DataSet.</span><span class="sxs-lookup"><span data-stu-id="7387d-119">The dataset object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7387d-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7387d-120">-Name</span></span>
<span data-ttu-id="7387d-121">Nazwa zestawu danych.</span><span class="sxs-lookup"><span data-stu-id="7387d-121">The dataset name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: DatasetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7387d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7387d-122">-PassThru</span></span>
<span data-ttu-id="7387d-123">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="7387d-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="7387d-124">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="7387d-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="7387d-125">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="7387d-125">-WorkspaceName</span></span>
<span data-ttu-id="7387d-126">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="7387d-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="7387d-127">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="7387d-127">-WorkspaceObject</span></span>
<span data-ttu-id="7387d-128">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="7387d-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="7387d-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7387d-129">-Confirm</span></span>
<span data-ttu-id="7387d-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7387d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7387d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7387d-131">-WhatIf</span></span>
<span data-ttu-id="7387d-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7387d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7387d-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7387d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7387d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7387d-134">CommonParameters</span></span>
<span data-ttu-id="7387d-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7387d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7387d-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7387d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7387d-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7387d-137">INPUTS</span></span>

### <span data-ttu-id="7387d-138">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="7387d-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="7387d-139">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="7387d-139">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="7387d-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7387d-140">OUTPUTS</span></span>

### <span data-ttu-id="7387d-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7387d-141">System.Boolean</span></span>

## <span data-ttu-id="7387d-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7387d-142">NOTES</span></span>

## <span data-ttu-id="7387d-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7387d-143">RELATED LINKS</span></span>
