---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/powershell/module/az.keyvault/new-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: af35cef768c668663b68cfd4a21e473109883aec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001313"
---
# <span data-ttu-id="8f352-101">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="8f352-101">New-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="8f352-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f352-102">SYNOPSIS</span></span>
<span data-ttu-id="8f352-103">Tworzy obiekt zasad certyfikatu w pamięci.</span><span class="sxs-lookup"><span data-stu-id="8f352-103">Creates an in-memory certificate policy object.</span></span>

## <span data-ttu-id="8f352-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8f352-104">SYNTAX</span></span>

### <span data-ttu-id="8f352-105">SubjectName (Default)</span><span class="sxs-lookup"><span data-stu-id="8f352-105">SubjectName (Default)</span></span>
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

### <span data-ttu-id="8f352-106">DNSNames</span><span class="sxs-lookup"><span data-stu-id="8f352-106">DNSNames</span></span>
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

## <span data-ttu-id="8f352-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="8f352-107">DESCRIPTION</span></span>
<span data-ttu-id="8f352-108">Polecenie **cmdlet New-AzKeyVaultCertificatePolicy** tworzy obiekt zasad certyfikatu w pamięci dla magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8f352-108">The **New-AzKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="8f352-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8f352-109">EXAMPLES</span></span>

### <span data-ttu-id="8f352-110">Przykład 1. Tworzenie zasad certyfikatu</span><span class="sxs-lookup"><span data-stu-id="8f352-110">Example 1: Create a certificate policy</span></span>
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

<span data-ttu-id="8f352-111">To polecenie tworzy zasady certyfikatu, które są ważne sześć miesięcy i są ponownie używane do odnawiania certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="8f352-111">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

### <span data-ttu-id="8f352-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="8f352-112">Example 2</span></span>

<span data-ttu-id="8f352-113">Tworzy obiekt zasad certyfikatu w pamięci.</span><span class="sxs-lookup"><span data-stu-id="8f352-113">Creates an in-memory certificate policy object.</span></span> <span data-ttu-id="8f352-114">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="8f352-114">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzKeyVaultCertificatePolicy -IssuerName 'Self' -KeyType RSA -RenewAtNumberOfDaysBeforeExpiry <Int32> -SecretContentType application/x-pkcs12 -SubjectName 'CN=contoso.com' -ValidityInMonths 6
```

### <span data-ttu-id="8f352-115">Przykład 3. Tworzenie certyfikatu alternatywnej nazwy podmiotu (SAN)</span><span class="sxs-lookup"><span data-stu-id="8f352-115">Example 3: Create a Subject Alternate Name (or SAN) certificate</span></span>

```powershell
PS C:\> New-AzKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -DnsName "contoso.com","support.contoso.com","docs.contoso.com" -IssuerName "Self"

SecretContentType               : application/x-pkcs12
Kty                             : RSA
KeySize                         : 2048
Curve                           :
Exportable                      :
ReuseKeyOnRenewal               : False
SubjectName                     : CN=contoso.com
DnsNames                        : {contoso.com, support.contoso.com, docs.contoso.com}
KeyUsage                        :
Ekus                            :
ValidityInMonths                :
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

<span data-ttu-id="8f352-116">W tym przykładzie jest tworzyny certyfikat SAN z 3 nazwami DNS.</span><span class="sxs-lookup"><span data-stu-id="8f352-116">This example creates a SAN certificate with 3 DNS names.</span></span>

## <span data-ttu-id="8f352-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8f352-117">PARAMETERS</span></span>

### <span data-ttu-id="8f352-118">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="8f352-118">-CertificateTransparency</span></span>
<span data-ttu-id="8f352-119">Wskazuje, czy dla tego certyfikatu/wystawcy włączono przezroczystość certyfikatu; jeśli nie zostanie określone, wartością domyślną jest "true"</span><span class="sxs-lookup"><span data-stu-id="8f352-119">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'</span></span>

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

### <span data-ttu-id="8f352-120">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="8f352-120">-CertificateType</span></span>
<span data-ttu-id="8f352-121">Określa typ certyfikatu wystawcy.</span><span class="sxs-lookup"><span data-stu-id="8f352-121">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="8f352-122">— Krzywa</span><span class="sxs-lookup"><span data-stu-id="8f352-122">-Curve</span></span>
<span data-ttu-id="8f352-123">Określa nazwę krzywej wielokropka klucza certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="8f352-123">Specifies the elliptic curve name of the key of the certificate.</span></span>
<span data-ttu-id="8f352-124">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="8f352-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8f352-125">P-256</span><span class="sxs-lookup"><span data-stu-id="8f352-125">P-256</span></span>
- <span data-ttu-id="8f352-126">P-384</span><span class="sxs-lookup"><span data-stu-id="8f352-126">P-384</span></span>
- <span data-ttu-id="8f352-127">P-521</span><span class="sxs-lookup"><span data-stu-id="8f352-127">P-521</span></span>
- <span data-ttu-id="8f352-128">P-256K</span><span class="sxs-lookup"><span data-stu-id="8f352-128">P-256K</span></span>
- <span data-ttu-id="8f352-129">SECP256K1</span><span class="sxs-lookup"><span data-stu-id="8f352-129">SECP256K1</span></span>

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

### <span data-ttu-id="8f352-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f352-130">-DefaultProfile</span></span>
<span data-ttu-id="8f352-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="8f352-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8f352-132">— Wyłączone</span><span class="sxs-lookup"><span data-stu-id="8f352-132">-Disabled</span></span>
<span data-ttu-id="8f352-133">Oznacza, że zasady certyfikatów są wyłączone.</span><span class="sxs-lookup"><span data-stu-id="8f352-133">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="8f352-134">-DnsName</span><span class="sxs-lookup"><span data-stu-id="8f352-134">-DnsName</span></span>
<span data-ttu-id="8f352-135">Określa nazwy DNS w certyfikacie.</span><span class="sxs-lookup"><span data-stu-id="8f352-135">Specifies the DNS names in the certificate.</span></span> <span data-ttu-id="8f352-136">Nazwy alternatywne tematu (SAN) można określić jako nazwy DNS.</span><span class="sxs-lookup"><span data-stu-id="8f352-136">Subject Alternative Names (SANs) can be specified as DNS names.</span></span>

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

### <span data-ttu-id="8f352-137">-Ekus</span><span class="sxs-lookup"><span data-stu-id="8f352-137">-Ekus</span></span>
<span data-ttu-id="8f352-138">Określa rozszerzone użycie kluczy (EKU) w certyfikacie.</span><span class="sxs-lookup"><span data-stu-id="8f352-138">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="8f352-139">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="8f352-139">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="8f352-140">Określa, ile dni przed wygaśnięciem rozpoczyna się proces automatycznego powiadamiania.</span><span class="sxs-lookup"><span data-stu-id="8f352-140">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="8f352-141">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="8f352-141">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="8f352-142">Określa procent okresu istnienia, po którym rozpoczyna się automatyczny proces powiadamiania.</span><span class="sxs-lookup"><span data-stu-id="8f352-142">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="8f352-143">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="8f352-143">-IssuerName</span></span>
<span data-ttu-id="8f352-144">Określa nazwę wystawcy certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="8f352-144">Specifies the name of the issuer for the certificate.</span></span>

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

### <span data-ttu-id="8f352-145">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="8f352-145">-KeyNotExportable</span></span>
<span data-ttu-id="8f352-146">Wskazuje, że klucza nie można wyeksportować.</span><span class="sxs-lookup"><span data-stu-id="8f352-146">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="8f352-147">-KeySize</span><span class="sxs-lookup"><span data-stu-id="8f352-147">-KeySize</span></span>
<span data-ttu-id="8f352-148">Określa rozmiar klucza certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="8f352-148">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="8f352-149">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="8f352-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8f352-150">2048</span><span class="sxs-lookup"><span data-stu-id="8f352-150">2048</span></span>
- <span data-ttu-id="8f352-151">3072</span><span class="sxs-lookup"><span data-stu-id="8f352-151">3072</span></span>
- <span data-ttu-id="8f352-152">4096</span><span class="sxs-lookup"><span data-stu-id="8f352-152">4096</span></span>
- <span data-ttu-id="8f352-153">256</span><span class="sxs-lookup"><span data-stu-id="8f352-153">256</span></span>
- <span data-ttu-id="8f352-154">384</span><span class="sxs-lookup"><span data-stu-id="8f352-154">384</span></span>
- <span data-ttu-id="8f352-155">521</span><span class="sxs-lookup"><span data-stu-id="8f352-155">521</span></span>

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

### <span data-ttu-id="8f352-156">-KeyType</span><span class="sxs-lookup"><span data-stu-id="8f352-156">-KeyType</span></span>
<span data-ttu-id="8f352-157">Określa typ klucza, który będzie kopią zapasową certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="8f352-157">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="8f352-158">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="8f352-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8f352-159">RSA</span><span class="sxs-lookup"><span data-stu-id="8f352-159">RSA</span></span>
- <span data-ttu-id="8f352-160">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="8f352-160">RSA-HSM</span></span>
- <span data-ttu-id="8f352-161">EC</span><span class="sxs-lookup"><span data-stu-id="8f352-161">EC</span></span>
- <span data-ttu-id="8f352-162">EC-HSM</span><span class="sxs-lookup"><span data-stu-id="8f352-162">EC-HSM</span></span>

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

### <span data-ttu-id="8f352-163">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="8f352-163">-KeyUsage</span></span>
<span data-ttu-id="8f352-164">Określa użycie klucza w certyfikacie.</span><span class="sxs-lookup"><span data-stu-id="8f352-164">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="8f352-165">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="8f352-165">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="8f352-166">Określa liczbę dni przed datą wygaśnięcia, po upływie której rozpocznie się automatyczny proces odnawiania certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="8f352-166">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="8f352-167">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="8f352-167">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="8f352-168">Określa procent okresu istnienia, po którym rozpocznie się automatyczny proces odnawiania certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="8f352-168">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="8f352-169">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="8f352-169">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="8f352-170">Wskazuje, że certyfikat może być ponownie użyty podczas odnawiania.</span><span class="sxs-lookup"><span data-stu-id="8f352-170">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="8f352-171">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="8f352-171">-SecretContentType</span></span>
<span data-ttu-id="8f352-172">Określa typ zawartości nowego magazynu kluczy— klucza tajnego.</span><span class="sxs-lookup"><span data-stu-id="8f352-172">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="8f352-173">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="8f352-173">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8f352-174">application/x-pkcs12</span><span class="sxs-lookup"><span data-stu-id="8f352-174">application/x-pkcs12</span></span>
- <span data-ttu-id="8f352-175">application/x-pem-file</span><span class="sxs-lookup"><span data-stu-id="8f352-175">application/x-pem-file</span></span>

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

### <span data-ttu-id="8f352-176">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="8f352-176">-SubjectName</span></span>
<span data-ttu-id="8f352-177">Określa nazwę podmiotu certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="8f352-177">Specifies the subject name of the certificate.</span></span> 

> [!NOTE]
> <span data-ttu-id="8f352-178">Jeśli w parametrze należy użyć przecinka (;) lub przecinka (.), należy ująć pole właściwości w `SubjectName` cudzysłów.</span><span class="sxs-lookup"><span data-stu-id="8f352-178">If you must use a comma (,) or a period (.) within a property in the `SubjectName` parameter, you must enclose the property field in quotation marks.</span></span> <span data-ttu-id="8f352-179">Na przykład możesz użyć O="Contoso, Ltd".</span><span class="sxs-lookup"><span data-stu-id="8f352-179">For example, you may use O="Contoso, Ltd."</span></span> <span data-ttu-id="8f352-180">w polu Nazwa organizacji.</span><span class="sxs-lookup"><span data-stu-id="8f352-180">in the Organization Name field.</span></span>

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

### <span data-ttu-id="8f352-181">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="8f352-181">-ValidityInMonths</span></span>
<span data-ttu-id="8f352-182">Określa liczbę miesięcy, przez które certyfikat jest ważny.</span><span class="sxs-lookup"><span data-stu-id="8f352-182">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="8f352-183">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8f352-183">-Confirm</span></span>
<span data-ttu-id="8f352-184">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8f352-184">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f352-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f352-185">-WhatIf</span></span>
<span data-ttu-id="8f352-186">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f352-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f352-187">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8f352-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f352-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f352-188">CommonParameters</span></span>
<span data-ttu-id="8f352-189">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f352-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f352-190">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8f352-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f352-191">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8f352-191">INPUTS</span></span>

### <span data-ttu-id="8f352-192">System.String</span><span class="sxs-lookup"><span data-stu-id="8f352-192">System.String</span></span>

### <span data-ttu-id="8f352-193">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8f352-193">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8f352-194">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8f352-194">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8f352-195">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="8f352-195">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="8f352-196">System.Collections.Generic.List'1[[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags, System.Security.Cryptography.X509Certificates, Version=4.2.1.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a]]</span><span class="sxs-lookup"><span data-stu-id="8f352-196">System.Collections.Generic.List\`1[[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags, System.Security.Cryptography.X509Certificates, Version=4.2.1.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a]]</span></span>

## <span data-ttu-id="8f352-197">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8f352-197">OUTPUTS</span></span>

### <span data-ttu-id="8f352-198">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="8f352-198">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="8f352-199">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8f352-199">NOTES</span></span>

## <span data-ttu-id="8f352-200">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8f352-200">RELATED LINKS</span></span>

[<span data-ttu-id="8f352-201">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="8f352-201">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="8f352-202">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="8f352-202">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

