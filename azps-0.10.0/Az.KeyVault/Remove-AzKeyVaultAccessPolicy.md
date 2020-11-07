---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: AE7B103B-23ED-4A66-A0DC-14FB0DF38FA8
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-Azkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultAccessPolicy.md
ms.openlocfilehash: f5cd00e0ef8e8936a4c87ee313054ae4c084a879
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/08/2020
ms.locfileid: "93899437"
---
# <span data-ttu-id="1c6eb-101">Remove-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1c6eb-101">Remove-AzKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="1c6eb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1c6eb-102">SYNOPSIS</span></span>
<span data-ttu-id="1c6eb-103">Usuwa wszystkie uprawnienia użytkownika lub aplikacji z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="1c6eb-103">Removes all permissions for a user or application from a key vault.</span></span>

## <span data-ttu-id="1c6eb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1c6eb-104">SYNTAX</span></span>

### <span data-ttu-id="1c6eb-105">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="1c6eb-105">ByServicePrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1c6eb-106">ByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="1c6eb-106">ByUserPrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -UserPrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1c6eb-107">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="1c6eb-107">ByObjectId</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1c6eb-108">ByEmail</span><span class="sxs-lookup"><span data-stu-id="1c6eb-108">ByEmail</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c6eb-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="1c6eb-109">ForVault</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-EnabledForDeployment] [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c6eb-110">Opis</span><span class="sxs-lookup"><span data-stu-id="1c6eb-110">DESCRIPTION</span></span>
<span data-ttu-id="1c6eb-111">Polecenie cmdlet **Remove-AzKeyVaultAccessPolicy** usuwa wszystkie uprawnienia użytkownika lub aplikacji albo dla wszystkich użytkowników i aplikacji z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="1c6eb-111">The **Remove-AzKeyVaultAccessPolicy** cmdlet removes all permissions for a user or application or for all users and applications from a key vault.</span></span>
<span data-ttu-id="1c6eb-112">Nawet jeśli usuniesz wszystkie uprawnienia, właściciel subskrypcji platformy Azure zawierającej Magazyn kluczy może dodawać uprawnienia do magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="1c6eb-112">Even if you remove all permissions, the owner of the Azure subscription that contains the key vault can add permissions to the key vault.</span></span>

<span data-ttu-id="1c6eb-113">Uwaga: chociaż określenie grupy zasobów jest opcjonalne dla tego polecenia cmdlet, należy to zrobić w celu uzyskania lepszej wydajności.</span><span class="sxs-lookup"><span data-stu-id="1c6eb-113">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="1c6eb-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1c6eb-114">EXAMPLES</span></span>

### <span data-ttu-id="1c6eb-115">Przykład 1: usuwanie uprawnień użytkownika</span><span class="sxs-lookup"><span data-stu-id="1c6eb-115">Example 1: Remove permissions for a user</span></span>
```
PS C:\>Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com'
```

<span data-ttu-id="1c6eb-116">To polecenie usuwa wszystkie uprawnienia użytkownika PattiFuller@contoso.com w magazynie kluczy o nazwie Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="1c6eb-116">This command removes all the permissions that a user PattiFuller@contoso.com has on the key vault named Contoso03Vault.</span></span>

### <span data-ttu-id="1c6eb-117">Przykład 2: usuwanie uprawnień do aplikacji</span><span class="sxs-lookup"><span data-stu-id="1c6eb-117">Example 2: Remove permissions for an application</span></span>
```
PS C:\>Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com'
```

<span data-ttu-id="1c6eb-118">To polecenie usuwa wszystkie uprawnienia aplikacji w magazynie kluczy o nazwie Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="1c6eb-118">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="1c6eb-119">W tym przykładzie zidentyfikowano aplikację przy użyciu nazwy głównej usługi zarejestrowanej w usłudze Azure Active Directory `http://payroll.contoso.com` .</span><span class="sxs-lookup"><span data-stu-id="1c6eb-119">This example identifies the application by using the service principal name registered in Azure Active Directory, `http://payroll.contoso.com`.</span></span>

### <span data-ttu-id="1c6eb-120">Przykład 3: usuwanie uprawnień do aplikacji przy użyciu jej identyfikatora obiektu</span><span class="sxs-lookup"><span data-stu-id="1c6eb-120">Example 3: Remove permissions for an application by using its object ID</span></span>
```
PS C:\>Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectID 34595082-9346-41b6-8d6b-295a2808b8db
```

<span data-ttu-id="1c6eb-121">To polecenie usuwa wszystkie uprawnienia aplikacji w magazynie kluczy o nazwie Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="1c6eb-121">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="1c6eb-122">W tym przykładzie aplikacja została zidentyfikowana przez identyfikator obiektu podmiotu usługi.</span><span class="sxs-lookup"><span data-stu-id="1c6eb-122">This example identifies the application by the object ID of the service principal.</span></span>

### <span data-ttu-id="1c6eb-123">Przykład 4: usuwanie uprawnień dla dostawcy zasobów Microsoft. COMPUTE</span><span class="sxs-lookup"><span data-stu-id="1c6eb-123">Example 4: Remove permissions for the Microsoft.Compute resource provider</span></span>
```
PS C:\>Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="1c6eb-124">To polecenie powoduje usunięcie uprawnień dla dostawcy zasobów Microsoft. COMPUTE w celu uzyskania kluczy tajnych z Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="1c6eb-124">This command removes permission for the Microsoft.Compute resource provider to get secrets from the Contoso03Vault.</span></span>

## <span data-ttu-id="1c6eb-125">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1c6eb-125">PARAMETERS</span></span>

### <span data-ttu-id="1c6eb-126">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="1c6eb-126">-ApplicationId</span></span>
<span data-ttu-id="1c6eb-127">Do użytku w przyszłości.</span><span class="sxs-lookup"><span data-stu-id="1c6eb-127">For future use.</span></span>

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

### <span data-ttu-id="1c6eb-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c6eb-128">-DefaultProfile</span></span>
<span data-ttu-id="1c6eb-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="1c6eb-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c6eb-130">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="1c6eb-130">-EmailAddress</span></span>
<span data-ttu-id="1c6eb-131">Określa adres e-mail użytkownika, którego dostęp należy usunąć.</span><span class="sxs-lookup"><span data-stu-id="1c6eb-131">Specifies the user email address of the user whose access you want to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByEmail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c6eb-132">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="1c6eb-132">-EnabledForDeployment</span></span>
<span data-ttu-id="1c6eb-133">Umożliwia dostawcy zasobów Microsoft. COMPUTE na pobieranie kluczy tajnych z tego magazynu kluczy, gdy do tego magazynu kluczy odwołuje się tworzenie zasobów, na przykład podczas tworzenia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1c6eb-133">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

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

### <span data-ttu-id="1c6eb-134">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="1c6eb-134">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="1c6eb-135">Umożliwia usłudze szyfrowania dysków Azure uzyskiwanie kluczy tajnych i ich odwinięcie z tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="1c6eb-135">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

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

### <span data-ttu-id="1c6eb-136">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="1c6eb-136">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="1c6eb-137">Umożliwia menedżerowi zasobów platformy Azure pobieranie kluczy tajnych z tego magazynu kluczy, gdy do tego magazynu kluczy odwołuje się wdrożenie szablonu.</span><span class="sxs-lookup"><span data-stu-id="1c6eb-137">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

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

### <span data-ttu-id="1c6eb-138">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="1c6eb-138">-ObjectId</span></span>
<span data-ttu-id="1c6eb-139">Określa identyfikator obiektu podmiotu użytkownika lub usługi w usłudze Azure Active Directory, dla którego należy usunąć uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="1c6eb-139">Specifies the object ID of the user or service principal in Azure Active Directory for which to remove permissions.</span></span>

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

### <span data-ttu-id="1c6eb-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1c6eb-140">-PassThru</span></span>
<span data-ttu-id="1c6eb-141">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="1c6eb-141">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1c6eb-142">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="1c6eb-142">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1c6eb-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c6eb-143">-ResourceGroupName</span></span>
<span data-ttu-id="1c6eb-144">Określa nazwę grupy zasobów skojarzonej z magazynem kluczy, którego zasady dostępu są modyfikowane.</span><span class="sxs-lookup"><span data-stu-id="1c6eb-144">Specifies the name of the resource group associated with the key vault whose access policy is being modified.</span></span>
<span data-ttu-id="1c6eb-145">Jeśli ta opcja nie jest określona, to polecenie cmdlet wyszukuje Magazyn kluczy w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1c6eb-145">If not specified, this cmdlet searches for the key vault in the current subscription.</span></span>

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

### <span data-ttu-id="1c6eb-146">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="1c6eb-146">-ServicePrincipalName</span></span>
<span data-ttu-id="1c6eb-147">Określa główną nazwę usługi aplikacji, której uprawnienia należy usunąć.</span><span class="sxs-lookup"><span data-stu-id="1c6eb-147">Specifies the service principal name of the application whose permissions you want to remove.</span></span>
<span data-ttu-id="1c6eb-148">Określ identyfikator aplikacji, określany także jako identyfikator klienta, zarejestrowany dla aplikacji w usłudze Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1c6eb-148">Specify the application ID, also known as client ID, registered for the application in Azure Active Directory.</span></span>

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

### <span data-ttu-id="1c6eb-149">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="1c6eb-149">-UserPrincipalName</span></span>
<span data-ttu-id="1c6eb-150">Określa główną nazwę użytkownika, którego dostęp należy usunąć.</span><span class="sxs-lookup"><span data-stu-id="1c6eb-150">Specifies the user principal name of the user whose access you want to remove.</span></span>

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

### <span data-ttu-id="1c6eb-151">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="1c6eb-151">-VaultName</span></span>
<span data-ttu-id="1c6eb-152">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="1c6eb-152">Specifies the name of the key vault.</span></span>
<span data-ttu-id="1c6eb-153">To polecenie cmdlet umożliwia usunięcie uprawnień do magazynu kluczy określanego przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="1c6eb-153">This cmdlet removes permissions for the key vault that this parameter specifies.</span></span>

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

### <span data-ttu-id="1c6eb-154">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1c6eb-154">-Confirm</span></span>
<span data-ttu-id="1c6eb-155">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c6eb-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c6eb-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c6eb-156">-WhatIf</span></span>
<span data-ttu-id="1c6eb-157">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c6eb-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c6eb-158">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1c6eb-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c6eb-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c6eb-159">CommonParameters</span></span>
<span data-ttu-id="1c6eb-160">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c6eb-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c6eb-161">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c6eb-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c6eb-162">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1c6eb-162">INPUTS</span></span>

### <span data-ttu-id="1c6eb-163">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="1c6eb-163">None</span></span>
<span data-ttu-id="1c6eb-164">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="1c6eb-164">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1c6eb-165">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1c6eb-165">OUTPUTS</span></span>

### <span data-ttu-id="1c6eb-166">Microsoft. Azure. Commands. platforming. models. PSVault</span><span class="sxs-lookup"><span data-stu-id="1c6eb-166">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

## <span data-ttu-id="1c6eb-167">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1c6eb-167">NOTES</span></span>

## <span data-ttu-id="1c6eb-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1c6eb-168">RELATED LINKS</span></span>

[<span data-ttu-id="1c6eb-169">Set-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1c6eb-169">Set-AzKeyVaultAccessPolicy</span></span>](./Set-AzKeyVaultAccessPolicy.md)

