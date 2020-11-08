---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 53BD6ED4-EA66-448B-8B18-F078C0738AF5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 90f02a261dc804f46a7ef503879a8ce9f43fad35
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/08/2020
ms.locfileid: "94061870"
---
# New-WAPackQuickVM

## STRESZCZENIe
Umożliwia utworzenie maszyny wirtualnej na podstawie szablonu.

## POLECENIA

```
New-WAPackQuickVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Te tematy są przestarzałe i zostaną usunięte w przyszłości.
W tym temacie opisano polecenie cmdlet w wersji 0.8.1 modułu PowerShell platformy Microsoft Azure.
Aby sprawdzić używaną wersję modułu, należy wpisać ją w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .

Polecenie cmdlet **New-WAPackQuickVM** umożliwia utworzenie maszyny wirtualnej na podstawie szablonu.

## Przykłady

### Przykład 1. Tworzenie maszyny wirtualnej na podstawie szablonu
```
PS C:\> $Credentials = Get-Credential
PS C:\> $TemplateId = Get-WAPackVMTemplate -Id 66242D17-189F-480D-87CF-8E1D749998C8
PS C:\> New-WAPackQuickVM -Name "VirtualMachine023" -Template $TemplateId -VMCredential $Credentials
```

Pierwsze polecenie tworzy obiekt **PSCredential** , a następnie zapisuje go w zmiennej $Credentials.
Polecenie cmdlet monituje o podanie konta i hasła.
Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Credential` .

Drugie polecenie pobiera szablon za pomocą polecenia cmdlet **Get-WAPackVMTemplate** .
Polecenie określa identyfikator szablonu.
Polecenie zapisuje obiekt Template w zmiennej $TemplateID.

Polecenie ostatnie powoduje utworzenie maszyny wirtualnej o nazwie VirtualMachine023.
Polecenie opiera się na maszynie wirtualnej na szablonie przechowywanym w $TemplateId.

## PARAMETRÓW

### -Name (nazwa)
Określa nazwę maszyny wirtualnej.

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

### -Profile
Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.
Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.

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

### — Szablon
Określa szablon.
Polecenie cmdlet umożliwia utworzenie maszyny wirtualnej na podstawie określonego szablonu.
Aby uzyskać obiekt szablonu, użyj polecenia cmdlet **Get-WAPackVMTemplate** .

```yaml
Type: VMTemplate
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMCredential
Określa poświadczenie dla lokalnego konta administratora.
Aby uzyskać obiekt **PSCredential** , użyj polecenia cmdlet **Get-Credential** .
Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Credential` .

```yaml
Type: PSCredential
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

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Nowe — WAPackVM](./New-WAPackVM.md)

[Get-WAPackVMTemplate](./Get-WAPackVMTemplate.md)


