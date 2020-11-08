---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2563898E-C4A0-4530-AB46-30A6FC1BE55C
online version: ''
schema: 2.0.0
ms.openlocfilehash: d295e2198cdbd8168d76b1f8e19e75fb4a662116
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054861"
---
# <span data-ttu-id="80594-101">New-AzureServiceRemoteDesktopExtensionConfig</span><span class="sxs-lookup"><span data-stu-id="80594-101">New-AzureServiceRemoteDesktopExtensionConfig</span></span>

## <span data-ttu-id="80594-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="80594-102">SYNOPSIS</span></span>
<span data-ttu-id="80594-103">Generowanie konfiguracji rozszerzenia pulpitu zdalnego dla wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="80594-103">Generates a remote desktop extension configuration for a deployment.</span></span>

## <span data-ttu-id="80594-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="80594-104">SYNTAX</span></span>

### <span data-ttu-id="80594-105">NewExtension (domyślny)</span><span class="sxs-lookup"><span data-stu-id="80594-105">NewExtension (Default)</span></span>
```
New-AzureServiceRemoteDesktopExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [-Credential] <PSCredential> [[-Expiration] <DateTime>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="80594-106">NewExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="80594-106">NewExtensionUsingThumbprint</span></span>
```
New-AzureServiceRemoteDesktopExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [-Credential] <PSCredential> [[-Expiration] <DateTime>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="80594-107">Opis</span><span class="sxs-lookup"><span data-stu-id="80594-107">DESCRIPTION</span></span>
<span data-ttu-id="80594-108">Polecenie cmdlet **New-AzureServiceRemoteDesktopExtensionConfig** generuje konfigurację rozszerzenia pulpitu zdalnego dla wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="80594-108">The **New-AzureServiceRemoteDesktopExtensionConfig** cmdlet generates a configuration for a remote desktop extension for a deployment.</span></span>

## <span data-ttu-id="80594-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="80594-109">EXAMPLES</span></span>

### <span data-ttu-id="80594-110">Przykład 1. generowanie konfiguracji rozszerzenia pulpitu zdalnego</span><span class="sxs-lookup"><span data-stu-id="80594-110">Example 1: Generate a remote desktop extension configuration</span></span>
```
PS C:\> $rdpConfig = New-AzureServiceRemoteDesktopExtensionConfig -Credential $cred
```

<span data-ttu-id="80594-111">To polecenie generuje konfigurację rozszerzenia pulpitu zdalnego dla określonych poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="80594-111">This command generates a remote desktop extension configuration for the specified credentials.</span></span>

### <span data-ttu-id="80594-112">Przykład 2: generowanie konfiguracji rozszerzenia pulpitu zdalnego dla określonej roli</span><span class="sxs-lookup"><span data-stu-id="80594-112">Example 2: Generate a remote desktop extension configuration for a specified role</span></span>
```
PS C:\> $rdpConfig = New-AzureServiceRemoteDesktopExtensionConfig -Credential $cred -Role "WebRole01"
```

<span data-ttu-id="80594-113">To polecenie generuje konfigurację rozszerzenia pulpitu zdalnego dla określonych poświadczeń i roli WebRole01.</span><span class="sxs-lookup"><span data-stu-id="80594-113">This command generates a remote desktop extension configuration for the specified credentials and the WebRole01 role.</span></span>

## <span data-ttu-id="80594-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="80594-114">PARAMETERS</span></span>

### <span data-ttu-id="80594-115">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="80594-115">-CertificateThumbprint</span></span>
<span data-ttu-id="80594-116">Określa odcisk palca certyfikatu, który ma zostać użyty do zaszyfrowania konfiguracji prywatnej.</span><span class="sxs-lookup"><span data-stu-id="80594-116">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="80594-117">Ten certyfikat musi już istnieć w magazynie certyfikatów.</span><span class="sxs-lookup"><span data-stu-id="80594-117">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="80594-118">Jeśli nie określisz certyfikatu, to polecenie cmdlet utworzy certyfikat.</span><span class="sxs-lookup"><span data-stu-id="80594-118">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

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

### <span data-ttu-id="80594-119">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="80594-119">-Credential</span></span>
<span data-ttu-id="80594-120">Określa poświadczenia, które należy włączyć dla pulpitu zdalnego.</span><span class="sxs-lookup"><span data-stu-id="80594-120">Specifies the credentials to enable for remote desktop.</span></span>
<span data-ttu-id="80594-121">Poświadczenia zawierają nazwę użytkownika i hasło.</span><span class="sxs-lookup"><span data-stu-id="80594-121">Credentials include a user name and password.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80594-122">-Data wygaśnięcia</span><span class="sxs-lookup"><span data-stu-id="80594-122">-Expiration</span></span>
<span data-ttu-id="80594-123">Określa obiekt **DateTime** , który pozwala użytkownikowi określić, kiedy wygasa konto użytkownika.</span><span class="sxs-lookup"><span data-stu-id="80594-123">Specifies a **DateTime** object that allows the user to specify when the user account expires.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80594-124">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="80594-124">-ExtensionId</span></span>
<span data-ttu-id="80594-125">Określa identyfikator rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="80594-125">Specifies the extension ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80594-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="80594-126">-InformationAction</span></span>
<span data-ttu-id="80594-127">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="80594-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="80594-128">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="80594-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="80594-129">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="80594-129">Continue</span></span>
- <span data-ttu-id="80594-130">Ignorować</span><span class="sxs-lookup"><span data-stu-id="80594-130">Ignore</span></span>
- <span data-ttu-id="80594-131">Inquire</span><span class="sxs-lookup"><span data-stu-id="80594-131">Inquire</span></span>
- <span data-ttu-id="80594-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="80594-132">SilentlyContinue</span></span>
- <span data-ttu-id="80594-133">Przestaw</span><span class="sxs-lookup"><span data-stu-id="80594-133">Stop</span></span>
- <span data-ttu-id="80594-134">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="80594-134">Suspend</span></span>

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

### <span data-ttu-id="80594-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="80594-135">-InformationVariable</span></span>
<span data-ttu-id="80594-136">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="80594-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="80594-137">-Profile</span><span class="sxs-lookup"><span data-stu-id="80594-137">-Profile</span></span>
<span data-ttu-id="80594-138">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80594-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="80594-139">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="80594-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="80594-140">-Rola</span><span class="sxs-lookup"><span data-stu-id="80594-140">-Role</span></span>
<span data-ttu-id="80594-141">Określa opcjonalną tablicę ról, dla których należy określić konfigurację pulpitu zdalnego.</span><span class="sxs-lookup"><span data-stu-id="80594-141">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="80594-142">Jeśli ten parametr nie jest określony, konfiguracja pulpitu zdalnego jest stosowana jako Konfiguracja domyślna dla wszystkich ról.</span><span class="sxs-lookup"><span data-stu-id="80594-142">If this parameter is not specified the remote desktop configuration is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="80594-143">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="80594-143">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="80594-144">Określa algorytm mieszania odcisku palca, który jest używany w odniesieniu do odcisku palca w celu identyfikacji certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="80594-144">Specifies a thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="80594-145">Ten parametr jest opcjonalny, a jego wartością domyślną jest SHA1.</span><span class="sxs-lookup"><span data-stu-id="80594-145">This parameter is optional and the default is sha1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80594-146">-Version</span><span class="sxs-lookup"><span data-stu-id="80594-146">-Version</span></span>
<span data-ttu-id="80594-147">Określa wersję rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="80594-147">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80594-148">-X509</span><span class="sxs-lookup"><span data-stu-id="80594-148">-X509Certificate</span></span>
<span data-ttu-id="80594-149">Określa certyfikat x509, który po określeniu zostanie automatycznie przekazany do usługi w chmurze i jest wykorzystywany do szyfrowania konfiguracji prywatnej rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="80594-149">Specifies an x509 certificate that when specified will be automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

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

### <span data-ttu-id="80594-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80594-150">CommonParameters</span></span>
<span data-ttu-id="80594-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80594-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80594-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80594-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80594-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="80594-153">INPUTS</span></span>

## <span data-ttu-id="80594-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="80594-154">OUTPUTS</span></span>

## <span data-ttu-id="80594-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="80594-155">NOTES</span></span>

## <span data-ttu-id="80594-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="80594-156">RELATED LINKS</span></span>

[<span data-ttu-id="80594-157">Set-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="80594-157">Set-AzureServiceRemoteDesktopExtension</span></span>](./Set-AzureServiceRemoteDesktopExtension.md)


