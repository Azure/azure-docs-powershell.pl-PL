---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F94584BC-EC02-412D-B089-B98A6FF8F505
online version: ''
schema: 2.0.0
ms.openlocfilehash: a5b7758a7316fa6c34ffe6b5225cd252f39c5d7c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054875"
---
# New-AzureQuickVM

## STRESZCZENIe
Umożliwia skonfigurowanie i utworzenie maszyny wirtualnej platformy Azure.

## POLECENIA

### Windows (domyślnie)
```
New-AzureQuickVM [-Windows] -ServiceName <String> [-Name <String>] -ImageName <String> [-Password <String>]
 [-ReverseDnsFqdn <String>] [-Location <String>] [-AffinityGroup <String>] [-AdminUsername <String>]
 [-Certificates <CertificateSettingList>] [-WaitForBoot] [-DisableWinRMHttps] [-EnableWinRMHttp]
 [-WinRMCertificate <X509Certificate2>] [-X509Certificates <X509Certificate2[]>] [-NoExportPrivateKey]
 [-NoWinRMEndpoint] [-VNetName <String>] [-SubnetNames <String[]>] [-DnsSettings <DnsServer[]>]
 [-HostCaching <String>] [-AvailabilitySetName <String>] [-InstanceSize <String>] [-MediaLocation <String>]
 [-DisableGuestAgent] [-CustomDataFile <String>] [-ReservedIPName <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### Linux
```
New-AzureQuickVM [-Linux] -ServiceName <String> [-Name <String>] -ImageName <String> [-Password <String>]
 [-ReverseDnsFqdn <String>] [-Location <String>] [-AffinityGroup <String>] [-LinuxUser <String>] [-WaitForBoot]
 [-SSHPublicKeys <SSHPublicKeyList>] [-SSHKeyPairs <SSHKeyPairList>] [-VNetName <String>]
 [-SubnetNames <String[]>] [-DnsSettings <DnsServer[]>] [-HostCaching <String>] [-AvailabilitySetName <String>]
 [-InstanceSize <String>] [-MediaLocation <String>] [-DisableGuestAgent] [-CustomDataFile <String>]
 [-ReservedIPName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzureQuickVM** umożliwia skonfigurowanie i utworzenie maszyny wirtualnej platformy Azure.
To polecenie cmdlet umożliwia wdrożenie maszyny wirtualnej w istniejącej usłudze Azure.
To polecenie cmdlet może również utworzyć usługę Azure obsługującą nową maszynę wirtualną.

## Przykłady

### Przykład 1: Tworzenie maszyny wirtualnej
```
PS C:\> New-AzureQuickVM -Windows -ServiceName "ContosoService17" -Name "VirutalMachine01" -ImageName "Image07" -Password "password" -AdminUsername "AdminMain" -WaitForBoot
```

To polecenie tworzy maszynę wirtualną z uruchomionym systemem operacyjnym Windows w istniejącej usłudze.
Polecenie cmdlet jest podstawą maszyny wirtualnej na określonym obrazie.
Polecenie określa parametr *WaitForBoot* .
Dlatego polecenie cmdlet oczekuje na uruchomienie maszyny wirtualnej.

### Przykład 2: Tworzenie maszyny wirtualnej z użyciem certyfikatów
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
PS C:\> New-AzureQuickVM -Windows -ServiceName "MySvc1" -name "MyWinVM1" -ImageName "Image07" -Password "password" -AdminUserName "AdminMain" -WinRMCertificate $certs[0] -X509Certificates $certs[1], $certs[2] -WaitForBoot
```

Pierwsze polecenie pobiera certyfikaty ze sklepu i przechowuje je w zmiennej $certs.

Drugie polecenie tworzy maszynę wirtualną z uruchomionym systemem operacyjnym Windows w istniejącej usłudze z obrazu.
Na maszynie wirtualnej jest włączony domyślnie odbiornik https usługi WinRM.
Polecenie określa parametr *WaitForBoot* .
Dlatego polecenie cmdlet oczekuje na uruchomienie maszyny wirtualnej.
Polecenie przekazuje certyfikat usługi WinRM i certyfikat x509 usłudze hostowanej.

### Przykład 3: Tworzenie maszyny wirtualnej z uruchomionym systemem operacyjnym Linux
```
PS C:\> New-AzureQuickVM -Linux -ServiceName "ContosoServiceLinux01" -Name "LinuxVirtualMachine01" -ImageName "LinuxImage01" -LinuxUser "RootMain" -Password "password" -Location "Central US"
```

To polecenie tworzy maszynę wirtualną, która uruchamia system operacyjny Linux z obrazu.
To polecenie tworzy usługę do obsługi nowej maszyny wirtualnej.
Polecenie określa lokalizację usługi.

### Przykład 4: Tworzenie maszyny wirtualnej i tworzenie usługi do obsługi nowej maszyny wirtualnej
```
PS C:\> $Locations = Get-AzureLocation
PS C:\> $Images = Get-AzureVMImage
PS C:\> New-AzureQuickVM -Windows -InstanceSize "Large" -ServiceName "ContosoService03" -Name " VirtualMachine25" -ImageName $images[4].imagename -Password "password" -AdminUsername "AdminMain" -Location $Locations[0].name
```

Pierwsze polecenie uzyskuje lokalizacje za pomocą polecenia cmdlet **Get-AzureLocation** , a następnie zapisuje je w zmiennej tablicowej $Locations.

Drugie polecenie pobiera dostępne obrazy za pomocą polecenia cmdlet **Get-AzureVMImage** , a następnie zapisuje je w zmiennej tablicowej $images.

Polecenie ostatnie powoduje utworzenie dużej maszyny wirtualnej o nazwie VirtualMachine25.
Na maszynie wirtualnej jest uruchamiany system operacyjny Windows.
Jest ona oparta na jednym z obrazów w $Images.
Polecenie utworzy usługę o nazwie ContosoService03 dla nowej maszyny wirtualnej.
Usługa znajduje się w lokalizacji $Locations.

### Przykład 5: Tworzenie maszyny wirtualnej zawierającej zarezerwowaną nazwę IP
```
PS C:\> $Locations = Get-AzureLocation
PS C:\> $Images = Get-AzureVMImage
PS C:\> New-AzureQuickVM -Windows -InstanceSize "Large" -ServiceName "ContosoService04" -Name "VirtualMachine27" -ImageName $Images[4].imagename -Password "password" -AdminUsername "AdminMain" -Location $Locations[0].name -ReservedIPName $ipName
```

Pierwsze polecenie uzyskuje lokalizacje, a następnie zapisuje je w zmiennej tablicowej $Locations.

Drugie polecenie pobiera dostępne obrazy, a następnie zapisuje je w zmiennej tablicowej $Images.

Polecenie ostatnie powoduje utworzenie maszyny wirtualnej o nazwie VirtualMachine27 na podstawie jednego z obrazów w $Images.
Polecenie tworzy usługę w lokalizacji w $Locations.
Maszyna wirtualna ma zarezerwowaną nazwę IP, uprzednio przechowywaną w zmiennej $ipName.

## PARAMETRÓW

### -AdminUsername
Określa nazwę użytkownika konta administratora, które to polecenie cmdlet tworzy na maszynie wirtualnej.

```yaml
Type: String
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AffinityGroup
Określa grupę koligacji dla maszyny wirtualnej.
Ten parametr lub parametr *Lokalizacja* można określić tylko wtedy, gdy to polecenie cmdlet utworzy usługę Azure dla maszyny wirtualnej.

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

### -AvailabilitySetName
Określa nazwę zestawu dostępności, w którym to polecenie cmdlet tworzy maszynę wirtualną.

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

### -Certificates
Określa listę certyfikatów, których używa ten aplet polecenia w celu utworzenia usługi.

```yaml
Type: CertificateSettingList
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomDataFile
Określa plik danych dla maszyny wirtualnej.
To polecenie cmdlet koduje zawartość pliku jako Base64.
Plik musi być mniejszy niż 64 kilobajtów.

Jeśli system operacyjny gościa to system operacyjny Windows, to polecenie cmdlet zapisuje te dane jako plik binarny o nazwie%SYSTEMDRIVE%\AzureData\CustomData.bin.

Jeśli system operacyjny gościa to Linux, to polecenie cmdlet przekazuje dane przy użyciu pliku ovf-env.xml.
Program instalacyjny skopiuje ten plik do katalogu/var/lib/waagent.
Agent również przechowuje dane zakodowane w formacie base64 w/var/lib/waagent/CustomData.

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

### -DisableGuestAgent
Wskazuje, że to polecenie cmdlet wyłącza infrastrukturę jako usługę IaaS (Agent gościa).

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

### -DisableWinRMHttps
Wskazuje, że to polecenie cmdlet wyłącza zdalne zarządzanie systemem Windows (WinRM) na protokole HTTPS.
Domyślnie usługa WinRM jest włączona przy użyciu protokołu HTTPS.

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DnsSettings
Określa tablicę obiektów serwera DNS definiujących ustawienia DNS nowego wdrożenia.
Aby utworzyć obiekt **DnsServer** , użyj polecenia cmdlet **New-AzureDns** .

```yaml
Type: DnsServer[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableWinRMHttp
Wskazuje, że to polecenie cmdlet włącza usługę WinRM przez HTTP.

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostCaching
Określa tryb buforowania hosta dla dysku systemu operacyjnego.
Prawidłowe wartości: 

- Odczytu
- ReadWrite

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

### -ImageName
Określa nazwę obrazu dysku, którego używa polecenie cmdlet do tworzenia dysku z systemem operacyjnym.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationAction
Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.

Dopuszczalne wartości tego parametru to:

- Kontynuacj
- Ignorować
- Inquire
- SilentlyContinue
- Przestaw
- Wykonywanie

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Określa zmienną informacyjną.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstanceSize
Określa rozmiar wystąpienia.
Prawidłowe wartości: 

- ExtraSmall
- Mała
- Pożywkę
- Większej
- ExtraLarge
- A5
- A6
- A7
- A8
- A9
- Basic_A0
- Basic_A1
- Basic_A2
- Basic_A3
- Basic_A4
- Standard_D1
- Standard_D2
- Standard_D3
- Standard_D4
- Standard_D11
- Standard_D12
- Standard_D13
- Standard_D14

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

### -Linux
Wskazuje, że to polecenie cmdlet tworzy maszynę wirtualną opartą na systemie Linux.

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LinuxUser
Określa nazwę użytkownika konta administracyjnego Linux, które to polecenie cmdlet tworzy na maszynie wirtualnej.

```yaml
Type: String
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Lokalizacja
Określa platformę Azure Datacenter, na której znajduje się maszyna wirtualna.
W przypadku określenia tego parametru polecenie cmdlet tworzy usługę platformy Azure w określonej lokalizacji.
Ten parametr lub parametr *AffinityGroup* należy określić tylko wtedy, gdy to polecenie cmdlet utworzy usługę Azure dla maszyny wirtualnej.

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

### -MediaLocation
Określa lokalizację magazynu platformy Azure, w którym to polecenie cmdlet tworzy dyski maszyn wirtualnych.

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

### -Name (nazwa)
Określa nazwę maszyny wirtualnej, którą tworzy polecenie cmdlet.

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

### -NoExportPrivateKey
Wskazuje, że ta konfiguracja nie przekazuje klucza prywatnego.

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWinRMEndpoint
Wskazuje, że to polecenie cmdlet nie dodaje punktu końcowego WinRM do maszyny wirtualnej.

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Password (hasło)
Określa hasło dla konta administracyjnego.

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

### -ReservedIPName
Określa zastrzeżoną nazwę IP.

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

### -ReverseDnsFqdn
Określa w pełni kwalifikowaną nazwę domeny dla wyszukiwania wstecznego DNS.

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

### -ServiceName
Określa nazwę nowej lub istniejącej usługi platformy Azure, do której to polecenie cmdlet doda nową maszynę wirtualną.

Jeśli określisz nową usługę, to polecenie cmdlet tworzy je.
Aby utworzyć nową usługę, należy określić *lokalizację* lub parametr *AffinityGroup* .

Jeśli określisz istniejącą usługę, nie określaj *lokalizacji* ani *AffinityGroup*.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SSHKeyPairs
Określa pary kluczy SSH.

```yaml
Type: SSHKeyPairList
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SSHPublicKeys
Określa klucze publiczne SSH.

```yaml
Type: SSHPublicKeyList
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetNames
Określa tablicę nazw podsieci dla maszyny wirtualnej.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VNetName
Określa nazwę sieci wirtualnej dla maszyny wirtualnej.

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

### -WaitForBoot
Wskazuje, że to polecenie cmdlet oczekuje, że maszyna wirtualna będzie mieć dostęp do ReadyRole stanu.
Jeśli maszyna wirtualna osiągnie jedno z następujących stanów, polecenie cmdlet nie powiedzie się: FailedStartingVM, ProvisioningFailed lub ProvisioningTimeout.

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

### -Windows
Wskazuje, że w tym poleceniu cmdlet jest tworzona maszyna wirtualna systemu Windows.

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WinRMCertificate
Określa certyfikat, który jest skojarzony z tym poleceniem cmdlet do punktu końcowego usługi WinRM.

```yaml
Type: X509Certificate2
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -X509
Określa tablicę certyfikatów x509, które są wdrażane w usłudze hostowanej.

```yaml
Type: X509Certificate2[]
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureLocation](./Get-AzureLocation.md)

[Get-AzureVMImage](./Get-AzureVMImage.md)

[Nowe — AzureDns](./New-AzureDns.md)


