---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleAssignment.md
ms.openlocfilehash: bf96dc0818b978c6c759d363c9d3e2637f27b704
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94061951"
---
# <span data-ttu-id="f7a6f-101">Get-AzSynapseRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="f7a6f-101">Get-AzSynapseRoleAssignment</span></span>

## <span data-ttu-id="f7a6f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f7a6f-102">SYNOPSIS</span></span>
<span data-ttu-id="f7a6f-103">Pobiera przypisanie roli Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="f7a6f-103">Gets a Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="f7a6f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f7a6f-104">SYNTAX</span></span>

### <span data-ttu-id="f7a6f-105">GetByWorkspaceNameAndNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f7a6f-105">GetByWorkspaceNameAndNameParameterSet (Default)</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> [-RoleDefinitionName <String>] [-SignInName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7a6f-106">GetByWorkspaceNameAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7a6f-106">GetByWorkspaceNameAndIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> [-RoleDefinitionName <String>] [-ObjectId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7a6f-107">GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7a6f-107">GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionId <String> [-ObjectId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7a6f-108">GetByWorkspaceNameAndAssignmentIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7a6f-108">GetByWorkspaceNameAndAssignmentIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> -RoleAssignmentId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7a6f-109">GetByWorkspaceNameAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7a6f-109">GetByWorkspaceNameAndServicePrincipalNameParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> [-RoleDefinitionName <String>]
 [-ServicePrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7a6f-110">GetByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7a6f-110">GetByWorkspaceObjectAndNameParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> [-RoleDefinitionName <String>]
 -SignInName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7a6f-111">GetByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7a6f-111">GetByWorkspaceObjectAndIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> [-RoleDefinitionName <String>]
 [-ObjectId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7a6f-112">GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7a6f-112">GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionId <String>
 [-ObjectId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7a6f-113">GetByWorkspaceObjectAndAssignmentIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7a6f-113">GetByWorkspaceObjectAndAssignmentIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleAssignmentId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7a6f-114">GetByWorkspaceObjectAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7a6f-114">GetByWorkspaceObjectAndServicePrincipalNameParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> [-RoleDefinitionName <String>]
 -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7a6f-115">Opis</span><span class="sxs-lookup"><span data-stu-id="f7a6f-115">DESCRIPTION</span></span>
<span data-ttu-id="f7a6f-116">Polecenie cmdlet **Get-AzSynapseRoleAssignment** umożliwia przypisanie roli Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="f7a6f-116">The **Get-AzSynapseRoleAssignment** cmdlet gets a Azure Synapse Analytics Role Assignment.</span></span>
<span data-ttu-id="f7a6f-117">Jeśli definicja roli lub główna nazwa użytkownika nie zostaną określone, to polecenie cmdlet będzie pobierać wszystkie zadania ról.</span><span class="sxs-lookup"><span data-stu-id="f7a6f-117">If you do not specify a role definition or a user principal name, this cmdlet gets all role assignment.</span></span>

## <span data-ttu-id="f7a6f-118">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f7a6f-118">EXAMPLES</span></span>

### <span data-ttu-id="f7a6f-119">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f7a6f-119">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="f7a6f-120">To polecenie pobiera wszystkie przypisania ról w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="f7a6f-120">This command gets all role assignments under a workspace.</span></span>

### <span data-ttu-id="f7a6f-121">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f7a6f-121">Example 2</span></span>
```powershells
PS C:\> Get-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleDefinitionName ContosoRole
```

<span data-ttu-id="f7a6f-122">To polecenie pobiera wszystkie zadania ról w obszarze roboczym ContosoWorkspace z nazwą roli ContosoRole.</span><span class="sxs-lookup"><span data-stu-id="f7a6f-122">This command gets all role assignments under workspace ContosoWorkspace with role name ContosoRole.</span></span>

### <span data-ttu-id="f7a6f-123">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="f7a6f-123">Example 3</span></span>
```powershells
PS C:\> Get-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleDefinitionName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="f7a6f-124">To polecenie uzyskuje przypisanie roli w obszarze roboczym ContosoWorkspace z nazwą roli ContosoRole i główną nazwą użytkownika Contosoname.</span><span class="sxs-lookup"><span data-stu-id="f7a6f-124">This command gets a role assignment under workspace ContosoWorkspace with role name ContosoRole and user principal name ContosoName.</span></span>

### <span data-ttu-id="f7a6f-125">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="f7a6f-125">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseRoleAssignment
```

<span data-ttu-id="f7a6f-126">To polecenie pobiera wszystkie przypisania ról w obszarze roboczym za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="f7a6f-126">This command gets all role assignments under a workspace through pipeline.</span></span>

## <span data-ttu-id="f7a6f-127">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f7a6f-127">PARAMETERS</span></span>

### <span data-ttu-id="f7a6f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7a6f-128">-DefaultProfile</span></span>
<span data-ttu-id="f7a6f-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f7a6f-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7a6f-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="f7a6f-130">-ObjectId</span></span>
<span data-ttu-id="f7a6f-131">Identyfikator ObjectId usługi Azure AD dla użytkownika, grupy lub podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="f7a6f-131">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndIdParameterSet, GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, GetByWorkspaceObjectAndIdParameterSet, GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7a6f-132">-RoleAssignmentId</span><span class="sxs-lookup"><span data-stu-id="f7a6f-132">-RoleAssignmentId</span></span>
<span data-ttu-id="f7a6f-133">Identyfikator zadania roli.</span><span class="sxs-lookup"><span data-stu-id="f7a6f-133">The ID of the role assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndAssignmentIdParameterSet, GetByWorkspaceObjectAndAssignmentIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7a6f-134">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="f7a6f-134">-RoleDefinitionId</span></span>
<span data-ttu-id="f7a6f-135">Identyfikator roli przypisanej do podmiotu zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="f7a6f-135">Id of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7a6f-136">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="f7a6f-136">-RoleDefinitionName</span></span>
<span data-ttu-id="f7a6f-137">Nazwa roli przypisanej do podmiotu zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="f7a6f-137">Name of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndNameParameterSet, GetByWorkspaceNameAndIdParameterSet, GetByWorkspaceNameAndServicePrincipalNameParameterSet, GetByWorkspaceObjectAndNameParameterSet, GetByWorkspaceObjectAndIdParameterSet, GetByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7a6f-138">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="f7a6f-138">-ServicePrincipalName</span></span>
<span data-ttu-id="f7a6f-139">Obiekt ServicePrincipalName głównej usługi.</span><span class="sxs-lookup"><span data-stu-id="f7a6f-139">The ServicePrincipalName of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndServicePrincipalNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7a6f-140">-SignInName</span><span class="sxs-lookup"><span data-stu-id="f7a6f-140">-SignInName</span></span>
<span data-ttu-id="f7a6f-141">Adres e-mail lub główna nazwa użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f7a6f-141">The email address or the user principal name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndNameParameterSet
Aliases: Email, UserPrincipalName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceObjectAndNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7a6f-142">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="f7a6f-142">-WorkspaceName</span></span>
<span data-ttu-id="f7a6f-143">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="f7a6f-143">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndNameParameterSet, GetByWorkspaceNameAndIdParameterSet, GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, GetByWorkspaceNameAndAssignmentIdParameterSet, GetByWorkspaceNameAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7a6f-144">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="f7a6f-144">-WorkspaceObject</span></span>
<span data-ttu-id="f7a6f-145">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="f7a6f-145">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByWorkspaceObjectAndNameParameterSet, GetByWorkspaceObjectAndIdParameterSet, GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet, GetByWorkspaceObjectAndAssignmentIdParameterSet, GetByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7a6f-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7a6f-146">CommonParameters</span></span>
<span data-ttu-id="f7a6f-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7a6f-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7a6f-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7a6f-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7a6f-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f7a6f-149">INPUTS</span></span>

### <span data-ttu-id="f7a6f-150">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f7a6f-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="f7a6f-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f7a6f-151">OUTPUTS</span></span>

### <span data-ttu-id="f7a6f-152">Microsoft. Azure. Commands. Synapse. models. PSRoleAssignmentDetails</span><span class="sxs-lookup"><span data-stu-id="f7a6f-152">Microsoft.Azure.Commands.Synapse.Models.PSRoleAssignmentDetails</span></span>

## <span data-ttu-id="f7a6f-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f7a6f-153">NOTES</span></span>

## <span data-ttu-id="f7a6f-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f7a6f-154">RELATED LINKS</span></span>
