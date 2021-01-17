---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: AE7B103B-23ED-4A66-A0DC-14FB0DF38FA8
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultAccessPolicy.md
ms.openlocfilehash: e19565aa8ae249acf61fce67f0a2b54e20143758
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323890"
---
# <span data-ttu-id="0df51-101">Remove-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0df51-101">Remove-AzKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="0df51-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0df51-102">SYNOPSIS</span></span>
<span data-ttu-id="0df51-103">Usuwa wszystkie uprawnienia użytkownika lub aplikacji z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="0df51-103">Removes all permissions for a user or application from a key vault.</span></span>

## <span data-ttu-id="0df51-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0df51-104">SYNTAX</span></span>

### <span data-ttu-id="0df51-105">ByUserPrincipalName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0df51-105">ByUserPrincipalName (Default)</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -UserPrincipalName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0df51-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="0df51-106">ByObjectId</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0df51-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="0df51-107">ByServicePrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0df51-108">ByEmail</span><span class="sxs-lookup"><span data-stu-id="0df51-108">ByEmail</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0df51-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="0df51-109">ForVault</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0df51-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="0df51-110">InputObjectByObjectId</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ObjectId <String> [-ApplicationId <Guid>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0df51-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="0df51-111">InputObjectByServicePrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ServicePrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0df51-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="0df51-112">InputObjectByUserPrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -UserPrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0df51-113">InputObjectByEmail</span><span class="sxs-lookup"><span data-stu-id="0df51-113">InputObjectByEmail</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -EmailAddress <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0df51-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="0df51-114">InputObjectForVault</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0df51-115">ResourceIdByObjectId</span><span class="sxs-lookup"><span data-stu-id="0df51-115">ResourceIdByObjectId</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -ObjectId <String> [-ApplicationId <Guid>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0df51-116">ResourceIdByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="0df51-116">ResourceIdByServicePrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -ServicePrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0df51-117">ResourceIdByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="0df51-117">ResourceIdByUserPrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -UserPrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0df51-118">ResourceIdByEmail</span><span class="sxs-lookup"><span data-stu-id="0df51-118">ResourceIdByEmail</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -EmailAddress <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0df51-119">ResourceIdForVault</span><span class="sxs-lookup"><span data-stu-id="0df51-119">ResourceIdForVault</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> [-EnabledForDeployment] [-EnabledForTemplateDeployment]
 [-EnabledForDiskEncryption] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0df51-120">Opis</span><span class="sxs-lookup"><span data-stu-id="0df51-120">DESCRIPTION</span></span>
<span data-ttu-id="0df51-121">Polecenie cmdlet **Remove-AzKeyVaultAccessPolicy** usuwa wszystkie uprawnienia użytkownika lub aplikacji albo dla wszystkich użytkowników i aplikacji z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="0df51-121">The **Remove-AzKeyVaultAccessPolicy** cmdlet removes all permissions for a user or application or for all users and applications from a key vault.</span></span>
<span data-ttu-id="0df51-122">Nawet jeśli usuniesz wszystkie uprawnienia, właściciel subskrypcji platformy Azure zawierającej Magazyn kluczy może dodawać uprawnienia do magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="0df51-122">Even if you remove all permissions, the owner of the Azure subscription that contains the key vault can add permissions to the key vault.</span></span>
<span data-ttu-id="0df51-123">Uwaga: chociaż określenie grupy zasobów jest opcjonalne dla tego polecenia cmdlet, należy to zrobić w celu uzyskania lepszej wydajności.</span><span class="sxs-lookup"><span data-stu-id="0df51-123">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="0df51-124">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0df51-124">EXAMPLES</span></span>

### <span data-ttu-id="0df51-125">Przykład 1: usuwanie uprawnień użytkownika</span><span class="sxs-lookup"><span data-stu-id="0df51-125">Example 1: Remove permissions for a user</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PassThru

Vault Name                       : Contoso03Vault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : False
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             :
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        :
                                   Permissions to Secrets                     :
                                   Permissions to Certificates                : get, create
                                   Permissions to (Key Vault Managed) Storage :


Network Rule Set                 :
                                   Default Action                             : Allow
                                   Bypass                                     : AzureServices
                                   IP Rules                                   :
                                   Virtual Network Rules                      :

Tags                             :
```

<span data-ttu-id="0df51-126">To polecenie usuwa wszystkie uprawnienia użytkownika PattiFuller@contoso.com w magazynie kluczy o nazwie Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="0df51-126">This command removes all the permissions that a user PattiFuller@contoso.com has on the key vault named Contoso03Vault.</span></span>  <span data-ttu-id="0df51-127">Jeśli jest określony parametr-PassThru, zwracany jest obiekt magazynu.</span><span class="sxs-lookup"><span data-stu-id="0df51-127">If -PassThru is specified, the KeyVault object is returned.</span></span>

### <span data-ttu-id="0df51-128">Przykład 2: usuwanie uprawnień do aplikacji</span><span class="sxs-lookup"><span data-stu-id="0df51-128">Example 2: Remove permissions for an application</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com'
```

<span data-ttu-id="0df51-129">To polecenie usuwa wszystkie uprawnienia aplikacji w magazynie kluczy o nazwie Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="0df51-129">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="0df51-130">W tym przykładzie zidentyfikowano aplikację przy użyciu nazwy głównej usługi zarejestrowanej w usłudze Azure Active Directory `http://payroll.contoso.com` .</span><span class="sxs-lookup"><span data-stu-id="0df51-130">This example identifies the application by using the service principal name registered in Azure Active Directory, `http://payroll.contoso.com`.</span></span>

### <span data-ttu-id="0df51-131">Przykład 3: usuwanie uprawnień do aplikacji przy użyciu jej identyfikatora obiektu</span><span class="sxs-lookup"><span data-stu-id="0df51-131">Example 3: Remove permissions for an application by using its object ID</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectID 34595082-9346-41b6-8d6b-295a2808b8db
```

<span data-ttu-id="0df51-132">To polecenie usuwa wszystkie uprawnienia aplikacji w magazynie kluczy o nazwie Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="0df51-132">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="0df51-133">W tym przykładzie aplikacja została zidentyfikowana przez identyfikator obiektu podmiotu usługi.</span><span class="sxs-lookup"><span data-stu-id="0df51-133">This example identifies the application by the object ID of the service principal.</span></span>

### <span data-ttu-id="0df51-134">Przykład 4: usuwanie uprawnień dla dostawcy zasobów Microsoft. COMPUTE</span><span class="sxs-lookup"><span data-stu-id="0df51-134">Example 4: Remove permissions for the Microsoft.Compute resource provider</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="0df51-135">To polecenie powoduje usunięcie uprawnień dla dostawcy zasobów Microsoft. COMPUTE w celu uzyskania kluczy tajnych z Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="0df51-135">This command removes permission for the Microsoft.Compute resource provider to get secrets from the Contoso03Vault.</span></span>

## <span data-ttu-id="0df51-136">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0df51-136">PARAMETERS</span></span>

### <span data-ttu-id="0df51-137">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="0df51-137">-ApplicationId</span></span>
<span data-ttu-id="0df51-138">Określa identyfikator aplikacji, której uprawnienia powinny zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="0df51-138">Specifies the ID of application whose permissions should be removed</span></span>

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

### <span data-ttu-id="0df51-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0df51-139">-DefaultProfile</span></span>
<span data-ttu-id="0df51-140">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="0df51-140">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0df51-141">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="0df51-141">-EmailAddress</span></span>
<span data-ttu-id="0df51-142">Określa adres e-mail użytkownika, którego dostęp należy usunąć.</span><span class="sxs-lookup"><span data-stu-id="0df51-142">Specifies the user email address of the user whose access you want to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByEmail, InputObjectByEmail, ResourceIdByEmail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0df51-143">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="0df51-143">-EnabledForDeployment</span></span>
<span data-ttu-id="0df51-144">Jeśli ta funkcja jest określona, wyłącza możliwość pobierania kluczy tajnych z tego magazynu kluczy przez dostawcę Microsoft. COMPUTE Provider, gdy jest używany do tworzenia zasobów.</span><span class="sxs-lookup"><span data-stu-id="0df51-144">If specified, disables the retrieval of secrets from this key vault by the Microsoft.Compute resource provider when referenced in resource creation.</span></span>

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

### <span data-ttu-id="0df51-145">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="0df51-145">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="0df51-146">Jeśli ta funkcja jest określona, wyłącza pobieranie kluczy tajnych z tego magazynu kluczy za pomocą szyfrowania dysków Azure.</span><span class="sxs-lookup"><span data-stu-id="0df51-146">If specified, disables the retrieval of secrets from this key vault by Azure Disk Encryption.</span></span>

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

### <span data-ttu-id="0df51-147">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="0df51-147">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="0df51-148">Jeśli ta funkcja jest określona, wyłącza pobieranie kluczy tajnych z tego magazynu kluczy za pomocą Menedżera zasobów Azure, gdy następuje odwołanie w szablonach.</span><span class="sxs-lookup"><span data-stu-id="0df51-148">If specified, disables the retrieval of secrets from this key vault by Azure Resource Manager when referenced in templates.</span></span>

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

### <span data-ttu-id="0df51-149">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0df51-149">-InputObject</span></span>
<span data-ttu-id="0df51-150">Obiekt magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="0df51-150">Key Vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmail, InputObjectForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0df51-151">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="0df51-151">-ObjectId</span></span>
<span data-ttu-id="0df51-152">Określa identyfikator obiektu podmiotu użytkownika lub usługi w usłudze Azure Active Directory, dla którego należy usunąć uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="0df51-152">Specifies the object ID of the user or service principal in Azure Active Directory for which to remove permissions.</span></span>

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

### <span data-ttu-id="0df51-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0df51-153">-PassThru</span></span>
<span data-ttu-id="0df51-154">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="0df51-154">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0df51-155">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="0df51-155">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0df51-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0df51-156">-ResourceGroupName</span></span>
<span data-ttu-id="0df51-157">Określa nazwę grupy zasobów skojarzonej z magazynem kluczy, którego zasady dostępu są modyfikowane.</span><span class="sxs-lookup"><span data-stu-id="0df51-157">Specifies the name of the resource group associated with the key vault whose access policy is being modified.</span></span>
<span data-ttu-id="0df51-158">Jeśli ta opcja nie jest określona, to polecenie cmdlet wyszukuje Magazyn kluczy w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="0df51-158">If not specified, this cmdlet searches for the key vault in the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmail, ForVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0df51-159">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0df51-159">-ResourceId</span></span>
<span data-ttu-id="0df51-160">Identyfikator zasobu magazynu.</span><span class="sxs-lookup"><span data-stu-id="0df51-160">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmail, ResourceIdForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0df51-161">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="0df51-161">-ServicePrincipalName</span></span>
<span data-ttu-id="0df51-162">Określa główną nazwę usługi aplikacji, której uprawnienia należy usunąć.</span><span class="sxs-lookup"><span data-stu-id="0df51-162">Specifies the service principal name of the application whose permissions you want to remove.</span></span>
<span data-ttu-id="0df51-163">Określ identyfikator aplikacji, określany także jako identyfikator klienta, zarejestrowany dla aplikacji w usłudze Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0df51-163">Specify the application ID, also known as client ID, registered for the application in Azure Active Directory.</span></span>

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

### <span data-ttu-id="0df51-164">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="0df51-164">-UserPrincipalName</span></span>
<span data-ttu-id="0df51-165">Określa główną nazwę użytkownika, którego dostęp należy usunąć.</span><span class="sxs-lookup"><span data-stu-id="0df51-165">Specifies the user principal name of the user whose access you want to remove.</span></span>

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

### <span data-ttu-id="0df51-166">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="0df51-166">-VaultName</span></span>
<span data-ttu-id="0df51-167">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="0df51-167">Specifies the name of the key vault.</span></span>
<span data-ttu-id="0df51-168">To polecenie cmdlet umożliwia usunięcie uprawnień do magazynu kluczy określanego przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="0df51-168">This cmdlet removes permissions for the key vault that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmail, ForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0df51-169">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0df51-169">-Confirm</span></span>
<span data-ttu-id="0df51-170">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0df51-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0df51-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0df51-171">-WhatIf</span></span>
<span data-ttu-id="0df51-172">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0df51-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0df51-173">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0df51-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0df51-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0df51-174">CommonParameters</span></span>
<span data-ttu-id="0df51-175">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0df51-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0df51-176">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0df51-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0df51-177">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0df51-177">INPUTS</span></span>

### <span data-ttu-id="0df51-178">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="0df51-178">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="0df51-179">System. String</span><span class="sxs-lookup"><span data-stu-id="0df51-179">System.String</span></span>

## <span data-ttu-id="0df51-180">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0df51-180">OUTPUTS</span></span>

### <span data-ttu-id="0df51-181">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="0df51-181">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="0df51-182">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0df51-182">NOTES</span></span>

## <span data-ttu-id="0df51-183">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0df51-183">RELATED LINKS</span></span>

[<span data-ttu-id="0df51-184">Set-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0df51-184">Set-AzKeyVaultAccessPolicy</span></span>](./Set-AzKeyVaultAccessPolicy.md)

