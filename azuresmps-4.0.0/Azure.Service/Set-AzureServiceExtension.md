---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D37920D3-AF6C-4CFC-B9A3-8ED931AEC0DC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 318683c26d05c624549363ff1afe4a2b963c1fe6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054413"
---
# <span data-ttu-id="824a4-101">Set-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="824a4-101">Set-AzureServiceExtension</span></span>

## <span data-ttu-id="824a4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="824a4-102">SYNOPSIS</span></span>
<span data-ttu-id="824a4-103">Dodaje rozszerzenie usługi chmury do wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="824a4-103">Adds a cloud service extension to a deployment.</span></span>

## <span data-ttu-id="824a4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="824a4-104">SYNTAX</span></span>

### <span data-ttu-id="824a4-105">Setextension (domyślne)</span><span class="sxs-lookup"><span data-stu-id="824a4-105">SetExtension (Default)</span></span>
```
Set-AzureServiceExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [-ExtensionName] <String>
 [-ProviderNamespace] <String> [-PublicConfiguration] <String> [-PrivateConfiguration] <String>
 [-Version] <String> [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="824a4-106">SetExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="824a4-106">SetExtensionUsingThumbprint</span></span>
```
Set-AzureServiceExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-CertificateThumbprint] <String> [[-ThumbprintAlgorithm] <String>] [-ExtensionName] <String>
 [-ProviderNamespace] <String> [-PublicConfiguration] <String> [-PrivateConfiguration] <String>
 [-Version] <String> [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="824a4-107">Opis</span><span class="sxs-lookup"><span data-stu-id="824a4-107">DESCRIPTION</span></span>
<span data-ttu-id="824a4-108">Polecenie cmdlet **Set-AzureServiceExtension** umożliwia dodanie rozszerzenia usługi w chmurze do wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="824a4-108">The **Set-AzureServiceExtension** cmdlet adds a cloud service extension to a deployment.</span></span>

## <span data-ttu-id="824a4-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="824a4-109">EXAMPLES</span></span>

### <span data-ttu-id="824a4-110">Przykład 1: Dodawanie usługi w chmurze do wdrożenia</span><span class="sxs-lookup"><span data-stu-id="824a4-110">Example 1: Add a cloud service to a deployment</span></span>
```
PS C:\> Set-AzureServiceExtension -Service $Svc -Slot "Production" -ExtensionName "RDP" -Version "1.0" -ProviderNamespace "Microsoft.Windows.Azure.Extensions" -PublicConfiguration $P1 -PrivateConfiguration $P2;
```

<span data-ttu-id="824a4-111">To polecenie umożliwia dodanie usługi w chmurze do wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="824a4-111">This command adds a cloud service to a deployment.</span></span>

### <span data-ttu-id="824a4-112">Przykład 2: Dodawanie usługi w chmurze do wdrożenia dla określonej roli</span><span class="sxs-lookup"><span data-stu-id="824a4-112">Example 2: Add a cloud service to a deployment for a specified role</span></span>
```
PS C:\> Set-AzureServiceExtension -Service $Svc -Slot "Production" -Role "WebRole1" -ExtensionName "RDP" -ProviderNamespace "Microsoft.Windows.Azure.Extensions" -PublicConfiguration $P1 -PrivateConfiguration $P2;
```

<span data-ttu-id="824a4-113">To polecenie umożliwia dodanie do wdrożenia usługi w chmurze dla określonej roli.</span><span class="sxs-lookup"><span data-stu-id="824a4-113">This command adds a cloud service to a deployment for a specified role.</span></span>

## <span data-ttu-id="824a4-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="824a4-114">PARAMETERS</span></span>

### <span data-ttu-id="824a4-115">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="824a4-115">-CertificateThumbprint</span></span>
<span data-ttu-id="824a4-116">Określa odcisk palca certyfikatu, który ma zostać użyty do zaszyfrowania konfiguracji prywatnej.</span><span class="sxs-lookup"><span data-stu-id="824a4-116">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="824a4-117">Ten certyfikat musi już istnieć w magazynie certyfikatów.</span><span class="sxs-lookup"><span data-stu-id="824a4-117">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="824a4-118">Jeśli nie określisz certyfikatu, to polecenie cmdlet utworzy certyfikat.</span><span class="sxs-lookup"><span data-stu-id="824a4-118">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

```yaml
Type: String
Parameter Sets: SetExtensionUsingThumbprint
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="824a4-119">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="824a4-119">-ExtensionId</span></span>
<span data-ttu-id="824a4-120">Określa identyfikator rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="824a4-120">Specifies the extension ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="824a4-121">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="824a4-121">-ExtensionName</span></span>
<span data-ttu-id="824a4-122">Określa nazwę rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="824a4-122">Specifies the extension name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="824a4-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="824a4-123">-InformationAction</span></span>
<span data-ttu-id="824a4-124">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="824a4-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="824a4-125">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="824a4-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="824a4-126">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="824a4-126">Continue</span></span>
- <span data-ttu-id="824a4-127">Ignorować</span><span class="sxs-lookup"><span data-stu-id="824a4-127">Ignore</span></span>
- <span data-ttu-id="824a4-128">Inquire</span><span class="sxs-lookup"><span data-stu-id="824a4-128">Inquire</span></span>
- <span data-ttu-id="824a4-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="824a4-129">SilentlyContinue</span></span>
- <span data-ttu-id="824a4-130">Przestaw</span><span class="sxs-lookup"><span data-stu-id="824a4-130">Stop</span></span>
- <span data-ttu-id="824a4-131">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="824a4-131">Suspend</span></span>

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

### <span data-ttu-id="824a4-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="824a4-132">-InformationVariable</span></span>
<span data-ttu-id="824a4-133">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="824a4-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="824a4-134">-PrivateConfiguration</span><span class="sxs-lookup"><span data-stu-id="824a4-134">-PrivateConfiguration</span></span>
<span data-ttu-id="824a4-135">Określa tekst konfiguracji prywatnej.</span><span class="sxs-lookup"><span data-stu-id="824a4-135">Specifies the private configuration text.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="824a4-136">-Profile</span><span class="sxs-lookup"><span data-stu-id="824a4-136">-Profile</span></span>
<span data-ttu-id="824a4-137">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="824a4-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="824a4-138">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="824a4-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="824a4-139">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="824a4-139">-ProviderNamespace</span></span>
<span data-ttu-id="824a4-140">Określa obszar nazw dostawcy rozszerzeń.</span><span class="sxs-lookup"><span data-stu-id="824a4-140">Specifies the extension provider namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="824a4-141">-PublicConfiguration</span><span class="sxs-lookup"><span data-stu-id="824a4-141">-PublicConfiguration</span></span>
<span data-ttu-id="824a4-142">Określa tekst konfiguracji publicznej.</span><span class="sxs-lookup"><span data-stu-id="824a4-142">Specifies the public configuration text.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="824a4-143">-Rola</span><span class="sxs-lookup"><span data-stu-id="824a4-143">-Role</span></span>
<span data-ttu-id="824a4-144">Określa opcjonalną tablicę ról, dla których należy określić konfigurację pulpitu zdalnego.</span><span class="sxs-lookup"><span data-stu-id="824a4-144">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="824a4-145">Jeśli ten parametr nie jest określony, konfiguracja pulpitu zdalnego jest stosowana jako Konfiguracja domyślna dla wszystkich ról.</span><span class="sxs-lookup"><span data-stu-id="824a4-145">If this parameter is not specified the remote desktop configuration is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="824a4-146">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="824a4-146">-ServiceName</span></span>
<span data-ttu-id="824a4-147">Określa nazwę usługi na platformie Azure wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="824a4-147">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="824a4-148">-Slot</span><span class="sxs-lookup"><span data-stu-id="824a4-148">-Slot</span></span>
<span data-ttu-id="824a4-149">Określa środowisko wdrożenia, które ma zostać zmodyfikowane.</span><span class="sxs-lookup"><span data-stu-id="824a4-149">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="824a4-150">Prawidłowe wartości to: production lub Staging.</span><span class="sxs-lookup"><span data-stu-id="824a4-150">Valid values are: Production or Staging.</span></span>

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

### <span data-ttu-id="824a4-151">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="824a4-151">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="824a4-152">Określa algorytm mieszania odcisku palca, który jest używany w odniesieniu do odcisku palca w celu zidentyfikowania certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="824a4-152">Specifies the thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="824a4-153">Ten parametr jest opcjonalny, a jego wartością domyślną jest SHA1.</span><span class="sxs-lookup"><span data-stu-id="824a4-153">This parameter is optional and the default is sha1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="824a4-154">-Version</span><span class="sxs-lookup"><span data-stu-id="824a4-154">-Version</span></span>
<span data-ttu-id="824a4-155">Określa wersję rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="824a4-155">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="824a4-156">-X509</span><span class="sxs-lookup"><span data-stu-id="824a4-156">-X509Certificate</span></span>
<span data-ttu-id="824a4-157">Określa certyfikat X. 509, który jest automatycznie przekazywany do usługi w chmurze i służy do szyfrowania konfiguracji prywatnej rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="824a4-157">Specifies an X.509 certificate that is automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

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

### <span data-ttu-id="824a4-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="824a4-158">CommonParameters</span></span>
<span data-ttu-id="824a4-159">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="824a4-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="824a4-160">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="824a4-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="824a4-161">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="824a4-161">INPUTS</span></span>

## <span data-ttu-id="824a4-162">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="824a4-162">OUTPUTS</span></span>

## <span data-ttu-id="824a4-163">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="824a4-163">NOTES</span></span>

## <span data-ttu-id="824a4-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="824a4-164">RELATED LINKS</span></span>

[<span data-ttu-id="824a4-165">Get-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="824a4-165">Get-AzureServiceExtension</span></span>](./Get-AzureServiceExtension.md)

[<span data-ttu-id="824a4-166">Remove-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="824a4-166">Remove-AzureServiceExtension</span></span>](./Remove-AzureServiceExtension.md)


