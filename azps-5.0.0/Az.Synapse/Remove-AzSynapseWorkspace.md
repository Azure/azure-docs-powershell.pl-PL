---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseWorkspace.md
ms.openlocfilehash: dcc73c78334fba9823ddc1d26463422bcc388bf2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94231602"
---
# <span data-ttu-id="b2801-101">Remove-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b2801-101">Remove-AzSynapseWorkspace</span></span>

## <span data-ttu-id="b2801-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b2801-102">SYNOPSIS</span></span>
<span data-ttu-id="b2801-103">Usuwa obszar roboczy analizy Synapse.</span><span class="sxs-lookup"><span data-stu-id="b2801-103">Deletes a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="b2801-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b2801-104">SYNTAX</span></span>

### <span data-ttu-id="b2801-105">DeleteByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b2801-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseWorkspace [-ResourceGroupName <String>] -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2801-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2801-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseWorkspace -InputObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2801-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2801-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseWorkspace -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2801-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b2801-108">DESCRIPTION</span></span>
<span data-ttu-id="b2801-109">Polecenie cmdlet **Remove-AzSynapseWorkspace** trwale usuwa obszar roboczy usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="b2801-109">The **Remove-AzSynapseWorkspace** cmdlet permanently deletes an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="b2801-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b2801-110">EXAMPLES</span></span>

### <span data-ttu-id="b2801-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b2801-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="b2801-112">To polecenie usuwa obszar roboczy usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="b2801-112">This command deletes an Azure Synapse Analytics workspace.</span></span>

### <span data-ttu-id="b2801-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b2801-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseWorkspace
```

<span data-ttu-id="b2801-114">To polecenie usuwa obszar roboczy usługi Azure Synapse Analytics za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="b2801-114">This command deletes an Azure Synapse Analytics workspace through pipeline.</span></span>

### <span data-ttu-id="b2801-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="b2801-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace
```

<span data-ttu-id="b2801-116">To polecenie usuwa obszar roboczy usługi Azure Synapse Analytics za pomocą potoku z określonym IDENTYFIKATORem zasobu.</span><span class="sxs-lookup"><span data-stu-id="b2801-116">This command deletes an Azure Synapse Analytics workspace through pipeline with the specified resource ID.</span></span>

## <span data-ttu-id="b2801-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b2801-117">PARAMETERS</span></span>

### <span data-ttu-id="b2801-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b2801-118">-AsJob</span></span>
<span data-ttu-id="b2801-119">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b2801-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b2801-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2801-120">-DefaultProfile</span></span>
<span data-ttu-id="b2801-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b2801-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2801-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b2801-122">-InputObject</span></span>
<span data-ttu-id="b2801-123">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="b2801-123">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2801-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b2801-124">-Name</span></span>
<span data-ttu-id="b2801-125">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="b2801-125">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2801-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b2801-126">-PassThru</span></span>
<span data-ttu-id="b2801-127">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="b2801-127">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="b2801-128">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="b2801-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="b2801-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2801-129">-ResourceGroupName</span></span>
<span data-ttu-id="b2801-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b2801-130">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2801-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b2801-131">-ResourceId</span></span>
<span data-ttu-id="b2801-132">Identyfikator zasobu obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="b2801-132">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2801-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b2801-133">-Confirm</span></span>
<span data-ttu-id="b2801-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2801-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2801-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2801-135">-WhatIf</span></span>
<span data-ttu-id="b2801-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2801-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2801-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b2801-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2801-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2801-138">CommonParameters</span></span>
<span data-ttu-id="b2801-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2801-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2801-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b2801-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2801-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b2801-141">INPUTS</span></span>

### <span data-ttu-id="b2801-142">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b2801-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="b2801-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b2801-143">OUTPUTS</span></span>

### <span data-ttu-id="b2801-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b2801-144">System.Boolean</span></span>

## <span data-ttu-id="b2801-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b2801-145">NOTES</span></span>

## <span data-ttu-id="b2801-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b2801-146">RELATED LINKS</span></span>
