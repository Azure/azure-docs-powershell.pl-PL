---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: AE7B103B-23ED-4A66-A0DC-14FB0DF38FA8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurermkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVaultAccessPolicy.md
ms.openlocfilehash: ca175d0873b74d8b13d1755f3d0986580c5853ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548092"
---
# <span data-ttu-id="cc5cb-101">Remove-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="cc5cb-101">Remove-AzureRmKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="cc5cb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cc5cb-102">SYNOPSIS</span></span>
<span data-ttu-id="cc5cb-103">Usuwa wszystkie uprawnienia użytkownika lub aplikacji z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="cc5cb-103">Removes all permissions for a user or application from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc5cb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cc5cb-104">SYNTAX</span></span>

### <span data-ttu-id="cc5cb-105">ByUserPrincipalName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cc5cb-105">ByUserPrincipalName (Default)</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -UserPrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cc5cb-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="cc5cb-106">ByObjectId</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cc5cb-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="cc5cb-107">ByServicePrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cc5cb-108">ByEmail</span><span class="sxs-lookup"><span data-stu-id="cc5cb-108">ByEmail</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc5cb-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="cc5cb-109">ForVault</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-EnabledForDeployment] [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc5cb-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="cc5cb-110">InputObjectByObjectId</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ObjectId <String> [-ApplicationId <Guid>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc5cb-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="cc5cb-111">InputObjectByServicePrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ServicePrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc5cb-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="cc5cb-112">InputObjectByUserPrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -UserPrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc5cb-113">InputObjectByEmail</span><span class="sxs-lookup"><span data-stu-id="cc5cb-113">InputObjectByEmail</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -EmailAddress <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc5cb-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="cc5cb-114">InputObjectForVault</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc5cb-115">Opis</span><span class="sxs-lookup"><span data-stu-id="cc5cb-115">DESCRIPTION</span></span>
<span data-ttu-id="cc5cb-116">Polecenie cmdlet **Remove-AzureRmKeyVaultAccessPolicy** usuwa wszystkie uprawnienia użytkownika lub aplikacji albo dla wszystkich użytkowników i aplikacji z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="cc5cb-116">The **Remove-AzureRmKeyVaultAccessPolicy** cmdlet removes all permissions for a user or application or for all users and applications from a key vault.</span></span>
<span data-ttu-id="cc5cb-117">Nawet jeśli usuniesz wszystkie uprawnienia, właściciel subskrypcji platformy Azure zawierającej Magazyn kluczy może dodawać uprawnienia do magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="cc5cb-117">Even if you remove all permissions, the owner of the Azure subscription that contains the key vault can add permissions to the key vault.</span></span>

<span data-ttu-id="cc5cb-118">Uwaga: chociaż określenie grupy zasobów jest opcjonalne dla tego polecenia cmdlet, należy to zrobić w celu uzyskania lepszej wydajności.</span><span class="sxs-lookup"><span data-stu-id="cc5cb-118">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="cc5cb-119">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cc5cb-119">EXAMPLES</span></span>

### <span data-ttu-id="cc5cb-120">Przykład 1: usuwanie uprawnień użytkownika</span><span class="sxs-lookup"><span data-stu-id="cc5cb-120">Example 1: Remove permissions for a user</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com'
```

<span data-ttu-id="cc5cb-121">To polecenie usuwa wszystkie uprawnienia użytkownika PattiFuller@contoso.com w magazynie kluczy o nazwie Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="cc5cb-121">This command removes all the permissions that a user PattiFuller@contoso.com has on the key vault named Contoso03Vault.</span></span>

### <span data-ttu-id="cc5cb-122">Przykład 2: usuwanie uprawnień do aplikacji</span><span class="sxs-lookup"><span data-stu-id="cc5cb-122">Example 2: Remove permissions for an application</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com'
```

<span data-ttu-id="cc5cb-123">To polecenie usuwa wszystkie uprawnienia aplikacji w magazynie kluczy o nazwie Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="cc5cb-123">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="cc5cb-124">W tym przykładzie zidentyfikowano aplikację przy użyciu nazwy głównej usługi zarejestrowanej w usłudze Azure Active Directory http://payroll.contoso.com .</span><span class="sxs-lookup"><span data-stu-id="cc5cb-124">This example identifies the application by using the service principal name registered in Azure Active Directory, http://payroll.contoso.com.</span></span>

### <span data-ttu-id="cc5cb-125">Przykład 3: usuwanie uprawnień do aplikacji przy użyciu jej identyfikatora obiektu</span><span class="sxs-lookup"><span data-stu-id="cc5cb-125">Example 3: Remove permissions for an application by using its object ID</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectID 34595082-9346-41b6-8d6b-295a2808b8db
```

<span data-ttu-id="cc5cb-126">To polecenie usuwa wszystkie uprawnienia aplikacji w magazynie kluczy o nazwie Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="cc5cb-126">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="cc5cb-127">W tym przykładzie aplikacja została zidentyfikowana przez identyfikator obiektu podmiotu usługi.</span><span class="sxs-lookup"><span data-stu-id="cc5cb-127">This example identifies the application by the object ID of the service principal.</span></span>

### <span data-ttu-id="cc5cb-128">Przykład 4: usuwanie uprawnień dla dostawcy zasobów Microsoft. COMPUTE</span><span class="sxs-lookup"><span data-stu-id="cc5cb-128">Example 4: Remove permissions for the Microsoft.Compute resource provider</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="cc5cb-129">To polecenie powoduje usunięcie uprawnień dla dostawcy zasobów Microsoft. COMPUTE w celu uzyskania kluczy tajnych z Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="cc5cb-129">This command removes permission for the Microsoft.Compute resource provider to get secrets from the Contoso03Vault.</span></span>

## <span data-ttu-id="cc5cb-130">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cc5cb-130">PARAMETERS</span></span>

### <span data-ttu-id="cc5cb-131">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="cc5cb-131">-ApplicationId</span></span>
<span data-ttu-id="cc5cb-132">Określa identyfikator aplikacji, której uprawnienia powinny zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="cc5cb-132">Specifies the ID of application whose permissions should be removed</span></span>

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

### <span data-ttu-id="cc5cb-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc5cb-133">-DefaultProfile</span></span>
<span data-ttu-id="cc5cb-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="cc5cb-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cc5cb-135">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="cc5cb-135">-EmailAddress</span></span>
<span data-ttu-id="cc5cb-136">Określa adres e-mail użytkownika, którego dostęp należy usunąć.</span><span class="sxs-lookup"><span data-stu-id="cc5cb-136">Specifies the user email address of the user whose access you want to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByEmail, InputObjectByEmail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc5cb-137">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="cc5cb-137">-EnabledForDeployment</span></span>
<span data-ttu-id="cc5cb-138">Jeśli ta funkcja jest określona, wyłącza możliwość pobierania kluczy tajnych z tego magazynu kluczy przez dostawcę Microsoft. COMPUTE Provider, gdy jest używany do tworzenia zasobów.</span><span class="sxs-lookup"><span data-stu-id="cc5cb-138">If specified, disables the retrieval of secrets from this key vault by the Microsoft.Compute resource provider when referenced in resource creation.</span></span>

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

### <span data-ttu-id="cc5cb-139">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="cc5cb-139">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="cc5cb-140">Jeśli ta funkcja jest określona, wyłącza pobieranie kluczy tajnych z tego magazynu kluczy za pomocą szyfrowania dysków Azure.</span><span class="sxs-lookup"><span data-stu-id="cc5cb-140">If specified, disables the retrieval of secrets from this key vault by Azure Disk Encryption.</span></span>

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

### <span data-ttu-id="cc5cb-141">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="cc5cb-141">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="cc5cb-142">Jeśli ta funkcja jest określona, wyłącza pobieranie kluczy tajnych z tego magazynu kluczy za pomocą Menedżera zasobów Azure, gdy następuje odwołanie w szablonach.</span><span class="sxs-lookup"><span data-stu-id="cc5cb-142">If specified, disables the retrieval of secrets from this key vault by Azure Resource Manager when referenced in templates.</span></span>

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

### <span data-ttu-id="cc5cb-143">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="cc5cb-143">-InputObject</span></span>
<span data-ttu-id="cc5cb-144">Obiekt magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="cc5cb-144">Key Vault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmail, InputObjectForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc5cb-145">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="cc5cb-145">-ObjectId</span></span>
<span data-ttu-id="cc5cb-146">Określa identyfikator obiektu podmiotu użytkownika lub usługi w usłudze Azure Active Directory, dla którego należy usunąć uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="cc5cb-146">Specifies the object ID of the user or service principal in Azure Active Directory for which to remove permissions.</span></span>

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

### <span data-ttu-id="cc5cb-147">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cc5cb-147">-PassThru</span></span>
<span data-ttu-id="cc5cb-148">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="cc5cb-148">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cc5cb-149">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="cc5cb-149">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cc5cb-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc5cb-150">-ResourceGroupName</span></span>
<span data-ttu-id="cc5cb-151">Określa nazwę grupy zasobów skojarzonej z magazynem kluczy, którego zasady dostępu są modyfikowane.</span><span class="sxs-lookup"><span data-stu-id="cc5cb-151">Specifies the name of the resource group associated with the key vault whose access policy is being modified.</span></span>
<span data-ttu-id="cc5cb-152">Jeśli ta opcja nie jest określona, to polecenie cmdlet wyszukuje Magazyn kluczy w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="cc5cb-152">If not specified, this cmdlet searches for the key vault in the current subscription.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmail, ForVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc5cb-153">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="cc5cb-153">-ServicePrincipalName</span></span>
<span data-ttu-id="cc5cb-154">Określa główną nazwę usługi aplikacji, której uprawnienia należy usunąć.</span><span class="sxs-lookup"><span data-stu-id="cc5cb-154">Specifies the service principal name of the application whose permissions you want to remove.</span></span>
<span data-ttu-id="cc5cb-155">Określ identyfikator aplikacji, określany także jako identyfikator klienta, zarejestrowany dla aplikacji w usłudze Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="cc5cb-155">Specify the application ID, also known as client ID, registered for the application in Azure Active Directory.</span></span>

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

### <span data-ttu-id="cc5cb-156">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="cc5cb-156">-UserPrincipalName</span></span>
<span data-ttu-id="cc5cb-157">Określa główną nazwę użytkownika, którego dostęp należy usunąć.</span><span class="sxs-lookup"><span data-stu-id="cc5cb-157">Specifies the user principal name of the user whose access you want to remove.</span></span>

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

### <span data-ttu-id="cc5cb-158">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="cc5cb-158">-VaultName</span></span>
<span data-ttu-id="cc5cb-159">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="cc5cb-159">Specifies the name of the key vault.</span></span>
<span data-ttu-id="cc5cb-160">To polecenie cmdlet umożliwia usunięcie uprawnień do magazynu kluczy określanego przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="cc5cb-160">This cmdlet removes permissions for the key vault that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmail, ForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc5cb-161">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cc5cb-161">-Confirm</span></span>
<span data-ttu-id="cc5cb-162">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc5cb-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc5cb-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc5cb-163">-WhatIf</span></span>
<span data-ttu-id="cc5cb-164">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc5cb-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc5cb-165">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cc5cb-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc5cb-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc5cb-166">CommonParameters</span></span>
<span data-ttu-id="cc5cb-167">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc5cb-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc5cb-168">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc5cb-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc5cb-169">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cc5cb-169">INPUTS</span></span>

### <span data-ttu-id="cc5cb-170">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="cc5cb-170">None</span></span>
<span data-ttu-id="cc5cb-171">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="cc5cb-171">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cc5cb-172">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cc5cb-172">OUTPUTS</span></span>

### <span data-ttu-id="cc5cb-173">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="cc5cb-173">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="cc5cb-174">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cc5cb-174">NOTES</span></span>

## <span data-ttu-id="cc5cb-175">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cc5cb-175">RELATED LINKS</span></span>

[<span data-ttu-id="cc5cb-176">Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="cc5cb-176">Set-AzureRmKeyVaultAccessPolicy</span></span>](./Set-AzureRmKeyVaultAccessPolicy.md)

