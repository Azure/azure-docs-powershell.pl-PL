---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5C8B1482-80B0-4060-A35D-E9D394156886
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9a6303e685ea02408772a237c6b5f154764107e4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054779"
---
# <span data-ttu-id="b4d4a-101">Set-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="b4d4a-101">Set-AzureServiceRemoteDesktopExtension</span></span>

## <span data-ttu-id="b4d4a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b4d4a-102">SYNOPSIS</span></span>
<span data-ttu-id="b4d4a-103">Umożliwia rozszerzenie pulpitu zdalnego na określonych rolach lub wszystkich rolach we wdrożonej usłudze lub wdrożeniu.</span><span class="sxs-lookup"><span data-stu-id="b4d4a-103">Enables remote desktop extension on specified role(s) or all roles on a deployed service or at deployment.</span></span>

## <span data-ttu-id="b4d4a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b4d4a-104">SYNTAX</span></span>

### <span data-ttu-id="b4d4a-105">Setextension (domyślne)</span><span class="sxs-lookup"><span data-stu-id="b4d4a-105">SetExtension (Default)</span></span>
```
Set-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [-Credential] <PSCredential>
 [[-Expiration] <DateTime>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b4d4a-106">SetExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="b4d4a-106">SetExtensionUsingThumbprint</span></span>
```
Set-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-CertificateThumbprint] <String> [[-ThumbprintAlgorithm] <String>] [-Credential] <PSCredential>
 [[-Expiration] <DateTime>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b4d4a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b4d4a-107">DESCRIPTION</span></span>
<span data-ttu-id="b4d4a-108">Polecenie cmdlet **Set-AzureServiceRemoteDesktopExtension** umożliwia rozszerzenie pulpitu zdalnego na określonych rolach lub we wszystkich rolach we wdrożonej usłudze lub wdrożeniu.</span><span class="sxs-lookup"><span data-stu-id="b4d4a-108">The **Set-AzureServiceRemoteDesktopExtension** cmdlet enables remote desktop extension on specified roles or all roles on a deployed service or at deployment.</span></span>

## <span data-ttu-id="b4d4a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b4d4a-109">EXAMPLES</span></span>

### <span data-ttu-id="b4d4a-110">Przykład 1: Włączanie rozszerzenia pulpitu zdalnego</span><span class="sxs-lookup"><span data-stu-id="b4d4a-110">Example 1: Enable remote desktop extension</span></span>
```
PS C:\> Set-AzureServiceRemoteDesktopExtension -ServiceName $svc -Credentials $creds
```

<span data-ttu-id="b4d4a-111">To polecenie włącza rozszerzenie pulpitu zdalnego dla określonej usługi.</span><span class="sxs-lookup"><span data-stu-id="b4d4a-111">This command enables the remote desktop extension for the specified service.</span></span>

### <span data-ttu-id="b4d4a-112">Przykład 2: Włączanie rozszerzenia pulpitu zdalnego dla określonej roli</span><span class="sxs-lookup"><span data-stu-id="b4d4a-112">Example 2: Enable remote desktop extension for a specified role</span></span>
```
PS C:\> Set-AzureServiceRemoteDesktopExtension -ServiceName $svc -Credentials $creds -Role "WebRole1"
```

<span data-ttu-id="b4d4a-113">To polecenie włącza rozszerzenie pulpitu zdalnego dla określonej usługi i roli.</span><span class="sxs-lookup"><span data-stu-id="b4d4a-113">This command enables the remote desktop extension for the specified service and role.</span></span>

## <span data-ttu-id="b4d4a-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b4d4a-114">PARAMETERS</span></span>

### <span data-ttu-id="b4d4a-115">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="b4d4a-115">-CertificateThumbprint</span></span>
<span data-ttu-id="b4d4a-116">Określa odcisk palca certyfikatu, który ma zostać użyty do zaszyfrowania konfiguracji prywatnej.</span><span class="sxs-lookup"><span data-stu-id="b4d4a-116">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="b4d4a-117">Ten certyfikat musi już istnieć w magazynie certyfikatów.</span><span class="sxs-lookup"><span data-stu-id="b4d4a-117">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="b4d4a-118">Jeśli nie określisz certyfikatu, to polecenie cmdlet utworzy certyfikat.</span><span class="sxs-lookup"><span data-stu-id="b4d4a-118">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

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

### <span data-ttu-id="b4d4a-119">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="b4d4a-119">-Credential</span></span>
<span data-ttu-id="b4d4a-120">Określa poświadczenia, które należy włączyć dla pulpitu zdalnego.</span><span class="sxs-lookup"><span data-stu-id="b4d4a-120">Specifies the credentials to enable for remote desktop.</span></span>
<span data-ttu-id="b4d4a-121">Poświadczenia zawierają nazwę użytkownika i hasło.</span><span class="sxs-lookup"><span data-stu-id="b4d4a-121">Credentials include a user name and password.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4d4a-122">-Data wygaśnięcia</span><span class="sxs-lookup"><span data-stu-id="b4d4a-122">-Expiration</span></span>
<span data-ttu-id="b4d4a-123">Określa obiekt daty i godziny umożliwiający użytkownikowi określenie terminu wygaśnięcia konta użytkownika.</span><span class="sxs-lookup"><span data-stu-id="b4d4a-123">Specifies a date time object that allows the user to specify when the user account expires.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4d4a-124">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="b4d4a-124">-ExtensionId</span></span>
<span data-ttu-id="b4d4a-125">Określa identyfikator rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="b4d4a-125">Specifies the extension ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4d4a-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b4d4a-126">-InformationAction</span></span>
<span data-ttu-id="b4d4a-127">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="b4d4a-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b4d4a-128">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="b4d4a-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b4d4a-129">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="b4d4a-129">Continue</span></span>
- <span data-ttu-id="b4d4a-130">Ignorować</span><span class="sxs-lookup"><span data-stu-id="b4d4a-130">Ignore</span></span>
- <span data-ttu-id="b4d4a-131">Inquire</span><span class="sxs-lookup"><span data-stu-id="b4d4a-131">Inquire</span></span>
- <span data-ttu-id="b4d4a-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b4d4a-132">SilentlyContinue</span></span>
- <span data-ttu-id="b4d4a-133">Przestaw</span><span class="sxs-lookup"><span data-stu-id="b4d4a-133">Stop</span></span>
- <span data-ttu-id="b4d4a-134">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="b4d4a-134">Suspend</span></span>

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

### <span data-ttu-id="b4d4a-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b4d4a-135">-InformationVariable</span></span>
<span data-ttu-id="b4d4a-136">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="b4d4a-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b4d4a-137">-Profile</span><span class="sxs-lookup"><span data-stu-id="b4d4a-137">-Profile</span></span>
<span data-ttu-id="b4d4a-138">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4d4a-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b4d4a-139">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="b4d4a-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b4d4a-140">-Rola</span><span class="sxs-lookup"><span data-stu-id="b4d4a-140">-Role</span></span>
<span data-ttu-id="b4d4a-141">Określa opcjonalną tablicę ról, dla których należy określić konfigurację pulpitu zdalnego.</span><span class="sxs-lookup"><span data-stu-id="b4d4a-141">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="b4d4a-142">Jeśli ten parametr nie zostanie określony, konfiguracja pulpitu zdalnego zostanie zastosowana jako Konfiguracja domyślna dla wszystkich ról.</span><span class="sxs-lookup"><span data-stu-id="b4d4a-142">If this parameter is not specified, the remote desktop configuration is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="b4d4a-143">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b4d4a-143">-ServiceName</span></span>
<span data-ttu-id="b4d4a-144">Określa nazwę usługi na platformie Azure wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="b4d4a-144">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="b4d4a-145">-Slot</span><span class="sxs-lookup"><span data-stu-id="b4d4a-145">-Slot</span></span>
<span data-ttu-id="b4d4a-146">Określa środowisko wdrożenia, które ma zostać zmodyfikowane.</span><span class="sxs-lookup"><span data-stu-id="b4d4a-146">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="b4d4a-147">Dopuszczalne wartości tego parametru to: produkcja, etapy.</span><span class="sxs-lookup"><span data-stu-id="b4d4a-147">The acceptable values for this parameter are: Production, Staging.</span></span>

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

### <span data-ttu-id="b4d4a-148">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="b4d4a-148">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="b4d4a-149">Określa algorytm mieszania odcisku palca, który jest używany w odniesieniu do odcisku palca w celu identyfikacji certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="b4d4a-149">Specifies a thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="b4d4a-150">Ten parametr jest opcjonalny, a jego wartością domyślną jest SHA1.</span><span class="sxs-lookup"><span data-stu-id="b4d4a-150">This parameter is optional and the default is sha1.</span></span>

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

### <span data-ttu-id="b4d4a-151">-Version</span><span class="sxs-lookup"><span data-stu-id="b4d4a-151">-Version</span></span>
<span data-ttu-id="b4d4a-152">Określa wersję rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="b4d4a-152">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4d4a-153">-X509</span><span class="sxs-lookup"><span data-stu-id="b4d4a-153">-X509Certificate</span></span>
<span data-ttu-id="b4d4a-154">Określa certyfikat x509, który jest automatycznie przekazywany do usługi w chmurze i jest wykorzystywany do szyfrowania prywatnej konfiguracji rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="b4d4a-154">Specifies an x509 certificate that is automatically uploaded to the cloud service and used for encrypting the private configuration of the extension.</span></span>

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

### <span data-ttu-id="b4d4a-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4d4a-155">CommonParameters</span></span>
<span data-ttu-id="b4d4a-156">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4d4a-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4d4a-157">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4d4a-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4d4a-158">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b4d4a-158">INPUTS</span></span>

## <span data-ttu-id="b4d4a-159">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b4d4a-159">OUTPUTS</span></span>

## <span data-ttu-id="b4d4a-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b4d4a-160">NOTES</span></span>

## <span data-ttu-id="b4d4a-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b4d4a-161">RELATED LINKS</span></span>

[<span data-ttu-id="b4d4a-162">Get-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="b4d4a-162">Get-AzureServiceRemoteDesktopExtension</span></span>](./Get-AzureServiceRemoteDesktopExtension.md)


