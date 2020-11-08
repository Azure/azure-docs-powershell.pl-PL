---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E27283AF-4057-48D9-9F08-7D36290DD907
online version: ''
schema: 2.0.0
ms.openlocfilehash: dfe55fb2ced2275eae06e96480249acd99d3ad6c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054862"
---
# <span data-ttu-id="e9396-101">New-AzureServiceExtensionConfig</span><span class="sxs-lookup"><span data-stu-id="e9396-101">New-AzureServiceExtensionConfig</span></span>

## <span data-ttu-id="e9396-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e9396-102">SYNOPSIS</span></span>
<span data-ttu-id="e9396-103">Umożliwia utworzenie konfiguracji rozszerzenia usługi w chmurze dla wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="e9396-103">Creates a cloud service extension configuration for a deployment.</span></span>

## <span data-ttu-id="e9396-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e9396-104">SYNTAX</span></span>

### <span data-ttu-id="e9396-105">NewExtension (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e9396-105">NewExtension (Default)</span></span>
```
New-AzureServiceExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [-ExtensionName] <String> [-ProviderNamespace] <String>
 [-PublicConfiguration] <String> [-PrivateConfiguration] <String> [-Version] <String> [[-ExtensionId] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="e9396-106">NewExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="e9396-106">NewExtensionUsingThumbprint</span></span>
```
New-AzureServiceExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [-ExtensionName] <String> [-ProviderNamespace] <String>
 [-PublicConfiguration] <String> [-PrivateConfiguration] <String> [-Version] <String> [[-ExtensionId] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="e9396-107">UpdateExtensionStatusParameterSetName</span><span class="sxs-lookup"><span data-stu-id="e9396-107">UpdateExtensionStatusParameterSetName</span></span>
```
New-AzureServiceExtensionConfig [[-Role] <String[]>] [-ExtensionId] <String> [-ExtensionState] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="e9396-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e9396-108">DESCRIPTION</span></span>
<span data-ttu-id="e9396-109">Polecenie cmdlet **New-AzureServiceExtensionConfig** umożliwia utworzenie konfiguracji rozszerzenia usługi w chmurze dla wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="e9396-109">The **New-AzureServiceExtensionConfig** cmdlet creates a cloud service extension configuration for a deployment.</span></span>

## <span data-ttu-id="e9396-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e9396-110">EXAMPLES</span></span>

### <span data-ttu-id="e9396-111">Przykład 1. Tworzenie konfiguracji rozszerzenia</span><span class="sxs-lookup"><span data-stu-id="e9396-111">Example 1: Create an extension configuration</span></span>
```
PS C:\> New-AzureServiceExtensionConfig -ExtensionName 'RDP' -Version '1.0' -ProviderNamespace Microsoft.Windows.Azure.Extensions -PublicConfiguration $p1 -PrivateConfiguration $p2;
```

<span data-ttu-id="e9396-112">To polecenie określa konfigurację rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="e9396-112">This command specifies an extension configuration.</span></span>

### <span data-ttu-id="e9396-113">Przykład 2: Tworzenie konfiguracji rozszerzenia dla roli</span><span class="sxs-lookup"><span data-stu-id="e9396-113">Example 2: Create an extension configuration for a role</span></span>
```
PS C:\> New-AzureServiceExtensionConfig -Role WebRole1 -ExtensionName 'RDP' -ProviderNamespace Microsoft.Windows.Azure.Extensions -PublicConfiguration $p1 -PrivateConfiguration $p2;
```

<span data-ttu-id="e9396-114">To polecenie określa konfigurację rozszerzenia dla roli WebRole1.</span><span class="sxs-lookup"><span data-stu-id="e9396-114">This command specifies an extension configuration for the role WebRole1.</span></span>

## <span data-ttu-id="e9396-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e9396-115">PARAMETERS</span></span>

### <span data-ttu-id="e9396-116">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="e9396-116">-CertificateThumbprint</span></span>
<span data-ttu-id="e9396-117">Określa odcisk palca certyfikatu, który ma zostać użyty do zaszyfrowania konfiguracji prywatnej.</span><span class="sxs-lookup"><span data-stu-id="e9396-117">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="e9396-118">Ten certyfikat musi już istnieć w magazynie certyfikatów.</span><span class="sxs-lookup"><span data-stu-id="e9396-118">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="e9396-119">Jeśli nie określisz certyfikatu, to polecenie cmdlet utworzy certyfikat.</span><span class="sxs-lookup"><span data-stu-id="e9396-119">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

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

### <span data-ttu-id="e9396-120">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="e9396-120">-ExtensionId</span></span>
<span data-ttu-id="e9396-121">Określa nazwę rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="e9396-121">Specifies the name of the extension.</span></span>

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

```yaml
Type: String
Parameter Sets: UpdateExtensionStatusParameterSetName
Aliases: 

Required: True
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9396-122">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="e9396-122">-ExtensionName</span></span>
<span data-ttu-id="e9396-123">Określa nazwę rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="e9396-123">Specifies the name of the extension.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9396-124">-ExtensionState</span><span class="sxs-lookup"><span data-stu-id="e9396-124">-ExtensionState</span></span>
<span data-ttu-id="e9396-125">Określa stan rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="e9396-125">Specifies the state of the extension.</span></span>
<span data-ttu-id="e9396-126">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="e9396-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e9396-127">Włączony</span><span class="sxs-lookup"><span data-stu-id="e9396-127">Enable</span></span> 
- <span data-ttu-id="e9396-128">Wyłącza</span><span class="sxs-lookup"><span data-stu-id="e9396-128">Disable</span></span> 
- <span data-ttu-id="e9396-129">Odinstaluj</span><span class="sxs-lookup"><span data-stu-id="e9396-129">Uninstall</span></span>

```yaml
Type: String
Parameter Sets: UpdateExtensionStatusParameterSetName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9396-130">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="e9396-130">-InformationAction</span></span>
<span data-ttu-id="e9396-131">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="e9396-131">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e9396-132">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="e9396-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e9396-133">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="e9396-133">Continue</span></span>
- <span data-ttu-id="e9396-134">Ignorować</span><span class="sxs-lookup"><span data-stu-id="e9396-134">Ignore</span></span>
- <span data-ttu-id="e9396-135">Inquire</span><span class="sxs-lookup"><span data-stu-id="e9396-135">Inquire</span></span>
- <span data-ttu-id="e9396-136">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e9396-136">SilentlyContinue</span></span>
- <span data-ttu-id="e9396-137">Przestaw</span><span class="sxs-lookup"><span data-stu-id="e9396-137">Stop</span></span>
- <span data-ttu-id="e9396-138">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="e9396-138">Suspend</span></span>

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

### <span data-ttu-id="e9396-139">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e9396-139">-InformationVariable</span></span>
<span data-ttu-id="e9396-140">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="e9396-140">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e9396-141">-PrivateConfiguration</span><span class="sxs-lookup"><span data-stu-id="e9396-141">-PrivateConfiguration</span></span>
<span data-ttu-id="e9396-142">Określa tekst konfiguracji prywatnej.</span><span class="sxs-lookup"><span data-stu-id="e9396-142">Specifies the private configuration text.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9396-143">-Profile</span><span class="sxs-lookup"><span data-stu-id="e9396-143">-Profile</span></span>
<span data-ttu-id="e9396-144">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9396-144">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e9396-145">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="e9396-145">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e9396-146">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="e9396-146">-ProviderNamespace</span></span>
<span data-ttu-id="e9396-147">Określa obszar nazw dostawcy rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="e9396-147">Specifies the Extension's Provider Namespace.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9396-148">-PublicConfiguration</span><span class="sxs-lookup"><span data-stu-id="e9396-148">-PublicConfiguration</span></span>
<span data-ttu-id="e9396-149">Określa tekst konfiguracji publicznej.</span><span class="sxs-lookup"><span data-stu-id="e9396-149">Specifies the public configuration text.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9396-150">-Rola</span><span class="sxs-lookup"><span data-stu-id="e9396-150">-Role</span></span>
<span data-ttu-id="e9396-151">Określa opcjonalną tablicę ról określającą konfigurację pulpitu zdalnego.</span><span class="sxs-lookup"><span data-stu-id="e9396-151">Specifies an optional array of roles to specify the remote desktop configuration for.</span></span>
<span data-ttu-id="e9396-152">Jeśli nie określono, konfiguracja pulpitu zdalnego jest stosowana jako Konfiguracja domyślna dla wszystkich ról.</span><span class="sxs-lookup"><span data-stu-id="e9396-152">If not specified the remote desktop configuration is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9396-153">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="e9396-153">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="e9396-154">Określa algorytm mieszania odcisku palca, który jest używany w odniesieniu do odcisku palca w celu identyfikacji certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="e9396-154">Specifies a thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="e9396-155">Ten parametr jest opcjonalny, a jego wartością domyślną jest SHA1.</span><span class="sxs-lookup"><span data-stu-id="e9396-155">This parameter is optional and the default is sha1.</span></span>

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

### <span data-ttu-id="e9396-156">-Version</span><span class="sxs-lookup"><span data-stu-id="e9396-156">-Version</span></span>
<span data-ttu-id="e9396-157">Określa wersję rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="e9396-157">Specifies the extension version.</span></span>

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

### <span data-ttu-id="e9396-158">-X509</span><span class="sxs-lookup"><span data-stu-id="e9396-158">-X509Certificate</span></span>
<span data-ttu-id="e9396-159">Określa certyfikat x509, który po określeniu zostanie automatycznie przekazany do usługi w chmurze i jest wykorzystywany do szyfrowania konfiguracji prywatnej rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="e9396-159">Specifies an x509 certificate that when specified will be automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

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

### <span data-ttu-id="e9396-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9396-160">CommonParameters</span></span>
<span data-ttu-id="e9396-161">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9396-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9396-162">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9396-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9396-163">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e9396-163">INPUTS</span></span>

## <span data-ttu-id="e9396-164">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e9396-164">OUTPUTS</span></span>

## <span data-ttu-id="e9396-165">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e9396-165">NOTES</span></span>

## <span data-ttu-id="e9396-166">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e9396-166">RELATED LINKS</span></span>

[<span data-ttu-id="e9396-167">Get-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="e9396-167">Get-AzureServiceExtension</span></span>](./Get-AzureServiceExtension.md)

[<span data-ttu-id="e9396-168">Set-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="e9396-168">Set-AzureServiceExtension</span></span>](./Set-AzureServiceExtension.md)


