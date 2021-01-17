---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseRoleAssignment.md
ms.openlocfilehash: 3ac6d0be30075409924c014c27a16b2f4cab21a0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383439"
---
# <span data-ttu-id="3c01d-101">Remove-AzSynapseRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="3c01d-101">Remove-AzSynapseRoleAssignment</span></span>

## <span data-ttu-id="3c01d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3c01d-102">SYNOPSIS</span></span>
<span data-ttu-id="3c01d-103">Usuwa przypisanie roli analiza Synapse.</span><span class="sxs-lookup"><span data-stu-id="3c01d-103">Deletes a Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="3c01d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3c01d-104">SYNTAX</span></span>

### <span data-ttu-id="3c01d-105">RemoveByWorkspaceNameAndNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3c01d-105">RemoveByWorkspaceNameAndNameParameterSet (Default)</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -SignInName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c01d-106">RemoveByWorkspaceNameAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c01d-106">RemoveByWorkspaceNameAndIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleAssignmentId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c01d-107">RemoveByWorkspaceNameAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c01d-107">RemoveByWorkspaceNameAndObjectIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -ObjectId <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c01d-108">RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c01d-108">RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionId <String> -ObjectId <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c01d-109">RemoveByWorkspaceNameAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c01d-109">RemoveByWorkspaceNameAndServicePrincipalNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String>
 -ServicePrincipalName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c01d-110">RemoveByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c01d-110">RemoveByWorkspaceObjectAndIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleAssignmentId <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c01d-111">RemoveByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c01d-111">RemoveByWorkspaceObjectAndNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -SignInName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3c01d-112">RemoveByWorkspaceObjectAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c01d-112">RemoveByWorkspaceObjectAndObjectIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ObjectId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3c01d-113">RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c01d-113">RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionId <String>
 -ObjectId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3c01d-114">RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c01d-114">RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ServicePrincipalName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c01d-115">Opis</span><span class="sxs-lookup"><span data-stu-id="3c01d-115">DESCRIPTION</span></span>
<span data-ttu-id="3c01d-116">Polecenie cmdlet **Remove-AzSynapseRoleAssignment** trwale usuwa przypisanie roli Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="3c01d-116">The **Remove-AzSynapseRoleAssignment** cmdlet permanently deletes an Azure Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="3c01d-117">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3c01d-117">EXAMPLES</span></span>

### <span data-ttu-id="3c01d-118">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3c01d-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleAssignmentId ContosoRoleAssignmentId
```

<span data-ttu-id="3c01d-119">To polecenie usuwa przypisanie roli Azure Synapse Analytics o identyfikator przydziału roli.</span><span class="sxs-lookup"><span data-stu-id="3c01d-119">This command deletes an Azure Synapse Analytics role assignment with a role assignment Id.</span></span>

### <span data-ttu-id="3c01d-120">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="3c01d-120">Example 2</span></span>
```powershell
PS C:\> Remove-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleAssignmentName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="3c01d-121">To polecenie usuwa przydział roli usługi Azure Synapse Analytics z nazwą roli i nazwą główną użytkownika.</span><span class="sxs-lookup"><span data-stu-id="3c01d-121">This command deletes an Azure Synapse Analytics role assignment with a role name and a user principal name.</span></span>

### <span data-ttu-id="3c01d-122">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="3c01d-122">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseRoleAssignment -RoleAssignmentId ContosoRoleAssignmentId
```

<span data-ttu-id="3c01d-123">To polecenie usuwa przydział roli usługi Azure Synapse Analytics z identyfikatorem przypisania roli za pomocą potoku.</span><span class="sxs-lookup"><span data-stu-id="3c01d-123">This command deletes an Azure Synapse Analytics role assignment with a role assignment Id through pipeline.</span></span>

## <span data-ttu-id="3c01d-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3c01d-124">PARAMETERS</span></span>

### <span data-ttu-id="3c01d-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3c01d-125">-AsJob</span></span>
<span data-ttu-id="3c01d-126">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="3c01d-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3c01d-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c01d-127">-DefaultProfile</span></span>
<span data-ttu-id="3c01d-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3c01d-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c01d-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="3c01d-129">-ObjectId</span></span>
<span data-ttu-id="3c01d-130">Identyfikator ObjectId usługi Azure AD dla użytkownika, grupy lub podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="3c01d-130">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndObjectIdParameterSet, RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet, RemoveByWorkspaceObjectAndObjectIdParameterSet, RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c01d-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3c01d-131">-PassThru</span></span>
<span data-ttu-id="3c01d-132">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="3c01d-132">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="3c01d-133">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="3c01d-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="3c01d-134">-RoleAssignmentId</span><span class="sxs-lookup"><span data-stu-id="3c01d-134">-RoleAssignmentId</span></span>
<span data-ttu-id="3c01d-135">Identyfikator zadania roli.</span><span class="sxs-lookup"><span data-stu-id="3c01d-135">The ID of the role assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndIdParameterSet, RemoveByWorkspaceObjectAndIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c01d-136">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="3c01d-136">-RoleDefinitionId</span></span>
<span data-ttu-id="3c01d-137">Identyfikator roli przypisanej do podmiotu zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="3c01d-137">Id of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet, RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c01d-138">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="3c01d-138">-RoleDefinitionName</span></span>
<span data-ttu-id="3c01d-139">Nazwa roli przypisanej do podmiotu zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="3c01d-139">Name of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndNameParameterSet, RemoveByWorkspaceNameAndObjectIdParameterSet, RemoveByWorkspaceNameAndServicePrincipalNameParameterSet, RemoveByWorkspaceObjectAndNameParameterSet, RemoveByWorkspaceObjectAndObjectIdParameterSet, RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c01d-140">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="3c01d-140">-ServicePrincipalName</span></span>
<span data-ttu-id="3c01d-141">Obiekt ServicePrincipalName głównej usługi.</span><span class="sxs-lookup"><span data-stu-id="3c01d-141">The ServicePrincipalName of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndServicePrincipalNameParameterSet, RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c01d-142">-SignInName</span><span class="sxs-lookup"><span data-stu-id="3c01d-142">-SignInName</span></span>
<span data-ttu-id="3c01d-143">Adres e-mail lub główna nazwa użytkownika.</span><span class="sxs-lookup"><span data-stu-id="3c01d-143">The email address or the user principal name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndNameParameterSet, RemoveByWorkspaceObjectAndNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c01d-144">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="3c01d-144">-WorkspaceName</span></span>
<span data-ttu-id="3c01d-145">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="3c01d-145">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndNameParameterSet, RemoveByWorkspaceNameAndIdParameterSet, RemoveByWorkspaceNameAndObjectIdParameterSet, RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet, RemoveByWorkspaceNameAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c01d-146">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="3c01d-146">-WorkspaceObject</span></span>
<span data-ttu-id="3c01d-147">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="3c01d-147">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByWorkspaceObjectAndIdParameterSet, RemoveByWorkspaceObjectAndNameParameterSet, RemoveByWorkspaceObjectAndObjectIdParameterSet, RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet, RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c01d-148">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3c01d-148">-Confirm</span></span>
<span data-ttu-id="3c01d-149">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c01d-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c01d-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c01d-150">-WhatIf</span></span>
<span data-ttu-id="3c01d-151">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c01d-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c01d-152">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3c01d-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c01d-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c01d-153">CommonParameters</span></span>
<span data-ttu-id="3c01d-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c01d-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c01d-155">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3c01d-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c01d-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3c01d-156">INPUTS</span></span>

### <span data-ttu-id="3c01d-157">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="3c01d-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="3c01d-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3c01d-158">OUTPUTS</span></span>

### <span data-ttu-id="3c01d-159">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3c01d-159">System.Boolean</span></span>

## <span data-ttu-id="3c01d-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3c01d-160">NOTES</span></span>

## <span data-ttu-id="3c01d-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3c01d-161">RELATED LINKS</span></span>
