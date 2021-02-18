---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 636FAD5B-8C39-4E5C-8978-6845C6B89BC0
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
ms.openlocfilehash: 5f47237088808fe8966d239f9a0de7c892301db0
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100410722"
---
# <span data-ttu-id="19f3c-101">Set-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="19f3c-101">Set-AzKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="19f3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19f3c-102">SYNOPSIS</span></span>
<span data-ttu-id="19f3c-103">Udziela lub modyfikuje istniejące uprawnienia użytkownika, aplikacji lub grupy zabezpieczeń do wykonywania operacji z magazynem kluczy.</span><span class="sxs-lookup"><span data-stu-id="19f3c-103">Grants or modifies existing permissions for a user, application, or security group to perform operations with a key vault.</span></span>

## <span data-ttu-id="19f3c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="19f3c-104">SYNTAX</span></span>

### <span data-ttu-id="19f3c-105">ByUserPrincipalName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="19f3c-105">ByUserPrincipalName (Default)</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="19f3c-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="19f3c-106">ByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19f3c-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="19f3c-107">ByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="19f3c-108">ByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="19f3c-108">ByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="19f3c-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="19f3c-109">ForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19f3c-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="19f3c-110">InputObjectByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19f3c-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="19f3c-111">InputObjectByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="19f3c-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="19f3c-112">InputObjectByUserPrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="19f3c-113">InputObjectByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="19f3c-113">InputObjectByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="19f3c-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="19f3c-114">InputObjectForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19f3c-115">ResourceIdByObjectId</span><span class="sxs-lookup"><span data-stu-id="19f3c-115">ResourceIdByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19f3c-116">ResourceIdByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="19f3c-116">ResourceIdByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="19f3c-117">ResourceIdByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="19f3c-117">ResourceIdByUserPrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -UserPrincipalName <String> [-PermissionsToKeys <String[]>]
 [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19f3c-118">ResourceIdByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="19f3c-118">ResourceIdByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -EmailAddress <String> [-PermissionsToKeys <String[]>]
 [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19f3c-119">ResourceIdForVault</span><span class="sxs-lookup"><span data-stu-id="19f3c-119">ResourceIdForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> [-EnabledForDeployment] [-EnabledForTemplateDeployment]
 [-EnabledForDiskEncryption] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="19f3c-120">OPIS</span><span class="sxs-lookup"><span data-stu-id="19f3c-120">DESCRIPTION</span></span>
<span data-ttu-id="19f3c-121">Polecenie **cmdlet Set-AzKeyVaultAccessPolicy** udziela lub modyfikuje istniejące uprawnienia użytkownika, aplikacji lub grupy zabezpieczeń do wykonywania określonych operacji za pomocą magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="19f3c-121">The **Set-AzKeyVaultAccessPolicy** cmdlet grants or modifies existing permissions for a user, application, or security group to perform the specified operations with a key vault.</span></span> <span data-ttu-id="19f3c-122">Nie modyfikuje uprawnień innych użytkowników, aplikacji ani grup zabezpieczeń w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="19f3c-122">It does not modify the permissions that other users, applications, or security groups have on the key vault.</span></span>
<span data-ttu-id="19f3c-123">Jeśli ustawiasz uprawnienia dla grupy zabezpieczeń, ta operacja dotyczy tylko użytkowników w tej grupie zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="19f3c-123">If you are setting permissions for a security group, this operation affects only users in that security group.</span></span>
<span data-ttu-id="19f3c-124">Wszystkie następujące katalogi muszą mieć ten sam katalog Azure:</span><span class="sxs-lookup"><span data-stu-id="19f3c-124">The following directories must all be the same Azure directory:</span></span>
- <span data-ttu-id="19f3c-125">Domyślny katalog subskrypcji platformy Azure, w którym znajduje się magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="19f3c-125">The default directory of the Azure subscription in which the key vault resides.</span></span>
- <span data-ttu-id="19f3c-126">Katalog Azure zawierający użytkownika lub grupę aplikacji, do których chcesz przyznać uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="19f3c-126">The Azure directory that contains the user or application group that you are granting permissions to.</span></span>
<span data-ttu-id="19f3c-127">Przykłady scenariuszy, w których te warunki nie są spełnione i to polecenie cmdlet nie będzie działać:</span><span class="sxs-lookup"><span data-stu-id="19f3c-127">Examples of scenarios when these conditions are not met and this cmdlet will not work are:</span></span>
- <span data-ttu-id="19f3c-128">Autoryzowanie użytkownika z innej organizacji w celu zarządzania Twoim magazynem kluczy.</span><span class="sxs-lookup"><span data-stu-id="19f3c-128">Authorizing a user from a different organization to manage your key vault.</span></span>
<span data-ttu-id="19f3c-129">Każda organizacja ma własny katalog.</span><span class="sxs-lookup"><span data-stu-id="19f3c-129">Each organization has its own directory.</span></span>
- <span data-ttu-id="19f3c-130">Twoje konto platformy Azure ma wiele katalogów.</span><span class="sxs-lookup"><span data-stu-id="19f3c-130">Your Azure account has multiple directories.</span></span>
<span data-ttu-id="19f3c-131">Jeśli zarejestrujesz aplikację w katalogu innym niż katalog domyślny, nie możesz autoryzować tej aplikacji do używania Twojego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="19f3c-131">If you register an application in a directory other than the default directory, you cannot authorize that application to use your key vault.</span></span>
<span data-ttu-id="19f3c-132">Aplikacja musi znajdować się w katalogu domyślnym.</span><span class="sxs-lookup"><span data-stu-id="19f3c-132">The application must be in the default directory.</span></span>
<span data-ttu-id="19f3c-133">Pamiętaj, że mimo że w przypadku tego polecenia cmdlet określenie grupy zasobów jest opcjonalne, należy to zrobić, aby uzyskać lepszą wydajność.</span><span class="sxs-lookup"><span data-stu-id="19f3c-133">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

> [!NOTE]
> <span data-ttu-id="19f3c-134">Podczas udzielania uprawnień zasad dostępu za pomocą podmiotu zabezpieczeń usługi należy użyć `-BypassObjectIdValidation` parametru.</span><span class="sxs-lookup"><span data-stu-id="19f3c-134">When using a service principal to grant access policy permissions, you must use the `-BypassObjectIdValidation` parameter.</span></span>

## <span data-ttu-id="19f3c-135">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="19f3c-135">EXAMPLES</span></span>

### <span data-ttu-id="19f3c-136">Przykład 1. Udzielanie użytkownikowi uprawnień do magazynu kluczy i modyfikowanie uprawnień</span><span class="sxs-lookup"><span data-stu-id="19f3c-136">Example 1: Grant permissions to a user for a key vault and modify the permissions</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys create,import,delete,list -PermissionsToSecrets set,delete -PassThru

Vault Name                       : Contoso03Vault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             : True
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : create, import, delete, list
                                   Permissions to Secrets                     : set, delete
                                   Permissions to Certificates                :
                                   Permissions to (Key Vault Managed) Storage :

Tags                             :

PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets set,delete,get -PassThru

Vault Name                       : Contoso03Vault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             : True
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : create, import, delete, list
                                   Permissions to Secrets                     : set, delete, get
                                   Permissions to Certificates                :
                                   Permissions to (Key Vault Managed) Storage :

Tags                             :

PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys @() -PassThru

Vault Name                       : Contoso03Vault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             : True
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        :
                                   Permissions to Secrets                     : set, delete, get
                                   Permissions to Certificates                :
                                   Permissions to (Key Vault Managed) Storage :

Tags                             :
```

<span data-ttu-id="19f3c-137">Pierwsze polecenie udziela użytkownikowi w usłudze Azure Active Directory uprawnień do wykonywania operacji na kluczach i tajemnicach związanych z magazynem kluczy o nazwie PattiFuller@contoso.com Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="19f3c-137">The first command grants permissions for a user in your Azure Active Directory, PattiFuller@contoso.com, to perform operations on keys and secrets with a key vault named Contoso03Vault.</span></span> <span data-ttu-id="19f3c-138">Parametr *PassThru* powoduje zwrócenie zaktualizowanego obiektu przez polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19f3c-138">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>
<span data-ttu-id="19f3c-139">Drugie polecenie modyfikuje uprawnienia, które zostały przyznane w pierwszym poleceniu, aby teraz zezwolić na uzyskiwanie sekretów oprócz ich ustawiania PattiFuller@contoso.com i usuwania.</span><span class="sxs-lookup"><span data-stu-id="19f3c-139">The second command modifies the permissions that were granted to PattiFuller@contoso.com in the first command, to now allow getting secrets in addition to setting and deleting them.</span></span> <span data-ttu-id="19f3c-140">Po tym poleceniu uprawnienia do operacji na kluczach pozostaną niezmienione.</span><span class="sxs-lookup"><span data-stu-id="19f3c-140">The permissions to key operations remain unchanged after this command.</span></span>
<span data-ttu-id="19f3c-141">Ostatnie polecenie dodatkowo zmodyfikuje istniejące uprawnienia do PattiFuller@contoso.com usuwania wszystkich uprawnień do kluczowych operacji.</span><span class="sxs-lookup"><span data-stu-id="19f3c-141">The final command further modifies the existing permissions for PattiFuller@contoso.com to remove all permissions to key operations.</span></span> <span data-ttu-id="19f3c-142">Uprawnienia do operacji tajnych pozostają niezmienione po tym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="19f3c-142">The permissions to secret operations remain unchanged after this command.</span></span>

### <span data-ttu-id="19f3c-143">Przykład 2. Udzielanie uprawnień podmiotu zabezpieczeń usługi aplikacji do odczytu i zapisu sekretów</span><span class="sxs-lookup"><span data-stu-id="19f3c-143">Example 2: Grant permissions for an application service principal to read and write secrets</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com' -PermissionsToSecrets Get,Set
```

<span data-ttu-id="19f3c-144">To polecenie udziela uprawnień aplikacji dla magazynu kluczy o nazwie Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="19f3c-144">This command grants permissions for an application for a key vault named Contoso03Vault.</span></span>
<span data-ttu-id="19f3c-145">Parametr *ServicePrincipalName* określa aplikację.</span><span class="sxs-lookup"><span data-stu-id="19f3c-145">The *ServicePrincipalName* parameter specifies the application.</span></span> <span data-ttu-id="19f3c-146">Aplikacja musi być zarejestrowana w usłudze Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="19f3c-146">The application must be registered in your Azure Active Directory.</span></span> <span data-ttu-id="19f3c-147">Wartość parametru *ServicePrincipalName* musi być główną nazwą usługi aplikacji lub identyfikatorem GUID aplikacji.</span><span class="sxs-lookup"><span data-stu-id="19f3c-147">The value of the *ServicePrincipalName* parameter must be either the service principal name of the application or the application ID GUID.</span></span>
<span data-ttu-id="19f3c-148">W tym przykładzie określono nazwę podmiotu zabezpieczeń usługi, a polecenie przyznaje uprawnienia aplikacji `http://payroll.contoso.com` do odczytu i zapisu sekretów.</span><span class="sxs-lookup"><span data-stu-id="19f3c-148">This example specifies the service principal name `http://payroll.contoso.com`, and the command grants the application permissions to read and write secrets.</span></span>

### <span data-ttu-id="19f3c-149">Przykład 3. Udzielanie uprawnień aplikacji przy użyciu identyfikatora obiektu</span><span class="sxs-lookup"><span data-stu-id="19f3c-149">Example 3: Grant permissions for an application using its object ID</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectId 34595082-9346-41b6-8d6b-295a2808b8db -PermissionsToSecrets Get,Set
```

<span data-ttu-id="19f3c-150">To polecenie udziela uprawnień aplikacji do odczytu i zapisu sekretów.</span><span class="sxs-lookup"><span data-stu-id="19f3c-150">This command grants the application permissions to read and write secrets.</span></span>
<span data-ttu-id="19f3c-151">W tym przykładzie określono aplikację, używając identyfikatora obiektu podmiotu zabezpieczeń usługi aplikacji.</span><span class="sxs-lookup"><span data-stu-id="19f3c-151">This example specifies the application using the object ID of the service principal of the application.</span></span>

### <span data-ttu-id="19f3c-152">Przykład 4. Udzielanie uprawnień do głównej nazwy użytkownika</span><span class="sxs-lookup"><span data-stu-id="19f3c-152">Example 4: Grant permissions for a user principal name</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets Get,List,Set
```

<span data-ttu-id="19f3c-153">To polecenie pozwala uzyskać, wyświetlić listę i ustawić uprawnienia dla określonej głównej nazwy użytkownika w celu uzyskania dostępu do tajemnic.</span><span class="sxs-lookup"><span data-stu-id="19f3c-153">This command grants get, list, and set permissions for the specified user principal name for access to secrets.</span></span>

### <span data-ttu-id="19f3c-154">Przykład 5. Włączanie pobierania tajemnic z magazynu kluczy przez dostawcę zasobów Microsoft.Compute</span><span class="sxs-lookup"><span data-stu-id="19f3c-154">Example 5: Enable secrets to be retrieved from a key vault by the Microsoft.Compute resource provider</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="19f3c-155">To polecenie udziela uprawnień dla tajemnic, które mają być pobierane z magazynu kluczy Contoso03Vault przez dostawcę zasobów Microsoft.Compute.</span><span class="sxs-lookup"><span data-stu-id="19f3c-155">This command grants the permissions for secrets to be retrieved from the Contoso03Vault key vault by the Microsoft.Compute resource provider.</span></span>

### <span data-ttu-id="19f3c-156">Przykład 6. Udzielanie uprawnień grupie zabezpieczeń</span><span class="sxs-lookup"><span data-stu-id="19f3c-156">Example 6: Grant permissions to a security group</span></span>
```powershell
PS C:\> Get-AzADGroup
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'myownvault' -ObjectId (Get-AzADGroup -SearchString 'group2')[0].Id -PermissionsToKeys get, set -PermissionsToSecrets get, set
```

<span data-ttu-id="19f3c-157">Pierwsze polecenie używa polecenia cmdlet Get-AzADGroup do uzyskania wszystkich grup usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="19f3c-157">The first command uses the Get-AzADGroup cmdlet to get all Active Directory groups.</span></span> <span data-ttu-id="19f3c-158">W wyniku widać 3 zwrócone grupy o nazwie **group1,** **group2** i **group3.**</span><span class="sxs-lookup"><span data-stu-id="19f3c-158">From the output, you see 3 groups returned, named **group1**, **group2**, and **group3**.</span></span> <span data-ttu-id="19f3c-159">Wiele grup może mieć tę samą nazwę, ale zawsze ma unikatowy identyfikator ObjectId.</span><span class="sxs-lookup"><span data-stu-id="19f3c-159">Multiple groups can have the same name but always have a unique ObjectId.</span></span> <span data-ttu-id="19f3c-160">Jeśli jest zwracana więcej niż jedna grupa o takiej samej nazwie, należy użyć w wynikach obiektu ObjectId, aby zidentyfikować tę, której chcesz użyć.</span><span class="sxs-lookup"><span data-stu-id="19f3c-160">When more than one group that has the same name is returned, use the ObjectId in the output to identify the one you want to use.</span></span>
<span data-ttu-id="19f3c-161">Następnie użyj danych wyjściowych tego polecenia z Set-AzKeyVaultAccessPolicy, aby udzielić uprawnień do grupy Group2 dla Twojego magazynu kluczy o **nazwie myownvault.**</span><span class="sxs-lookup"><span data-stu-id="19f3c-161">You then use the output of this command with Set-AzKeyVaultAccessPolicy to grant permissions to group2 for your key vault, named **myownvault**.</span></span> <span data-ttu-id="19f3c-162">W tym przykładzie wyliczane są grupy o nazwie "grupa2" w tym samym wierszu polecenia.</span><span class="sxs-lookup"><span data-stu-id="19f3c-162">This example enumerates the groups named 'group2' inline in the same command line.</span></span>
<span data-ttu-id="19f3c-163">Na liście zwróconej może być wiele grup o nazwie "grupa2".</span><span class="sxs-lookup"><span data-stu-id="19f3c-163">There may be multiple groups in the returned list that are named 'group2'.</span></span>
<span data-ttu-id="19f3c-164">W tym przykładzie jest wybierany pierwszy indeks \[ 0 \] na liście zwróconej.</span><span class="sxs-lookup"><span data-stu-id="19f3c-164">This example picks the first one, indicated by index \[0\] in the returned list.</span></span>

### <span data-ttu-id="19f3c-165">Przykład 7. Udzielanie usłudze Azure Information Protection dostępu do klucza dzierżawy zarządzanej przez klienta (BYOK)</span><span class="sxs-lookup"><span data-stu-id="19f3c-165">Example 7: Grant Azure Information Protection access to the customer-managed tenant key (BYOK)</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso04Vault' -ServicePrincipalName 00000012-0000-0000-c000-000000000000 -PermissionsToKeys decrypt,sign,get
```

<span data-ttu-id="19f3c-166">To polecenie autoryzuje usługę Azure Information Protection do używania klucza zarządzanego przez klienta (czyli klucza własnego, czyli scenariusza "BYOK") jako klucza dzierżawy usługi Azure Information Protection.</span><span class="sxs-lookup"><span data-stu-id="19f3c-166">This command authorizes Azure Information Protection to use a customer-managed key (the bring your own key, or "BYOK" scenario) as the Azure Information Protection tenant key.</span></span>
<span data-ttu-id="19f3c-167">Po uruchomieniu tego polecenia określ własną nazwę magazynu kluczy, ale musisz określić parametr *ServicePrincipalName* z identyfikatorem GUID **00000012-0000-0000-c000-000000000000** oraz określić uprawnienia w przykładzie.</span><span class="sxs-lookup"><span data-stu-id="19f3c-167">When you run this command, specify your own key vault name but you must specify the *ServicePrincipalName* parameter with the GUID **00000012-0000-0000-c000-000000000000** and specify the permissions in the example.</span></span>

## <span data-ttu-id="19f3c-168">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19f3c-168">PARAMETERS</span></span>

### <span data-ttu-id="19f3c-169">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="19f3c-169">-ApplicationId</span></span>
<span data-ttu-id="19f3c-170">Do użytku w przyszłości.</span><span class="sxs-lookup"><span data-stu-id="19f3c-170">For future use.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: ByObjectId, InputObjectByObjectId, ResourceIdByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19f3c-171">-BypassObjectIdValidation</span><span class="sxs-lookup"><span data-stu-id="19f3c-171">-BypassObjectIdValidation</span></span>
<span data-ttu-id="19f3c-172">Umożliwia określenie identyfikatora obiektu bez sprawdzania, czy obiekt istnieje w usłudze Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="19f3c-172">Enables you to specify an object ID without validating that the object exists in Azure Active Directory.</span></span>
<span data-ttu-id="19f3c-173">Użyj tego parametru tylko wtedy, gdy chcesz udzielić dostępu do twojego magazynu kluczy identyfikatorowi obiektu, który odwołuje się do grupy zabezpieczeń delegowanych z innej dzierżawy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="19f3c-173">Use this parameter only if you want to grant access to your key vault to an object ID that refers to a delegated security group from another Azure tenant.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByObjectId, InputObjectByObjectId, ResourceIdByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19f3c-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19f3c-174">-DefaultProfile</span></span>
<span data-ttu-id="19f3c-175">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="19f3c-175">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="19f3c-176">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="19f3c-176">-EmailAddress</span></span>
<span data-ttu-id="19f3c-177">Określa adres e-mail użytkownika, któremu mają być udzielane uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="19f3c-177">Specifies the user email address of the user to whom to grant permissions.</span></span>
<span data-ttu-id="19f3c-178">Ten adres e-mail musi znajdować się w katalogu skojarzonym z bieżącą subskrypcją i być unikatowy.</span><span class="sxs-lookup"><span data-stu-id="19f3c-178">This email address must exist in the directory associated with the current subscription and be unique.</span></span>

```yaml
Type: System.String
Parameter Sets: ByEmailAddress, InputObjectByEmailAddress, ResourceIdByEmailAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19f3c-179">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="19f3c-179">-EnabledForDeployment</span></span>
<span data-ttu-id="19f3c-180">Umożliwia dostawcy zasobów Microsoft.Compute pobieranie sekretów z tego magazynu kluczy, gdy do tego magazynu kluczy odwołuje się podczas tworzenia zasobów, na przykład podczas tworzenia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="19f3c-180">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault, InputObjectForVault, ResourceIdForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19f3c-181">-EnabledForScriptEncryption</span><span class="sxs-lookup"><span data-stu-id="19f3c-181">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="19f3c-182">Umożliwia usłudze szyfrowania dysków Azure uzyskiwanie sekretów i odłącza klucze z tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="19f3c-182">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault, InputObjectForVault, ResourceIdForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19f3c-183">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="19f3c-183">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="19f3c-184">Umożliwia usłudze Azure Resource Manager uzyskiwanie sekretów z tego magazynu kluczy, gdy do tego magazynu kluczy odwołuje się we wdrożeniu szablonu.</span><span class="sxs-lookup"><span data-stu-id="19f3c-184">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault, InputObjectForVault, ResourceIdForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19f3c-185">-InputObject</span><span class="sxs-lookup"><span data-stu-id="19f3c-185">-InputObject</span></span>
<span data-ttu-id="19f3c-186">Obiekt magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="19f3c-186">Key Vault Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem
Parameter Sets: InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, InputObjectForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19f3c-187">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="19f3c-187">-ObjectId</span></span>
<span data-ttu-id="19f3c-188">Określa identyfikator obiektu użytkownika lub podmiotu zabezpieczeń usługi w usłudze Azure Active Directory, dla którego mają być udzielane uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="19f3c-188">Specifies the object ID of the user or service principal in Azure Active Directory for which to grant permissions.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectId, InputObjectByObjectId, ResourceIdByObjectId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19f3c-189">-PassThru</span><span class="sxs-lookup"><span data-stu-id="19f3c-189">-PassThru</span></span>
<span data-ttu-id="19f3c-190">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="19f3c-190">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="19f3c-191">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="19f3c-191">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="19f3c-192">-PermissionsToCertificates</span><span class="sxs-lookup"><span data-stu-id="19f3c-192">-PermissionsToCertificates</span></span>
<span data-ttu-id="19f3c-193">Określa tablicę uprawnień certyfikatu, które mają być udzielane użytkownikowi lub podmiotowi zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="19f3c-193">Specifies an array of certificate permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="19f3c-194">Dopuszczalne wartości dla tego parametru:</span><span class="sxs-lookup"><span data-stu-id="19f3c-194">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="19f3c-195">Pobierz</span><span class="sxs-lookup"><span data-stu-id="19f3c-195">Get</span></span>
- <span data-ttu-id="19f3c-196">Lista</span><span class="sxs-lookup"><span data-stu-id="19f3c-196">List</span></span>
- <span data-ttu-id="19f3c-197">Usuń</span><span class="sxs-lookup"><span data-stu-id="19f3c-197">Delete</span></span>
- <span data-ttu-id="19f3c-198">Tworzenie</span><span class="sxs-lookup"><span data-stu-id="19f3c-198">Create</span></span>
- <span data-ttu-id="19f3c-199">Importowanie</span><span class="sxs-lookup"><span data-stu-id="19f3c-199">Import</span></span>
- <span data-ttu-id="19f3c-200">Aktualizacja</span><span class="sxs-lookup"><span data-stu-id="19f3c-200">Update</span></span>
- <span data-ttu-id="19f3c-201">Managecontacts</span><span class="sxs-lookup"><span data-stu-id="19f3c-201">Managecontacts</span></span>
- <span data-ttu-id="19f3c-202">Getissuers</span><span class="sxs-lookup"><span data-stu-id="19f3c-202">Getissuers</span></span>
- <span data-ttu-id="19f3c-203">Listissuers</span><span class="sxs-lookup"><span data-stu-id="19f3c-203">Listissuers</span></span>
- <span data-ttu-id="19f3c-204">Setissuers</span><span class="sxs-lookup"><span data-stu-id="19f3c-204">Setissuers</span></span>
- <span data-ttu-id="19f3c-205">Deleteissuers</span><span class="sxs-lookup"><span data-stu-id="19f3c-205">Deleteissuers</span></span>
- <span data-ttu-id="19f3c-206">Zarządzanie usługami</span><span class="sxs-lookup"><span data-stu-id="19f3c-206">Manageissuers</span></span>
- <span data-ttu-id="19f3c-207">Odzyskaj</span><span class="sxs-lookup"><span data-stu-id="19f3c-207">Recover</span></span>
- <span data-ttu-id="19f3c-208">Kopia zapasowa</span><span class="sxs-lookup"><span data-stu-id="19f3c-208">Backup</span></span>
- <span data-ttu-id="19f3c-209">Przywróć</span><span class="sxs-lookup"><span data-stu-id="19f3c-209">Restore</span></span>
- <span data-ttu-id="19f3c-210">Przeczyszczanie</span><span class="sxs-lookup"><span data-stu-id="19f3c-210">Purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: get, list, delete, create, import, update, managecontacts, getissuers, listissuers, setissuers, deleteissuers, manageissuers, recover, purge, backup, restore

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19f3c-211">-PermissionsToKeys</span><span class="sxs-lookup"><span data-stu-id="19f3c-211">-PermissionsToKeys</span></span>
<span data-ttu-id="19f3c-212">Określa tablicę uprawnień do operacji klucza, które mają być udzielane użytkownikowi lub podmiotowi zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="19f3c-212">Specifies an array of key operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="19f3c-213">Dopuszczalne wartości dla tego parametru:</span><span class="sxs-lookup"><span data-stu-id="19f3c-213">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="19f3c-214">Odszyfrowywanie</span><span class="sxs-lookup"><span data-stu-id="19f3c-214">Decrypt</span></span>
- <span data-ttu-id="19f3c-215">Szyfruj</span><span class="sxs-lookup"><span data-stu-id="19f3c-215">Encrypt</span></span>
- <span data-ttu-id="19f3c-216">UnwrapKey</span><span class="sxs-lookup"><span data-stu-id="19f3c-216">UnwrapKey</span></span>
- <span data-ttu-id="19f3c-217">WrapKey</span><span class="sxs-lookup"><span data-stu-id="19f3c-217">WrapKey</span></span>
- <span data-ttu-id="19f3c-218">Weryfikuj</span><span class="sxs-lookup"><span data-stu-id="19f3c-218">Verify</span></span>
- <span data-ttu-id="19f3c-219">Podpisz</span><span class="sxs-lookup"><span data-stu-id="19f3c-219">Sign</span></span>
- <span data-ttu-id="19f3c-220">Pobierz</span><span class="sxs-lookup"><span data-stu-id="19f3c-220">Get</span></span>
- <span data-ttu-id="19f3c-221">Lista</span><span class="sxs-lookup"><span data-stu-id="19f3c-221">List</span></span>
- <span data-ttu-id="19f3c-222">Aktualizacja</span><span class="sxs-lookup"><span data-stu-id="19f3c-222">Update</span></span>
- <span data-ttu-id="19f3c-223">Tworzenie</span><span class="sxs-lookup"><span data-stu-id="19f3c-223">Create</span></span>
- <span data-ttu-id="19f3c-224">Importowanie</span><span class="sxs-lookup"><span data-stu-id="19f3c-224">Import</span></span>
- <span data-ttu-id="19f3c-225">Usuń</span><span class="sxs-lookup"><span data-stu-id="19f3c-225">Delete</span></span>
- <span data-ttu-id="19f3c-226">Kopia zapasowa</span><span class="sxs-lookup"><span data-stu-id="19f3c-226">Backup</span></span>
- <span data-ttu-id="19f3c-227">Przywróć</span><span class="sxs-lookup"><span data-stu-id="19f3c-227">Restore</span></span>
- <span data-ttu-id="19f3c-228">Odzyskaj</span><span class="sxs-lookup"><span data-stu-id="19f3c-228">Recover</span></span>
- <span data-ttu-id="19f3c-229">Przeczyszczanie</span><span class="sxs-lookup"><span data-stu-id="19f3c-229">Purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: decrypt, encrypt, unwrapKey, wrapKey, verify, sign, get, list, update, create, import, delete, backup, restore, recover, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19f3c-230">-PermissionsToSecrets</span><span class="sxs-lookup"><span data-stu-id="19f3c-230">-PermissionsToSecrets</span></span>
<span data-ttu-id="19f3c-231">Określa tablicę uprawnień do tajnych operacji, które należy przyznać użytkownikowi lub podmiotowi zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="19f3c-231">Specifies an array of secret operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="19f3c-232">Dopuszczalne wartości dla tego parametru:</span><span class="sxs-lookup"><span data-stu-id="19f3c-232">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="19f3c-233">Pobierz</span><span class="sxs-lookup"><span data-stu-id="19f3c-233">Get</span></span>
- <span data-ttu-id="19f3c-234">Lista</span><span class="sxs-lookup"><span data-stu-id="19f3c-234">List</span></span>
- <span data-ttu-id="19f3c-235">Ustaw</span><span class="sxs-lookup"><span data-stu-id="19f3c-235">Set</span></span>
- <span data-ttu-id="19f3c-236">Usuń</span><span class="sxs-lookup"><span data-stu-id="19f3c-236">Delete</span></span>
- <span data-ttu-id="19f3c-237">Kopia zapasowa</span><span class="sxs-lookup"><span data-stu-id="19f3c-237">Backup</span></span>
- <span data-ttu-id="19f3c-238">Przywróć</span><span class="sxs-lookup"><span data-stu-id="19f3c-238">Restore</span></span>
- <span data-ttu-id="19f3c-239">Odzyskaj</span><span class="sxs-lookup"><span data-stu-id="19f3c-239">Recover</span></span>
- <span data-ttu-id="19f3c-240">Przeczyszczanie</span><span class="sxs-lookup"><span data-stu-id="19f3c-240">Purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: get, list, set, delete, backup, restore, recover, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19f3c-241">-PermissionsToStorage</span><span class="sxs-lookup"><span data-stu-id="19f3c-241">-PermissionsToStorage</span></span>
<span data-ttu-id="19f3c-242">Określa uprawnienia do działania na koncie magazynu zarządzanego i operację SaS w celu udzielenia podmiotowi użytkownika lub podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="19f3c-242">Specifies managed storage account and SaS-definition operation permissions to grant to a user or service principal.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: get, list, delete, set, update, regeneratekey, getsas, listsas, deletesas, setsas, recover, backup, restore, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19f3c-243">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19f3c-243">-ResourceGroupName</span></span>
<span data-ttu-id="19f3c-244">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="19f3c-244">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, ForVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19f3c-245">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="19f3c-245">-ResourceId</span></span>
<span data-ttu-id="19f3c-246">Identyfikator zasobu magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="19f3c-246">Key Vault Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress, ResourceIdForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19f3c-247">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="19f3c-247">-ServicePrincipalName</span></span>
<span data-ttu-id="19f3c-248">Określa nazwę podmiotu zabezpieczeń usługi aplikacji, której uprawnienia mają być udzielane.</span><span class="sxs-lookup"><span data-stu-id="19f3c-248">Specifies the service principal name of the application to which to grant permissions.</span></span>
<span data-ttu-id="19f3c-249">Określ identyfikator aplikacji, nazywany również identyfikatorem klienta, zarejestrowany dla aplikacji w usłudze AzureActive Directory.</span><span class="sxs-lookup"><span data-stu-id="19f3c-249">Specify the application ID, also known as client ID, registered for the application in AzureActive Directory.</span></span> <span data-ttu-id="19f3c-250">Aplikacja o nazwie podmiotu zabezpieczeń usługi, która określa ten parametr, musi być zarejestrowana w usłudze Azure Directory zawierającej Bieżącą subskrypcję.</span><span class="sxs-lookup"><span data-stu-id="19f3c-250">The application with the service principal name that this parameter specifies must be registered in the Azure directory that contains your current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServicePrincipalName, InputObjectByServicePrincipalName, ResourceIdByServicePrincipalName
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19f3c-251">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="19f3c-251">-UserPrincipalName</span></span>
<span data-ttu-id="19f3c-252">Określa główną nazwę użytkownika, któremu mają być udzielane uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="19f3c-252">Specifies the user principal name of the user to whom to grant permissions.</span></span>
<span data-ttu-id="19f3c-253">Główna nazwa użytkownika musi istnieć w katalogu skojarzonym z bieżącą subskrypcją.</span><span class="sxs-lookup"><span data-stu-id="19f3c-253">This user principal name must exist in the directory associated with the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, InputObjectByUserPrincipalName, ResourceIdByUserPrincipalName
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19f3c-254">-VaultName</span><span class="sxs-lookup"><span data-stu-id="19f3c-254">-VaultName</span></span>
<span data-ttu-id="19f3c-255">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="19f3c-255">Specifies the name of a key vault.</span></span>
<span data-ttu-id="19f3c-256">To polecenie cmdlet modyfikuje zasady dostępu dla magazynu kluczy, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="19f3c-256">This cmdlet modifies the access policy for the key vault that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, ForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19f3c-257">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="19f3c-257">-Confirm</span></span>
<span data-ttu-id="19f3c-258">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="19f3c-258">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19f3c-259">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19f3c-259">-WhatIf</span></span>
<span data-ttu-id="19f3c-260">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19f3c-260">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="19f3c-261">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="19f3c-261">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19f3c-262">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19f3c-262">CommonParameters</span></span>
<span data-ttu-id="19f3c-263">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19f3c-263">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19f3c-264">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="19f3c-264">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19f3c-265">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="19f3c-265">INPUTS</span></span>

### <span data-ttu-id="19f3c-266">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="19f3c-266">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

### <span data-ttu-id="19f3c-267">System.String</span><span class="sxs-lookup"><span data-stu-id="19f3c-267">System.String</span></span>

## <span data-ttu-id="19f3c-268">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="19f3c-268">OUTPUTS</span></span>

### <span data-ttu-id="19f3c-269">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="19f3c-269">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="19f3c-270">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="19f3c-270">NOTES</span></span>

## <span data-ttu-id="19f3c-271">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="19f3c-271">RELATED LINKS</span></span>

[<span data-ttu-id="19f3c-272">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="19f3c-272">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="19f3c-273">Remove-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="19f3c-273">Remove-AzKeyVaultAccessPolicy</span></span>](./Remove-AzKeyVaultAccessPolicy.md)

