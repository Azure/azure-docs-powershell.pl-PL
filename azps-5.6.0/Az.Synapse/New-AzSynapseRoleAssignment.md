---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/new-azsynapseroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseRoleAssignment.md
ms.openlocfilehash: 7e216a6d2751ddd24e7d948cb6cca036c2a9b336
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976074"
---
# <span data-ttu-id="be085-101">New-AzSynapseRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="be085-101">New-AzSynapseRoleAssignment</span></span>

## <span data-ttu-id="be085-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be085-102">SYNOPSIS</span></span>
<span data-ttu-id="be085-103">Tworzy przypisanie roli Analizy Synapse.</span><span class="sxs-lookup"><span data-stu-id="be085-103">Creates a Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="be085-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="be085-104">SYNTAX</span></span>

### <span data-ttu-id="be085-105">NewByWorkspaceNameAndNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="be085-105">NewByWorkspaceNameAndNameParameterSet (Default)</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -SignInName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be085-106">NewByWorkspaceNameAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="be085-106">NewByWorkspaceNameAndIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -ObjectId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be085-107">NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="be085-107">NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionId <String> -ObjectId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be085-108">NewByWorkspaceNameAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="be085-108">NewByWorkspaceNameAndServicePrincipalNameParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -ServicePrincipalName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be085-109">NewByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="be085-109">NewByWorkspaceObjectAndNameParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -SignInName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="be085-110">NewByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="be085-110">NewByWorkspaceObjectAndIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ObjectId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="be085-111">NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="be085-111">NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionId <String> -ObjectId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be085-112">NewByWorkspaceObjectAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="be085-112">NewByWorkspaceObjectAndServicePrincipalNameParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ServicePrincipalName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="be085-113">OPIS</span><span class="sxs-lookup"><span data-stu-id="be085-113">DESCRIPTION</span></span>
<span data-ttu-id="be085-114">Polecenie **cmdlet New-AzSynapseRoleAssignment** tworzy przypisanie roli usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="be085-114">The **New-AzSynapseRoleAssignment** cmdlet creates an Azure Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="be085-115">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="be085-115">EXAMPLES</span></span>

### <span data-ttu-id="be085-116">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="be085-116">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleDefinitionName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="be085-117">To polecenie przypisuje nazwę ContosoRole użytkownikowi, którego główna nazwa to ContosoName.</span><span class="sxs-lookup"><span data-stu-id="be085-117">This command assigns ContosoRole to the user whose principal name is ContosoName.</span></span>

### <span data-ttu-id="be085-118">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="be085-118">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseRoleAssignment -RoleDefinitionName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="be085-119">To polecenie przypisuje użytkownikowi ContosoRole, którego główna nazwa to ContosoName za pośrednictwem potoku.</span><span class="sxs-lookup"><span data-stu-id="be085-119">This command assigns ContosoRole to the user whose principal name is ContosoName through pipeline.</span></span>

## <span data-ttu-id="be085-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="be085-120">PARAMETERS</span></span>

### <span data-ttu-id="be085-121">— AsJob</span><span class="sxs-lookup"><span data-stu-id="be085-121">-AsJob</span></span>
<span data-ttu-id="be085-122">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="be085-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="be085-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be085-123">-DefaultProfile</span></span>
<span data-ttu-id="be085-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="be085-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be085-125">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="be085-125">-ObjectId</span></span>
<span data-ttu-id="be085-126">Identyfikator ObjectId usługi Azure AD użytkownika, grupy lub podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="be085-126">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndIdParameterSet, NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, NewByWorkspaceObjectAndIdParameterSet, NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be085-127">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="be085-127">-RoleDefinitionId</span></span>
<span data-ttu-id="be085-128">Identyfikator roli przypisanej do podmiotu głównego.</span><span class="sxs-lookup"><span data-stu-id="be085-128">Id of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be085-129">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="be085-129">-RoleDefinitionName</span></span>
<span data-ttu-id="be085-130">Nazwa roli przypisanej do podmiotu głównego.</span><span class="sxs-lookup"><span data-stu-id="be085-130">Name of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndNameParameterSet, NewByWorkspaceNameAndIdParameterSet, NewByWorkspaceNameAndServicePrincipalNameParameterSet, NewByWorkspaceObjectAndNameParameterSet, NewByWorkspaceObjectAndIdParameterSet, NewByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be085-131">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="be085-131">-ServicePrincipalName</span></span>
<span data-ttu-id="be085-132">ServicePrincipalName podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="be085-132">The ServicePrincipalName of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndServicePrincipalNameParameterSet, NewByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be085-133">-SignInName</span><span class="sxs-lookup"><span data-stu-id="be085-133">-SignInName</span></span>
<span data-ttu-id="be085-134">Adres e-mail lub główna nazwa użytkownika.</span><span class="sxs-lookup"><span data-stu-id="be085-134">The email address or the user principal name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndNameParameterSet, NewByWorkspaceObjectAndNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be085-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="be085-135">-WorkspaceName</span></span>
<span data-ttu-id="be085-136">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="be085-136">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndNameParameterSet, NewByWorkspaceNameAndIdParameterSet, NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, NewByWorkspaceNameAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be085-137">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="be085-137">-WorkspaceObject</span></span>
<span data-ttu-id="be085-138">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="be085-138">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: NewByWorkspaceObjectAndNameParameterSet, NewByWorkspaceObjectAndIdParameterSet, NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet, NewByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be085-139">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="be085-139">-Confirm</span></span>
<span data-ttu-id="be085-140">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="be085-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be085-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be085-141">-WhatIf</span></span>
<span data-ttu-id="be085-142">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be085-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be085-143">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="be085-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be085-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be085-144">CommonParameters</span></span>
<span data-ttu-id="be085-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be085-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be085-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="be085-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be085-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="be085-147">INPUTS</span></span>

### <span data-ttu-id="be085-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="be085-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="be085-149">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="be085-149">OUTPUTS</span></span>

### <span data-ttu-id="be085-150">Microsoft.Azure.Commands.Synapse.Models.PSRoleAssignmentDetails</span><span class="sxs-lookup"><span data-stu-id="be085-150">Microsoft.Azure.Commands.Synapse.Models.PSRoleAssignmentDetails</span></span>

## <span data-ttu-id="be085-151">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="be085-151">NOTES</span></span>

## <span data-ttu-id="be085-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="be085-152">RELATED LINKS</span></span>
