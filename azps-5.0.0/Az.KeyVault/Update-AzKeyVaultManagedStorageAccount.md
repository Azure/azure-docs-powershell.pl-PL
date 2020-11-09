---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 72d23725f537df4f3e2244e799437394496bf434
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304572"
---
# <span data-ttu-id="5ef11-101">Update-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5ef11-101">Update-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="5ef11-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5ef11-102">SYNOPSIS</span></span>
<span data-ttu-id="5ef11-103">Aktualizowanie edytowalnych atrybutów konta usługi Azure Storage zarządzanego w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="5ef11-103">Update editable attributes of a Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="5ef11-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5ef11-104">SYNTAX</span></span>

### <span data-ttu-id="5ef11-105">ByDefinitionName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5ef11-105">ByDefinitionName (Default)</span></span>
```
Update-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-ActiveKeyName <String>]
 [-AutoRegenerateKey <Boolean>] [-RegenerationPeriod <TimeSpan>] [-Enable <Boolean>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ef11-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5ef11-106">ByInputObject</span></span>
```
Update-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-ActiveKeyName <String>] [-AutoRegenerateKey <Boolean>] [-RegenerationPeriod <TimeSpan>] [-Enable <Boolean>]
 [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5ef11-107">Opis</span><span class="sxs-lookup"><span data-stu-id="5ef11-107">DESCRIPTION</span></span>
<span data-ttu-id="5ef11-108">Zaktualizuj atrybuty edytowalne magazynu kluczy zarządzanego na koncie usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="5ef11-108">Update the editable attributes of a Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="5ef11-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5ef11-109">EXAMPLES</span></span>

### <span data-ttu-id="5ef11-110">Przykład 1: aktualizowanie aktywnego klucza na key2 ' na koncie usługi Azure Storage zarządzanego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="5ef11-110">Example 1: Update the active key to 'key2' on a Key Vault managed Azure Storage Account.</span></span>
```powershell
PS C:\> Update-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -ActiveKeyName 'key2'

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Active Key Name     : key2
Auto Regenerate Key : True
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 5/21/2018 11:55:58 PM
Updated             : 5/21/2018 11:55:58 PM
Tags                :
```

<span data-ttu-id="5ef11-111">Aktualizuje klucz aktywny konta usługi Azure Storage zarządzanego w magazynie kluczy na "key2".</span><span class="sxs-lookup"><span data-stu-id="5ef11-111">Updates the Key Vault managed Azure Storage Account active key to 'key2'.</span></span> <span data-ttu-id="5ef11-112">do generowania tokenów SAS po tej aktualizacji zostanie użyte "key2".</span><span class="sxs-lookup"><span data-stu-id="5ef11-112">'key2' will be used to generate SAS tokens after this update.</span></span>

### <span data-ttu-id="5ef11-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="5ef11-113">Example 2</span></span>

<span data-ttu-id="5ef11-114">Aktualizowanie edytowalnych atrybutów konta usługi Azure Storage zarządzanego w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="5ef11-114">Update editable attributes of a Key Vault managed Azure Storage Account.</span></span> <span data-ttu-id="5ef11-115">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="5ef11-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Update-AzKeyVaultManagedStorageAccount -AccountName 'mystorageaccount' -AutoRegenerateKey $false -RegenerationPeriod $regenerationPeriod -VaultName 'myvault'
```

## <span data-ttu-id="5ef11-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5ef11-116">PARAMETERS</span></span>

### <span data-ttu-id="5ef11-117">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5ef11-117">-AccountName</span></span>
<span data-ttu-id="5ef11-118">Nazwa konta magazynu zarządzanego w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="5ef11-118">Key Vault managed storage account name.</span></span> <span data-ttu-id="5ef11-119">Polecenie cmdlet tworzy nazwę FQDN nazwy konta zarządzanego magazynu na podstawie nazwy magazynu, obecnie wybranego środowiska i zarządzanej nazwy konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="5ef11-119">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ef11-120">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="5ef11-120">-ActiveKeyName</span></span>
<span data-ttu-id="5ef11-121">Nazwa aktywnego klucza.</span><span class="sxs-lookup"><span data-stu-id="5ef11-121">Active key name.</span></span>
<span data-ttu-id="5ef11-122">Jeśli nie określono tej wartości, istniejąca wartość nazwy aktywnego klucza zarządzanego konta magazynu pozostanie niezmieniona</span><span class="sxs-lookup"><span data-stu-id="5ef11-122">If not specified, the existing value of managed storage account's active key name remains unchanged</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ef11-123">-AutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="5ef11-123">-AutoRegenerateKey</span></span>
<span data-ttu-id="5ef11-124">Automatyczne generowanie klucza.</span><span class="sxs-lookup"><span data-stu-id="5ef11-124">Auto regenerate key.</span></span>
<span data-ttu-id="5ef11-125">Jeśli nie podano, istniejąca wartość klucza automatycznego ponownego generowania konta magazynu zarządzanego nie jest zmieniana</span><span class="sxs-lookup"><span data-stu-id="5ef11-125">If not specified, the existing value of auto regenerate key of managed storage account remains unchanged</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ef11-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ef11-126">-DefaultProfile</span></span>
<span data-ttu-id="5ef11-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="5ef11-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5ef11-128">-Enable</span><span class="sxs-lookup"><span data-stu-id="5ef11-128">-Enable</span></span>
<span data-ttu-id="5ef11-129">Jeśli ta funkcja jest dostępna, umożliwia użycie klucza zarządzanego konta magazynu na potrzeby generowania tokenów SAS, jeśli wartość jest równa prawda.</span><span class="sxs-lookup"><span data-stu-id="5ef11-129">If present, enables a use of a managed storage account key for sas token generation if value is true.</span></span> <span data-ttu-id="5ef11-130">Wyłącza użycie klucza zarządzanego konta magazynu na potrzeby generowania tokenów SAS, jeśli wartość jest równa FAŁSZ.</span><span class="sxs-lookup"><span data-stu-id="5ef11-130">Disables use of a managed storage account key for sas token generation if value is false.</span></span> <span data-ttu-id="5ef11-131">Jeśli nie określono tej wartości, istniejąca wartość w stanie włączony/wyłączony konta magazynu pozostanie niezmieniona.</span><span class="sxs-lookup"><span data-stu-id="5ef11-131">If not specified, the existing value of the storage account's enabled/disabled state remains unchanged.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ef11-132">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5ef11-132">-InputObject</span></span>
<span data-ttu-id="5ef11-133">Obiekt ManagedStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="5ef11-133">ManagedStorageAccount object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ef11-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5ef11-134">-PassThru</span></span>
<span data-ttu-id="5ef11-135">Polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="5ef11-135">Cmdlet does not return object by default.</span></span> <span data-ttu-id="5ef11-136">Jeśli ten przełącznik jest określony, zwrotny obiekt konta magazynu zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="5ef11-136">If this switch is specified, return managed storage account object.</span></span>

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

### <span data-ttu-id="5ef11-137">-RegenerationPeriod</span><span class="sxs-lookup"><span data-stu-id="5ef11-137">-RegenerationPeriod</span></span>
<span data-ttu-id="5ef11-138">Okres regeneracji.</span><span class="sxs-lookup"><span data-stu-id="5ef11-138">Regeneration period.</span></span> <span data-ttu-id="5ef11-139">Jeśli klucz automatycznego ponownego generowania jest włączony, ta wartość określa przedział czasu, po którym nieaktywny klucz konta zarządzanej przestrzeni dyskowej zostanie automatycznie wygenerowany ponownie i stanie się aktywny.</span><span class="sxs-lookup"><span data-stu-id="5ef11-139">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the active key.</span></span> <span data-ttu-id="5ef11-140">Jeśli nie podano tego parametru, istniejąca wartość okresu regeneracji kluczy z zarządzanego konta magazynu pozostanie niezmieniona</span><span class="sxs-lookup"><span data-stu-id="5ef11-140">If not specified, the existing value of regeneration period of keys of managed storage account remains unchanged</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ef11-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="5ef11-141">-Tag</span></span>
<span data-ttu-id="5ef11-142">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="5ef11-142">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5ef11-143">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="5ef11-143">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ef11-144">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="5ef11-144">-VaultName</span></span>
<span data-ttu-id="5ef11-145">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="5ef11-145">Vault name.</span></span>
<span data-ttu-id="5ef11-146">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="5ef11-146">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ef11-147">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5ef11-147">-Confirm</span></span>
<span data-ttu-id="5ef11-148">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ef11-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ef11-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ef11-149">-WhatIf</span></span>
<span data-ttu-id="5ef11-150">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ef11-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ef11-151">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5ef11-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ef11-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ef11-152">CommonParameters</span></span>
<span data-ttu-id="5ef11-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ef11-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ef11-154">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ef11-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ef11-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5ef11-155">INPUTS</span></span>

### <span data-ttu-id="5ef11-156">Microsoft. Azure. Commands. platforming. models. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="5ef11-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="5ef11-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5ef11-157">OUTPUTS</span></span>

### <span data-ttu-id="5ef11-158">Microsoft. Azure. Commands. platforming. models. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5ef11-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="5ef11-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5ef11-159">NOTES</span></span>

## <span data-ttu-id="5ef11-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5ef11-160">RELATED LINKS</span></span>

[<span data-ttu-id="5ef11-161">AZ.</span><span class="sxs-lookup"><span data-stu-id="5ef11-161">Az.KeyVault</span></span>](/powershell/module/az.keyvault)
