---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/add-azurermaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Connect-AzureRmAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Connect-AzureRmAccount.md
ms.openlocfilehash: a0f29e666a289faddbfce848b97cb0272ce67d0d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719071"
---
# Connect-AzureRmAccount

## STRESZCZENIe
Połącz się z usługą Azure za pomocą konta uwierzytelnionego do użycia z żądaniami polecenia cmdlet Menedżera zasobów platformy Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### UserWithSubscriptionId (domyślny)
```
Connect-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ServicePrincipalWithSubscriptionId
```
Connect-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal]
 -TenantId <String> [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ServicePrincipalCertificateWithSubscriptionId
```
Connect-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> [-Subscription <String>] [-ContextName <String>]
 [-SkipContextPopulation] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AccessTokenWithSubscriptionId
```
Connect-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String>
 [-GraphAccessToken <String>] [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>]
 [-ContextName <String>] [-SkipValidation] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ManagedServiceLogin
```
Connect-AzureRmAccount [-Environment <String>] [-TenantId <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-ManagedServiceSecret <SecureString>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet Connect-AzureRmAccount łączy się z usługą Azure za pomocą konta uwierzytelnionego do użycia z żądaniami polecenia cmdlet Menedżera zasobów platformy Azure.
Tego konta można używać tylko z poleceniami cmdlet Menedżera zasobów platformy Azure.
Aby dodać uwierzytelnione konto do użycia z poleceniami cmdlet zarządzania usługami, użyj Add-AzureAccount lub polecenia cmdlet Import-AzurePublishSettingsFile.
Jeśli nie odnaleziono kontekstu dla bieżącego użytkownika, to polecenie wypełni listę kontekstową użytkownika z kontekstem dla każdej z nich (pierwszych 25) subskrypcji. Listę kontekstów utworzonych dla użytkownika można znaleźć, uruchamiając "Get-AzureRmContext-ListAvailable". Aby pominąć tę populację kontekstu, możesz uruchomić to polecenie za pomocą parametru przełącznika "-SkipContextPopulation".
Po wykonaniu tego polecenia cmdlet możesz rozłączyć się z kontem na platformie Azure, korzystając z funkcji Disconnect-AzureRmAccount.

## Przykłady

### Przykład 1. Użyj interakcyjnego logowania, aby połączyć się z kontem platformy Azure
```powershell
PS C:\> Connect-AzureRmAccount

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

To polecenie nawiązuje połączenie z kontem na platformie Azure.
Aby uruchomić polecenia cmdlet Menedżera zasobów platformy Azure przy użyciu tego konta, w monicie należy podać poświadczenia konta Microsoft lub identyfikatora organizacji.
Jeśli dla poświadczeń włączono uwierzytelnianie wieloskładnikowe, należy zalogować się przy użyciu opcji interakcyjnej lub użyć uwierzytelniania głównego usługi.

### Przykład 2: Nawiązywanie połączenia z kontem na platformie Azure przy użyciu poświadczeń identyfikatora organizacji
```powershell
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzureRmAccount -Credential $Credential

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

Pierwsze polecenie wyświetli monit o podanie poświadczeń użytkownika (nazwa użytkownika i hasło), a następnie zapisze je w zmiennej $Credential.
Drugie polecenie nawiązuje połączenie z kontem na platformie Azure przy użyciu poświadczeń przechowywanych w $Credential.
To konto jest uwierzytelniane za pomocą Menedżera zasobów platformy Azure przy użyciu poświadczeń identyfikatora organizacji.
Za pomocą tego konta nie można używać uwierzytelniania wieloskładnikowego ani poświadczeń konta Microsoft w celu uruchamiania poleceń cmdlet Menedżera zasobów platformy Azure.

### Przykład 3: Nawiązywanie połączenia z kontem głównym usługi Azure
```powershell
PS C:\> $Credential = Get-Credential

PS C:\> Connect-AzureRmAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
xxxx-xxxx-xxxx-xxxx    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

Pierwsze polecenie uzyskuje główne poświadczenia usługi (Identyfikator aplikacji i główny klucz tajny usługi), a następnie zapisuje je w zmiennej $Credential.
Drugie polecenie nawiązuje połączenie z platformą Azure przy użyciu głównych poświadczeń usługi przechowywanych w $Credential dla określonego dzierżawy.
Parametr serviceprincipal Switch wskazuje, że konto jest uwierzytelniane jako podmiot zabezpieczeń usługi.

### Przykład 4: używanie interakcyjnego logowania do nawiązywania połączenia z kontem dla konkretnej dzierżawy i abonamentu
```powershell
PS C:\> Connect-AzureRmAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

To polecenie nawiązuje połączenie z kontem na platformie Azure i skonfigurowano program AzureRM PowerShell, aby domyślnie uruchamiać polecenia cmdlet dla określonego dzierżawy i abonamentu.

### Przykład 5: Dodawanie konta przy użyciu identyfikatora logowania tożsamości usługi zarządzanej
```powershell
PS C:\> Connect-AzureRmAccount -MSI

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
MSI@50342              Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

To polecenie nawiązuje połączenie przy użyciu tożsamości usługi zarządzanej dla środowiska hosta (na przykład w przypadku, gdy w VirtualMachine jest używana tożsamość usługi, która jest skojarzona z daną zarządzaną tożsamością).

### Przykład 6: Dodawanie konta przy użyciu certyfikatów
```powershell
# For more information on creating a self-signed certificate
# and giving it proper permissions, please see the following:
# https://docs.microsoft.com/en-us/azure/active-directory/develop/howto-authenticate-service-principal-powershell
PS C:\> $Thumbprint = "0SZTNJ34TCCMUJ5MJZGR8XQD3S0RVHJBA33Z8ZXV"
PS C:\> $TenantId = "4cd76576-b611-43d0-8f2b-adcb139531bf"
PS C:\> $ApplicationId = "3794a65a-e4e4-493d-ac1d-f04308d712dd"
PS C:\> Connect-AzureRmAccount -CertificateThumbprint $Thumbprint -ApplicationId $ApplicationId -Tenant $TenantId -ServicePrincipal

Account             SubscriptionName TenantId            Environment
-------             ---------------- --------            -----------
xxxx-xxxx-xxxx-xxxx Subscription1    xxxx-xxxx-xxxx-xxxx AzureCloud

Account          : 3794a65a-e4e4-493d-ac1d-f04308d712dd
SubscriptionName : MyTestSubscription
SubscriptionId   : 85f0f653-1f86-4d2c-a9f1-042efc00085c
TenantId         : 4cd76576-b611-43d0-8f2b-adcb139531bf
Environment      : AzureCloud
```

To polecenie nawiązuje połączenie z kontem na platformie Azure przy użyciu uwierzytelniania głównego usług opartego na certyfikatach. Theservice podmiot zabezpieczeń używany do uwierzytelniania powinien być utworzony przy użyciu danego certyfikatu.

## PARAMETRÓW

### -AccessToken
Określa token dostępu.

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AccountId
Identyfikator konta dla tokenu dostępu

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Identyfikator aplikacji
NAZWY

```yaml
Type: System.String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificateThumbprint
Skrót certyfikatu (odcisk palca)

```yaml
Type: System.String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ontextname
Nazwa kontekstu domyślnego w tej nazwie logowania.  Po zalogowaniu będzie można wybrać ten kontekst według tej nazwy.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Poświadczenie
Określa obiekt PSCredential.
Aby uzyskać więcej informacji na temat obiektu PSCredential, wpisz Get-Help Get-Credential.
Obiekt PSCredential zapewnia identyfikator użytkownika i hasło dla poświadczeń identyfikatora organizacji lub identyfikator aplikacji oraz klucz tajny dla poświadczeń głównych usługi.

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: UserWithSubscriptionId
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: ServicePrincipalWithSubscriptionId
Aliases:

Required: True
Position: 0
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

### -Środowisko
Środowisko zawierające konto do logowania

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EnvironmentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Zastąp istniejący kontekst o tej samej nazwie (jeśli istnieje).

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

### -GraphAccessToken
AccessToken dla usługi Graph

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Identity (tożsamość)
Logowanie przy użyciu tożsamości usługi zarządzanej w bieżącym środowisku.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedServiceLogin
Aliases: MSI, ManagedService

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyVaultAccessToken
AccessToken dla usługi magazynu

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagedServiceHostName
Nazwa hosta na potrzeby zarządzanego logowania usługi

```yaml
Type: System.String
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: localhost
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagedServicePort
Numer portu dla zarządzanego logowania usługi

```yaml
Type: System.Int32
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: 50342
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagedServiceSecret
Klucz tajny, który jest wykorzystywany w przypadku określonych rodzajów logowania zarządzanych usług.

```yaml
Type: System.Security.SecureString
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Zakres
Określa zakres zmian kontekstu, na przykład, czy zmiany są stosowane tylko do bieżącego procesu, czy do wszystkich sesji uruchomionych przez tego użytkownika.

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Serviceprincipal
Wskazuje, że to konto uwierzytelnia się, dostarczając poświadczenia podmiotu zabezpieczeń usługi.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipContextPopulation
Pomija populację kontekstu, jeśli nie zostaną znalezione żadne konteksty.

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

### -SkipValidation
Pomijanie sprawdzania poprawności tokenu dostępu

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Subscription
Nazwa lub Identyfikator subskrypcji

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName, SubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Dzierżawy
Opcjonalna nazwa domeny lub identyfikator dzierżawy. Nazwa domeny nie będzie działać we wszystkich sytuacjach logowania. W przypadku logowania dostawcy rozwiązań w chmurze (CSP) jest wymagany identyfikator dzierżawy.

```yaml
Type: System.String
Parameter Sets: UserWithSubscriptionId, AccessTokenWithSubscriptionId, ManagedServiceLogin
Aliases: Domain

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: Domain

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet. Polecenie cmdlet nie jest uruchamiane.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String
Parametry: subskrypcja (ByValue)

## WYSYŁA

### Microsoft. Azure. Commands. profile. PSAzureProfile

## INFORMACYJN

## LINKI POKREWNE
