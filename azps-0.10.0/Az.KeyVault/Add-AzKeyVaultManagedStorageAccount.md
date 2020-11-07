---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 85a0bc0f552688d036dc76ebbc6d15c608ade433
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893054"
---
# <span data-ttu-id="438a0-101">Add-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="438a0-101">Add-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="438a0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="438a0-102">SYNOPSIS</span></span>
<span data-ttu-id="438a0-103">Umożliwia dodanie istniejącego konta usługi Azure Storage do określonego magazynu kluczy dla swoich kluczy, które mają być zarządzane przez usługę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="438a0-103">Adds an existing Azure Storage Account to the specified key vault for its keys to be managed by the Key Vault service.</span></span>

## <span data-ttu-id="438a0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="438a0-104">SYNTAX</span></span>

```
Add-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-AccountResourceId] <String> [-ActiveKeyName] <String> [-DisableAutoRegenerateKey]
 [-RegenerationPeriod <TimeSpan>] [-Disable] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="438a0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="438a0-105">DESCRIPTION</span></span>
<span data-ttu-id="438a0-106">Skonfiguruj istniejące konto usługi Azure Storage, korzystając z magazynu kluczy na potrzeby kluczy konta magazynu, które mają być zarządzane przez Magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="438a0-106">Sets up an existing Azure Storage Account with Key Vault for Storage Account keys to be managed by Key Vault.</span></span> <span data-ttu-id="438a0-107">Konto magazynu musi już istnieć.</span><span class="sxs-lookup"><span data-stu-id="438a0-107">The Storage Account must already exist.</span></span> <span data-ttu-id="438a0-108">Klucze magazynowania nigdy nie są narażone na dzwonienie.</span><span class="sxs-lookup"><span data-stu-id="438a0-108">The Storage Keys are never exposed to caller.</span></span>
<span data-ttu-id="438a0-109">Automatyczne ponowne generowanie magazynu kluczy i przełączanie aktywnego klucza na podstawie okresu regeneracji.</span><span class="sxs-lookup"><span data-stu-id="438a0-109">Key Vault auto regenerates and switches the active key based on the regeneration period.</span></span>

## <span data-ttu-id="438a0-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="438a0-110">EXAMPLES</span></span>

### <span data-ttu-id="438a0-111">Przykład 1: Ustawianie konta usługi Azure Storage za pomocą magazynu kluczy do zarządzania kluczami</span><span class="sxs-lookup"><span data-stu-id="438a0-111">Example 1: Set an Azure Storage Account with Key Vault to manage its keys</span></span>
```
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -ResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount' -ActiveKeyName 'key1' -RegenerationPeriod $regenerationPeriod
```

<span data-ttu-id="438a0-112">Ustawia konto magazynu z kluczowym magazynem dla swoich kluczy, które mają być zarządzane przez Magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="438a0-112">Sets a Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="438a0-113">Aktywnym zestawem kluczy jest "KEY1".</span><span class="sxs-lookup"><span data-stu-id="438a0-113">The active key set is 'key1'.</span></span> <span data-ttu-id="438a0-114">Ten klucz zostanie wykorzystany do wygenerowania tokenów SAS.</span><span class="sxs-lookup"><span data-stu-id="438a0-114">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="438a0-115">Po upływie czasu tego polecenia Magazyn kluczy będzie ponownie generował klucz "key2", a następnie ustawił go jako aktywny klucz.</span><span class="sxs-lookup"><span data-stu-id="438a0-115">Key Vault will regenerate 'key2' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="438a0-116">Ten proces automatycznego ponownego generowania będzie kontynuowany między "KEY1" a "key2" z przerwą 90 dni.</span><span class="sxs-lookup"><span data-stu-id="438a0-116">This auto regeneration process will continue between 'key1' and 'key2' with a gap of 90 days.</span></span>

### <span data-ttu-id="438a0-117">Przykład 2: Ustawianie klasycznego konta magazynu platformy Azure za pomocą magazynu kluczy do zarządzania kluczami</span><span class="sxs-lookup"><span data-stu-id="438a0-117">Example 2: Set a Classic Azure Storage Account with Key Vault to manage its keys</span></span>
```
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -ResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount' -ActiveKeyName 'Primary' -RegenerationPeriod $regenerationPeriod
```

<span data-ttu-id="438a0-118">Umożliwia ustawienie klasycznego konta magazynu za pomocą magazynu kluczy na potrzeby zarządzania kluczami w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="438a0-118">Sets a Classic Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="438a0-119">Aktywnym zestawem kluczy jest "podstawowy".</span><span class="sxs-lookup"><span data-stu-id="438a0-119">The active key set is 'Primary'.</span></span> <span data-ttu-id="438a0-120">Ten klucz zostanie wykorzystany do wygenerowania tokenów SAS.</span><span class="sxs-lookup"><span data-stu-id="438a0-120">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="438a0-121">Po upływie czasu tego polecenia Magazyn kluczy ponownie wygeneruje klucz pomocniczy po okresie ponownego generowania i ustawi go jako aktywny.</span><span class="sxs-lookup"><span data-stu-id="438a0-121">Key Vault will regenerate 'Secondary' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="438a0-122">Ten proces automatycznego ponownego generowania będzie kontynuowany między "podstawowy" a "drugorzędny" z przerwą 90 dni.</span><span class="sxs-lookup"><span data-stu-id="438a0-122">This auto regeneration process will continue between 'Primary' and 'Secondary' with a gap of 90 days.</span></span>

## <span data-ttu-id="438a0-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="438a0-123">PARAMETERS</span></span>

### <span data-ttu-id="438a0-124">-AccountName</span><span class="sxs-lookup"><span data-stu-id="438a0-124">-AccountName</span></span>
<span data-ttu-id="438a0-125">Nazwa konta magazynu zarządzanego w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="438a0-125">Key Vault managed storage account name.</span></span> <span data-ttu-id="438a0-126">Polecenie cmdlet tworzy nazwę FQDN nazwy konta zarządzanego magazynu na podstawie nazwy magazynu, obecnie wybranego środowiska i zarządzanej nazwy konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="438a0-126">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="438a0-127">-AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="438a0-127">-AccountResourceId</span></span>
<span data-ttu-id="438a0-128">Identyfikator zasobu platformy Azure konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="438a0-128">Azure resource id of the storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountResourceId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="438a0-129">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="438a0-129">-ActiveKeyName</span></span>
<span data-ttu-id="438a0-130">Nazwa klucza konta magazynu, który musi być wykorzystywany do generowania tokenów SAS.</span><span class="sxs-lookup"><span data-stu-id="438a0-130">Name of the storage account key that must be used for generating sas tokens.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="438a0-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="438a0-131">-DefaultProfile</span></span>
<span data-ttu-id="438a0-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="438a0-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="438a0-133">-Disable</span><span class="sxs-lookup"><span data-stu-id="438a0-133">-Disable</span></span>
<span data-ttu-id="438a0-134">Wyłącza używanie klucza zarządzanych kont magazynu na potrzeby generowania tokenów SAS.</span><span class="sxs-lookup"><span data-stu-id="438a0-134">Disables the use of managed storage account's key for generation of sas tokens.</span></span>

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

### <span data-ttu-id="438a0-135">-DisableAutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="438a0-135">-DisableAutoRegenerateKey</span></span>
<span data-ttu-id="438a0-136">Automatyczne generowanie klucza.</span><span class="sxs-lookup"><span data-stu-id="438a0-136">Auto regenerate key.</span></span> <span data-ttu-id="438a0-137">Jeśli prawda, nieaktywny klucz konta magazynu zarządzanego jest automatycznie regenerowany i staje się nowym kluczem po upływie okresu regeneracji.</span><span class="sxs-lookup"><span data-stu-id="438a0-137">If true, then the managed storage account's inactive key gets auto regenerated and becomes the new active key after the regeneration period.</span></span> <span data-ttu-id="438a0-138">Jeśli wartość false, klucze zarządzanego konta magazynu nie są automatycznie generowane ponownie.</span><span class="sxs-lookup"><span data-stu-id="438a0-138">If false, then the keys of managed storage account are not auto regenerated.</span></span>

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

### <span data-ttu-id="438a0-139">-RegenerationPeriod</span><span class="sxs-lookup"><span data-stu-id="438a0-139">-RegenerationPeriod</span></span>
<span data-ttu-id="438a0-140">Okres regeneracji.</span><span class="sxs-lookup"><span data-stu-id="438a0-140">Regeneration period.</span></span> <span data-ttu-id="438a0-141">Jeśli klucz automatycznego ponownego generowania jest włączony, ta wartość określa przedział czasu, po którym nieaktywny klucz konta zarządzanej przestrzeni dyskowej zostanie automatycznie wygenerowany ponownie i stanie się nowym aktywnym kluczem.</span><span class="sxs-lookup"><span data-stu-id="438a0-141">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the new active key.</span></span>

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

### <span data-ttu-id="438a0-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="438a0-142">-Tag</span></span>
<span data-ttu-id="438a0-143">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="438a0-143">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="438a0-144">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="438a0-144">For example:</span></span>

<span data-ttu-id="438a0-145">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="438a0-145">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="438a0-146">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="438a0-146">-VaultName</span></span>
<span data-ttu-id="438a0-147">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="438a0-147">Vault name.</span></span>
<span data-ttu-id="438a0-148">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="438a0-148">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="438a0-149">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="438a0-149">-Confirm</span></span>
<span data-ttu-id="438a0-150">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="438a0-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="438a0-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="438a0-151">-WhatIf</span></span>
<span data-ttu-id="438a0-152">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="438a0-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="438a0-153">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="438a0-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="438a0-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="438a0-154">CommonParameters</span></span>
<span data-ttu-id="438a0-155">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="438a0-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="438a0-156">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="438a0-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="438a0-157">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="438a0-157">INPUTS</span></span>

### <span data-ttu-id="438a0-158">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="438a0-158">None</span></span>
<span data-ttu-id="438a0-159">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="438a0-159">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="438a0-160">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="438a0-160">OUTPUTS</span></span>

### <span data-ttu-id="438a0-161">Microsoft. Azure. Commands. platforming. models. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="438a0-161">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="438a0-162">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="438a0-162">NOTES</span></span>

## <span data-ttu-id="438a0-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="438a0-163">RELATED LINKS</span></span>

[<span data-ttu-id="438a0-164">AZ.</span><span class="sxs-lookup"><span data-stu-id="438a0-164">Az.KeyVault</span></span>](/powershell/module/Az.keyvault)
