---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/update-AzKeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: ea3d16ec55186017852df30f6ff745f79703f224
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892990"
---
# <span data-ttu-id="680fc-101">Update-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="680fc-101">Update-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="680fc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="680fc-102">SYNOPSIS</span></span>
<span data-ttu-id="680fc-103">Aktualizowanie edytowalnych atrybutów konta usługi Azure Storage zarządzanego w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="680fc-103">Update editable attributes of a Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="680fc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="680fc-104">SYNTAX</span></span>

```
Update-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-ActiveKeyName <String>] [-AutoRegenerateKey <Boolean>] [-RegenerationPeriod <TimeSpan>] [-Enable <Boolean>]
 [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="680fc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="680fc-105">DESCRIPTION</span></span>
<span data-ttu-id="680fc-106">Zaktualizuj atrybuty edytowalne magazynu kluczy zarządzanego na koncie usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="680fc-106">Update the editable attributes of a Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="680fc-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="680fc-107">EXAMPLES</span></span>

### <span data-ttu-id="680fc-108">Przykład 1: aktualizowanie aktywnego klucza na key2 ' na koncie usługi Azure Storage zarządzanego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="680fc-108">Example 1:Update the active key to 'key2' on a Key Vault managed Azure Storage Account.</span></span>
```
PS C:\> Update-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -ActiveKeyName 'key2'
```

<span data-ttu-id="680fc-109">Aktualizuje klucz aktywny konta usługi Azure Storage zarządzanego w magazynie kluczy na "key2".</span><span class="sxs-lookup"><span data-stu-id="680fc-109">Updates the Key Vault managed Azure Storage Account active key to 'key2'.</span></span> <span data-ttu-id="680fc-110">do generowania tokenów SAS po tej aktualizacji zostanie użyte "key2".</span><span class="sxs-lookup"><span data-stu-id="680fc-110">'key2' will be used to generate SAS tokens after this update.</span></span>

## <span data-ttu-id="680fc-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="680fc-111">PARAMETERS</span></span>

### <span data-ttu-id="680fc-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="680fc-112">-AccountName</span></span>
<span data-ttu-id="680fc-113">Nazwa konta magazynu zarządzanego w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="680fc-113">Key Vault managed storage account name.</span></span> <span data-ttu-id="680fc-114">Polecenie cmdlet tworzy nazwę FQDN nazwy konta zarządzanego magazynu na podstawie nazwy magazynu, obecnie wybranego środowiska i zarządzanej nazwy konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="680fc-114">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="680fc-115">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="680fc-115">-ActiveKeyName</span></span>
<span data-ttu-id="680fc-116">Nazwa aktywnego klucza.</span><span class="sxs-lookup"><span data-stu-id="680fc-116">Active key name.</span></span>
<span data-ttu-id="680fc-117">Jeśli nie określono tej wartości, istniejąca wartość nazwy aktywnego klucza zarządzanego konta magazynu pozostanie niezmieniona</span><span class="sxs-lookup"><span data-stu-id="680fc-117">If not specified, the existing value of managed storage account's active key name remains unchanged</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="680fc-118">-AutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="680fc-118">-AutoRegenerateKey</span></span>
<span data-ttu-id="680fc-119">Automatyczne generowanie klucza.</span><span class="sxs-lookup"><span data-stu-id="680fc-119">Auto regenerate key.</span></span>
<span data-ttu-id="680fc-120">Jeśli nie podano, istniejąca wartość klucza automatycznego ponownego generowania konta magazynu zarządzanego nie jest zmieniana</span><span class="sxs-lookup"><span data-stu-id="680fc-120">If not specified, the existing value of auto regenerate key of managed storage account remains unchanged</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="680fc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="680fc-121">-DefaultProfile</span></span>
<span data-ttu-id="680fc-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="680fc-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="680fc-123">-Enable</span><span class="sxs-lookup"><span data-stu-id="680fc-123">-Enable</span></span>
<span data-ttu-id="680fc-124">Jeśli ta funkcja jest dostępna, umożliwia użycie klucza zarządzanego konta magazynu na potrzeby generowania tokenów SAS, jeśli wartość jest równa prawda.</span><span class="sxs-lookup"><span data-stu-id="680fc-124">If present, enables a use of a managed storage account key for sas token generation if value is true.</span></span> <span data-ttu-id="680fc-125">Wyłącza użycie klucza zarządzanego konta magazynu na potrzeby generowania tokenów SAS, jeśli wartość jest równa FAŁSZ.</span><span class="sxs-lookup"><span data-stu-id="680fc-125">Disables use of a managed storage account key for sas token generation if value is false.</span></span> <span data-ttu-id="680fc-126">Jeśli nie określono tej wartości, istniejąca wartość w stanie włączony/wyłączony konta magazynu pozostanie niezmieniona.</span><span class="sxs-lookup"><span data-stu-id="680fc-126">If not specified, the existing value of the storage account's enabled/disabled state remains unchanged.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="680fc-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="680fc-127">-PassThru</span></span>
<span data-ttu-id="680fc-128">Polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="680fc-128">Cmdlet does not return object by default.</span></span> <span data-ttu-id="680fc-129">Jeśli ten przełącznik jest określony, zwrotny obiekt konta magazynu zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="680fc-129">If this switch is specified, return managed storage account object.</span></span>

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

### <span data-ttu-id="680fc-130">-RegenerationPeriod</span><span class="sxs-lookup"><span data-stu-id="680fc-130">-RegenerationPeriod</span></span>
<span data-ttu-id="680fc-131">Okres regeneracji.</span><span class="sxs-lookup"><span data-stu-id="680fc-131">Regeneration period.</span></span> <span data-ttu-id="680fc-132">Jeśli klucz automatycznego ponownego generowania jest włączony, ta wartość określa przedział czasu, po którym nieaktywny klucz konta zarządzanej przestrzeni dyskowej zostanie automatycznie wygenerowany ponownie i stanie się aktywny.</span><span class="sxs-lookup"><span data-stu-id="680fc-132">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the active key.</span></span> <span data-ttu-id="680fc-133">Jeśli nie podano tego parametru, istniejąca wartość okresu regeneracji kluczy z zarządzanego konta magazynu pozostanie niezmieniona</span><span class="sxs-lookup"><span data-stu-id="680fc-133">If not specified, the existing value of regeneration period of keys of managed storage account remains unchanged</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="680fc-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="680fc-134">-Tag</span></span>
<span data-ttu-id="680fc-135">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="680fc-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="680fc-136">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="680fc-136">For example:</span></span>

<span data-ttu-id="680fc-137">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="680fc-137">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="680fc-138">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="680fc-138">-VaultName</span></span>
<span data-ttu-id="680fc-139">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="680fc-139">Vault name.</span></span>
<span data-ttu-id="680fc-140">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="680fc-140">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="680fc-141">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="680fc-141">-Confirm</span></span>
<span data-ttu-id="680fc-142">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="680fc-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="680fc-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="680fc-143">-WhatIf</span></span>
<span data-ttu-id="680fc-144">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="680fc-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="680fc-145">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="680fc-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="680fc-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="680fc-146">CommonParameters</span></span>
<span data-ttu-id="680fc-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="680fc-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="680fc-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="680fc-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="680fc-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="680fc-149">INPUTS</span></span>

### <span data-ttu-id="680fc-150">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="680fc-150">None</span></span>
<span data-ttu-id="680fc-151">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="680fc-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="680fc-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="680fc-152">OUTPUTS</span></span>

### <span data-ttu-id="680fc-153">Microsoft. Azure. Commands. platforming. models. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="680fc-153">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="680fc-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="680fc-154">NOTES</span></span>

## <span data-ttu-id="680fc-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="680fc-155">RELATED LINKS</span></span>

[<span data-ttu-id="680fc-156">AZ.</span><span class="sxs-lookup"><span data-stu-id="680fc-156">Az.KeyVault</span></span>](/powershell/module/Az.keyvault)
