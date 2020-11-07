---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/new-azurekeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: a77cd700064777c769d5499cb099cfa3f9a53ec0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716947"
---
# <span data-ttu-id="f13bf-101">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="f13bf-101">New-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="f13bf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f13bf-102">SYNOPSIS</span></span>
<span data-ttu-id="f13bf-103">Tworzy obiekt zasad certyfikatu w pamięci.</span><span class="sxs-lookup"><span data-stu-id="f13bf-103">Creates an in-memory certificate policy object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f13bf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f13bf-104">SYNTAX</span></span>

### <span data-ttu-id="f13bf-105">SubjectName (wartość domyślna)</span><span class="sxs-lookup"><span data-stu-id="f13bf-105">SubjectName (Default)</span></span>
```
New-AzureKeyVaultCertificatePolicy [-IssuerName] <String> [-SubjectName] <String>
 [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>]
 [-ReuseKeyOnRenewal] [-Disabled]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f13bf-106">DNSNames</span><span class="sxs-lookup"><span data-stu-id="f13bf-106">DNSNames</span></span>
```
New-AzureKeyVaultCertificatePolicy [-IssuerName] <String> [[-SubjectName] <String>]
 [-DnsName] <System.Collections.Generic.List`1[System.String]> [-RenewAtNumberOfDaysBeforeExpiry <Int32>]
 [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>] [-ReuseKeyOnRenewal] [-Disabled]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f13bf-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f13bf-107">DESCRIPTION</span></span>
<span data-ttu-id="f13bf-108">Polecenie cmdlet **New-AzureKeyVaultCertificatePolicy** umożliwia utworzenie obiektu zasad certyfikatu w pamięci dla magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f13bf-108">The **New-AzureKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="f13bf-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f13bf-109">EXAMPLES</span></span>

### <span data-ttu-id="f13bf-110">Przykład 1: Tworzenie zasad certyfikatów</span><span class="sxs-lookup"><span data-stu-id="f13bf-110">Example 1: Create a certificate policy</span></span>
```powershell
PS C:\> New-AzureKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal

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

<span data-ttu-id="f13bf-111">To polecenie tworzy zasady certyfikatów, które są ważne przez sześć miesięcy i odnowią certyfikat za pomocą klucza.</span><span class="sxs-lookup"><span data-stu-id="f13bf-111">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

## <span data-ttu-id="f13bf-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f13bf-112">PARAMETERS</span></span>

### <span data-ttu-id="f13bf-113">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="f13bf-113">-CertificateType</span></span>
<span data-ttu-id="f13bf-114">Określa typ certyfikatu dla emitenta.</span><span class="sxs-lookup"><span data-stu-id="f13bf-114">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="f13bf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f13bf-115">-DefaultProfile</span></span>
<span data-ttu-id="f13bf-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f13bf-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f13bf-117">-Wyłączone</span><span class="sxs-lookup"><span data-stu-id="f13bf-117">-Disabled</span></span>
<span data-ttu-id="f13bf-118">Wskazuje, że zasada certyfikatu jest wyłączona.</span><span class="sxs-lookup"><span data-stu-id="f13bf-118">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="f13bf-119">-DnsName</span><span class="sxs-lookup"><span data-stu-id="f13bf-119">-DnsName</span></span>
<span data-ttu-id="f13bf-120">Określa nazwy DNS w certyfikacie.</span><span class="sxs-lookup"><span data-stu-id="f13bf-120">Specifies the DNS names in the certificate.</span></span>

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

### <span data-ttu-id="f13bf-121">-Ekus</span><span class="sxs-lookup"><span data-stu-id="f13bf-121">-Ekus</span></span>
<span data-ttu-id="f13bf-122">Określa ulepszone użycie klucza (EKUs) w certyfikacie.</span><span class="sxs-lookup"><span data-stu-id="f13bf-122">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="f13bf-123">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="f13bf-123">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="f13bf-124">Określa, ile dni przed wygaśnięciem rozpocznie się proces powiadomień automatycznych.</span><span class="sxs-lookup"><span data-stu-id="f13bf-124">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="f13bf-125">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="f13bf-125">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="f13bf-126">Określa wartość procentową okresu istnienia, po upływie którego rozpocznie się proces automatycznego powiadomienia.</span><span class="sxs-lookup"><span data-stu-id="f13bf-126">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="f13bf-127">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="f13bf-127">-IssuerName</span></span>
<span data-ttu-id="f13bf-128">Określa nazwę wystawcy certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="f13bf-128">Specifies the name of the issuer for the certificate.</span></span>

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

### <span data-ttu-id="f13bf-129">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="f13bf-129">-KeyNotExportable</span></span>
<span data-ttu-id="f13bf-130">Wskazuje, że nie można eksportować klucza.</span><span class="sxs-lookup"><span data-stu-id="f13bf-130">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="f13bf-131">-KeyType</span><span class="sxs-lookup"><span data-stu-id="f13bf-131">-KeyType</span></span>
<span data-ttu-id="f13bf-132">Określa typ klucza klucza, który wykonuje kopię zapasową certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="f13bf-132">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="f13bf-133">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="f13bf-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f13bf-134">ALGORYTM</span><span class="sxs-lookup"><span data-stu-id="f13bf-134">RSA</span></span>
- <span data-ttu-id="f13bf-135">RSA — HSM</span><span class="sxs-lookup"><span data-stu-id="f13bf-135">RSA-HSM</span></span>

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

### <span data-ttu-id="f13bf-136">-Użycie</span><span class="sxs-lookup"><span data-stu-id="f13bf-136">-KeyUsage</span></span>
<span data-ttu-id="f13bf-137">Określa użycie klucza w certyfikacie.</span><span class="sxs-lookup"><span data-stu-id="f13bf-137">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="f13bf-138">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="f13bf-138">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="f13bf-139">Określa liczbę dni przed wygaśnięciem, po upływie której rozpocznie się proces automatycznego odnawiania certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="f13bf-139">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="f13bf-140">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="f13bf-140">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="f13bf-141">Określa wartość procentową okresu istnienia, po upływie którego rozpocznie się proces automatycznego odnawiania certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="f13bf-141">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="f13bf-142">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="f13bf-142">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="f13bf-143">Wskazuje, że certyfikat jest ponownie używany podczas odnawiania klucza.</span><span class="sxs-lookup"><span data-stu-id="f13bf-143">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="f13bf-144">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="f13bf-144">-SecretContentType</span></span>
<span data-ttu-id="f13bf-145">Określa typ zawartości nowego klucza tajnego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="f13bf-145">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="f13bf-146">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="f13bf-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f13bf-147">application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="f13bf-147">application/x-pkcs12</span></span>
- <span data-ttu-id="f13bf-148">application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="f13bf-148">application/x-pem-file</span></span>

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

### <span data-ttu-id="f13bf-149">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="f13bf-149">-SubjectName</span></span>
<span data-ttu-id="f13bf-150">Określa nazwę podmiotu certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="f13bf-150">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="f13bf-151">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="f13bf-151">-ValidityInMonths</span></span>
<span data-ttu-id="f13bf-152">Określa liczbę miesięcy ważności certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="f13bf-152">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="f13bf-153">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f13bf-153">-Confirm</span></span>
<span data-ttu-id="f13bf-154">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f13bf-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f13bf-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f13bf-155">-WhatIf</span></span>
<span data-ttu-id="f13bf-156">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f13bf-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f13bf-157">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f13bf-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f13bf-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f13bf-158">CommonParameters</span></span>
<span data-ttu-id="f13bf-159">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f13bf-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f13bf-160">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f13bf-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f13bf-161">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f13bf-161">INPUTS</span></span>

### <span data-ttu-id="f13bf-162">System. String</span><span class="sxs-lookup"><span data-stu-id="f13bf-162">System.String</span></span>

### <span data-ttu-id="f13bf-163">System. Collections. Generic. list "1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="f13bf-163">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="f13bf-164">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="f13bf-164">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="f13bf-165">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f13bf-165">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="f13bf-166">System. Collections. Generic. list "1 [[System. Security. Kryptografia. x509. X509KeyUsageFlags, system, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="f13bf-166">System.Collections.Generic.List\`1[[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags, System, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="f13bf-167">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f13bf-167">OUTPUTS</span></span>

### <span data-ttu-id="f13bf-168">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="f13bf-168">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="f13bf-169">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f13bf-169">NOTES</span></span>

## <span data-ttu-id="f13bf-170">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f13bf-170">RELATED LINKS</span></span>

[<span data-ttu-id="f13bf-171">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="f13bf-171">Get-AzureKeyVaultCertificatePolicy</span></span>](./Get-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="f13bf-172">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="f13bf-172">Set-AzureKeyVaultCertificatePolicy</span></span>](./Set-AzureKeyVaultCertificatePolicy.md)

