---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 0B3EF123-8424-4CCA-95E8-01301B70CBDC
online version: ''
schema: 2.0.0
ms.openlocfilehash: f84db81f51a4f8d0da605917f99e14c1721cd89d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055348"
---
# Add-AzureProvisioningConfig

## STRESZCZENIe
Dodaje konfigurację inicjowania obsługi maszyny wirtualnej platformy Azure.

## POLECENIA

### Windows (domyślnie)
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-CustomDataFile <String>] [-Windows]
 [-AdminUsername <String>] [-Password <String>] [-ResetPasswordOnFirstLogon] [-DisableAutomaticUpdates]
 [-NoRDPEndpoint] [-TimeZone <String>] [-Certificates <CertificateSettingList>] [-EnableWinRMHttp]
 [-DisableWinRMHttps] [-WinRMCertificate <X509Certificate2>] [-X509Certificates <X509Certificate2[]>]
 [-NoExportPrivateKey] [-NoWinRMEndpoint] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### Linux
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-Linux] [-LinuxUser <String>]
 [-DisableSSH] [-NoSSHEndpoint] [-NoSSHPassword] [-SSHPublicKeys <SSHPublicKeyList>]
 [-SSHKeyPairs <SSHKeyPairList>] [-CustomDataFile <String>] [-Password <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### WindowsDomain
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-CustomDataFile <String>]
 -AdminUsername <String> [-WindowsDomain] [-Password <String>] [-ResetPasswordOnFirstLogon]
 [-DisableAutomaticUpdates] [-NoRDPEndpoint] [-TimeZone <String>] [-Certificates <CertificateSettingList>]
 -JoinDomain <String> -Domain <String> -DomainUserName <String> -DomainPassword <String>
 [-MachineObjectOU <String>] [-EnableWinRMHttp] [-DisableWinRMHttps] [-WinRMCertificate <X509Certificate2>]
 [-X509Certificates <X509Certificate2[]>] [-NoExportPrivateKey] [-NoWinRMEndpoint] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Add-AzureProvisioningConfig** umożliwia dodanie informacji o konfiguracji inicjowania obsługi do konfiguracji maszyny wirtualnej platformy Azure.
Za pomocą obiektu konfiguracji można utworzyć maszynę wirtualną.

To polecenie cmdlet obsługuje różne konfiguracje obsługi, w tym autonomiczne serwery z systemem Windows, serwery systemu Windows połączone z domeną usługi Active Directory oraz serwery z systemem Linux.

Aby utworzyć serwer przyłączony domeny usługi Active Directory, określ w pełni kwalifikowaną nazwę domeny domeny usługi Active Directory oraz poświadczenia domeny użytkownika, który ma uprawnienia do dołączania do maszyny wirtualnej w domenie.

## Przykłady

### Przykład 1. Tworzenie autonomicznej maszyny wirtualnej
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" | New-AzureVM -ServiceName "ContosoService"
```

To polecenie tworzy obiekt konfiguracji maszyny wirtualnej przy użyciu polecenia cmdlet **New-AzureVMConfig** .
Polecenie przekazuje ten obiekt do bieżącego polecenia cmdlet za pomocą operatora potoku.
Bieżące polecenie cmdlet umożliwia dodanie konfiguracji inicjowania obsługi dla maszyny wirtualnej z uruchomionym systemem operacyjnym Windows.
Konfiguracja obejmuje nazwę użytkownika i hasło administratora.
Polecenie przekazanie konfiguracji do polecenia cmdlet **New-AzureVM** , które powoduje utworzenie maszyny wirtualnej.

### Przykład 2: Tworzenie maszyny wirtualnej przyłączonego do domeny
```
PS C:\> New-AzureVMConfig -Name "DomainVM" -InstanceSize Small -ImageName "Image09" | Add-AzureProvisioningConfig -WindowsDomain -Password "password" -AdminUsername "AdminMain" -ResetPasswordOnFirstLogon -JoinDomain "contoso.com" -Domain "contoso" -DomainUserName "DomainAdminUser" -DomainPassword "DomainPassword" -MachineObjectOU 'OU=AzureVMs,DC=contoso,DC=com' | New-AzureVM -ServiceName "ContosoService"
```

To polecenie tworzy obiekt konfiguracji maszyny wirtualnej, a następnie przekazuje go do bieżącego polecenia cmdlet.
Bieżące polecenie cmdlet umożliwia dodanie konfiguracji inicjowania obsługi maszyny wirtualnej w celu dołączenia jej do domeny contoso.
Polecenie zawiera nazwę użytkownika i hasło potrzebne do przyłączenia maszyny wirtualnej do domeny.
Konfiguracja wymaga, aby użytkownik zmienił hasło użytkownika przy pierwszym logowaniu.
Polecenie tworzy maszynę wirtualną na podstawie obiektu inicjowania obsługi.

### Przykład 3: Tworzenie maszyny wirtualnej opartej na systemie Linux
```
PS C:\> New-AzureVMConfig -Name "LinuxVM" -InstanceSize Small -ImageName "LinuxImage03" | Add-AzureProvisioningConfig -Linux -LinuxUser "LinuxRoot" -Password "password" | New-AzureVM -ServiceName "ContosoService"
```

To polecenie tworzy obiekt konfiguracji maszyny wirtualnej, a następnie przekazuje go do bieżącego polecenia cmdlet.
Bieżące polecenie cmdlet umożliwia dodanie konfiguracji inicjowania obsługi dla maszyny wirtualnej, na której jest uruchomiony system operacyjny Linux.
Konfiguracja obejmuje główną nazwę użytkownika i hasło.
Polecenie tworzy maszynę wirtualną na podstawie obiektu inicjowania obsługi.

### Przykład 4: Tworzenie maszyny wirtualnej zawierającej certyfikaty dla usługi WinRM
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image11" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -WinRMCertificate $certs[0] -X509Certificates $certs[1], $certs[2] | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

Pierwsze polecenie pobiera certyfikaty z magazynu certyfikatów, a następnie zapisuje je w zmiennej tablicowej $certs.

Drugie polecenie tworzy obiekt konfiguracji maszyny wirtualnej, a następnie przekazuje go do bieżącego polecenia cmdlet.
Bieżące polecenie cmdlet umożliwia dodanie konfiguracji inicjowania obsługi, zawierającej certyfikaty dla usługi WinRM.
Polecenie tworzy maszynę wirtualną na podstawie obiektu inicjowania obsługi.

### Przykład 5: Tworzenie maszyny wirtualnej z obsługą usługi WinRM za pośrednictwem protokołu HTTP
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image14" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -EnableWinRMHttp | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

To polecenie tworzy obiekt konfiguracji maszyny wirtualnej, a następnie przekazuje go do bieżącego polecenia cmdlet.
Bieżące polecenie cmdlet umożliwia dodanie konfiguracji inicjowania obsługi z obsługą usługi WinRM za pośrednictwem protokołu HTTP.
Polecenie tworzy maszynę wirtualną na podstawie obiektu inicjowania obsługi.

### Przykład 6: Tworzenie maszyny wirtualnej z wyłączonym WinRM w usłudze HTTPS
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -DisableWinRMHttps | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

To polecenie tworzy obiekt konfiguracji maszyny wirtualnej, a następnie przekazuje go do bieżącego polecenia cmdlet.
Bieżące polecenie cmdlet umożliwia dodanie konfiguracji inicjowania obsługi, która wyłącza usługę WinRM przez HTTPS.
Polecenie tworzy maszynę wirtualną na podstawie obiektu inicjowania obsługi.

### Przykład 7: Tworzenie maszyny wirtualnej bez eksportowania kluczy
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -X509Certificates $certs[0], $certs[1] -NoExportPrivateKey | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

Pierwsze polecenie pobiera certyfikaty z magazynu certyfikatów, a następnie zapisuje je w zmiennej tablicowej $certs.

Drugie polecenie tworzy obiekt konfiguracji maszyny wirtualnej, a następnie przekazuje go do bieżącego polecenia cmdlet.
Bieżące polecenie cmdlet umożliwia dodanie konfiguracji inicjowania obsługi dla maszyny wirtualnej zawierającej certyfikaty i nie powoduje wyeksportowania kluczy prywatnych.
Polecenie tworzy maszynę wirtualną na podstawie obiektu inicjowania obsługi.

## PARAMETRÓW

### -AdminUsername
Określa nazwę użytkownika konta administratora, którą tworzy ta konfiguracja na maszynie wirtualnej.

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

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Certificates
Określa zestaw certyfikatów, które są instalowane w ramach tej konfiguracji na maszynie wirtualnej.

```yaml
Type: CertificateSettingList
Parameter Sets: Windows, WindowsDomain
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

Jeśli system operacyjny gościa to system operacyjny Windows, ta konfiguracja zapisuje te dane jako plik binarny o nazwie%SYSTEMDRIVE%\AzureData\CustomData.bin.

Jeśli system operacyjny gościa to Linux, ta konfiguracja przekazuje dane przy użyciu pliku ovf-env.xml.
Konfiguracja kopiuje ten plik do katalogu/var/lib/waagent.
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

### -DisableAutomaticUpdates
Wskazuje, że ta konfiguracja wyłącza aktualizacje automatyczne.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableGuestAgent
Wskazuje, że ta konfiguracja wyłącza infrastrukturę jako agenta gościa usługi (IaaS).

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

### -DisableSSH
Wskazuje, że ta konfiguracja wyłącza SSH.

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWinRMHttps
Wskazuje, że ta konfiguracja wyłącza usługę Windows Remote Management (WinRM) w protokole HTTPS.
Domyślnie usługa WinRM jest włączona przy użyciu protokołu HTTPS.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Domain
Określa nazwę domeny konta, która ma uprawnienia do dodawania komputera do domeny.

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainPassword
Określa hasło konta użytkownika, które ma uprawnienia do dodawania komputera do domeny.

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainUserName
Określa nazwę konta użytkownika, które ma uprawnienia do dodawania komputera do domeny.

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableWinRMHttp
Wskazuje, że ta konfiguracja włącza usługę WinRM przez HTTP.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
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

### -JoinDomain
Określa w pełni kwalifikowaną nazwę domeny (FQDN) domeny, do której należy dołączyć.

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Linux
Wskazuje, że w tej konfiguracji jest tworzona konfiguracja systemu Linux.

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
Określa nazwę użytkownika konta administracyjnego systemu Linux, którą ta konfiguracja tworzy na maszynie wirtualnej.

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

### -MachineObjectOU
Określa w pełni kwalifikowaną nazwę jednostki organizacyjnej, w której konfiguracja tworzy konto komputera.

```yaml
Type: String
Parameter Sets: WindowsDomain
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
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoRDPEndpoint
Wskazuje, że ta konfiguracja służy do tworzenia maszyny wirtualnej bez punktu końcowego pulpitu zdalnego.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoSSHEndpoint
Wskazuje, że ta konfiguracja służy do tworzenia maszyny wirtualnej bez punktu końcowego SSH.

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoSSHPassword
Wskazuje, że ta konfiguracja umożliwia utworzenie maszyny wirtualnej bez hasła SSH.

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWinRMEndpoint
Wskazuje, że ta konfiguracja nie powoduje dodania punktu końcowego usługi WinRM do maszyny wirtualnej.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Password (hasło)
Określa hasło konta administratora.

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

### -ResetPasswordOnFirstLogon
Wskazuje, że maszyna wirtualna wymaga od użytkownika zmiany hasła przy pierwszym logowaniu.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
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

### -TimeZone
Określa strefę czasową dla maszyny wirtualnej, na przykład Pacyficzny czas standardowy lub Kanada (środkowy czas standardowy).

```yaml
Type: String
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
Określa obiekt maszyny wirtualnej.

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Windows
Wskazuje, że w tej konfiguracji jest tworzona autonomiczna maszyna wirtualna z uruchomionym systemem operacyjnym Windows.

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

### -WindowsDomain
Wskazuje, że w tej konfiguracji jest tworzony system Windows Server dołączony do domeny usługi Active Directory.

```yaml
Type: SwitchParameter
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WinRMCertificate
Określa certyfikat, który jest skojarzony z tą konfiguracją do punktu końcowego usługi WinRM.

```yaml
Type: X509Certificate2
Parameter Sets: Windows, WindowsDomain
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
Parameter Sets: Windows, WindowsDomain
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

[Nowe — AzureVM](./New-AzureVM.md)

[Nowe — AzureVMConfig](./New-AzureVMConfig.md)


