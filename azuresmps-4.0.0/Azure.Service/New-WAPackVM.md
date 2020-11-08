---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: AA7BD103-5C91-4E3B-9E46-2CAEDA5BA615
online version: ''
schema: 2.0.0
ms.openlocfilehash: d8f5643756cfad93399664298378e97264dedc2f
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/08/2020
ms.locfileid: "94061868"
---
# New-WAPackVM

## STRESZCZENIe
Umożliwia utworzenie maszyny wirtualnej.

## POLECENIA

### CreateVMFromTemplate (domyślny)
```
New-WAPackVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential> [-VNet <VMNetwork>]
 [-ProductKey <String>] [-Windows] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### CreateLinuxVMFromTemplate
```
New-WAPackVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential> [-VNet <VMNetwork>] [-Linux]
 [-AdministratorSSHKey <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### CreateVMFromOSDisk
```
New-WAPackVM -Name <String> [-VNet <VMNetwork>] -OSDisk <VirtualHardDisk> -VMSizeProfile <HardwareProfile>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Te tematy są przestarzałe i zostaną usunięte w przyszłości.
W tym temacie opisano polecenie cmdlet w wersji 0.8.1 modułu PowerShell platformy Microsoft Azure.
Aby sprawdzić używaną wersję modułu, należy wpisać ją w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .

Polecenie cmdlet **New-WAPackVM** umożliwia utworzenie maszyny wirtualnej.

## Przykłady

### Przykład 1: Tworzenie maszyny wirtualnej dla systemu operacyjnego Windows przy użyciu szablonu
```
PS C:\> $Credentials = Get-Credential PS C:\> $Template = Get-WAPackVMTemplate -Name "ContosoTemplate04"PS C:\> New-WAPackVM -Name "ContosoV023" -Template $Template -VMCredential $Credentials -Windows
```

Pierwsze polecenie tworzy obiekt **PSCredential** , a następnie zapisuje go w zmiennej $Credentials.
Polecenie cmdlet monituje o podanie konta i hasła.
Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Credential` .

Drugie polecenie pobiera szablon maszyny wirtualnej o nazwie ContosoTemplate04 przy użyciu polecenia cmdlet **Get-WAPackVMTemplate** , a następnie zapisuje go w zmiennej $Template.

Polecenie ostatnie powoduje utworzenie maszyny wirtualnej o nazwie ContosoV023 na podstawie szablonu przechowywanego w zmiennej $Template.
W tym poleceniu jest określany parametr *Windows* , a w związku z tym na maszynie wirtualnej musi być uruchomiona wersja systemu operacyjnego Windows.

### Przykład 2: Tworzenie maszyny wirtualnej dla systemu operacyjnego Linux przy użyciu szablonu
```
PS C:\> $Credentials = Get-Credential
PS C:\> $Template = Get-WAPackVMTemplate -Name "ContosoTemplate19"
PS C:\> New-WAPackVM -Linux -Name "ContosoV028" -Template $Template -VMCredential $Credentials
```

Pierwsze polecenie tworzy obiekt **PSCredential** , a następnie zapisuje go w zmiennej $Credentials.

Drugie polecenie pobiera szablon maszyny wirtualnej o nazwie ContosoTemplate19 przy użyciu polecenia cmdlet **Get-WAPackVMTemplate** , a następnie zapisuje go w zmiennej $Template.

Polecenie ostatnie powoduje utworzenie maszyny wirtualnej o nazwie ContosoV028 na podstawie szablonu przechowywanego w zmiennej $Template.
W tym poleceniu jest określany parametr *Linux* , a w związku z tym na maszynie wirtualnej musi być uruchomiona wersja systemu operacyjnego Linux.

### Przykład 3: Tworzenie maszyny wirtualnej na dysku z systemem operacyjnym i profilu rozmiaru
```
PS C:\> $OSDisk = Get-WAPackVMOSDisk -Name "ContosoDiskOS"
PS C:\> $SizeProfile = Get-WAPackVMSizeProfile -Name "MediumSizeVM"
PS C:\> New-WAPackVM -Name "ContosoV073" -OSDisk $OSDisk -VMSizeProfile $SizeProfile
```

Pierwsze polecenie uzyskuje dysk z systemem operacyjnym o nazwie ContosoDiskOS przy użyciu polecenia cmdlet **Get-WAPackVMOSDisk** , a następnie zapisuje go w zmiennej $OSDisk.

Drugie polecenie pobiera profil rozmiaru o nazwie MediumSizeVM przy użyciu polecenia cmdlet **Get-WAPackVMSizeProfile** , a następnie zapisuje go w zmiennej $SizeProfile.

Polecenie ostatnie powoduje utworzenie maszyny wirtualnej o nazwie ContosoV073 z dysku systemu operacyjnego zapisanego w $OSDisk i profilu rozmiaru przechowywanego w $SizeProfile.

## PARAMETRÓW

### -AdministratorSSHKey
Określa klucz Secure Shell (SSH) dla konta administratora.

```yaml
Type: String
Parameter Sets: CreateLinuxVMFromTemplate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Linux
Wskazuje, że polecenie cmdlet umożliwia utworzenie maszyny wirtualnej w celu uruchomienia systemu operacyjnego Linux.

```yaml
Type: SwitchParameter
Parameter Sets: CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -OSDisk
Określa dysk systemu operacyjnego jako obiekt **VirtualHardDisk** .
Aby uzyskać dysk z systemem operacyjnym, użyj polecenia cmdlet **Get-WAPackVMOSDisk** .

```yaml
Type: VirtualHardDisk
Parameter Sets: CreateVMFromOSDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ProductKey
Określa klucz produktu.
Klucz produktu to 25-cyfrowy numer identyfikujący licencję produktu.
Użyj klucza produktu dla systemu operacyjnego, który planujesz zainstalować na maszynie wirtualnej lub hoście.

```yaml
Type: String
Parameter Sets: CreateVMFromTemplate
Aliases:

Required: False
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
Aby uzyskać obiekt szablonu, użyj polecenia cmdlet Get-WAPackVMTemplate.

```yaml
Type: VMTemplate
Parameter Sets: CreateVMFromTemplate, CreateLinuxVMFromTemplate
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
Parameter Sets: CreateVMFromTemplate, CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMSizeProfile
Określa profil rozmiaru maszyny wirtualnej jako obiekt **HardwareProfile** .
Aby uzyskać profil rozmiaru, użyj polecenia cmdlet **Get-WAPackVMSizeProfile** .

```yaml
Type: HardwareProfile
Parameter Sets: CreateVMFromOSDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VNet
Określa sieć wirtualną.
Polecenie cmdlet umożliwia połączenie maszyny wirtualnej z określoną siecią wirtualną.
Aby uzyskać sieć wirtualną, użyj polecenia cmdlet **Get-WAPackVNet** .

```yaml
Type: VMNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Windows
Wskazuje, że polecenie cmdlet umożliwia utworzenie maszyny wirtualnej do uruchamiania systemu operacyjnego Windows.

```yaml
Type: SwitchParameter
Parameter Sets: CreateVMFromTemplate
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

[Get-WAPackVM](./Get-WAPackVM.md)

[Remove-WAPackVM](./Remove-WAPackVM.md)

[Restart-WAPackVM](./Restart-WAPackVM.md)

[Życiorys — WAPackVM](./Resume-WAPackVM.md)

[Set-WAPackVM](./Set-WAPackVM.md)

[Start — WAPackVM](./Start-WAPackVM.md)

[Zatrzymaj — WAPackVM](./Stop-WAPackVM.md)

[Suspend — WAPackVM](./Suspend-WAPackVM.md)

[Get-WAPackVMSizeProfile](./Get-WAPackVMSizeProfile.md)

[Get-WAPackVMTemplate](./Get-WAPackVMTemplate.md)

[Get-WAPackVMOSDisk](./Get-WAPackVMOSDisk.md)


