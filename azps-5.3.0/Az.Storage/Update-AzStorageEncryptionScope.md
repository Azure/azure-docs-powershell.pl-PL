---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageencryptionscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageEncryptionScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageEncryptionScope.md
ms.openlocfilehash: 6c8f07cbdb70b84d235afa7ce953da0bac477f55
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375949"
---
# <span data-ttu-id="8707d-101">Update-AzStorageEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="8707d-101">Update-AzStorageEncryptionScope</span></span>

## <span data-ttu-id="8707d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8707d-102">SYNOPSIS</span></span>
<span data-ttu-id="8707d-103">Modyfikowanie zakresu szyfrowania dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="8707d-103">Modify an encryption scope for a Storage account.</span></span>

## <span data-ttu-id="8707d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8707d-104">SYNTAX</span></span>

### <span data-ttu-id="8707d-105">AccountName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="8707d-105">AccountName (Default)</span></span>
```
Update-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-StorageEncryption] [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8707d-106">AccountNameKeyVault</span><span class="sxs-lookup"><span data-stu-id="8707d-106">AccountNameKeyVault</span></span>
```
Update-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-KeyvaultEncryption] -KeyUri <String> [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8707d-107">AccountName</span><span class="sxs-lookup"><span data-stu-id="8707d-107">AccountObject</span></span>
```
Update-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-StorageEncryption] [-State <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8707d-108">AccountObjectKeyVault</span><span class="sxs-lookup"><span data-stu-id="8707d-108">AccountObjectKeyVault</span></span>
```
Update-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-KeyvaultEncryption] -KeyUri <String> [-State <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8707d-109">EncryptionScopeObject</span><span class="sxs-lookup"><span data-stu-id="8707d-109">EncryptionScopeObject</span></span>
```
Update-AzStorageEncryptionScope -InputObject <PSEncryptionScope> [-StorageEncryption] [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8707d-110">EncryptionScopeObjectKeyVault</span><span class="sxs-lookup"><span data-stu-id="8707d-110">EncryptionScopeObjectKeyVault</span></span>
```
Update-AzStorageEncryptionScope -InputObject <PSEncryptionScope> [-KeyvaultEncryption] -KeyUri <String>
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8707d-111">Opis</span><span class="sxs-lookup"><span data-stu-id="8707d-111">DESCRIPTION</span></span>
<span data-ttu-id="8707d-112">Polecenie cmdlet **Update-AzStorageEncryptionScope** modyfikuje zakres szyfrowania dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="8707d-112">The **Update-AzStorageEncryptionScope** cmdlet modifies an encryption scope for a Storage account.</span></span>

## <span data-ttu-id="8707d-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8707d-113">EXAMPLES</span></span>

### <span data-ttu-id="8707d-114">Przykład 1: wyłączanie zakresu szyfrowania</span><span class="sxs-lookup"><span data-stu-id="8707d-114">Example 1: Disable an encryption scope</span></span>
```
PS C:\> Update-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"  -EncryptionScopeName testscope -State Disabled 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source            KeyVaultKeyUri                                                                          
----      -----    ------            --------------                                                                          
testscope Disabled Microsoft.Storage
```

<span data-ttu-id="8707d-115">To polecenie wyłącza zakres szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="8707d-115">This command disables an encryption scope.</span></span>

### <span data-ttu-id="8707d-116">Przykład 2: Włączanie zakresu szyfrowania</span><span class="sxs-lookup"><span data-stu-id="8707d-116">Example 2: Enable an encryption scope</span></span>
```
PS C:\> Update-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"  -EncryptionScopeName testscope -State Enabled 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source            KeyVaultKeyUri                                                                          
----      -----    ------            --------------                                                                          
testscope Enabled  Microsoft.Storage
```

<span data-ttu-id="8707d-117">To polecenie włącza zakres szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="8707d-117">This command enables an encryption scope.</span></span>

### <span data-ttu-id="8707d-118">Przykład 3: aktualizowanie zakresu szyfrowania w celu użycia szyfrowania magazynu</span><span class="sxs-lookup"><span data-stu-id="8707d-118">Example 3: Update an encryption scope to use Storage Encryption</span></span>
```
PS C:\> Update-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"  -EncryptionScopeName testscope -StorageEncryption

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source            KeyVaultKeyUri                                         
----      -----    ------            --------------                                         
testscope Enabled  Microsoft.Storage
```

<span data-ttu-id="8707d-119">To polecenie umożliwia zaktualizowanie zakresu szyfrowania w celu użycia szyfrowania magazynu.</span><span class="sxs-lookup"><span data-stu-id="8707d-119">This command updates an encryption scope to use Storage Encryption.</span></span>

### <span data-ttu-id="8707d-120">Przykład 4: aktualizowanie zakresu szyfrowania w celu używania szyfrowania opartego na magazynie</span><span class="sxs-lookup"><span data-stu-id="8707d-120">Example 4: Update an encryption scope to use Keyvault Encryption</span></span>
```
PS C:\> Update-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EncryptionScopeName testscope -KeyvaultEncryption -KeyUri "https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source             KeyVaultKeyUri                                         
----      -----    ------             --------------                                         
testscope Enabled  Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57
```

<span data-ttu-id="8707d-121">To polecenie updtaes zakres szyfrowania w celu korzystania z szyfrowania magazynu.</span><span class="sxs-lookup"><span data-stu-id="8707d-121">This command updtaes an encryption scope to use Keyvault Encryption.</span></span>
<span data-ttu-id="8707d-122">Tożsamość konta magazynu musi mieć uprawnienia Get, wrapkey, unwrapkey dla klucza magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="8707d-122">The Storage account Identity need have get,wrapkey,unwrapkey permissions to the keyvault key.</span></span>

## <span data-ttu-id="8707d-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8707d-123">PARAMETERS</span></span>

### <span data-ttu-id="8707d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8707d-124">-DefaultProfile</span></span>
<span data-ttu-id="8707d-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8707d-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8707d-126">-EncryptionScopeName</span><span class="sxs-lookup"><span data-stu-id="8707d-126">-EncryptionScopeName</span></span>
<span data-ttu-id="8707d-127">Nazwa usługi Azure Storage EncryptionScope</span><span class="sxs-lookup"><span data-stu-id="8707d-127">Azure Storage EncryptionScope name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountNameKeyVault, AccountObject, AccountObjectKeyVault
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8707d-128">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8707d-128">-InputObject</span></span>
<span data-ttu-id="8707d-129">Obiekt EncryptionScope</span><span class="sxs-lookup"><span data-stu-id="8707d-129">EncryptionScope object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope
Parameter Sets: EncryptionScopeObject, EncryptionScopeObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8707d-130">-KeyUri</span><span class="sxs-lookup"><span data-stu-id="8707d-130">-KeyUri</span></span>
<span data-ttu-id="8707d-131">Kluczowy identyfikator URI</span><span class="sxs-lookup"><span data-stu-id="8707d-131">The key Uri</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameKeyVault, AccountObjectKeyVault, EncryptionScopeObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8707d-132">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="8707d-132">-KeyvaultEncryption</span></span>
<span data-ttu-id="8707d-133">Tworzenie zakresu szyfrowania za pomocą źródła klucza Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8707d-133">Create encryption scope with keySource as Microsoft.Keyvault</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountNameKeyVault, AccountObjectKeyVault, EncryptionScopeObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8707d-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8707d-134">-ResourceGroupName</span></span>
<span data-ttu-id="8707d-135">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8707d-135">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountNameKeyVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8707d-136">-State</span><span class="sxs-lookup"><span data-stu-id="8707d-136">-State</span></span>
<span data-ttu-id="8707d-137">Aktualizuj stan zakresu szyfrowania, możliwe wartości obejmują: "włączony", "wyłączony".</span><span class="sxs-lookup"><span data-stu-id="8707d-137">Update encryption scope State, Possible values include: 'Enabled', 'Disabled'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8707d-138">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="8707d-138">-StorageAccount</span></span>
<span data-ttu-id="8707d-139">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="8707d-139">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject, AccountObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8707d-140">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8707d-140">-StorageAccountName</span></span>
<span data-ttu-id="8707d-141">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="8707d-141">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountNameKeyVault
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8707d-142">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="8707d-142">-StorageEncryption</span></span>
<span data-ttu-id="8707d-143">Utwórz zakres szyfrowania za pomocą źródła klucza Microsoft. Storage.</span><span class="sxs-lookup"><span data-stu-id="8707d-143">Create encryption scope with keySource as Microsoft.Storage.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountName, AccountObject, EncryptionScopeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8707d-144">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8707d-144">-Confirm</span></span>
<span data-ttu-id="8707d-145">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8707d-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8707d-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8707d-146">-WhatIf</span></span>
<span data-ttu-id="8707d-147">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8707d-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8707d-148">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8707d-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8707d-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8707d-149">CommonParameters</span></span>
<span data-ttu-id="8707d-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8707d-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8707d-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8707d-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8707d-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8707d-152">INPUTS</span></span>

### <span data-ttu-id="8707d-153">Microsoft. Azure. Commands. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8707d-153">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="8707d-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8707d-154">OUTPUTS</span></span>

### <span data-ttu-id="8707d-155">Microsoft. Azure. Commands. Management. Storage. models. PSEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="8707d-155">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span></span>

## <span data-ttu-id="8707d-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8707d-156">NOTES</span></span>

## <span data-ttu-id="8707d-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8707d-157">RELATED LINKS</span></span>
