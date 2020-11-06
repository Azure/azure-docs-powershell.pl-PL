---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 636FAD5B-8C39-4E5C-8978-6845C6B89BC0
online version: https://go.microsoft.com/fwlink/?LinkId=690163
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureRmKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureRmKeyVaultAccessPolicy.md
ms.openlocfilehash: 9ebf606a41a3a972b2d636846fbdc7834388ef29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553255"
---
# Set-AzureRmKeyVaultAccessPolicy

## STRESZCZENIe
Udziela lub modyfikuje istniejące uprawnienia dla użytkownika, aplikacji lub grupy zabezpieczeń w celu wykonania operacji za pomocą magazynu kluczy.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### ByServicePrincipalName
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByUserPrincipalName
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -UserPrincipalName <String> [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByObjectId
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByEmailAddress
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ForVault
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzureRmKeyVaultAccessPolicy** udziela lub modyfikuje istniejące uprawnienia dla użytkownika, aplikacji lub grupy zabezpieczeń w celu wykonania określonych operacji w magazynie kluczy.
W magazynie kluczy nie są modyfikowane uprawnienia innych użytkowników, aplikacji ani grup zabezpieczeń.

Jeśli ustawiasz uprawnienia dla grupy zabezpieczeń, ta operacja będzie miała wpływ tylko na użytkowników tej grupy zabezpieczeń.

Wszystkie następujące katalogi muszą być tego samego katalogu platformy Azure: 
- Katalog domyślny subskrypcji platformy Azure, w której znajduje się magazyn kluczy.
- Katalog platformy Azure zawierający użytkownika lub grupę aplikacji, do których udzielasz uprawnień.

Przykłady scenariuszy, w których te warunki nie są spełnione, a to polecenie cmdlet nie będzie działać: 

- Autoryzowanie użytkownika od innej organizacji do zarządzania magazynem kluczy.
Każda organizacja ma swój własny katalog. 
- Twoje konto platformy Azure ma wiele katalogów.
Jeśli zarejestrujesz aplikację w katalogu innym niż katalog domyślny, nie możesz autoryzować tej aplikacji do korzystania z Twojego magazynu kluczy.
Aplikacja musi znajdować się w katalogu domyślnym.

Uwaga: chociaż określenie grupy zasobów jest opcjonalne dla tego polecenia cmdlet, należy to zrobić w celu uzyskania lepszej wydajności.

## Przykłady

### Przykład 1: udzielanie uprawnień użytkownikowi w magazynie kluczy magazynu kluczy i modyfikowanie magazynu usługi permissionskey
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys create,import,delete,list -PermissionsToSecrets 'set,delete'
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets set,delete,get -PassThru
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys @() -PassThru
```

Pierwsze polecenie udziela uprawnień użytkownikowi w usłudze Azure Active Directory, PattiFuller@contoso.com Aby wykonywać operacje na kluczach i kluczach tajnych przy użyciu magazynu kluczy o nazwie Contoso03Vault.

Drugie polecenie modyfikuje uprawnienia udzielone PattiFuller@contoso.com w pierwszym poleceniu w celu umożliwienia natychmiastowego wprowadzenia kluczy tajnych oraz ich usunięcia.
Uprawnienia do kluczowych operacji pozostają niezmienione po wykonaniu tego polecenia.
Parametr *PassThru* powoduje, że zaktualizowany obiekt jest zwracany przez polecenie cmdlet.

Polecenie ostatnie modyfikuje istniejące uprawnienia w PattiFuller@contoso.com celu usunięcia wszystkich uprawnień do kluczowych operacji.
Po wykonaniu tego polecenia uprawnienia do tajnych operacji pozostają niezmienione.
Parametr *PassThru* powoduje, że zaktualizowany obiekt jest zwracany przez polecenie cmdlet.

### Przykład 2: udzielanie uprawnień głównemu usłudze aplikacji w celu odczytywania i zapisywania kluczy tajnych
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com' -PermissionsToSecrets Get,Set
```

To polecenie udziela uprawnień do aplikacji dla magazynu kluczy o nazwie Contoso03Vault.
Parametr *ServicePrincipalName* określa aplikację.
Aplikacja musi być zarejestrowana w usłudze Azure Active Directory.
Wartość parametru *ServicePrincipalName* musi być nazwą główną usługi aplikacji lub identyfikatorem GUID identyfikatora aplikacji.
W tym przykładzie określono nazwę główną usługi http://payroll.contoso.com , a polecenie przyznaje uprawnienia aplikacji do odczytu i zapisu kluczy tajnych.

### Przykład 3: udzielanie uprawnień do aplikacji przy użyciu jej identyfikatora obiektu
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectId 34595082-9346-41b6-8d6b-295a2808b8db -PermissionsToSecrets Get,Set
```

To polecenie udziela uprawnień aplikacji do odczytu i zapisu kluczy tajnych.
W tym przykładzie określono aplikację przy użyciu identyfikatora obiektu głównego usługi aplikacji.

### Przykład 4: udzielanie uprawnień dla głównej nazwy użytkownika
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets Get,List,Set
```

To polecenie udziela uprawnień Get, list i ustawia uprawnienia dla określonej nazwy głównej użytkownika w celu uzyskania dostępu do kluczy tajnych.

### Przykład 5: Włączanie kluczy tajnych do pobrania z magazynu kluczy przez firmę Microsoft. COMPUTE Resource providerkey
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

To polecenie udziela uprawnień do pobierania kluczy tajnych z magazynu kluczy Contoso03Vault przez dostawcę Microsoft. COMPUTE Resource.

### Przykład 6: udzielanie uprawnień grupie zabezpieczeń
```
PS C:\>Get-AzureRmADGroup
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'myownvault' -ObjectId (Get-AzureRmADGroup -SearchString 'group2')[0].Id -PermissionsToKeys All -PermissionsToSecrets All
DisplayName                    Type                           ObjectId
-----------                    ----                           --------
group1                                                        96a0daa6-9841-4a9c-bdeb-e7062276c688
group2                                                        b8a401eb-63ad-4a30-b0e1-a7461969fe54
group3                                                        da07a6be-2c1e-4e42-934d-ceb57cf652b4
```

W pierwszym poleceniu jest używane polecenie cmdlet Get-AzureRmADGroup, aby uzyskać dostęp do wszystkich grup usługi Active Directory.
Na podstawie wyników są wyświetlane 3 grupy zwrócone, nazwane **grupa1** , **group2** oraz **Group3**.
Wiele grup może mieć taką samą nazwę, ale zawsze mają unikatowy identyfikator ObjectId.
Gdy jest zwracana więcej niż jedna grupa o takiej samej nazwie, użyj identyfikatora ObjectId w wynikach, aby zidentyfikować odpowiedni element.

Następnie należy użyć tego polecenia z Set-AzureRmKeyVaultAccessPolicy, aby udzielić uprawnień group2 dla magazynu kluczy o nazwie **myownvault**.
W tym przykładzie są wyliczane grupy o nazwie "group2" w tym samym wierszu polecenia.
Na zwróconej liście może być wiele grup o nazwie "group2".
W tym przykładzie wybierany jest pierwszy z nich, wskazany indeksem \[ 0 \] na liście zwróconej.

### Przykład 7: udzielanie dostępu do usługi Azure Information Protection do klucza dzierżawy zarządzanego przez klienta (BYOK)
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso04Vault' -ServicePrincipalName 00000012-0000-0000-c000-000000000000 -PermissionsToKeys decrypt,encrypt,unwrapkey,wrapkey,verify,sign,get
```

To polecenie upoważnia ochronę informacji platformy Azure do korzystania z klucza zarządzanego przez klienta (w celu skorzystania z własnego klucza lub scenariusza "BYOK") jako klucza dzierżawy usługi Azure Information Protection.
Po uruchomieniu tego polecenia określ własną nazwę magazynu, ale musisz określić parametr *ServicePrincipalName* z identyfikatorem GUID **00000012-0000-0000-C000-000000000000** i określić wszystkie uprawnienia w przykładzie.

## PARAMETRÓW

### -Identyfikator aplikacji
Do użytku w przyszłości.

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: ByObjectId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -BypassObjectIdValidation
Umożliwia określenie identyfikatora obiektu bez sprawdzania, czy obiekt istnieje w usłudze Azure Active Directory.
Tego parametru należy używać tylko wtedy, gdy użytkownik chce udzielić dostępu do magazynu kluczy do identyfikatora obiektu, który odwołuje się do delegowanej grupy zabezpieczeń z innej dzierżawy platformy Azure.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByObjectId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EmailAddress
Określa adres e-mail użytkownika, któremu chcesz udzielić uprawnień.
Ten adres e-mail musi znajdować się w katalogu skojarzonym z bieżącą subskrypcją i być unikatowy.

```yaml
Type: System.String
Parameter Sets: ByEmailAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EnabledForDeployment
Umożliwia dostawcy zasobów Microsoft. COMPUTE na pobieranie kluczy tajnych z tego magazynu kluczy, gdy do tego magazynu kluczy odwołuje się tworzenie zasobów, na przykład podczas tworzenia maszyny wirtualnej.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EnabledForDiskEncryption
Umożliwia usłudze szyfrowania dysków Azure uzyskiwanie kluczy tajnych i ich odwinięcie z tego magazynu kluczy.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EnabledForTemplateDeployment
Umożliwia menedżerowi zasobów platformy Azure pobieranie kluczy tajnych z tego magazynu kluczy, gdy do tego magazynu kluczy odwołuje się wdrożenie szablonu.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ObjectId
Określa identyfikator obiektu podmiotu użytkownika lub usługi w usłudze Azure Active Directory, dla którego ma zostać udzielone uprawnienia.

```yaml
Type: System.String
Parameter Sets: ByObjectId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Zwraca obiekt reprezentujący element, z którym pracujesz.
Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.

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

### -PermissionsToCertificates
Określa tablicę uprawnień certyfikatów, które mają zostać udzielone użytkownikowi lub podmiotowi zabezpieczeń usługi.
Dopuszczalne wartości tego parametru to:

- Pobierz
- Lista
- Usuwać
- Tworzonych
- Przywoz
- Aktualizowane
- Managecontacts
- Emitenci
- Listissuers
- Autoemitenci
- Deleteissuers
- Manageissuers

```yaml
Type: System.String[]
Parameter Sets: ByServicePrincipalName, ByUserPrincipalName, ByObjectId, ByEmailAddress
Aliases: 
Accepted values: get, list, delete, create, import, update, managecontacts, getissuers, listissuers, setissuers, deleteissuers, manageissuers, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PermissionsToKeys
Określa tablicę uprawnień kluczowych operacji, które mają zostać udzielone użytkownikowi lub podmiotowi zabezpieczeń usługi.
Dopuszczalne wartości tego parametru to:

- Szyfruj
- Szyfrowane
- UnwrapKey
- WrapKey
- Sprawdzić
- Zapisywania
- Pobierz
- Lista
- Aktualizowane
- Tworzonych
- Przywoz
- Usuwać
- Wykonania
- Przywrócenie
- Odzyskiwanie
- Wyczyścić

```yaml
Type: System.String[]
Parameter Sets: ByServicePrincipalName, ByUserPrincipalName, ByObjectId, ByEmailAddress
Aliases: 
Accepted values: decrypt, encrypt, unwrapKey, wrapKey, verify, sign, get, list, update, create, import, delete, backup, restore, recover, purge, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PermissionsToSecrets
Określa tablicę uprawnień do tajnego działania, które mają zostać udzielone użytkownikowi lub podmiotowi zabezpieczeń usługi.
Dopuszczalne wartości tego parametru to:

- Pobierz
- Lista
- Ustawić
- Usuwać
- Wykonania
- Przywrócenie
- Odzyskiwanie
- Wyczyścić

```yaml
Type: System.String[]
Parameter Sets: ByServicePrincipalName, ByUserPrincipalName, ByObjectId, ByEmailAddress
Aliases: 
Accepted values: get, list, set, delete, backup, restore, recover, purge, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PermissionsToStorage
Określa uprawnienia konta magazynu zarządzanego i operacji definicji SAS, które mają zostać udzielone użytkownikowi lub podmiotowi zabezpieczeń usługi.

```yaml
Type: System.String[]
Parameter Sets: ByServicePrincipalName, ByUserPrincipalName, ByObjectId, ByEmailAddress
Aliases: 
Accepted values: get, list, delete, set, update, regeneratekey, getsas, listsas, deletesas, setsas, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServicePrincipalName
Określa główną nazwę usługi aplikacji, do której mają być udzielane uprawnienia.
Określ identyfikator aplikacji, określany także jako identyfikator klienta, zarejestrowany dla aplikacji w katalogu AzureActive.
Aplikacja o głównej nazwie usługi, którą ten parametr określa, musi być zarejestrowana w katalogu platformy Azure, który zawiera bieżący abonament.

```yaml
Type: System.String
Parameter Sets: ByServicePrincipalName
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UserPrincipalName
Określa główną nazwę użytkownika, któremu chcesz udzielić uprawnień.
Ta główna nazwa użytkownika musi istnieć w katalogu skojarzonym z bieżącą subskrypcją.

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Magazynname
Określa nazwę magazynu kluczy.
To polecenie cmdlet modyfikuje zasady dostępu dla magazynu kluczy określanego przez ten parametr.

```yaml
Type: System.String
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
Type: System.Management.Automation.SwitchParameter
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
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### String, GUID, String [], przełącznik

## WYSYŁA

### Microsoft. Azure. Commands. platforming. models. PSVault

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureRmKeyVault](./Get-AzureRmKeyVault.md)

[Remove-AzureRmKeyVaultAccessPolicy](./Remove-AzureRmKeyVaultAccessPolicy.md)

