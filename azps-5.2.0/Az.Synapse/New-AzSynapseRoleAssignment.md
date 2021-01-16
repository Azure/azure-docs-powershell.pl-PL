---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapseroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseRoleAssignment.md
ms.openlocfilehash: 6fdb2a51354df01c308629eaedb09cba3a8d2fdf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341929"
---
# <span data-ttu-id="7cf9a-101">New-AzSynapseRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="7cf9a-101">New-AzSynapseRoleAssignment</span></span>

## <span data-ttu-id="7cf9a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7cf9a-102">SYNOPSIS</span></span>
<span data-ttu-id="7cf9a-103">Tworzy przypisanie roli analiza Synapse.</span><span class="sxs-lookup"><span data-stu-id="7cf9a-103">Creates a Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="7cf9a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7cf9a-104">SYNTAX</span></span>

### <span data-ttu-id="7cf9a-105">NewByWorkspaceNameAndNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7cf9a-105">NewByWorkspaceNameAndNameParameterSet (Default)</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -SignInName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cf9a-106">NewByWorkspaceNameAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7cf9a-106">NewByWorkspaceNameAndIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -ObjectId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cf9a-107">NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7cf9a-107">NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionId <String> -ObjectId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cf9a-108">NewByWorkspaceNameAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7cf9a-108">NewByWorkspaceNameAndServicePrincipalNameParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -ServicePrincipalName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cf9a-109">NewByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7cf9a-109">NewByWorkspaceObjectAndNameParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -SignInName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7cf9a-110">NewByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7cf9a-110">NewByWorkspaceObjectAndIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ObjectId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7cf9a-111">NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7cf9a-111">NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionId <String> -ObjectId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cf9a-112">NewByWorkspaceObjectAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7cf9a-112">NewByWorkspaceObjectAndServicePrincipalNameParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ServicePrincipalName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7cf9a-113">Opis</span><span class="sxs-lookup"><span data-stu-id="7cf9a-113">DESCRIPTION</span></span>
<span data-ttu-id="7cf9a-114">Polecenie cmdlet **New-AzSynapseRoleAssignment** tworzy przypisanie roli Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="7cf9a-114">The **New-AzSynapseRoleAssignment** cmdlet creates an Azure Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="7cf9a-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7cf9a-115">EXAMPLES</span></span>

### <span data-ttu-id="7cf9a-116">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7cf9a-116">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleDefinitionName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="7cf9a-117">To polecenie umożliwia przypisanie ContosoRole użytkownikowi, którego główna nazwa to Contosoname.</span><span class="sxs-lookup"><span data-stu-id="7cf9a-117">This command assigns ContosoRole to the user whose principal name is ContosoName.</span></span>

### <span data-ttu-id="7cf9a-118">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="7cf9a-118">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseRoleAssignment -RoleDefinitionName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="7cf9a-119">To polecenie przypisuje ContosoRole użytkownikowi, którego główna nazwa to contoso.</span><span class="sxs-lookup"><span data-stu-id="7cf9a-119">This command assigns ContosoRole to the user whose principal name is ContosoName through pipeline.</span></span>

## <span data-ttu-id="7cf9a-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7cf9a-120">PARAMETERS</span></span>

### <span data-ttu-id="7cf9a-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7cf9a-121">-AsJob</span></span>
<span data-ttu-id="7cf9a-122">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="7cf9a-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7cf9a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cf9a-123">-DefaultProfile</span></span>
<span data-ttu-id="7cf9a-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf9a-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7cf9a-125">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="7cf9a-125">-ObjectId</span></span>
<span data-ttu-id="7cf9a-126">Identyfikator ObjectId usługi Azure AD dla użytkownika, grupy lub podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="7cf9a-126">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>

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

### <span data-ttu-id="7cf9a-127">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="7cf9a-127">-RoleDefinitionId</span></span>
<span data-ttu-id="7cf9a-128">Identyfikator roli przypisanej do podmiotu zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="7cf9a-128">Id of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="7cf9a-129">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="7cf9a-129">-RoleDefinitionName</span></span>
<span data-ttu-id="7cf9a-130">Nazwa roli przypisanej do podmiotu zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="7cf9a-130">Name of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="7cf9a-131">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="7cf9a-131">-ServicePrincipalName</span></span>
<span data-ttu-id="7cf9a-132">Obiekt ServicePrincipalName głównej usługi.</span><span class="sxs-lookup"><span data-stu-id="7cf9a-132">The ServicePrincipalName of the service principal.</span></span>

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

### <span data-ttu-id="7cf9a-133">-SignInName</span><span class="sxs-lookup"><span data-stu-id="7cf9a-133">-SignInName</span></span>
<span data-ttu-id="7cf9a-134">Adres e-mail lub główna nazwa użytkownika.</span><span class="sxs-lookup"><span data-stu-id="7cf9a-134">The email address or the user principal name of the user.</span></span>

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

### <span data-ttu-id="7cf9a-135">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="7cf9a-135">-WorkspaceName</span></span>
<span data-ttu-id="7cf9a-136">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="7cf9a-136">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="7cf9a-137">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="7cf9a-137">-WorkspaceObject</span></span>
<span data-ttu-id="7cf9a-138">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="7cf9a-138">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="7cf9a-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7cf9a-139">-Confirm</span></span>
<span data-ttu-id="7cf9a-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7cf9a-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cf9a-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cf9a-141">-WhatIf</span></span>
<span data-ttu-id="7cf9a-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7cf9a-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cf9a-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7cf9a-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cf9a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cf9a-144">CommonParameters</span></span>
<span data-ttu-id="7cf9a-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cf9a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cf9a-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7cf9a-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cf9a-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7cf9a-147">INPUTS</span></span>

### <span data-ttu-id="7cf9a-148">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="7cf9a-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="7cf9a-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7cf9a-149">OUTPUTS</span></span>

### <span data-ttu-id="7cf9a-150">Microsoft. Azure. Commands. Synapse. models. PSRoleAssignmentDetails</span><span class="sxs-lookup"><span data-stu-id="7cf9a-150">Microsoft.Azure.Commands.Synapse.Models.PSRoleAssignmentDetails</span></span>

## <span data-ttu-id="7cf9a-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7cf9a-151">NOTES</span></span>

## <span data-ttu-id="7cf9a-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7cf9a-152">RELATED LINKS</span></span>
