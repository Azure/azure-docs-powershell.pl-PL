---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 9D821623-DEF9-49E4-9C44-10643A92A2E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7f6690aa45125a0d1b3383b08443234f47a1f7e3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054399"
---
# <span data-ttu-id="e3be9-101">Set-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="e3be9-101">Set-AzureWebsite</span></span>

## <span data-ttu-id="e3be9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e3be9-102">SYNOPSIS</span></span>
<span data-ttu-id="e3be9-103">Umożliwia skonfigurowanie witryny sieci Web działającej na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="e3be9-103">Configures a website running in Azure.</span></span>

## <span data-ttu-id="e3be9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e3be9-104">SYNTAX</span></span>

```
Set-AzureWebsite [-NumberOfWorkers <Int32>] [-DefaultDocuments <String[]>] [-NetFrameworkVersion <String>]
 [-PhpVersion <String>] [-RequestTracingEnabled <Boolean>] [-HttpLoggingEnabled <Boolean>]
 [-DetailedErrorLoggingEnabled <Boolean>] [-HostNames <String[]>] [-AppSettings <Hashtable>]
 [-Metadata <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.NameValuePair]>]
 [-ConnectionStrings <ConnStringPropertyBag>] [-HandlerMappings <HandlerMapping[]>]
 [-SiteWithConfig <SiteWithConfig>] [-PassThru] [-ManagedPipelineMode <ManagedPipelineMode>]
 [-WebSocketsEnabled <Boolean>]
 [-RoutingRules <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.RoutingRule]>]
 [-Use32BitWorkerProcess <Boolean>] [-AutoSwapSlotName <String>]
 [-SlotStickyAppSettingNames <System.Collections.Generic.List`1[System.String]>]
 [-SlotStickyConnectionStringNames <System.Collections.Generic.List`1[System.String]>] [-Name <String>]
 [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e3be9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e3be9-105">DESCRIPTION</span></span>
<span data-ttu-id="e3be9-106">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e3be9-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="e3be9-107">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="e3be9-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="e3be9-108">Polecenie cmdlet **Set-AzureWebsite** umożliwia skonfigurowanie witryny sieci Web działającej na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="e3be9-108">The **Set-AzureWebsite** cmdlet configures a website running in Azure.</span></span>

## <span data-ttu-id="e3be9-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e3be9-109">EXAMPLES</span></span>

### <span data-ttu-id="e3be9-110">Przykład 1: Włączanie rejestrowania HTTP dla witryny sieci Web</span><span class="sxs-lookup"><span data-stu-id="e3be9-110">Example 1: Enable HTTP logging for a website</span></span>
```
PS C:\> Set-AzureWebsite -HttpLoggingEnabled 1
```

<span data-ttu-id="e3be9-111">W tym przykładzie przedstawiono możliwość rejestrowania HTTP.</span><span class="sxs-lookup"><span data-stu-id="e3be9-111">This example enables HTTP logging.</span></span>

### <span data-ttu-id="e3be9-112">Przykład 2: Ustawianie poświadczeń magazynowania dla witryny sieci Web</span><span class="sxs-lookup"><span data-stu-id="e3be9-112">Example 2: Set storage credentials for a website</span></span>
```
PS C:\> $settings = New-Object Hashtable$settings["AZURE_STORAGE_ACCOUNT"= myaccountname$settings["AZURE_STORAGE_ACCESS_KEY"] = myaccesskeySet-AzureWebsite -AppSettings $settings myWebsite
```

<span data-ttu-id="e3be9-113">W tym przykładzie są ustawiane poświadczenia magazynowania w witrynie sieci Web o nazwie Moja witryna sieci Web ze zmiennymi środowiskowymi dla AZURE_STORAGE_ACCOUNT i AZURE_STORAGE_ACCESS_KEY.</span><span class="sxs-lookup"><span data-stu-id="e3be9-113">This example sets storage credentials in a website named myWebsite with environment variables for AZURE_STORAGE_ACCOUNT and AZURE_STORAGE_ACCESS_KEY.</span></span>

## <span data-ttu-id="e3be9-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e3be9-114">PARAMETERS</span></span>

### <span data-ttu-id="e3be9-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="e3be9-115">-AppSettings</span></span>
<span data-ttu-id="e3be9-116">Określa zmienne środowiskowe, które będą używane przez witrynę sieci Web.</span><span class="sxs-lookup"><span data-stu-id="e3be9-116">Specifies the environment variables that will be used by the website.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3be9-117">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="e3be9-117">-AutoSwapSlotName</span></span>
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

### <span data-ttu-id="e3be9-118">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="e3be9-118">-ConnectionStrings</span></span>
<span data-ttu-id="e3be9-119">Określa parametry połączenia używane w witrynie sieci Web.</span><span class="sxs-lookup"><span data-stu-id="e3be9-119">Specifies the connection strings used by the website.</span></span>

```yaml
Type: ConnStringPropertyBag
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3be9-120">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="e3be9-120">-DefaultDocuments</span></span>
<span data-ttu-id="e3be9-121">Określa dokumenty, które są automatycznie wyświetlane podczas przeglądania witryny sieci Web.</span><span class="sxs-lookup"><span data-stu-id="e3be9-121">Specifies the documents that are automatically displayed when browsing the website.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3be9-122">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="e3be9-122">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="e3be9-123">Określa, czy w witrynie sieci Web są rejestrowane szczegółowe błędy usług IIS.</span><span class="sxs-lookup"><span data-stu-id="e3be9-123">Determines whether detailed IIS errors are logged for the website.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3be9-124">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="e3be9-124">-HandlerMappings</span></span>
<span data-ttu-id="e3be9-125">Określa mapowania obsługi używane w witrynie sieci Web.</span><span class="sxs-lookup"><span data-stu-id="e3be9-125">Specifies the handler mappings used by the website.</span></span>

```yaml
Type: HandlerMapping[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3be9-126">-Nazwa_hostas</span><span class="sxs-lookup"><span data-stu-id="e3be9-126">-HostNames</span></span>
<span data-ttu-id="e3be9-127">Określa w pełni kwalifikowane nazwy hostów, które mogą być używane do uzyskiwania dostępu do witryny sieci Web.</span><span class="sxs-lookup"><span data-stu-id="e3be9-127">Specifies the fully qualified host names that can be used to access the website.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3be9-128">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="e3be9-128">-HttpLoggingEnabled</span></span>
<span data-ttu-id="e3be9-129">Określa, czy rejestrowanie http jest włączone dla witryny sieci Web.</span><span class="sxs-lookup"><span data-stu-id="e3be9-129">Determines whether http logging is enabled for the website.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3be9-130">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="e3be9-130">-ManagedPipelineMode</span></span>
<span data-ttu-id="e3be9-131">Określa zarządzany tryb potokowy.</span><span class="sxs-lookup"><span data-stu-id="e3be9-131">Specifies the managed pipeline mode.</span></span>

```yaml
Type: ManagedPipelineMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3be9-132">-Metadata</span><span class="sxs-lookup"><span data-stu-id="e3be9-132">-Metadata</span></span>
<span data-ttu-id="e3be9-133">Określa metadane witryny sieci Web.</span><span class="sxs-lookup"><span data-stu-id="e3be9-133">Specifies the metadata for the website.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.NameValuePair]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3be9-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e3be9-134">-Name</span></span>
<span data-ttu-id="e3be9-135">Określa nazwę witryny sieci Web.</span><span class="sxs-lookup"><span data-stu-id="e3be9-135">Specifies the name of the website.</span></span>

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

### <span data-ttu-id="e3be9-136">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="e3be9-136">-NetFrameworkVersion</span></span>
<span data-ttu-id="e3be9-137">Określa wersję platformy .NET Framework wymaganą przez witrynę sieci Web.</span><span class="sxs-lookup"><span data-stu-id="e3be9-137">Specifies the version of the .Net Framework required by the website.</span></span>

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

### <span data-ttu-id="e3be9-138">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="e3be9-138">-NumberOfWorkers</span></span>
<span data-ttu-id="e3be9-139">Określa liczbę procesów roboczych, w których jest uruchomiona witryna sieci Web.</span><span class="sxs-lookup"><span data-stu-id="e3be9-139">Specifies the number of worker processes running the website.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3be9-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e3be9-140">-PassThru</span></span>
<span data-ttu-id="e3be9-141">Wskazuje, że to polecenie cmdlet zwraca wartość **logiczną** .</span><span class="sxs-lookup"><span data-stu-id="e3be9-141">Indicates that this cmdlet returns a **Boolean** value.</span></span>

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

### <span data-ttu-id="e3be9-142">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="e3be9-142">-PhpVersion</span></span>
<span data-ttu-id="e3be9-143">Określa wersję PHP wymaganą przez witrynę sieci Web.</span><span class="sxs-lookup"><span data-stu-id="e3be9-143">Specifies the PHP version required by the website.</span></span>

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

### <span data-ttu-id="e3be9-144">-Profile</span><span class="sxs-lookup"><span data-stu-id="e3be9-144">-Profile</span></span>
<span data-ttu-id="e3be9-145">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3be9-145">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e3be9-146">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="e3be9-146">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e3be9-147">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="e3be9-147">-RequestTracingEnabled</span></span>
<span data-ttu-id="e3be9-148">Określa, czy śledzenie żądań jest włączone dla witryny sieci Web.</span><span class="sxs-lookup"><span data-stu-id="e3be9-148">Determines whether request tracing is enabled for the website.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3be9-149">-RoutingRules</span><span class="sxs-lookup"><span data-stu-id="e3be9-149">-RoutingRules</span></span>
<span data-ttu-id="e3be9-150">Określa reguły routingu, które mają być używane do testów w produkcji.</span><span class="sxs-lookup"><span data-stu-id="e3be9-150">Specifies the routing rules to use for testing in production.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.RoutingRule]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3be9-151">-SiteWithConfig</span><span class="sxs-lookup"><span data-stu-id="e3be9-151">-SiteWithConfig</span></span>
<span data-ttu-id="e3be9-152">Określa konfigurację używaną w witrynie sieci Web.</span><span class="sxs-lookup"><span data-stu-id="e3be9-152">Specifies the configuration used by the website.</span></span>

```yaml
Type: SiteWithConfig
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3be9-153">-Slot</span><span class="sxs-lookup"><span data-stu-id="e3be9-153">-Slot</span></span>
<span data-ttu-id="e3be9-154">Określa nazwę gniazda witryny sieci Web.</span><span class="sxs-lookup"><span data-stu-id="e3be9-154">Specifies the slot name of the website.</span></span>

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

### <span data-ttu-id="e3be9-155">-SlotStickyAppSettingNames</span><span class="sxs-lookup"><span data-stu-id="e3be9-155">-SlotStickyAppSettingNames</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3be9-156">-SlotStickyConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="e3be9-156">-SlotStickyConnectionStringNames</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3be9-157">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="e3be9-157">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="e3be9-158">Określa, czy włączyć tryb 32-bitowy.</span><span class="sxs-lookup"><span data-stu-id="e3be9-158">Specifies whether to enable 32-bit mode.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3be9-159">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="e3be9-159">-WebSocketsEnabled</span></span>
<span data-ttu-id="e3be9-160">Określa, czy włączyć obiekty WebSocket.</span><span class="sxs-lookup"><span data-stu-id="e3be9-160">Specifies whether to enable WebSockets.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3be9-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3be9-161">CommonParameters</span></span>
<span data-ttu-id="e3be9-162">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3be9-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3be9-163">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3be9-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3be9-164">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e3be9-164">INPUTS</span></span>

## <span data-ttu-id="e3be9-165">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e3be9-165">OUTPUTS</span></span>

## <span data-ttu-id="e3be9-166">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e3be9-166">NOTES</span></span>

## <span data-ttu-id="e3be9-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e3be9-167">RELATED LINKS</span></span>

[<span data-ttu-id="e3be9-168">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="e3be9-168">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="e3be9-169">Nowe — AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="e3be9-169">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="e3be9-170">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="e3be9-170">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)


