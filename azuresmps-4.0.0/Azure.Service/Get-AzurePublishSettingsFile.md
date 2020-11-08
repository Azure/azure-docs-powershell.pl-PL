---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: A5419F76-B85E-445D-84EA-CC695B175C8D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1364cf1bbec1fdca2a8c9901556d38de0b620358
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054599"
---
# Get-AzurePublishSettingsFile

## STRESZCZENIe
Pobiera plik ustawień publikowania dla subskrypcji platformy Azure.

## POLECENIA

```
Get-AzurePublishSettingsFile [-Environment <String>] [-Realm <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzurePublishSettingsFile** pobiera plik ustawień publikowania dla abonamentu na koncie.
Po ukończeniu polecenia możesz użyć polecenia cmdlet **Import-PublishSettingsFile** , aby ustawić ustawienia dostępne dla programu Windows PowerShell.

Aby konto platformy Azure było dostępne dla programu Windows PowerShell, możesz użyć pliku ustawień publikowania lub polecenia cmdlet **Add-AzureAccount** .
Publikowanie plików ustawień umożliwia przygotowywanie sesji z wyprzedzeniem, aby można było uruchamiać skrypty i zadania w tle bez opieki.
Jednak nie wszystkie usługi obsługują pliki ustawień publikowania.
Na przykład moduł **AzureResourceManager** nie obsługuje plików ustawień publikowania.

Po uruchomieniu polecenia **Get-AzurePublishSettingsFile** zostanie otwarta przeglądarka domyślna i zostanie wyświetlony monit o zalogowanie się do konta platformy Azure, wybranie subskrypcji i wybranie lokalizacji systemu plików dla pliku ustawień publikowania.
Następnie pobiera plik ustawień publikowania dla subskrypcji do wybranego pliku.

"Plik ustawień publikowania" to plik XML z rozszerzeniem nazwy pliku publishsettings.
Plik zawiera zakodowany certyfikat, który zawiera poświadczenia zarządzania dla subskrypcji platformy Azure.

**Uwaga dotycząca zabezpieczeń:** Pliki ustawień publikowania zawierają poświadczenia, które służą do administrowania subskrypcjami i usługami platformy Azure.
Jeśli Złośliwi użytkownicy uzyskują dostęp do pliku ustawień publikowania, mogą edytować, tworzyć i usuwać usługi platformy Azure.
Zgodnie z najważniejszymi wskazówkami dotyczącymi zabezpieczeń Zapisz plik w lokalizacji w folderze pobrane pliki lub dokumenty, a następnie usuń go po użyciu polecenia cmdlet **importu-AzurePublishSettingsFile** w celu zaimportowania ustawień.

W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.
Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .

## Przykłady

### Przykład 1: Pobieranie pliku ustawień publikowania
```
PS C:\> Get-AzurePublishSettingsFile
```

To polecenie otwiera przeglądarkę domyślną, nawiązuje połączenie z kontem Windows Azure, a następnie pobiera plik publishsettings dla swojego konta.

### Przykład 2: Określanie obszaru
```
PS C:\> Get-AzurePublishSettingsFile -Realm contoso.com -Passthru
```

To polecenie pobiera plik ustawień publikowania dla konta w domenie contoso.com.
Użyj polecenia z parametrem **Realm** , gdy logujesz się do platformy Azure przy użyciu konta organizacji, a nie konta Microsoft.

## PARAMETRÓW

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
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Zwraca wartość $True, jeśli wykonanie polecenia powiedzie się i $False, jeśli nie powiodło się.
Domyślnie to polecenie cmdlet nie zwraca żadnych danych wyjściowych.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Obszar
Określa organizację w IDENTYFIKATORze organizacji.
Na przykład jeśli logujesz się do platformy Azure jako admin@contoso.com , wartość parametru **Realm** to contoso.com.
Za pomocą tego parametru można zalogowanie się do witryny Azure Portal za pomocą identyfikatora organizacji.
Ten parametr nie jest wymagany w przypadku korzystania z konta Microsoft, takiego jak konto outlook.com lub live.com.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono
Możesz popotokować dane wejściowe tego polecenia cmdlet, korzystając z nazwy właściwości, ale nie według wartości.

## WYSYŁA

### Brak lub system. Boolean
Po użyciu parametru *PassThru* to polecenie cmdlet zwraca wartość logiczną.
W przeciwnym razie to polecenie cmdlet nie zwraca żadnych danych wyjściowych.

## INFORMACYJN

## LINKI POKREWNE

[Dodaj-AzureAccount](./Add-AzureAccount.md)

[Import — AzurePublishSettingsFile](./Import-AzurePublishSettingsFile.md)


