---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 636FAD5B-8C39-4E5C-8978-6845C6B89BC0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurermkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureRmKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureRmKeyVaultAccessPolicy.md
ms.openlocfilehash: d7cd2718377fee36b5aa49f91385de73e3ea6367
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716946"
---
# <span data-ttu-id="8d918-101">Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8d918-101">Set-AzureRmKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="8d918-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8d918-102">SYNOPSIS</span></span>
<span data-ttu-id="8d918-103">Udziela lub modyfikuje istniejące uprawnienia dla użytkownika, aplikacji lub grupy zabezpieczeń w celu wykonania operacji za pomocą magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="8d918-103">Grants or modifies existing permissions for a user, application, or security group to perform operations with a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d918-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8d918-104">SYNTAX</span></span>

### <span data-ttu-id="8d918-105">ByUserPrincipalName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8d918-105">ByUserPrincipalName (Default)</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -UserPrincipalName <String> [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d918-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="8d918-106">ByObjectId</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d918-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="8d918-107">ByServicePrincipalName</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d918-108">ByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="8d918-108">ByEmailAddress</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8d918-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="8d918-109">ForVault</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d918-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="8d918-110">InputObjectByObjectId</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ObjectId <String>
 [-ApplicationId <Guid>] [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d918-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="8d918-111">InputObjectByServicePrincipalName</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8d918-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="8d918-112">InputObjectByUserPrincipalName</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8d918-113">InputObjectByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="8d918-113">InputObjectByEmailAddress</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8d918-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="8d918-114">InputObjectForVault</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d918-115">ResourceIdByObjectId</span><span class="sxs-lookup"><span data-stu-id="8d918-115">ResourceIdByObjectId</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-ResourceId] <String> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d918-116">ResourceIdByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="8d918-116">ResourceIdByServicePrincipalName</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-ResourceId] <String> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8d918-117">ResourceIdByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="8d918-117">ResourceIdByUserPrincipalName</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-ResourceId] <String> -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8d918-118">ResourceIdByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="8d918-118">ResourceIdByEmailAddress</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-ResourceId] <String> -EmailAddress <String> [-PermissionsToKeys <String[]>]
 [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d918-119">ResourceIdForVault</span><span class="sxs-lookup"><span data-stu-id="8d918-119">ResourceIdForVault</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-ResourceId] <String> [-EnabledForDeployment] [-EnabledForTemplateDeployment]
 [-EnabledForDiskEncryption] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8d918-120">Opis</span><span class="sxs-lookup"><span data-stu-id="8d918-120">DESCRIPTION</span></span>
<span data-ttu-id="8d918-121">Polecenie cmdlet **Set-AzureRmKeyVaultAccessPolicy** udziela lub modyfikuje istniejące uprawnienia dla użytkownika, aplikacji lub grupy zabezpieczeń w celu wykonania określonych operacji w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="8d918-121">The **Set-AzureRmKeyVaultAccessPolicy** cmdlet grants or modifies existing permissions for a user, application, or security group to perform the specified operations with a key vault.</span></span> <span data-ttu-id="8d918-122">W magazynie kluczy nie są modyfikowane uprawnienia innych użytkowników, aplikacji ani grup zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="8d918-122">It does not modify the permissions that other users, applications, or security groups have on the key vault.</span></span>
<span data-ttu-id="8d918-123">Jeśli ustawiasz uprawnienia dla grupy zabezpieczeń, ta operacja będzie miała wpływ tylko na użytkowników tej grupy zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="8d918-123">If you are setting permissions for a security group, this operation affects only users in that security group.</span></span>
<span data-ttu-id="8d918-124">Wszystkie następujące katalogi muszą być tego samego katalogu platformy Azure:</span><span class="sxs-lookup"><span data-stu-id="8d918-124">The following directories must all be the same Azure directory:</span></span> 
- <span data-ttu-id="8d918-125">Katalog domyślny subskrypcji platformy Azure, w której znajduje się magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="8d918-125">The default directory of the Azure subscription in which the key vault resides.</span></span>
- <span data-ttu-id="8d918-126">Katalog platformy Azure zawierający użytkownika lub grupę aplikacji, do których udzielasz uprawnień.</span><span class="sxs-lookup"><span data-stu-id="8d918-126">The Azure directory that contains the user or application group that you are granting permissions to.</span></span>
<span data-ttu-id="8d918-127">Przykłady scenariuszy, w których te warunki nie są spełnione, a to polecenie cmdlet nie będzie działać:</span><span class="sxs-lookup"><span data-stu-id="8d918-127">Examples of scenarios when these conditions are not met and this cmdlet will not work are:</span></span> 
- <span data-ttu-id="8d918-128">Autoryzowanie użytkownika od innej organizacji do zarządzania magazynem kluczy.</span><span class="sxs-lookup"><span data-stu-id="8d918-128">Authorizing a user from a different organization to manage your key vault.</span></span>
<span data-ttu-id="8d918-129">Każda organizacja ma swój własny katalog.</span><span class="sxs-lookup"><span data-stu-id="8d918-129">Each organization has its own directory.</span></span> 
- <span data-ttu-id="8d918-130">Twoje konto platformy Azure ma wiele katalogów.</span><span class="sxs-lookup"><span data-stu-id="8d918-130">Your Azure account has multiple directories.</span></span>
<span data-ttu-id="8d918-131">Jeśli zarejestrujesz aplikację w katalogu innym niż katalog domyślny, nie możesz autoryzować tej aplikacji do korzystania z Twojego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="8d918-131">If you register an application in a directory other than the default directory, you cannot authorize that application to use your key vault.</span></span>
<span data-ttu-id="8d918-132">Aplikacja musi znajdować się w katalogu domyślnym.</span><span class="sxs-lookup"><span data-stu-id="8d918-132">The application must be in the default directory.</span></span>
<span data-ttu-id="8d918-133">Uwaga: chociaż określenie grupy zasobów jest opcjonalne dla tego polecenia cmdlet, należy to zrobić w celu uzyskania lepszej wydajności.</span><span class="sxs-lookup"><span data-stu-id="8d918-133">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="8d918-134">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8d918-134">EXAMPLES</span></span>

### <span data-ttu-id="8d918-135">Przykład 1: udzielanie uprawnień użytkownikowi dla magazynu kluczy i modyfikowanie uprawnień</span><span class="sxs-lookup"><span data-stu-id="8d918-135">Example 1: Grant permissions to a user for a key vault and modify the permissions</span></span>
```powershell
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys create,import,delete,list -PermissionsToSecrets set,delete -PassThru

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

PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets set,delete,get -PassThru

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

PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys @() -PassThru

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

<span data-ttu-id="8d918-136">Pierwsze polecenie udziela uprawnień użytkownikowi w usłudze Azure Active Directory, PattiFuller@contoso.com Aby wykonywać operacje na kluczach i kluczach tajnych przy użyciu magazynu kluczy o nazwie Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="8d918-136">The first command grants permissions for a user in your Azure Active Directory, PattiFuller@contoso.com, to perform operations on keys and secrets with a key vault named Contoso03Vault.</span></span> <span data-ttu-id="8d918-137">Parametr *PassThru* powoduje, że zaktualizowany obiekt jest zwracany przez polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d918-137">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>
<span data-ttu-id="8d918-138">Drugie polecenie modyfikuje uprawnienia udzielone PattiFuller@contoso.com w pierwszym poleceniu w celu umożliwienia natychmiastowego wprowadzenia kluczy tajnych oraz ich usunięcia.</span><span class="sxs-lookup"><span data-stu-id="8d918-138">The second command modifies the permissions that were granted to PattiFuller@contoso.com in the first command, to now allow getting secrets in addition to setting and deleting them.</span></span> <span data-ttu-id="8d918-139">Uprawnienia do kluczowych operacji pozostają niezmienione po wykonaniu tego polecenia.</span><span class="sxs-lookup"><span data-stu-id="8d918-139">The permissions to key operations remain unchanged after this command.</span></span>
<span data-ttu-id="8d918-140">Polecenie ostatnie modyfikuje istniejące uprawnienia w PattiFuller@contoso.com celu usunięcia wszystkich uprawnień do kluczowych operacji.</span><span class="sxs-lookup"><span data-stu-id="8d918-140">The final command further modifies the existing permissions for PattiFuller@contoso.com to remove all permissions to key operations.</span></span> <span data-ttu-id="8d918-141">Po wykonaniu tego polecenia uprawnienia do tajnych operacji pozostają niezmienione.</span><span class="sxs-lookup"><span data-stu-id="8d918-141">The permissions to secret operations remain unchanged after this command.</span></span> 

### <span data-ttu-id="8d918-142">Przykład 2: udzielanie uprawnień głównemu usłudze aplikacji w celu odczytywania i zapisywania kluczy tajnych</span><span class="sxs-lookup"><span data-stu-id="8d918-142">Example 2: Grant permissions for an application service principal to read and write secrets</span></span>
```powershell
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com' -PermissionsToSecrets Get,Set
```

<span data-ttu-id="8d918-143">To polecenie udziela uprawnień do aplikacji dla magazynu kluczy o nazwie Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="8d918-143">This command grants permissions for an application for a key vault named Contoso03Vault.</span></span> <span data-ttu-id="8d918-144">Parametr *ServicePrincipalName* określa aplikację.</span><span class="sxs-lookup"><span data-stu-id="8d918-144">The *ServicePrincipalName* parameter specifies the application.</span></span> <span data-ttu-id="8d918-145">Aplikacja musi być zarejestrowana w usłudze Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8d918-145">The application must be registered in your Azure Active Directory.</span></span> <span data-ttu-id="8d918-146">Wartość parametru *ServicePrincipalName* musi być nazwą główną usługi aplikacji lub identyfikatorem GUID identyfikatora aplikacji.</span><span class="sxs-lookup"><span data-stu-id="8d918-146">The value of the *ServicePrincipalName* parameter must be either the service principal name of the application or the application ID GUID.</span></span>
<span data-ttu-id="8d918-147">W tym przykładzie określono nazwę główną usługi http://payroll.contoso.com , a polecenie przyznaje uprawnienia aplikacji do odczytu i zapisu kluczy tajnych.</span><span class="sxs-lookup"><span data-stu-id="8d918-147">This example specifies the service principal name http://payroll.contoso.com, and the command grants the application permissions to read and write secrets.</span></span>

### <span data-ttu-id="8d918-148">Przykład 3: udzielanie uprawnień do aplikacji przy użyciu jej identyfikatora obiektu</span><span class="sxs-lookup"><span data-stu-id="8d918-148">Example 3: Grant permissions for an application using its object ID</span></span>
```powershell
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectId 34595082-9346-41b6-8d6b-295a2808b8db -PermissionsToSecrets Get,Set
```

<span data-ttu-id="8d918-149">To polecenie udziela uprawnień aplikacji do odczytu i zapisu kluczy tajnych.</span><span class="sxs-lookup"><span data-stu-id="8d918-149">This command grants the application permissions to read and write secrets.</span></span>
<span data-ttu-id="8d918-150">W tym przykładzie określono aplikację przy użyciu identyfikatora obiektu głównego usługi aplikacji.</span><span class="sxs-lookup"><span data-stu-id="8d918-150">This example specifies the application using the object ID of the service principal of the application.</span></span>

### <span data-ttu-id="8d918-151">Przykład 4: udzielanie uprawnień dla głównej nazwy użytkownika</span><span class="sxs-lookup"><span data-stu-id="8d918-151">Example 4: Grant permissions for a user principal name</span></span>
```powershell
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets Get,List,Set
```

<span data-ttu-id="8d918-152">To polecenie udziela uprawnień Get, list i ustawia uprawnienia dla określonej nazwy głównej użytkownika w celu uzyskania dostępu do kluczy tajnych.</span><span class="sxs-lookup"><span data-stu-id="8d918-152">This command grants get, list, and set permissions for the specified user principal name for access to secrets.</span></span>

### <span data-ttu-id="8d918-153">Przykład 5: Włączanie kluczy tajnych do pobrania z magazynu kluczy przez firmę Microsoft. Oblicz dostawcę zasobów</span><span class="sxs-lookup"><span data-stu-id="8d918-153">Example 5: Enable secrets to be retrieved from a key vault by the Microsoft.Compute resource provider</span></span>
```powershell
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="8d918-154">To polecenie udziela uprawnień do pobierania kluczy tajnych z magazynu kluczy Contoso03Vault przez dostawcę Microsoft. COMPUTE Resource.</span><span class="sxs-lookup"><span data-stu-id="8d918-154">This command grants the permissions for secrets to be retrieved from the Contoso03Vault key vault by the Microsoft.Compute resource provider.</span></span>

### <span data-ttu-id="8d918-155">Przykład 6: udzielanie uprawnień grupie zabezpieczeń</span><span class="sxs-lookup"><span data-stu-id="8d918-155">Example 6: Grant permissions to a security group</span></span>
```powershell
PS C:\> Get-AzureRmADGroup
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'myownvault' -ObjectId (Get-AzureRmADGroup -SearchString 'group2')[0].Id -PermissionsToKeys get, set -PermissionsToSecrets get, set
```

<span data-ttu-id="8d918-156">W pierwszym poleceniu jest używane polecenie cmdlet Get-AzureRmADGroup, aby uzyskać dostęp do wszystkich grup usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8d918-156">The first command uses the Get-AzureRmADGroup cmdlet to get all Active Directory groups.</span></span> <span data-ttu-id="8d918-157">Na podstawie wyników są wyświetlane 3 grupy zwrócone, nazwane **grupa1** , **group2** oraz **Group3**.</span><span class="sxs-lookup"><span data-stu-id="8d918-157">From the output, you see 3 groups returned, named **group1** , **group2** , and **group3**.</span></span> <span data-ttu-id="8d918-158">Wiele grup może mieć taką samą nazwę, ale zawsze mają unikatowy identyfikator ObjectId.</span><span class="sxs-lookup"><span data-stu-id="8d918-158">Multiple groups can have the same name but always have a unique ObjectId.</span></span> <span data-ttu-id="8d918-159">Gdy jest zwracana więcej niż jedna grupa o takiej samej nazwie, użyj identyfikatora ObjectId w wynikach, aby zidentyfikować odpowiedni element.</span><span class="sxs-lookup"><span data-stu-id="8d918-159">When more than one group that has the same name is returned, use the ObjectId in the output to identify the one you want to use.</span></span>
<span data-ttu-id="8d918-160">Następnie należy użyć tego polecenia z Set-AzureRmKeyVaultAccessPolicy, aby udzielić uprawnień group2 dla magazynu kluczy o nazwie **myownvault**.</span><span class="sxs-lookup"><span data-stu-id="8d918-160">You then use the output of this command with Set-AzureRmKeyVaultAccessPolicy to grant permissions to group2 for your key vault, named **myownvault**.</span></span> <span data-ttu-id="8d918-161">W tym przykładzie są wyliczane grupy o nazwie "group2" w tym samym wierszu polecenia.</span><span class="sxs-lookup"><span data-stu-id="8d918-161">This example enumerates the groups named 'group2' inline in the same command line.</span></span>
<span data-ttu-id="8d918-162">Na zwróconej liście może być wiele grup o nazwie "group2".</span><span class="sxs-lookup"><span data-stu-id="8d918-162">There may be multiple groups in the returned list that are named 'group2'.</span></span>
<span data-ttu-id="8d918-163">W tym przykładzie wybierany jest pierwszy z nich, wskazany indeksem \[ 0 \] na liście zwróconej.</span><span class="sxs-lookup"><span data-stu-id="8d918-163">This example picks the first one, indicated by index \[0\] in the returned list.</span></span>

### <span data-ttu-id="8d918-164">Przykład 7: udzielanie dostępu do usługi Azure Information Protection do klucza dzierżawy zarządzanego przez klienta (BYOK)</span><span class="sxs-lookup"><span data-stu-id="8d918-164">Example 7: Grant Azure Information Protection access to the customer-managed tenant key (BYOK)</span></span>
```powershell
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso04Vault' -ServicePrincipalName 00000012-0000-0000-c000-000000000000 -PermissionsToKeys decrypt,sign,get
```

<span data-ttu-id="8d918-165">To polecenie upoważnia ochronę informacji platformy Azure do korzystania z klucza zarządzanego przez klienta (w celu skorzystania z własnego klucza lub scenariusza "BYOK") jako klucza dzierżawy usługi Azure Information Protection.</span><span class="sxs-lookup"><span data-stu-id="8d918-165">This command authorizes Azure Information Protection to use a customer-managed key (the bring your own key, or "BYOK" scenario) as the Azure Information Protection tenant key.</span></span>
<span data-ttu-id="8d918-166">Po uruchomieniu tego polecenia określ własną nazwę magazynu kluczy, ale musisz określić parametr *ServicePrincipalName* z identyfikatorem GUID **00000012-0000-0000-C000-000000000000** i określ uprawnienia w przykładzie.</span><span class="sxs-lookup"><span data-stu-id="8d918-166">When you run this command, specify your own key vault name but you must specify the *ServicePrincipalName* parameter with the GUID **00000012-0000-0000-c000-000000000000** and specify the permissions in the example.</span></span>

## <span data-ttu-id="8d918-167">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8d918-167">PARAMETERS</span></span>

### <span data-ttu-id="8d918-168">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="8d918-168">-ApplicationId</span></span>
<span data-ttu-id="8d918-169">Do użytku w przyszłości.</span><span class="sxs-lookup"><span data-stu-id="8d918-169">For future use.</span></span>

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

### <span data-ttu-id="8d918-170">-BypassObjectIdValidation</span><span class="sxs-lookup"><span data-stu-id="8d918-170">-BypassObjectIdValidation</span></span>
<span data-ttu-id="8d918-171">Umożliwia określenie identyfikatora obiektu bez sprawdzania, czy obiekt istnieje w usłudze Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8d918-171">Enables you to specify an object ID without validating that the object exists in Azure Active Directory.</span></span>
<span data-ttu-id="8d918-172">Tego parametru należy używać tylko wtedy, gdy użytkownik chce udzielić dostępu do magazynu kluczy do identyfikatora obiektu, który odwołuje się do delegowanej grupy zabezpieczeń z innej dzierżawy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8d918-172">Use this parameter only if you want to grant access to your key vault to an object ID that refers to a delegated security group from another Azure tenant.</span></span>

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

### <span data-ttu-id="8d918-173">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d918-173">-DefaultProfile</span></span>
<span data-ttu-id="8d918-174">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="8d918-174">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d918-175">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="8d918-175">-EmailAddress</span></span>
<span data-ttu-id="8d918-176">Określa adres e-mail użytkownika, któremu chcesz udzielić uprawnień.</span><span class="sxs-lookup"><span data-stu-id="8d918-176">Specifies the user email address of the user to whom to grant permissions.</span></span>
<span data-ttu-id="8d918-177">Ten adres e-mail musi znajdować się w katalogu skojarzonym z bieżącą subskrypcją i być unikatowy.</span><span class="sxs-lookup"><span data-stu-id="8d918-177">This email address must exist in the directory associated with the current subscription and be unique.</span></span>

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

### <span data-ttu-id="8d918-178">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="8d918-178">-EnabledForDeployment</span></span>
<span data-ttu-id="8d918-179">Umożliwia dostawcy zasobów Microsoft. COMPUTE na pobieranie kluczy tajnych z tego magazynu kluczy, gdy do tego magazynu kluczy odwołuje się tworzenie zasobów, na przykład podczas tworzenia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8d918-179">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

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

### <span data-ttu-id="8d918-180">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="8d918-180">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="8d918-181">Umożliwia usłudze szyfrowania dysków Azure uzyskiwanie kluczy tajnych i ich odwinięcie z tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="8d918-181">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

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

### <span data-ttu-id="8d918-182">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="8d918-182">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="8d918-183">Umożliwia menedżerowi zasobów platformy Azure pobieranie kluczy tajnych z tego magazynu kluczy, gdy do tego magazynu kluczy odwołuje się wdrożenie szablonu.</span><span class="sxs-lookup"><span data-stu-id="8d918-183">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

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

### <span data-ttu-id="8d918-184">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8d918-184">-InputObject</span></span>
<span data-ttu-id="8d918-185">Obiekt magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="8d918-185">Key Vault Object</span></span>

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

### <span data-ttu-id="8d918-186">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="8d918-186">-ObjectId</span></span>
<span data-ttu-id="8d918-187">Określa identyfikator obiektu podmiotu użytkownika lub usługi w usłudze Azure Active Directory, dla którego ma zostać udzielone uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="8d918-187">Specifies the object ID of the user or service principal in Azure Active Directory for which to grant permissions.</span></span>

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

### <span data-ttu-id="8d918-188">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8d918-188">-PassThru</span></span>
<span data-ttu-id="8d918-189">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="8d918-189">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8d918-190">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="8d918-190">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8d918-191">-PermissionsToCertificates</span><span class="sxs-lookup"><span data-stu-id="8d918-191">-PermissionsToCertificates</span></span>
<span data-ttu-id="8d918-192">Określa tablicę uprawnień certyfikatów, które mają zostać udzielone użytkownikowi lub podmiotowi zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="8d918-192">Specifies an array of certificate permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="8d918-193">Dopuszczalne wartości dla tego parametru:</span><span class="sxs-lookup"><span data-stu-id="8d918-193">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="8d918-194">Pobierz</span><span class="sxs-lookup"><span data-stu-id="8d918-194">Get</span></span>
- <span data-ttu-id="8d918-195">Lista</span><span class="sxs-lookup"><span data-stu-id="8d918-195">List</span></span>
- <span data-ttu-id="8d918-196">Usuwać</span><span class="sxs-lookup"><span data-stu-id="8d918-196">Delete</span></span>
- <span data-ttu-id="8d918-197">Tworzonych</span><span class="sxs-lookup"><span data-stu-id="8d918-197">Create</span></span>
- <span data-ttu-id="8d918-198">Przywoz</span><span class="sxs-lookup"><span data-stu-id="8d918-198">Import</span></span>
- <span data-ttu-id="8d918-199">Aktualizowane</span><span class="sxs-lookup"><span data-stu-id="8d918-199">Update</span></span>
- <span data-ttu-id="8d918-200">Managecontacts</span><span class="sxs-lookup"><span data-stu-id="8d918-200">Managecontacts</span></span>
- <span data-ttu-id="8d918-201">Emitenci</span><span class="sxs-lookup"><span data-stu-id="8d918-201">Getissuers</span></span>
- <span data-ttu-id="8d918-202">Listissuers</span><span class="sxs-lookup"><span data-stu-id="8d918-202">Listissuers</span></span>
- <span data-ttu-id="8d918-203">Autoemitenci</span><span class="sxs-lookup"><span data-stu-id="8d918-203">Setissuers</span></span>
- <span data-ttu-id="8d918-204">Deleteissuers</span><span class="sxs-lookup"><span data-stu-id="8d918-204">Deleteissuers</span></span>
- <span data-ttu-id="8d918-205">Manageissuers</span><span class="sxs-lookup"><span data-stu-id="8d918-205">Manageissuers</span></span>
- <span data-ttu-id="8d918-206">Odzyskiwanie</span><span class="sxs-lookup"><span data-stu-id="8d918-206">Recover</span></span>
- <span data-ttu-id="8d918-207">Wykonania</span><span class="sxs-lookup"><span data-stu-id="8d918-207">Backup</span></span>
- <span data-ttu-id="8d918-208">Przywrócenie</span><span class="sxs-lookup"><span data-stu-id="8d918-208">Restore</span></span>
- <span data-ttu-id="8d918-209">Wyczyścić</span><span class="sxs-lookup"><span data-stu-id="8d918-209">Purge</span></span>

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

### <span data-ttu-id="8d918-210">-PermissionsToKeys</span><span class="sxs-lookup"><span data-stu-id="8d918-210">-PermissionsToKeys</span></span>
<span data-ttu-id="8d918-211">Określa tablicę uprawnień kluczowych operacji, które mają zostać udzielone użytkownikowi lub podmiotowi zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="8d918-211">Specifies an array of key operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="8d918-212">Dopuszczalne wartości dla tego parametru:</span><span class="sxs-lookup"><span data-stu-id="8d918-212">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="8d918-213">Szyfruj</span><span class="sxs-lookup"><span data-stu-id="8d918-213">Decrypt</span></span>
- <span data-ttu-id="8d918-214">Szyfrowane</span><span class="sxs-lookup"><span data-stu-id="8d918-214">Encrypt</span></span>
- <span data-ttu-id="8d918-215">UnwrapKey</span><span class="sxs-lookup"><span data-stu-id="8d918-215">UnwrapKey</span></span>
- <span data-ttu-id="8d918-216">WrapKey</span><span class="sxs-lookup"><span data-stu-id="8d918-216">WrapKey</span></span>
- <span data-ttu-id="8d918-217">Sprawdzić</span><span class="sxs-lookup"><span data-stu-id="8d918-217">Verify</span></span>
- <span data-ttu-id="8d918-218">Zapisywania</span><span class="sxs-lookup"><span data-stu-id="8d918-218">Sign</span></span>
- <span data-ttu-id="8d918-219">Pobierz</span><span class="sxs-lookup"><span data-stu-id="8d918-219">Get</span></span>
- <span data-ttu-id="8d918-220">Lista</span><span class="sxs-lookup"><span data-stu-id="8d918-220">List</span></span>
- <span data-ttu-id="8d918-221">Aktualizowane</span><span class="sxs-lookup"><span data-stu-id="8d918-221">Update</span></span>
- <span data-ttu-id="8d918-222">Tworzonych</span><span class="sxs-lookup"><span data-stu-id="8d918-222">Create</span></span>
- <span data-ttu-id="8d918-223">Przywoz</span><span class="sxs-lookup"><span data-stu-id="8d918-223">Import</span></span>
- <span data-ttu-id="8d918-224">Usuwać</span><span class="sxs-lookup"><span data-stu-id="8d918-224">Delete</span></span>
- <span data-ttu-id="8d918-225">Wykonania</span><span class="sxs-lookup"><span data-stu-id="8d918-225">Backup</span></span>
- <span data-ttu-id="8d918-226">Przywrócenie</span><span class="sxs-lookup"><span data-stu-id="8d918-226">Restore</span></span>
- <span data-ttu-id="8d918-227">Odzyskiwanie</span><span class="sxs-lookup"><span data-stu-id="8d918-227">Recover</span></span>
- <span data-ttu-id="8d918-228">Wyczyścić</span><span class="sxs-lookup"><span data-stu-id="8d918-228">Purge</span></span>

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

### <span data-ttu-id="8d918-229">-PermissionsToSecrets</span><span class="sxs-lookup"><span data-stu-id="8d918-229">-PermissionsToSecrets</span></span>
<span data-ttu-id="8d918-230">Określa tablicę uprawnień do tajnego działania, które mają zostać udzielone użytkownikowi lub podmiotowi zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="8d918-230">Specifies an array of secret operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="8d918-231">Dopuszczalne wartości dla tego parametru:</span><span class="sxs-lookup"><span data-stu-id="8d918-231">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="8d918-232">Pobierz</span><span class="sxs-lookup"><span data-stu-id="8d918-232">Get</span></span>
- <span data-ttu-id="8d918-233">Lista</span><span class="sxs-lookup"><span data-stu-id="8d918-233">List</span></span>
- <span data-ttu-id="8d918-234">Ustawić</span><span class="sxs-lookup"><span data-stu-id="8d918-234">Set</span></span>
- <span data-ttu-id="8d918-235">Usuwać</span><span class="sxs-lookup"><span data-stu-id="8d918-235">Delete</span></span>
- <span data-ttu-id="8d918-236">Wykonania</span><span class="sxs-lookup"><span data-stu-id="8d918-236">Backup</span></span>
- <span data-ttu-id="8d918-237">Przywrócenie</span><span class="sxs-lookup"><span data-stu-id="8d918-237">Restore</span></span>
- <span data-ttu-id="8d918-238">Odzyskiwanie</span><span class="sxs-lookup"><span data-stu-id="8d918-238">Recover</span></span>
- <span data-ttu-id="8d918-239">Wyczyścić</span><span class="sxs-lookup"><span data-stu-id="8d918-239">Purge</span></span>

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

### <span data-ttu-id="8d918-240">-PermissionsToStorage</span><span class="sxs-lookup"><span data-stu-id="8d918-240">-PermissionsToStorage</span></span>
<span data-ttu-id="8d918-241">Określa zarządzane konto magazynu i uprawnienia operacji definicji SaS, które mają zostać udzielone użytkownikowi lub podmiotowi zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="8d918-241">Specifies managed storage account and SaS-definition operation permissions to grant to a user or service principal.</span></span>

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

### <span data-ttu-id="8d918-242">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d918-242">-ResourceGroupName</span></span>
<span data-ttu-id="8d918-243">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8d918-243">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="8d918-244">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8d918-244">-ResourceId</span></span>
<span data-ttu-id="8d918-245">Identyfikator zasobu magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="8d918-245">Key Vault Resource Id</span></span>

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

### <span data-ttu-id="8d918-246">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="8d918-246">-ServicePrincipalName</span></span>
<span data-ttu-id="8d918-247">Określa główną nazwę usługi aplikacji, do której mają być udzielane uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="8d918-247">Specifies the service principal name of the application to which to grant permissions.</span></span>
<span data-ttu-id="8d918-248">Określ identyfikator aplikacji, określany także jako identyfikator klienta, zarejestrowany dla aplikacji w katalogu AzureActive.</span><span class="sxs-lookup"><span data-stu-id="8d918-248">Specify the application ID, also known as client ID, registered for the application in AzureActive Directory.</span></span> <span data-ttu-id="8d918-249">Aplikacja o głównej nazwie usługi, którą ten parametr określa, musi być zarejestrowana w katalogu platformy Azure, który zawiera bieżący abonament.</span><span class="sxs-lookup"><span data-stu-id="8d918-249">The application with the service principal name that this parameter specifies must be registered in the Azure directory that contains your current subscription.</span></span>

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

### <span data-ttu-id="8d918-250">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="8d918-250">-UserPrincipalName</span></span>
<span data-ttu-id="8d918-251">Określa główną nazwę użytkownika, któremu chcesz udzielić uprawnień.</span><span class="sxs-lookup"><span data-stu-id="8d918-251">Specifies the user principal name of the user to whom to grant permissions.</span></span>
<span data-ttu-id="8d918-252">Ta główna nazwa użytkownika musi istnieć w katalogu skojarzonym z bieżącą subskrypcją.</span><span class="sxs-lookup"><span data-stu-id="8d918-252">This user principal name must exist in the directory associated with the current subscription.</span></span>

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

### <span data-ttu-id="8d918-253">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="8d918-253">-VaultName</span></span>
<span data-ttu-id="8d918-254">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="8d918-254">Specifies the name of a key vault.</span></span>
<span data-ttu-id="8d918-255">To polecenie cmdlet modyfikuje zasady dostępu dla magazynu kluczy określanego przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="8d918-255">This cmdlet modifies the access policy for the key vault that this parameter specifies.</span></span>

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

### <span data-ttu-id="8d918-256">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8d918-256">-Confirm</span></span>
<span data-ttu-id="8d918-257">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d918-257">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d918-258">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d918-258">-WhatIf</span></span>
<span data-ttu-id="8d918-259">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d918-259">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8d918-260">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8d918-260">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d918-261">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d918-261">CommonParameters</span></span>
<span data-ttu-id="8d918-262">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d918-262">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d918-263">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d918-263">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d918-264">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8d918-264">INPUTS</span></span>

### <span data-ttu-id="8d918-265">Microsoft. Azure. Commands. platforming. models. PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="8d918-265">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>
<span data-ttu-id="8d918-266">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8d918-266">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="8d918-267">System. String</span><span class="sxs-lookup"><span data-stu-id="8d918-267">System.String</span></span>

## <span data-ttu-id="8d918-268">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8d918-268">OUTPUTS</span></span>

### <span data-ttu-id="8d918-269">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="8d918-269">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="8d918-270">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8d918-270">NOTES</span></span>

## <span data-ttu-id="8d918-271">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8d918-271">RELATED LINKS</span></span>

[<span data-ttu-id="8d918-272">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="8d918-272">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="8d918-273">Remove-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8d918-273">Remove-AzureRmKeyVaultAccessPolicy</span></span>](./Remove-AzureRmKeyVaultAccessPolicy.md)
