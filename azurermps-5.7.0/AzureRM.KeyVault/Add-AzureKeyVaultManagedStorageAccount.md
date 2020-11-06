---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 526472514be086118f8c5ed74cefb6983ad67065
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542583"
---
# Add-AzureKeyVaultManagedStorageAccount

## STRESZCZENIe
Umożliwia dodanie istniejącego konta usługi Azure Storage do określonego magazynu kluczy dla swoich kluczy, które mają być zarządzane przez usługę magazynu kluczy.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Add-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-AccountResourceId] <String> [-ActiveKeyName] <String> [-DisableAutoRegenerateKey]
 [-RegenerationPeriod <TimeSpan>] [-Disable] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Skonfiguruj istniejące konto usługi Azure Storage, korzystając z magazynu kluczy na potrzeby kluczy konta magazynu, które mają być zarządzane przez Magazyn kluczy. Konto magazynu musi już istnieć. Klucze magazynowania nigdy nie są narażone na dzwonienie.
Automatyczne ponowne generowanie magazynu kluczy i przełączanie aktywnego klucza na podstawie okresu regeneracji.

## Przykłady

### Przykład 1: Ustawianie konta usługi Azure Storage za pomocą magazynu kluczy do zarządzania kluczami
```
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -ResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount' -ActiveKeyName 'key1' -RegenerationPeriod $regenerationPeriod
```

Ustawia konto magazynu z kluczowym magazynem dla swoich kluczy, które mają być zarządzane przez Magazyn kluczy. Aktywnym zestawem kluczy jest "KEY1". Ten klucz zostanie wykorzystany do wygenerowania tokenów SAS. Po upływie czasu tego polecenia Magazyn kluczy będzie ponownie generował klucz "key2", a następnie ustawił go jako aktywny klucz. Ten proces automatycznego ponownego generowania będzie kontynuowany między "KEY1" a "key2" z przerwą 90 dni.

### Przykład 2: Ustawianie klasycznego konta magazynu platformy Azure za pomocą magazynu kluczy do zarządzania kluczami
```
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -ResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount' -ActiveKeyName 'Primary' -RegenerationPeriod $regenerationPeriod
```

Umożliwia ustawienie klasycznego konta magazynu za pomocą magazynu kluczy na potrzeby zarządzania kluczami w magazynie kluczy. Aktywnym zestawem kluczy jest "podstawowy". Ten klucz zostanie wykorzystany do wygenerowania tokenów SAS. Po upływie czasu tego polecenia Magazyn kluczy ponownie wygeneruje klucz pomocniczy po okresie ponownego generowania i ustawi go jako aktywny. Ten proces automatycznego ponownego generowania będzie kontynuowany między "podstawowy" a "drugorzędny" z przerwą 90 dni.

## PARAMETRÓW

### -AccountName
Nazwa konta magazynu zarządzanego w magazynie kluczy. Polecenie cmdlet tworzy nazwę FQDN nazwy konta zarządzanego magazynu na podstawie nazwy magazynu, obecnie wybranego środowiska i zarządzanej nazwy konta magazynu.

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

### -AccountResourceId
Identyfikator zasobu platformy Azure konta magazynu.

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

### -ActiveKeyName
Nazwa klucza konta magazynu, który musi być wykorzystywany do generowania tokenów SAS.

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

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure

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

### -Disable
Wyłącza używanie klucza zarządzanych kont magazynu na potrzeby generowania tokenów SAS.

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

### -DisableAutoRegenerateKey
Automatyczne generowanie klucza. Jeśli prawda, nieaktywny klucz konta magazynu zarządzanego jest automatycznie regenerowany i staje się nowym kluczem po upływie okresu regeneracji. Jeśli wartość false, klucze zarządzanego konta magazynu nie są automatycznie generowane ponownie.

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

### -RegenerationPeriod
Okres regeneracji. Jeśli klucz automatycznego ponownego generowania jest włączony, ta wartość określa przedział czasu, po którym nieaktywny klucz konta zarządzanej przestrzeni dyskowej zostanie automatycznie wygenerowany ponownie i stanie się nowym aktywnym kluczem.

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

### -Tag
Pary klucz-wartość w formie tabeli skrótów. Na przykład:

@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}

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

### -Magazynname
Nazwa magazynu.
Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.

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

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

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

### -WhatIf
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.
Polecenie cmdlet nie jest uruchamiane.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono
To polecenie cmdlet nie akceptuje żadnych danych wejściowych.

## WYSYŁA

### Microsoft. Azure. Commands. platforming. models. ManagedStorageAccount

## INFORMACYJN

## LINKI POKREWNE

[AzureRM.](/powershell/module/azurerm.keyvault)
