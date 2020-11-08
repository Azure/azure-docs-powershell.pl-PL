---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: b0d690358fb5598b1a88ecb7fe169c8ef3d2718f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053847"
---
# <span data-ttu-id="48f1f-101">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="48f1f-101">New-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="48f1f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="48f1f-102">SYNOPSIS</span></span>
<span data-ttu-id="48f1f-103">Tworzy obiekt zasad certyfikatu w pamięci.</span><span class="sxs-lookup"><span data-stu-id="48f1f-103">Creates an in-memory certificate policy object.</span></span>

## <span data-ttu-id="48f1f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="48f1f-104">SYNTAX</span></span>

### <span data-ttu-id="48f1f-105">SubjectName (wartość domyślna)</span><span class="sxs-lookup"><span data-stu-id="48f1f-105">SubjectName (Default)</span></span>
```
New-AzKeyVaultCertificatePolicy [-IssuerName] <String> [-SubjectName] <String>
 [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>]
 [-ReuseKeyOnRenewal] [-Disabled]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeySize <Int32>] [-KeyNotExportable] [-CertificateTransparency <Boolean>]
 [-Curve <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48f1f-106">DNSNames</span><span class="sxs-lookup"><span data-stu-id="48f1f-106">DNSNames</span></span>
```
New-AzKeyVaultCertificatePolicy [-IssuerName] <String> [[-SubjectName] <String>]
 [-DnsName] <System.Collections.Generic.List`1[System.String]> [-RenewAtNumberOfDaysBeforeExpiry <Int32>]
 [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>] [-ReuseKeyOnRenewal] [-Disabled]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeySize <Int32>] [-KeyNotExportable] [-CertificateTransparency <Boolean>]
 [-Curve <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48f1f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="48f1f-107">DESCRIPTION</span></span>
<span data-ttu-id="48f1f-108">Polecenie cmdlet **New-AzKeyVaultCertificatePolicy** umożliwia utworzenie obiektu zasad certyfikatu w pamięci dla magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="48f1f-108">The **New-AzKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="48f1f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="48f1f-109">EXAMPLES</span></span>

### <span data-ttu-id="48f1f-110">Przykład 1: Tworzenie zasad certyfikatów</span><span class="sxs-lookup"><span data-stu-id="48f1f-110">Example 1: Create a certificate policy</span></span>
```powershell
PS C:\> New-AzKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal

SecretContentType               : application/x-pkcs12
Kty                             :
KeySize                         : 2048
Curve                           :
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

<span data-ttu-id="48f1f-111">To polecenie tworzy zasady certyfikatów, które są ważne przez sześć miesięcy i odnowią certyfikat za pomocą klucza.</span><span class="sxs-lookup"><span data-stu-id="48f1f-111">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

## <span data-ttu-id="48f1f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="48f1f-112">PARAMETERS</span></span>

### <span data-ttu-id="48f1f-113">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="48f1f-113">-CertificateTransparency</span></span>
<span data-ttu-id="48f1f-114">Wskazuje, czy dla tego certyfikatu/wystawcy jest włączone przezroczystość certyfikatu; Jeśli argument nie jest określony, wartością domyślną jest "prawda"</span><span class="sxs-lookup"><span data-stu-id="48f1f-114">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48f1f-115">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="48f1f-115">-CertificateType</span></span>
<span data-ttu-id="48f1f-116">Określa typ certyfikatu dla emitenta.</span><span class="sxs-lookup"><span data-stu-id="48f1f-116">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="48f1f-117">-Krzywa</span><span class="sxs-lookup"><span data-stu-id="48f1f-117">-Curve</span></span>
<span data-ttu-id="48f1f-118">Określa nazwę krzywej eliptycznej klucza certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="48f1f-118">Specifies the elliptic curve name of the key of the certificate.</span></span>
<span data-ttu-id="48f1f-119">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="48f1f-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="48f1f-120">P-256</span><span class="sxs-lookup"><span data-stu-id="48f1f-120">P-256</span></span>
- <span data-ttu-id="48f1f-121">P-384</span><span class="sxs-lookup"><span data-stu-id="48f1f-121">P-384</span></span>
- <span data-ttu-id="48f1f-122">P-521</span><span class="sxs-lookup"><span data-stu-id="48f1f-122">P-521</span></span>
- <span data-ttu-id="48f1f-123">P-256K</span><span class="sxs-lookup"><span data-stu-id="48f1f-123">P-256K</span></span>
- <span data-ttu-id="48f1f-124">SECP256K1</span><span class="sxs-lookup"><span data-stu-id="48f1f-124">SECP256K1</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: P-256, P-384, P-521, P-256K, SECP256K1

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48f1f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48f1f-125">-DefaultProfile</span></span>
<span data-ttu-id="48f1f-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="48f1f-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="48f1f-127">-Wyłączone</span><span class="sxs-lookup"><span data-stu-id="48f1f-127">-Disabled</span></span>
<span data-ttu-id="48f1f-128">Wskazuje, że zasada certyfikatu jest wyłączona.</span><span class="sxs-lookup"><span data-stu-id="48f1f-128">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="48f1f-129">-DnsName</span><span class="sxs-lookup"><span data-stu-id="48f1f-129">-DnsName</span></span>
<span data-ttu-id="48f1f-130">Określa nazwy DNS w certyfikacie.</span><span class="sxs-lookup"><span data-stu-id="48f1f-130">Specifies the DNS names in the certificate.</span></span>

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

### <span data-ttu-id="48f1f-131">-Ekus</span><span class="sxs-lookup"><span data-stu-id="48f1f-131">-Ekus</span></span>
<span data-ttu-id="48f1f-132">Określa ulepszone użycie klucza (EKUs) w certyfikacie.</span><span class="sxs-lookup"><span data-stu-id="48f1f-132">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="48f1f-133">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="48f1f-133">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="48f1f-134">Określa, ile dni przed wygaśnięciem rozpocznie się proces powiadomień automatycznych.</span><span class="sxs-lookup"><span data-stu-id="48f1f-134">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="48f1f-135">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="48f1f-135">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="48f1f-136">Określa wartość procentową okresu istnienia, po upływie którego rozpocznie się proces automatycznego powiadomienia.</span><span class="sxs-lookup"><span data-stu-id="48f1f-136">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="48f1f-137">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="48f1f-137">-IssuerName</span></span>
<span data-ttu-id="48f1f-138">Określa nazwę wystawcy certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="48f1f-138">Specifies the name of the issuer for the certificate.</span></span>

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

### <span data-ttu-id="48f1f-139">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="48f1f-139">-KeyNotExportable</span></span>
<span data-ttu-id="48f1f-140">Wskazuje, że nie można eksportować klucza.</span><span class="sxs-lookup"><span data-stu-id="48f1f-140">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="48f1f-141">-Rozmiar czcionki</span><span class="sxs-lookup"><span data-stu-id="48f1f-141">-KeySize</span></span>
<span data-ttu-id="48f1f-142">Określa kluczowy rozmiar certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="48f1f-142">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="48f1f-143">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="48f1f-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="48f1f-144">2048</span><span class="sxs-lookup"><span data-stu-id="48f1f-144">2048</span></span>
- <span data-ttu-id="48f1f-145">3072</span><span class="sxs-lookup"><span data-stu-id="48f1f-145">3072</span></span>
- <span data-ttu-id="48f1f-146">4096</span><span class="sxs-lookup"><span data-stu-id="48f1f-146">4096</span></span>
- <span data-ttu-id="48f1f-147">256</span><span class="sxs-lookup"><span data-stu-id="48f1f-147">256</span></span>
- <span data-ttu-id="48f1f-148">384</span><span class="sxs-lookup"><span data-stu-id="48f1f-148">384</span></span>
- <span data-ttu-id="48f1f-149">521</span><span class="sxs-lookup"><span data-stu-id="48f1f-149">521</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:
Accepted values: 2048, 3072, 4096, 256, 384, 521

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48f1f-150">-KeyType</span><span class="sxs-lookup"><span data-stu-id="48f1f-150">-KeyType</span></span>
<span data-ttu-id="48f1f-151">Określa typ klucza klucza, który wykonuje kopię zapasową certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="48f1f-151">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="48f1f-152">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="48f1f-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="48f1f-153">ALGORYTM</span><span class="sxs-lookup"><span data-stu-id="48f1f-153">RSA</span></span>
- <span data-ttu-id="48f1f-154">RSA — HSM</span><span class="sxs-lookup"><span data-stu-id="48f1f-154">RSA-HSM</span></span>
- <span data-ttu-id="48f1f-155">Wspólnoty</span><span class="sxs-lookup"><span data-stu-id="48f1f-155">EC</span></span>
- <span data-ttu-id="48f1f-156">EC — HSM</span><span class="sxs-lookup"><span data-stu-id="48f1f-156">EC-HSM</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA, RSA-HSM, EC, EC-HSM

Required: False
Position: Named
Default value: RSA
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48f1f-157">-Użycie</span><span class="sxs-lookup"><span data-stu-id="48f1f-157">-KeyUsage</span></span>
<span data-ttu-id="48f1f-158">Określa użycie klucza w certyfikacie.</span><span class="sxs-lookup"><span data-stu-id="48f1f-158">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="48f1f-159">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="48f1f-159">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="48f1f-160">Określa liczbę dni przed wygaśnięciem, po upływie której rozpocznie się proces automatycznego odnawiania certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="48f1f-160">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="48f1f-161">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="48f1f-161">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="48f1f-162">Określa wartość procentową okresu istnienia, po upływie którego rozpocznie się proces automatycznego odnawiania certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="48f1f-162">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="48f1f-163">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="48f1f-163">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="48f1f-164">Wskazuje, że certyfikat jest ponownie używany podczas odnawiania klucza.</span><span class="sxs-lookup"><span data-stu-id="48f1f-164">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="48f1f-165">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="48f1f-165">-SecretContentType</span></span>
<span data-ttu-id="48f1f-166">Określa typ zawartości nowego klucza tajnego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="48f1f-166">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="48f1f-167">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="48f1f-167">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="48f1f-168">application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="48f1f-168">application/x-pkcs12</span></span>
- <span data-ttu-id="48f1f-169">application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="48f1f-169">application/x-pem-file</span></span>

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

### <span data-ttu-id="48f1f-170">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="48f1f-170">-SubjectName</span></span>
<span data-ttu-id="48f1f-171">Określa nazwę podmiotu certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="48f1f-171">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="48f1f-172">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="48f1f-172">-ValidityInMonths</span></span>
<span data-ttu-id="48f1f-173">Określa liczbę miesięcy ważności certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="48f1f-173">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="48f1f-174">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="48f1f-174">-Confirm</span></span>
<span data-ttu-id="48f1f-175">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48f1f-175">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48f1f-176">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48f1f-176">-WhatIf</span></span>
<span data-ttu-id="48f1f-177">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48f1f-177">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48f1f-178">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="48f1f-178">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48f1f-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48f1f-179">CommonParameters</span></span>
<span data-ttu-id="48f1f-180">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48f1f-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48f1f-181">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="48f1f-181">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48f1f-182">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="48f1f-182">INPUTS</span></span>

### <span data-ttu-id="48f1f-183">System. String</span><span class="sxs-lookup"><span data-stu-id="48f1f-183">System.String</span></span>

### <span data-ttu-id="48f1f-184">System. Collections. Generic. list "1 [[System. String; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="48f1f-184">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="48f1f-185">System. Nullable ' 1 [[System. Int32; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="48f1f-185">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="48f1f-186">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="48f1f-186">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="48f1f-187">System. Collections. Generic. list "1 [[System. Security. Kryptografia. x509. X509KeyUsageFlags, system. Security. Kryptografia. x509, Version = 4.2.1.0, Culture = neutral, PublicKeyToken = b03f5f7f11d50a3a]]</span><span class="sxs-lookup"><span data-stu-id="48f1f-187">System.Collections.Generic.List\`1[[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags, System.Security.Cryptography.X509Certificates, Version=4.2.1.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a]]</span></span>

## <span data-ttu-id="48f1f-188">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="48f1f-188">OUTPUTS</span></span>

### <span data-ttu-id="48f1f-189">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="48f1f-189">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="48f1f-190">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="48f1f-190">NOTES</span></span>

## <span data-ttu-id="48f1f-191">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="48f1f-191">RELATED LINKS</span></span>

[<span data-ttu-id="48f1f-192">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="48f1f-192">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="48f1f-193">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="48f1f-193">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

