---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azmanagedhsmroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzManagedHsmRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzManagedHsmRoleAssignment.md
ms.openlocfilehash: 038049af40d84b678da12a57918328b3b0725127
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224254"
---
# <span data-ttu-id="5edbe-101">Remove-AzManagedHsmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="5edbe-101">Remove-AzManagedHsmRoleAssignment</span></span>

## <span data-ttu-id="5edbe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5edbe-102">SYNOPSIS</span></span>
<span data-ttu-id="5edbe-103">Usuwa przypisanie roli do określonego podmiotu zabezpieczeń, który jest przypisany do określonej roli w określonym zakresie.</span><span class="sxs-lookup"><span data-stu-id="5edbe-103">Removes a role assignment to the specified principal who is assigned to a particular role at a particular scope.</span></span>

## <span data-ttu-id="5edbe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5edbe-104">SYNTAX</span></span>

### <span data-ttu-id="5edbe-105">DefinitionNameSignInName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5edbe-105">DefinitionNameSignInName (Default)</span></span>
```
Remove-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -SignInName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5edbe-106">DefinitionNameApplicationId</span><span class="sxs-lookup"><span data-stu-id="5edbe-106">DefinitionNameApplicationId</span></span>
```
Remove-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ApplicationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5edbe-107">DefinitionNameObjectId</span><span class="sxs-lookup"><span data-stu-id="5edbe-107">DefinitionNameObjectId</span></span>
```
Remove-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ObjectId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5edbe-108">DefinitionIdApplicationId</span><span class="sxs-lookup"><span data-stu-id="5edbe-108">DefinitionIdApplicationId</span></span>
```
Remove-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ApplicationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5edbe-109">DefinitionIdObjectId</span><span class="sxs-lookup"><span data-stu-id="5edbe-109">DefinitionIdObjectId</span></span>
```
Remove-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ObjectId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5edbe-110">DefinitionIdSignInName</span><span class="sxs-lookup"><span data-stu-id="5edbe-110">DefinitionIdSignInName</span></span>
```
Remove-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -SignInName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5edbe-111">RemoveByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5edbe-111">RemoveByNameParameterSet</span></span>
```
Remove-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] [-PassThru]
 -RoleAssignmentName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5edbe-112">Inputobject</span><span class="sxs-lookup"><span data-stu-id="5edbe-112">InputObject</span></span>
```
Remove-AzManagedHsmRoleAssignment [-Scope <String>] [-PassThru] -InputObject <PSKeyVaultRoleAssignment>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5edbe-113">Opis</span><span class="sxs-lookup"><span data-stu-id="5edbe-113">DESCRIPTION</span></span>
<span data-ttu-id="5edbe-114">Użyj `Remove-AzManagedHsmRoleAssignment` polecenia cmdlet, aby odebrać dostęp każdemu podmiotowi zabezpieczeń w danym zakresie i danej roli.</span><span class="sxs-lookup"><span data-stu-id="5edbe-114">Use the `Remove-AzManagedHsmRoleAssignment` cmdlet to revoke access to any principal at given scope and given role.</span></span> <span data-ttu-id="5edbe-115">NALEŻY określić obiekt główny zadania.</span><span class="sxs-lookup"><span data-stu-id="5edbe-115">The object of the assignment i.e. the principal MUST be specified.</span></span> <span data-ttu-id="5edbe-116">Głównym użytkownikiem może być użytkownik (SignInName lub identyfikator obiektu ObjectId), Grupa zabezpieczeń (użycie parametru ObjectId w celu zidentyfikowania grupy) lub podmiot zabezpieczeń (Użyj parametrów identyfikatora aplikacji lub identyfikatora ObjectId w celu zidentyfikowania elementu serviceprincipal).</span><span class="sxs-lookup"><span data-stu-id="5edbe-116">The principal can be a user (use SignInName or ObjectId parameters to identify a user), security group (use ObjectId parameter to identify a group) or service principal (use ApplicationId or ObjectId parameters to identify a ServicePrincipal.</span></span> <span data-ttu-id="5edbe-117">Rola, do której jest przypisany podmiot zabezpieczeń, musi być określona przy użyciu parametru RoleDefinitionName lub RoleDefinitionId.</span><span class="sxs-lookup"><span data-stu-id="5edbe-117">The role that the principal is assigned to MUST be specified using the RoleDefinitionName or RoleDefinitionId parameter.</span></span>

## <span data-ttu-id="5edbe-118">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5edbe-118">EXAMPLES</span></span>

### <span data-ttu-id="5edbe-119">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5edbe-119">Example 1</span></span>
```powershell
PS C:\> Remove-AzManagedHsmRoleAssignment -HsmName myHsm -RoleDefinitionName "Managed HSM Policy Administrator" -SignInName user1@microsoft.com -Scope "/keys"
```

<span data-ttu-id="5edbe-120">W tym przykładzie odwołano rolę "Administrator zarządzający zasadami HSM" user1@microsoft.com w zakresie "" w "/Keys".</span><span class="sxs-lookup"><span data-stu-id="5edbe-120">This example revokes "Managed HSM Policy Administrator" role of "user1@microsoft.com" at "/keys" scope.</span></span>

### <span data-ttu-id="5edbe-121">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="5edbe-121">Example 2</span></span>
```powershell
PS C:\> Get-AzManagedHsmRoleAssignment -HsmName myHsm -SignInName user1@microsoft.com | Remove-AzManagedHsmRoleAssignment
```

<span data-ttu-id="5edbe-122">W tym przykładzie odebrano wszystkie role " user1@microsoft.com " we wszystkich zakresach.</span><span class="sxs-lookup"><span data-stu-id="5edbe-122">This example revokes all roles of "user1@microsoft.com" at all scopes.</span></span>

## <span data-ttu-id="5edbe-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5edbe-123">PARAMETERS</span></span>

### <span data-ttu-id="5edbe-124">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="5edbe-124">-ApplicationId</span></span>
<span data-ttu-id="5edbe-125">Nazwa SPN aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5edbe-125">The app SPN.</span></span>

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

### <span data-ttu-id="5edbe-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5edbe-126">-DefaultProfile</span></span>
<span data-ttu-id="5edbe-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5edbe-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5edbe-128">-HsmName</span><span class="sxs-lookup"><span data-stu-id="5edbe-128">-HsmName</span></span>
<span data-ttu-id="5edbe-129">Nazwa modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="5edbe-129">Name of the HSM.</span></span>

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

### <span data-ttu-id="5edbe-130">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5edbe-130">-InputObject</span></span>
<span data-ttu-id="5edbe-131">Obiekt przydziału roli.</span><span class="sxs-lookup"><span data-stu-id="5edbe-131">Role assignment object.</span></span>

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

### <span data-ttu-id="5edbe-132">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="5edbe-132">-ObjectId</span></span>
<span data-ttu-id="5edbe-133">Identyfikator obiektu użytkownika lub grupy.</span><span class="sxs-lookup"><span data-stu-id="5edbe-133">The user or group object id.</span></span>

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

### <span data-ttu-id="5edbe-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5edbe-134">-PassThru</span></span>
<span data-ttu-id="5edbe-135">Zwraca wartość true, gdy HSM jest przywracany.</span><span class="sxs-lookup"><span data-stu-id="5edbe-135">Return true when the HSM is restored.</span></span>

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

### <span data-ttu-id="5edbe-136">-RoleAssignmentName</span><span class="sxs-lookup"><span data-stu-id="5edbe-136">-RoleAssignmentName</span></span>
<span data-ttu-id="5edbe-137">Nazwa przypisania roli.</span><span class="sxs-lookup"><span data-stu-id="5edbe-137">Name of the role assignment.</span></span>

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

### <span data-ttu-id="5edbe-138">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="5edbe-138">-RoleDefinitionId</span></span>
<span data-ttu-id="5edbe-139">Identyfikator roli, do której należy dany podmiot zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="5edbe-139">Role Id the principal is assigned to.</span></span>

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

### <span data-ttu-id="5edbe-140">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="5edbe-140">-RoleDefinitionName</span></span>
<span data-ttu-id="5edbe-141">Imię i nazwisko roli RBAC, z którą należy przypisać podmiot.</span><span class="sxs-lookup"><span data-stu-id="5edbe-141">Name of the RBAC role to assign the principal with.</span></span>

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

### <span data-ttu-id="5edbe-142">-Zakres</span><span class="sxs-lookup"><span data-stu-id="5edbe-142">-Scope</span></span>
<span data-ttu-id="5edbe-143">Zakres, na który dotyczy przypisanie roli lub definicja, na przykład "/" lub "/Keys" lub "/keys/{keyName}".</span><span class="sxs-lookup"><span data-stu-id="5edbe-143">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="5edbe-144">w przypadku pominięcia użyto "/".</span><span class="sxs-lookup"><span data-stu-id="5edbe-144">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="5edbe-145">-SignInName</span><span class="sxs-lookup"><span data-stu-id="5edbe-145">-SignInName</span></span>
<span data-ttu-id="5edbe-146">Użytkownik SignInName.</span><span class="sxs-lookup"><span data-stu-id="5edbe-146">The user SignInName.</span></span>

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

### <span data-ttu-id="5edbe-147">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5edbe-147">-Confirm</span></span>
<span data-ttu-id="5edbe-148">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5edbe-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5edbe-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5edbe-149">-WhatIf</span></span>
<span data-ttu-id="5edbe-150">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5edbe-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5edbe-151">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5edbe-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5edbe-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5edbe-152">CommonParameters</span></span>
<span data-ttu-id="5edbe-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5edbe-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5edbe-154">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5edbe-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5edbe-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5edbe-155">INPUTS</span></span>

### <span data-ttu-id="5edbe-156">Microsoft. Azure. Commands. platforming. models. PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="5edbe-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="5edbe-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5edbe-157">OUTPUTS</span></span>

### <span data-ttu-id="5edbe-158">Microsoft. Azure. Commands. platforming. models. PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="5edbe-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="5edbe-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5edbe-159">NOTES</span></span>

## <span data-ttu-id="5edbe-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5edbe-160">RELATED LINKS</span></span>
