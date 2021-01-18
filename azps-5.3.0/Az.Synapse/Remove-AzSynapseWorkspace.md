---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseWorkspace.md
ms.openlocfilehash: fbdca80b33dd15e34a958cb63a41377b400d03ce
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501315"
---
# <span data-ttu-id="2bf29-101">Remove-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="2bf29-101">Remove-AzSynapseWorkspace</span></span>

## <span data-ttu-id="2bf29-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2bf29-102">SYNOPSIS</span></span>
<span data-ttu-id="2bf29-103">Usuwa obszar roboczy analizy Synapse.</span><span class="sxs-lookup"><span data-stu-id="2bf29-103">Deletes a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="2bf29-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2bf29-104">SYNTAX</span></span>

### <span data-ttu-id="2bf29-105">DeleteByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2bf29-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseWorkspace [-ResourceGroupName <String>] -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2bf29-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2bf29-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseWorkspace -InputObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2bf29-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2bf29-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseWorkspace -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2bf29-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2bf29-108">DESCRIPTION</span></span>
<span data-ttu-id="2bf29-109">Polecenie cmdlet **Remove-AzSynapseWorkspace** trwale usuwa obszar roboczy usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="2bf29-109">The **Remove-AzSynapseWorkspace** cmdlet permanently deletes an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="2bf29-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2bf29-110">EXAMPLES</span></span>

### <span data-ttu-id="2bf29-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2bf29-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="2bf29-112">To polecenie usuwa obszar roboczy usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="2bf29-112">This command deletes an Azure Synapse Analytics workspace.</span></span>

### <span data-ttu-id="2bf29-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="2bf29-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseWorkspace
```

<span data-ttu-id="2bf29-114">To polecenie usuwa obszar roboczy usługi Azure Synapse Analytics za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="2bf29-114">This command deletes an Azure Synapse Analytics workspace through pipeline.</span></span>

### <span data-ttu-id="2bf29-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="2bf29-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace
```

<span data-ttu-id="2bf29-116">To polecenie usuwa obszar roboczy usługi Azure Synapse Analytics za pomocą potoku z określonym IDENTYFIKATORem zasobu.</span><span class="sxs-lookup"><span data-stu-id="2bf29-116">This command deletes an Azure Synapse Analytics workspace through pipeline with the specified resource ID.</span></span>

## <span data-ttu-id="2bf29-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2bf29-117">PARAMETERS</span></span>

### <span data-ttu-id="2bf29-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2bf29-118">-AsJob</span></span>
<span data-ttu-id="2bf29-119">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="2bf29-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2bf29-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bf29-120">-DefaultProfile</span></span>
<span data-ttu-id="2bf29-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2bf29-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2bf29-122">-Force</span><span class="sxs-lookup"><span data-stu-id="2bf29-122">-Force</span></span>
<span data-ttu-id="2bf29-123">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2bf29-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2bf29-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2bf29-124">-InputObject</span></span>
<span data-ttu-id="2bf29-125">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="2bf29-125">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="2bf29-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2bf29-126">-Name</span></span>
<span data-ttu-id="2bf29-127">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="2bf29-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="2bf29-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2bf29-128">-PassThru</span></span>
<span data-ttu-id="2bf29-129">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="2bf29-129">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="2bf29-130">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="2bf29-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="2bf29-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bf29-131">-ResourceGroupName</span></span>
<span data-ttu-id="2bf29-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2bf29-132">Resource group name.</span></span>

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

### <span data-ttu-id="2bf29-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2bf29-133">-ResourceId</span></span>
<span data-ttu-id="2bf29-134">Identyfikator zasobu obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="2bf29-134">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="2bf29-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2bf29-135">-Confirm</span></span>
<span data-ttu-id="2bf29-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2bf29-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2bf29-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bf29-137">-WhatIf</span></span>
<span data-ttu-id="2bf29-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2bf29-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2bf29-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2bf29-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2bf29-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bf29-140">CommonParameters</span></span>
<span data-ttu-id="2bf29-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bf29-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bf29-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2bf29-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bf29-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2bf29-143">INPUTS</span></span>

### <span data-ttu-id="2bf29-144">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="2bf29-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="2bf29-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2bf29-145">OUTPUTS</span></span>

### <span data-ttu-id="2bf29-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2bf29-146">System.Boolean</span></span>

## <span data-ttu-id="2bf29-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2bf29-147">NOTES</span></span>

## <span data-ttu-id="2bf29-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2bf29-148">RELATED LINKS</span></span>
