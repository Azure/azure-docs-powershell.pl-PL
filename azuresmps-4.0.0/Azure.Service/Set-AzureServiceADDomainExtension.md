---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 350638E1-636E-484B-88EB-91F48129D80B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0c665288d12897e4ab7277dd4ccf4bc5d975c037
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055014"
---
# <span data-ttu-id="395c1-101">Set-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="395c1-101">Set-AzureServiceADDomainExtension</span></span>

## <span data-ttu-id="395c1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="395c1-102">SYNOPSIS</span></span>
<span data-ttu-id="395c1-103">Umożliwia rozszerzenie domeny usługi AD dla usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="395c1-103">Enables an AD Domain extension for a cloud service.</span></span>

## <span data-ttu-id="395c1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="395c1-104">SYNTAX</span></span>

### <span data-ttu-id="395c1-105">JoinDomainUsingEnumOptions (domyślny)</span><span class="sxs-lookup"><span data-stu-id="395c1-105">JoinDomainUsingEnumOptions (Default)</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-UnjoinDomainCredential] <PSCredential>] [[-Options] <JoinOptions>]
 [[-OUPath] <String>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="395c1-106">JoinDomainUsingJoinOption</span><span class="sxs-lookup"><span data-stu-id="395c1-106">JoinDomainUsingJoinOption</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-UnjoinDomainCredential] <PSCredential>] [-JoinOption] <UInt32>
 [[-OUPath] <String>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="395c1-107">Grupa robocza</span><span class="sxs-lookup"><span data-stu-id="395c1-107">WorkGroupName</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [-WorkgroupName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="395c1-108">JoinDomainUsingEnumOptionsAndThumbprint</span><span class="sxs-lookup"><span data-stu-id="395c1-108">JoinDomainUsingEnumOptionsAndThumbprint</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-CertificateThumbprint] <String> [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-UnjoinDomainCredential] <PSCredential>] [[-Options] <JoinOptions>]
 [[-OUPath] <String>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="395c1-109">JoinDomainUsingJoinOptionAndThumbprint</span><span class="sxs-lookup"><span data-stu-id="395c1-109">JoinDomainUsingJoinOptionAndThumbprint</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-CertificateThumbprint] <String> [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-UnjoinDomainCredential] <PSCredential>] [-JoinOption] <UInt32>
 [[-OUPath] <String>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="395c1-110">WorkGroupNameThumbprint</span><span class="sxs-lookup"><span data-stu-id="395c1-110">WorkGroupNameThumbprint</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-CertificateThumbprint] <String> [[-ThumbprintAlgorithm] <String>] [-WorkgroupName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="395c1-111">Opis</span><span class="sxs-lookup"><span data-stu-id="395c1-111">DESCRIPTION</span></span>
<span data-ttu-id="395c1-112">Polecenie cmdlet **Set-AzureServiceADDomainExtension** włącza rozszerzenie domeny AD (Active Directory) dla usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="395c1-112">The **Set-AzureServiceADDomainExtension** cmdlet enables an AD (Active Directory) Domain extension for a cloud service.</span></span>

## <span data-ttu-id="395c1-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="395c1-113">EXAMPLES</span></span>

### <span data-ttu-id="395c1-114">1:1</span><span class="sxs-lookup"><span data-stu-id="395c1-114">1:</span></span>
```

```

## <span data-ttu-id="395c1-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="395c1-115">PARAMETERS</span></span>

### <span data-ttu-id="395c1-116">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="395c1-116">-CertificateThumbprint</span></span>
<span data-ttu-id="395c1-117">Określa odcisk palca certyfikatu, który ma zostać użyty do zaszyfrowania konfiguracji prywatnej.</span><span class="sxs-lookup"><span data-stu-id="395c1-117">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="395c1-118">Ten certyfikat musi już istnieć w magazynie certyfikatów.</span><span class="sxs-lookup"><span data-stu-id="395c1-118">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="395c1-119">Jeśli nie określisz certyfikatu, to polecenie cmdlet utworzy certyfikat.</span><span class="sxs-lookup"><span data-stu-id="395c1-119">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint, WorkGroupNameThumbprint
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="395c1-120">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="395c1-120">-Credential</span></span>
<span data-ttu-id="395c1-121">Określa poświadczenia do dołączenia do domeny usługi AD.</span><span class="sxs-lookup"><span data-stu-id="395c1-121">Specifies the credentials to join the AD domain.</span></span>
<span data-ttu-id="395c1-122">Poświadczenia zawierają nazwę użytkownika i hasło.</span><span class="sxs-lookup"><span data-stu-id="395c1-122">Credentials include a user name and password.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="395c1-123">-NazwaDomeny</span><span class="sxs-lookup"><span data-stu-id="395c1-123">-DomainName</span></span>
<span data-ttu-id="395c1-124">Określa nazwę domeny usługi AD.</span><span class="sxs-lookup"><span data-stu-id="395c1-124">Specifies the AD domain name.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="395c1-125">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="395c1-125">-ExtensionId</span></span>
<span data-ttu-id="395c1-126">Określa identyfikator rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="395c1-126">Specifies the extension ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="395c1-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="395c1-127">-InformationAction</span></span>
<span data-ttu-id="395c1-128">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="395c1-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="395c1-129">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="395c1-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="395c1-130">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="395c1-130">Continue</span></span>
- <span data-ttu-id="395c1-131">Ignorować</span><span class="sxs-lookup"><span data-stu-id="395c1-131">Ignore</span></span>
- <span data-ttu-id="395c1-132">Inquire</span><span class="sxs-lookup"><span data-stu-id="395c1-132">Inquire</span></span>
- <span data-ttu-id="395c1-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="395c1-133">SilentlyContinue</span></span>
- <span data-ttu-id="395c1-134">Przestaw</span><span class="sxs-lookup"><span data-stu-id="395c1-134">Stop</span></span>
- <span data-ttu-id="395c1-135">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="395c1-135">Suspend</span></span>

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

### <span data-ttu-id="395c1-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="395c1-136">-InformationVariable</span></span>
<span data-ttu-id="395c1-137">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="395c1-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="395c1-138">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="395c1-138">-JoinOption</span></span>
<span data-ttu-id="395c1-139">Określa Wyliczenie opcji sprzężenia.</span><span class="sxs-lookup"><span data-stu-id="395c1-139">Specifies the join option enumeration.</span></span>

```yaml
Type: UInt32
Parameter Sets: JoinDomainUsingJoinOption, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: True
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="395c1-140">-Opcje</span><span class="sxs-lookup"><span data-stu-id="395c1-140">-Options</span></span>
<span data-ttu-id="395c1-141">Określa opcję sprzężenia liczby całkowitej bez znaku.</span><span class="sxs-lookup"><span data-stu-id="395c1-141">Specifies the unsigned integer join option.</span></span>

```yaml
Type: JoinOptions
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingEnumOptionsAndThumbprint
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="395c1-142">-OUPath</span><span class="sxs-lookup"><span data-stu-id="395c1-142">-OUPath</span></span>
<span data-ttu-id="395c1-143">Określa ścieżkę jednostki organizacyjnej (OU) dla operacji dołączania domeny usługi AD.</span><span class="sxs-lookup"><span data-stu-id="395c1-143">Specifies the Organization Unit (OU) path for the AD domain join operation.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="395c1-144">-Profile</span><span class="sxs-lookup"><span data-stu-id="395c1-144">-Profile</span></span>
<span data-ttu-id="395c1-145">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="395c1-145">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="395c1-146">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="395c1-146">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="395c1-147">-Restart</span><span class="sxs-lookup"><span data-stu-id="395c1-147">-Restart</span></span>
<span data-ttu-id="395c1-148">Określa, czy należy ponownie uruchomić komputer, jeśli operacja dołączania się powiedzie.</span><span class="sxs-lookup"><span data-stu-id="395c1-148">Specifies whether to restart the computer if the join operation succeeds.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="395c1-149">-Rola</span><span class="sxs-lookup"><span data-stu-id="395c1-149">-Role</span></span>
<span data-ttu-id="395c1-150">Określa opcjonalną tablicę ról, dla których należy określić konfigurację pulpitu zdalnego.</span><span class="sxs-lookup"><span data-stu-id="395c1-150">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="395c1-151">Jeśli nie określono, konfiguracja domeny usługi AD zostanie zastosowana jako Konfiguracja domyślna dla wszystkich ról.</span><span class="sxs-lookup"><span data-stu-id="395c1-151">If not specified the AD domain configuration is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="395c1-152">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="395c1-152">-ServiceName</span></span>
<span data-ttu-id="395c1-153">Określa nazwę usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="395c1-153">Specifies the cloud service name.</span></span>

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

### <span data-ttu-id="395c1-154">-Slot</span><span class="sxs-lookup"><span data-stu-id="395c1-154">-Slot</span></span>
<span data-ttu-id="395c1-155">Określa środowisko wdrożenia, które ma zostać zmodyfikowane.</span><span class="sxs-lookup"><span data-stu-id="395c1-155">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="395c1-156">Dopuszczalne wartości tego parametru to: production lub Staging.</span><span class="sxs-lookup"><span data-stu-id="395c1-156">The acceptable values for this parameter are: Production or Staging.</span></span>

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

### <span data-ttu-id="395c1-157">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="395c1-157">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="395c1-158">Określa algorytm mieszania odcisku palca, który jest używany w odniesieniu do odcisku palca w celu identyfikacji certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="395c1-158">Specifies a thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="395c1-159">Ten parametr jest opcjonalny, a jego wartością domyślną jest SHA1.</span><span class="sxs-lookup"><span data-stu-id="395c1-159">This parameter is optional and the default is sha1.</span></span>

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

### <span data-ttu-id="395c1-160">-UnjoinDomainCredential</span><span class="sxs-lookup"><span data-stu-id="395c1-160">-UnjoinDomainCredential</span></span>
<span data-ttu-id="395c1-161">Określa poświadczenia (nazwa użytkownika i hasło) do odłączenia się do domeny usługi AD.</span><span class="sxs-lookup"><span data-stu-id="395c1-161">Specifies the credentials (user name and password) to unjoin the AD domain.</span></span>

```yaml
Type: PSCredential
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="395c1-162">-Version</span><span class="sxs-lookup"><span data-stu-id="395c1-162">-Version</span></span>
<span data-ttu-id="395c1-163">Określa wersję rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="395c1-163">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="395c1-164">-Workgroupname</span><span class="sxs-lookup"><span data-stu-id="395c1-164">-WorkgroupName</span></span>
<span data-ttu-id="395c1-165">Określa nazwę grupy roboczej.</span><span class="sxs-lookup"><span data-stu-id="395c1-165">Specifies the workgroup name.</span></span>

```yaml
Type: String
Parameter Sets: WorkGroupName, WorkGroupNameThumbprint
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="395c1-166">-X509</span><span class="sxs-lookup"><span data-stu-id="395c1-166">-X509Certificate</span></span>
<span data-ttu-id="395c1-167">Określa certyfikat x509, który po określeniu zostanie automatycznie przekazany do usługi w chmurze i jest wykorzystywany do szyfrowania konfiguracji prywatnej rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="395c1-167">Specifies an x509 certificate that when specified will be automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, WorkGroupName
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="395c1-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="395c1-168">CommonParameters</span></span>
<span data-ttu-id="395c1-169">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="395c1-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="395c1-170">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="395c1-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="395c1-171">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="395c1-171">INPUTS</span></span>

## <span data-ttu-id="395c1-172">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="395c1-172">OUTPUTS</span></span>

## <span data-ttu-id="395c1-173">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="395c1-173">NOTES</span></span>

## <span data-ttu-id="395c1-174">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="395c1-174">RELATED LINKS</span></span>

[<span data-ttu-id="395c1-175">Get-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="395c1-175">Get-AzureServiceADDomainExtension</span></span>](./Get-AzureServiceADDomainExtension.md)

[<span data-ttu-id="395c1-176">Remove-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="395c1-176">Remove-AzureServiceADDomainExtension</span></span>](./Remove-AzureServiceADDomainExtension.md)

[<span data-ttu-id="395c1-177">Nowe — AzureServiceADDomainExtensionConfig</span><span class="sxs-lookup"><span data-stu-id="395c1-177">New-AzureServiceADDomainExtensionConfig</span></span>](./New-AzureServiceADDomainExtensionConfig.md)


