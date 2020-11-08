---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/remove-azfunctionappsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppSetting.md
ms.openlocfilehash: abfa704b042b0a8cd25b8682e3b93306b5ca6277
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224382"
---
# Remove-AzFunctionAppSetting

## STRESZCZENIe
Usuwa ustawienia aplikacji z aplikacji funkcji.

## POLECENIA

### ByName (domyślny)
```
Remove-AzFunctionAppSetting -Name <String> -ResourceGroupName <String> -AppSettingName <String[]>
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### ByObjectInput
```
Remove-AzFunctionAppSetting -AppSettingName <String[]> -InputObject <ISite> [-Force]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## Opis
Usuwa ustawienia aplikacji z aplikacji funkcji.

## Przykłady

### Przykład 1: usuwanie ustawień aplikacji w aplikacji funkcji.
```powershell
PS C:\> Remove-AzFunctionAppSetting -Name MyAppName -ResourceGroupName MyResourceGroupName -AppSettingName "MyAppSetting1", "MyAppSetting2"
```

To polecenie usuwa ustawienia aplikacji w aplikacji funkcji.

## PARAMETRÓW

### -AppSettingName
Lista ustawień aplikacji funkcji, które mają zostać usunięte z aplikacji funkcji.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
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

### -Force
Wymusza usunięcie aplikacji funkcji cmdlet bez monitowania o potwierdzenie.

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

### -Inputobject
Aby skonstruować, zobacz sekcję notatki dla właściwości INPUTobject i Utwórz tablicę skrótów.

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

### -Name (nazwa)
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

### -ResourceGroupName
Nazwa grupy zasobów, do której należy zasób.

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

### -Subskrypcji
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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### Microsoft. Azure. PowerShell. polecenia. Functions. models. Api20190801. ISite

## WYSYŁA

### Microsoft. Azure. PowerShell. polecenia. Functions. models. Api20190801. IStringDictionary

## INFORMACYJN

PISUJE

ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW

Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości. Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.


INPUTobject <ISite> : 
  - `Location <String>`: Lokalizacja zasobu.
  - `CloningInfoSourceWebAppId <String>`: Identyfikator zasobu ARM aplikacji źródłowej. Identyfikator zasobu aplikacji ma postać/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} dla gniazd produkcyjnych i/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} dla innych gniazd.
  - `[Kind <String>]`: Rodzaj zasobu.
  - `[Tag <IResourceTags>]`: Znaczniki zasobów.
    - `[(Any) <String>]`: Wskazuje, że do tego obiektu można dodać dowolną właściwość.
  - `[ClientAffinityEnabled <Boolean?>]`: <code>true</code> Aby włączyć koligację klienta <code>false</code> , zatrzymywanie wysyłania plików cookie koligacji sesji, które umożliwiają kierowanie żądań klientów w tej samej sesji do tego samego wystąpienia. Wartość domyślna to <code>true</code> .
  - `[ClientCertEnabled <Boolean?>]`: <code>true</code> Aby włączyć uwierzytelnianie certyfikatu klienta (uwierzytelnianie obustronne TLS); w przeciwnym razie <code>false</code> . Wartość domyślna to <code>false</code> .
  - `[ClientCertExclusionPath <String>]`: uwierzytelnianie certyfikatu klienta ścieżki wykluczeń rozdzielanych przecinkami
  - `[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Ustawienia aplikacji zastępują dla sklonowanej aplikacji. Jeśli to ustawienie zostanie określone, te ustawienia zastępują ustawienia sklonowane z aplikacji źródłowej. W przeciwnym razie ustawienia aplikacji z aplikacji źródłowej są zachowywane.
    - `[(Any) <String>]`: Wskazuje, że do tego obiektu można dodać dowolną właściwość.
  - `[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> Aby sklonować niestandardowe nazwy hostów z aplikacji źródłowej; w przeciwnym razie <code>false</code> .
  - `[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> Aby sklonować kontrolę źródła z aplikacji źródłowej, w przeciwnym razie <code>false</code> .
  - `[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> Aby skonfigurować równoważenie obciążenia dla aplikacji źródłowej i docelowej.
  - `[CloningInfoCorrelationId <String>]`: Identyfikator korelacji operacji klonowania. Ten identyfikator polega na wielu operacjach klonowania razem, aby użyć tej samej migawki.
  - `[CloningInfoHostingEnvironment <String>]`: Środowisko App Service Environment.
  - `[CloningInfoOverwrite <Boolean?>]`: <code>true</code> Aby zastąpić aplikację docelową, w przeciwnym razie <code>false</code> .
  - `[CloningInfoSourceWebAppLocation <String>]`: Lokalizacja aplikacji źródłowej: Zachodnia USA lub Europa Północna
  - `[CloningInfoTrafficManagerProfileId <String>]`: Identyfikator zasobu ARM profilu usługi Traffic Manager, który ma być używany, jeśli istnieje. Identyfikator zasobu usługi Traffic Manager ma postać/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.
  - `[CloningInfoTrafficManagerProfileName <String>]`: Nazwa profilu usługi Traffic Manager do utworzenia. Jest to potrzebne tylko wtedy, gdy profil w usłudze Traffic Manager już nie istnieje.
  - `[Config <ISiteConfig>]`: Konfiguracja aplikacji.
    - `IsPushEnabled <Boolean>`: Pobiera lub ustawia flagę wskazującą, czy punkt końcowy jest włączony.
    - `[ActionMinProcessExecutionTime <String>]`: Minimalny czas przetwarzania procesu przed wykonaniem akcji
    - `[ActionType <AutoHealActionType?>]`: Wstępnie zdefiniowana akcja do wykonania.
    - `[AlwaysOn <Boolean?>]`: <code>true</code> Jeśli funkcja zawsze włączony jest włączona, w przeciwnym razie <code>false</code> .
    - `[ApiDefinitionUrl <String>]`: Adres URL definicji interfejsu API.
    - `[ApiManagementConfigId <String>]`: Identyfikator APIM-Api.
    - `[AppCommandLine <String>]`: Wiersz polecenia aplikacji, który ma zostać uruchomiony.
    - `[AppSetting <INameValuePair[]>]`: Ustawienia aplikacji.
      - `[Name <String>]`: Nazwa pary.
      - `[Value <String>]`: Wartość pary.
    - `[AutoHealEnabled <Boolean?>]`: <code>true</code> Jeśli funkcja automatycznego dopasowywania jest włączona, w przeciwnym razie <code>false</code> .
    - `[AutoSwapSlotName <String>]`: Automatyczne zamienianie nazwy gniazda.
    - `[ConnectionString <IConnStringInfo[]>]`: Parametry połączenia.
      - `[ConnectionString <String>]`: Wartość parametrów połączenia.
      - `[Name <String>]`: Nazwa ciągu połączenia.
      - `[Type <ConnectionStringType?>]`: Typ bazy danych.
    - `[CorAllowedOrigin <String[]>]`: Pobiera lub ustawia listę źródeł, którym należy zezwolić na nawiązywanie połączeń między pochodzeniu (na przykład: http://example.com:12345) . Użyj znaku "*", aby zezwolić wszystkim.
    - `[CorSupportCredentials <Boolean?>]`: Pobiera lub ustawia, czy żądania CORS z poświadczeniami są dozwolone. https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentialsAby uzyskać więcej informacji, zobacz.
    - `[CustomActionExe <String>]`: Plik wykonywalny do uruchomienia.
    - `[CustomActionParameter <String>]`: Parametry pliku wykonywalnego.
    - `[DefaultDocument <String[]>]`: Dokumenty domyślne.
    - `[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> Jeśli jest włączony szczegółowy dziennik błędów; w przeciwnym razie <code>false</code> .
    - `[DocumentRoot <String>]`: Katalog główny dokumentu.
    - `[DynamicTagsJson <String>]`: Pobiera lub ustawia ciąg JSON zawierający listę tagów dynamicznych, które będą oceniane na podstawie oświadczeń użytkownika w punkcie końcowym rejestracji wypychanej.
    - `[ExperimentRampUpRule <IRampUpRule[]>]`: Lista reguł dopełnienia.
      - `[ActionHostName <String>]`: Nazwa hosta gniazda, do którego będzie przekierowywany ruch w przypadku podjęcia decyzji. Przykład. myapp-stage.azurewebsites.net.
      - `[ChangeDecisionCallbackUrl <String>]`: W rozszerzeniu witryny programu TiPCallback można podać adres URL, który może być określony. Zobacz rozszerzenie witryny TiPCallback dla szkieletu i kontraktów.         https://www.siteextensions.net/packages/TiPCallback/
      - `[ChangeIntervalInMinute <Int32?>]`: Określa interwał w minutach w celu przeszacowania ReroutePercentage.
      - `[ChangeStep <Double?>]`: W scenariuszu automatycznego zwiększania poziomu w górę jest to krok do dodania/usunięcia, <code>ReroutePercentage</code> dopóki nie osiągnie on \n <code>MinReroutePercentage</code> lub         <code>MaxReroutePercentage</code> . Metryki witryn są sprawdzane co N minut określonych w <code>ChangeIntervalInMinutes</code> .\nCustom algorytm decyzyjny może być podany w TiPCallback rozszerzeniu witryny, w którym można określić adres URL <code>ChangeDecisionCallbackUrl</code> .
      - `[MaxReroutePercentage <Double?>]`: Określa górną granicę, poniżej której ReroutePercentage pozostanie.
      - `[MinReroutePercentage <Double?>]`: Określa dolną granicę, powyżej której ReroutePercentage będzie się utrzymywać.
      - `[Name <String>]`: Nazwa reguły routingu. Zalecaną nazwą będzie wskazanie gniazda, które otrzyma dane doświadczenie.
      - `[ReroutePercentage <Double?>]`: Procent ruchu, do którego będzie przekierowywany <code>ActionHostName</code> .
    - `[FtpsState <FtpsState?>]`: Stan usługi FTP/FTPS
    - `[HandlerMapping <IHandlerMapping[]>]`: Mapowania obsługi.
      - `[Argument <String>]`: Argumenty wiersza polecenia, które mają być przekazywane do procesora skryptów.
      - `[Extension <String>]`: Żądania dotyczące tego rozszerzenia będą obsługiwane przy użyciu określonej aplikacji FastCGI.
      - `[ScriptProcessor <String>]`: Ścieżka bezwzględna do aplikacji FastCGI.
    - `[HealthCheckPath <String>]`: Ścieżka kontroli kondycji
    - `[Http20Enabled <Boolean?>]`: Http20Enabled: konfiguruje witrynę sieci Web, aby umożliwić klientom nawiązywanie połączenia za pośrednictwem protokołu HTTP 2.0
    - `[HttpLoggingEnabled <Boolean?>]`: <code>true</code> Jeśli rejestrowanie http jest włączone; w przeciwnym razie <code>false</code> .
    - `[IPSecurityRestriction <IIPSecurityRestriction[]>]`: Ograniczenia zabezpieczeń IP dla głównego.
      - `[Action <String>]`: Zezwalanie na dostęp lub odmawianie dostępu do tego zakresu adresów IP.
      - `[Description <String>]`: Opis reguły ograniczeń adresów IP.
      - `[IPAddress <String>]`: Adres IP obowiązuje ograniczenie zabezpieczeń.         Może być w formie czystych adresów IPv4 (wymaganej właściwości maska_podsieci) lub notacji CIDR, takiej jak IPv4/Maska (z wiodącym dopasowaniem bitów). W przypadku CIDR nie wolno określać właściwości maska_podsieci.
      - `[Name <String>]`: Nazwa reguły ograniczania adresu IP.
      - `[Priority <Int32?>]`: Priorytet reguły ograniczenia IP.
      - `[SubnetMask <String>]`: Maska podsieci dla zakresu adresów IP, dla których obowiązuje ograniczenie.
      - `[SubnetTrafficTag <Int32?>]`: (wewnętrzny) znacznik ruchu podsieci
      - `[Tag <IPFilterTag?>]`: Określa, do czego będzie stosowany ten filtr IP. Jest to obsługa filtrowania adresów IP na serwerach proxy.
      - `[VnetSubnetResourceId <String>]`: Identyfikator zasobu sieci wirtualnej
      - `[VnetTrafficTag <Int32?>]`: (wewnętrzny) tag ruchu w sieci VNET
    - `[JavaContainer <String>]`: Kontener Java.
    - `[JavaContainerVersion <String>]`: Wersja kontenera Java.
    - `[JavaVersion <String>]`: Wersja Java.
    - `[LimitMaxDiskSizeInMb <Int64?>]`: Maksymalne dozwolone użycie rozmiaru dysku (w MB).
    - `[LimitMaxMemoryInMb <Int64?>]`: Maksymalne dozwolone użycie pamięci w MB.
    - `[LimitMaxPercentageCpu <Double?>]`: Maksymalny dozwolony procent użycia procesora CPU.
    - `[LinuxFxVersion <String>]`: Struktura i wersja aplikacji Linux
    - `[LoadBalancing <SiteLoadBalancing?>]`: Równoważenie obciążenia witryny.
    - `[LocalMySqlEnabled <Boolean?>]`: <code>true</code> Aby włączyć lokalną MySQL; w przeciwnym razie <code>false</code> .
    - `[LogsDirectorySizeLimit <Int32?>]`: Limit rozmiaru katalogu dziennika HTTP.
    - `[MachineKeyDecryption <String>]`: Algorytm używany do odszyfrowywania.
    - `[MachineKeyDecryptionKey <String>]`: Klucz odszyfrowujący.
    - `[MachineKeyValidation <String>]`: MachineKey sprawdzanie poprawności.
    - `[MachineKeyValidationKey <String>]`: Klucz sprawdzania poprawności.
    - `[ManagedPipelineMode <ManagedPipelineMode?>]`: Zarządzany tryb potokowy.
    - `[ManagedServiceIdentityId <Int32?>]`: Zarządzany identyfikator tożsamości usługi
    - `[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: konfiguruje minimalną wersję TLS wymaganą dla żądań SSL
    - `[NetFrameworkVersion <String>]`: Wersja programu .NET Framework.
    - `[NodeVersion <String>]`: Wersja programu Node.js.
    - `[NumberOfWorker <Int32?>]`: Liczba pracowników.
    - `[PhpVersion <String>]`: Wersja programu PHP.
    - `[PowerShellVersion <String>]`: Wersja programu PowerShell.
    - `[PreWarmedInstanceCount <Int32?>]`: Liczba przedgrzanych wystąpień.         To ustawienie dotyczy tylko planów zużycia i elastyczności
    - `[PublishingUsername <String>]`: Publikowanie nazwy użytkownika.
    - `[PushKind <String>]`: Rodzaj zasobu.
    - `[PythonVersion <String>]`: Wersja języka Python.
    - `[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> Jeśli debugowanie zdalne jest włączone, w przeciwnym razie <code>false</code> .
    - `[RemoteDebuggingVersion <String>]`: Zdalna wersja debugowania.
    - `[RequestCount <Int32?>]`: Liczba żądań.
    - `[RequestTimeInterval <String>]`: Interwał czasowy.
    - `[RequestTracingEnabled <Boolean?>]`: <code>true</code> Jeśli śledzenie żądań jest włączone, w przeciwnym razie <code>false</code> .
    - `[RequestTracingExpirationTime <DateTime?>]`: Czas wygaśnięcia śledzenia żądań.
    - `[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: Ograniczenia zabezpieczeń IP dla SCM.
    - `[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: Ograniczenia zabezpieczeń IP dla SCM umożliwiają korzystanie z głównego.
    - `[ScmType <ScmType?>]`: Typ SCM.
    - `[SlowRequestCount <Int32?>]`: Liczba żądań.
    - `[SlowRequestTimeInterval <String>]`: Interwał czasowy.
    - `[SlowRequestTimeTaken <String>]`: Czas trwania.
    - `[TagWhitelistJson <String>]`: Pobiera lub ustawia ciąg JSON zawierający listę tagów, które są whitelisted do użytku w punkcie końcowym rejestracji wypychanej.
    - `[TagsRequiringAuth <String>]`: Pobiera lub ustawia ciąg JSON zawierający listę tagów, które wymagają uwierzytelnienia użytkownika do użycia w punkcie końcowym rejestracji wypychanej.         Tagi mogą składać się z znaków alfanumerycznych i następujących elementów: _, "@", "#", ".", ":", "-".         Sprawdzanie poprawności należy przeprowadzić na PushRequestHandler.
    - `[TracingOption <String>]`: Opcje śledzenia.
    - `[TriggerPrivateBytesInKb <Int32?>]`: Reguła oparta na bajtach prywatnych.
    - `[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: Reguła oparta na kodach statusu.
      - `[Count <Int32?>]`: Liczba żądań.
      - `[Status <Int32?>]`: Kod stanu HTTP.
      - `[SubStatus <Int32?>]`: Żądanie podrzędne o statusie.
      - `[TimeInterval <String>]`: Interwał czasowy.
      - `[Win32Status <Int32?>]`: Kod błędu Win32.
    - `[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> Aby używać usługi 32-bitowego procesu roboczego, w przeciwnym razie <code>false</code> .
    - `[VirtualApplication <IVirtualApplication[]>]`: Aplikacje wirtualne.
      - `[PhysicalPath <String>]`: Ścieżka fizyczna.
      - `[PreloadEnabled <Boolean?>]`: <code>true</code> Jeśli wstępne ładowanie jest włączone; w przeciwnym razie <code>false</code> .
      - `[VirtualDirectory <IVirtualDirectory[]>]`: Katalogi wirtualne aplikacji wirtualnej.
        - `[PhysicalPath <String>]`: Ścieżka fizyczna.
        - `[VirtualPath <String>]`: Ścieżka do aplikacji wirtualnej.
      - `[VirtualPath <String>]`: Ścieżka wirtualna.
    - `[VnetName <String>]`: Nazwa sieci wirtualnej.
    - `[WebSocketsEnabled <Boolean?>]`: <code>true</code> Jeśli protokół WebSocket jest włączony; w przeciwnym razie <code>false</code> .
    - `[WindowsFxVersion <String>]`: Struktura i wersja aplikacji Xenon
    - `[XManagedServiceIdentityId <Int32?>]`: Jawny identyfikator tożsamości usługi zarządzanej
  - `[ContainerSize <Int32?>]`: Rozmiar kontenera funkcji.
  - `[DailyMemoryTimeQuota <Int32?>]`: Maksymalny dozwolony przydział czasu na pamięć (dotyczy tylko aplikacji dynamicznych).
  - `[Enabled <Boolean?>]`: <code>true</code> Jeśli aplikacja jest włączona, w przeciwnym razie <code>false</code> . Ustawienie tej wartości na wartość FAŁSZ wyłącza aplikację (Pobiera aplikację w trybie offline).
  - `[HostNameSslState <IHostNameSslState[]>]`: Stany SSL hosta służą do zarządzania powiązaniami protokołu SSL dla hostów aplikacji.
    - `[HostType <HostType?>]`: Wskazuje, czy nazwa hosta jest nazwą hosta standardowego, czy repozytorium.
    - `[Name <String>]`Nazwą.
    - `[SslState <SslState?>]`: Typ protokołu SSL.
    - `[Thumbprint <String>]`: Odcisk palca certyfikatu SSL.
    - `[ToUpdate <Boolean?>]`: Ustawienie w celu <code>true</code> zaktualizowania istniejącej nazwy hosta.
    - `[VirtualIP <String>]`: Wirtualny adres IP przypisany do nazwy hosta, jeśli jest włączony protokół SSL oparty na protokole IP.
  - `[HostNamesDisabled <Boolean?>]`: <code>true</code> Aby wyłączyć publiczne nazwy hostów aplikacji; w przeciwnym razie <code>false</code> .          Jeśli <code>true</code> aplikacja jest dostępna tylko za pośrednictwem procesu zarządzania interfejsem API.
  - `[HostingEnvironmentProfileId <String>]`: Identyfikator zasobu środowiska App Service Environment.
  - `[HttpsOnly <Boolean?>]`: HttpsOnly: konfiguruje witrynę sieci Web w celu akceptowania tylko żądań HTTPS. Problemy z przekierowaniem dla żądań http
  - `[HyperV <Boolean?>]`: Piaskownica funkcji Hyper-V.
  - `[IdentityType <ManagedServiceIdentityType?>]`: Typ zarządzanej tożsamości usługi.
  - `[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: Lista tożsamości przypisanych użytkownikowi skojarzonych z zasobem. Odwołania do kluczy słownika tożsamości użytkownika będą miały identyfikatory zasobów ARM w formularzu: "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}
    - `[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: Wskazuje, że do tego obiektu można dodać dowolną właściwość.
  - `[IsXenon <Boolean?>]`: Przestarzałe: Piaskownica funkcji Hyper-V.
  - `[RedundancyMode <RedundancyMode?>]`: Tryb nadmiarowości witryny
  - `[Reserved <Boolean?>]`: <code>true</code> Jeśli jest zarezerwowany; w przeciwnym razie <code>false</code> .
  - `[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> Aby zatrzymać witrynę SCM (KUDU), gdy aplikacja zostanie zatrzymana, w przeciwnym razie <code>false</code> . Wartość domyślna to <code>false</code> .
  - `[ServerFarmId <String>]`: Identyfikator zasobu skojarzonego planu usługi App Service, sformatowana jako: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".

## LINKI POKREWNE

