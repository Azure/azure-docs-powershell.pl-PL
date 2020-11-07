---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: 271da96d18628c899b10ac17185fd4c3a921d8a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527918"
---
# <span data-ttu-id="78bc9-101">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="78bc9-101">Set-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="78bc9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="78bc9-102">SYNOPSIS</span></span>
<span data-ttu-id="78bc9-103">Tworzy lub aktualizuje zasady dotyczące certyfikatu w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="78bc9-103">Creates or updates the policy for a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78bc9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="78bc9-104">SYNTAX</span></span>

### <span data-ttu-id="78bc9-105">ExpandedRenewPercentage (domyślny)</span><span class="sxs-lookup"><span data-stu-id="78bc9-105">ExpandedRenewPercentage (Default)</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> [-RenewAtPercentageLifetime <Int32>]
 [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-CertificateTransparency <Boolean>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78bc9-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="78bc9-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-InputObject] <PSKeyVaultCertificatePolicy> [-EmailAtNumberOfDaysBeforeExpiry <Int32>]
 [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>] [-CertificateTransparency <Boolean>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78bc9-107">ExpandedRenewNumber</span><span class="sxs-lookup"><span data-stu-id="78bc9-107">ExpandedRenewNumber</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 -RenewAtNumberOfDaysBeforeExpiry <Int32> [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>]
 [-Disabled] [-SubjectName <String>] [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-CertificateTransparency <Boolean>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78bc9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="78bc9-108">DESCRIPTION</span></span>
<span data-ttu-id="78bc9-109">Polecenie cmdlet **Set-AzureKeyVaultCertificatePolicy** służy do tworzenia lub aktualizowania zasad certyfikatu w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="78bc9-109">The **Set-AzureKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="78bc9-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="78bc9-110">EXAMPLES</span></span>

### <span data-ttu-id="78bc9-111">Przykład 1: Ustawianie zasad certyfikatów</span><span class="sxs-lookup"><span data-stu-id="78bc9-111">Example 1: Set a certificate policy</span></span>
```powershell
PS C:\> Set-AzureKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01" -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal $True -PassThru

SecretContentType               : application/x-pkcs12
Kty                             :
KeySize                         : 2048
Exportable                      :
ReuseKeyOnRenewal               : True
SubjectName                     : CN=contoso.com
DnsNames                        :
KeyUsage                        :
Ekus                            :
ValidityInMonths                : 6
IssuerName                      : Self
CertificateType                 :
RenewAtNumberOfDaysBeforeExpiry :
RenewAtPercentageLifetime       :
EmailAtNumberOfDaysBeforeExpiry :
EmailAtPercentageLifetime       :
CertificateTransparency         :
Enabled                         : True
Created                         :
Updated                         :
```

<span data-ttu-id="78bc9-112">To polecenie ustawia zasady dla certyfikatu TestCert01 w magazynie kluczy ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="78bc9-112">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="78bc9-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="78bc9-113">PARAMETERS</span></span>

### <span data-ttu-id="78bc9-114">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="78bc9-114">-CertificateTransparency</span></span>
<span data-ttu-id="78bc9-115">Wskazuje, czy dla tego certyfikatu/wystawcy jest włączone przezroczystość certyfikatu; Jeśli argument nie jest określony, wartością domyślną jest "prawda"</span><span class="sxs-lookup"><span data-stu-id="78bc9-115">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78bc9-116">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="78bc9-116">-CertificateType</span></span>
<span data-ttu-id="78bc9-117">Określa typ certyfikatu dla emitenta.</span><span class="sxs-lookup"><span data-stu-id="78bc9-117">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78bc9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78bc9-118">-DefaultProfile</span></span>
<span data-ttu-id="78bc9-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="78bc9-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78bc9-120">-Wyłączone</span><span class="sxs-lookup"><span data-stu-id="78bc9-120">-Disabled</span></span>
<span data-ttu-id="78bc9-121">Wskazuje, że zasada certyfikatu jest wyłączona.</span><span class="sxs-lookup"><span data-stu-id="78bc9-121">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78bc9-122">-DnsName</span><span class="sxs-lookup"><span data-stu-id="78bc9-122">-DnsName</span></span>
<span data-ttu-id="78bc9-123">Określa nazwę podmiotu certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="78bc9-123">Specifies the subject name of the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases: DnsNames

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78bc9-124">-Ekus</span><span class="sxs-lookup"><span data-stu-id="78bc9-124">-Ekus</span></span>
<span data-ttu-id="78bc9-125">Określa ulepszone użycie klucza (EKUs) w certyfikacie.</span><span class="sxs-lookup"><span data-stu-id="78bc9-125">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78bc9-126">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="78bc9-126">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="78bc9-127">Określa liczbę dni, po upływie których należy zacząć automatyczne odnawianie.</span><span class="sxs-lookup"><span data-stu-id="78bc9-127">Specifies the number of days before expiration when automatic renewal should start.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78bc9-128">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="78bc9-128">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="78bc9-129">Określa wartość procentową okresu istnienia, po upływie którego rozpocznie się proces automatycznego powiadomienia.</span><span class="sxs-lookup"><span data-stu-id="78bc9-129">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78bc9-130">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="78bc9-130">-InputObject</span></span>
<span data-ttu-id="78bc9-131">Określa zasady certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="78bc9-131">Specifies the certificate policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy
Parameter Sets: ByValue
Aliases: CertificatePolicy

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78bc9-132">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="78bc9-132">-IssuerName</span></span>
<span data-ttu-id="78bc9-133">Określa nazwę wystawcy dla tego certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="78bc9-133">Specifies the name of the issuer for this certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78bc9-134">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="78bc9-134">-KeyNotExportable</span></span>
<span data-ttu-id="78bc9-135">Wskazuje, że nie można eksportować klucza.</span><span class="sxs-lookup"><span data-stu-id="78bc9-135">Indicates that the key is not exportable.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78bc9-136">-KeyType</span><span class="sxs-lookup"><span data-stu-id="78bc9-136">-KeyType</span></span>
<span data-ttu-id="78bc9-137">Określa typ klucza klucza, który wykonuje kopię zapasową certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="78bc9-137">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="78bc9-138">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="78bc9-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="78bc9-139">ALGORYTM</span><span class="sxs-lookup"><span data-stu-id="78bc9-139">RSA</span></span>
- <span data-ttu-id="78bc9-140">RSA — HSM</span><span class="sxs-lookup"><span data-stu-id="78bc9-140">RSA-HSM</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA, RSA-HSM

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78bc9-141">-Użycie</span><span class="sxs-lookup"><span data-stu-id="78bc9-141">-KeyUsage</span></span>
<span data-ttu-id="78bc9-142">Określa użycie klucza w certyfikacie.</span><span class="sxs-lookup"><span data-stu-id="78bc9-142">Specifies the key usages in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:
Accepted values: None, EncipherOnly, CrlSign, KeyCertSign, KeyAgreement, DataEncipherment, KeyEncipherment, NonRepudiation, DigitalSignature, DecipherOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78bc9-143">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="78bc9-143">-Name</span></span>
<span data-ttu-id="78bc9-144">Określa nazwę certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="78bc9-144">Specifies the name of the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78bc9-145">-PassThru</span><span class="sxs-lookup"><span data-stu-id="78bc9-145">-PassThru</span></span>
<span data-ttu-id="78bc9-146">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="78bc9-146">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="78bc9-147">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="78bc9-147">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="78bc9-148">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="78bc9-148">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="78bc9-149">Określa liczbę dni przed wygaśnięciem, po upływie której rozpocznie się proces automatycznego odnawiania certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="78bc9-149">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ExpandedRenewNumber
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78bc9-150">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="78bc9-150">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="78bc9-151">Określa wartość procentową okresu istnienia, po upływie którego rozpocznie się proces automatycznego odnawiania certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="78bc9-151">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ExpandedRenewPercentage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78bc9-152">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="78bc9-152">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="78bc9-153">Wskazuje, że certyfikat jest ponownie używany podczas odnawiania klucza.</span><span class="sxs-lookup"><span data-stu-id="78bc9-153">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78bc9-154">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="78bc9-154">-SecretContentType</span></span>
<span data-ttu-id="78bc9-155">Określa typ zawartości nowego klucza tajnego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="78bc9-155">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="78bc9-156">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="78bc9-156">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="78bc9-157">application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="78bc9-157">application/x-pkcs12</span></span>
- <span data-ttu-id="78bc9-158">application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="78bc9-158">application/x-pem-file</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78bc9-159">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="78bc9-159">-SubjectName</span></span>
<span data-ttu-id="78bc9-160">Określa nazwę podmiotu certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="78bc9-160">Specifies the subject name of the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78bc9-161">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="78bc9-161">-ValidityInMonths</span></span>
<span data-ttu-id="78bc9-162">Określa liczbę miesięcy ważności certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="78bc9-162">Specifies the number of months the certificate is valid.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78bc9-163">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="78bc9-163">-VaultName</span></span>
<span data-ttu-id="78bc9-164">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="78bc9-164">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78bc9-165">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="78bc9-165">-Confirm</span></span>
<span data-ttu-id="78bc9-166">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78bc9-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78bc9-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78bc9-167">-WhatIf</span></span>
<span data-ttu-id="78bc9-168">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78bc9-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78bc9-169">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="78bc9-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78bc9-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78bc9-170">CommonParameters</span></span>
<span data-ttu-id="78bc9-171">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78bc9-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78bc9-172">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78bc9-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78bc9-173">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="78bc9-173">INPUTS</span></span>

### <span data-ttu-id="78bc9-174">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="78bc9-174">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="78bc9-175">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="78bc9-175">OUTPUTS</span></span>

### <span data-ttu-id="78bc9-176">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="78bc9-176">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="78bc9-177">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="78bc9-177">NOTES</span></span>

## <span data-ttu-id="78bc9-178">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="78bc9-178">RELATED LINKS</span></span>

[<span data-ttu-id="78bc9-179">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="78bc9-179">Get-AzureKeyVaultCertificatePolicy</span></span>](./Get-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="78bc9-180">Nowe — AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="78bc9-180">New-AzureKeyVaultCertificatePolicy</span></span>](./New-AzureKeyVaultCertificatePolicy.md)
