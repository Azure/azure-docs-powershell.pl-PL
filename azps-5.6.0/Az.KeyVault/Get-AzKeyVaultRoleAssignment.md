---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/get-azkeyvaultroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultRoleAssignment.md
ms.openlocfilehash: 7de4753d47ff2a285da6a9d3d60e0f95fcbf6e92
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001457"
---
# <span data-ttu-id="35a7a-101">Get-AzKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="35a7a-101">Get-AzKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="35a7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35a7a-102">SYNOPSIS</span></span>
<span data-ttu-id="35a7a-103">Uzyskiwanie lub lista przypisań ról zarządzanego hsm.</span><span class="sxs-lookup"><span data-stu-id="35a7a-103">Get or list role assignments of a managed HSM.</span></span> <span data-ttu-id="35a7a-104">Użyj odpowiednich parametrów, aby wyświetlić listę przydziałów dla określonego użytkownika lub definicji roli.</span><span class="sxs-lookup"><span data-stu-id="35a7a-104">Use respective parameters to list assignments to a specific user or a role definition.</span></span>

## <span data-ttu-id="35a7a-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="35a7a-105">SYNTAX</span></span>

### <span data-ttu-id="35a7a-106">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="35a7a-106">List (Default)</span></span>
```
Get-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] [-RoleDefinitionName <String>]
 [-RoleDefinitionId <String>] [-ObjectId <String>] [-SignInName <String>] [-ApplicationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35a7a-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="35a7a-107">GetByName</span></span>
```
Get-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleAssignmentName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35a7a-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="35a7a-108">DESCRIPTION</span></span>
<span data-ttu-id="35a7a-109">Użyj tego `Get-AzKeyVaultRoleAssignment` polecenia, aby wyświetlić listę wszystkich przydziałów ról, które mają zastosowanie w zakresie.</span><span class="sxs-lookup"><span data-stu-id="35a7a-109">Use the `Get-AzKeyVaultRoleAssignment` command to list all role assignments that are effective on a scope.</span></span>
<span data-ttu-id="35a7a-110">Bez żadnych parametrów to polecenie zwraca wszystkie przypisania ról wykonane w ramach zarządzanego systemu HSM.</span><span class="sxs-lookup"><span data-stu-id="35a7a-110">Without any parameters, this command returns all the role assignments made under the managed HSM.</span></span>
<span data-ttu-id="35a7a-111">Tę listę można filtrować przy użyciu parametrów filtrowania dla podmiotu głównego, roli i zakresu.</span><span class="sxs-lookup"><span data-stu-id="35a7a-111">This list can be filtered using filtering parameters for principal, role and scope.</span></span>
<span data-ttu-id="35a7a-112">Należy określić temat zadania.</span><span class="sxs-lookup"><span data-stu-id="35a7a-112">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="35a7a-113">Aby określić użytkownika, użyj parametrów SignInName lub Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="35a7a-113">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="35a7a-114">Aby określić grupę zabezpieczeń, użyj parametru Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="35a7a-114">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="35a7a-115">Aby określić aplikację usługi Azure AD, użyj parametrów ApplicationId lub ObjectId.</span><span class="sxs-lookup"><span data-stu-id="35a7a-115">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>
<span data-ttu-id="35a7a-116">Przypisaną rolę należy określić przy użyciu parametru RoleDefinitionName lub RoleDefinitionId.</span><span class="sxs-lookup"><span data-stu-id="35a7a-116">The role that is being assigned must be specified using the RoleDefinitionName or RoleDefinitionId parameter.</span></span>
<span data-ttu-id="35a7a-117">Zakres, w którym udzielany jest dostęp, można określić.</span><span class="sxs-lookup"><span data-stu-id="35a7a-117">The scope at which access is being granted may be specified.</span></span> <span data-ttu-id="35a7a-118">Wartość domyślna to "/".</span><span class="sxs-lookup"><span data-stu-id="35a7a-118">It defaults to "/".</span></span>

## <span data-ttu-id="35a7a-119">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="35a7a-119">EXAMPLES</span></span>

### <span data-ttu-id="35a7a-120">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="35a7a-120">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVaultRoleAssignment -HsmName myHsm

RoleDefinitionName         DisplayName                      ObjectType Scope
------------------         -----------                      ---------- -----
Managed HSM Administrator  User 1 (user1@microsoft.com)     User       /
Managed HSM Crypto Auditor User 2 (user2@microsoft.com)     User       /keys
Managed HSM Backup         User 2 (user2@microsoft.com)     User       /
Managed HSM Administrator  User 2 (user2@microsoft.com)     User       /
```

<span data-ttu-id="35a7a-121">W tym przykładzie wymieniono wszystkie przypisania ról "mójHsm" we wszystkich zakresach.</span><span class="sxs-lookup"><span data-stu-id="35a7a-121">This example lists all role assignments of "myHsm" on all the scope.</span></span>

### <span data-ttu-id="35a7a-122">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="35a7a-122">Example 2</span></span>
```powershell
PS C:\> Get-AzKeyVaultRoleAssignment -HsmName myHsm -SignInName user1@microsoft.com -Scope "/keys"

RoleDefinitionName         DisplayName                      ObjectType Scope
------------------         -----------                      ---------- -----
Managed HSM Crypto Auditor User 1 (user1@microsoft.com)     User       /keys
Managed HSM Backup         User 1 (user1@microsoft.com)     User       /keys
```

<span data-ttu-id="35a7a-123">W tym przykładzie wymieniono wszystkie przypisania ról "myHsm" w zakresie "/keys" i odfiltrowuje wynik według nazwy logowania użytkownika.</span><span class="sxs-lookup"><span data-stu-id="35a7a-123">This example lists all role assignments of "myHsm" on "/keys" scope and filters the result by user sign-in name.</span></span>

## <span data-ttu-id="35a7a-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35a7a-124">PARAMETERS</span></span>

### <span data-ttu-id="35a7a-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="35a7a-125">-ApplicationId</span></span>
<span data-ttu-id="35a7a-126">The app SPN.</span><span class="sxs-lookup"><span data-stu-id="35a7a-126">The app SPN.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases: SPN, ServicePrincipalName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35a7a-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35a7a-127">-DefaultProfile</span></span>
<span data-ttu-id="35a7a-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="35a7a-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35a7a-129">-HsmName</span><span class="sxs-lookup"><span data-stu-id="35a7a-129">-HsmName</span></span>
<span data-ttu-id="35a7a-130">Nazwa hsm.</span><span class="sxs-lookup"><span data-stu-id="35a7a-130">Name of the HSM.</span></span>

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

### <span data-ttu-id="35a7a-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="35a7a-131">-ObjectId</span></span>
<span data-ttu-id="35a7a-132">Identyfikator obiektu użytkownika lub grupy.</span><span class="sxs-lookup"><span data-stu-id="35a7a-132">The user or group object id.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases: Id, PrincipalId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35a7a-133">-RoleAssignmentName</span><span class="sxs-lookup"><span data-stu-id="35a7a-133">-RoleAssignmentName</span></span>
<span data-ttu-id="35a7a-134">Nazwa przydziału roli.</span><span class="sxs-lookup"><span data-stu-id="35a7a-134">Name of the role assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35a7a-135">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="35a7a-135">-RoleDefinitionId</span></span>
<span data-ttu-id="35a7a-136">Identyfikator roli, do których jest przydzielony podmiot zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="35a7a-136">Role Id the principal is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases: RoleId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35a7a-137">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="35a7a-137">-RoleDefinitionName</span></span>
<span data-ttu-id="35a7a-138">Nazwa roli RBAC, do których ma zostać przypisany podmiot zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="35a7a-138">Name of the RBAC role to assign the principal with.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases: RoleName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35a7a-139">— Zakres</span><span class="sxs-lookup"><span data-stu-id="35a7a-139">-Scope</span></span>
<span data-ttu-id="35a7a-140">Zakres, do którego ma zastosowanie przypisanie roli lub definicja, np. '/' lub '/keys' lub '/keys/{keyName}'.</span><span class="sxs-lookup"><span data-stu-id="35a7a-140">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="35a7a-141">W przypadku pominięcia tej przeoczonej godziny należy użyć "/".</span><span class="sxs-lookup"><span data-stu-id="35a7a-141">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="35a7a-142">-SignInName</span><span class="sxs-lookup"><span data-stu-id="35a7a-142">-SignInName</span></span>
<span data-ttu-id="35a7a-143">Nazwa_logowania użytkownika.</span><span class="sxs-lookup"><span data-stu-id="35a7a-143">The user SignInName.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases: Email, UserPrincipalName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35a7a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35a7a-144">CommonParameters</span></span>
<span data-ttu-id="35a7a-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35a7a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35a7a-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="35a7a-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35a7a-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="35a7a-147">INPUTS</span></span>

### <span data-ttu-id="35a7a-148">Brak</span><span class="sxs-lookup"><span data-stu-id="35a7a-148">None</span></span>

## <span data-ttu-id="35a7a-149">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="35a7a-149">OUTPUTS</span></span>

### <span data-ttu-id="35a7a-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="35a7a-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="35a7a-151">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="35a7a-151">NOTES</span></span>

## <span data-ttu-id="35a7a-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="35a7a-152">RELATED LINKS</span></span>
