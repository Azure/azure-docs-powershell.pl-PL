---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultRoleAssignment.md
ms.openlocfilehash: 9e2dd07ac0346cacb99bbcc2e05d47b57ac8ccd6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180442"
---
# <span data-ttu-id="c6ebb-101">Remove-AzKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="c6ebb-101">Remove-AzKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="c6ebb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6ebb-102">SYNOPSIS</span></span>
<span data-ttu-id="c6ebb-103">Usuwa przypisanie roli do określonego podmiotu zabezpieczeń, który jest przypisany do określonej roli w określonym zakresie.</span><span class="sxs-lookup"><span data-stu-id="c6ebb-103">Removes a role assignment to the specified principal who is assigned to a particular role at a particular scope.</span></span>

## <span data-ttu-id="c6ebb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c6ebb-104">SYNTAX</span></span>

### <span data-ttu-id="c6ebb-105">DefinitionNameSignInName (domyślna)</span><span class="sxs-lookup"><span data-stu-id="c6ebb-105">DefinitionNameSignInName (Default)</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -SignInName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c6ebb-106">DefinitionNameApplicationId</span><span class="sxs-lookup"><span data-stu-id="c6ebb-106">DefinitionNameApplicationId</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ApplicationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c6ebb-107">DefinitionNameObjectId</span><span class="sxs-lookup"><span data-stu-id="c6ebb-107">DefinitionNameObjectId</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ObjectId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c6ebb-108">DefinitionIdApplicationId</span><span class="sxs-lookup"><span data-stu-id="c6ebb-108">DefinitionIdApplicationId</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ApplicationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c6ebb-109">DefinitionIdObjectId</span><span class="sxs-lookup"><span data-stu-id="c6ebb-109">DefinitionIdObjectId</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ObjectId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c6ebb-110">DefinitionIdSignInName</span><span class="sxs-lookup"><span data-stu-id="c6ebb-110">DefinitionIdSignInName</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -SignInName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c6ebb-111">RemoveByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6ebb-111">RemoveByNameParameterSet</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] [-PassThru] -RoleAssignmentName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6ebb-112">InputObject</span><span class="sxs-lookup"><span data-stu-id="c6ebb-112">InputObject</span></span>
```
Remove-AzKeyVaultRoleAssignment [-Scope <String>] [-PassThru] -InputObject <PSKeyVaultRoleAssignment>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6ebb-113">OPIS</span><span class="sxs-lookup"><span data-stu-id="c6ebb-113">DESCRIPTION</span></span>
<span data-ttu-id="c6ebb-114">Użyj polecenia `Remove-AzKeyVaultRoleAssignment` cmdlet, aby odwołać dostęp do dowolnego podmiotu głównego w danym zakresie i w danej roli.</span><span class="sxs-lookup"><span data-stu-id="c6ebb-114">Use the `Remove-AzKeyVaultRoleAssignment` cmdlet to revoke access to any principal at given scope and given role.</span></span> <span data-ttu-id="c6ebb-115">Obiekt przydziału, czyli musi zostać określony główny podmiot.</span><span class="sxs-lookup"><span data-stu-id="c6ebb-115">The object of the assignment i.e. the principal MUST be specified.</span></span> <span data-ttu-id="c6ebb-116">Podmiot zabezpieczeń może być użytkownikiem (za pomocą parametrów SignInName lub ObjectId identyfikuje użytkownika), grupą zabezpieczeń (identyfikując grupę za pomocą parametru ObjectId) lub podmiotem zabezpieczeń usługi (w celu zidentyfikowania parametru ServicePrincipal należy użyć parametrów ApplicationId lub ObjectId).</span><span class="sxs-lookup"><span data-stu-id="c6ebb-116">The principal can be a user (use SignInName or ObjectId parameters to identify a user), security group (use ObjectId parameter to identify a group) or service principal (use ApplicationId or ObjectId parameters to identify a ServicePrincipal.</span></span> <span data-ttu-id="c6ebb-117">Rola przypisana do podmiotu zabezpieczeń MUSI zostać określona przy użyciu parametru RoleDefinitionName lub RoleDefinitionId.</span><span class="sxs-lookup"><span data-stu-id="c6ebb-117">The role that the principal is assigned to MUST be specified using the RoleDefinitionName or RoleDefinitionId parameter.</span></span>

## <span data-ttu-id="c6ebb-118">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c6ebb-118">EXAMPLES</span></span>

### <span data-ttu-id="c6ebb-119">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c6ebb-119">Example 1</span></span>
```powershell
PS C:\> Remove-AzKeyVaultRoleAssignment -HsmName myHsm -RoleDefinitionName "Managed HSM Policy Administrator" -SignInName user1@microsoft.com -Scope "/keys"
```

<span data-ttu-id="c6ebb-120">W tym przykładzie odwołana jest rola " zarządzanego administratora zasad HSM" user1@microsoft.com dla " w zakresie "/keys".</span><span class="sxs-lookup"><span data-stu-id="c6ebb-120">This example revokes "Managed HSM Policy Administrator" role of "user1@microsoft.com" at "/keys" scope.</span></span>

### <span data-ttu-id="c6ebb-121">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c6ebb-121">Example 2</span></span>
```powershell
PS C:\> Get-AzKeyVaultRoleAssignment -HsmName myHsm -SignInName user1@microsoft.com | Remove-AzKeyVaultRoleAssignment
```

<span data-ttu-id="c6ebb-122">W tym przykładzie wszystkie role " user1@microsoft.com " są odwołane we wszystkich zakresach.</span><span class="sxs-lookup"><span data-stu-id="c6ebb-122">This example revokes all roles of "user1@microsoft.com" at all scopes.</span></span>

## <span data-ttu-id="c6ebb-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c6ebb-123">PARAMETERS</span></span>

### <span data-ttu-id="c6ebb-124">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="c6ebb-124">-ApplicationId</span></span>
<span data-ttu-id="c6ebb-125">The app SPN.</span><span class="sxs-lookup"><span data-stu-id="c6ebb-125">The app SPN.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionNameApplicationId, DefinitionIdApplicationId
Aliases: SPN, ServicePrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6ebb-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6ebb-126">-DefaultProfile</span></span>
<span data-ttu-id="c6ebb-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c6ebb-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6ebb-128">-HsmName</span><span class="sxs-lookup"><span data-stu-id="c6ebb-128">-HsmName</span></span>
<span data-ttu-id="c6ebb-129">Nazwa hsm.</span><span class="sxs-lookup"><span data-stu-id="c6ebb-129">Name of the HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionNameSignInName, DefinitionNameApplicationId, DefinitionNameObjectId, DefinitionIdApplicationId, DefinitionIdObjectId, DefinitionIdSignInName, RemoveByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6ebb-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c6ebb-130">-InputObject</span></span>
<span data-ttu-id="c6ebb-131">Obiekt przypisywania ról.</span><span class="sxs-lookup"><span data-stu-id="c6ebb-131">Role assignment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6ebb-132">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="c6ebb-132">-ObjectId</span></span>
<span data-ttu-id="c6ebb-133">Identyfikator obiektu użytkownika lub grupy.</span><span class="sxs-lookup"><span data-stu-id="c6ebb-133">The user or group object id.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionNameObjectId, DefinitionIdObjectId
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6ebb-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c6ebb-134">-PassThru</span></span>
<span data-ttu-id="c6ebb-135">Zwraca wartość prawda po przywróceniu HSM.</span><span class="sxs-lookup"><span data-stu-id="c6ebb-135">Return true when the HSM is restored.</span></span>

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

### <span data-ttu-id="c6ebb-136">-RoleAssignmentName</span><span class="sxs-lookup"><span data-stu-id="c6ebb-136">-RoleAssignmentName</span></span>
<span data-ttu-id="c6ebb-137">Nazwa przydziału roli.</span><span class="sxs-lookup"><span data-stu-id="c6ebb-137">Name of the role assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6ebb-138">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="c6ebb-138">-RoleDefinitionId</span></span>
<span data-ttu-id="c6ebb-139">Identyfikator roli, do których jest przydzielony podmiot zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="c6ebb-139">Role Id the principal is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionIdApplicationId, DefinitionIdObjectId, DefinitionIdSignInName
Aliases: RoleId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6ebb-140">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="c6ebb-140">-RoleDefinitionName</span></span>
<span data-ttu-id="c6ebb-141">Nazwa roli RBAC, do których ma zostać przypisany podmiot zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="c6ebb-141">Name of the RBAC role to assign the principal with.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionNameSignInName, DefinitionNameApplicationId, DefinitionNameObjectId
Aliases: RoleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6ebb-142">— Zakres</span><span class="sxs-lookup"><span data-stu-id="c6ebb-142">-Scope</span></span>
<span data-ttu-id="c6ebb-143">Zakres, do którego ma zastosowanie przypisanie roli lub definicja, np. '/' lub '/keys' lub '/keys/{keyName}'.</span><span class="sxs-lookup"><span data-stu-id="c6ebb-143">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="c6ebb-144">W przypadku pominięcia tej przeoczonej w tym przypadku jest używane "/".</span><span class="sxs-lookup"><span data-stu-id="c6ebb-144">'/' is used when omitted.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6ebb-145">-SignInName</span><span class="sxs-lookup"><span data-stu-id="c6ebb-145">-SignInName</span></span>
<span data-ttu-id="c6ebb-146">Nazwa_logowania użytkownika.</span><span class="sxs-lookup"><span data-stu-id="c6ebb-146">The user SignInName.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionNameSignInName, DefinitionIdSignInName
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6ebb-147">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c6ebb-147">-Confirm</span></span>
<span data-ttu-id="c6ebb-148">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c6ebb-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6ebb-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6ebb-149">-WhatIf</span></span>
<span data-ttu-id="c6ebb-150">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6ebb-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6ebb-151">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c6ebb-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6ebb-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6ebb-152">CommonParameters</span></span>
<span data-ttu-id="c6ebb-153">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6ebb-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6ebb-154">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c6ebb-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6ebb-155">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c6ebb-155">INPUTS</span></span>

### <span data-ttu-id="c6ebb-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="c6ebb-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="c6ebb-157">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c6ebb-157">OUTPUTS</span></span>

### <span data-ttu-id="c6ebb-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="c6ebb-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="c6ebb-159">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c6ebb-159">NOTES</span></span>

## <span data-ttu-id="c6ebb-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c6ebb-160">RELATED LINKS</span></span>
