---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 79D64D7C-6671-4F03-8776-70A716F36512
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2bc0525ee7238de421842b74f52f7dd4fa59df1a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055227"
---
# Import-AzurePublishSettingsFile

## STRESZCZENIe
Importuje plik ustawień publikowania, który umożliwia zarządzanie kontami platformy Azure w programie Windows PowerShell.

## POLECENIA

```
Import-AzurePublishSettingsFile -PublishSettingsFile <String> [-Environment <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Import-AzurePublishSettingsFile** importuje plik ustawień publikowania (*. publishsettings), który zawiera informacje na temat kont platformy Azure i zapisuje plik danych abonamentu na komputerze.
Po zakończeniu działania polecenia cmdlet możesz zarządzać kontami platformy Azure w programie Windows PowerShell.

Przed uruchomieniem programu **Import-AzurePublishSettingsFile** Uruchom polecenie **Get-AzurePublishSettingsFile** , które umożliwia pobranie i zapisanie pliku ustawień publikowania w celu jego zaimportowania.

Aby konto platformy Azure było dostępne dla programu Windows PowerShell, możesz użyć pliku ustawień publikowania lub polecenia cmdlet **Add-AzureAccount** .
Publikowanie plików ustawień umożliwia przygotowywanie sesji z wyprzedzeniem, aby można było uruchamiać skrypty i zadania w tle bez opieki.
Jednak nie wszystkie usługi obsługują pliki ustawień publikowania.
Na przykład moduł **AzureResourceManager** nie obsługuje plików ustawień publikowania.

**Uwaga dotycząca zabezpieczeń:** Pliki ustawień publikowania zawierają certyfikat zarządzania, który jest kodowany, ale nie jest szyfrowany.
Jeśli Złośliwi użytkownicy uzyskują dostęp do pliku ustawień publikowania, mogą oni mieć możliwość edytowania, tworzenia i usuwania usług platformy Azure.
Zgodnie z najważniejszymi wskazówkami dotyczącymi zabezpieczeń Zapisz plik w lokalizacji w folderze pobrane pliki lub dokumenty, a następnie usuń go po użyciu polecenia cmdlet **importu-AzurePublishSettingsFile** w celu zaimportowania ustawień.

## Przykłady

### Przykład 1: Importowanie pliku
```
PS C:\> Import-AzurePublishSettingsFile -PublishSettingsFile C:\Temp\MyAccount.publishsettings
```

To polecenie umożliwia zaimportowanie pliku "C:\Temp\MyAccount.publishsettings".

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

### -PublishSettingsFile
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
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

### Znaleziono
To polecenie cmdlet nie generuje żadnych danych wyjściowych.

## INFORMACYJN
* "Plik ustawień publikowania" to plik XML z rozszerzeniem nazwy pliku publishsettings. Plik zawiera zakodowany certyfikat, który zawiera poświadczenia zarządzania dla subskrypcji platformy Azure. Po zaimportowaniu pliku usuń go, aby uniknąć zagrożenia bezpieczeństwa.
* "Plik danych abonamentu" to plik XML, który można bezpiecznie zapisać na komputerze. Domyślnie jest on zapisany w profilu użytkownika mobilnego ($home/AppData/Roaming).

## LINKI POKREWNE

[Jak zainstalować i skonfigurować środowisko Azure PowerShell](https://azure.microsoft.com/documentation/articles/install-configure-powershell/)

[Dodaj-AzureAccount](./Add-AzureAccount.md)

[Get-AzurePublishSettingsFile](./Get-AzurePublishSettingsFile.md)


