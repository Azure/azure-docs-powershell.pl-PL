---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseLinkedService.md
ms.openlocfilehash: c70cc0f8659a04e8a10a4fbd2b776d22fca6a616
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365015"
---
# <span data-ttu-id="4e2a3-101">Remove-AzSynapseLinkedService</span><span class="sxs-lookup"><span data-stu-id="4e2a3-101">Remove-AzSynapseLinkedService</span></span>

## <span data-ttu-id="4e2a3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4e2a3-102">SYNOPSIS</span></span>
<span data-ttu-id="4e2a3-103">Usuwa połączoną usługę z obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="4e2a3-103">Removes a linked service from workspace.</span></span>

## <span data-ttu-id="4e2a3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4e2a3-104">SYNTAX</span></span>

### <span data-ttu-id="4e2a3-105">RemoveByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4e2a3-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseLinkedService -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e2a3-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="4e2a3-106">RemoveByObject</span></span>
```
Remove-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e2a3-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="4e2a3-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseLinkedService -InputObject <PSLinkedServiceResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e2a3-108">Opis</span><span class="sxs-lookup"><span data-stu-id="4e2a3-108">DESCRIPTION</span></span>
<span data-ttu-id="4e2a3-109">Polecenie cmdlet **Remove-AzSynapseLinkedService** umożliwia usunięcie połączonej usługi z obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="4e2a3-109">The **Remove-AzSynapseLinkedService** cmdlet removes a linked service from workspace.</span></span>

## <span data-ttu-id="4e2a3-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4e2a3-110">EXAMPLES</span></span>

### <span data-ttu-id="4e2a3-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4e2a3-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
```

<span data-ttu-id="4e2a3-112">To polecenie powoduje usunięcie połączonej usługi o nazwie ContosoLinkedService z obszaru roboczego o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="4e2a3-112">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="4e2a3-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="4e2a3-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseLinkedService -Name ContosoLinkedService
```

<span data-ttu-id="4e2a3-114">To polecenie powoduje usunięcie połączonej usługi o nazwie ContosoLinkedService z obszaru roboczego o nazwie ContosoWorkspace za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="4e2a3-114">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="4e2a3-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="4e2a3-115">Example 3</span></span>
```powershell
PS C:\> $linkedService = Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
PS C:\> $linkedService | Remove-AzSynapseLinkedService
```

<span data-ttu-id="4e2a3-116">To polecenie powoduje usunięcie połączonej usługi o nazwie ContosoLinkedService z obszaru roboczego o nazwie ContosoWorkspace za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="4e2a3-116">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="4e2a3-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4e2a3-117">PARAMETERS</span></span>

### <span data-ttu-id="4e2a3-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4e2a3-118">-AsJob</span></span>
<span data-ttu-id="4e2a3-119">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="4e2a3-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4e2a3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e2a3-120">-DefaultProfile</span></span>
<span data-ttu-id="4e2a3-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4e2a3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e2a3-122">-Force</span><span class="sxs-lookup"><span data-stu-id="4e2a3-122">-Force</span></span>
<span data-ttu-id="4e2a3-123">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4e2a3-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4e2a3-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4e2a3-124">-InputObject</span></span>
<span data-ttu-id="4e2a3-125">Połączony obiekt usługi.</span><span class="sxs-lookup"><span data-stu-id="4e2a3-125">The linked service object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e2a3-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4e2a3-126">-Name</span></span>
<span data-ttu-id="4e2a3-127">Nazwa połączonej usługi.</span><span class="sxs-lookup"><span data-stu-id="4e2a3-127">The linked service name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: LinkedServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e2a3-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4e2a3-128">-PassThru</span></span>
<span data-ttu-id="4e2a3-129">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="4e2a3-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="4e2a3-130">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="4e2a3-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="4e2a3-131">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="4e2a3-131">-WorkspaceName</span></span>
<span data-ttu-id="4e2a3-132">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="4e2a3-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="4e2a3-133">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="4e2a3-133">-WorkspaceObject</span></span>
<span data-ttu-id="4e2a3-134">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="4e2a3-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="4e2a3-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4e2a3-135">-Confirm</span></span>
<span data-ttu-id="4e2a3-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e2a3-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e2a3-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e2a3-137">-WhatIf</span></span>
<span data-ttu-id="4e2a3-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e2a3-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4e2a3-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4e2a3-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e2a3-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e2a3-140">CommonParameters</span></span>
<span data-ttu-id="4e2a3-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e2a3-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e2a3-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4e2a3-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e2a3-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4e2a3-143">INPUTS</span></span>

### <span data-ttu-id="4e2a3-144">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="4e2a3-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="4e2a3-145">Microsoft. Azure. Commands. Synapse. models. PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="4e2a3-145">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="4e2a3-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4e2a3-146">OUTPUTS</span></span>

### <span data-ttu-id="4e2a3-147">Microsoft. Azure. Commands. Synapse. models. PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="4e2a3-147">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="4e2a3-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4e2a3-148">NOTES</span></span>

## <span data-ttu-id="4e2a3-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4e2a3-149">RELATED LINKS</span></span>
