---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: 963a7005e95941a644b35a57f80b558f02e2d6a0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220853"
---
# <span data-ttu-id="6a2c1-101">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="6a2c1-101">Set-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="6a2c1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6a2c1-102">SYNOPSIS</span></span>
<span data-ttu-id="6a2c1-103">Tworzy lub aktualizuje zasady dotyczące certyfikatu w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="6a2c1-103">Creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="6a2c1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6a2c1-104">SYNTAX</span></span>

### <span data-ttu-id="6a2c1-105">ExpandedRenewPercentage (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6a2c1-105">ExpandedRenewPercentage (Default)</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> [-RenewAtPercentageLifetime <Int32>]
 [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeySize <Int32>] [-KeyNotExportable] [-CertificateTransparency <Boolean>] [-PassThru]
 [-Curve <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a2c1-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="6a2c1-106">ByValue</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-InputObject] <PSKeyVaultCertificatePolicy> [-EmailAtNumberOfDaysBeforeExpiry <Int32>]
 [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>] [-KeySize <Int32>]
 [-CertificateTransparency <Boolean>] [-PassThru] [-Curve <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a2c1-107">ExpandedRenewNumber</span><span class="sxs-lookup"><span data-stu-id="6a2c1-107">ExpandedRenewNumber</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> -RenewAtNumberOfDaysBeforeExpiry <Int32>
 [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeySize <Int32>] [-KeyNotExportable] [-CertificateTransparency <Boolean>] [-PassThru]
 [-Curve <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a2c1-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6a2c1-108">DESCRIPTION</span></span>
<span data-ttu-id="6a2c1-109">Polecenie cmdlet **Set-AzKeyVaultCertificatePolicy** służy do tworzenia lub aktualizowania zasad certyfikatu w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="6a2c1-109">The **Set-AzKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="6a2c1-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6a2c1-110">EXAMPLES</span></span>

### <span data-ttu-id="6a2c1-111">Przykład 1: Ustawianie zasad certyfikatów</span><span class="sxs-lookup"><span data-stu-id="6a2c1-111">Example 1: Set a certificate policy</span></span>
```powershell
PS C:\> Set-AzKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01" -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal $True -PassThru

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

<span data-ttu-id="6a2c1-112">To polecenie ustawia zasady dla certyfikatu TestCert01 w magazynie kluczy ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="6a2c1-112">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="6a2c1-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6a2c1-113">PARAMETERS</span></span>

### <span data-ttu-id="6a2c1-114">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="6a2c1-114">-CertificateTransparency</span></span>
<span data-ttu-id="6a2c1-115">Wskazuje, czy dla tego certyfikatu/wystawcy jest włączone przezroczystość certyfikatu; Jeśli argument nie jest określony, wartością domyślną jest "prawda".</span><span class="sxs-lookup"><span data-stu-id="6a2c1-115">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'.</span></span>
<span data-ttu-id="6a2c1-116">`-IssuerName` Podczas ustawiania tej właściwości należy określić.</span><span class="sxs-lookup"><span data-stu-id="6a2c1-116">`-IssuerName` needs to be specified when setting this property.</span></span>

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

### <span data-ttu-id="6a2c1-117">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="6a2c1-117">-CertificateType</span></span>
<span data-ttu-id="6a2c1-118">Określa typ certyfikatu dla emitenta.</span><span class="sxs-lookup"><span data-stu-id="6a2c1-118">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="6a2c1-119">-Krzywa</span><span class="sxs-lookup"><span data-stu-id="6a2c1-119">-Curve</span></span>
<span data-ttu-id="6a2c1-120">Określa nazwę krzywej eliptycznej klucza certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="6a2c1-120">Specifies the elliptic curve name of the key of the certificate.</span></span>
<span data-ttu-id="6a2c1-121">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="6a2c1-121">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6a2c1-122">P-256</span><span class="sxs-lookup"><span data-stu-id="6a2c1-122">P-256</span></span>
- <span data-ttu-id="6a2c1-123">P-384</span><span class="sxs-lookup"><span data-stu-id="6a2c1-123">P-384</span></span>
- <span data-ttu-id="6a2c1-124">P-521</span><span class="sxs-lookup"><span data-stu-id="6a2c1-124">P-521</span></span>
- <span data-ttu-id="6a2c1-125">P-256K</span><span class="sxs-lookup"><span data-stu-id="6a2c1-125">P-256K</span></span>
- <span data-ttu-id="6a2c1-126">SECP256K1</span><span class="sxs-lookup"><span data-stu-id="6a2c1-126">SECP256K1</span></span>

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

### <span data-ttu-id="6a2c1-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a2c1-127">-DefaultProfile</span></span>
<span data-ttu-id="6a2c1-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="6a2c1-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6a2c1-129">-Wyłączone</span><span class="sxs-lookup"><span data-stu-id="6a2c1-129">-Disabled</span></span>
<span data-ttu-id="6a2c1-130">Wskazuje, że zasada certyfikatu jest wyłączona.</span><span class="sxs-lookup"><span data-stu-id="6a2c1-130">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="6a2c1-131">-DnsName</span><span class="sxs-lookup"><span data-stu-id="6a2c1-131">-DnsName</span></span>
<span data-ttu-id="6a2c1-132">Określa nazwę podmiotu certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="6a2c1-132">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="6a2c1-133">-Ekus</span><span class="sxs-lookup"><span data-stu-id="6a2c1-133">-Ekus</span></span>
<span data-ttu-id="6a2c1-134">Określa ulepszone użycie klucza (EKUs) w certyfikacie.</span><span class="sxs-lookup"><span data-stu-id="6a2c1-134">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="6a2c1-135">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="6a2c1-135">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="6a2c1-136">Określa liczbę dni, po upływie których należy zacząć automatyczne odnawianie.</span><span class="sxs-lookup"><span data-stu-id="6a2c1-136">Specifies the number of days before expiration when automatic renewal should start.</span></span>

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

### <span data-ttu-id="6a2c1-137">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="6a2c1-137">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="6a2c1-138">Określa wartość procentową okresu istnienia, po upływie którego rozpocznie się proces automatycznego powiadomienia.</span><span class="sxs-lookup"><span data-stu-id="6a2c1-138">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="6a2c1-139">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6a2c1-139">-InputObject</span></span>
<span data-ttu-id="6a2c1-140">Określa zasady certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="6a2c1-140">Specifies the certificate policy.</span></span>

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

### <span data-ttu-id="6a2c1-141">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="6a2c1-141">-IssuerName</span></span>
<span data-ttu-id="6a2c1-142">Określa nazwę wystawcy dla tego certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="6a2c1-142">Specifies the name of the issuer for this certificate.</span></span>

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

### <span data-ttu-id="6a2c1-143">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="6a2c1-143">-KeyNotExportable</span></span>
<span data-ttu-id="6a2c1-144">Wskazuje, że nie można eksportować klucza.</span><span class="sxs-lookup"><span data-stu-id="6a2c1-144">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="6a2c1-145">-Rozmiar czcionki</span><span class="sxs-lookup"><span data-stu-id="6a2c1-145">-KeySize</span></span>
<span data-ttu-id="6a2c1-146">Określa kluczowy rozmiar certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="6a2c1-146">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="6a2c1-147">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="6a2c1-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6a2c1-148">2048</span><span class="sxs-lookup"><span data-stu-id="6a2c1-148">2048</span></span>
- <span data-ttu-id="6a2c1-149">3072</span><span class="sxs-lookup"><span data-stu-id="6a2c1-149">3072</span></span>
- <span data-ttu-id="6a2c1-150">4096</span><span class="sxs-lookup"><span data-stu-id="6a2c1-150">4096</span></span>
- <span data-ttu-id="6a2c1-151">256</span><span class="sxs-lookup"><span data-stu-id="6a2c1-151">256</span></span>
- <span data-ttu-id="6a2c1-152">384</span><span class="sxs-lookup"><span data-stu-id="6a2c1-152">384</span></span>
- <span data-ttu-id="6a2c1-153">521</span><span class="sxs-lookup"><span data-stu-id="6a2c1-153">521</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:
Accepted values: 2048, 3072, 4096, 256, 384, 521

Required: False
Position: Named
Default value: 2048
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a2c1-154">-KeyType</span><span class="sxs-lookup"><span data-stu-id="6a2c1-154">-KeyType</span></span>
<span data-ttu-id="6a2c1-155">Określa typ klucza klucza, który wykonuje kopię zapasową certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="6a2c1-155">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="6a2c1-156">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="6a2c1-156">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6a2c1-157">ALGORYTM</span><span class="sxs-lookup"><span data-stu-id="6a2c1-157">RSA</span></span>
- <span data-ttu-id="6a2c1-158">RSA — HSM</span><span class="sxs-lookup"><span data-stu-id="6a2c1-158">RSA-HSM</span></span>
- <span data-ttu-id="6a2c1-159">Wspólnoty</span><span class="sxs-lookup"><span data-stu-id="6a2c1-159">EC</span></span>
- <span data-ttu-id="6a2c1-160">EC — HSM</span><span class="sxs-lookup"><span data-stu-id="6a2c1-160">EC-HSM</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA, RSA-HSM, EC, EC-HSM

Required: False
Position: Named
Default value: RSA
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a2c1-161">-Użycie</span><span class="sxs-lookup"><span data-stu-id="6a2c1-161">-KeyUsage</span></span>
<span data-ttu-id="6a2c1-162">Określa użycie klucza w certyfikacie.</span><span class="sxs-lookup"><span data-stu-id="6a2c1-162">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="6a2c1-163">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6a2c1-163">-Name</span></span>
<span data-ttu-id="6a2c1-164">Określa nazwę certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="6a2c1-164">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="6a2c1-165">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6a2c1-165">-PassThru</span></span>
<span data-ttu-id="6a2c1-166">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="6a2c1-166">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6a2c1-167">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="6a2c1-167">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6a2c1-168">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="6a2c1-168">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="6a2c1-169">Określa liczbę dni przed wygaśnięciem, po upływie której rozpocznie się proces automatycznego odnawiania certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="6a2c1-169">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="6a2c1-170">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="6a2c1-170">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="6a2c1-171">Określa wartość procentową okresu istnienia, po upływie którego rozpocznie się proces automatycznego odnawiania certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="6a2c1-171">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="6a2c1-172">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="6a2c1-172">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="6a2c1-173">Wskazuje, że certyfikat jest ponownie używany podczas odnawiania klucza.</span><span class="sxs-lookup"><span data-stu-id="6a2c1-173">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="6a2c1-174">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="6a2c1-174">-SecretContentType</span></span>
<span data-ttu-id="6a2c1-175">Określa typ zawartości nowego klucza tajnego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="6a2c1-175">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="6a2c1-176">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="6a2c1-176">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6a2c1-177">application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="6a2c1-177">application/x-pkcs12</span></span>
- <span data-ttu-id="6a2c1-178">application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="6a2c1-178">application/x-pem-file</span></span>

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

### <span data-ttu-id="6a2c1-179">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="6a2c1-179">-SubjectName</span></span>
<span data-ttu-id="6a2c1-180">Określa nazwę podmiotu certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="6a2c1-180">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="6a2c1-181">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="6a2c1-181">-ValidityInMonths</span></span>
<span data-ttu-id="6a2c1-182">Określa liczbę miesięcy ważności certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="6a2c1-182">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="6a2c1-183">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="6a2c1-183">-VaultName</span></span>
<span data-ttu-id="6a2c1-184">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="6a2c1-184">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="6a2c1-185">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6a2c1-185">-Confirm</span></span>
<span data-ttu-id="6a2c1-186">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a2c1-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a2c1-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a2c1-187">-WhatIf</span></span>
<span data-ttu-id="6a2c1-188">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a2c1-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a2c1-189">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6a2c1-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a2c1-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a2c1-190">CommonParameters</span></span>
<span data-ttu-id="6a2c1-191">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a2c1-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a2c1-192">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6a2c1-192">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a2c1-193">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6a2c1-193">INPUTS</span></span>

### <span data-ttu-id="6a2c1-194">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="6a2c1-194">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="6a2c1-195">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6a2c1-195">OUTPUTS</span></span>

### <span data-ttu-id="6a2c1-196">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="6a2c1-196">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="6a2c1-197">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6a2c1-197">NOTES</span></span>

## <span data-ttu-id="6a2c1-198">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6a2c1-198">RELATED LINKS</span></span>

[<span data-ttu-id="6a2c1-199">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="6a2c1-199">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="6a2c1-200">Nowe — AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="6a2c1-200">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

