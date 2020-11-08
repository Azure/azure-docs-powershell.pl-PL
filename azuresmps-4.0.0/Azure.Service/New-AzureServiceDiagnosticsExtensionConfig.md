---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1F76C63E-5289-4F88-9522-3FF4EF732908
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8a232ec03da38ea3d527dcd9aa214dbf681bcc6a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054864"
---
# <span data-ttu-id="49542-101">New-AzureServiceDiagnosticsExtensionConfig</span><span class="sxs-lookup"><span data-stu-id="49542-101">New-AzureServiceDiagnosticsExtensionConfig</span></span>

## <span data-ttu-id="49542-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="49542-102">SYNOPSIS</span></span>
<span data-ttu-id="49542-103">Generuje konfigurację rozszerzenia diagnostycznego dla określonych ról lub wszystkich ról.</span><span class="sxs-lookup"><span data-stu-id="49542-103">Generates a configuration for a diagnostics extension for specified role(s) or all roles.</span></span>

## <span data-ttu-id="49542-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="49542-104">SYNTAX</span></span>

### <span data-ttu-id="49542-105">NewExtension (domyślny)</span><span class="sxs-lookup"><span data-stu-id="49542-105">NewExtension (Default)</span></span>
```
New-AzureServiceDiagnosticsExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [[-StorageAccountName] <String>] [[-StorageAccountKey] <String>]
 [[-StorageAccountEndpoint] <String>] [[-StorageContext] <AzureStorageContext>]
 [-DiagnosticsConfigurationPath] <String> [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="49542-106">NewExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="49542-106">NewExtensionUsingThumbprint</span></span>
```
New-AzureServiceDiagnosticsExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [[-StorageAccountKey] <String>] [[-StorageAccountEndpoint] <String>]
 [[-StorageContext] <AzureStorageContext>] [-DiagnosticsConfigurationPath] <String> [[-ExtensionId] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="49542-107">SetExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="49542-107">SetExtensionUsingThumbprint</span></span>
```
New-AzureServiceDiagnosticsExtensionConfig [[-StorageAccountName] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="49542-108">Opis</span><span class="sxs-lookup"><span data-stu-id="49542-108">DESCRIPTION</span></span>
<span data-ttu-id="49542-109">Polecenie cmdlet **New-AzureServiceDiagnosticsExtensionConfig** generuje konfigurację rozszerzenia diagnostycznego dla określonych ról lub wszystkich ról.</span><span class="sxs-lookup"><span data-stu-id="49542-109">The **New-AzureServiceDiagnosticsExtensionConfig** cmdlet generates a configuration for a diagnostics extension for specified roles or all roles.</span></span>

## <span data-ttu-id="49542-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="49542-110">EXAMPLES</span></span>

### <span data-ttu-id="49542-111">Przykład 1. Tworzenie rozszerzenia Diagnostyka platformy Azure dla wszystkich ról w usłudze chmury</span><span class="sxs-lookup"><span data-stu-id="49542-111">Example 1: Create the Azure Diagnostics extension for all roles in the cloud service</span></span>
```
PS C:\> $WadConfig = New-AzureServiceDiagnosticExtensionConfig -StorageContext $StorageContext -DiagnosticsConfigurationPath $WadConfigXML
```

<span data-ttu-id="49542-112">To polecenie tworzy rozszerzenie Diagnostyka platformy Azure dla wszystkich ról w usłudze chmury.</span><span class="sxs-lookup"><span data-stu-id="49542-112">This command creates the Azure Diagnostics extension for all of the roles in the cloud service.</span></span>

### <span data-ttu-id="49542-113">Przykład 2: Tworzenie rozszerzenia Diagnostyka platformy Azure dla roli</span><span class="sxs-lookup"><span data-stu-id="49542-113">Example 2: Create the Azure Diagnostics extension for a role</span></span>
```
PS C:\> $WadConfig = New-AzureServiceDiagnosticExtensionConfig -StorageContext $StorageContext -DiagnosticsConfigurationPath $WadConfigXML -Role "WebRole1"
```

<span data-ttu-id="49542-114">To polecenie tworzy rozszerzenie Diagnostyka platformy Azure dla roli WebRole01 w usłudze chmury.</span><span class="sxs-lookup"><span data-stu-id="49542-114">This command creates the Azure Diagnostics extension for the role WebRole01 in the cloud service.</span></span>

## <span data-ttu-id="49542-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="49542-115">PARAMETERS</span></span>

### <span data-ttu-id="49542-116">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="49542-116">-CertificateThumbprint</span></span>
<span data-ttu-id="49542-117">Określa odcisk palca certyfikatu, który ma zostać użyty do zaszyfrowania konfiguracji prywatnej.</span><span class="sxs-lookup"><span data-stu-id="49542-117">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="49542-118">Ten certyfikat musi już istnieć w magazynie certyfikatów.</span><span class="sxs-lookup"><span data-stu-id="49542-118">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="49542-119">Jeśli nie określisz certyfikatu, to polecenie cmdlet utworzy certyfikat.</span><span class="sxs-lookup"><span data-stu-id="49542-119">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

```yaml
Type: String
Parameter Sets: NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49542-120">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="49542-120">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="49542-121">Określa ścieżkę konfiguracji diagnostyki.</span><span class="sxs-lookup"><span data-stu-id="49542-121">Specifies the diagnostics configuration path.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49542-122">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="49542-122">-ExtensionId</span></span>
<span data-ttu-id="49542-123">Określa identyfikator rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="49542-123">Specifies the extension ID.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49542-124">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="49542-124">-InformationAction</span></span>
<span data-ttu-id="49542-125">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="49542-125">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="49542-126">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="49542-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="49542-127">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="49542-127">Continue</span></span>
- <span data-ttu-id="49542-128">Ignorować</span><span class="sxs-lookup"><span data-stu-id="49542-128">Ignore</span></span>
- <span data-ttu-id="49542-129">Inquire</span><span class="sxs-lookup"><span data-stu-id="49542-129">Inquire</span></span>
- <span data-ttu-id="49542-130">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="49542-130">SilentlyContinue</span></span>
- <span data-ttu-id="49542-131">Przestaw</span><span class="sxs-lookup"><span data-stu-id="49542-131">Stop</span></span>
- <span data-ttu-id="49542-132">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="49542-132">Suspend</span></span>

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

### <span data-ttu-id="49542-133">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="49542-133">-InformationVariable</span></span>
<span data-ttu-id="49542-134">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="49542-134">Specifies an information variable.</span></span>

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

### <span data-ttu-id="49542-135">-Profile</span><span class="sxs-lookup"><span data-stu-id="49542-135">-Profile</span></span>
<span data-ttu-id="49542-136">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49542-136">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="49542-137">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="49542-137">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="49542-138">-Rola</span><span class="sxs-lookup"><span data-stu-id="49542-138">-Role</span></span>
<span data-ttu-id="49542-139">Określa opcjonalną tablicę ról określającą konfigurację diagnostyki.</span><span class="sxs-lookup"><span data-stu-id="49542-139">Specifies an optional array of roles to specify the diagnostics configuration for.</span></span>
<span data-ttu-id="49542-140">Jeśli nie określono, konfiguracja diagnostyki jest stosowana jako domyślna konfiguracja wszystkich ról.</span><span class="sxs-lookup"><span data-stu-id="49542-140">If not specified the diagnostics configuration is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49542-141">-StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="49542-141">-StorageAccountEndpoint</span></span>
<span data-ttu-id="49542-142">Określa punkt końcowy konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="49542-142">Specifies the storage account endpoint.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49542-143">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="49542-143">-StorageAccountKey</span></span>
<span data-ttu-id="49542-144">Określa klucz konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="49542-144">Specifies the storage account key.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49542-145">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="49542-145">-StorageAccountName</span></span>
<span data-ttu-id="49542-146">Określa nazwę konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="49542-146">Specifies the storage account name.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49542-147">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="49542-147">-StorageContext</span></span>
<span data-ttu-id="49542-148">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="49542-148">Specifies an Azure storage context.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49542-149">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="49542-149">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="49542-150">Określa algorytm mieszania odcisku palca, który jest używany w odniesieniu do odcisku palca w celu identyfikacji certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="49542-150">Specifies a thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="49542-151">Ten parametr jest opcjonalny, a jego wartością domyślną jest SHA1.</span><span class="sxs-lookup"><span data-stu-id="49542-151">This parameter is optional and the default is sha1.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49542-152">-X509</span><span class="sxs-lookup"><span data-stu-id="49542-152">-X509Certificate</span></span>
<span data-ttu-id="49542-153">Określa certyfikat X. 509, który jest automatycznie przekazywany do usługi w chmurze i służy do szyfrowania konfiguracji prywatnej rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="49542-153">Specifies an X.509 certificate that is automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: NewExtension
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49542-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49542-154">CommonParameters</span></span>
<span data-ttu-id="49542-155">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49542-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49542-156">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49542-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49542-157">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="49542-157">INPUTS</span></span>

## <span data-ttu-id="49542-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="49542-158">OUTPUTS</span></span>

## <span data-ttu-id="49542-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="49542-159">NOTES</span></span>

## <span data-ttu-id="49542-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="49542-160">RELATED LINKS</span></span>

[<span data-ttu-id="49542-161">Get-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="49542-161">Get-AzureServiceDiagnosticsExtension</span></span>](./Get-AzureServiceDiagnosticsExtension.md)

[<span data-ttu-id="49542-162">Set-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="49542-162">Set-AzureServiceDiagnosticsExtension</span></span>](./Set-AzureServiceDiagnosticsExtension.md)


