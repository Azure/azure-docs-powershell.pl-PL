---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/update-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 1a21db1918d9baef48d3efd15dc72c2cb542a925
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545179"
---
# <span data-ttu-id="28b46-101">Update-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="28b46-101">Update-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="28b46-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="28b46-102">SYNOPSIS</span></span>
<span data-ttu-id="28b46-103">Aktualizowanie edytowalnych atrybutów konta usługi Azure Storage zarządzanego w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="28b46-103">Update editable attributes of a Key Vault managed Azure Storage Account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28b46-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="28b46-104">SYNTAX</span></span>

### <span data-ttu-id="28b46-105">ByDefinitionName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="28b46-105">ByDefinitionName (Default)</span></span>
```
Update-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-ActiveKeyName <String>] [-AutoRegenerateKey <Boolean>] [-RegenerationPeriod <TimeSpan>] [-Enable <Boolean>]
 [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="28b46-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="28b46-106">ByInputObject</span></span>
```
Update-AzureKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-ActiveKeyName <String>] [-AutoRegenerateKey <Boolean>] [-RegenerationPeriod <TimeSpan>] [-Enable <Boolean>]
 [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="28b46-107">Opis</span><span class="sxs-lookup"><span data-stu-id="28b46-107">DESCRIPTION</span></span>
<span data-ttu-id="28b46-108">Zaktualizuj atrybuty edytowalne magazynu kluczy zarządzanego na koncie usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="28b46-108">Update the editable attributes of a Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="28b46-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="28b46-109">EXAMPLES</span></span>

### <span data-ttu-id="28b46-110">Przykład 1: aktualizowanie aktywnego klucza na key2 ' na koncie usługi Azure Storage zarządzanego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="28b46-110">Example 1: Update the active key to 'key2' on a Key Vault managed Azure Storage Account.</span></span>
```powershell
PS C:\> Update-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -ActiveKeyName 'key2'

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

<span data-ttu-id="28b46-111">Aktualizuje klucz aktywny konta usługi Azure Storage zarządzanego w magazynie kluczy na "key2".</span><span class="sxs-lookup"><span data-stu-id="28b46-111">Updates the Key Vault managed Azure Storage Account active key to 'key2'.</span></span> <span data-ttu-id="28b46-112">do generowania tokenów SAS po tej aktualizacji zostanie użyte "key2".</span><span class="sxs-lookup"><span data-stu-id="28b46-112">'key2' will be used to generate SAS tokens after this update.</span></span>

## <span data-ttu-id="28b46-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="28b46-113">PARAMETERS</span></span>

### <span data-ttu-id="28b46-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="28b46-114">-AccountName</span></span>
<span data-ttu-id="28b46-115">Nazwa konta magazynu zarządzanego w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="28b46-115">Key Vault managed storage account name.</span></span> <span data-ttu-id="28b46-116">Polecenie cmdlet tworzy nazwę FQDN nazwy konta zarządzanego magazynu na podstawie nazwy magazynu, obecnie wybranego środowiska i zarządzanej nazwy konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="28b46-116">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="28b46-117">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="28b46-117">-ActiveKeyName</span></span>
<span data-ttu-id="28b46-118">Nazwa aktywnego klucza.</span><span class="sxs-lookup"><span data-stu-id="28b46-118">Active key name.</span></span>
<span data-ttu-id="28b46-119">Jeśli nie określono tej wartości, istniejąca wartość nazwy aktywnego klucza zarządzanego konta magazynu pozostanie niezmieniona</span><span class="sxs-lookup"><span data-stu-id="28b46-119">If not specified, the existing value of managed storage account's active key name remains unchanged</span></span>

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

### <span data-ttu-id="28b46-120">-AutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="28b46-120">-AutoRegenerateKey</span></span>
<span data-ttu-id="28b46-121">Automatyczne generowanie klucza.</span><span class="sxs-lookup"><span data-stu-id="28b46-121">Auto regenerate key.</span></span>
<span data-ttu-id="28b46-122">Jeśli nie podano, istniejąca wartość klucza automatycznego ponownego generowania konta magazynu zarządzanego nie jest zmieniana</span><span class="sxs-lookup"><span data-stu-id="28b46-122">If not specified, the existing value of auto regenerate key of managed storage account remains unchanged</span></span>

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

### <span data-ttu-id="28b46-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28b46-123">-DefaultProfile</span></span>
<span data-ttu-id="28b46-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="28b46-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="28b46-125">-Enable</span><span class="sxs-lookup"><span data-stu-id="28b46-125">-Enable</span></span>
<span data-ttu-id="28b46-126">Jeśli ta funkcja jest dostępna, umożliwia użycie klucza zarządzanego konta magazynu na potrzeby generowania tokenów SAS, jeśli wartość jest równa prawda.</span><span class="sxs-lookup"><span data-stu-id="28b46-126">If present, enables a use of a managed storage account key for sas token generation if value is true.</span></span> <span data-ttu-id="28b46-127">Wyłącza użycie klucza zarządzanego konta magazynu na potrzeby generowania tokenów SAS, jeśli wartość jest równa FAŁSZ.</span><span class="sxs-lookup"><span data-stu-id="28b46-127">Disables use of a managed storage account key for sas token generation if value is false.</span></span> <span data-ttu-id="28b46-128">Jeśli nie określono tej wartości, istniejąca wartość w stanie włączony/wyłączony konta magazynu pozostanie niezmieniona.</span><span class="sxs-lookup"><span data-stu-id="28b46-128">If not specified, the existing value of the storage account's enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="28b46-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="28b46-129">-InputObject</span></span>
<span data-ttu-id="28b46-130">Obiekt ManagedStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="28b46-130">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="28b46-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="28b46-131">-PassThru</span></span>
<span data-ttu-id="28b46-132">Polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="28b46-132">Cmdlet does not return object by default.</span></span> <span data-ttu-id="28b46-133">Jeśli ten przełącznik jest określony, zwrotny obiekt konta magazynu zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="28b46-133">If this switch is specified, return managed storage account object.</span></span>

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

### <span data-ttu-id="28b46-134">-RegenerationPeriod</span><span class="sxs-lookup"><span data-stu-id="28b46-134">-RegenerationPeriod</span></span>
<span data-ttu-id="28b46-135">Okres regeneracji.</span><span class="sxs-lookup"><span data-stu-id="28b46-135">Regeneration period.</span></span> <span data-ttu-id="28b46-136">Jeśli klucz automatycznego ponownego generowania jest włączony, ta wartość określa przedział czasu, po którym nieaktywny klucz konta zarządzanej przestrzeni dyskowej zostanie automatycznie wygenerowany ponownie i stanie się aktywny.</span><span class="sxs-lookup"><span data-stu-id="28b46-136">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the active key.</span></span> <span data-ttu-id="28b46-137">Jeśli nie podano tego parametru, istniejąca wartość okresu regeneracji kluczy z zarządzanego konta magazynu pozostanie niezmieniona</span><span class="sxs-lookup"><span data-stu-id="28b46-137">If not specified, the existing value of regeneration period of keys of managed storage account remains unchanged</span></span>

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

### <span data-ttu-id="28b46-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="28b46-138">-Tag</span></span>
<span data-ttu-id="28b46-139">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="28b46-139">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="28b46-140">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="28b46-140">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="28b46-141">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="28b46-141">-VaultName</span></span>
<span data-ttu-id="28b46-142">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="28b46-142">Vault name.</span></span>
<span data-ttu-id="28b46-143">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="28b46-143">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="28b46-144">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="28b46-144">-Confirm</span></span>
<span data-ttu-id="28b46-145">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28b46-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28b46-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28b46-146">-WhatIf</span></span>
<span data-ttu-id="28b46-147">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28b46-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28b46-148">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="28b46-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28b46-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28b46-149">CommonParameters</span></span>
<span data-ttu-id="28b46-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28b46-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28b46-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28b46-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28b46-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="28b46-152">INPUTS</span></span>

### <span data-ttu-id="28b46-153">Microsoft. Azure. Commands. platforming. models. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="28b46-153">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>
<span data-ttu-id="28b46-154">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="28b46-154">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="28b46-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="28b46-155">OUTPUTS</span></span>

### <span data-ttu-id="28b46-156">Microsoft. Azure. Commands. platforming. models. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="28b46-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="28b46-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="28b46-157">NOTES</span></span>

## <span data-ttu-id="28b46-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="28b46-158">RELATED LINKS</span></span>

[<span data-ttu-id="28b46-159">AzureRM.</span><span class="sxs-lookup"><span data-stu-id="28b46-159">AzureRM.KeyVault</span></span>](/powershell/module/azurerm.keyvault)
