---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: AE7B103B-23ED-4A66-A0DC-14FB0DF38FA8
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultAccessPolicy.md
ms.openlocfilehash: e19565aa8ae249acf61fce67f0a2b54e20143758
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243355"
---
# <span data-ttu-id="cb5e2-101">Remove-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="cb5e2-101">Remove-AzKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="cb5e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb5e2-102">SYNOPSIS</span></span>
<span data-ttu-id="cb5e2-103">Usuwa wszystkie uprawnienia użytkownika lub aplikacji z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="cb5e2-103">Removes all permissions for a user or application from a key vault.</span></span>

## <span data-ttu-id="cb5e2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cb5e2-104">SYNTAX</span></span>

### <span data-ttu-id="cb5e2-105">ByUserPrincipalName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="cb5e2-105">ByUserPrincipalName (Default)</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -UserPrincipalName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb5e2-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="cb5e2-106">ByObjectId</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cb5e2-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="cb5e2-107">ByServicePrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cb5e2-108">ByEmail</span><span class="sxs-lookup"><span data-stu-id="cb5e2-108">ByEmail</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb5e2-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="cb5e2-109">ForVault</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb5e2-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="cb5e2-110">InputObjectByObjectId</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ObjectId <String> [-ApplicationId <Guid>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb5e2-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="cb5e2-111">InputObjectByServicePrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ServicePrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb5e2-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="cb5e2-112">InputObjectByUserPrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -UserPrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb5e2-113">InputObjectByEmail</span><span class="sxs-lookup"><span data-stu-id="cb5e2-113">InputObjectByEmail</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -EmailAddress <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb5e2-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="cb5e2-114">InputObjectForVault</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb5e2-115">ResourceIdByObjectId</span><span class="sxs-lookup"><span data-stu-id="cb5e2-115">ResourceIdByObjectId</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -ObjectId <String> [-ApplicationId <Guid>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb5e2-116">ResourceIdByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="cb5e2-116">ResourceIdByServicePrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -ServicePrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb5e2-117">ResourceIdByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="cb5e2-117">ResourceIdByUserPrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -UserPrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb5e2-118">ResourceIdByEmail</span><span class="sxs-lookup"><span data-stu-id="cb5e2-118">ResourceIdByEmail</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -EmailAddress <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb5e2-119">ResourceIdForVault</span><span class="sxs-lookup"><span data-stu-id="cb5e2-119">ResourceIdForVault</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> [-EnabledForDeployment] [-EnabledForTemplateDeployment]
 [-EnabledForDiskEncryption] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cb5e2-120">OPIS</span><span class="sxs-lookup"><span data-stu-id="cb5e2-120">DESCRIPTION</span></span>
<span data-ttu-id="cb5e2-121">Polecenie **cmdlet Remove-AzKeyVaultAccessPolicy** usuwa wszystkie uprawnienia użytkownika lub aplikacji albo wszystkich użytkowników i aplikacji z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="cb5e2-121">The **Remove-AzKeyVaultAccessPolicy** cmdlet removes all permissions for a user or application or for all users and applications from a key vault.</span></span>
<span data-ttu-id="cb5e2-122">Nawet jeśli usuniesz wszystkie uprawnienia, właściciel subskrypcji platformy Azure, która zawiera magazyn kluczy, może dodać uprawnienia do magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="cb5e2-122">Even if you remove all permissions, the owner of the Azure subscription that contains the key vault can add permissions to the key vault.</span></span>
<span data-ttu-id="cb5e2-123">Pamiętaj, że mimo że w przypadku tego polecenia cmdlet określenie grupy zasobów jest opcjonalne, należy to zrobić, aby uzyskać lepszą wydajność.</span><span class="sxs-lookup"><span data-stu-id="cb5e2-123">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="cb5e2-124">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cb5e2-124">EXAMPLES</span></span>

### <span data-ttu-id="cb5e2-125">Przykład 1. Usuwanie uprawnień użytkownika</span><span class="sxs-lookup"><span data-stu-id="cb5e2-125">Example 1: Remove permissions for a user</span></span>
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

<span data-ttu-id="cb5e2-126">To polecenie usuwa wszystkie uprawnienia, które użytkownik ma w magazynie kluczy o nazwie PattiFuller@contoso.com Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="cb5e2-126">This command removes all the permissions that a user PattiFuller@contoso.com has on the key vault named Contoso03Vault.</span></span>  <span data-ttu-id="cb5e2-127">Jeśli jest określona wartość -PassThru, jest zwracany obiekt KeyVault.</span><span class="sxs-lookup"><span data-stu-id="cb5e2-127">If -PassThru is specified, the KeyVault object is returned.</span></span>

### <span data-ttu-id="cb5e2-128">Przykład 2. Usuwanie uprawnień dla aplikacji</span><span class="sxs-lookup"><span data-stu-id="cb5e2-128">Example 2: Remove permissions for an application</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com'
```

<span data-ttu-id="cb5e2-129">To polecenie usuwa wszystkie uprawnienia aplikacji w magazynie kluczy o nazwie Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="cb5e2-129">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="cb5e2-130">W tym przykładzie aplikacja jest identyfikowana przy użyciu nazwy podmiotu zabezpieczeń usługi zarejestrowanej w usłudze Azure Active `http://payroll.contoso.com` Directory.</span><span class="sxs-lookup"><span data-stu-id="cb5e2-130">This example identifies the application by using the service principal name registered in Azure Active Directory, `http://payroll.contoso.com`.</span></span>

### <span data-ttu-id="cb5e2-131">Przykład 3. Usuwanie uprawnień aplikacji przy użyciu identyfikatora obiektu</span><span class="sxs-lookup"><span data-stu-id="cb5e2-131">Example 3: Remove permissions for an application by using its object ID</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectID 34595082-9346-41b6-8d6b-295a2808b8db
```

<span data-ttu-id="cb5e2-132">To polecenie usuwa wszystkie uprawnienia aplikacji w magazynie kluczy o nazwie Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="cb5e2-132">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="cb5e2-133">W tym przykładzie aplikacja jest identyfikowana za pomocą identyfikatora obiektu podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="cb5e2-133">This example identifies the application by the object ID of the service principal.</span></span>

### <span data-ttu-id="cb5e2-134">Przykład 4. Usuwanie uprawnień dostawcy zasobów Microsoft.Compute</span><span class="sxs-lookup"><span data-stu-id="cb5e2-134">Example 4: Remove permissions for the Microsoft.Compute resource provider</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="cb5e2-135">To polecenie usuwa uprawnienia dostawcy zasobów Microsoft.Compute w celu uzyskania sekretów z witryny Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="cb5e2-135">This command removes permission for the Microsoft.Compute resource provider to get secrets from the Contoso03Vault.</span></span>

## <span data-ttu-id="cb5e2-136">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb5e2-136">PARAMETERS</span></span>

### <span data-ttu-id="cb5e2-137">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="cb5e2-137">-ApplicationId</span></span>
<span data-ttu-id="cb5e2-138">Określa identyfikator aplikacji, której uprawnienia powinny zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="cb5e2-138">Specifies the ID of application whose permissions should be removed</span></span>

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

### <span data-ttu-id="cb5e2-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb5e2-139">-DefaultProfile</span></span>
<span data-ttu-id="cb5e2-140">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="cb5e2-140">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cb5e2-141">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="cb5e2-141">-EmailAddress</span></span>
<span data-ttu-id="cb5e2-142">Określa adres e-mail użytkownika, którego dostęp chcesz usunąć.</span><span class="sxs-lookup"><span data-stu-id="cb5e2-142">Specifies the user email address of the user whose access you want to remove.</span></span>

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

### <span data-ttu-id="cb5e2-143">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="cb5e2-143">-EnabledForDeployment</span></span>
<span data-ttu-id="cb5e2-144">Jeśli jest to określone, wyłącza pobieranie sekretów z tego magazynu kluczy przez dostawcę zasobów Microsoft.Compute, gdy odwołuje się do nich podczas tworzenia zasobów.</span><span class="sxs-lookup"><span data-stu-id="cb5e2-144">If specified, disables the retrieval of secrets from this key vault by the Microsoft.Compute resource provider when referenced in resource creation.</span></span>

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

### <span data-ttu-id="cb5e2-145">-EnabledForScriptEncryption</span><span class="sxs-lookup"><span data-stu-id="cb5e2-145">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="cb5e2-146">Jeśli jest to określone, wyłącza pobieranie sekretów z tego magazynu kluczy przez szyfrowanie dysków platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cb5e2-146">If specified, disables the retrieval of secrets from this key vault by Azure Disk Encryption.</span></span>

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

### <span data-ttu-id="cb5e2-147">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="cb5e2-147">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="cb5e2-148">Jeśli jest to określone, wyłącza pobieranie sekretów z tego magazynu kluczy przez usługę Azure Resource Manager podczas tworzenia odwoływać się do nich w szablonach.</span><span class="sxs-lookup"><span data-stu-id="cb5e2-148">If specified, disables the retrieval of secrets from this key vault by Azure Resource Manager when referenced in templates.</span></span>

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

### <span data-ttu-id="cb5e2-149">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb5e2-149">-InputObject</span></span>
<span data-ttu-id="cb5e2-150">Obiekt magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="cb5e2-150">Key Vault object.</span></span>

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

### <span data-ttu-id="cb5e2-151">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="cb5e2-151">-ObjectId</span></span>
<span data-ttu-id="cb5e2-152">Określa identyfikator obiektu użytkownika lub podmiotu zabezpieczeń usługi w usłudze Azure Active Directory, dla którego mają być usuwane uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="cb5e2-152">Specifies the object ID of the user or service principal in Azure Active Directory for which to remove permissions.</span></span>

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

### <span data-ttu-id="cb5e2-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cb5e2-153">-PassThru</span></span>
<span data-ttu-id="cb5e2-154">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="cb5e2-154">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cb5e2-155">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="cb5e2-155">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cb5e2-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb5e2-156">-ResourceGroupName</span></span>
<span data-ttu-id="cb5e2-157">Określa nazwę grupy zasobów skojarzonej z magazynem kluczy, którego zasady dostępu są modyfikowane.</span><span class="sxs-lookup"><span data-stu-id="cb5e2-157">Specifies the name of the resource group associated with the key vault whose access policy is being modified.</span></span>
<span data-ttu-id="cb5e2-158">Jeśli nie zostanie określone, to polecenie cmdlet wyszukuje magazyn kluczy w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="cb5e2-158">If not specified, this cmdlet searches for the key vault in the current subscription.</span></span>

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

### <span data-ttu-id="cb5e2-159">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb5e2-159">-ResourceId</span></span>
<span data-ttu-id="cb5e2-160">Identyfikator zasobu KeyVault.</span><span class="sxs-lookup"><span data-stu-id="cb5e2-160">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="cb5e2-161">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="cb5e2-161">-ServicePrincipalName</span></span>
<span data-ttu-id="cb5e2-162">Określa nazwę podmiotu zabezpieczeń usługi aplikacji, której uprawnienia chcesz usunąć.</span><span class="sxs-lookup"><span data-stu-id="cb5e2-162">Specifies the service principal name of the application whose permissions you want to remove.</span></span>
<span data-ttu-id="cb5e2-163">Określ identyfikator aplikacji, nazywany również identyfikatorem klienta, zarejestrowanego dla aplikacji w usłudze Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="cb5e2-163">Specify the application ID, also known as client ID, registered for the application in Azure Active Directory.</span></span>

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

### <span data-ttu-id="cb5e2-164">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="cb5e2-164">-UserPrincipalName</span></span>
<span data-ttu-id="cb5e2-165">Określa główną nazwę użytkownika, którego dostęp chcesz usunąć.</span><span class="sxs-lookup"><span data-stu-id="cb5e2-165">Specifies the user principal name of the user whose access you want to remove.</span></span>

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

### <span data-ttu-id="cb5e2-166">-VaultName</span><span class="sxs-lookup"><span data-stu-id="cb5e2-166">-VaultName</span></span>
<span data-ttu-id="cb5e2-167">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="cb5e2-167">Specifies the name of the key vault.</span></span>
<span data-ttu-id="cb5e2-168">To polecenie cmdlet usuwa uprawnienia do magazynu kluczy, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="cb5e2-168">This cmdlet removes permissions for the key vault that this parameter specifies.</span></span>

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

### <span data-ttu-id="cb5e2-169">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cb5e2-169">-Confirm</span></span>
<span data-ttu-id="cb5e2-170">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cb5e2-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb5e2-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb5e2-171">-WhatIf</span></span>
<span data-ttu-id="cb5e2-172">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb5e2-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb5e2-173">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="cb5e2-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb5e2-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb5e2-174">CommonParameters</span></span>
<span data-ttu-id="cb5e2-175">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb5e2-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb5e2-176">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cb5e2-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb5e2-177">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cb5e2-177">INPUTS</span></span>

### <span data-ttu-id="cb5e2-178">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="cb5e2-178">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="cb5e2-179">System.String</span><span class="sxs-lookup"><span data-stu-id="cb5e2-179">System.String</span></span>

## <span data-ttu-id="cb5e2-180">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cb5e2-180">OUTPUTS</span></span>

### <span data-ttu-id="cb5e2-181">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="cb5e2-181">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="cb5e2-182">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cb5e2-182">NOTES</span></span>

## <span data-ttu-id="cb5e2-183">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cb5e2-183">RELATED LINKS</span></span>

[<span data-ttu-id="cb5e2-184">Set-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="cb5e2-184">Set-AzKeyVaultAccessPolicy</span></span>](./Set-AzKeyVaultAccessPolicy.md)

