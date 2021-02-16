---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseLinkedService.md
ms.openlocfilehash: c70cc0f8659a04e8a10a4fbd2b776d22fca6a616
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195587"
---
# <span data-ttu-id="e19ee-101">Remove-AzSynapseLinkedService</span><span class="sxs-lookup"><span data-stu-id="e19ee-101">Remove-AzSynapseLinkedService</span></span>

## <span data-ttu-id="e19ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e19ee-102">SYNOPSIS</span></span>
<span data-ttu-id="e19ee-103">Usuwa usługę połączona z obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="e19ee-103">Removes a linked service from workspace.</span></span>

## <span data-ttu-id="e19ee-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e19ee-104">SYNTAX</span></span>

### <span data-ttu-id="e19ee-105">RemoveByName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="e19ee-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseLinkedService -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e19ee-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="e19ee-106">RemoveByObject</span></span>
```
Remove-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e19ee-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="e19ee-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseLinkedService -InputObject <PSLinkedServiceResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e19ee-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="e19ee-108">DESCRIPTION</span></span>
<span data-ttu-id="e19ee-109">Polecenie **cmdlet Remove-AzSynapseLinkedService** usuwa usługę połączona z obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="e19ee-109">The **Remove-AzSynapseLinkedService** cmdlet removes a linked service from workspace.</span></span>

## <span data-ttu-id="e19ee-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e19ee-110">EXAMPLES</span></span>

### <span data-ttu-id="e19ee-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e19ee-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
```

<span data-ttu-id="e19ee-112">To polecenie usuwa usługę połączona o nazwie ContosoLinkedService z obszaru roboczego o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="e19ee-112">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="e19ee-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e19ee-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseLinkedService -Name ContosoLinkedService
```

<span data-ttu-id="e19ee-114">To polecenie usuwa z potoku usługę połączona o nazwie ContosoLinkedService z obszaru roboczego o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="e19ee-114">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="e19ee-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="e19ee-115">Example 3</span></span>
```powershell
PS C:\> $linkedService = Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
PS C:\> $linkedService | Remove-AzSynapseLinkedService
```

<span data-ttu-id="e19ee-116">To polecenie usuwa z potoku usługę połączona o nazwie ContosoLinkedService z obszaru roboczego o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="e19ee-116">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="e19ee-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e19ee-117">PARAMETERS</span></span>

### <span data-ttu-id="e19ee-118">— AsJob</span><span class="sxs-lookup"><span data-stu-id="e19ee-118">-AsJob</span></span>
<span data-ttu-id="e19ee-119">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e19ee-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e19ee-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e19ee-120">-DefaultProfile</span></span>
<span data-ttu-id="e19ee-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e19ee-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e19ee-122">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="e19ee-122">-Force</span></span>
<span data-ttu-id="e19ee-123">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e19ee-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="e19ee-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e19ee-124">-InputObject</span></span>
<span data-ttu-id="e19ee-125">Obiekt usługi połączonej.</span><span class="sxs-lookup"><span data-stu-id="e19ee-125">The linked service object.</span></span>

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

### <span data-ttu-id="e19ee-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e19ee-126">-Name</span></span>
<span data-ttu-id="e19ee-127">Nazwa połączonej usługi.</span><span class="sxs-lookup"><span data-stu-id="e19ee-127">The linked service name.</span></span>

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

### <span data-ttu-id="e19ee-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e19ee-128">-PassThru</span></span>
<span data-ttu-id="e19ee-129">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="e19ee-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="e19ee-130">Jeśli ten przełącznik zostanie określony, zostanie on podany jako prawda, jeśli zostanie pomyślnie określony.</span><span class="sxs-lookup"><span data-stu-id="e19ee-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="e19ee-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e19ee-131">-WorkspaceName</span></span>
<span data-ttu-id="e19ee-132">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="e19ee-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="e19ee-133">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e19ee-133">-WorkspaceObject</span></span>
<span data-ttu-id="e19ee-134">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="e19ee-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e19ee-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e19ee-135">-Confirm</span></span>
<span data-ttu-id="e19ee-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e19ee-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e19ee-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e19ee-137">-WhatIf</span></span>
<span data-ttu-id="e19ee-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e19ee-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e19ee-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e19ee-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e19ee-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e19ee-140">CommonParameters</span></span>
<span data-ttu-id="e19ee-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e19ee-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e19ee-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e19ee-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e19ee-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e19ee-143">INPUTS</span></span>

### <span data-ttu-id="e19ee-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e19ee-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="e19ee-145">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="e19ee-145">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="e19ee-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e19ee-146">OUTPUTS</span></span>

### <span data-ttu-id="e19ee-147">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="e19ee-147">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="e19ee-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e19ee-148">NOTES</span></span>

## <span data-ttu-id="e19ee-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e19ee-149">RELATED LINKS</span></span>
