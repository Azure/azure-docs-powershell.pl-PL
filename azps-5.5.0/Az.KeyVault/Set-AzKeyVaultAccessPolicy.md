---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 636FAD5B-8C39-4E5C-8978-6845C6B89BC0
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
ms.openlocfilehash: eeaea44ec387dc7739a97b5026054186ff817ab3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185514"
---
# <span data-ttu-id="df60c-101">Set-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="df60c-101">Set-AzKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="df60c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df60c-102">SYNOPSIS</span></span>
<span data-ttu-id="df60c-103">Udziela lub modyfikuje istniejące uprawnienia użytkownika, aplikacji lub grupy zabezpieczeń do wykonywania operacji z magazynem kluczy.</span><span class="sxs-lookup"><span data-stu-id="df60c-103">Grants or modifies existing permissions for a user, application, or security group to perform operations with a key vault.</span></span>

## <span data-ttu-id="df60c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="df60c-104">SYNTAX</span></span>

### <span data-ttu-id="df60c-105">ByUserPrincipalName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="df60c-105">ByUserPrincipalName (Default)</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="df60c-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="df60c-106">ByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df60c-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="df60c-107">ByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="df60c-108">ByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="df60c-108">ByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="df60c-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="df60c-109">ForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df60c-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="df60c-110">InputObjectByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df60c-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="df60c-111">InputObjectByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="df60c-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="df60c-112">InputObjectByUserPrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="df60c-113">InputObjectByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="df60c-113">InputObjectByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="df60c-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="df60c-114">InputObjectForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df60c-115">ResourceIdByObjectId</span><span class="sxs-lookup"><span data-stu-id="df60c-115">ResourceIdByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df60c-116">ResourceIdByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="df60c-116">ResourceIdByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="df60c-117">ResourceIdByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="df60c-117">ResourceIdByUserPrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -UserPrincipalName <String> [-PermissionsToKeys <String[]>]
 [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df60c-118">ResourceIdByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="df60c-118">ResourceIdByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -EmailAddress <String> [-PermissionsToKeys <String[]>]
 [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df60c-119">ResourceIdForVault</span><span class="sxs-lookup"><span data-stu-id="df60c-119">ResourceIdForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> [-EnabledForDeployment] [-EnabledForTemplateDeployment]
 [-EnabledForDiskEncryption] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="df60c-120">OPIS</span><span class="sxs-lookup"><span data-stu-id="df60c-120">DESCRIPTION</span></span>
<span data-ttu-id="df60c-121">Polecenie **cmdlet Set-AzKeyVaultAccessPolicy** udziela lub modyfikuje istniejące uprawnienia użytkownika, aplikacji lub grupy zabezpieczeń do wykonywania określonych operacji za pomocą magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="df60c-121">The **Set-AzKeyVaultAccessPolicy** cmdlet grants or modifies existing permissions for a user, application, or security group to perform the specified operations with a key vault.</span></span> <span data-ttu-id="df60c-122">Nie modyfikuje uprawnień innych użytkowników, aplikacji ani grup zabezpieczeń w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="df60c-122">It does not modify the permissions that other users, applications, or security groups have on the key vault.</span></span>
<span data-ttu-id="df60c-123">Jeśli ustawiasz uprawnienia dla grupy zabezpieczeń, ta operacja dotyczy tylko użytkowników w tej grupie zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="df60c-123">If you are setting permissions for a security group, this operation affects only users in that security group.</span></span>
<span data-ttu-id="df60c-124">Wszystkie następujące katalogi muszą mieć ten sam katalog Azure:</span><span class="sxs-lookup"><span data-stu-id="df60c-124">The following directories must all be the same Azure directory:</span></span>
- <span data-ttu-id="df60c-125">Domyślny katalog subskrypcji platformy Azure, w którym znajduje się magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="df60c-125">The default directory of the Azure subscription in which the key vault resides.</span></span>
- <span data-ttu-id="df60c-126">Katalog Azure zawierający użytkownika lub grupę aplikacji, do których chcesz przyznać uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="df60c-126">The Azure directory that contains the user or application group that you are granting permissions to.</span></span>
<span data-ttu-id="df60c-127">Oto przykłady scenariuszy, w których te warunki nie są spełnione i to polecenie cmdlet nie będzie działać:</span><span class="sxs-lookup"><span data-stu-id="df60c-127">Examples of scenarios when these conditions are not met and this cmdlet will not work are:</span></span>
- <span data-ttu-id="df60c-128">Autoryzowanie użytkownika z innej organizacji w celu zarządzania Twoim magazynem kluczy.</span><span class="sxs-lookup"><span data-stu-id="df60c-128">Authorizing a user from a different organization to manage your key vault.</span></span>
<span data-ttu-id="df60c-129">Każda organizacja ma własny katalog.</span><span class="sxs-lookup"><span data-stu-id="df60c-129">Each organization has its own directory.</span></span>
- <span data-ttu-id="df60c-130">Twoje konto platformy Azure ma wiele katalogów.</span><span class="sxs-lookup"><span data-stu-id="df60c-130">Your Azure account has multiple directories.</span></span>
<span data-ttu-id="df60c-131">Jeśli zarejestrujesz aplikację w katalogu innym niż katalog domyślny, nie możesz autoryzować tej aplikacji do używania Twojego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="df60c-131">If you register an application in a directory other than the default directory, you cannot authorize that application to use your key vault.</span></span>
<span data-ttu-id="df60c-132">Aplikacja musi znajdować się w katalogu domyślnym.</span><span class="sxs-lookup"><span data-stu-id="df60c-132">The application must be in the default directory.</span></span>
<span data-ttu-id="df60c-133">Pamiętaj, że mimo że w przypadku tego polecenia cmdlet określenie grupy zasobów jest opcjonalne, należy to zrobić, aby uzyskać lepszą wydajność.</span><span class="sxs-lookup"><span data-stu-id="df60c-133">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

> [!NOTE]
> <span data-ttu-id="df60c-134">Podczas udzielania uprawnień zasad dostępu za pomocą podmiotu zabezpieczeń usługi należy użyć `-BypassObjectIdValidation` parametru.</span><span class="sxs-lookup"><span data-stu-id="df60c-134">When using a service principal to grant access policy permissions, you must use the `-BypassObjectIdValidation` parameter.</span></span>

## <span data-ttu-id="df60c-135">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="df60c-135">EXAMPLES</span></span>

### <span data-ttu-id="df60c-136">Przykład 1. Udzielanie użytkownikowi uprawnień do magazynu kluczy i modyfikowanie uprawnień</span><span class="sxs-lookup"><span data-stu-id="df60c-136">Example 1: Grant permissions to a user for a key vault and modify the permissions</span></span>
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

<span data-ttu-id="df60c-137">Pierwsze polecenie udziela użytkownikowi w usłudze Azure Active Directory uprawnień do wykonywania operacji na kluczach i sekretach magazynu kluczy o nazwie PattiFuller@contoso.com Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="df60c-137">The first command grants permissions for a user in your Azure Active Directory, PattiFuller@contoso.com, to perform operations on keys and secrets with a key vault named Contoso03Vault.</span></span> <span data-ttu-id="df60c-138">Parametr *PassThru* powoduje zwrócenie zaktualizowanego obiektu przez polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df60c-138">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>
<span data-ttu-id="df60c-139">Drugie polecenie modyfikuje uprawnienia, które zostały przyznane w pierwszym poleceniu, aby teraz zezwolić na uzyskiwanie sekretów oprócz ich ustawiania PattiFuller@contoso.com i usuwania.</span><span class="sxs-lookup"><span data-stu-id="df60c-139">The second command modifies the permissions that were granted to PattiFuller@contoso.com in the first command, to now allow getting secrets in addition to setting and deleting them.</span></span> <span data-ttu-id="df60c-140">Po tym poleceniu uprawnienia do operacji na kluczach pozostaną niezmienione.</span><span class="sxs-lookup"><span data-stu-id="df60c-140">The permissions to key operations remain unchanged after this command.</span></span>
<span data-ttu-id="df60c-141">Ostatnie polecenie dodatkowo zmodyfikuje istniejące uprawnienia do PattiFuller@contoso.com usuwania wszystkich uprawnień do kluczowych operacji.</span><span class="sxs-lookup"><span data-stu-id="df60c-141">The final command further modifies the existing permissions for PattiFuller@contoso.com to remove all permissions to key operations.</span></span> <span data-ttu-id="df60c-142">Po tym poleceniu uprawnienia do operacji tajnych pozostają niezmienione.</span><span class="sxs-lookup"><span data-stu-id="df60c-142">The permissions to secret operations remain unchanged after this command.</span></span>

### <span data-ttu-id="df60c-143">Przykład 2. Udzielanie uprawnień podmiotu zabezpieczeń usługi aplikacji do odczytu i zapisu sekretów</span><span class="sxs-lookup"><span data-stu-id="df60c-143">Example 2: Grant permissions for an application service principal to read and write secrets</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com' -PermissionsToSecrets Get,Set
```

<span data-ttu-id="df60c-144">To polecenie udziela uprawnień aplikacji dla magazynu kluczy o nazwie Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="df60c-144">This command grants permissions for an application for a key vault named Contoso03Vault.</span></span>
<span data-ttu-id="df60c-145">Parametr *ServicePrincipalName* określa aplikację.</span><span class="sxs-lookup"><span data-stu-id="df60c-145">The *ServicePrincipalName* parameter specifies the application.</span></span> <span data-ttu-id="df60c-146">Aplikacja musi być zarejestrowana w usłudze Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="df60c-146">The application must be registered in your Azure Active Directory.</span></span> <span data-ttu-id="df60c-147">Wartość parametru *ServicePrincipalName* musi być główną nazwą usługi aplikacji lub identyfikatorem GUID aplikacji.</span><span class="sxs-lookup"><span data-stu-id="df60c-147">The value of the *ServicePrincipalName* parameter must be either the service principal name of the application or the application ID GUID.</span></span>
<span data-ttu-id="df60c-148">W tym przykładzie określono nazwę podmiotu zabezpieczeń usługi, a polecenie udziela uprawnień aplikacji do `http://payroll.contoso.com` odczytu i zapisu sekretów.</span><span class="sxs-lookup"><span data-stu-id="df60c-148">This example specifies the service principal name `http://payroll.contoso.com`, and the command grants the application permissions to read and write secrets.</span></span>

### <span data-ttu-id="df60c-149">Przykład 3. Udzielanie uprawnień aplikacji przy użyciu identyfikatora obiektu</span><span class="sxs-lookup"><span data-stu-id="df60c-149">Example 3: Grant permissions for an application using its object ID</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectId 34595082-9346-41b6-8d6b-295a2808b8db -PermissionsToSecrets Get,Set
```

<span data-ttu-id="df60c-150">To polecenie udziela uprawnień aplikacji do odczytu i zapisu sekretów.</span><span class="sxs-lookup"><span data-stu-id="df60c-150">This command grants the application permissions to read and write secrets.</span></span>
<span data-ttu-id="df60c-151">W tym przykładzie określono aplikację, używając identyfikatora obiektu podmiotu zabezpieczeń usługi aplikacji.</span><span class="sxs-lookup"><span data-stu-id="df60c-151">This example specifies the application using the object ID of the service principal of the application.</span></span>

### <span data-ttu-id="df60c-152">Przykład 4. Udzielanie uprawnień do głównej nazwy użytkownika</span><span class="sxs-lookup"><span data-stu-id="df60c-152">Example 4: Grant permissions for a user principal name</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets Get,List,Set
```

<span data-ttu-id="df60c-153">To polecenie pozwala uzyskać, wyświetlić listę i ustawić uprawnienia dla określonej głównej nazwy użytkownika w celu uzyskania dostępu do tajemnic.</span><span class="sxs-lookup"><span data-stu-id="df60c-153">This command grants get, list, and set permissions for the specified user principal name for access to secrets.</span></span>

### <span data-ttu-id="df60c-154">Przykład 5. Włączanie pobierania sekretów z magazynu kluczy przez dostawcę zasobów Microsoft.Compute</span><span class="sxs-lookup"><span data-stu-id="df60c-154">Example 5: Enable secrets to be retrieved from a key vault by the Microsoft.Compute resource provider</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="df60c-155">To polecenie udziela uprawnień dla tajemnic pobierania z magazynu kluczy Contoso03Vault przez dostawcę zasobów Microsoft.Compute.</span><span class="sxs-lookup"><span data-stu-id="df60c-155">This command grants the permissions for secrets to be retrieved from the Contoso03Vault key vault by the Microsoft.Compute resource provider.</span></span>

### <span data-ttu-id="df60c-156">Przykład 6. Udzielanie uprawnień grupie zabezpieczeń</span><span class="sxs-lookup"><span data-stu-id="df60c-156">Example 6: Grant permissions to a security group</span></span>
```powershell
PS C:\> Get-AzADGroup
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'myownvault' -ObjectId (Get-AzADGroup -SearchString 'group2')[0].Id -PermissionsToKeys get, set -PermissionsToSecrets get, set
```

<span data-ttu-id="df60c-157">Pierwsze polecenie używa polecenia cmdlet Get-AzADGroup do uzyskania wszystkich grup usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="df60c-157">The first command uses the Get-AzADGroup cmdlet to get all Active Directory groups.</span></span> <span data-ttu-id="df60c-158">W wyniku widać 3 zwrócone grupy o nazwie **group1,** **group2** i **group3.**</span><span class="sxs-lookup"><span data-stu-id="df60c-158">From the output, you see 3 groups returned, named **group1**, **group2**, and **group3**.</span></span> <span data-ttu-id="df60c-159">Wiele grup może mieć tę samą nazwę, ale zawsze ma unikatowy identyfikator ObjectId.</span><span class="sxs-lookup"><span data-stu-id="df60c-159">Multiple groups can have the same name but always have a unique ObjectId.</span></span> <span data-ttu-id="df60c-160">Jeśli jest zwracana więcej niż jedna grupa o takiej samej nazwie, należy użyć w wynikach obiektu ObjectId, aby zidentyfikować tę, której chcesz użyć.</span><span class="sxs-lookup"><span data-stu-id="df60c-160">When more than one group that has the same name is returned, use the ObjectId in the output to identify the one you want to use.</span></span>
<span data-ttu-id="df60c-161">Następnie użyj danych wyjściowych tego polecenia z Set-AzKeyVaultAccessPolicy, aby udzielić uprawnień do grupy Group2 dla Twojego magazynu kluczy o **nazwie myownvault.**</span><span class="sxs-lookup"><span data-stu-id="df60c-161">You then use the output of this command with Set-AzKeyVaultAccessPolicy to grant permissions to group2 for your key vault, named **myownvault**.</span></span> <span data-ttu-id="df60c-162">W tym przykładzie wyliczane są grupy o nazwie "grupa2" w tym samym wierszu polecenia.</span><span class="sxs-lookup"><span data-stu-id="df60c-162">This example enumerates the groups named 'group2' inline in the same command line.</span></span>
<span data-ttu-id="df60c-163">Na liście zwróconej może być wiele grup o nazwie "grupa2".</span><span class="sxs-lookup"><span data-stu-id="df60c-163">There may be multiple groups in the returned list that are named 'group2'.</span></span>
<span data-ttu-id="df60c-164">W tym przykładzie wybierany jest pierwszy indeks \[ 0 \] na liście zwróconej.</span><span class="sxs-lookup"><span data-stu-id="df60c-164">This example picks the first one, indicated by index \[0\] in the returned list.</span></span>

### <span data-ttu-id="df60c-165">Przykład 7. Udzielanie usłudze Azure Information Protection dostępu do klucza dzierżawy zarządzanej przez klienta (BYOK)</span><span class="sxs-lookup"><span data-stu-id="df60c-165">Example 7: Grant Azure Information Protection access to the customer-managed tenant key (BYOK)</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso04Vault' -ServicePrincipalName 00000012-0000-0000-c000-000000000000 -PermissionsToKeys decrypt,sign,get
```

<span data-ttu-id="df60c-166">To polecenie autoryzuje usługę Azure Information Protection do używania klucza zarządzanego przez klienta (czyli klucza własnego, czyli scenariusza "BYOK") jako klucza dzierżawy usługi Azure Information Protection.</span><span class="sxs-lookup"><span data-stu-id="df60c-166">This command authorizes Azure Information Protection to use a customer-managed key (the bring your own key, or "BYOK" scenario) as the Azure Information Protection tenant key.</span></span>
<span data-ttu-id="df60c-167">Po uruchomieniu tego polecenia określ własną nazwę magazynu klucza, ale musisz określić parametr *ServicePrincipalName* z identyfikatorem GUID **00000012-0000-0000-c000-000000000000** i określić uprawnienia w przykładzie.</span><span class="sxs-lookup"><span data-stu-id="df60c-167">When you run this command, specify your own key vault name but you must specify the *ServicePrincipalName* parameter with the GUID **00000012-0000-0000-c000-000000000000** and specify the permissions in the example.</span></span>

## <span data-ttu-id="df60c-168">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="df60c-168">PARAMETERS</span></span>

### <span data-ttu-id="df60c-169">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="df60c-169">-ApplicationId</span></span>
<span data-ttu-id="df60c-170">Do użytku w przyszłości.</span><span class="sxs-lookup"><span data-stu-id="df60c-170">For future use.</span></span>

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

### <span data-ttu-id="df60c-171">-BypassObjectIdValidation</span><span class="sxs-lookup"><span data-stu-id="df60c-171">-BypassObjectIdValidation</span></span>
<span data-ttu-id="df60c-172">Umożliwia określenie identyfikatora obiektu bez sprawdzania, czy obiekt istnieje w usłudze Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="df60c-172">Enables you to specify an object ID without validating that the object exists in Azure Active Directory.</span></span>
<span data-ttu-id="df60c-173">Użyj tego parametru tylko wtedy, gdy chcesz udzielić dostępu do magazynu kluczy identyfikatorowi obiektu, który odwołuje się do grupy zabezpieczeń delegowanych z innej dzierżawy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="df60c-173">Use this parameter only if you want to grant access to your key vault to an object ID that refers to a delegated security group from another Azure tenant.</span></span>

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

### <span data-ttu-id="df60c-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df60c-174">-DefaultProfile</span></span>
<span data-ttu-id="df60c-175">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="df60c-175">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="df60c-176">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="df60c-176">-EmailAddress</span></span>
<span data-ttu-id="df60c-177">Określa adres e-mail użytkownika, któremu mają być udzielane uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="df60c-177">Specifies the user email address of the user to whom to grant permissions.</span></span>
<span data-ttu-id="df60c-178">Ten adres e-mail musi znajdować się w katalogu skojarzonym z bieżącą subskrypcją i być unikatowy.</span><span class="sxs-lookup"><span data-stu-id="df60c-178">This email address must exist in the directory associated with the current subscription and be unique.</span></span>

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

### <span data-ttu-id="df60c-179">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="df60c-179">-EnabledForDeployment</span></span>
<span data-ttu-id="df60c-180">Umożliwia dostawcy zasobów Microsoft.Compute pobieranie sekretów z tego magazynu kluczy, gdy do tego magazynu kluczy odwołuje się podczas tworzenia zasobów, na przykład podczas tworzenia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="df60c-180">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

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

### <span data-ttu-id="df60c-181">-EnabledForScriptEncryption</span><span class="sxs-lookup"><span data-stu-id="df60c-181">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="df60c-182">Umożliwia usłudze szyfrowania dysków Platformy Azure uzyskiwanie sekretów i odłącza klucze z tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="df60c-182">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

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

### <span data-ttu-id="df60c-183">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="df60c-183">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="df60c-184">Umożliwia usłudze Azure Resource Manager uzyskiwanie sekretów z tego magazynu kluczy, gdy do tego magazynu kluczy odwołuje się we wdrożeniu szablonu.</span><span class="sxs-lookup"><span data-stu-id="df60c-184">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

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

### <span data-ttu-id="df60c-185">-InputObject</span><span class="sxs-lookup"><span data-stu-id="df60c-185">-InputObject</span></span>
<span data-ttu-id="df60c-186">Obiekt magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="df60c-186">Key Vault Object</span></span>

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

### <span data-ttu-id="df60c-187">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="df60c-187">-ObjectId</span></span>
<span data-ttu-id="df60c-188">Określa identyfikator obiektu użytkownika lub podmiotu zabezpieczeń usługi w usłudze Azure Active Directory, dla którego mają być udzielane uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="df60c-188">Specifies the object ID of the user or service principal in Azure Active Directory for which to grant permissions.</span></span>

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

### <span data-ttu-id="df60c-189">-PassThru</span><span class="sxs-lookup"><span data-stu-id="df60c-189">-PassThru</span></span>
<span data-ttu-id="df60c-190">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="df60c-190">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="df60c-191">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="df60c-191">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="df60c-192">-PermissionsToCertificates</span><span class="sxs-lookup"><span data-stu-id="df60c-192">-PermissionsToCertificates</span></span>
<span data-ttu-id="df60c-193">Określa tablicę uprawnień certyfikatu, które mają być udzielane użytkownikowi lub podmiotowi zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="df60c-193">Specifies an array of certificate permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="df60c-194">Dopuszczalne wartości dla tego parametru:</span><span class="sxs-lookup"><span data-stu-id="df60c-194">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="df60c-195">Wszystkie</span><span class="sxs-lookup"><span data-stu-id="df60c-195">All</span></span>
- <span data-ttu-id="df60c-196">Pobierz</span><span class="sxs-lookup"><span data-stu-id="df60c-196">Get</span></span>
- <span data-ttu-id="df60c-197">Lista</span><span class="sxs-lookup"><span data-stu-id="df60c-197">List</span></span>
- <span data-ttu-id="df60c-198">Usuń</span><span class="sxs-lookup"><span data-stu-id="df60c-198">Delete</span></span>
- <span data-ttu-id="df60c-199">Tworzenie</span><span class="sxs-lookup"><span data-stu-id="df60c-199">Create</span></span>
- <span data-ttu-id="df60c-200">Importowanie</span><span class="sxs-lookup"><span data-stu-id="df60c-200">Import</span></span>
- <span data-ttu-id="df60c-201">Aktualizacja</span><span class="sxs-lookup"><span data-stu-id="df60c-201">Update</span></span>
- <span data-ttu-id="df60c-202">Managecontacts</span><span class="sxs-lookup"><span data-stu-id="df60c-202">Managecontacts</span></span>
- <span data-ttu-id="df60c-203">Getissuers</span><span class="sxs-lookup"><span data-stu-id="df60c-203">Getissuers</span></span>
- <span data-ttu-id="df60c-204">Listissuers</span><span class="sxs-lookup"><span data-stu-id="df60c-204">Listissuers</span></span>
- <span data-ttu-id="df60c-205">Setissuers</span><span class="sxs-lookup"><span data-stu-id="df60c-205">Setissuers</span></span>
- <span data-ttu-id="df60c-206">Deleteissuers</span><span class="sxs-lookup"><span data-stu-id="df60c-206">Deleteissuers</span></span>
- <span data-ttu-id="df60c-207">Zarządzanie usługami</span><span class="sxs-lookup"><span data-stu-id="df60c-207">Manageissuers</span></span>
- <span data-ttu-id="df60c-208">Odzyskaj</span><span class="sxs-lookup"><span data-stu-id="df60c-208">Recover</span></span>
- <span data-ttu-id="df60c-209">Kopia zapasowa</span><span class="sxs-lookup"><span data-stu-id="df60c-209">Backup</span></span>
- <span data-ttu-id="df60c-210">Przywróć</span><span class="sxs-lookup"><span data-stu-id="df60c-210">Restore</span></span>
- <span data-ttu-id="df60c-211">Przeczyszczanie</span><span class="sxs-lookup"><span data-stu-id="df60c-211">Purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: all, get, list, delete, create, import, update, managecontacts, getissuers, listissuers, setissuers, deleteissuers, manageissuers, recover, purge, backup, restore

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df60c-212">-PermissionsToKeys</span><span class="sxs-lookup"><span data-stu-id="df60c-212">-PermissionsToKeys</span></span>
<span data-ttu-id="df60c-213">Określa tablicę uprawnień do obsługi kluczy, które mają być udzielane użytkownikowi lub podmiotowi zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="df60c-213">Specifies an array of key operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="df60c-214">Dopuszczalne wartości dla tego parametru:</span><span class="sxs-lookup"><span data-stu-id="df60c-214">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="df60c-215">Wszystkie</span><span class="sxs-lookup"><span data-stu-id="df60c-215">All</span></span>
- <span data-ttu-id="df60c-216">Odszyfrowywanie</span><span class="sxs-lookup"><span data-stu-id="df60c-216">Decrypt</span></span>
- <span data-ttu-id="df60c-217">Szyfrowanie</span><span class="sxs-lookup"><span data-stu-id="df60c-217">Encrypt</span></span>
- <span data-ttu-id="df60c-218">UnwrapKey</span><span class="sxs-lookup"><span data-stu-id="df60c-218">UnwrapKey</span></span>
- <span data-ttu-id="df60c-219">WrapKey</span><span class="sxs-lookup"><span data-stu-id="df60c-219">WrapKey</span></span>
- <span data-ttu-id="df60c-220">Weryfikuj</span><span class="sxs-lookup"><span data-stu-id="df60c-220">Verify</span></span>
- <span data-ttu-id="df60c-221">Podpisz</span><span class="sxs-lookup"><span data-stu-id="df60c-221">Sign</span></span>
- <span data-ttu-id="df60c-222">Pobierz</span><span class="sxs-lookup"><span data-stu-id="df60c-222">Get</span></span>
- <span data-ttu-id="df60c-223">Lista</span><span class="sxs-lookup"><span data-stu-id="df60c-223">List</span></span>
- <span data-ttu-id="df60c-224">Aktualizacja</span><span class="sxs-lookup"><span data-stu-id="df60c-224">Update</span></span>
- <span data-ttu-id="df60c-225">Tworzenie</span><span class="sxs-lookup"><span data-stu-id="df60c-225">Create</span></span>
- <span data-ttu-id="df60c-226">Importowanie</span><span class="sxs-lookup"><span data-stu-id="df60c-226">Import</span></span>
- <span data-ttu-id="df60c-227">Usuń</span><span class="sxs-lookup"><span data-stu-id="df60c-227">Delete</span></span>
- <span data-ttu-id="df60c-228">Kopia zapasowa</span><span class="sxs-lookup"><span data-stu-id="df60c-228">Backup</span></span>
- <span data-ttu-id="df60c-229">Przywróć</span><span class="sxs-lookup"><span data-stu-id="df60c-229">Restore</span></span>
- <span data-ttu-id="df60c-230">Odzyskaj</span><span class="sxs-lookup"><span data-stu-id="df60c-230">Recover</span></span>
- <span data-ttu-id="df60c-231">Przeczyszczanie</span><span class="sxs-lookup"><span data-stu-id="df60c-231">Purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: all, decrypt, encrypt, unwrapKey, wrapKey, verify, sign, get, list, update, create, import, delete, backup, restore, recover, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df60c-232">-PermissionsToSecrets</span><span class="sxs-lookup"><span data-stu-id="df60c-232">-PermissionsToSecrets</span></span>
<span data-ttu-id="df60c-233">Określa tablicę uprawnień operacji tajnych do udzielania użytkownikowi lub podmiotowi zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="df60c-233">Specifies an array of secret operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="df60c-234">Dopuszczalne wartości dla tego parametru:</span><span class="sxs-lookup"><span data-stu-id="df60c-234">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="df60c-235">Wszystkie</span><span class="sxs-lookup"><span data-stu-id="df60c-235">All</span></span>
- <span data-ttu-id="df60c-236">Pobierz</span><span class="sxs-lookup"><span data-stu-id="df60c-236">Get</span></span>
- <span data-ttu-id="df60c-237">Lista</span><span class="sxs-lookup"><span data-stu-id="df60c-237">List</span></span>
- <span data-ttu-id="df60c-238">Ustaw</span><span class="sxs-lookup"><span data-stu-id="df60c-238">Set</span></span>
- <span data-ttu-id="df60c-239">Usuń</span><span class="sxs-lookup"><span data-stu-id="df60c-239">Delete</span></span>
- <span data-ttu-id="df60c-240">Kopia zapasowa</span><span class="sxs-lookup"><span data-stu-id="df60c-240">Backup</span></span>
- <span data-ttu-id="df60c-241">Przywróć</span><span class="sxs-lookup"><span data-stu-id="df60c-241">Restore</span></span>
- <span data-ttu-id="df60c-242">Odzyskaj</span><span class="sxs-lookup"><span data-stu-id="df60c-242">Recover</span></span>
- <span data-ttu-id="df60c-243">Przeczyszczanie</span><span class="sxs-lookup"><span data-stu-id="df60c-243">Purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: all, get, list, set, delete, backup, restore, recover, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df60c-244">-PermissionsToStorage</span><span class="sxs-lookup"><span data-stu-id="df60c-244">-PermissionsToStorage</span></span>
<span data-ttu-id="df60c-245">Określa uprawnienia do działania na koncie magazynu zarządzanego i operację SaS w celu udzielenia podmiotowi użytkownika lub podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="df60c-245">Specifies managed storage account and SaS-definition operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="df60c-246">Dopuszczalne wartości dla tego parametru:</span><span class="sxs-lookup"><span data-stu-id="df60c-246">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="df60c-247">wszystko</span><span class="sxs-lookup"><span data-stu-id="df60c-247">all</span></span>
- <span data-ttu-id="df60c-248">Pobierz</span><span class="sxs-lookup"><span data-stu-id="df60c-248">get</span></span>
- <span data-ttu-id="df60c-249">lista</span><span class="sxs-lookup"><span data-stu-id="df60c-249">list</span></span>
- <span data-ttu-id="df60c-250">usuń</span><span class="sxs-lookup"><span data-stu-id="df60c-250">delete</span></span>
- <span data-ttu-id="df60c-251">ustaw</span><span class="sxs-lookup"><span data-stu-id="df60c-251">set</span></span>
- <span data-ttu-id="df60c-252">aktualizacja</span><span class="sxs-lookup"><span data-stu-id="df60c-252">update</span></span>
- <span data-ttu-id="df60c-253">generuj klucz ponownie</span><span class="sxs-lookup"><span data-stu-id="df60c-253">regeneratekey</span></span>
- <span data-ttu-id="df60c-254">getsas</span><span class="sxs-lookup"><span data-stu-id="df60c-254">getsas</span></span>
- <span data-ttu-id="df60c-255">listsas</span><span class="sxs-lookup"><span data-stu-id="df60c-255">listsas</span></span>
- <span data-ttu-id="df60c-256">deletesas</span><span class="sxs-lookup"><span data-stu-id="df60c-256">deletesas</span></span>
- <span data-ttu-id="df60c-257">setsas</span><span class="sxs-lookup"><span data-stu-id="df60c-257">setsas</span></span>
- <span data-ttu-id="df60c-258">odzyskiwanie</span><span class="sxs-lookup"><span data-stu-id="df60c-258">recover</span></span>
- <span data-ttu-id="df60c-259">kopia zapasowa</span><span class="sxs-lookup"><span data-stu-id="df60c-259">backup</span></span>
- <span data-ttu-id="df60c-260">przywracanie</span><span class="sxs-lookup"><span data-stu-id="df60c-260">restore</span></span>
- <span data-ttu-id="df60c-261">przeczyszczanie</span><span class="sxs-lookup"><span data-stu-id="df60c-261">purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: all, get, list, delete, set, update, regeneratekey, getsas, listsas, deletesas, setsas, recover, backup, restore, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df60c-262">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df60c-262">-ResourceGroupName</span></span>
<span data-ttu-id="df60c-263">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="df60c-263">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="df60c-264">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="df60c-264">-ResourceId</span></span>
<span data-ttu-id="df60c-265">Identyfikator zasobu magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="df60c-265">Key Vault Resource Id</span></span>

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

### <span data-ttu-id="df60c-266">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="df60c-266">-ServicePrincipalName</span></span>
<span data-ttu-id="df60c-267">Określa nazwę podmiotu zabezpieczeń usługi aplikacji, której uprawnienia mają być udzielane.</span><span class="sxs-lookup"><span data-stu-id="df60c-267">Specifies the service principal name of the application to which to grant permissions.</span></span>
<span data-ttu-id="df60c-268">Określ identyfikator aplikacji, nazywany również identyfikatorem klienta, zarejestrowany dla aplikacji w usłudze AzureActive Directory.</span><span class="sxs-lookup"><span data-stu-id="df60c-268">Specify the application ID, also known as client ID, registered for the application in AzureActive Directory.</span></span> <span data-ttu-id="df60c-269">Aplikacja o nazwie podmiotu zabezpieczeń usługi, która określa ten parametr, musi być zarejestrowana w usłudze Azure Directory zawierającej Bieżącą subskrypcję.</span><span class="sxs-lookup"><span data-stu-id="df60c-269">The application with the service principal name that this parameter specifies must be registered in the Azure directory that contains your current subscription.</span></span>

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

### <span data-ttu-id="df60c-270">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="df60c-270">-UserPrincipalName</span></span>
<span data-ttu-id="df60c-271">Określa główną nazwę użytkownika, któremu mają być udzielane uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="df60c-271">Specifies the user principal name of the user to whom to grant permissions.</span></span>
<span data-ttu-id="df60c-272">Główna nazwa użytkownika musi istnieć w katalogu skojarzonym z bieżącą subskrypcją.</span><span class="sxs-lookup"><span data-stu-id="df60c-272">This user principal name must exist in the directory associated with the current subscription.</span></span>

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

### <span data-ttu-id="df60c-273">-VaultName</span><span class="sxs-lookup"><span data-stu-id="df60c-273">-VaultName</span></span>
<span data-ttu-id="df60c-274">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="df60c-274">Specifies the name of a key vault.</span></span>
<span data-ttu-id="df60c-275">To polecenie cmdlet modyfikuje zasady dostępu dla magazynu kluczy, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="df60c-275">This cmdlet modifies the access policy for the key vault that this parameter specifies.</span></span>

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

### <span data-ttu-id="df60c-276">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="df60c-276">-Confirm</span></span>
<span data-ttu-id="df60c-277">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="df60c-277">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df60c-278">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df60c-278">-WhatIf</span></span>
<span data-ttu-id="df60c-279">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df60c-279">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="df60c-280">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="df60c-280">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df60c-281">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df60c-281">CommonParameters</span></span>
<span data-ttu-id="df60c-282">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df60c-282">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df60c-283">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="df60c-283">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df60c-284">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="df60c-284">INPUTS</span></span>

### <span data-ttu-id="df60c-285">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="df60c-285">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

### <span data-ttu-id="df60c-286">System.String</span><span class="sxs-lookup"><span data-stu-id="df60c-286">System.String</span></span>

## <span data-ttu-id="df60c-287">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="df60c-287">OUTPUTS</span></span>

### <span data-ttu-id="df60c-288">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="df60c-288">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="df60c-289">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="df60c-289">NOTES</span></span>

## <span data-ttu-id="df60c-290">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="df60c-290">RELATED LINKS</span></span>

[<span data-ttu-id="df60c-291">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="df60c-291">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="df60c-292">Remove-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="df60c-292">Remove-AzKeyVaultAccessPolicy</span></span>](./Remove-AzKeyVaultAccessPolicy.md)

