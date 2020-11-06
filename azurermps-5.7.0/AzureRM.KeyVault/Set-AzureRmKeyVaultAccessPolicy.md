---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 636FAD5B-8C39-4E5C-8978-6845C6B89BC0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurermkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureRmKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureRmKeyVaultAccessPolicy.md
ms.openlocfilehash: 20a36e35c509ecca889d4059bd7e74ccafa22dc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542548"
---
# <span data-ttu-id="1ef26-101">Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1ef26-101">Set-AzureRmKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="1ef26-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1ef26-102">SYNOPSIS</span></span>
<span data-ttu-id="1ef26-103">Udziela lub modyfikuje istniejące uprawnienia dla użytkownika, aplikacji lub grupy zabezpieczeń w celu wykonania operacji za pomocą magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="1ef26-103">Grants or modifies existing permissions for a user, application, or security group to perform operations with a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ef26-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1ef26-104">SYNTAX</span></span>

### <span data-ttu-id="1ef26-105">ByUserPrincipalName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1ef26-105">ByUserPrincipalName (Default)</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -UserPrincipalName <String> [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ef26-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="1ef26-106">ByObjectId</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ef26-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="1ef26-107">ByServicePrincipalName</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ef26-108">ByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="1ef26-108">ByEmailAddress</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1ef26-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="1ef26-109">ForVault</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ef26-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="1ef26-110">InputObjectByObjectId</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ef26-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="1ef26-111">InputObjectByServicePrincipalName</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1ef26-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="1ef26-112">InputObjectByUserPrincipalName</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1ef26-113">InputObjectByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="1ef26-113">InputObjectByEmailAddress</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1ef26-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="1ef26-114">InputObjectForVault</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ef26-115">Opis</span><span class="sxs-lookup"><span data-stu-id="1ef26-115">DESCRIPTION</span></span>
<span data-ttu-id="1ef26-116">Polecenie cmdlet **Set-AzureRmKeyVaultAccessPolicy** udziela lub modyfikuje istniejące uprawnienia dla użytkownika, aplikacji lub grupy zabezpieczeń w celu wykonania określonych operacji w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="1ef26-116">The **Set-AzureRmKeyVaultAccessPolicy** cmdlet grants or modifies existing permissions for a user, application, or security group to perform the specified operations with a key vault.</span></span> <span data-ttu-id="1ef26-117">W magazynie kluczy nie są modyfikowane uprawnienia innych użytkowników, aplikacji ani grup zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="1ef26-117">It does not modify the permissions that other users, applications, or security groups have on the key vault.</span></span>

<span data-ttu-id="1ef26-118">Jeśli ustawiasz uprawnienia dla grupy zabezpieczeń, ta operacja będzie miała wpływ tylko na użytkowników tej grupy zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="1ef26-118">If you are setting permissions for a security group, this operation affects only users in that security group.</span></span>

<span data-ttu-id="1ef26-119">Wszystkie następujące katalogi muszą być tego samego katalogu platformy Azure:</span><span class="sxs-lookup"><span data-stu-id="1ef26-119">The following directories must all be the same Azure directory:</span></span> 
- <span data-ttu-id="1ef26-120">Katalog domyślny subskrypcji platformy Azure, w której znajduje się magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="1ef26-120">The default directory of the Azure subscription in which the key vault resides.</span></span>
- <span data-ttu-id="1ef26-121">Katalog platformy Azure zawierający użytkownika lub grupę aplikacji, do których udzielasz uprawnień.</span><span class="sxs-lookup"><span data-stu-id="1ef26-121">The Azure directory that contains the user or application group that you are granting permissions to.</span></span>

<span data-ttu-id="1ef26-122">Przykłady scenariuszy, w których te warunki nie są spełnione, a to polecenie cmdlet nie będzie działać:</span><span class="sxs-lookup"><span data-stu-id="1ef26-122">Examples of scenarios when these conditions are not met and this cmdlet will not work are:</span></span> 

- <span data-ttu-id="1ef26-123">Autoryzowanie użytkownika od innej organizacji do zarządzania magazynem kluczy.</span><span class="sxs-lookup"><span data-stu-id="1ef26-123">Authorizing a user from a different organization to manage your key vault.</span></span>
<span data-ttu-id="1ef26-124">Każda organizacja ma swój własny katalog.</span><span class="sxs-lookup"><span data-stu-id="1ef26-124">Each organization has its own directory.</span></span> 
- <span data-ttu-id="1ef26-125">Twoje konto platformy Azure ma wiele katalogów.</span><span class="sxs-lookup"><span data-stu-id="1ef26-125">Your Azure account has multiple directories.</span></span>
<span data-ttu-id="1ef26-126">Jeśli zarejestrujesz aplikację w katalogu innym niż katalog domyślny, nie możesz autoryzować tej aplikacji do korzystania z Twojego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="1ef26-126">If you register an application in a directory other than the default directory, you cannot authorize that application to use your key vault.</span></span>
<span data-ttu-id="1ef26-127">Aplikacja musi znajdować się w katalogu domyślnym.</span><span class="sxs-lookup"><span data-stu-id="1ef26-127">The application must be in the default directory.</span></span>

<span data-ttu-id="1ef26-128">Uwaga: chociaż określenie grupy zasobów jest opcjonalne dla tego polecenia cmdlet, należy to zrobić w celu uzyskania lepszej wydajności.</span><span class="sxs-lookup"><span data-stu-id="1ef26-128">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="1ef26-129">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1ef26-129">EXAMPLES</span></span>

### <span data-ttu-id="1ef26-130">Przykład 1: udzielanie uprawnień użytkownikowi dla magazynu kluczy i modyfikowanie uprawnień</span><span class="sxs-lookup"><span data-stu-id="1ef26-130">Example 1: Grant permissions to a user for a key vault and modify the permissions</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys create,import,delete,list -PermissionsToSecrets set,delete
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets set,delete,get -PassThru
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys @() -PassThru
```

<span data-ttu-id="1ef26-131">Pierwsze polecenie udziela uprawnień użytkownikowi w usłudze Azure Active Directory, PattiFuller@contoso.com Aby wykonywać operacje na kluczach i kluczach tajnych przy użyciu magazynu kluczy o nazwie Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="1ef26-131">The first command grants permissions for a user in your Azure Active Directory, PattiFuller@contoso.com, to perform operations on keys and secrets with a key vault named Contoso03Vault.</span></span>

<span data-ttu-id="1ef26-132">Drugie polecenie modyfikuje uprawnienia udzielone PattiFuller@contoso.com w pierwszym poleceniu w celu umożliwienia natychmiastowego wprowadzenia kluczy tajnych oraz ich usunięcia.</span><span class="sxs-lookup"><span data-stu-id="1ef26-132">The second command modifies the permissions that were granted to PattiFuller@contoso.com in the first command, to now allow getting secrets in addition to setting and deleting them.</span></span> <span data-ttu-id="1ef26-133">Uprawnienia do kluczowych operacji pozostają niezmienione po wykonaniu tego polecenia.</span><span class="sxs-lookup"><span data-stu-id="1ef26-133">The permissions to key operations remain unchanged after this command.</span></span> <span data-ttu-id="1ef26-134">Parametr *PassThru* powoduje, że zaktualizowany obiekt jest zwracany przez polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ef26-134">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>

<span data-ttu-id="1ef26-135">Polecenie ostatnie modyfikuje istniejące uprawnienia w PattiFuller@contoso.com celu usunięcia wszystkich uprawnień do kluczowych operacji.</span><span class="sxs-lookup"><span data-stu-id="1ef26-135">The final command further modifies the existing permissions for PattiFuller@contoso.com to remove all permissions to key operations.</span></span> <span data-ttu-id="1ef26-136">Po wykonaniu tego polecenia uprawnienia do tajnych operacji pozostają niezmienione.</span><span class="sxs-lookup"><span data-stu-id="1ef26-136">The permissions to secret operations remain unchanged after this command.</span></span> <span data-ttu-id="1ef26-137">Parametr *PassThru* powoduje, że zaktualizowany obiekt jest zwracany przez polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ef26-137">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>

### <span data-ttu-id="1ef26-138">Przykład 2: udzielanie uprawnień głównemu usłudze aplikacji w celu odczytywania i zapisywania kluczy tajnych</span><span class="sxs-lookup"><span data-stu-id="1ef26-138">Example 2: Grant permissions for an application service principal to read and write secrets</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com' -PermissionsToSecrets Get,Set
```

<span data-ttu-id="1ef26-139">To polecenie udziela uprawnień do aplikacji dla magazynu kluczy o nazwie Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="1ef26-139">This command grants permissions for an application for a key vault named Contoso03Vault.</span></span> 

<span data-ttu-id="1ef26-140">Parametr *ServicePrincipalName* określa aplikację.</span><span class="sxs-lookup"><span data-stu-id="1ef26-140">The *ServicePrincipalName* parameter specifies the application.</span></span> <span data-ttu-id="1ef26-141">Aplikacja musi być zarejestrowana w usłudze Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1ef26-141">The application must be registered in your Azure Active Directory.</span></span> <span data-ttu-id="1ef26-142">Wartość parametru *ServicePrincipalName* musi być nazwą główną usługi aplikacji lub identyfikatorem GUID identyfikatora aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1ef26-142">The value of the *ServicePrincipalName* parameter must be either the service principal name of the application or the application ID GUID.</span></span>

<span data-ttu-id="1ef26-143">W tym przykładzie określono nazwę główną usługi http://payroll.contoso.com , a polecenie przyznaje uprawnienia aplikacji do odczytu i zapisu kluczy tajnych.</span><span class="sxs-lookup"><span data-stu-id="1ef26-143">This example specifies the service principal name http://payroll.contoso.com, and the command grants the application permissions to read and write secrets.</span></span>

### <span data-ttu-id="1ef26-144">Przykład 3: udzielanie uprawnień do aplikacji przy użyciu jej identyfikatora obiektu</span><span class="sxs-lookup"><span data-stu-id="1ef26-144">Example 3: Grant permissions for an application using its object ID</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectId 34595082-9346-41b6-8d6b-295a2808b8db -PermissionsToSecrets Get,Set
```

<span data-ttu-id="1ef26-145">To polecenie udziela uprawnień aplikacji do odczytu i zapisu kluczy tajnych.</span><span class="sxs-lookup"><span data-stu-id="1ef26-145">This command grants the application permissions to read and write secrets.</span></span>

<span data-ttu-id="1ef26-146">W tym przykładzie określono aplikację przy użyciu identyfikatora obiektu głównego usługi aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1ef26-146">This example specifies the application using the object ID of the service principal of the application.</span></span>

### <span data-ttu-id="1ef26-147">Przykład 4: udzielanie uprawnień dla głównej nazwy użytkownika</span><span class="sxs-lookup"><span data-stu-id="1ef26-147">Example 4: Grant permissions for a user principal name</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets Get,List,Set
```

<span data-ttu-id="1ef26-148">To polecenie udziela uprawnień Get, list i ustawia uprawnienia dla określonej nazwy głównej użytkownika w celu uzyskania dostępu do kluczy tajnych.</span><span class="sxs-lookup"><span data-stu-id="1ef26-148">This command grants get, list, and set permissions for the specified user principal name for access to secrets.</span></span>

### <span data-ttu-id="1ef26-149">Przykład 5: Włączanie kluczy tajnych do pobrania z magazynu kluczy przez firmę Microsoft. Oblicz dostawcę zasobów</span><span class="sxs-lookup"><span data-stu-id="1ef26-149">Example 5: Enable secrets to be retrieved from a key vault by the Microsoft.Compute resource provider</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="1ef26-150">To polecenie udziela uprawnień do pobierania kluczy tajnych z magazynu kluczy Contoso03Vault przez dostawcę Microsoft. COMPUTE Resource.</span><span class="sxs-lookup"><span data-stu-id="1ef26-150">This command grants the permissions for secrets to be retrieved from the Contoso03Vault key vault by the Microsoft.Compute resource provider.</span></span>

### <span data-ttu-id="1ef26-151">Przykład 6: udzielanie uprawnień grupie zabezpieczeń</span><span class="sxs-lookup"><span data-stu-id="1ef26-151">Example 6: Grant permissions to a security group</span></span>
```
PS C:\>Get-AzureRmADGroup
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'myownvault' -ObjectId (Get-AzureRmADGroup -SearchString 'group2')[0].Id -PermissionsToKeys All -PermissionsToSecrets All
DisplayName                    Type                           ObjectId
-----------                    ----                           --------
group1                                                        96a0daa6-9841-4a9c-bdeb-e7062276c688
group2                                                        b8a401eb-63ad-4a30-b0e1-a7461969fe54
group3                                                        da07a6be-2c1e-4e42-934d-ceb57cf652b4
```

<span data-ttu-id="1ef26-152">W pierwszym poleceniu jest używane polecenie cmdlet Get-AzureRmADGroup, aby uzyskać dostęp do wszystkich grup usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1ef26-152">The first command uses the Get-AzureRmADGroup cmdlet to get all Active Directory groups.</span></span> <span data-ttu-id="1ef26-153">Na podstawie wyników są wyświetlane 3 grupy zwrócone, nazwane **grupa1** , **group2** oraz **Group3**.</span><span class="sxs-lookup"><span data-stu-id="1ef26-153">From the output, you see 3 groups returned, named **group1** , **group2** , and **group3**.</span></span> <span data-ttu-id="1ef26-154">Wiele grup może mieć taką samą nazwę, ale zawsze mają unikatowy identyfikator ObjectId.</span><span class="sxs-lookup"><span data-stu-id="1ef26-154">Multiple groups can have the same name but always have a unique ObjectId.</span></span> <span data-ttu-id="1ef26-155">Gdy jest zwracana więcej niż jedna grupa o takiej samej nazwie, użyj identyfikatora ObjectId w wynikach, aby zidentyfikować odpowiedni element.</span><span class="sxs-lookup"><span data-stu-id="1ef26-155">When more than one group that has the same name is returned, use the ObjectId in the output to identify the one you want to use.</span></span>

<span data-ttu-id="1ef26-156">Następnie należy użyć tego polecenia z Set-AzureRmKeyVaultAccessPolicy, aby udzielić uprawnień group2 dla magazynu kluczy o nazwie **myownvault**.</span><span class="sxs-lookup"><span data-stu-id="1ef26-156">You then use the output of this command with Set-AzureRmKeyVaultAccessPolicy to grant permissions to group2 for your key vault, named **myownvault**.</span></span> <span data-ttu-id="1ef26-157">W tym przykładzie są wyliczane grupy o nazwie "group2" w tym samym wierszu polecenia.</span><span class="sxs-lookup"><span data-stu-id="1ef26-157">This example enumerates the groups named 'group2' inline in the same command line.</span></span>

<span data-ttu-id="1ef26-158">Na zwróconej liście może być wiele grup o nazwie "group2".</span><span class="sxs-lookup"><span data-stu-id="1ef26-158">There may be multiple groups in the returned list that are named 'group2'.</span></span>
<span data-ttu-id="1ef26-159">W tym przykładzie wybierany jest pierwszy z nich, wskazany indeksem \[ 0 \] na liście zwróconej.</span><span class="sxs-lookup"><span data-stu-id="1ef26-159">This example picks the first one, indicated by index \[0\] in the returned list.</span></span>

### <span data-ttu-id="1ef26-160">Przykład 7: udzielanie dostępu do usługi Azure Information Protection do klucza dzierżawy zarządzanego przez klienta (BYOK)</span><span class="sxs-lookup"><span data-stu-id="1ef26-160">Example 7: Grant Azure Information Protection access to the customer-managed tenant key (BYOK)</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso04Vault' -ServicePrincipalName 00000012-0000-0000-c000-000000000000 -PermissionsToKeys decrypt,sign,get
```

<span data-ttu-id="1ef26-161">To polecenie upoważnia ochronę informacji platformy Azure do korzystania z klucza zarządzanego przez klienta (w celu skorzystania z własnego klucza lub scenariusza "BYOK") jako klucza dzierżawy usługi Azure Information Protection.</span><span class="sxs-lookup"><span data-stu-id="1ef26-161">This command authorizes Azure Information Protection to use a customer-managed key (the bring your own key, or "BYOK" scenario) as the Azure Information Protection tenant key.</span></span>

<span data-ttu-id="1ef26-162">Po uruchomieniu tego polecenia określ własną nazwę magazynu kluczy, ale musisz określić parametr *ServicePrincipalName* z identyfikatorem GUID **00000012-0000-0000-C000-000000000000** i określ uprawnienia w przykładzie.</span><span class="sxs-lookup"><span data-stu-id="1ef26-162">When you run this command, specify your own key vault name but you must specify the *ServicePrincipalName* parameter with the GUID **00000012-0000-0000-c000-000000000000** and specify the permissions in the example.</span></span>

## <span data-ttu-id="1ef26-163">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1ef26-163">PARAMETERS</span></span>

### <span data-ttu-id="1ef26-164">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="1ef26-164">-ApplicationId</span></span>
<span data-ttu-id="1ef26-165">Do użytku w przyszłości.</span><span class="sxs-lookup"><span data-stu-id="1ef26-165">For future use.</span></span>

```yaml
Type: Guid
Parameter Sets: ByObjectId, InputObjectByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ef26-166">-BypassObjectIdValidation</span><span class="sxs-lookup"><span data-stu-id="1ef26-166">-BypassObjectIdValidation</span></span>
<span data-ttu-id="1ef26-167">Umożliwia określenie identyfikatora obiektu bez sprawdzania, czy obiekt istnieje w usłudze Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1ef26-167">Enables you to specify an object ID without validating that the object exists in Azure Active Directory.</span></span>

<span data-ttu-id="1ef26-168">Tego parametru należy używać tylko wtedy, gdy użytkownik chce udzielić dostępu do magazynu kluczy do identyfikatora obiektu, który odwołuje się do delegowanej grupy zabezpieczeń z innej dzierżawy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1ef26-168">Use this parameter only if you want to grant access to your key vault to an object ID that refers to a delegated security group from another Azure tenant.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByObjectId, InputObjectByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ef26-169">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ef26-169">-DefaultProfile</span></span>
<span data-ttu-id="1ef26-170">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="1ef26-170">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ef26-171">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="1ef26-171">-EmailAddress</span></span>
<span data-ttu-id="1ef26-172">Określa adres e-mail użytkownika, któremu chcesz udzielić uprawnień.</span><span class="sxs-lookup"><span data-stu-id="1ef26-172">Specifies the user email address of the user to whom to grant permissions.</span></span>

<span data-ttu-id="1ef26-173">Ten adres e-mail musi znajdować się w katalogu skojarzonym z bieżącą subskrypcją i być unikatowy.</span><span class="sxs-lookup"><span data-stu-id="1ef26-173">This email address must exist in the directory associated with the current subscription and be unique.</span></span>

```yaml
Type: String
Parameter Sets: ByEmailAddress, InputObjectByEmailAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ef26-174">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="1ef26-174">-EnabledForDeployment</span></span>
<span data-ttu-id="1ef26-175">Umożliwia dostawcy zasobów Microsoft. COMPUTE na pobieranie kluczy tajnych z tego magazynu kluczy, gdy do tego magazynu kluczy odwołuje się tworzenie zasobów, na przykład podczas tworzenia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1ef26-175">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault, InputObjectForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ef26-176">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="1ef26-176">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="1ef26-177">Umożliwia usłudze szyfrowania dysków Azure uzyskiwanie kluczy tajnych i ich odwinięcie z tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="1ef26-177">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault, InputObjectForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ef26-178">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="1ef26-178">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="1ef26-179">Umożliwia menedżerowi zasobów platformy Azure pobieranie kluczy tajnych z tego magazynu kluczy, gdy do tego magazynu kluczy odwołuje się wdrożenie szablonu.</span><span class="sxs-lookup"><span data-stu-id="1ef26-179">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault, InputObjectForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ef26-180">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1ef26-180">-InputObject</span></span>
<span data-ttu-id="1ef26-181">Obiekt magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="1ef26-181">Key Vault Object</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, InputObjectForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ef26-182">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="1ef26-182">-ObjectId</span></span>
<span data-ttu-id="1ef26-183">Określa identyfikator obiektu podmiotu użytkownika lub usługi w usłudze Azure Active Directory, dla którego ma zostać udzielone uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="1ef26-183">Specifies the object ID of the user or service principal in Azure Active Directory for which to grant permissions.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectId, InputObjectByObjectId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ef26-184">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1ef26-184">-PassThru</span></span>
<span data-ttu-id="1ef26-185">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="1ef26-185">Returns an object representing the item with which you are working.</span></span>

<span data-ttu-id="1ef26-186">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="1ef26-186">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ef26-187">-PermissionsToCertificates</span><span class="sxs-lookup"><span data-stu-id="1ef26-187">-PermissionsToCertificates</span></span>
<span data-ttu-id="1ef26-188">Określa tablicę uprawnień certyfikatów, które mają zostać udzielone użytkownikowi lub podmiotowi zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="1ef26-188">Specifies an array of certificate permissions to grant to a user or service principal.</span></span>

<span data-ttu-id="1ef26-189">Dopuszczalne wartości dla tego parametru:</span><span class="sxs-lookup"><span data-stu-id="1ef26-189">The acceptable values for this parameter:</span></span>

- <span data-ttu-id="1ef26-190">Pobierz</span><span class="sxs-lookup"><span data-stu-id="1ef26-190">Get</span></span>
- <span data-ttu-id="1ef26-191">Lista</span><span class="sxs-lookup"><span data-stu-id="1ef26-191">List</span></span>
- <span data-ttu-id="1ef26-192">Usuwać</span><span class="sxs-lookup"><span data-stu-id="1ef26-192">Delete</span></span>
- <span data-ttu-id="1ef26-193">Tworzonych</span><span class="sxs-lookup"><span data-stu-id="1ef26-193">Create</span></span>
- <span data-ttu-id="1ef26-194">Przywoz</span><span class="sxs-lookup"><span data-stu-id="1ef26-194">Import</span></span>
- <span data-ttu-id="1ef26-195">Aktualizowane</span><span class="sxs-lookup"><span data-stu-id="1ef26-195">Update</span></span>
- <span data-ttu-id="1ef26-196">Managecontacts</span><span class="sxs-lookup"><span data-stu-id="1ef26-196">Managecontacts</span></span>
- <span data-ttu-id="1ef26-197">Emitenci</span><span class="sxs-lookup"><span data-stu-id="1ef26-197">Getissuers</span></span>
- <span data-ttu-id="1ef26-198">Listissuers</span><span class="sxs-lookup"><span data-stu-id="1ef26-198">Listissuers</span></span>
- <span data-ttu-id="1ef26-199">Autoemitenci</span><span class="sxs-lookup"><span data-stu-id="1ef26-199">Setissuers</span></span>
- <span data-ttu-id="1ef26-200">Deleteissuers</span><span class="sxs-lookup"><span data-stu-id="1ef26-200">Deleteissuers</span></span>
- <span data-ttu-id="1ef26-201">Manageissuers</span><span class="sxs-lookup"><span data-stu-id="1ef26-201">Manageissuers</span></span>

```yaml
Type: String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress
Aliases:
Accepted values: get, list, delete, create, import, update, managecontacts, getissuers, listissuers, setissuers, deleteissuers, manageissuers, recover, purge, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ef26-202">-PermissionsToKeys</span><span class="sxs-lookup"><span data-stu-id="1ef26-202">-PermissionsToKeys</span></span>
<span data-ttu-id="1ef26-203">Określa tablicę uprawnień kluczowych operacji, które mają zostać udzielone użytkownikowi lub podmiotowi zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="1ef26-203">Specifies an array of key operation permissions to grant to a user or service principal.</span></span>

<span data-ttu-id="1ef26-204">Dopuszczalne wartości dla tego parametru:</span><span class="sxs-lookup"><span data-stu-id="1ef26-204">The acceptable values for this parameter:</span></span>

- <span data-ttu-id="1ef26-205">Szyfruj</span><span class="sxs-lookup"><span data-stu-id="1ef26-205">Decrypt</span></span>
- <span data-ttu-id="1ef26-206">Szyfrowane</span><span class="sxs-lookup"><span data-stu-id="1ef26-206">Encrypt</span></span>
- <span data-ttu-id="1ef26-207">UnwrapKey</span><span class="sxs-lookup"><span data-stu-id="1ef26-207">UnwrapKey</span></span>
- <span data-ttu-id="1ef26-208">WrapKey</span><span class="sxs-lookup"><span data-stu-id="1ef26-208">WrapKey</span></span>
- <span data-ttu-id="1ef26-209">Sprawdzić</span><span class="sxs-lookup"><span data-stu-id="1ef26-209">Verify</span></span>
- <span data-ttu-id="1ef26-210">Zapisywania</span><span class="sxs-lookup"><span data-stu-id="1ef26-210">Sign</span></span>
- <span data-ttu-id="1ef26-211">Pobierz</span><span class="sxs-lookup"><span data-stu-id="1ef26-211">Get</span></span>
- <span data-ttu-id="1ef26-212">Lista</span><span class="sxs-lookup"><span data-stu-id="1ef26-212">List</span></span>
- <span data-ttu-id="1ef26-213">Aktualizowane</span><span class="sxs-lookup"><span data-stu-id="1ef26-213">Update</span></span>
- <span data-ttu-id="1ef26-214">Tworzonych</span><span class="sxs-lookup"><span data-stu-id="1ef26-214">Create</span></span>
- <span data-ttu-id="1ef26-215">Przywoz</span><span class="sxs-lookup"><span data-stu-id="1ef26-215">Import</span></span>
- <span data-ttu-id="1ef26-216">Usuwać</span><span class="sxs-lookup"><span data-stu-id="1ef26-216">Delete</span></span>
- <span data-ttu-id="1ef26-217">Wykonania</span><span class="sxs-lookup"><span data-stu-id="1ef26-217">Backup</span></span>
- <span data-ttu-id="1ef26-218">Przywrócenie</span><span class="sxs-lookup"><span data-stu-id="1ef26-218">Restore</span></span>
- <span data-ttu-id="1ef26-219">Odzyskiwanie</span><span class="sxs-lookup"><span data-stu-id="1ef26-219">Recover</span></span>
- <span data-ttu-id="1ef26-220">Wyczyścić</span><span class="sxs-lookup"><span data-stu-id="1ef26-220">Purge</span></span>

```yaml
Type: String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress
Aliases:
Accepted values: decrypt, encrypt, unwrapKey, wrapKey, verify, sign, get, list, update, create, import, delete, backup, restore, recover, purge, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ef26-221">-PermissionsToSecrets</span><span class="sxs-lookup"><span data-stu-id="1ef26-221">-PermissionsToSecrets</span></span>
<span data-ttu-id="1ef26-222">Określa tablicę uprawnień do tajnego działania, które mają zostać udzielone użytkownikowi lub podmiotowi zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="1ef26-222">Specifies an array of secret operation permissions to grant to a user or service principal.</span></span>

<span data-ttu-id="1ef26-223">Dopuszczalne wartości dla tego parametru:</span><span class="sxs-lookup"><span data-stu-id="1ef26-223">The acceptable values for this parameter:</span></span>

- <span data-ttu-id="1ef26-224">Pobierz</span><span class="sxs-lookup"><span data-stu-id="1ef26-224">Get</span></span>
- <span data-ttu-id="1ef26-225">Lista</span><span class="sxs-lookup"><span data-stu-id="1ef26-225">List</span></span>
- <span data-ttu-id="1ef26-226">Ustawić</span><span class="sxs-lookup"><span data-stu-id="1ef26-226">Set</span></span>
- <span data-ttu-id="1ef26-227">Usuwać</span><span class="sxs-lookup"><span data-stu-id="1ef26-227">Delete</span></span>
- <span data-ttu-id="1ef26-228">Wykonania</span><span class="sxs-lookup"><span data-stu-id="1ef26-228">Backup</span></span>
- <span data-ttu-id="1ef26-229">Przywrócenie</span><span class="sxs-lookup"><span data-stu-id="1ef26-229">Restore</span></span>
- <span data-ttu-id="1ef26-230">Odzyskiwanie</span><span class="sxs-lookup"><span data-stu-id="1ef26-230">Recover</span></span>
- <span data-ttu-id="1ef26-231">Wyczyścić</span><span class="sxs-lookup"><span data-stu-id="1ef26-231">Purge</span></span>

```yaml
Type: String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress
Aliases:
Accepted values: get, list, set, delete, backup, restore, recover, purge, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ef26-232">-PermissionsToStorage</span><span class="sxs-lookup"><span data-stu-id="1ef26-232">-PermissionsToStorage</span></span>
<span data-ttu-id="1ef26-233">Określa zarządzane konto magazynu i uprawnienia operacji definicji SaS, które mają zostać udzielone użytkownikowi lub podmiotowi zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="1ef26-233">Specifies managed storage account and SaS-definition operation permissions to grant to a user or service principal.</span></span>

```yaml
Type: String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress
Aliases:
Accepted values: get, list, delete, set, update, regeneratekey, getsas, listsas, deletesas, setsas, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ef26-234">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ef26-234">-ResourceGroupName</span></span>
<span data-ttu-id="1ef26-235">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1ef26-235">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, ForVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ef26-236">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="1ef26-236">-ServicePrincipalName</span></span>
<span data-ttu-id="1ef26-237">Określa główną nazwę usługi aplikacji, do której mają być udzielane uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="1ef26-237">Specifies the service principal name of the application to which to grant permissions.</span></span>

<span data-ttu-id="1ef26-238">Określ identyfikator aplikacji, określany także jako identyfikator klienta, zarejestrowany dla aplikacji w katalogu AzureActive.</span><span class="sxs-lookup"><span data-stu-id="1ef26-238">Specify the application ID, also known as client ID, registered for the application in AzureActive Directory.</span></span> <span data-ttu-id="1ef26-239">Aplikacja o głównej nazwie usługi, którą ten parametr określa, musi być zarejestrowana w katalogu platformy Azure, który zawiera bieżący abonament.</span><span class="sxs-lookup"><span data-stu-id="1ef26-239">The application with the service principal name that this parameter specifies must be registered in the Azure directory that contains your current subscription.</span></span>

```yaml
Type: String
Parameter Sets: ByServicePrincipalName, InputObjectByServicePrincipalName
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ef26-240">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="1ef26-240">-UserPrincipalName</span></span>
<span data-ttu-id="1ef26-241">Określa główną nazwę użytkownika, któremu chcesz udzielić uprawnień.</span><span class="sxs-lookup"><span data-stu-id="1ef26-241">Specifies the user principal name of the user to whom to grant permissions.</span></span>

<span data-ttu-id="1ef26-242">Ta główna nazwa użytkownika musi istnieć w katalogu skojarzonym z bieżącą subskrypcją.</span><span class="sxs-lookup"><span data-stu-id="1ef26-242">This user principal name must exist in the directory associated with the current subscription.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName, InputObjectByUserPrincipalName
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ef26-243">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="1ef26-243">-VaultName</span></span>
<span data-ttu-id="1ef26-244">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="1ef26-244">Specifies the name of a key vault.</span></span>

<span data-ttu-id="1ef26-245">To polecenie cmdlet modyfikuje zasady dostępu dla magazynu kluczy określanego przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="1ef26-245">This cmdlet modifies the access policy for the key vault that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, ForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ef26-246">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1ef26-246">-Confirm</span></span>
<span data-ttu-id="1ef26-247">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ef26-247">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ef26-248">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ef26-248">-WhatIf</span></span>
<span data-ttu-id="1ef26-249">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ef26-249">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1ef26-250">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1ef26-250">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ef26-251">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ef26-251">CommonParameters</span></span>
<span data-ttu-id="1ef26-252">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ef26-252">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ef26-253">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ef26-253">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ef26-254">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1ef26-254">INPUTS</span></span>

### <span data-ttu-id="1ef26-255">String, GUID, String [], przełącznik</span><span class="sxs-lookup"><span data-stu-id="1ef26-255">String, Guid, String[], Switch</span></span>

## <span data-ttu-id="1ef26-256">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1ef26-256">OUTPUTS</span></span>

### <span data-ttu-id="1ef26-257">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="1ef26-257">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="1ef26-258">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1ef26-258">NOTES</span></span>

## <span data-ttu-id="1ef26-259">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1ef26-259">RELATED LINKS</span></span>

[<span data-ttu-id="1ef26-260">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="1ef26-260">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="1ef26-261">Remove-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1ef26-261">Remove-AzureRmKeyVaultAccessPolicy</span></span>](./Remove-AzureRmKeyVaultAccessPolicy.md)

