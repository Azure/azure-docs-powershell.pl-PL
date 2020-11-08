---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 636FAD5B-8C39-4E5C-8978-6845C6B89BC0
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/set-Azkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
ms.openlocfilehash: a774c438f9be25dc55f48c5121031956374a2cb7
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/08/2020
ms.locfileid: "94061839"
---
# <span data-ttu-id="bef52-101">Set-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="bef52-101">Set-AzKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="bef52-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bef52-102">SYNOPSIS</span></span>
<span data-ttu-id="bef52-103">Udziela lub modyfikuje istniejące uprawnienia dla użytkownika, aplikacji lub grupy zabezpieczeń w celu wykonania operacji za pomocą magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="bef52-103">Grants or modifies existing permissions for a user, application, or security group to perform operations with a key vault.</span></span>

## <span data-ttu-id="bef52-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bef52-104">SYNTAX</span></span>

### <span data-ttu-id="bef52-105">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="bef52-105">ByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bef52-106">ByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="bef52-106">ByUserPrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -UserPrincipalName <String> [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bef52-107">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="bef52-107">ByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bef52-108">ByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="bef52-108">ByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bef52-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="bef52-109">ForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bef52-110">Opis</span><span class="sxs-lookup"><span data-stu-id="bef52-110">DESCRIPTION</span></span>
<span data-ttu-id="bef52-111">Polecenie cmdlet **Set-AzKeyVaultAccessPolicy** udziela lub modyfikuje istniejące uprawnienia dla użytkownika, aplikacji lub grupy zabezpieczeń w celu wykonania określonych operacji w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="bef52-111">The **Set-AzKeyVaultAccessPolicy** cmdlet grants or modifies existing permissions for a user, application, or security group to perform the specified operations with a key vault.</span></span> <span data-ttu-id="bef52-112">W magazynie kluczy nie są modyfikowane uprawnienia innych użytkowników, aplikacji ani grup zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="bef52-112">It does not modify the permissions that other users, applications, or security groups have on the key vault.</span></span>

<span data-ttu-id="bef52-113">Jeśli ustawiasz uprawnienia dla grupy zabezpieczeń, ta operacja będzie miała wpływ tylko na użytkowników tej grupy zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="bef52-113">If you are setting permissions for a security group, this operation affects only users in that security group.</span></span>

<span data-ttu-id="bef52-114">Wszystkie następujące katalogi muszą być tego samego katalogu platformy Azure:</span><span class="sxs-lookup"><span data-stu-id="bef52-114">The following directories must all be the same Azure directory:</span></span>
- <span data-ttu-id="bef52-115">Katalog domyślny subskrypcji platformy Azure, w której znajduje się magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="bef52-115">The default directory of the Azure subscription in which the key vault resides.</span></span>
- <span data-ttu-id="bef52-116">Katalog platformy Azure zawierający użytkownika lub grupę aplikacji, do których udzielasz uprawnień.</span><span class="sxs-lookup"><span data-stu-id="bef52-116">The Azure directory that contains the user or application group that you are granting permissions to.</span></span>

<span data-ttu-id="bef52-117">Przykłady scenariuszy, w których te warunki nie są spełnione, a to polecenie cmdlet nie będzie działać:</span><span class="sxs-lookup"><span data-stu-id="bef52-117">Examples of scenarios when these conditions are not met and this cmdlet will not work are:</span></span>

- <span data-ttu-id="bef52-118">Autoryzowanie użytkownika od innej organizacji do zarządzania magazynem kluczy.</span><span class="sxs-lookup"><span data-stu-id="bef52-118">Authorizing a user from a different organization to manage your key vault.</span></span>
<span data-ttu-id="bef52-119">Każda organizacja ma swój własny katalog.</span><span class="sxs-lookup"><span data-stu-id="bef52-119">Each organization has its own directory.</span></span>
- <span data-ttu-id="bef52-120">Twoje konto platformy Azure ma wiele katalogów.</span><span class="sxs-lookup"><span data-stu-id="bef52-120">Your Azure account has multiple directories.</span></span>
<span data-ttu-id="bef52-121">Jeśli zarejestrujesz aplikację w katalogu innym niż katalog domyślny, nie możesz autoryzować tej aplikacji do korzystania z Twojego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="bef52-121">If you register an application in a directory other than the default directory, you cannot authorize that application to use your key vault.</span></span>
<span data-ttu-id="bef52-122">Aplikacja musi znajdować się w katalogu domyślnym.</span><span class="sxs-lookup"><span data-stu-id="bef52-122">The application must be in the default directory.</span></span>

<span data-ttu-id="bef52-123">Uwaga: chociaż określenie grupy zasobów jest opcjonalne dla tego polecenia cmdlet, należy to zrobić w celu uzyskania lepszej wydajności.</span><span class="sxs-lookup"><span data-stu-id="bef52-123">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="bef52-124">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bef52-124">EXAMPLES</span></span>

### <span data-ttu-id="bef52-125">Przykład 1: udzielanie uprawnień użytkownikowi dla magazynu kluczy i modyfikowanie uprawnień</span><span class="sxs-lookup"><span data-stu-id="bef52-125">Example 1: Grant permissions to a user for a key vault and modify the permissions</span></span>
```
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys create,import,delete,list -PermissionsToSecrets set,delete
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets set,delete,get -PassThru
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys @() -PassThru
```

<span data-ttu-id="bef52-126">Pierwsze polecenie udziela uprawnień użytkownikowi w usłudze Azure Active Directory, PattiFuller@contoso.com Aby wykonywać operacje na kluczach i kluczach tajnych przy użyciu magazynu kluczy o nazwie Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="bef52-126">The first command grants permissions for a user in your Azure Active Directory, PattiFuller@contoso.com, to perform operations on keys and secrets with a key vault named Contoso03Vault.</span></span>

<span data-ttu-id="bef52-127">Drugie polecenie modyfikuje uprawnienia udzielone PattiFuller@contoso.com w pierwszym poleceniu w celu umożliwienia natychmiastowego wprowadzenia kluczy tajnych oraz ich usunięcia.</span><span class="sxs-lookup"><span data-stu-id="bef52-127">The second command modifies the permissions that were granted to PattiFuller@contoso.com in the first command, to now allow getting secrets in addition to setting and deleting them.</span></span> <span data-ttu-id="bef52-128">Uprawnienia do kluczowych operacji pozostają niezmienione po wykonaniu tego polecenia.</span><span class="sxs-lookup"><span data-stu-id="bef52-128">The permissions to key operations remain unchanged after this command.</span></span> <span data-ttu-id="bef52-129">Parametr *PassThru* powoduje, że zaktualizowany obiekt jest zwracany przez polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bef52-129">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>

<span data-ttu-id="bef52-130">Polecenie ostatnie modyfikuje istniejące uprawnienia w PattiFuller@contoso.com celu usunięcia wszystkich uprawnień do kluczowych operacji.</span><span class="sxs-lookup"><span data-stu-id="bef52-130">The final command further modifies the existing permissions for PattiFuller@contoso.com to remove all permissions to key operations.</span></span> <span data-ttu-id="bef52-131">Po wykonaniu tego polecenia uprawnienia do tajnych operacji pozostają niezmienione.</span><span class="sxs-lookup"><span data-stu-id="bef52-131">The permissions to secret operations remain unchanged after this command.</span></span> <span data-ttu-id="bef52-132">Parametr *PassThru* powoduje, że zaktualizowany obiekt jest zwracany przez polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bef52-132">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>

### <span data-ttu-id="bef52-133">Przykład 2: udzielanie uprawnień głównemu usłudze aplikacji w celu odczytywania i zapisywania kluczy tajnych</span><span class="sxs-lookup"><span data-stu-id="bef52-133">Example 2: Grant permissions for an application service principal to read and write secrets</span></span>
```
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com' -PermissionsToSecrets Get,Set
```

<span data-ttu-id="bef52-134">To polecenie udziela uprawnień do aplikacji dla magazynu kluczy o nazwie Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="bef52-134">This command grants permissions for an application for a key vault named Contoso03Vault.</span></span>

<span data-ttu-id="bef52-135">Parametr *ServicePrincipalName* określa aplikację.</span><span class="sxs-lookup"><span data-stu-id="bef52-135">The *ServicePrincipalName* parameter specifies the application.</span></span> <span data-ttu-id="bef52-136">Aplikacja musi być zarejestrowana w usłudze Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="bef52-136">The application must be registered in your Azure Active Directory.</span></span> <span data-ttu-id="bef52-137">Wartość parametru *ServicePrincipalName* musi być nazwą główną usługi aplikacji lub identyfikatorem GUID identyfikatora aplikacji.</span><span class="sxs-lookup"><span data-stu-id="bef52-137">The value of the *ServicePrincipalName* parameter must be either the service principal name of the application or the application ID GUID.</span></span>

<span data-ttu-id="bef52-138">W tym przykładzie określono nazwę główną usługi `http://payroll.contoso.com` , a polecenie przyznaje uprawnienia aplikacji do odczytu i zapisu kluczy tajnych.</span><span class="sxs-lookup"><span data-stu-id="bef52-138">This example specifies the service principal name `http://payroll.contoso.com`, and the command grants the application permissions to read and write secrets.</span></span>

### <span data-ttu-id="bef52-139">Przykład 3: udzielanie uprawnień do aplikacji przy użyciu jej identyfikatora obiektu</span><span class="sxs-lookup"><span data-stu-id="bef52-139">Example 3: Grant permissions for an application using its object ID</span></span>
```
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectId 34595082-9346-41b6-8d6b-295a2808b8db -PermissionsToSecrets Get,Set
```

<span data-ttu-id="bef52-140">To polecenie udziela uprawnień aplikacji do odczytu i zapisu kluczy tajnych.</span><span class="sxs-lookup"><span data-stu-id="bef52-140">This command grants the application permissions to read and write secrets.</span></span>

<span data-ttu-id="bef52-141">W tym przykładzie określono aplikację przy użyciu identyfikatora obiektu głównego usługi aplikacji.</span><span class="sxs-lookup"><span data-stu-id="bef52-141">This example specifies the application using the object ID of the service principal of the application.</span></span>

### <span data-ttu-id="bef52-142">Przykład 4: udzielanie uprawnień dla głównej nazwy użytkownika</span><span class="sxs-lookup"><span data-stu-id="bef52-142">Example 4: Grant permissions for a user principal name</span></span>
```
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets Get,List,Set
```

<span data-ttu-id="bef52-143">To polecenie udziela uprawnień Get, list i ustawia uprawnienia dla określonej nazwy głównej użytkownika w celu uzyskania dostępu do kluczy tajnych.</span><span class="sxs-lookup"><span data-stu-id="bef52-143">This command grants get, list, and set permissions for the specified user principal name for access to secrets.</span></span>

### <span data-ttu-id="bef52-144">Przykład 5: Włączanie kluczy tajnych do pobrania z magazynu kluczy przez firmę Microsoft. Obliczanie dostawcy zasobów</span><span class="sxs-lookup"><span data-stu-id="bef52-144">Example 5: Enable secrets to be retrieved from a key vault vault by the Microsoft.Compute resource provider</span></span>
```
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="bef52-145">To polecenie udziela uprawnień do pobierania kluczy tajnych z magazynu kluczy Contoso03Vault przez dostawcę Microsoft. COMPUTE Resource.</span><span class="sxs-lookup"><span data-stu-id="bef52-145">This command grants the permissions for secrets to be retrieved from the Contoso03Vault key vault by the Microsoft.Compute resource provider.</span></span>

### <span data-ttu-id="bef52-146">Przykład 6: udzielanie uprawnień grupie zabezpieczeń</span><span class="sxs-lookup"><span data-stu-id="bef52-146">Example 6: Grant permissions to a security group</span></span>
```
PS C:\>Get-AzADGroup
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'myownvault' -ObjectId (Get-AzADGroup -SearchString 'group2')[0].Id -PermissionsToKeys All -PermissionsToSecrets All
DisplayName                    Type                           ObjectId
-----------                    ----                           --------
group1                                                        96a0daa6-9841-4a9c-bdeb-e7062276c688
group2                                                        b8a401eb-63ad-4a30-b0e1-a7461969fe54
group3                                                        da07a6be-2c1e-4e42-934d-ceb57cf652b4
```

<span data-ttu-id="bef52-147">W pierwszym poleceniu jest używane polecenie cmdlet Get-AzADGroup, aby uzyskać dostęp do wszystkich grup usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="bef52-147">The first command uses the Get-AzADGroup cmdlet to get all Active Directory groups.</span></span> <span data-ttu-id="bef52-148">Na podstawie wyników są wyświetlane 3 grupy zwrócone, nazwane **grupa1** , **group2** oraz **Group3**.</span><span class="sxs-lookup"><span data-stu-id="bef52-148">From the output, you see 3 groups returned, named **group1** , **group2** , and **group3**.</span></span> <span data-ttu-id="bef52-149">Wiele grup może mieć taką samą nazwę, ale zawsze mają unikatowy identyfikator ObjectId.</span><span class="sxs-lookup"><span data-stu-id="bef52-149">Multiple groups can have the same name but always have a unique ObjectId.</span></span> <span data-ttu-id="bef52-150">Gdy jest zwracana więcej niż jedna grupa o takiej samej nazwie, użyj identyfikatora ObjectId w wynikach, aby zidentyfikować odpowiedni element.</span><span class="sxs-lookup"><span data-stu-id="bef52-150">When more than one group that has the same name is returned, use the ObjectId in the output to identify the one you want to use.</span></span>

<span data-ttu-id="bef52-151">Następnie należy użyć tego polecenia z Set-AzKeyVaultAccessPolicy, aby udzielić uprawnień group2 dla magazynu kluczy o nazwie **myownvault**.</span><span class="sxs-lookup"><span data-stu-id="bef52-151">You then use the output of this command with Set-AzKeyVaultAccessPolicy to grant permissions to group2 for your key vault, named **myownvault**.</span></span> <span data-ttu-id="bef52-152">W tym przykładzie są wyliczane grupy o nazwie "group2" w tym samym wierszu polecenia.</span><span class="sxs-lookup"><span data-stu-id="bef52-152">This example enumerates the groups named 'group2' inline in the same command line.</span></span>

<span data-ttu-id="bef52-153">Na zwróconej liście może być wiele grup o nazwie "group2".</span><span class="sxs-lookup"><span data-stu-id="bef52-153">There may be multiple groups in the returned list that are named 'group2'.</span></span>
<span data-ttu-id="bef52-154">W tym przykładzie wybierany jest pierwszy z nich, wskazany indeksem \[ 0 \] na liście zwróconej.</span><span class="sxs-lookup"><span data-stu-id="bef52-154">This example picks the first one, indicated by index \[0\] in the returned list.</span></span>

### <span data-ttu-id="bef52-155">Przykład 7: udzielanie dostępu do usługi Azure Information Protection do klucza dzierżawy zarządzanego przez klienta (BYOK)</span><span class="sxs-lookup"><span data-stu-id="bef52-155">Example 7: Grant Azure Information Protection access to the customer-managed tenant key (BYOK)</span></span>
```
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName 'Contoso04Vault' -ServicePrincipalName 00000012-0000-0000-c000-000000000000 -PermissionsToKeys decrypt,sign,get
```

<span data-ttu-id="bef52-156">To polecenie upoważnia ochronę informacji platformy Azure do korzystania z klucza zarządzanego przez klienta (w celu skorzystania z własnego klucza lub scenariusza "BYOK") jako klucza dzierżawy usługi Azure Information Protection.</span><span class="sxs-lookup"><span data-stu-id="bef52-156">This command authorizes Azure Information Protection to use a customer-managed key (the bring your own key, or "BYOK" scenario) as the Azure Information Protection tenant key.</span></span>

<span data-ttu-id="bef52-157">Po uruchomieniu tego polecenia określ własną nazwę magazynu kluczy, ale musisz określić parametr *ServicePrincipalName* z identyfikatorem GUID **00000012-0000-0000-C000-000000000000** i określ uprawnienia w przykładzie.</span><span class="sxs-lookup"><span data-stu-id="bef52-157">When you run this command, specify your own key vault name but you must specify the *ServicePrincipalName* parameter with the GUID **00000012-0000-0000-c000-000000000000** and specify the permissions in the example.</span></span>

## <span data-ttu-id="bef52-158">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bef52-158">PARAMETERS</span></span>

### <span data-ttu-id="bef52-159">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="bef52-159">-ApplicationId</span></span>
<span data-ttu-id="bef52-160">Do użytku w przyszłości.</span><span class="sxs-lookup"><span data-stu-id="bef52-160">For future use.</span></span>

```yaml
Type: Guid
Parameter Sets: ByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bef52-161">-BypassObjectIdValidation</span><span class="sxs-lookup"><span data-stu-id="bef52-161">-BypassObjectIdValidation</span></span>
<span data-ttu-id="bef52-162">Umożliwia określenie identyfikatora obiektu bez sprawdzania, czy obiekt istnieje w usłudze Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="bef52-162">Enables you to specify an object ID without validating that the object exists in Azure Active Directory.</span></span>

<span data-ttu-id="bef52-163">Tego parametru należy używać tylko wtedy, gdy użytkownik chce udzielić dostępu do magazynu kluczy do identyfikatora obiektu, który odwołuje się do delegowanej grupy zabezpieczeń z innej dzierżawy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bef52-163">Use this parameter only if you want to grant access to your key vault to an object ID that refers to a delegated security group from another Azure tenant.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bef52-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bef52-164">-DefaultProfile</span></span>
<span data-ttu-id="bef52-165">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="bef52-165">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bef52-166">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="bef52-166">-EmailAddress</span></span>
<span data-ttu-id="bef52-167">Określa adres e-mail użytkownika, któremu chcesz udzielić uprawnień.</span><span class="sxs-lookup"><span data-stu-id="bef52-167">Specifies the user email address of the user to whom to grant permissions.</span></span>

<span data-ttu-id="bef52-168">Ten adres e-mail musi znajdować się w katalogu skojarzonym z bieżącą subskrypcją i być unikatowy.</span><span class="sxs-lookup"><span data-stu-id="bef52-168">This email address must exist in the directory associated with the current subscription and be unique.</span></span>

```yaml
Type: String
Parameter Sets: ByEmailAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bef52-169">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="bef52-169">-EnabledForDeployment</span></span>
<span data-ttu-id="bef52-170">Umożliwia dostawcy zasobów Microsoft. COMPUTE na pobieranie kluczy tajnych z tego magazynu kluczy, gdy do tego magazynu kluczy odwołuje się tworzenie zasobów, na przykład podczas tworzenia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bef52-170">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bef52-171">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="bef52-171">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="bef52-172">Umożliwia usłudze szyfrowania dysków Azure uzyskiwanie kluczy tajnych i ich odwinięcie z tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="bef52-172">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bef52-173">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="bef52-173">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="bef52-174">Umożliwia menedżerowi zasobów platformy Azure pobieranie kluczy tajnych z tego magazynu kluczy, gdy do tego magazynu kluczy odwołuje się wdrożenie szablonu.</span><span class="sxs-lookup"><span data-stu-id="bef52-174">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bef52-175">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="bef52-175">-ObjectId</span></span>
<span data-ttu-id="bef52-176">Określa identyfikator obiektu podmiotu użytkownika lub usługi w usłudze Azure Active Directory, dla którego ma zostać udzielone uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="bef52-176">Specifies the object ID of the user or service principal in Azure Active Directory for which to grant permissions.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bef52-177">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bef52-177">-PassThru</span></span>
<span data-ttu-id="bef52-178">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="bef52-178">Returns an object representing the item with which you are working.</span></span>

<span data-ttu-id="bef52-179">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="bef52-179">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="bef52-180">-PermissionsToCertificates</span><span class="sxs-lookup"><span data-stu-id="bef52-180">-PermissionsToCertificates</span></span>
<span data-ttu-id="bef52-181">Określa tablicę uprawnień certyfikatów, które mają zostać udzielone użytkownikowi lub podmiotowi zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="bef52-181">Specifies an array of certificate permissions to grant to a user or service principal.</span></span>

<span data-ttu-id="bef52-182">Dopuszczalne wartości dla tego parametru:</span><span class="sxs-lookup"><span data-stu-id="bef52-182">The acceptable values for this parameter:</span></span>

- <span data-ttu-id="bef52-183">Pobierz</span><span class="sxs-lookup"><span data-stu-id="bef52-183">Get</span></span>
- <span data-ttu-id="bef52-184">Lista</span><span class="sxs-lookup"><span data-stu-id="bef52-184">List</span></span>
- <span data-ttu-id="bef52-185">Usuwać</span><span class="sxs-lookup"><span data-stu-id="bef52-185">Delete</span></span>
- <span data-ttu-id="bef52-186">Tworzonych</span><span class="sxs-lookup"><span data-stu-id="bef52-186">Create</span></span>
- <span data-ttu-id="bef52-187">Przywoz</span><span class="sxs-lookup"><span data-stu-id="bef52-187">Import</span></span>
- <span data-ttu-id="bef52-188">Aktualizowane</span><span class="sxs-lookup"><span data-stu-id="bef52-188">Update</span></span>
- <span data-ttu-id="bef52-189">Managecontacts</span><span class="sxs-lookup"><span data-stu-id="bef52-189">Managecontacts</span></span>
- <span data-ttu-id="bef52-190">Emitenci</span><span class="sxs-lookup"><span data-stu-id="bef52-190">Getissuers</span></span>
- <span data-ttu-id="bef52-191">Listissuers</span><span class="sxs-lookup"><span data-stu-id="bef52-191">Listissuers</span></span>
- <span data-ttu-id="bef52-192">Autoemitenci</span><span class="sxs-lookup"><span data-stu-id="bef52-192">Setissuers</span></span>
- <span data-ttu-id="bef52-193">Deleteissuers</span><span class="sxs-lookup"><span data-stu-id="bef52-193">Deleteissuers</span></span>
- <span data-ttu-id="bef52-194">Manageissuers</span><span class="sxs-lookup"><span data-stu-id="bef52-194">Manageissuers</span></span>

```yaml
Type: String[]
Parameter Sets: ByServicePrincipalName, ByUserPrincipalName, ByObjectId, ByEmailAddress
Aliases:
Accepted values: get, list, delete, create, import, update, managecontacts, getissuers, listissuers, setissuers, deleteissuers, manageissuers, recover, purge, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bef52-195">-PermissionsToKeys</span><span class="sxs-lookup"><span data-stu-id="bef52-195">-PermissionsToKeys</span></span>
<span data-ttu-id="bef52-196">Określa tablicę uprawnień kluczowych operacji, które mają zostać udzielone użytkownikowi lub podmiotowi zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="bef52-196">Specifies an array of key operation permissions to grant to a user or service principal.</span></span>

<span data-ttu-id="bef52-197">Dopuszczalne wartości dla tego parametru:</span><span class="sxs-lookup"><span data-stu-id="bef52-197">The acceptable values for this parameter:</span></span>

- <span data-ttu-id="bef52-198">Szyfruj</span><span class="sxs-lookup"><span data-stu-id="bef52-198">Decrypt</span></span>
- <span data-ttu-id="bef52-199">Szyfrowane</span><span class="sxs-lookup"><span data-stu-id="bef52-199">Encrypt</span></span>
- <span data-ttu-id="bef52-200">UnwrapKey</span><span class="sxs-lookup"><span data-stu-id="bef52-200">UnwrapKey</span></span>
- <span data-ttu-id="bef52-201">WrapKey</span><span class="sxs-lookup"><span data-stu-id="bef52-201">WrapKey</span></span>
- <span data-ttu-id="bef52-202">Sprawdzić</span><span class="sxs-lookup"><span data-stu-id="bef52-202">Verify</span></span>
- <span data-ttu-id="bef52-203">Zapisywania</span><span class="sxs-lookup"><span data-stu-id="bef52-203">Sign</span></span>
- <span data-ttu-id="bef52-204">Pobierz</span><span class="sxs-lookup"><span data-stu-id="bef52-204">Get</span></span>
- <span data-ttu-id="bef52-205">Lista</span><span class="sxs-lookup"><span data-stu-id="bef52-205">List</span></span>
- <span data-ttu-id="bef52-206">Aktualizowane</span><span class="sxs-lookup"><span data-stu-id="bef52-206">Update</span></span>
- <span data-ttu-id="bef52-207">Tworzonych</span><span class="sxs-lookup"><span data-stu-id="bef52-207">Create</span></span>
- <span data-ttu-id="bef52-208">Przywoz</span><span class="sxs-lookup"><span data-stu-id="bef52-208">Import</span></span>
- <span data-ttu-id="bef52-209">Usuwać</span><span class="sxs-lookup"><span data-stu-id="bef52-209">Delete</span></span>
- <span data-ttu-id="bef52-210">Wykonania</span><span class="sxs-lookup"><span data-stu-id="bef52-210">Backup</span></span>
- <span data-ttu-id="bef52-211">Przywrócenie</span><span class="sxs-lookup"><span data-stu-id="bef52-211">Restore</span></span>
- <span data-ttu-id="bef52-212">Odzyskiwanie</span><span class="sxs-lookup"><span data-stu-id="bef52-212">Recover</span></span>
- <span data-ttu-id="bef52-213">Wyczyścić</span><span class="sxs-lookup"><span data-stu-id="bef52-213">Purge</span></span>

```yaml
Type: String[]
Parameter Sets: ByServicePrincipalName, ByUserPrincipalName, ByObjectId, ByEmailAddress
Aliases:
Accepted values: decrypt, encrypt, unwrapKey, wrapKey, verify, sign, get, list, update, create, import, delete, backup, restore, recover, purge, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bef52-214">-PermissionsToSecrets</span><span class="sxs-lookup"><span data-stu-id="bef52-214">-PermissionsToSecrets</span></span>
<span data-ttu-id="bef52-215">Określa tablicę uprawnień do tajnego działania, które mają zostać udzielone użytkownikowi lub podmiotowi zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="bef52-215">Specifies an array of secret operation permissions to grant to a user or service principal.</span></span>

<span data-ttu-id="bef52-216">Dopuszczalne wartości dla tego parametru:</span><span class="sxs-lookup"><span data-stu-id="bef52-216">The acceptable values for this parameter:</span></span>

- <span data-ttu-id="bef52-217">Pobierz</span><span class="sxs-lookup"><span data-stu-id="bef52-217">Get</span></span>
- <span data-ttu-id="bef52-218">Lista</span><span class="sxs-lookup"><span data-stu-id="bef52-218">List</span></span>
- <span data-ttu-id="bef52-219">Ustawić</span><span class="sxs-lookup"><span data-stu-id="bef52-219">Set</span></span>
- <span data-ttu-id="bef52-220">Usuwać</span><span class="sxs-lookup"><span data-stu-id="bef52-220">Delete</span></span>
- <span data-ttu-id="bef52-221">Wykonania</span><span class="sxs-lookup"><span data-stu-id="bef52-221">Backup</span></span>
- <span data-ttu-id="bef52-222">Przywrócenie</span><span class="sxs-lookup"><span data-stu-id="bef52-222">Restore</span></span>
- <span data-ttu-id="bef52-223">Odzyskiwanie</span><span class="sxs-lookup"><span data-stu-id="bef52-223">Recover</span></span>
- <span data-ttu-id="bef52-224">Wyczyścić</span><span class="sxs-lookup"><span data-stu-id="bef52-224">Purge</span></span>

```yaml
Type: String[]
Parameter Sets: ByServicePrincipalName, ByUserPrincipalName, ByObjectId, ByEmailAddress
Aliases:
Accepted values: get, list, set, delete, backup, restore, recover, purge, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bef52-225">-PermissionsToStorage</span><span class="sxs-lookup"><span data-stu-id="bef52-225">-PermissionsToStorage</span></span>
<span data-ttu-id="bef52-226">Określa zarządzane konto magazynu i uprawnienia operacji definicji SaS, które mają zostać udzielone użytkownikowi lub podmiotowi zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="bef52-226">Specifies managed storage account and SaS-definition operation permissions to grant to a user or service principal.</span></span>

```yaml
Type: String[]
Parameter Sets: ByServicePrincipalName, ByUserPrincipalName, ByObjectId, ByEmailAddress
Aliases:
Accepted values: get, list, delete, set, update, regeneratekey, getsas, listsas, deletesas, setsas, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bef52-227">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bef52-227">-ResourceGroupName</span></span>
<span data-ttu-id="bef52-228">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bef52-228">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bef52-229">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="bef52-229">-ServicePrincipalName</span></span>
<span data-ttu-id="bef52-230">Określa główną nazwę usługi aplikacji, do której mają być udzielane uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="bef52-230">Specifies the service principal name of the application to which to grant permissions.</span></span>

<span data-ttu-id="bef52-231">Określ identyfikator aplikacji, określany także jako identyfikator klienta, zarejestrowany dla aplikacji w katalogu AzureActive.</span><span class="sxs-lookup"><span data-stu-id="bef52-231">Specify the application ID, also known as client ID, registered for the application in AzureActive Directory.</span></span> <span data-ttu-id="bef52-232">Aplikacja o głównej nazwie usługi, którą ten parametr określa, musi być zarejestrowana w katalogu platformy Azure, który zawiera bieżący abonament.</span><span class="sxs-lookup"><span data-stu-id="bef52-232">The application with the service principal name that this parameter specifies must be registered in the Azure directory that contains your current subscription.</span></span>

```yaml
Type: String
Parameter Sets: ByServicePrincipalName
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bef52-233">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="bef52-233">-UserPrincipalName</span></span>
<span data-ttu-id="bef52-234">Określa główną nazwę użytkownika, któremu chcesz udzielić uprawnień.</span><span class="sxs-lookup"><span data-stu-id="bef52-234">Specifies the user principal name of the user to whom to grant permissions.</span></span>

<span data-ttu-id="bef52-235">Ta główna nazwa użytkownika musi istnieć w katalogu skojarzonym z bieżącą subskrypcją.</span><span class="sxs-lookup"><span data-stu-id="bef52-235">This user principal name must exist in the directory associated with the current subscription.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bef52-236">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="bef52-236">-VaultName</span></span>
<span data-ttu-id="bef52-237">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="bef52-237">Specifies the name of a key vault.</span></span>

<span data-ttu-id="bef52-238">To polecenie cmdlet modyfikuje zasady dostępu dla magazynu kluczy określanego przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="bef52-238">This cmdlet modifies the access policy for the key vault that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bef52-239">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bef52-239">-Confirm</span></span>
<span data-ttu-id="bef52-240">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bef52-240">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bef52-241">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bef52-241">-WhatIf</span></span>
<span data-ttu-id="bef52-242">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bef52-242">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bef52-243">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bef52-243">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bef52-244">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bef52-244">CommonParameters</span></span>
<span data-ttu-id="bef52-245">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bef52-245">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bef52-246">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bef52-246">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bef52-247">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bef52-247">INPUTS</span></span>

### <span data-ttu-id="bef52-248">String, GUID, String [], przełącznik</span><span class="sxs-lookup"><span data-stu-id="bef52-248">String, Guid, String[], Switch</span></span>

## <span data-ttu-id="bef52-249">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bef52-249">OUTPUTS</span></span>

### <span data-ttu-id="bef52-250">Microsoft. Azure. Commands. platforming. models. PSVault</span><span class="sxs-lookup"><span data-stu-id="bef52-250">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

## <span data-ttu-id="bef52-251">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bef52-251">NOTES</span></span>

## <span data-ttu-id="bef52-252">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bef52-252">RELATED LINKS</span></span>

[<span data-ttu-id="bef52-253">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="bef52-253">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="bef52-254">Remove-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="bef52-254">Remove-AzKeyVaultAccessPolicy</span></span>](./Remove-AzKeyVaultAccessPolicy.md)

