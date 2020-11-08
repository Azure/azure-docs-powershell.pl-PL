---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 03EAFFB2-EA64-4227-A33B-D24EB4A75F71
online version: ''
schema: 2.0.0
ms.openlocfilehash: ac88bc2494bad975c6169262edd05c7b821061bb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055362"
---
# Add-AzureAccount

## STRESZCZENIe
Dodaje konto platformy Azure do programu Windows PowerShell.

## POLECENIA

### Użytkownik (domyślnie)
```
Add-AzureAccount [-Environment <String>] [-Credential <PSCredential>] [-Tenant <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Serviceprincipal
```
Add-AzureAccount [-Environment <String>] -Credential <PSCredential> [-ServicePrincipal] -Tenant <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Add-AzureAccount** umożliwia udostępnianie konta platformy Azure i jego subskrypcji w programie Windows PowerShell.
Przypomina to logowanie się do konta platformy Azure w programie Windows PowerShell.
Aby wylogować się z konta, użyj polecenia cmdlet **Remove-AzureAccount** .

**Dodatek Add-AzureAccount** pobiera informacje o koncie platformy Azure i zapisuje je w pliku danych subskrypcji w profilu użytkownika mobilnego.
Jest również dostępny token dostępu, który umożliwia programowi Windows PowerShell uzyskiwanie dostępu do konta platformy Azure w Twoim imieniu.
Po zakończeniu wykonywania polecenia możesz zarządzać kontem platformy Azure w programie Windows PowerShell.

Dostępne są dwie różne metody tworzenia konta platformy Azure w programie Windows PowerShell.
Możesz użyć polecenia cmdlet **Add-AzureAccount** , które używa tokenów dostępu do uwierzytelniania w usłudze Azure Active Directory (Azure AD) lub **importu-AzurePublishSettingsFile** , który używa certyfikatu zarządzania.
Aby uzyskać wskazówki dotyczące metody, której należy użyć, zobacz [jak: Nawiązywanie połączenia z subskrypcją](https://azure.microsoft.com/documentation/articles/install-configure-powershell) ( https://azure.microsoft.com/documentation/articles/install-configure-powershell/#Connect) .

Po uruchomieniu polecenia **Add-AzureAccount** zostanie wyświetlone interaktywne okno, w którym jest wyświetlany monit o zalogowanie się do konta platformy Azure.
To logowanie jest ważne do czasu wygaśnięcia tokenu dostępu.
Gdy wygaśnie, polecenia cmdlet wymagające dostępu do konta wymagają ponownego uruchomienia polecenia **Add-AzureAccount** .

W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.
Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .

## Przykłady

### Przykład 1: Dodawanie konta
```
PS C:\> Add-AzureAccount
```

To polecenie dodaje konto platformy Azure do programu Windows PowerShell.
Po uruchomieniu polecenia w systemie Windows zostanie wyświetlony monit o podanie nazwy użytkownika i hasła do konta.

### Przykład 2: używanie alternatywnego pliku danych subskrypcji
```
PS C:\> Add-AzureAccount -SubscriptionDataFile C:\Testing\SDF.xml
```

To polecenie używa parametru **SubscriptionDataFile** w celu kierowania polecenia **Add-AzureAccount** w celu przechowywania danych konta w pliku C:\Testing\SDF.xml, a nie w pliku domyślnym.

## PARAMETRÓW

### — Poświadczenie
```yaml
Type: PSCredential
Parameter Sets: User
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: PSCredential
Parameter Sets: ServicePrincipal
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Środowisko
Określa środowisko Azure.

Środowisko platformy Azure niezależne wdrożenie platformy Microsoft Azure, takiej jak AzureCloud dla usługi Azure i AzureChinaCloud dla platformy Azure obsługiwanej przez firmę 21Vianet w Chinach.
Lokalne środowiska platformy Azure można też tworzyć, korzystając z pakietu Azure i poleceń cmdlet WAPack.
Aby uzyskać więcej informacji, zobacz [pakiet Azure](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profile
Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet. Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Serviceprincipal
```yaml
Type: SwitchParameter
Parameter Sets: ServicePrincipal
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Dzierżawca
```yaml
Type: String
Parameter Sets: User
Aliases: TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ServicePrincipal
Aliases: TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono
Nie można popotokować danych wejściowych tego polecenia cmdlet

## WYSYŁA

### Znaleziono
To polecenie cmdlet nie zwraca żadnych danych wyjściowych.

## INFORMACYJN
* **Dodatek Add-AzureAccount** (i metoda uwierzytelniania usługi Azure AD) ma pierwszeństwo przed **importem-AzurePublishSettings** (i metodą certyfikatu zarządzania). Jeśli na koncie jest używane polecenie **Add-AzureAccount** , zostanie użyta metoda uwierzytelniania usługi Azure AD, a certyfikat zarządzania jest ignorowany. Aby usunąć token usługi Azure AD i przywrócić metodę certyfikatu zarządzania, użyj polecenia cmdlet **Remove-AzureAccount** . Aby uzyskać więcej informacji, wpisz ciąg: **Get-Help Remove-AzureAccount**.
* Błąd — Twoje poświadczenia wygasły. Użyj Add-AzureAccount, aby zalogować się ponownie. wskazuje, że token dostępu wygasł i program Windows PowerShell nie może uzyskać dostępu do konta platformy Azure. Aby przywrócić dostęp do konta, ponownie uruchom polecenie **Add-AzureAccount** .
* Polecenia cmdlet konta i subskrypcji usługi Azure PowerShell uzyskują dane z pliku danych subskrypcji, a nie z konta usługi Live Azure. Jeśli zmienisz swoje konto lub abonamenty poza programem Windows PowerShell, na przykład za pomocą portalu zarządzania Azure, ponownie uruchom **dodatek Add-AzureAccount** , aby odświeżyć plik danych subskrypcji.

## LINKI POKREWNE

[Dodaj-AzureEnvironment](./Add-AzureEnvironment.md)

[Get-AzureEnvironment](./Get-AzureEnvironment.md)

[Import — AzurePublishSettingsFile](./Import-AzurePublishSettingsFile.md)

[Get-AzureAccount](./Get-AzureAccount.md)

[Remove-AzureAccount](./Remove-AzureAccount.md)


