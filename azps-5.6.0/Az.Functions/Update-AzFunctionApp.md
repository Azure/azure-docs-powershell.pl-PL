---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/update-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionApp.md
ms.openlocfilehash: 7ea6f485026faa183f66d5bb2e70eb57c4a9fb97
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006746"
---
# Update-AzFunctionApp

## SYNOPSIS
Aktualizuje aplikację funkcji.

## SKŁADNIA

### ByName (Default)
```
Update-AzFunctionApp -Name <String> -ResourceGroupName <String> [-ApplicationInsightsKey <String>]
 [-ApplicationInsightsName <String>] [-IdentityID <String>] [-IdentityType <ManagedServiceIdentityType>]
 [-PlanName <String>] [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### ByObjectInput
```
Update-AzFunctionApp -InputObject <ISite> [-ApplicationInsightsKey <String>]
 [-ApplicationInsightsName <String>] [-IdentityID <String>] [-IdentityType <ManagedServiceIdentityType>]
 [-PlanName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## OPIS
Aktualizuje aplikację funkcji.

## PRZYKŁADY

### Przykład 1. Zaktualizuj plan hostingu aplikacji funkcji.
```powershell
PS C:\> Update-AzFunctionApp -Name MyUniqueFunctionAppName -ResourceGroupName MyResourceGroupName -PlanName NewPlanName 
```

To polecenie aktualizuje plan hostingu aplikacji funkcji.

### Przykład 2. Ustawianie tożsamości zarządzanej systemuAssigned dla aplikacji funkcyjnej.
```powershell
PS C:\> Update-AzFunctionApp -Name MyUniqueFunctionAppName -ResourceGroupName MyResourceGroupName -IdentityType SystemAssigned 
```

To polecenie ustawia tożsamość zarządzaną przypisaną przez SystemAssigned dla aplikacji funkcyjnej.

### Przykład 3. Aktualizowanie szczegółowych informacji aplikacji funkcji.
```powershell
PS C:\> Update-AzFunctionApp -Name MyUniqueFunctionAppName -ResourceGroupName MyResourceGroupName -ApplicationInsightsName ApplicationInsightsProjectName 
```

To polecenie aktualizuje aplikację aplikacji Application Insights.

### Przykład 3. Usuwanie tożsamości zarządzanej z aplikacji funkcji.
```powershell
PS C:\> Update-AzFunctionApp -Name MyUniqueFunctionAppName -ResourceGroupName MyResourceGroupName -IdentityType None 
```

To polecenie usuwa tożsamość zarządzaną z aplikacji funkcyjnej.

## PARAMETERS

### -ApplicationInsightsKey
Klucz instrumentacji aplikacji do dodania.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppInsightsKey

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationInsightsName
Nazwa istniejącego projektu szczegółowych informacji o aplikacji, który ma zostać dodany do aplikacji funkcyjnej.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppInsightsName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — AsJob
Uruchamia polecenie cmdlet jako zadanie w tle.

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

### -DefaultProfile


```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### - IdentityID
Określa listę tożsamości użytkowników skojarzonych z aplikacją funkcji.
Odwołania do tożsamości użytkownika ARM identyfikatory zasobów w postaci: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}"

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

### -IdentityType
Określa typ tożsamości używany w aplikacji funkcji.
Wpisanie typu "Brak" spowoduje usunięcie wszystkich tożsamości z aplikacji funkcji.
Dopuszczalne wartości dla tego parametru to: - SystemAssigned - UserAssigned - None

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Support.ManagedServiceIdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Aby skonstruować, zobacz sekcję NOTES, aby uzyskać informacje o właściwościach INPUTOBJECT i utworzyć tabelę skrótu.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite
Parameter Sets: ByObjectInput
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### — Nazwa
Nazwa aplikacji funkcji.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWait
Rozpoczyna operację i zwraca bezpośrednio przed jej ukończeniem.
Aby ustalić, czy operacja została pomyślnie ukończona, użyj innego mechanizmu.

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

### -PlanName
Nazwa planu usługi.

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

### -ResourceGroupName
Nazwa grupy zasobów.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### - SubscriptionId
Identyfikator subskrypcji platformy Azure.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### — Tag
Tagi zasobów.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Potwierdź
Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.

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
Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.
Polecenie cmdlet nie zostanie uruchomione.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Microsoft.Azure.PowerShell.cmdlet.functions.models.api20190801.iSite

## DANE WYJŚCIOWE

### Microsoft.Azure.PowerShell.cmdlet.functions.models.api20190801.iSite

## NOTATKI

ALIASY

ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW

Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości. Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.


INPUTOBJECT: <ISite> 
  - `Location <String>`: Lokalizacja zasobu.
  - `CloningInfoSourceWebAppId <String>`: ARM identyfikator zasobu aplikacji źródłowej. Identyfikator zasobu aplikacji to formularz /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} for production slots and /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} for other slots.
  - `[Kind <String>]`: Rodzaj zasobu.
  - `[Tag <IResourceTags>]`: tagi zasobów.
    - `[(Any) <String>]`: Wskazuje to, że do tego obiektu można dodać dowolną właściwość.
  - `[ClientAffinityEnabled <Boolean?>]`: <code>true</code> aby włączyć ffinity klienta; aby zatrzymać wysyłanie plików cookie chętnych do sesji, które wysyłają żądania klienta w tej samej sesji <code>false</code> do tego samego wystąpienia. Wartość domyślna <code>true</code> to.
  - `[ClientCertEnabled <Boolean?>]`: <code>true</code> aby włączyć uwierzytelnianie klienta (TLS, mutual authentication), w przeciwnym <code>false</code> razie. Wartość domyślna <code>false</code> to.
  - `[ClientCertExclusionPath <String>]`: ścieżki wykluczeń oddzielone przecinkami uwierzytelniania klienta
  - `[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: ustawienie aplikacji zastępuje sklonowane aplikacje. Jeśli jest to określone, te ustawienia zastępują ustawienia sklonowane z aplikacji źródłowej. W przeciwnym razie ustawienia aplikacji z aplikacji źródłowej zostaną zachowane.
    - `[(Any) <String>]`: Wskazuje to, że do tego obiektu można dodać dowolną właściwość.
  - `[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> aby sklonować niestandardowe nazwy hosta z aplikacji źródłowej; w przeciwnym <code>false</code> razie.
  - `[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> aby sklonować kontrolkę źródłową z aplikacji źródłowej; w przeciwnym <code>false</code> razie.
  - `[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> aby skonfigurować równoważenie obciążenia dla aplikacji źródłowej i docelowej.
  - `[CloningInfoCorrelationId <String>]`: Identyfikator korelacji operacji klonowania. Ten identyfikator łączy wiele operacji klonowania w celu użycia tej samej migawki.
  - `[CloningInfoHostingEnvironment <String>]`: Środowisko usługi aplikacji.
  - `[CloningInfoOverwrite <Boolean?>]`: <code>true</code> aby zastąpić aplikację docelową; w przeciwnym <code>false</code> razie.
  - `[CloningInfoSourceWebAppLocation <String>]`: Lokalizacja aplikacji źródłowej, np.: Stany Zjednoczone Zachód lub Europa Północna
  - `[CloningInfoTrafficManagerProfileId <String>]`: ARM identyfikator zasobu profilu Menedżera ruchu, jeśli istnieje. Identyfikator zasobu Menedżera ruchu to formularz /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.
  - `[CloningInfoTrafficManagerProfileName <String>]`: nazwa profilu Menedżera ruchu do utworzenia. Jest to potrzebne tylko wtedy, gdy nie istnieje jeszcze profil menedżera ruchu.
  - `[Config <ISiteConfig>]`: konfiguracja aplikacji.
    - `IsPushEnabled <Boolean>`: Pobiera lub ustawia flagę wskazującą, czy punkt końcowy push jest włączony.
    - `[ActionMinProcessExecutionTime <String>]`: minimalny czas wykonywania procesu przed podjęciem działania
    - `[ActionType <AutoHealActionType?>]`: Wstępnie zdefiniowana akcja do wykonanego działania.
    - `[AlwaysOn <Boolean?>]`: <code>true</code> jeśli opcja Zawsze jest włączona; w przeciwnym <code>false</code> razie.
    - `[ApiDefinitionUrl <String>]`: adres URL definicji interfejsu API.
    - `[ApiManagementConfigId <String>]`: APIM-Api identyfikator.
    - `[AppCommandLine <String>]`: wiersz polecenia aplikacji do uruchomienia.
    - `[AppSetting <INameValuePair[]>]`: Ustawienia aplikacji.
      - `[Name <String>]`: nazwa parowania.
      - `[Value <String>]`: Paruj wartość.
    - `[AutoHealEnabled <Boolean?>]`: <code>true</code> jeśli jest włączona funkcja Autosytowania, a w przeciwnym razie <code>false</code> .
    - `[AutoSwapSlotName <String>]`: nazwa gniazda automatycznego zamiany.
    - `[ConnectionString <IConnStringInfo[]>]`: Parametry połączenia.
      - `[ConnectionString <String>]`: wartość parametrów połączenia.
      - `[Name <String>]`: nazwa parametrów połączenia.
      - `[Type <ConnectionStringType?>]`: typ bazy danych.
    - `[CorAllowedOrigin <String[]>]`: pobiera lub ustawia listę pochodzenia, z których powinno być dozwolone dzwonienie między pochodzeniem (na http://example.com:12345) przykład: Aby zezwolić wszystkim, użyj "*".
    - `[CorSupportCredentials <Boolean?>]`: Pobiera lub określa, czy żądania CORS z poświadczeniami są dozwolone. Aby         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         uzyskać więcej informacji, zobacz te informacje.
    - `[CustomActionExe <String>]`: Plik wykonywalny do uruchomienia.
    - `[CustomActionParameter <String>]`: parametry pliku wykonywalnego.
    - `[DefaultDocument <String[]>]`: dokumenty domyślne.
    - `[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> jeśli funkcja szczegółowego rejestrowania błędów jest włączona; w przeciwnym <code>false</code> razie.
    - `[DocumentRoot <String>]`: katalog główny dokumentu.
    - `[DynamicTagsJson <String>]`: Pobiera lub ustawia ciąg JSON zawierający listę tagów dynamicznych, które będą obliczane na stronie claims użytkowników w punkcie końcowym wypychania rejestracji.
    - `[ExperimentRampUpRule <IRampUpRule[]>]`: lista reguł dotyczących rampy.
      - `[ActionHostName <String>]`: nazwa hosta miejsca, do którego ruch zostanie przekierowany w razie decyzji. Np. myapp-stage.azurewebsites.net.
      - `[ChangeDecisionCallbackUrl <String>]`: Niestandardowy algorytm decyzyjny może być podany w rozszerzeniu witryny TiPCallback, którego adres URL można określić. Zobacz rozszerzenie witryny TiPCallback dla szkieletów i kontraktów.         https://www.siteextensions.net/packages/TiPCallback/
      - `[ChangeIntervalInMinute <Int32?>]`: Określa interwał w minutach, aby ponownie określić wartość ReroutePercentage.
      - `[ChangeStep <Double?>]`: W scenariuszu automatycznego rozsuwu jest to krok, z którym należy dodać/usunąć, aż osiągnie <code>ReroutePercentage</code> \n <code>MinReroutePercentage</code> lub         <code>MaxReroutePercentage</code> . Metryki witryny są sprawdzane co N minut określonych w pliku .\nCustom decision algorithm can be provided in TiPCallback site extension (Rozszerzenie <code>ChangeIntervalInMinutes</code> witryny TiPCallback), którego adres URL można określić <code>ChangeDecisionCallbackUrl</code> w .
      - `[MaxReroutePercentage <Double?>]`: Określa górną granicę, poniżej której pozostanie wartość ReroutePercentage.
      - `[MinReroutePercentage <Double?>]`: Określa dolną granicę, powyżej której pozostanie wartość ReroutePercentage.
      - `[Name <String>]`: nazwa reguły routingu. Zalecaną nazwą będzie wskaż miejsce, w którym zostanie wyświetlony ruch w eksperymencie.
      - `[ReroutePercentage <Double?>]`: procent ruchu, do którego zostanie przekierowany <code>ActionHostName</code> ruch.
    - `[FtpsState <FtpsState?>]`: stan usługi FTP/FTPS
    - `[HandlerMapping <IHandlerMapping[]>]`: mapowania programów obsługi.
      - `[Argument <String>]`: argumenty wiersza polecenia przekazywane do edytora skryptów.
      - `[Extension <String>]`: Żądania z tym rozszerzeniem będą obsługiwane przy użyciu określonej aplikacji FastCGI.
      - `[ScriptProcessor <String>]`: ścieżka bezwzględna do aplikacji FastCGI.
    - `[HealthCheckPath <String>]`: ścieżka kontroli kondycji
    - `[Http20Enabled <Boolean?>]`: Http20Enabled: konfiguruje witrynę sieci Web w celu zezwalania klientom na łączenie się przez http2.0
    - `[HttpLoggingEnabled <Boolean?>]`: <code>true</code> jeśli rejestrowanie HTTP jest włączone; w przeciwnym <code>false</code> razie.
    - `[IPSecurityRestriction <IIPSecurityRestriction[]>]`: ograniczenia zabezpieczeń adresów IP dla głównych adresów IP.
      - `[Action <String>]`: Zezwalaj lub odmów dostępu dla tego zakresu adresów IP.
      - `[Description <String>]`: opis reguły ograniczeń adresów IP.
      - `[IPAddress <String>]`: adres IP, dla których obowiązuje ograniczenie zabezpieczeń.         Może mieć postać wyłącznie adresu ipv4 (wymagana właściwość SubnetMask) lub notacji CIDR, takiej jak ipv4/mask (wiodące dopasowanie bitów). W przypadku cidru CIDR nie można określić właściwości SubnetMask.
      - `[Name <String>]`: nazwa reguły ograniczeń adresów IP.
      - `[Priority <Int32?>]`: Priorytet reguły ograniczeń adresów IP.
      - `[SubnetMask <String>]`: Maska podsieci dla zakresu adresów IP, dla których jest obowiązujące ograniczenie.
      - `[SubnetTrafficTag <Int32?>]`: (wewnętrzny) Tag ruchu podsieci
      - `[Tag <IPFilterTag?>]`: określa, do czego będzie używany ten filtr IP. Ma to na celu obsługę filtrowania adresów IP w serwerach proxy.
      - `[VnetSubnetResourceId <String>]`: Identyfikator zasobu sieci wirtualnej
      - `[VnetTrafficTag <Int32?>]`: (wewnętrzny) tag ruchu w sieci Vnet
    - `[JavaContainer <String>]`: kontener języka Java.
    - `[JavaContainerVersion <String>]`: wersja kontenera języka Java.
    - `[JavaVersion <String>]`: wersja Java.
    - `[LimitMaxDiskSizeInMb <Int64?>]`: Maksymalny dozwolony rozmiar dysku w MB.
    - `[LimitMaxMemoryInMb <Int64?>]`: Maksymalna dozwolona ilość pamięci w MB.
    - `[LimitMaxPercentageCpu <Double?>]`: Maksymalna dozwolona wartość procentowa użycia procesora.
    - `[LinuxFxVersion <String>]`: Linux App Framework i wersja
    - `[LoadBalancing <SiteLoadBalancing?>]`: Równoważenie obciążenia witryny.
    - `[LocalMySqlEnabled <Boolean?>]`: <code>true</code> w celu włączenia lokalnego mysql; w przeciwnym <code>false</code> razie.
    - `[LogsDirectorySizeLimit <Int32?>]`: Limit rozmiaru katalogów dzienników HTTP.
    - `[MachineKeyDecryption <String>]`: Algorytm używany do odszyfrowywania.
    - `[MachineKeyDecryptionKey <String>]`: Klucz odszyfrowywania.
    - `[MachineKeyValidation <String>]`: Sprawdzanie poprawności klucza maszynowego.
    - `[MachineKeyValidationKey <String>]`: klucz sprawdzania poprawności.
    - `[ManagedPipelineMode <ManagedPipelineMode?>]`: tryb zarządzanych potoków.
    - `[ManagedServiceIdentityId <Int32?>]`: Identyfikator tożsamości usługi zarządzanej
    - `[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: konfiguruje minimalną wersję protokołu TLS wymaganą dla żądań SSL.
    - `[NetFrameworkVersion <String>]`: .NET Framework wersji.
    - `[NodeVersion <String>]`: wersja Node.js.
    - `[NumberOfWorker <Int32?>]`: Liczba pracowników.
    - `[PhpVersion <String>]`: Wersja PHP.
    - `[PowerShellVersion <String>]`: wersja programu PowerShell.
    - `[PreWarmedInstanceCount <Int32?>]`: liczba prewarmed instances.         To ustawienie dotyczy tylko planów zużycia i elastyczności
    - `[PublishingUsername <String>]`: nazwa użytkownika publikowania.
    - `[PushKind <String>]`: Rodzaj zasobu.
    - `[PythonVersion <String>]`: Wersja języka Python.
    - `[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> jeśli debugowanie zdalne jest włączone; w przeciwnym <code>false</code> razie.
    - `[RemoteDebuggingVersion <String>]`: Wersja debugowania zdalnego.
    - `[RequestCount <Int32?>]`: Liczba żądań.
    - `[RequestTimeInterval <String>]`: interwał czasu.
    - `[RequestTracingEnabled <Boolean?>]`: <code>true</code> jeśli śledzenie żądania jest włączone; w przeciwnym <code>false</code> razie.
    - `[RequestTracingExpirationTime <DateTime?>]`: Zażądaj czasu wygaśnięcia śledzenia.
    - `[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: ograniczenia zabezpieczeń adresów IP dla usługi scm.
    - `[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: ograniczenia zabezpieczeń adresów IP dla usługi scm do używania głównych.
    - `[ScmType <ScmType?>]`: typ SCM.
    - `[SlowRequestCount <Int32?>]`: Liczba żądań.
    - `[SlowRequestTimeInterval <String>]`: interwał czasu.
    - `[SlowRequestTimeTaken <String>]`: Czas trwania.
    - `[TagWhitelistJson <String>]`: Pobiera lub ustawia ciąg JSON zawierający listę tagów, które są na liście na białej liście do użycia w punkcie końcowym wypychania rejestracji.
    - `[TagsRequiringAuth <String>]`: Pobiera lub ustawia ciąg JSON zawierający listę tagów, które wymagają uwierzytelniania użytkownika w punkcie końcowym wypychania rejestracji.         Tagi mogą składać się ze znaków alfanumerycznych i następujących znaków: '_', '@', '#', '.', ':', '-'.         Sprawdzanie poprawności należy przeprowadzić na stronie PushRequestHandler.
    - `[TracingOption <String>]`: Opcje śledzenia.
    - `[TriggerPrivateBytesInKb <Int32?>]`: reguła oparta na bajtach prywatnych.
    - `[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: reguła oparta na kodach stanów.
      - `[Count <Int32?>]`: Liczba żądań.
      - `[Status <Int32?>]`: kod stanu HTTP.
      - `[SubStatus <Int32?>]`: Zażądaj stanu podrzędnego.
      - `[TimeInterval <String>]`: interwał czasu.
      - `[Win32Status <Int32?>]`: Kod błędu win32.
    - `[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> aby użyć 32-bitowego procesu pracownika; w przeciwnym <code>false</code> razie.
    - `[VirtualApplication <IVirtualApplication[]>]`: aplikacje wirtualne.
      - `[PhysicalPath <String>]`: Ścieżka fizyczna.
      - `[PreloadEnabled <Boolean?>]`: <code>true</code> jeśli wstępne ładowanie jest włączone; w przeciwnym <code>false</code> razie.
      - `[VirtualDirectory <IVirtualDirectory[]>]`: katalogi wirtualne dla aplikacji wirtualnej.
        - `[PhysicalPath <String>]`: Ścieżka fizyczna.
        - `[VirtualPath <String>]`: Ścieżka do aplikacji wirtualnej.
      - `[VirtualPath <String>]`: Ścieżka wirtualna.
    - `[VnetName <String>]`: nazwa sieci wirtualnej.
    - `[WebSocketsEnabled <Boolean?>]`: <code>true</code> jeśli funkcja WebSocket jest włączona; w przeciwnym <code>false</code> razie.
    - `[WindowsFxVersion <String>]`: Xenon App Framework i wersja
    - `[XManagedServiceIdentityId <Int32?>]`: Jawny identyfikator tożsamości usługi zarządzanej
  - `[ContainerSize <Int32?>]`: rozmiar kontenera funkcji.
  - `[DailyMemoryTimeQuota <Int32?>]`: Maksymalny dozwolony dzienny przydział czasu pamięci (obowiązuje tylko w przypadku aplikacji dynamicznych).
  - `[Enabled <Boolean?>]`: <code>true</code> jeśli aplikacja jest włączona; w przeciwnym <code>false</code> razie. Ustawienie wartości fałsz powoduje wyłączenie aplikacji (przenosi ją do trybu offline).
  - `[HostNameSslState <IHostNameSslState[]>]`: Stany SSL o nazwie hosta służą do zarządzania powiązaniami SSL dla nazw hostów aplikacji.
    - `[HostType <HostType?>]`: wskazuje, czy nazwa hosta jest standardową, czy nazwą hosta repozytorium.
    - `[Name <String>]`: Nazwa hosta.
    - `[SslState <SslState?>]`: typ SSL.
    - `[Thumbprint <String>]`: Thumbprint certyfikatu SSL.
    - `[ToUpdate <Boolean?>]`: ustaw, <code>true</code> aby zaktualizować istniejącą nazwę hosta.
    - `[VirtualIP <String>]`: wirtualny adres IP przypisany do nazwy hosta, jeśli jest włączony protokół SSL oparty na adresie IP.
  - `[HostNamesDisabled <Boolean?>]`: <code>true</code> aby wyłączyć publiczne nazwy hostów aplikacji; w przeciwnym <code>false</code> razie.          Jeśli, <code>true</code> aplikacja jest dostępna tylko za pośrednictwem procesu zarządzania interfejsem API.
  - `[HostingEnvironmentProfileId <String>]`: Identyfikator zasobu w środowisku usługi aplikacji.
  - `[HttpsOnly <Boolean?>]`: HttpsOnly: konfiguruje witrynę sieci Web tak, aby akceptowała tylko żądania https. Przekierowywanie problemów dla żądań http
  - `[HyperV <Boolean?>]`: Piaskownica Hyper-V.
  - `[IdentityType <ManagedServiceIdentityType?>]`: typ tożsamości usługi zarządzanej.
  - `[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: lista tożsamości przypisanych do użytkownika skojarzonych z zasobem. Odwołania do kluczy słownika tożsamości użytkownika będą ARM identyfikatorami zasobów w postaci: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}
    - `[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: Wskazuje to, że do tego obiektu można dodać dowolną właściwość.
  - `[IsXenon <Boolean?>]`: Przestarzałe: piaskownica Hyper-V.
  - `[RedundancyMode <RedundancyMode?>]`: tryb nadmiarowości witryn
  - `[Reserved <Boolean?>]`: <code>true</code> jeśli zarezerwowane; w przeciwnym <code>false</code> razie.
  - `[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> aby zatrzymać witrynę SCM (KUDU), gdy aplikacja zostanie zatrzymana; w przeciwnym <code>false</code> razie. Wartość domyślna <code>false</code> to.
  - `[ServerFarmId <String>]`: Identyfikator zasobu skojarzonego planu usługi aplikacji w formacie: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".

## LINKI POKREWNE

