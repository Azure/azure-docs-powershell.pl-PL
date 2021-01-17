---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 636FAD5B-8C39-4E5C-8978-6845C6B89BC0
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
ms.openlocfilehash: eeaea44ec387dc7739a97b5026054186ff817ab3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360815"
---
# <span data-ttu-id="f13ed-101">Set-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f13ed-101">Set-AzKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="f13ed-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f13ed-102">SYNOPSIS</span></span>
<span data-ttu-id="f13ed-103">Udziela lub modyfikuje istniejące uprawnienia dla użytkownika, aplikacji lub grupy zabezpieczeń w celu wykonania operacji za pomocą magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="f13ed-103">Grants or modifies existing permissions for a user, application, or security group to perform operations with a key vault.</span></span>

## <span data-ttu-id="f13ed-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f13ed-104">SYNTAX</span></span>

### <span data-ttu-id="f13ed-105">ByUserPrincipalName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f13ed-105">ByUserPrincipalName (Default)</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f13ed-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="f13ed-106">ByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f13ed-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="f13ed-107">ByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f13ed-108">ByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="f13ed-108">ByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f13ed-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="f13ed-109">ForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f13ed-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="f13ed-110">InputObjectByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f13ed-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="f13ed-111">InputObjectByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f13ed-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="f13ed-112">InputObjectByUserPrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f13ed-113">InputObjectByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="f13ed-113">InputObjectByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f13ed-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="f13ed-114">InputObjectForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f13ed-115">ResourceIdByObjectId</span><span class="sxs-lookup"><span data-stu-id="f13ed-115">ResourceIdByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f13ed-116">ResourceIdByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="f13ed-116">ResourceIdByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f13ed-117">ResourceIdByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="f13ed-117">ResourceIdByUserPrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -UserPrincipalName <String> [-PermissionsToKeys <String[]>]
 [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f13ed-118">ResourceIdByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="f13ed-118">ResourceIdByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -EmailAddress <String> [-PermissionsToKeys <String[]>]
 [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f13ed-119">ResourceIdForVault</span><span class="sxs-lookup"><span data-stu-id="f13ed-119">ResourceIdForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> [-EnabledForDeployment] [-EnabledForTemplateDeployment]
 [-EnabledForDiskEncryption] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f13ed-120">Opis</span><span class="sxs-lookup"><span data-stu-id="f13ed-120">DESCRIPTION</span></span>
<span data-ttu-id="f13ed-121">Polecenie cmdlet **Set-AzKeyVaultAccessPolicy** udziela lub modyfikuje istniejące uprawnienia dla użytkownika, aplikacji lub grupy zabezpieczeń w celu wykonania określonych operacji w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="f13ed-121">The **Set-AzKeyVaultAccessPolicy** cmdlet grants or modifies existing permissions for a user, application, or security group to perform the specified operations with a key vault.</span></span> <span data-ttu-id="f13ed-122">W magazynie kluczy nie są modyfikowane uprawnienia innych użytkowników, aplikacji ani grup zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="f13ed-122">It does not modify the permissions that other users, applications, or security groups have on the key vault.</span></span>
<span data-ttu-id="f13ed-123">Jeśli ustawiasz uprawnienia dla grupy zabezpieczeń, ta operacja będzie miała wpływ tylko na użytkowników tej grupy zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="f13ed-123">If you are setting permissions for a security group, this operation affects only users in that security group.</span></span>
<span data-ttu-id="f13ed-124">Wszystkie następujące katalogi muszą być tego samego katalogu platformy Azure:</span><span class="sxs-lookup"><span data-stu-id="f13ed-124">The following directories must all be the same Azure directory:</span></span>
- <span data-ttu-id="f13ed-125">Katalog domyślny subskrypcji platformy Azure, w której znajduje się magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="f13ed-125">The default directory of the Azure subscription in which the key vault resides.</span></span>
- <span data-ttu-id="f13ed-126">Katalog platformy Azure zawierający użytkownika lub grupę aplikacji, do których udzielasz uprawnień.</span><span class="sxs-lookup"><span data-stu-id="f13ed-126">The Azure directory that contains the user or application group that you are granting permissions to.</span></span>
<span data-ttu-id="f13ed-127">Przykłady scenariuszy, w których te warunki nie są spełnione, a to polecenie cmdlet nie będzie działać:</span><span class="sxs-lookup"><span data-stu-id="f13ed-127">Examples of scenarios when these conditions are not met and this cmdlet will not work are:</span></span>
- <span data-ttu-id="f13ed-128">Autoryzowanie użytkownika od innej organizacji do zarządzania magazynem kluczy.</span><span class="sxs-lookup"><span data-stu-id="f13ed-128">Authorizing a user from a different organization to manage your key vault.</span></span>
<span data-ttu-id="f13ed-129">Każda organizacja ma swój własny katalog.</span><span class="sxs-lookup"><span data-stu-id="f13ed-129">Each organization has its own directory.</span></span>
- <span data-ttu-id="f13ed-130">Twoje konto platformy Azure ma wiele katalogów.</span><span class="sxs-lookup"><span data-stu-id="f13ed-130">Your Azure account has multiple directories.</span></span>
<span data-ttu-id="f13ed-131">Jeśli zarejestrujesz aplikację w katalogu innym niż katalog domyślny, nie możesz autoryzować tej aplikacji do korzystania z Twojego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="f13ed-131">If you register an application in a directory other than the default directory, you cannot authorize that application to use your key vault.</span></span>
<span data-ttu-id="f13ed-132">Aplikacja musi znajdować się w katalogu domyślnym.</span><span class="sxs-lookup"><span data-stu-id="f13ed-132">The application must be in the default directory.</span></span>
<span data-ttu-id="f13ed-133">Uwaga: chociaż określenie grupy zasobów jest opcjonalne dla tego polecenia cmdlet, należy to zrobić w celu uzyskania lepszej wydajności.</span><span class="sxs-lookup"><span data-stu-id="f13ed-133">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

> [!NOTE]
> <span data-ttu-id="f13ed-134">Używając podmiotu zabezpieczeń usługi do udzielania uprawnień zasad dostępu, należy użyć `-BypassObjectIdValidation` parametru.</span><span class="sxs-lookup"><span data-stu-id="f13ed-134">When using a service principal to grant access policy permissions, you must use the `-BypassObjectIdValidation` parameter.</span></span>

## <span data-ttu-id="f13ed-135">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f13ed-135">EXAMPLES</span></span>

### <span data-ttu-id="f13ed-136">Przykład 1: udzielanie uprawnień użytkownikowi dla magazynu kluczy i modyfikowanie uprawnień</span><span class="sxs-lookup"><span data-stu-id="f13ed-136">Example 1: Grant permissions to a user for a key vault and modify the permissions</span></span>
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

<span data-ttu-id="f13ed-137">Pierwsze polecenie udziela uprawnień użytkownikowi w usłudze Azure Active Directory, PattiFuller@contoso.com Aby wykonywać operacje na kluczach i kluczach tajnych przy użyciu magazynu kluczy o nazwie Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="f13ed-137">The first command grants permissions for a user in your Azure Active Directory, PattiFuller@contoso.com, to perform operations on keys and secrets with a key vault named Contoso03Vault.</span></span> <span data-ttu-id="f13ed-138">Parametr *PassThru* powoduje, że zaktualizowany obiekt jest zwracany przez polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f13ed-138">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>
<span data-ttu-id="f13ed-139">Drugie polecenie modyfikuje uprawnienia udzielone PattiFuller@contoso.com w pierwszym poleceniu w celu umożliwienia natychmiastowego wprowadzenia kluczy tajnych oraz ich usunięcia.</span><span class="sxs-lookup"><span data-stu-id="f13ed-139">The second command modifies the permissions that were granted to PattiFuller@contoso.com in the first command, to now allow getting secrets in addition to setting and deleting them.</span></span> <span data-ttu-id="f13ed-140">Uprawnienia do kluczowych operacji pozostają niezmienione po wykonaniu tego polecenia.</span><span class="sxs-lookup"><span data-stu-id="f13ed-140">The permissions to key operations remain unchanged after this command.</span></span>
<span data-ttu-id="f13ed-141">Polecenie ostatnie modyfikuje istniejące uprawnienia w PattiFuller@contoso.com celu usunięcia wszystkich uprawnień do kluczowych operacji.</span><span class="sxs-lookup"><span data-stu-id="f13ed-141">The final command further modifies the existing permissions for PattiFuller@contoso.com to remove all permissions to key operations.</span></span> <span data-ttu-id="f13ed-142">Po wykonaniu tego polecenia uprawnienia do tajnych operacji pozostają niezmienione.</span><span class="sxs-lookup"><span data-stu-id="f13ed-142">The permissions to secret operations remain unchanged after this command.</span></span>

### <span data-ttu-id="f13ed-143">Przykład 2: udzielanie uprawnień głównemu usłudze aplikacji w celu odczytywania i zapisywania kluczy tajnych</span><span class="sxs-lookup"><span data-stu-id="f13ed-143">Example 2: Grant permissions for an application service principal to read and write secrets</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com' -PermissionsToSecrets Get,Set
```

<span data-ttu-id="f13ed-144">To polecenie udziela uprawnień do aplikacji dla magazynu kluczy o nazwie Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="f13ed-144">This command grants permissions for an application for a key vault named Contoso03Vault.</span></span>
<span data-ttu-id="f13ed-145">Parametr *ServicePrincipalName* określa aplikację.</span><span class="sxs-lookup"><span data-stu-id="f13ed-145">The *ServicePrincipalName* parameter specifies the application.</span></span> <span data-ttu-id="f13ed-146">Aplikacja musi być zarejestrowana w usłudze Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f13ed-146">The application must be registered in your Azure Active Directory.</span></span> <span data-ttu-id="f13ed-147">Wartość parametru *ServicePrincipalName* musi być nazwą główną usługi aplikacji lub identyfikatorem GUID identyfikatora aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f13ed-147">The value of the *ServicePrincipalName* parameter must be either the service principal name of the application or the application ID GUID.</span></span>
<span data-ttu-id="f13ed-148">W tym przykładzie określono nazwę główną usługi `http://payroll.contoso.com` , a polecenie przyznaje uprawnienia aplikacji do odczytu i zapisu kluczy tajnych.</span><span class="sxs-lookup"><span data-stu-id="f13ed-148">This example specifies the service principal name `http://payroll.contoso.com`, and the command grants the application permissions to read and write secrets.</span></span>

### <span data-ttu-id="f13ed-149">Przykład 3: udzielanie uprawnień do aplikacji przy użyciu jej identyfikatora obiektu</span><span class="sxs-lookup"><span data-stu-id="f13ed-149">Example 3: Grant permissions for an application using its object ID</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectId 34595082-9346-41b6-8d6b-295a2808b8db -PermissionsToSecrets Get,Set
```

<span data-ttu-id="f13ed-150">To polecenie udziela uprawnień aplikacji do odczytu i zapisu kluczy tajnych.</span><span class="sxs-lookup"><span data-stu-id="f13ed-150">This command grants the application permissions to read and write secrets.</span></span>
<span data-ttu-id="f13ed-151">W tym przykładzie określono aplikację przy użyciu identyfikatora obiektu głównego usługi aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f13ed-151">This example specifies the application using the object ID of the service principal of the application.</span></span>

### <span data-ttu-id="f13ed-152">Przykład 4: udzielanie uprawnień dla głównej nazwy użytkownika</span><span class="sxs-lookup"><span data-stu-id="f13ed-152">Example 4: Grant permissions for a user principal name</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets Get,List,Set
```

<span data-ttu-id="f13ed-153">To polecenie udziela uprawnień Get, list i ustawia uprawnienia dla określonej nazwy głównej użytkownika w celu uzyskania dostępu do kluczy tajnych.</span><span class="sxs-lookup"><span data-stu-id="f13ed-153">This command grants get, list, and set permissions for the specified user principal name for access to secrets.</span></span>

### <span data-ttu-id="f13ed-154">Przykład 5: Włączanie kluczy tajnych do pobrania z magazynu kluczy przez firmę Microsoft. Oblicz dostawcę zasobów</span><span class="sxs-lookup"><span data-stu-id="f13ed-154">Example 5: Enable secrets to be retrieved from a key vault by the Microsoft.Compute resource provider</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="f13ed-155">To polecenie udziela uprawnień do pobierania kluczy tajnych z magazynu kluczy Contoso03Vault przez dostawcę Microsoft. COMPUTE Resource.</span><span class="sxs-lookup"><span data-stu-id="f13ed-155">This command grants the permissions for secrets to be retrieved from the Contoso03Vault key vault by the Microsoft.Compute resource provider.</span></span>

### <span data-ttu-id="f13ed-156">Przykład 6: udzielanie uprawnień grupie zabezpieczeń</span><span class="sxs-lookup"><span data-stu-id="f13ed-156">Example 6: Grant permissions to a security group</span></span>
```powershell
PS C:\> Get-AzADGroup
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'myownvault' -ObjectId (Get-AzADGroup -SearchString 'group2')[0].Id -PermissionsToKeys get, set -PermissionsToSecrets get, set
```

<span data-ttu-id="f13ed-157">W pierwszym poleceniu jest używane polecenie cmdlet Get-AzADGroup, aby uzyskać dostęp do wszystkich grup usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f13ed-157">The first command uses the Get-AzADGroup cmdlet to get all Active Directory groups.</span></span> <span data-ttu-id="f13ed-158">Na podstawie wyników są wyświetlane 3 grupy zwrócone, nazwane **grupa1**, **group2** oraz **Group3**.</span><span class="sxs-lookup"><span data-stu-id="f13ed-158">From the output, you see 3 groups returned, named **group1**, **group2**, and **group3**.</span></span> <span data-ttu-id="f13ed-159">Wiele grup może mieć taką samą nazwę, ale zawsze mają unikatowy identyfikator ObjectId.</span><span class="sxs-lookup"><span data-stu-id="f13ed-159">Multiple groups can have the same name but always have a unique ObjectId.</span></span> <span data-ttu-id="f13ed-160">Gdy jest zwracana więcej niż jedna grupa o takiej samej nazwie, użyj identyfikatora ObjectId w wynikach, aby zidentyfikować odpowiedni element.</span><span class="sxs-lookup"><span data-stu-id="f13ed-160">When more than one group that has the same name is returned, use the ObjectId in the output to identify the one you want to use.</span></span>
<span data-ttu-id="f13ed-161">Następnie należy użyć tego polecenia z Set-AzKeyVaultAccessPolicy, aby udzielić uprawnień group2 dla magazynu kluczy o nazwie **myownvault**.</span><span class="sxs-lookup"><span data-stu-id="f13ed-161">You then use the output of this command with Set-AzKeyVaultAccessPolicy to grant permissions to group2 for your key vault, named **myownvault**.</span></span> <span data-ttu-id="f13ed-162">W tym przykładzie są wyliczane grupy o nazwie "group2" w tym samym wierszu polecenia.</span><span class="sxs-lookup"><span data-stu-id="f13ed-162">This example enumerates the groups named 'group2' inline in the same command line.</span></span>
<span data-ttu-id="f13ed-163">Na zwróconej liście może być wiele grup o nazwie "group2".</span><span class="sxs-lookup"><span data-stu-id="f13ed-163">There may be multiple groups in the returned list that are named 'group2'.</span></span>
<span data-ttu-id="f13ed-164">W tym przykładzie wybierany jest pierwszy z nich, wskazany indeksem \[ 0 \] na liście zwróconej.</span><span class="sxs-lookup"><span data-stu-id="f13ed-164">This example picks the first one, indicated by index \[0\] in the returned list.</span></span>

### <span data-ttu-id="f13ed-165">Przykład 7: udzielanie dostępu do usługi Azure Information Protection do klucza dzierżawy zarządzanego przez klienta (BYOK)</span><span class="sxs-lookup"><span data-stu-id="f13ed-165">Example 7: Grant Azure Information Protection access to the customer-managed tenant key (BYOK)</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso04Vault' -ServicePrincipalName 00000012-0000-0000-c000-000000000000 -PermissionsToKeys decrypt,sign,get
```

<span data-ttu-id="f13ed-166">To polecenie upoważnia ochronę informacji platformy Azure do korzystania z klucza zarządzanego przez klienta (w celu skorzystania z własnego klucza lub scenariusza "BYOK") jako klucza dzierżawy usługi Azure Information Protection.</span><span class="sxs-lookup"><span data-stu-id="f13ed-166">This command authorizes Azure Information Protection to use a customer-managed key (the bring your own key, or "BYOK" scenario) as the Azure Information Protection tenant key.</span></span>
<span data-ttu-id="f13ed-167">Po uruchomieniu tego polecenia określ własną nazwę magazynu kluczy, ale musisz określić parametr *ServicePrincipalName* z identyfikatorem GUID **00000012-0000-0000-C000-000000000000** i określ uprawnienia w przykładzie.</span><span class="sxs-lookup"><span data-stu-id="f13ed-167">When you run this command, specify your own key vault name but you must specify the *ServicePrincipalName* parameter with the GUID **00000012-0000-0000-c000-000000000000** and specify the permissions in the example.</span></span>

## <span data-ttu-id="f13ed-168">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f13ed-168">PARAMETERS</span></span>

### <span data-ttu-id="f13ed-169">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="f13ed-169">-ApplicationId</span></span>
<span data-ttu-id="f13ed-170">Do użytku w przyszłości.</span><span class="sxs-lookup"><span data-stu-id="f13ed-170">For future use.</span></span>

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

### <span data-ttu-id="f13ed-171">-BypassObjectIdValidation</span><span class="sxs-lookup"><span data-stu-id="f13ed-171">-BypassObjectIdValidation</span></span>
<span data-ttu-id="f13ed-172">Umożliwia określenie identyfikatora obiektu bez sprawdzania, czy obiekt istnieje w usłudze Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f13ed-172">Enables you to specify an object ID without validating that the object exists in Azure Active Directory.</span></span>
<span data-ttu-id="f13ed-173">Tego parametru należy używać tylko wtedy, gdy użytkownik chce udzielić dostępu do magazynu kluczy do identyfikatora obiektu, który odwołuje się do delegowanej grupy zabezpieczeń z innej dzierżawy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f13ed-173">Use this parameter only if you want to grant access to your key vault to an object ID that refers to a delegated security group from another Azure tenant.</span></span>

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

### <span data-ttu-id="f13ed-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f13ed-174">-DefaultProfile</span></span>
<span data-ttu-id="f13ed-175">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f13ed-175">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f13ed-176">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="f13ed-176">-EmailAddress</span></span>
<span data-ttu-id="f13ed-177">Określa adres e-mail użytkownika, któremu chcesz udzielić uprawnień.</span><span class="sxs-lookup"><span data-stu-id="f13ed-177">Specifies the user email address of the user to whom to grant permissions.</span></span>
<span data-ttu-id="f13ed-178">Ten adres e-mail musi znajdować się w katalogu skojarzonym z bieżącą subskrypcją i być unikatowy.</span><span class="sxs-lookup"><span data-stu-id="f13ed-178">This email address must exist in the directory associated with the current subscription and be unique.</span></span>

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

### <span data-ttu-id="f13ed-179">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="f13ed-179">-EnabledForDeployment</span></span>
<span data-ttu-id="f13ed-180">Umożliwia dostawcy zasobów Microsoft. COMPUTE na pobieranie kluczy tajnych z tego magazynu kluczy, gdy do tego magazynu kluczy odwołuje się tworzenie zasobów, na przykład podczas tworzenia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f13ed-180">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

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

### <span data-ttu-id="f13ed-181">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="f13ed-181">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="f13ed-182">Umożliwia usłudze szyfrowania dysków Azure uzyskiwanie kluczy tajnych i ich odwinięcie z tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="f13ed-182">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

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

### <span data-ttu-id="f13ed-183">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="f13ed-183">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="f13ed-184">Umożliwia menedżerowi zasobów platformy Azure pobieranie kluczy tajnych z tego magazynu kluczy, gdy do tego magazynu kluczy odwołuje się wdrożenie szablonu.</span><span class="sxs-lookup"><span data-stu-id="f13ed-184">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

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

### <span data-ttu-id="f13ed-185">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f13ed-185">-InputObject</span></span>
<span data-ttu-id="f13ed-186">Obiekt magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="f13ed-186">Key Vault Object</span></span>

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

### <span data-ttu-id="f13ed-187">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="f13ed-187">-ObjectId</span></span>
<span data-ttu-id="f13ed-188">Określa identyfikator obiektu podmiotu użytkownika lub usługi w usłudze Azure Active Directory, dla którego ma zostać udzielone uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="f13ed-188">Specifies the object ID of the user or service principal in Azure Active Directory for which to grant permissions.</span></span>

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

### <span data-ttu-id="f13ed-189">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f13ed-189">-PassThru</span></span>
<span data-ttu-id="f13ed-190">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="f13ed-190">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f13ed-191">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="f13ed-191">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f13ed-192">-PermissionsToCertificates</span><span class="sxs-lookup"><span data-stu-id="f13ed-192">-PermissionsToCertificates</span></span>
<span data-ttu-id="f13ed-193">Określa tablicę uprawnień certyfikatów, które mają zostać udzielone użytkownikowi lub podmiotowi zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="f13ed-193">Specifies an array of certificate permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="f13ed-194">Dopuszczalne wartości dla tego parametru:</span><span class="sxs-lookup"><span data-stu-id="f13ed-194">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="f13ed-195">Cały</span><span class="sxs-lookup"><span data-stu-id="f13ed-195">All</span></span>
- <span data-ttu-id="f13ed-196">Pobierz</span><span class="sxs-lookup"><span data-stu-id="f13ed-196">Get</span></span>
- <span data-ttu-id="f13ed-197">Lista</span><span class="sxs-lookup"><span data-stu-id="f13ed-197">List</span></span>
- <span data-ttu-id="f13ed-198">Usuwać</span><span class="sxs-lookup"><span data-stu-id="f13ed-198">Delete</span></span>
- <span data-ttu-id="f13ed-199">Tworzonych</span><span class="sxs-lookup"><span data-stu-id="f13ed-199">Create</span></span>
- <span data-ttu-id="f13ed-200">Przywoz</span><span class="sxs-lookup"><span data-stu-id="f13ed-200">Import</span></span>
- <span data-ttu-id="f13ed-201">Aktualizowane</span><span class="sxs-lookup"><span data-stu-id="f13ed-201">Update</span></span>
- <span data-ttu-id="f13ed-202">Managecontacts</span><span class="sxs-lookup"><span data-stu-id="f13ed-202">Managecontacts</span></span>
- <span data-ttu-id="f13ed-203">Emitenci</span><span class="sxs-lookup"><span data-stu-id="f13ed-203">Getissuers</span></span>
- <span data-ttu-id="f13ed-204">Listissuers</span><span class="sxs-lookup"><span data-stu-id="f13ed-204">Listissuers</span></span>
- <span data-ttu-id="f13ed-205">Autoemitenci</span><span class="sxs-lookup"><span data-stu-id="f13ed-205">Setissuers</span></span>
- <span data-ttu-id="f13ed-206">Deleteissuers</span><span class="sxs-lookup"><span data-stu-id="f13ed-206">Deleteissuers</span></span>
- <span data-ttu-id="f13ed-207">Manageissuers</span><span class="sxs-lookup"><span data-stu-id="f13ed-207">Manageissuers</span></span>
- <span data-ttu-id="f13ed-208">Odzyskiwanie</span><span class="sxs-lookup"><span data-stu-id="f13ed-208">Recover</span></span>
- <span data-ttu-id="f13ed-209">Wykonania</span><span class="sxs-lookup"><span data-stu-id="f13ed-209">Backup</span></span>
- <span data-ttu-id="f13ed-210">Przywrócenie</span><span class="sxs-lookup"><span data-stu-id="f13ed-210">Restore</span></span>
- <span data-ttu-id="f13ed-211">Wyczyścić</span><span class="sxs-lookup"><span data-stu-id="f13ed-211">Purge</span></span>

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

### <span data-ttu-id="f13ed-212">-PermissionsToKeys</span><span class="sxs-lookup"><span data-stu-id="f13ed-212">-PermissionsToKeys</span></span>
<span data-ttu-id="f13ed-213">Określa tablicę uprawnień kluczowych operacji, które mają zostać udzielone użytkownikowi lub podmiotowi zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="f13ed-213">Specifies an array of key operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="f13ed-214">Dopuszczalne wartości dla tego parametru:</span><span class="sxs-lookup"><span data-stu-id="f13ed-214">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="f13ed-215">Cały</span><span class="sxs-lookup"><span data-stu-id="f13ed-215">All</span></span>
- <span data-ttu-id="f13ed-216">Szyfruj</span><span class="sxs-lookup"><span data-stu-id="f13ed-216">Decrypt</span></span>
- <span data-ttu-id="f13ed-217">Szyfrowane</span><span class="sxs-lookup"><span data-stu-id="f13ed-217">Encrypt</span></span>
- <span data-ttu-id="f13ed-218">UnwrapKey</span><span class="sxs-lookup"><span data-stu-id="f13ed-218">UnwrapKey</span></span>
- <span data-ttu-id="f13ed-219">WrapKey</span><span class="sxs-lookup"><span data-stu-id="f13ed-219">WrapKey</span></span>
- <span data-ttu-id="f13ed-220">Sprawdzić</span><span class="sxs-lookup"><span data-stu-id="f13ed-220">Verify</span></span>
- <span data-ttu-id="f13ed-221">Zapisywania</span><span class="sxs-lookup"><span data-stu-id="f13ed-221">Sign</span></span>
- <span data-ttu-id="f13ed-222">Pobierz</span><span class="sxs-lookup"><span data-stu-id="f13ed-222">Get</span></span>
- <span data-ttu-id="f13ed-223">Lista</span><span class="sxs-lookup"><span data-stu-id="f13ed-223">List</span></span>
- <span data-ttu-id="f13ed-224">Aktualizowane</span><span class="sxs-lookup"><span data-stu-id="f13ed-224">Update</span></span>
- <span data-ttu-id="f13ed-225">Tworzonych</span><span class="sxs-lookup"><span data-stu-id="f13ed-225">Create</span></span>
- <span data-ttu-id="f13ed-226">Przywoz</span><span class="sxs-lookup"><span data-stu-id="f13ed-226">Import</span></span>
- <span data-ttu-id="f13ed-227">Usuwać</span><span class="sxs-lookup"><span data-stu-id="f13ed-227">Delete</span></span>
- <span data-ttu-id="f13ed-228">Wykonania</span><span class="sxs-lookup"><span data-stu-id="f13ed-228">Backup</span></span>
- <span data-ttu-id="f13ed-229">Przywrócenie</span><span class="sxs-lookup"><span data-stu-id="f13ed-229">Restore</span></span>
- <span data-ttu-id="f13ed-230">Odzyskiwanie</span><span class="sxs-lookup"><span data-stu-id="f13ed-230">Recover</span></span>
- <span data-ttu-id="f13ed-231">Wyczyścić</span><span class="sxs-lookup"><span data-stu-id="f13ed-231">Purge</span></span>

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

### <span data-ttu-id="f13ed-232">-PermissionsToSecrets</span><span class="sxs-lookup"><span data-stu-id="f13ed-232">-PermissionsToSecrets</span></span>
<span data-ttu-id="f13ed-233">Określa tablicę uprawnień do tajnego działania, które mają zostać udzielone użytkownikowi lub podmiotowi zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="f13ed-233">Specifies an array of secret operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="f13ed-234">Dopuszczalne wartości dla tego parametru:</span><span class="sxs-lookup"><span data-stu-id="f13ed-234">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="f13ed-235">Cały</span><span class="sxs-lookup"><span data-stu-id="f13ed-235">All</span></span>
- <span data-ttu-id="f13ed-236">Pobierz</span><span class="sxs-lookup"><span data-stu-id="f13ed-236">Get</span></span>
- <span data-ttu-id="f13ed-237">Lista</span><span class="sxs-lookup"><span data-stu-id="f13ed-237">List</span></span>
- <span data-ttu-id="f13ed-238">Ustawić</span><span class="sxs-lookup"><span data-stu-id="f13ed-238">Set</span></span>
- <span data-ttu-id="f13ed-239">Usuwać</span><span class="sxs-lookup"><span data-stu-id="f13ed-239">Delete</span></span>
- <span data-ttu-id="f13ed-240">Wykonania</span><span class="sxs-lookup"><span data-stu-id="f13ed-240">Backup</span></span>
- <span data-ttu-id="f13ed-241">Przywrócenie</span><span class="sxs-lookup"><span data-stu-id="f13ed-241">Restore</span></span>
- <span data-ttu-id="f13ed-242">Odzyskiwanie</span><span class="sxs-lookup"><span data-stu-id="f13ed-242">Recover</span></span>
- <span data-ttu-id="f13ed-243">Wyczyścić</span><span class="sxs-lookup"><span data-stu-id="f13ed-243">Purge</span></span>

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

### <span data-ttu-id="f13ed-244">-PermissionsToStorage</span><span class="sxs-lookup"><span data-stu-id="f13ed-244">-PermissionsToStorage</span></span>
<span data-ttu-id="f13ed-245">Określa zarządzane konto magazynu i uprawnienia operacji definicji SaS, które mają zostać udzielone użytkownikowi lub podmiotowi zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="f13ed-245">Specifies managed storage account and SaS-definition operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="f13ed-246">Dopuszczalne wartości dla tego parametru:</span><span class="sxs-lookup"><span data-stu-id="f13ed-246">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="f13ed-247">cały</span><span class="sxs-lookup"><span data-stu-id="f13ed-247">all</span></span>
- <span data-ttu-id="f13ed-248">Pobierz</span><span class="sxs-lookup"><span data-stu-id="f13ed-248">get</span></span>
- <span data-ttu-id="f13ed-249">Lista</span><span class="sxs-lookup"><span data-stu-id="f13ed-249">list</span></span>
- <span data-ttu-id="f13ed-250">usuwać</span><span class="sxs-lookup"><span data-stu-id="f13ed-250">delete</span></span>
- <span data-ttu-id="f13ed-251">ustawić</span><span class="sxs-lookup"><span data-stu-id="f13ed-251">set</span></span>
- <span data-ttu-id="f13ed-252">aktualizowane</span><span class="sxs-lookup"><span data-stu-id="f13ed-252">update</span></span>
- <span data-ttu-id="f13ed-253">regeneratekey</span><span class="sxs-lookup"><span data-stu-id="f13ed-253">regeneratekey</span></span>
- <span data-ttu-id="f13ed-254">getsas</span><span class="sxs-lookup"><span data-stu-id="f13ed-254">getsas</span></span>
- <span data-ttu-id="f13ed-255">listsas</span><span class="sxs-lookup"><span data-stu-id="f13ed-255">listsas</span></span>
- <span data-ttu-id="f13ed-256">deletesas</span><span class="sxs-lookup"><span data-stu-id="f13ed-256">deletesas</span></span>
- <span data-ttu-id="f13ed-257">setsas</span><span class="sxs-lookup"><span data-stu-id="f13ed-257">setsas</span></span>
- <span data-ttu-id="f13ed-258">odzyskiwanie</span><span class="sxs-lookup"><span data-stu-id="f13ed-258">recover</span></span>
- <span data-ttu-id="f13ed-259">wykonania</span><span class="sxs-lookup"><span data-stu-id="f13ed-259">backup</span></span>
- <span data-ttu-id="f13ed-260">przywrócenie</span><span class="sxs-lookup"><span data-stu-id="f13ed-260">restore</span></span>
- <span data-ttu-id="f13ed-261">wyczyścić</span><span class="sxs-lookup"><span data-stu-id="f13ed-261">purge</span></span>

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

### <span data-ttu-id="f13ed-262">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f13ed-262">-ResourceGroupName</span></span>
<span data-ttu-id="f13ed-263">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f13ed-263">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f13ed-264">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f13ed-264">-ResourceId</span></span>
<span data-ttu-id="f13ed-265">Identyfikator zasobu magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="f13ed-265">Key Vault Resource Id</span></span>

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

### <span data-ttu-id="f13ed-266">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="f13ed-266">-ServicePrincipalName</span></span>
<span data-ttu-id="f13ed-267">Określa główną nazwę usługi aplikacji, do której mają być udzielane uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="f13ed-267">Specifies the service principal name of the application to which to grant permissions.</span></span>
<span data-ttu-id="f13ed-268">Określ identyfikator aplikacji, określany także jako identyfikator klienta, zarejestrowany dla aplikacji w katalogu AzureActive.</span><span class="sxs-lookup"><span data-stu-id="f13ed-268">Specify the application ID, also known as client ID, registered for the application in AzureActive Directory.</span></span> <span data-ttu-id="f13ed-269">Aplikacja o głównej nazwie usługi, którą ten parametr określa, musi być zarejestrowana w katalogu platformy Azure, który zawiera bieżący abonament.</span><span class="sxs-lookup"><span data-stu-id="f13ed-269">The application with the service principal name that this parameter specifies must be registered in the Azure directory that contains your current subscription.</span></span>

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

### <span data-ttu-id="f13ed-270">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="f13ed-270">-UserPrincipalName</span></span>
<span data-ttu-id="f13ed-271">Określa główną nazwę użytkownika, któremu chcesz udzielić uprawnień.</span><span class="sxs-lookup"><span data-stu-id="f13ed-271">Specifies the user principal name of the user to whom to grant permissions.</span></span>
<span data-ttu-id="f13ed-272">Ta główna nazwa użytkownika musi istnieć w katalogu skojarzonym z bieżącą subskrypcją.</span><span class="sxs-lookup"><span data-stu-id="f13ed-272">This user principal name must exist in the directory associated with the current subscription.</span></span>

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

### <span data-ttu-id="f13ed-273">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="f13ed-273">-VaultName</span></span>
<span data-ttu-id="f13ed-274">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="f13ed-274">Specifies the name of a key vault.</span></span>
<span data-ttu-id="f13ed-275">To polecenie cmdlet modyfikuje zasady dostępu dla magazynu kluczy określanego przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="f13ed-275">This cmdlet modifies the access policy for the key vault that this parameter specifies.</span></span>

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

### <span data-ttu-id="f13ed-276">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f13ed-276">-Confirm</span></span>
<span data-ttu-id="f13ed-277">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f13ed-277">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f13ed-278">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f13ed-278">-WhatIf</span></span>
<span data-ttu-id="f13ed-279">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f13ed-279">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f13ed-280">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f13ed-280">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f13ed-281">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f13ed-281">CommonParameters</span></span>
<span data-ttu-id="f13ed-282">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f13ed-282">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f13ed-283">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f13ed-283">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f13ed-284">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f13ed-284">INPUTS</span></span>

### <span data-ttu-id="f13ed-285">Microsoft. Azure. Commands. platforming. models. PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="f13ed-285">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

### <span data-ttu-id="f13ed-286">System. String</span><span class="sxs-lookup"><span data-stu-id="f13ed-286">System.String</span></span>

## <span data-ttu-id="f13ed-287">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f13ed-287">OUTPUTS</span></span>

### <span data-ttu-id="f13ed-288">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="f13ed-288">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="f13ed-289">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f13ed-289">NOTES</span></span>

## <span data-ttu-id="f13ed-290">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f13ed-290">RELATED LINKS</span></span>

[<span data-ttu-id="f13ed-291">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="f13ed-291">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="f13ed-292">Remove-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f13ed-292">Remove-AzKeyVaultAccessPolicy</span></span>](./Remove-AzKeyVaultAccessPolicy.md)

