---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseWorkspace.md
ms.openlocfilehash: 84180165e835678dc74a7ed08f6a06c51cec8134
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198330"
---
# <span data-ttu-id="dd43b-101">Update-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="dd43b-101">Update-AzSynapseWorkspace</span></span>

## <span data-ttu-id="dd43b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd43b-102">SYNOPSIS</span></span>
<span data-ttu-id="dd43b-103">Aktualizuje obszar roboczy analizy Synapse.</span><span class="sxs-lookup"><span data-stu-id="dd43b-103">Updates a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="dd43b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="dd43b-104">SYNTAX</span></span>

### <span data-ttu-id="dd43b-105">SetByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="dd43b-105">SetByNameParameterSet (Default)</span></span>
```
Update-AzSynapseWorkspace [-ResourceGroupName <String>] [-Name <String>] [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd43b-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd43b-106">SetByInputObjectParameterSet</span></span>
```
Update-AzSynapseWorkspace -InputObject <PSSynapseWorkspace> [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd43b-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd43b-107">SetByResourceIdParameterSet</span></span>
```
Update-AzSynapseWorkspace -ResourceId <String> [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd43b-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="dd43b-108">DESCRIPTION</span></span>
<span data-ttu-id="dd43b-109">Polecenie **cmdlet Update-AzSynapseWorkspace** aktualizuje obszar roboczy usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="dd43b-109">The **Update-AzSynapseWorkspace** cmdlet updates an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="dd43b-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="dd43b-110">EXAMPLES</span></span>

### <span data-ttu-id="dd43b-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="dd43b-111">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseWorkspace -Name ContosoWorkspace -Tag @{'key'='value'}
```

<span data-ttu-id="dd43b-112">To polecenie aktualizuje tagi dla określonego obszaru roboczego usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="dd43b-112">This commands updates tags for the specififed Azure Synapse Analytics workspace.</span></span>

### <span data-ttu-id="dd43b-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="dd43b-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseWorkspace -Tag @{'key'='value1'}
```

<span data-ttu-id="dd43b-114">To polecenie aktualizuje tagi dla określonego obszaru roboczego usługi Azure Synapse Analytics za pośrednictwem potoku.</span><span class="sxs-lookup"><span data-stu-id="dd43b-114">This commands updates tags for the specififed Azure Synapse Analytics workspace through pipeline.</span></span>

### <span data-ttu-id="dd43b-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="dd43b-115">Example 3</span></span>
```powershell
PS C:\> Update-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace -Tag @{'key'='value2'}
```

<span data-ttu-id="dd43b-116">To polecenie aktualizuje tagi dla określonego obszaru roboczego usługi Azure Synapse Analytics za pośrednictwem potoku przy użyciu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="dd43b-116">This commands updates tags for the specififed Azure Synapse Analytics workspace through pipeline with resource ID.</span></span>

## <span data-ttu-id="dd43b-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dd43b-117">PARAMETERS</span></span>

### <span data-ttu-id="dd43b-118">— AsJob</span><span class="sxs-lookup"><span data-stu-id="dd43b-118">-AsJob</span></span>
<span data-ttu-id="dd43b-119">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="dd43b-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dd43b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd43b-120">-DefaultProfile</span></span>
<span data-ttu-id="dd43b-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="dd43b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd43b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd43b-122">-InputObject</span></span>
<span data-ttu-id="dd43b-123">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="dd43b-123">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd43b-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="dd43b-124">-Name</span></span>
<span data-ttu-id="dd43b-125">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="dd43b-125">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: WorkspaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd43b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd43b-126">-ResourceGroupName</span></span>
<span data-ttu-id="dd43b-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="dd43b-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd43b-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd43b-128">-ResourceId</span></span>
<span data-ttu-id="dd43b-129">Identyfikator zasobu obszaru roboczego programu Synapse.</span><span class="sxs-lookup"><span data-stu-id="dd43b-129">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd43b-130">-SqlAdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="dd43b-130">-SqlAdministratorLoginPassword</span></span>
<span data-ttu-id="dd43b-131">Nowe hasło administratora języka SQL dla obszaru roboczego programu Groove.</span><span class="sxs-lookup"><span data-stu-id="dd43b-131">The new SQL administrator password for the workspace.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd43b-132">— Tag</span><span class="sxs-lookup"><span data-stu-id="dd43b-132">-Tag</span></span>
<span data-ttu-id="dd43b-133">A string,string dictionary of tags associated with the resource.</span><span class="sxs-lookup"><span data-stu-id="dd43b-133">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd43b-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dd43b-134">-Confirm</span></span>
<span data-ttu-id="dd43b-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="dd43b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd43b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd43b-136">-WhatIf</span></span>
<span data-ttu-id="dd43b-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd43b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd43b-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="dd43b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd43b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd43b-139">CommonParameters</span></span>
<span data-ttu-id="dd43b-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd43b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd43b-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dd43b-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd43b-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dd43b-142">INPUTS</span></span>

### <span data-ttu-id="dd43b-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="dd43b-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="dd43b-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dd43b-144">OUTPUTS</span></span>

### <span data-ttu-id="dd43b-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="dd43b-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="dd43b-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="dd43b-146">NOTES</span></span>

## <span data-ttu-id="dd43b-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dd43b-147">RELATED LINKS</span></span>
