---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: 370662b1d24f9b5b71653506be7a3add5a3801f8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304614"
---
# <span data-ttu-id="5deba-101">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="5deba-101">New-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="5deba-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5deba-102">SYNOPSIS</span></span>
<span data-ttu-id="5deba-103">Tworzy obiekt zasad certyfikatu w pamięci.</span><span class="sxs-lookup"><span data-stu-id="5deba-103">Creates an in-memory certificate policy object.</span></span>

## <span data-ttu-id="5deba-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5deba-104">SYNTAX</span></span>

### <span data-ttu-id="5deba-105">SubjectName (wartość domyślna)</span><span class="sxs-lookup"><span data-stu-id="5deba-105">SubjectName (Default)</span></span>
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

### <span data-ttu-id="5deba-106">DNSNames</span><span class="sxs-lookup"><span data-stu-id="5deba-106">DNSNames</span></span>
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

## <span data-ttu-id="5deba-107">Opis</span><span class="sxs-lookup"><span data-stu-id="5deba-107">DESCRIPTION</span></span>
<span data-ttu-id="5deba-108">Polecenie cmdlet **New-AzKeyVaultCertificatePolicy** umożliwia utworzenie obiektu zasad certyfikatu w pamięci dla magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5deba-108">The **New-AzKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="5deba-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5deba-109">EXAMPLES</span></span>

### <span data-ttu-id="5deba-110">Przykład 1: Tworzenie zasad certyfikatów</span><span class="sxs-lookup"><span data-stu-id="5deba-110">Example 1: Create a certificate policy</span></span>
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

<span data-ttu-id="5deba-111">To polecenie tworzy zasady certyfikatów, które są ważne przez sześć miesięcy i odnowią certyfikat za pomocą klucza.</span><span class="sxs-lookup"><span data-stu-id="5deba-111">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

### <span data-ttu-id="5deba-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="5deba-112">Example 2</span></span>

<span data-ttu-id="5deba-113">Tworzy obiekt zasad certyfikatu w pamięci.</span><span class="sxs-lookup"><span data-stu-id="5deba-113">Creates an in-memory certificate policy object.</span></span> <span data-ttu-id="5deba-114">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="5deba-114">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzKeyVaultCertificatePolicy -IssuerName 'Self' -KeyType RSA -RenewAtNumberOfDaysBeforeExpiry <Int32> -SecretContentType application/x-pkcs12 -SubjectName 'CN=contoso.com' -ValidityInMonths 6
```

### <span data-ttu-id="5deba-115">Przykład 3: Tworzenie certyfikatu alternatywnej nazwy podmiotu (lub sieci SAN)</span><span class="sxs-lookup"><span data-stu-id="5deba-115">Example 3: Create a Subject Alternate Name (or SAN) certificate</span></span>

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

<span data-ttu-id="5deba-116">W tym przykładzie jest tworzony certyfikat sieci SAN z trzema nazwami DNS.</span><span class="sxs-lookup"><span data-stu-id="5deba-116">This example creates a SAN certificate with 3 DNS names.</span></span>

## <span data-ttu-id="5deba-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5deba-117">PARAMETERS</span></span>

### <span data-ttu-id="5deba-118">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="5deba-118">-CertificateTransparency</span></span>
<span data-ttu-id="5deba-119">Wskazuje, czy dla tego certyfikatu/wystawcy jest włączone przezroczystość certyfikatu; Jeśli argument nie jest określony, wartością domyślną jest "prawda"</span><span class="sxs-lookup"><span data-stu-id="5deba-119">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'</span></span>

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

### <span data-ttu-id="5deba-120">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="5deba-120">-CertificateType</span></span>
<span data-ttu-id="5deba-121">Określa typ certyfikatu dla emitenta.</span><span class="sxs-lookup"><span data-stu-id="5deba-121">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="5deba-122">-Krzywa</span><span class="sxs-lookup"><span data-stu-id="5deba-122">-Curve</span></span>
<span data-ttu-id="5deba-123">Określa nazwę krzywej eliptycznej klucza certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="5deba-123">Specifies the elliptic curve name of the key of the certificate.</span></span>
<span data-ttu-id="5deba-124">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="5deba-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5deba-125">P-256</span><span class="sxs-lookup"><span data-stu-id="5deba-125">P-256</span></span>
- <span data-ttu-id="5deba-126">P-384</span><span class="sxs-lookup"><span data-stu-id="5deba-126">P-384</span></span>
- <span data-ttu-id="5deba-127">P-521</span><span class="sxs-lookup"><span data-stu-id="5deba-127">P-521</span></span>
- <span data-ttu-id="5deba-128">P-256K</span><span class="sxs-lookup"><span data-stu-id="5deba-128">P-256K</span></span>
- <span data-ttu-id="5deba-129">SECP256K1</span><span class="sxs-lookup"><span data-stu-id="5deba-129">SECP256K1</span></span>

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

### <span data-ttu-id="5deba-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5deba-130">-DefaultProfile</span></span>
<span data-ttu-id="5deba-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="5deba-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5deba-132">-Wyłączone</span><span class="sxs-lookup"><span data-stu-id="5deba-132">-Disabled</span></span>
<span data-ttu-id="5deba-133">Wskazuje, że zasada certyfikatu jest wyłączona.</span><span class="sxs-lookup"><span data-stu-id="5deba-133">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="5deba-134">-DnsName</span><span class="sxs-lookup"><span data-stu-id="5deba-134">-DnsName</span></span>
<span data-ttu-id="5deba-135">Określa nazwy DNS w certyfikacie.</span><span class="sxs-lookup"><span data-stu-id="5deba-135">Specifies the DNS names in the certificate.</span></span> <span data-ttu-id="5deba-136">Alternatywne nazwy podmiotów (San) można określić jako nazwy DNS.</span><span class="sxs-lookup"><span data-stu-id="5deba-136">Subject Alternative Names (SANs) can be specified as DNS names.</span></span>

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

### <span data-ttu-id="5deba-137">-Ekus</span><span class="sxs-lookup"><span data-stu-id="5deba-137">-Ekus</span></span>
<span data-ttu-id="5deba-138">Określa ulepszone użycie klucza (EKUs) w certyfikacie.</span><span class="sxs-lookup"><span data-stu-id="5deba-138">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="5deba-139">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="5deba-139">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="5deba-140">Określa, ile dni przed wygaśnięciem rozpocznie się proces powiadomień automatycznych.</span><span class="sxs-lookup"><span data-stu-id="5deba-140">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="5deba-141">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="5deba-141">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="5deba-142">Określa wartość procentową okresu istnienia, po upływie którego rozpocznie się proces automatycznego powiadomienia.</span><span class="sxs-lookup"><span data-stu-id="5deba-142">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="5deba-143">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="5deba-143">-IssuerName</span></span>
<span data-ttu-id="5deba-144">Określa nazwę wystawcy certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="5deba-144">Specifies the name of the issuer for the certificate.</span></span>

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

### <span data-ttu-id="5deba-145">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="5deba-145">-KeyNotExportable</span></span>
<span data-ttu-id="5deba-146">Wskazuje, że nie można eksportować klucza.</span><span class="sxs-lookup"><span data-stu-id="5deba-146">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="5deba-147">-Rozmiar czcionki</span><span class="sxs-lookup"><span data-stu-id="5deba-147">-KeySize</span></span>
<span data-ttu-id="5deba-148">Określa kluczowy rozmiar certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="5deba-148">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="5deba-149">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="5deba-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5deba-150">2048</span><span class="sxs-lookup"><span data-stu-id="5deba-150">2048</span></span>
- <span data-ttu-id="5deba-151">3072</span><span class="sxs-lookup"><span data-stu-id="5deba-151">3072</span></span>
- <span data-ttu-id="5deba-152">4096</span><span class="sxs-lookup"><span data-stu-id="5deba-152">4096</span></span>
- <span data-ttu-id="5deba-153">256</span><span class="sxs-lookup"><span data-stu-id="5deba-153">256</span></span>
- <span data-ttu-id="5deba-154">384</span><span class="sxs-lookup"><span data-stu-id="5deba-154">384</span></span>
- <span data-ttu-id="5deba-155">521</span><span class="sxs-lookup"><span data-stu-id="5deba-155">521</span></span>

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

### <span data-ttu-id="5deba-156">-KeyType</span><span class="sxs-lookup"><span data-stu-id="5deba-156">-KeyType</span></span>
<span data-ttu-id="5deba-157">Określa typ klucza klucza, który wykonuje kopię zapasową certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="5deba-157">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="5deba-158">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="5deba-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5deba-159">ALGORYTM</span><span class="sxs-lookup"><span data-stu-id="5deba-159">RSA</span></span>
- <span data-ttu-id="5deba-160">RSA — HSM</span><span class="sxs-lookup"><span data-stu-id="5deba-160">RSA-HSM</span></span>
- <span data-ttu-id="5deba-161">Wspólnoty</span><span class="sxs-lookup"><span data-stu-id="5deba-161">EC</span></span>
- <span data-ttu-id="5deba-162">EC — HSM</span><span class="sxs-lookup"><span data-stu-id="5deba-162">EC-HSM</span></span>

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

### <span data-ttu-id="5deba-163">-Użycie</span><span class="sxs-lookup"><span data-stu-id="5deba-163">-KeyUsage</span></span>
<span data-ttu-id="5deba-164">Określa użycie klucza w certyfikacie.</span><span class="sxs-lookup"><span data-stu-id="5deba-164">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="5deba-165">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="5deba-165">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="5deba-166">Określa liczbę dni przed wygaśnięciem, po upływie której rozpocznie się proces automatycznego odnawiania certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="5deba-166">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="5deba-167">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="5deba-167">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="5deba-168">Określa wartość procentową okresu istnienia, po upływie którego rozpocznie się proces automatycznego odnawiania certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="5deba-168">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="5deba-169">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="5deba-169">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="5deba-170">Wskazuje, że certyfikat jest ponownie używany podczas odnawiania klucza.</span><span class="sxs-lookup"><span data-stu-id="5deba-170">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="5deba-171">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="5deba-171">-SecretContentType</span></span>
<span data-ttu-id="5deba-172">Określa typ zawartości nowego klucza tajnego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="5deba-172">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="5deba-173">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="5deba-173">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5deba-174">application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="5deba-174">application/x-pkcs12</span></span>
- <span data-ttu-id="5deba-175">application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="5deba-175">application/x-pem-file</span></span>

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

### <span data-ttu-id="5deba-176">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="5deba-176">-SubjectName</span></span>
<span data-ttu-id="5deba-177">Określa nazwę podmiotu certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="5deba-177">Specifies the subject name of the certificate.</span></span> 

> [!NOTE]
> <span data-ttu-id="5deba-178">Jeśli konieczne jest użycie przecinka (,) lub kropki (.) we właściwości w `SubjectName` parametrze, należy umieścić pole właściwości w cudzysłowie.</span><span class="sxs-lookup"><span data-stu-id="5deba-178">If you must use a comma (,) or a period (.) within a property in the `SubjectName` parameter, you must enclose the property field in quotation marks.</span></span> <span data-ttu-id="5deba-179">Na przykład możesz użyć O = "contoso, Ltd".</span><span class="sxs-lookup"><span data-stu-id="5deba-179">For example, you may use O="Contoso, Ltd."</span></span> <span data-ttu-id="5deba-180">w polu Nazwa organizacji.</span><span class="sxs-lookup"><span data-stu-id="5deba-180">in the Organization Name field.</span></span>

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

### <span data-ttu-id="5deba-181">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="5deba-181">-ValidityInMonths</span></span>
<span data-ttu-id="5deba-182">Określa liczbę miesięcy ważności certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="5deba-182">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="5deba-183">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5deba-183">-Confirm</span></span>
<span data-ttu-id="5deba-184">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5deba-184">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5deba-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5deba-185">-WhatIf</span></span>
<span data-ttu-id="5deba-186">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5deba-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5deba-187">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5deba-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5deba-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5deba-188">CommonParameters</span></span>
<span data-ttu-id="5deba-189">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5deba-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5deba-190">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5deba-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5deba-191">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5deba-191">INPUTS</span></span>

### <span data-ttu-id="5deba-192">System. String</span><span class="sxs-lookup"><span data-stu-id="5deba-192">System.String</span></span>

### <span data-ttu-id="5deba-193">System. Collections. Generic. list "1 [[System. String; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5deba-193">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="5deba-194">System. Nullable ' 1 [[System. Int32; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5deba-194">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="5deba-195">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5deba-195">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="5deba-196">System. Collections. Generic. list "1 [[System. Security. Kryptografia. x509. X509KeyUsageFlags, system. Security. Kryptografia. x509, Version = 4.2.1.0, Culture = neutral, PublicKeyToken = b03f5f7f11d50a3a]]</span><span class="sxs-lookup"><span data-stu-id="5deba-196">System.Collections.Generic.List\`1[[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags, System.Security.Cryptography.X509Certificates, Version=4.2.1.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a]]</span></span>

## <span data-ttu-id="5deba-197">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5deba-197">OUTPUTS</span></span>

### <span data-ttu-id="5deba-198">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="5deba-198">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="5deba-199">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5deba-199">NOTES</span></span>

## <span data-ttu-id="5deba-200">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5deba-200">RELATED LINKS</span></span>

[<span data-ttu-id="5deba-201">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="5deba-201">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="5deba-202">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="5deba-202">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

