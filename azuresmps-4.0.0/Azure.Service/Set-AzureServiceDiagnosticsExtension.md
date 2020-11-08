---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2E738CEF-BBDD-425D-B12C-86FF7C45A634
online version: ''
schema: 2.0.0
ms.openlocfilehash: 518528d4af8889cf36b30c417e0170e0ea228ebf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055013"
---
# <span data-ttu-id="e31a8-101">Set-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="e31a8-101">Set-AzureServiceDiagnosticsExtension</span></span>

## <span data-ttu-id="e31a8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e31a8-102">SYNOPSIS</span></span>
<span data-ttu-id="e31a8-103">Umożliwia rozszerzenie usługi Azure Diagnostics w określonych rolach lub we wszystkich rolach w wdrożonej usłudze lub wdrożeniu.</span><span class="sxs-lookup"><span data-stu-id="e31a8-103">Enables Azure Diagnostics extension on specified roles or all roles on a deployed service or at deployment.</span></span>

## <span data-ttu-id="e31a8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e31a8-104">SYNTAX</span></span>

### <span data-ttu-id="e31a8-105">Setextension (domyślne)</span><span class="sxs-lookup"><span data-stu-id="e31a8-105">SetExtension (Default)</span></span>
```
Set-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [[-StorageAccountName] <String>]
 [[-StorageAccountKey] <String>] [[-StorageAccountEndpoint] <String>] [[-StorageContext] <AzureStorageContext>]
 [-DiagnosticsConfigurationPath] <String> [[-Version] <String>] [[-ExtensionId] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="e31a8-106">SetExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="e31a8-106">SetExtensionUsingThumbprint</span></span>
```
Set-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-CertificateThumbprint] <String>] [[-ThumbprintAlgorithm] <String>] [[-StorageAccountName] <String>]
 [[-StorageAccountKey] <String>] [[-StorageAccountEndpoint] <String>] [[-StorageContext] <AzureStorageContext>]
 [-DiagnosticsConfigurationPath] <String> [[-Version] <String>] [[-ExtensionId] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="e31a8-107">SetExtensionUsingDiagnosticsConfiguration</span><span class="sxs-lookup"><span data-stu-id="e31a8-107">SetExtensionUsingDiagnosticsConfiguration</span></span>
```
Set-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>]
 [-DiagnosticsConfiguration] <ExtensionConfigurationInput[]> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e31a8-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e31a8-108">DESCRIPTION</span></span>
<span data-ttu-id="e31a8-109">Polecenie cmdlet **Set-AzureServiceDiagnosticsExtension** umożliwia rozszerzenie diagnostyki platformy Azure na określonych rolach lub we wszystkich rolach we wdrożonej usłudze lub wdrożeniu.</span><span class="sxs-lookup"><span data-stu-id="e31a8-109">The **Set-AzureServiceDiagnosticsExtension** cmdlet enables Azure Diagnostics extension on specified roles or all roles on a deployed service or at deployment.</span></span>

## <span data-ttu-id="e31a8-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e31a8-110">EXAMPLES</span></span>

### <span data-ttu-id="e31a8-111">Przykład 1: Włączanie rozszerzenia Diagnostyka platformy Azure</span><span class="sxs-lookup"><span data-stu-id="e31a8-111">Example 1: Enable Azure Diagnostics extension</span></span>
```
PS C:\> Set-AzureServiceDiagnosticsExtension -ServiceName $Svc -StorageContext $StorageContext -DiagnosticsConfigurationPath $WadConfigXML
```

<span data-ttu-id="e31a8-112">To polecenie włącza rozszerzenie Diagnostyka platformy Azure dla wszystkich ról.</span><span class="sxs-lookup"><span data-stu-id="e31a8-112">This command enables the Azure Diagnostics extension for all roles.</span></span>

### <span data-ttu-id="e31a8-113">Przykład 2: Włączanie rozszerzenia Diagnostyka platformy Azure dla określonej roli</span><span class="sxs-lookup"><span data-stu-id="e31a8-113">Example 2: Enable Azure Diagnostics extension for a specified role</span></span>
```
PS C:\> Set-AzureServiceDiagnosticsExtension -ServiceName $Svc -StorageContext $StorageContext -DiagnosticsConfigurationPath $WadConfigXML -Role "WebRole01"
```

<span data-ttu-id="e31a8-114">To polecenie włącza rozszerzenie Diagnostyka platformy Azure dla określonej roli.</span><span class="sxs-lookup"><span data-stu-id="e31a8-114">This command enables the Azure Diagnostics extension for a specified role.</span></span>

## <span data-ttu-id="e31a8-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e31a8-115">PARAMETERS</span></span>

### <span data-ttu-id="e31a8-116">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="e31a8-116">-CertificateThumbprint</span></span>
<span data-ttu-id="e31a8-117">Określa odcisk palca certyfikatu, który ma zostać użyty do zaszyfrowania konfiguracji prywatnej.</span><span class="sxs-lookup"><span data-stu-id="e31a8-117">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="e31a8-118">Ten certyfikat musi już istnieć w magazynie certyfikatów.</span><span class="sxs-lookup"><span data-stu-id="e31a8-118">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="e31a8-119">Jeśli nie określisz certyfikatu, to polecenie cmdlet utworzy certyfikat.</span><span class="sxs-lookup"><span data-stu-id="e31a8-119">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

```yaml
Type: String
Parameter Sets: SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e31a8-120">-DiagnosticsConfiguration</span><span class="sxs-lookup"><span data-stu-id="e31a8-120">-DiagnosticsConfiguration</span></span>
<span data-ttu-id="e31a8-121">Określa tablicę konfiguracji diagnostyki usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="e31a8-121">Specifies an array of configuration for Azure Diagnostics.</span></span>

```yaml
Type: ExtensionConfigurationInput[]
Parameter Sets: SetExtensionUsingDiagnosticsConfiguration
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e31a8-122">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="e31a8-122">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="e31a8-123">Określa konfigurację diagnostyki Azure Diagnostics.</span><span class="sxs-lookup"><span data-stu-id="e31a8-123">Specifies the configuration for Azure Diagnostics.</span></span>
<span data-ttu-id="e31a8-124">Schemat można pobrać za pomocą następującego polecenia:</span><span class="sxs-lookup"><span data-stu-id="e31a8-124">You can download the schema by using the following command:</span></span> 

`(Get-AzureServiceAvailableExtension -ExtensionName 'PaaSDiagnostics' -ProviderNamespace 'Microsoft.Azure.Diagnostics').PublicConfigurationSchema | Out-File -Encoding utf8 -FilePath 'WadConfig.xsd'`

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e31a8-125">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="e31a8-125">-ExtensionId</span></span>
<span data-ttu-id="e31a8-126">Określa identyfikator rozszerzenia</span><span class="sxs-lookup"><span data-stu-id="e31a8-126">Specifies the extension ID</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e31a8-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="e31a8-127">-InformationAction</span></span>
<span data-ttu-id="e31a8-128">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="e31a8-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e31a8-129">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="e31a8-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e31a8-130">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="e31a8-130">Continue</span></span>
- <span data-ttu-id="e31a8-131">Ignorować</span><span class="sxs-lookup"><span data-stu-id="e31a8-131">Ignore</span></span>
- <span data-ttu-id="e31a8-132">Inquire</span><span class="sxs-lookup"><span data-stu-id="e31a8-132">Inquire</span></span>
- <span data-ttu-id="e31a8-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e31a8-133">SilentlyContinue</span></span>
- <span data-ttu-id="e31a8-134">Przestaw</span><span class="sxs-lookup"><span data-stu-id="e31a8-134">Stop</span></span>
- <span data-ttu-id="e31a8-135">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="e31a8-135">Suspend</span></span>

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

### <span data-ttu-id="e31a8-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e31a8-136">-InformationVariable</span></span>
<span data-ttu-id="e31a8-137">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="e31a8-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e31a8-138">-Profile</span><span class="sxs-lookup"><span data-stu-id="e31a8-138">-Profile</span></span>
<span data-ttu-id="e31a8-139">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e31a8-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e31a8-140">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="e31a8-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e31a8-141">-Rola</span><span class="sxs-lookup"><span data-stu-id="e31a8-141">-Role</span></span>
<span data-ttu-id="e31a8-142">Określa opcjonalną tablicę ról, dla których ma zostać określona konfiguracja diagnostyki platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e31a8-142">Specifies an optional array of roles for which to specify the Azure Diagnostics configuration.</span></span>
<span data-ttu-id="e31a8-143">Jeśli ten parametr nie zostanie określony, konfiguracja diagnostyki zostanie zastosowana jako Konfiguracja domyślna dla wszystkich ról.</span><span class="sxs-lookup"><span data-stu-id="e31a8-143">If you do not specify this parameter, the diagnostics configuration is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e31a8-144">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e31a8-144">-ServiceName</span></span>
<span data-ttu-id="e31a8-145">Określa nazwę usługi na platformie Azure wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="e31a8-145">Specifies the Azure service name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e31a8-146">-Slot</span><span class="sxs-lookup"><span data-stu-id="e31a8-146">-Slot</span></span>
<span data-ttu-id="e31a8-147">Określa środowisko wdrożenia, które ma zostać zmodyfikowane.</span><span class="sxs-lookup"><span data-stu-id="e31a8-147">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="e31a8-148">Dopuszczalne wartości tego parametru to: production lub Staging.</span><span class="sxs-lookup"><span data-stu-id="e31a8-148">The acceptable values for this parameter are: Production or Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e31a8-149">-StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="e31a8-149">-StorageAccountEndpoint</span></span>
<span data-ttu-id="e31a8-150">Określa punkt końcowy konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="e31a8-150">Specifies a storage account endpoint.</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e31a8-151">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="e31a8-151">-StorageAccountKey</span></span>
<span data-ttu-id="e31a8-152">Określa klucz konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="e31a8-152">Specifies a storage account key.</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e31a8-153">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e31a8-153">-StorageAccountName</span></span>
<span data-ttu-id="e31a8-154">Określa nazwę konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="e31a8-154">Specifies a storage account name.</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e31a8-155">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="e31a8-155">-StorageContext</span></span>
<span data-ttu-id="e31a8-156">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="e31a8-156">Specifies an Azure storage context.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e31a8-157">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="e31a8-157">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="e31a8-158">Określa algorytm mieszania odcisku palca, który jest używany z odciskiem palca w celu identyfikacji certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="e31a8-158">Specifies a thumbprint hashing algorithm that is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="e31a8-159">Ten parametr jest opcjonalny, a jego wartością domyślną jest SHA1.</span><span class="sxs-lookup"><span data-stu-id="e31a8-159">This parameter is optional and the default is sha1.</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e31a8-160">-Version</span><span class="sxs-lookup"><span data-stu-id="e31a8-160">-Version</span></span>
<span data-ttu-id="e31a8-161">Określa wersję rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="e31a8-161">Specifies the version of the extension.</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e31a8-162">-X509</span><span class="sxs-lookup"><span data-stu-id="e31a8-162">-X509Certificate</span></span>
<span data-ttu-id="e31a8-163">Określa certyfikat X. 509, który po określeniu jest automatycznie przekazywany do usługi w chmurze i służy do szyfrowania konfiguracji prywatnej rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="e31a8-163">Specifies an X.509 certificate that, when specified, is automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: SetExtension
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e31a8-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e31a8-164">CommonParameters</span></span>
<span data-ttu-id="e31a8-165">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e31a8-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e31a8-166">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e31a8-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e31a8-167">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e31a8-167">INPUTS</span></span>

## <span data-ttu-id="e31a8-168">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e31a8-168">OUTPUTS</span></span>

## <span data-ttu-id="e31a8-169">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e31a8-169">NOTES</span></span>

## <span data-ttu-id="e31a8-170">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e31a8-170">RELATED LINKS</span></span>

[<span data-ttu-id="e31a8-171">Get-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="e31a8-171">Get-AzureServiceDiagnosticsExtension</span></span>](./Get-AzureServiceDiagnosticsExtension.md)

[<span data-ttu-id="e31a8-172">Remove-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="e31a8-172">Remove-AzureServiceDiagnosticsExtension</span></span>](./Remove-AzureServiceDiagnosticsExtension.md)


