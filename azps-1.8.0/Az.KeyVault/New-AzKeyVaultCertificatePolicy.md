---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: e5b03660c37dff6333479c19d7de039d368fd4ee
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867943"
---
# <span data-ttu-id="6169a-101">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="6169a-101">New-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="6169a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6169a-102">SYNOPSIS</span></span>
<span data-ttu-id="6169a-103">Tworzy obiekt zasad certyfikatu w pamięci.</span><span class="sxs-lookup"><span data-stu-id="6169a-103">Creates an in-memory certificate policy object.</span></span>

## <span data-ttu-id="6169a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6169a-104">SYNTAX</span></span>

### <span data-ttu-id="6169a-105">SubjectName (wartość domyślna)</span><span class="sxs-lookup"><span data-stu-id="6169a-105">SubjectName (Default)</span></span>
```
New-AzKeyVaultCertificatePolicy [-IssuerName] <String> [-SubjectName] <String>
 [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>]
 [-ReuseKeyOnRenewal] [-Disabled]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6169a-106">DNSNames</span><span class="sxs-lookup"><span data-stu-id="6169a-106">DNSNames</span></span>
```
New-AzKeyVaultCertificatePolicy [-IssuerName] <String> [[-SubjectName] <String>]
 [-DnsName] <System.Collections.Generic.List`1[System.String]> [-RenewAtNumberOfDaysBeforeExpiry <Int32>]
 [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>] [-ReuseKeyOnRenewal] [-Disabled]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6169a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="6169a-107">DESCRIPTION</span></span>
<span data-ttu-id="6169a-108">Polecenie cmdlet **New-AzKeyVaultCertificatePolicy** umożliwia utworzenie obiektu zasad certyfikatu w pamięci dla magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6169a-108">The **New-AzKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="6169a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6169a-109">EXAMPLES</span></span>

### <span data-ttu-id="6169a-110">Przykład 1: Tworzenie zasad certyfikatów</span><span class="sxs-lookup"><span data-stu-id="6169a-110">Example 1: Create a certificate policy</span></span>
```powershell
PS C:\> New-AzKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal

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

<span data-ttu-id="6169a-111">To polecenie tworzy zasady certyfikatów, które są ważne przez sześć miesięcy i odnowią certyfikat za pomocą klucza.</span><span class="sxs-lookup"><span data-stu-id="6169a-111">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

## <span data-ttu-id="6169a-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6169a-112">PARAMETERS</span></span>

### <span data-ttu-id="6169a-113">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="6169a-113">-CertificateType</span></span>
<span data-ttu-id="6169a-114">Określa typ certyfikatu dla emitenta.</span><span class="sxs-lookup"><span data-stu-id="6169a-114">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6169a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6169a-115">-DefaultProfile</span></span>
<span data-ttu-id="6169a-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="6169a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6169a-117">-Wyłączone</span><span class="sxs-lookup"><span data-stu-id="6169a-117">-Disabled</span></span>
<span data-ttu-id="6169a-118">Wskazuje, że zasada certyfikatu jest wyłączona.</span><span class="sxs-lookup"><span data-stu-id="6169a-118">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6169a-119">-DnsName</span><span class="sxs-lookup"><span data-stu-id="6169a-119">-DnsName</span></span>
<span data-ttu-id="6169a-120">Określa nazwy DNS w certyfikacie.</span><span class="sxs-lookup"><span data-stu-id="6169a-120">Specifies the DNS names in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: DNSNames
Aliases: DnsNames

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6169a-121">-Ekus</span><span class="sxs-lookup"><span data-stu-id="6169a-121">-Ekus</span></span>
<span data-ttu-id="6169a-122">Określa ulepszone użycie klucza (EKUs) w certyfikacie.</span><span class="sxs-lookup"><span data-stu-id="6169a-122">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="6169a-123">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="6169a-123">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="6169a-124">Określa, ile dni przed wygaśnięciem rozpocznie się proces powiadomień automatycznych.</span><span class="sxs-lookup"><span data-stu-id="6169a-124">Specifies how many days before expiry the automatic notification process begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6169a-125">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="6169a-125">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="6169a-126">Określa wartość procentową okresu istnienia, po upływie którego rozpocznie się proces automatycznego powiadomienia.</span><span class="sxs-lookup"><span data-stu-id="6169a-126">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6169a-127">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="6169a-127">-IssuerName</span></span>
<span data-ttu-id="6169a-128">Określa nazwę wystawcy certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="6169a-128">Specifies the name of the issuer for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6169a-129">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="6169a-129">-KeyNotExportable</span></span>
<span data-ttu-id="6169a-130">Wskazuje, że nie można eksportować klucza.</span><span class="sxs-lookup"><span data-stu-id="6169a-130">Indicates that the key is not exportable.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6169a-131">-KeyType</span><span class="sxs-lookup"><span data-stu-id="6169a-131">-KeyType</span></span>
<span data-ttu-id="6169a-132">Określa typ klucza klucza, który wykonuje kopię zapasową certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="6169a-132">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="6169a-133">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="6169a-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6169a-134">ALGORYTM</span><span class="sxs-lookup"><span data-stu-id="6169a-134">RSA</span></span>
- <span data-ttu-id="6169a-135">RSA — HSM</span><span class="sxs-lookup"><span data-stu-id="6169a-135">RSA-HSM</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA, RSA-HSM

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6169a-136">-Użycie</span><span class="sxs-lookup"><span data-stu-id="6169a-136">-KeyUsage</span></span>
<span data-ttu-id="6169a-137">Określa użycie klucza w certyfikacie.</span><span class="sxs-lookup"><span data-stu-id="6169a-137">Specifies the key usages in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]
Parameter Sets: (All)
Aliases:
Accepted values: None, EncipherOnly, CrlSign, KeyCertSign, KeyAgreement, DataEncipherment, KeyEncipherment, NonRepudiation, DigitalSignature, DecipherOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6169a-138">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="6169a-138">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="6169a-139">Określa liczbę dni przed wygaśnięciem, po upływie której rozpocznie się proces automatycznego odnawiania certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="6169a-139">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6169a-140">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="6169a-140">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="6169a-141">Określa wartość procentową okresu istnienia, po upływie którego rozpocznie się proces automatycznego odnawiania certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="6169a-141">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6169a-142">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="6169a-142">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="6169a-143">Wskazuje, że certyfikat jest ponownie używany podczas odnawiania klucza.</span><span class="sxs-lookup"><span data-stu-id="6169a-143">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6169a-144">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="6169a-144">-SecretContentType</span></span>
<span data-ttu-id="6169a-145">Określa typ zawartości nowego klucza tajnego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="6169a-145">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="6169a-146">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="6169a-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6169a-147">application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="6169a-147">application/x-pkcs12</span></span>
- <span data-ttu-id="6169a-148">application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="6169a-148">application/x-pem-file</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6169a-149">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="6169a-149">-SubjectName</span></span>
<span data-ttu-id="6169a-150">Określa nazwę podmiotu certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="6169a-150">Specifies the subject name of the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: SubjectName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DNSNames
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6169a-151">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="6169a-151">-ValidityInMonths</span></span>
<span data-ttu-id="6169a-152">Określa liczbę miesięcy ważności certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="6169a-152">Specifies the number of months the certificate is valid.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6169a-153">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6169a-153">-Confirm</span></span>
<span data-ttu-id="6169a-154">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6169a-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6169a-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6169a-155">-WhatIf</span></span>
<span data-ttu-id="6169a-156">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6169a-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6169a-157">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6169a-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6169a-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6169a-158">CommonParameters</span></span>
<span data-ttu-id="6169a-159">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6169a-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6169a-160">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6169a-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6169a-161">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6169a-161">INPUTS</span></span>

### <span data-ttu-id="6169a-162">System. String</span><span class="sxs-lookup"><span data-stu-id="6169a-162">System.String</span></span>

### <span data-ttu-id="6169a-163">System. Collections. Generic. list "1 [[System. String; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6169a-163">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="6169a-164">System. Nullable ' 1 [[System. Int32; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6169a-164">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="6169a-165">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6169a-165">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="6169a-166">System. Collections. Generic. list "1 [[System. Security. Kryptografia. x509. X509KeyUsageFlags, system. Security. Kryptografia. x509, Version = 4.2.1.0, Culture = neutral, PublicKeyToken = b03f5f7f11d50a3a]]</span><span class="sxs-lookup"><span data-stu-id="6169a-166">System.Collections.Generic.List\`1[[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags, System.Security.Cryptography.X509Certificates, Version=4.2.1.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a]]</span></span>

## <span data-ttu-id="6169a-167">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6169a-167">OUTPUTS</span></span>

### <span data-ttu-id="6169a-168">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="6169a-168">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="6169a-169">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6169a-169">NOTES</span></span>

## <span data-ttu-id="6169a-170">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6169a-170">RELATED LINKS</span></span>

[<span data-ttu-id="6169a-171">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="6169a-171">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="6169a-172">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="6169a-172">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

