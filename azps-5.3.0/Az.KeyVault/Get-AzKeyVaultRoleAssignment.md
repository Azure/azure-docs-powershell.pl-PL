---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultRoleAssignment.md
ms.openlocfilehash: c610339bf90069f30d6107d46fc92fd896d6816c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98500926"
---
# <span data-ttu-id="e03da-101">Get-AzKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="e03da-101">Get-AzKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="e03da-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e03da-102">SYNOPSIS</span></span>
<span data-ttu-id="e03da-103">Uzyskiwanie lub wyświetlanie przydziałów ról zarządzanego modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="e03da-103">Get or list role assignments of a managed HSM.</span></span> <span data-ttu-id="e03da-104">Użyj odpowiednich parametrów, aby wyświetlić listę przydziałów dla określonego użytkownika lub definicji roli.</span><span class="sxs-lookup"><span data-stu-id="e03da-104">Use respective parameters to list assignments to a specific user or a role definition.</span></span>

## <span data-ttu-id="e03da-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e03da-105">SYNTAX</span></span>

### <span data-ttu-id="e03da-106">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="e03da-106">List (Default)</span></span>
```
Get-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] [-RoleDefinitionName <String>]
 [-RoleDefinitionId <String>] [-ObjectId <String>] [-SignInName <String>] [-ApplicationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e03da-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="e03da-107">GetByName</span></span>
```
Get-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleAssignmentName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e03da-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e03da-108">DESCRIPTION</span></span>
<span data-ttu-id="e03da-109">Użyj tego `Get-AzKeyVaultRoleAssignment` polecenia, aby wyświetlić wszystkie przydziały ról, które obowiązują w zakresie.</span><span class="sxs-lookup"><span data-stu-id="e03da-109">Use the `Get-AzKeyVaultRoleAssignment` command to list all role assignments that are effective on a scope.</span></span>
<span data-ttu-id="e03da-110">Bez żadnych parametrów to polecenie zwraca wszystkie zadania ról utworzone w ramach zarządzanego modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="e03da-110">Without any parameters, this command returns all the role assignments made under the managed HSM.</span></span>
<span data-ttu-id="e03da-111">Ta lista może być filtrowana przy użyciu parametrów filtrowania podmiotu zabezpieczeń, roli i zakresu.</span><span class="sxs-lookup"><span data-stu-id="e03da-111">This list can be filtered using filtering parameters for principal, role and scope.</span></span>
<span data-ttu-id="e03da-112">Należy określić temat zadania.</span><span class="sxs-lookup"><span data-stu-id="e03da-112">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="e03da-113">Aby określić użytkownika, użyj parametrów SignInName lub Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="e03da-113">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="e03da-114">Aby określić grupę zabezpieczeń, użyj parametru ObjectId usługi Azure AD.</span><span class="sxs-lookup"><span data-stu-id="e03da-114">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="e03da-115">Aby określić aplikację Azure AD, użyj parametrów identyfikatora aplikacji lub obiektu ObjectId.</span><span class="sxs-lookup"><span data-stu-id="e03da-115">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>
<span data-ttu-id="e03da-116">Rola, która jest przypisywana, musi być określona przy użyciu parametru RoleDefinitionName lub RoleDefinitionId.</span><span class="sxs-lookup"><span data-stu-id="e03da-116">The role that is being assigned must be specified using the RoleDefinitionName or RoleDefinitionId parameter.</span></span>
<span data-ttu-id="e03da-117">Zakres, w którym jest udzielany dostęp, można określić.</span><span class="sxs-lookup"><span data-stu-id="e03da-117">The scope at which access is being granted may be specified.</span></span> <span data-ttu-id="e03da-118">Domyślnie jest to "/".</span><span class="sxs-lookup"><span data-stu-id="e03da-118">It defaults to "/".</span></span>

## <span data-ttu-id="e03da-119">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e03da-119">EXAMPLES</span></span>

### <span data-ttu-id="e03da-120">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e03da-120">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVaultRoleAssignment -HsmName myHsm

RoleDefinitionName         DisplayName                      ObjectType Scope
------------------         -----------                      ---------- -----
Managed HSM Administrator  User 1 (user1@microsoft.com)     User       /
Managed HSM Crypto Auditor User 2 (user2@microsoft.com)     User       /keys
Managed HSM Backup         User 2 (user2@microsoft.com)     User       /
Managed HSM Administrator  User 2 (user2@microsoft.com)     User       /
```

<span data-ttu-id="e03da-121">W tym przykładzie podano wszystkie przypisania ról dotyczące "myHsm" we wszystkich zakresach.</span><span class="sxs-lookup"><span data-stu-id="e03da-121">This example lists all role assignments of "myHsm" on all the scope.</span></span>

### <span data-ttu-id="e03da-122">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e03da-122">Example 2</span></span>
```powershell
PS C:\> Get-AzKeyVaultRoleAssignment -HsmName myHsm -SignInName user1@microsoft.com -Scope "/keys"

RoleDefinitionName         DisplayName                      ObjectType Scope
------------------         -----------                      ---------- -----
Managed HSM Crypto Auditor User 1 (user1@microsoft.com)     User       /keys
Managed HSM Backup         User 1 (user1@microsoft.com)     User       /keys
```

<span data-ttu-id="e03da-123">W tym przykładzie wymieniono wszystkie przypisania ról "myHsm" w zakresie "/Keys" i filtruje wynik według nazwy logowania użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e03da-123">This example lists all role assignments of "myHsm" on "/keys" scope and filters the result by user sign-in name.</span></span>

## <span data-ttu-id="e03da-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e03da-124">PARAMETERS</span></span>

### <span data-ttu-id="e03da-125">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="e03da-125">-ApplicationId</span></span>
<span data-ttu-id="e03da-126">Nazwa SPN aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e03da-126">The app SPN.</span></span>

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

### <span data-ttu-id="e03da-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e03da-127">-DefaultProfile</span></span>
<span data-ttu-id="e03da-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e03da-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e03da-129">-HsmName</span><span class="sxs-lookup"><span data-stu-id="e03da-129">-HsmName</span></span>
<span data-ttu-id="e03da-130">Nazwa modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="e03da-130">Name of the HSM.</span></span>

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

### <span data-ttu-id="e03da-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="e03da-131">-ObjectId</span></span>
<span data-ttu-id="e03da-132">Identyfikator obiektu użytkownika lub grupy.</span><span class="sxs-lookup"><span data-stu-id="e03da-132">The user or group object id.</span></span>

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

### <span data-ttu-id="e03da-133">-RoleAssignmentName</span><span class="sxs-lookup"><span data-stu-id="e03da-133">-RoleAssignmentName</span></span>
<span data-ttu-id="e03da-134">Nazwa przypisania roli.</span><span class="sxs-lookup"><span data-stu-id="e03da-134">Name of the role assignment.</span></span>

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

### <span data-ttu-id="e03da-135">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="e03da-135">-RoleDefinitionId</span></span>
<span data-ttu-id="e03da-136">Identyfikator roli, do której należy dany podmiot zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="e03da-136">Role Id the principal is assigned to.</span></span>

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

### <span data-ttu-id="e03da-137">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="e03da-137">-RoleDefinitionName</span></span>
<span data-ttu-id="e03da-138">Imię i nazwisko roli RBAC, z którą należy przypisać podmiot.</span><span class="sxs-lookup"><span data-stu-id="e03da-138">Name of the RBAC role to assign the principal with.</span></span>

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

### <span data-ttu-id="e03da-139">-Zakres</span><span class="sxs-lookup"><span data-stu-id="e03da-139">-Scope</span></span>
<span data-ttu-id="e03da-140">Zakres, na który dotyczy przypisanie roli lub definicja, na przykład "/" lub "/Keys" lub "/keys/{keyName}".</span><span class="sxs-lookup"><span data-stu-id="e03da-140">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="e03da-141">w przypadku pominięcia użyto "/".</span><span class="sxs-lookup"><span data-stu-id="e03da-141">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="e03da-142">-SignInName</span><span class="sxs-lookup"><span data-stu-id="e03da-142">-SignInName</span></span>
<span data-ttu-id="e03da-143">Użytkownik SignInName.</span><span class="sxs-lookup"><span data-stu-id="e03da-143">The user SignInName.</span></span>

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

### <span data-ttu-id="e03da-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e03da-144">CommonParameters</span></span>
<span data-ttu-id="e03da-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e03da-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e03da-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e03da-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e03da-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e03da-147">INPUTS</span></span>

### <span data-ttu-id="e03da-148">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e03da-148">None</span></span>

## <span data-ttu-id="e03da-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e03da-149">OUTPUTS</span></span>

### <span data-ttu-id="e03da-150">Microsoft. Azure. Commands. platforming. models. PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="e03da-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="e03da-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e03da-151">NOTES</span></span>

## <span data-ttu-id="e03da-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e03da-152">RELATED LINKS</span></span>
