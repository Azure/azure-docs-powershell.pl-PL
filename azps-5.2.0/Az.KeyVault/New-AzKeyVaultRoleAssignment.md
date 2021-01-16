---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultRoleAssignment.md
ms.openlocfilehash: ee90ab1b4ba22f1a5c40427f7fc435c75cef992d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336973"
---
# <span data-ttu-id="3652b-101">New-AzKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="3652b-101">New-AzKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="3652b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3652b-102">SYNOPSIS</span></span>
<span data-ttu-id="3652b-103">Umożliwia przypisanie określonej roli RBAC do określonego podmiotu zabezpieczeń w określonym zakresie.</span><span class="sxs-lookup"><span data-stu-id="3652b-103">Assigns the specified RBAC role to the specified principal, at the specified scope.</span></span>

## <span data-ttu-id="3652b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3652b-104">SYNTAX</span></span>

### <span data-ttu-id="3652b-105">DefinitionNameSignInName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3652b-105">DefinitionNameSignInName (Default)</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -SignInName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3652b-106">DefinitionNameApplicationId</span><span class="sxs-lookup"><span data-stu-id="3652b-106">DefinitionNameApplicationId</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ApplicationId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3652b-107">DefinitionNameObjectId</span><span class="sxs-lookup"><span data-stu-id="3652b-107">DefinitionNameObjectId</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3652b-108">DefinitionIdApplicationId</span><span class="sxs-lookup"><span data-stu-id="3652b-108">DefinitionIdApplicationId</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ApplicationId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3652b-109">DefinitionIdObjectId</span><span class="sxs-lookup"><span data-stu-id="3652b-109">DefinitionIdObjectId</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3652b-110">DefinitionIdSignInName</span><span class="sxs-lookup"><span data-stu-id="3652b-110">DefinitionIdSignInName</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -SignInName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3652b-111">Opis</span><span class="sxs-lookup"><span data-stu-id="3652b-111">DESCRIPTION</span></span>
<span data-ttu-id="3652b-112">`New-AzKeyVaultRoleAssignment`Aby udzielić dostępu, użyj polecenia.</span><span class="sxs-lookup"><span data-stu-id="3652b-112">Use the `New-AzKeyVaultRoleAssignment` command to grant access.</span></span>
<span data-ttu-id="3652b-113">Dostęp jest udzielany przez przypisanie odpowiedniej roli RBAC do odpowiednich zakresów.</span><span class="sxs-lookup"><span data-stu-id="3652b-113">Access is granted by assigning the appropriate RBAC role to them at the right scope.</span></span>
<span data-ttu-id="3652b-114">Należy określić temat zadania.</span><span class="sxs-lookup"><span data-stu-id="3652b-114">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="3652b-115">Aby określić użytkownika, użyj parametrów SignInName lub Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="3652b-115">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="3652b-116">Aby określić grupę zabezpieczeń, użyj parametru ObjectId usługi Azure AD.</span><span class="sxs-lookup"><span data-stu-id="3652b-116">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="3652b-117">Aby określić aplikację Azure AD, użyj parametrów identyfikatora aplikacji lub obiektu ObjectId.</span><span class="sxs-lookup"><span data-stu-id="3652b-117">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>
<span data-ttu-id="3652b-118">Rola, która jest przypisywana, musi być określona przy użyciu parametru RoleDefinitionId PR RoleDefinitionName.</span><span class="sxs-lookup"><span data-stu-id="3652b-118">The role that is being assigned must be specified using the RoleDefinitionName pr RoleDefinitionId parameter.</span></span> <span data-ttu-id="3652b-119">Zakres, w którym jest udzielany dostęp, można określić.</span><span class="sxs-lookup"><span data-stu-id="3652b-119">The scope at which access is being granted may be specified.</span></span> <span data-ttu-id="3652b-120">Domyślna wybrana subskrypcja.</span><span class="sxs-lookup"><span data-stu-id="3652b-120">It defaults to the selected subscription.</span></span>

## <span data-ttu-id="3652b-121">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3652b-121">EXAMPLES</span></span>

### <span data-ttu-id="3652b-122">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3652b-122">Example 1</span></span>
```powershell
PS C:\> New-AzKeyVaultRoleAssignment -HsmName myHsm -RoleDefinitionName "Managed HSM Policy Administrator" -SignInName user1@microsoft.com

RoleDefinitionName               DisplayName                    ObjectType Scope
------------------               -----------                    ---------- -----
Managed HSM Policy Administrator User 1 (user1@microsoft.com)   User       /
```

<span data-ttu-id="3652b-123">W tym przykładzie przypisano rolę "Administrator zarządzający zasadami modułu HSM" do użytkownika " user1@microsoft.com " w najwyższym zakresie.</span><span class="sxs-lookup"><span data-stu-id="3652b-123">This example assigns role "Managed HSM Policy Administrator" to user "user1@microsoft.com" at top scope.</span></span>

## <span data-ttu-id="3652b-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3652b-124">PARAMETERS</span></span>

### <span data-ttu-id="3652b-125">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="3652b-125">-ApplicationId</span></span>
<span data-ttu-id="3652b-126">Nazwa SPN aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3652b-126">The app SPN.</span></span>

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

### <span data-ttu-id="3652b-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3652b-127">-DefaultProfile</span></span>
<span data-ttu-id="3652b-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3652b-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3652b-129">-HsmName</span><span class="sxs-lookup"><span data-stu-id="3652b-129">-HsmName</span></span>
<span data-ttu-id="3652b-130">Nazwa modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="3652b-130">Name of the HSM.</span></span>

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

### <span data-ttu-id="3652b-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="3652b-131">-ObjectId</span></span>
<span data-ttu-id="3652b-132">Identyfikator obiektu użytkownika lub grupy.</span><span class="sxs-lookup"><span data-stu-id="3652b-132">The user or group object id.</span></span>

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

### <span data-ttu-id="3652b-133">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="3652b-133">-RoleDefinitionId</span></span>
<span data-ttu-id="3652b-134">Identyfikator roli, do której należy dany podmiot zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="3652b-134">Role Id the principal is assigned to.</span></span>

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

### <span data-ttu-id="3652b-135">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="3652b-135">-RoleDefinitionName</span></span>
<span data-ttu-id="3652b-136">Imię i nazwisko roli RBAC, z którą należy przypisać podmiot.</span><span class="sxs-lookup"><span data-stu-id="3652b-136">Name of the RBAC role to assign the principal with.</span></span>

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

### <span data-ttu-id="3652b-137">-Zakres</span><span class="sxs-lookup"><span data-stu-id="3652b-137">-Scope</span></span>
<span data-ttu-id="3652b-138">Zakres, na który dotyczy przypisanie roli lub definicja, na przykład "/" lub "/Keys" lub "/keys/{keyName}".</span><span class="sxs-lookup"><span data-stu-id="3652b-138">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="3652b-139">w przypadku pominięcia użyto "/".</span><span class="sxs-lookup"><span data-stu-id="3652b-139">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="3652b-140">-SignInName</span><span class="sxs-lookup"><span data-stu-id="3652b-140">-SignInName</span></span>
<span data-ttu-id="3652b-141">Użytkownik SignInName.</span><span class="sxs-lookup"><span data-stu-id="3652b-141">The user SignInName.</span></span>

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

### <span data-ttu-id="3652b-142">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3652b-142">-Confirm</span></span>
<span data-ttu-id="3652b-143">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3652b-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3652b-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3652b-144">-WhatIf</span></span>
<span data-ttu-id="3652b-145">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3652b-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3652b-146">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3652b-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3652b-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3652b-147">CommonParameters</span></span>
<span data-ttu-id="3652b-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3652b-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3652b-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3652b-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3652b-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3652b-150">INPUTS</span></span>

### <span data-ttu-id="3652b-151">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3652b-151">None</span></span>

## <span data-ttu-id="3652b-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3652b-152">OUTPUTS</span></span>

### <span data-ttu-id="3652b-153">Microsoft. Azure. Commands. platforming. models. PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="3652b-153">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="3652b-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3652b-154">NOTES</span></span>

## <span data-ttu-id="3652b-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3652b-155">RELATED LINKS</span></span>
