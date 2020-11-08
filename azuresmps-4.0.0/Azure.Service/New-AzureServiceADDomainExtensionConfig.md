---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: DFD4BA63-A7DE-49DD-878C-68062EF17873
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4d4830d049ab01142c75847b4afd5419729f14d1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054863"
---
# <span data-ttu-id="eb128-101">New-AzureServiceADDomainExtensionConfig</span><span class="sxs-lookup"><span data-stu-id="eb128-101">New-AzureServiceADDomainExtensionConfig</span></span>

## <span data-ttu-id="eb128-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eb128-102">SYNOPSIS</span></span>
<span data-ttu-id="eb128-103">Generuje konfigurację rozszerzenia domeny usługi Active Directory dla usług w chmurze.</span><span class="sxs-lookup"><span data-stu-id="eb128-103">Generates the configuration for the AD domain extension for cloud services.</span></span>

## <span data-ttu-id="eb128-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eb128-104">SYNTAX</span></span>

### <span data-ttu-id="eb128-105">JoinDomainUsingEnumOptions (domyślny)</span><span class="sxs-lookup"><span data-stu-id="eb128-105">JoinDomainUsingEnumOptions (Default)</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-UnjoinDomainCredential] <PSCredential>] [[-Options] <JoinOptions>] [[-OUPath] <String>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="eb128-106">JoinDomainUsingJoinOption</span><span class="sxs-lookup"><span data-stu-id="eb128-106">JoinDomainUsingJoinOption</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-UnjoinDomainCredential] <PSCredential>] [-JoinOption] <UInt32> [[-OUPath] <String>] [[-Version] <String>]
 [[-ExtensionId] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="eb128-107">Grupa robocza</span><span class="sxs-lookup"><span data-stu-id="eb128-107">WorkGroupName</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [-WorkgroupName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="eb128-108">JoinDomainUsingEnumOptionsAndThumbprint</span><span class="sxs-lookup"><span data-stu-id="eb128-108">JoinDomainUsingEnumOptionsAndThumbprint</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-UnjoinDomainCredential] <PSCredential>] [[-Options] <JoinOptions>] [[-OUPath] <String>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="eb128-109">JoinDomainUsingJoinOptionAndThumbprint</span><span class="sxs-lookup"><span data-stu-id="eb128-109">JoinDomainUsingJoinOptionAndThumbprint</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-UnjoinDomainCredential] <PSCredential>] [-JoinOption] <UInt32> [[-OUPath] <String>] [[-Version] <String>]
 [[-ExtensionId] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="eb128-110">WorkGroupNameThumbprint</span><span class="sxs-lookup"><span data-stu-id="eb128-110">WorkGroupNameThumbprint</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [-WorkgroupName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="eb128-111">Opis</span><span class="sxs-lookup"><span data-stu-id="eb128-111">DESCRIPTION</span></span>
<span data-ttu-id="eb128-112">Polecenie cmdlet **New-AzureServiceADDomainExtensionConfig** generuje konfigurację rozszerzenia domeny Active Directory (AD) dla usług w chmurze.</span><span class="sxs-lookup"><span data-stu-id="eb128-112">The **New-AzureServiceADDomainExtensionConfig** cmdlet generates the configuration for the Active Directory (AD) domain extension for cloud services.</span></span>

## <span data-ttu-id="eb128-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eb128-113">EXAMPLES</span></span>

### <span data-ttu-id="eb128-114">Przykład 1. Określanie konfiguracji domeny usługi AD</span><span class="sxs-lookup"><span data-stu-id="eb128-114">Example 1: Specify an AD domain configuration</span></span>
```
PS C:\> $ExtensionCfg = New-AzureServiceADDomainExtensionConfig -Role WorkerRole1 -DomainName $Domain -Credential $Cred -JoinOption 35;

PS C:\> New-AzureDeployment -ServiceName $CloudSvc -Slot "Production" -Package $Pkg -Configuration $Config -ExtensionConfiguration $ExtensionCfg;
```

<span data-ttu-id="eb128-115">To polecenie generuje konfigurację rozszerzenia domeny usługi AD.</span><span class="sxs-lookup"><span data-stu-id="eb128-115">This command generates a configuration for the AD domain extension.</span></span>

## <span data-ttu-id="eb128-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eb128-116">PARAMETERS</span></span>

### <span data-ttu-id="eb128-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="eb128-117">-CertificateThumbprint</span></span>
<span data-ttu-id="eb128-118">Określa odcisk palca certyfikatu, który ma zostać użyty do zaszyfrowania konfiguracji prywatnej.</span><span class="sxs-lookup"><span data-stu-id="eb128-118">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="eb128-119">Ten certyfikat musi już istnieć w magazynie certyfikatów.</span><span class="sxs-lookup"><span data-stu-id="eb128-119">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="eb128-120">Jeśli nie określisz certyfikatu, to polecenie cmdlet utworzy certyfikat.</span><span class="sxs-lookup"><span data-stu-id="eb128-120">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint, WorkGroupNameThumbprint
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb128-121">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="eb128-121">-Credential</span></span>
<span data-ttu-id="eb128-122">Określa poświadczenia, które mają zostać użyte do dołączenia do domeny usługi AD.</span><span class="sxs-lookup"><span data-stu-id="eb128-122">Specifies the credentials to use to join the AD domain.</span></span>
<span data-ttu-id="eb128-123">Poświadczenia zawierają nazwę użytkownika i hasło.</span><span class="sxs-lookup"><span data-stu-id="eb128-123">Credentials include a user name and password.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb128-124">-NazwaDomeny</span><span class="sxs-lookup"><span data-stu-id="eb128-124">-DomainName</span></span>
<span data-ttu-id="eb128-125">Określa nazwę domeny usługi AD.</span><span class="sxs-lookup"><span data-stu-id="eb128-125">Specifies the AD domain name.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb128-126">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="eb128-126">-ExtensionId</span></span>
<span data-ttu-id="eb128-127">Określa identyfikator rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="eb128-127">Specifies the extension ID.</span></span>

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

### <span data-ttu-id="eb128-128">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="eb128-128">-InformationAction</span></span>
<span data-ttu-id="eb128-129">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="eb128-129">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="eb128-130">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="eb128-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="eb128-131">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="eb128-131">Continue</span></span>
- <span data-ttu-id="eb128-132">Ignorować</span><span class="sxs-lookup"><span data-stu-id="eb128-132">Ignore</span></span>
- <span data-ttu-id="eb128-133">Inquire</span><span class="sxs-lookup"><span data-stu-id="eb128-133">Inquire</span></span>
- <span data-ttu-id="eb128-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="eb128-134">SilentlyContinue</span></span>
- <span data-ttu-id="eb128-135">Przestaw</span><span class="sxs-lookup"><span data-stu-id="eb128-135">Stop</span></span>
- <span data-ttu-id="eb128-136">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="eb128-136">Suspend</span></span>

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

### <span data-ttu-id="eb128-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="eb128-137">-InformationVariable</span></span>
<span data-ttu-id="eb128-138">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="eb128-138">Specifies an information variable.</span></span>

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

### <span data-ttu-id="eb128-139">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="eb128-139">-JoinOption</span></span>
<span data-ttu-id="eb128-140">Określa Wyliczenie opcji sprzężenia.</span><span class="sxs-lookup"><span data-stu-id="eb128-140">Specifies the join option enumeration.</span></span>

```yaml
Type: UInt32
Parameter Sets: JoinDomainUsingJoinOption, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb128-141">-Opcje</span><span class="sxs-lookup"><span data-stu-id="eb128-141">-Options</span></span>
<span data-ttu-id="eb128-142">Określa opcję sprzężenia liczby całkowitej bez znaku.</span><span class="sxs-lookup"><span data-stu-id="eb128-142">Specifies the unsigned integer join option.</span></span>

```yaml
Type: JoinOptions
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingEnumOptionsAndThumbprint
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb128-143">-OUPath</span><span class="sxs-lookup"><span data-stu-id="eb128-143">-OUPath</span></span>
<span data-ttu-id="eb128-144">Określa ścieżkę jednostki organizacyjnej (OU) dla operacji dołączania domeny usługi AD.</span><span class="sxs-lookup"><span data-stu-id="eb128-144">Specifies the organization unit (OU) path for AD domain join operation.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb128-145">-Profile</span><span class="sxs-lookup"><span data-stu-id="eb128-145">-Profile</span></span>
<span data-ttu-id="eb128-146">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb128-146">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="eb128-147">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="eb128-147">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="eb128-148">-Restart</span><span class="sxs-lookup"><span data-stu-id="eb128-148">-Restart</span></span>
<span data-ttu-id="eb128-149">Określa, czy należy ponownie uruchomić komputer, jeśli operacja dołączania się powiedzie.</span><span class="sxs-lookup"><span data-stu-id="eb128-149">Specifies whether to restart the computer if the join operation succeeds.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb128-150">-Rola</span><span class="sxs-lookup"><span data-stu-id="eb128-150">-Role</span></span>
<span data-ttu-id="eb128-151">Określa opcjonalną tablicę ról określającą konfigurację pulpitu zdalnego dla konfiguracji domeny usługi AD.</span><span class="sxs-lookup"><span data-stu-id="eb128-151">Specifies an optional array of roles to specify the remote desktop configuration for the AD domain configuration.</span></span>
<span data-ttu-id="eb128-152">Jeśli ten parametr nie zostanie określony, konfiguracja domeny usługi AD zostanie zastosowana jako Konfiguracja domyślna dla wszystkich ról.</span><span class="sxs-lookup"><span data-stu-id="eb128-152">If you do not specify this parameter, the AD domain configuration is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="eb128-153">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="eb128-153">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="eb128-154">Określa algorytm mieszania odcisku palca, który jest używany z odciskiem palca w celu identyfikacji certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="eb128-154">Specifies a thumbprint hashing algorithm that is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="eb128-155">Ten parametr jest opcjonalny, a jego wartością domyślną jest SHA1.</span><span class="sxs-lookup"><span data-stu-id="eb128-155">This parameter is optional and the default is sha1.</span></span>

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

### <span data-ttu-id="eb128-156">-UnjoinDomainCredential</span><span class="sxs-lookup"><span data-stu-id="eb128-156">-UnjoinDomainCredential</span></span>
<span data-ttu-id="eb128-157">Określa poświadczenia (nazwa użytkownika i hasło) do odłączenia się do domeny usługi AD.</span><span class="sxs-lookup"><span data-stu-id="eb128-157">Specifies the credentials (user name and password) to unjoin the AD domain.</span></span>

```yaml
Type: PSCredential
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb128-158">-Version</span><span class="sxs-lookup"><span data-stu-id="eb128-158">-Version</span></span>
<span data-ttu-id="eb128-159">Określa wersję rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="eb128-159">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb128-160">-Workgroupname</span><span class="sxs-lookup"><span data-stu-id="eb128-160">-WorkgroupName</span></span>
<span data-ttu-id="eb128-161">Określa nazwę grupy roboczej.</span><span class="sxs-lookup"><span data-stu-id="eb128-161">Specifies the workgroup name.</span></span>

```yaml
Type: String
Parameter Sets: WorkGroupName, WorkGroupNameThumbprint
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb128-162">-X509</span><span class="sxs-lookup"><span data-stu-id="eb128-162">-X509Certificate</span></span>
<span data-ttu-id="eb128-163">Określa certyfikat X. 509, który jest automatycznie przekazywany do usługi w chmurze i służy do szyfrowania konfiguracji prywatnej rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="eb128-163">Specifies an X.509 certificate that is automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, WorkGroupName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb128-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb128-164">CommonParameters</span></span>
<span data-ttu-id="eb128-165">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb128-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb128-166">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb128-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb128-167">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eb128-167">INPUTS</span></span>

## <span data-ttu-id="eb128-168">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eb128-168">OUTPUTS</span></span>

## <span data-ttu-id="eb128-169">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eb128-169">NOTES</span></span>

## <span data-ttu-id="eb128-170">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eb128-170">RELATED LINKS</span></span>

[<span data-ttu-id="eb128-171">Get-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="eb128-171">Get-AzureServiceADDomainExtension</span></span>](./Get-AzureServiceADDomainExtension.md)

[<span data-ttu-id="eb128-172">Set-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="eb128-172">Set-AzureServiceADDomainExtension</span></span>](./Set-AzureServiceADDomainExtension.md)


