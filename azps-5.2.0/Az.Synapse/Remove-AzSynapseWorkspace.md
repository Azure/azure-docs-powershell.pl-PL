---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseWorkspace.md
ms.openlocfilehash: fbdca80b33dd15e34a958cb63a41377b400d03ce
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334717"
---
# <span data-ttu-id="044ea-101">Remove-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="044ea-101">Remove-AzSynapseWorkspace</span></span>

## <span data-ttu-id="044ea-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="044ea-102">SYNOPSIS</span></span>
<span data-ttu-id="044ea-103">Usuwa obszar roboczy analizy Synapse.</span><span class="sxs-lookup"><span data-stu-id="044ea-103">Deletes a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="044ea-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="044ea-104">SYNTAX</span></span>

### <span data-ttu-id="044ea-105">DeleteByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="044ea-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseWorkspace [-ResourceGroupName <String>] -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="044ea-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="044ea-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseWorkspace -InputObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="044ea-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="044ea-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseWorkspace -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="044ea-108">Opis</span><span class="sxs-lookup"><span data-stu-id="044ea-108">DESCRIPTION</span></span>
<span data-ttu-id="044ea-109">Polecenie cmdlet **Remove-AzSynapseWorkspace** trwale usuwa obszar roboczy usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="044ea-109">The **Remove-AzSynapseWorkspace** cmdlet permanently deletes an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="044ea-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="044ea-110">EXAMPLES</span></span>

### <span data-ttu-id="044ea-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="044ea-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="044ea-112">To polecenie usuwa obszar roboczy usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="044ea-112">This command deletes an Azure Synapse Analytics workspace.</span></span>

### <span data-ttu-id="044ea-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="044ea-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseWorkspace
```

<span data-ttu-id="044ea-114">To polecenie usuwa obszar roboczy usługi Azure Synapse Analytics za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="044ea-114">This command deletes an Azure Synapse Analytics workspace through pipeline.</span></span>

### <span data-ttu-id="044ea-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="044ea-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace
```

<span data-ttu-id="044ea-116">To polecenie usuwa obszar roboczy usługi Azure Synapse Analytics za pomocą potoku z określonym IDENTYFIKATORem zasobu.</span><span class="sxs-lookup"><span data-stu-id="044ea-116">This command deletes an Azure Synapse Analytics workspace through pipeline with the specified resource ID.</span></span>

## <span data-ttu-id="044ea-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="044ea-117">PARAMETERS</span></span>

### <span data-ttu-id="044ea-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="044ea-118">-AsJob</span></span>
<span data-ttu-id="044ea-119">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="044ea-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="044ea-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="044ea-120">-DefaultProfile</span></span>
<span data-ttu-id="044ea-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="044ea-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="044ea-122">-Force</span><span class="sxs-lookup"><span data-stu-id="044ea-122">-Force</span></span>
<span data-ttu-id="044ea-123">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="044ea-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="044ea-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="044ea-124">-InputObject</span></span>
<span data-ttu-id="044ea-125">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="044ea-125">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="044ea-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="044ea-126">-Name</span></span>
<span data-ttu-id="044ea-127">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="044ea-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="044ea-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="044ea-128">-PassThru</span></span>
<span data-ttu-id="044ea-129">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="044ea-129">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="044ea-130">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="044ea-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="044ea-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="044ea-131">-ResourceGroupName</span></span>
<span data-ttu-id="044ea-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="044ea-132">Resource group name.</span></span>

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

### <span data-ttu-id="044ea-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="044ea-133">-ResourceId</span></span>
<span data-ttu-id="044ea-134">Identyfikator zasobu obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="044ea-134">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="044ea-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="044ea-135">-Confirm</span></span>
<span data-ttu-id="044ea-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="044ea-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="044ea-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="044ea-137">-WhatIf</span></span>
<span data-ttu-id="044ea-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="044ea-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="044ea-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="044ea-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="044ea-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="044ea-140">CommonParameters</span></span>
<span data-ttu-id="044ea-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="044ea-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="044ea-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="044ea-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="044ea-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="044ea-143">INPUTS</span></span>

### <span data-ttu-id="044ea-144">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="044ea-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="044ea-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="044ea-145">OUTPUTS</span></span>

### <span data-ttu-id="044ea-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="044ea-146">System.Boolean</span></span>

## <span data-ttu-id="044ea-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="044ea-147">NOTES</span></span>

## <span data-ttu-id="044ea-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="044ea-148">RELATED LINKS</span></span>
