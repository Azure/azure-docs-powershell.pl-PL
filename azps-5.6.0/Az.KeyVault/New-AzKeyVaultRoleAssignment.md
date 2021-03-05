---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/new-azkeyvaultroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultRoleAssignment.md
ms.openlocfilehash: ae55bf782f627c17cd73cbb075fd9f0d36ae6081
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001274"
---
# <span data-ttu-id="1a96a-101">New-AzKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="1a96a-101">New-AzKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="1a96a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a96a-102">SYNOPSIS</span></span>
<span data-ttu-id="1a96a-103">Przypisuje określoną rolę RBAC do określonego podmiotu zabezpieczeń w określonym zakresie.</span><span class="sxs-lookup"><span data-stu-id="1a96a-103">Assigns the specified RBAC role to the specified principal, at the specified scope.</span></span>

## <span data-ttu-id="1a96a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1a96a-104">SYNTAX</span></span>

### <span data-ttu-id="1a96a-105">DefinitionNameSignInName (domyślna)</span><span class="sxs-lookup"><span data-stu-id="1a96a-105">DefinitionNameSignInName (Default)</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -SignInName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a96a-106">DefinitionNameApplicationId</span><span class="sxs-lookup"><span data-stu-id="1a96a-106">DefinitionNameApplicationId</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ApplicationId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a96a-107">DefinitionNameObjectId</span><span class="sxs-lookup"><span data-stu-id="1a96a-107">DefinitionNameObjectId</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a96a-108">DefinitionIdApplicationId</span><span class="sxs-lookup"><span data-stu-id="1a96a-108">DefinitionIdApplicationId</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ApplicationId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a96a-109">DefinitionIdObjectId</span><span class="sxs-lookup"><span data-stu-id="1a96a-109">DefinitionIdObjectId</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a96a-110">DefinitionIdSignInName</span><span class="sxs-lookup"><span data-stu-id="1a96a-110">DefinitionIdSignInName</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -SignInName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a96a-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="1a96a-111">DESCRIPTION</span></span>
<span data-ttu-id="1a96a-112">Użyj tego `New-AzKeyVaultRoleAssignment` polecenia, aby udzielić dostępu.</span><span class="sxs-lookup"><span data-stu-id="1a96a-112">Use the `New-AzKeyVaultRoleAssignment` command to grant access.</span></span>
<span data-ttu-id="1a96a-113">Dostęp jest udzielany przez przypisanie do nich odpowiedniej roli RBAC w odpowiednim zakresie.</span><span class="sxs-lookup"><span data-stu-id="1a96a-113">Access is granted by assigning the appropriate RBAC role to them at the right scope.</span></span>
<span data-ttu-id="1a96a-114">Należy określić temat zadania.</span><span class="sxs-lookup"><span data-stu-id="1a96a-114">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="1a96a-115">Aby określić użytkownika, użyj parametrów SignInName lub Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="1a96a-115">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="1a96a-116">Aby określić grupę zabezpieczeń, użyj parametru Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="1a96a-116">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="1a96a-117">Aby określić aplikację usługi Azure AD, użyj parametrów ApplicationId lub ObjectId.</span><span class="sxs-lookup"><span data-stu-id="1a96a-117">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>
<span data-ttu-id="1a96a-118">Przypisaną rolę należy określić przy użyciu parametru RoleDefinitionName pr RoleDefinitionId.</span><span class="sxs-lookup"><span data-stu-id="1a96a-118">The role that is being assigned must be specified using the RoleDefinitionName pr RoleDefinitionId parameter.</span></span> <span data-ttu-id="1a96a-119">Zakres, w którym udzielany jest dostęp, można określić.</span><span class="sxs-lookup"><span data-stu-id="1a96a-119">The scope at which access is being granted may be specified.</span></span> <span data-ttu-id="1a96a-120">Domyślnie wybrana subskrypcja jest zaznaczona.</span><span class="sxs-lookup"><span data-stu-id="1a96a-120">It defaults to the selected subscription.</span></span>

## <span data-ttu-id="1a96a-121">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1a96a-121">EXAMPLES</span></span>

### <span data-ttu-id="1a96a-122">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1a96a-122">Example 1</span></span>
```powershell
PS C:\> New-AzKeyVaultRoleAssignment -HsmName myHsm -RoleDefinitionName "Managed HSM Policy Administrator" -SignInName user1@microsoft.com

RoleDefinitionName               DisplayName                    ObjectType Scope
------------------               -----------                    ---------- -----
Managed HSM Policy Administrator User 1 (user1@microsoft.com)   User       /
```

<span data-ttu-id="1a96a-123">W tym przykładzie przypisano rolę "Administrator zarządzanych zasad HSM" użytkownikowi " user1@microsoft.com w górnym zakresie.</span><span class="sxs-lookup"><span data-stu-id="1a96a-123">This example assigns role "Managed HSM Policy Administrator" to user "user1@microsoft.com" at top scope.</span></span>

## <span data-ttu-id="1a96a-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a96a-124">PARAMETERS</span></span>

### <span data-ttu-id="1a96a-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="1a96a-125">-ApplicationId</span></span>
<span data-ttu-id="1a96a-126">The app SPN.</span><span class="sxs-lookup"><span data-stu-id="1a96a-126">The app SPN.</span></span>

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

### <span data-ttu-id="1a96a-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a96a-127">-DefaultProfile</span></span>
<span data-ttu-id="1a96a-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1a96a-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a96a-129">-HsmName</span><span class="sxs-lookup"><span data-stu-id="1a96a-129">-HsmName</span></span>
<span data-ttu-id="1a96a-130">Nazwa hsm.</span><span class="sxs-lookup"><span data-stu-id="1a96a-130">Name of the HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a96a-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="1a96a-131">-ObjectId</span></span>
<span data-ttu-id="1a96a-132">Identyfikator obiektu użytkownika lub grupy.</span><span class="sxs-lookup"><span data-stu-id="1a96a-132">The user or group object id.</span></span>

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

### <span data-ttu-id="1a96a-133">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="1a96a-133">-RoleDefinitionId</span></span>
<span data-ttu-id="1a96a-134">Identyfikator roli, do których jest przydzielony podmiot zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="1a96a-134">Role Id the principal is assigned to.</span></span>

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

### <span data-ttu-id="1a96a-135">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="1a96a-135">-RoleDefinitionName</span></span>
<span data-ttu-id="1a96a-136">Nazwa roli RBAC, do których ma zostać przypisany podmiot zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="1a96a-136">Name of the RBAC role to assign the principal with.</span></span>

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

### <span data-ttu-id="1a96a-137">— Zakres</span><span class="sxs-lookup"><span data-stu-id="1a96a-137">-Scope</span></span>
<span data-ttu-id="1a96a-138">Zakres, do którego ma zastosowanie przypisanie roli lub definicja, np. '/' lub '/keys' lub '/keys/{keyName}'.</span><span class="sxs-lookup"><span data-stu-id="1a96a-138">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="1a96a-139">W przypadku pominięcia tej przeoczonej godziny należy użyć "/".</span><span class="sxs-lookup"><span data-stu-id="1a96a-139">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="1a96a-140">-SignInName</span><span class="sxs-lookup"><span data-stu-id="1a96a-140">-SignInName</span></span>
<span data-ttu-id="1a96a-141">Nazwa_logowania użytkownika.</span><span class="sxs-lookup"><span data-stu-id="1a96a-141">The user SignInName.</span></span>

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

### <span data-ttu-id="1a96a-142">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1a96a-142">-Confirm</span></span>
<span data-ttu-id="1a96a-143">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1a96a-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a96a-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a96a-144">-WhatIf</span></span>
<span data-ttu-id="1a96a-145">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a96a-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a96a-146">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1a96a-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a96a-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a96a-147">CommonParameters</span></span>
<span data-ttu-id="1a96a-148">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a96a-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a96a-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1a96a-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a96a-150">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1a96a-150">INPUTS</span></span>

### <span data-ttu-id="1a96a-151">Brak</span><span class="sxs-lookup"><span data-stu-id="1a96a-151">None</span></span>

## <span data-ttu-id="1a96a-152">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1a96a-152">OUTPUTS</span></span>

### <span data-ttu-id="1a96a-153">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="1a96a-153">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="1a96a-154">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1a96a-154">NOTES</span></span>

## <span data-ttu-id="1a96a-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1a96a-155">RELATED LINKS</span></span>
