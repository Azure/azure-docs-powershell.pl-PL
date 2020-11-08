---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: 5a6b88ce85b8b9296d9666955a93d1240b631634
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051508"
---
# <span data-ttu-id="42014-101">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="42014-101">Set-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="42014-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="42014-102">SYNOPSIS</span></span>
<span data-ttu-id="42014-103">Tworzy lub aktualizuje zasady dotyczące certyfikatu w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="42014-103">Creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="42014-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="42014-104">SYNTAX</span></span>

### <span data-ttu-id="42014-105">ExpandedRenewPercentage (domyślny)</span><span class="sxs-lookup"><span data-stu-id="42014-105">ExpandedRenewPercentage (Default)</span></span>
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

### <span data-ttu-id="42014-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="42014-106">ByValue</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-InputObject] <PSKeyVaultCertificatePolicy> [-EmailAtNumberOfDaysBeforeExpiry <Int32>]
 [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>] [-KeySize <Int32>]
 [-CertificateTransparency <Boolean>] [-PassThru] [-Curve <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42014-107">ExpandedRenewNumber</span><span class="sxs-lookup"><span data-stu-id="42014-107">ExpandedRenewNumber</span></span>
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

## <span data-ttu-id="42014-108">Opis</span><span class="sxs-lookup"><span data-stu-id="42014-108">DESCRIPTION</span></span>
<span data-ttu-id="42014-109">Polecenie cmdlet **Set-AzKeyVaultCertificatePolicy** służy do tworzenia lub aktualizowania zasad certyfikatu w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="42014-109">The **Set-AzKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="42014-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="42014-110">EXAMPLES</span></span>

### <span data-ttu-id="42014-111">Przykład 1: Ustawianie zasad certyfikatów</span><span class="sxs-lookup"><span data-stu-id="42014-111">Example 1: Set a certificate policy</span></span>
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

<span data-ttu-id="42014-112">To polecenie ustawia zasady dla certyfikatu TestCert01 w magazynie kluczy ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="42014-112">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="42014-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="42014-113">PARAMETERS</span></span>

### <span data-ttu-id="42014-114">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="42014-114">-CertificateTransparency</span></span>
<span data-ttu-id="42014-115">Wskazuje, czy dla tego certyfikatu/wystawcy jest włączone przezroczystość certyfikatu; Jeśli argument nie jest określony, wartością domyślną jest "prawda"</span><span class="sxs-lookup"><span data-stu-id="42014-115">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'</span></span>

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

### <span data-ttu-id="42014-116">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="42014-116">-CertificateType</span></span>
<span data-ttu-id="42014-117">Określa typ certyfikatu dla emitenta.</span><span class="sxs-lookup"><span data-stu-id="42014-117">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="42014-118">-Krzywa</span><span class="sxs-lookup"><span data-stu-id="42014-118">-Curve</span></span>
<span data-ttu-id="42014-119">Określa nazwę krzywej eliptycznej klucza certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="42014-119">Specifies the elliptic curve name of the key of the certificate.</span></span>
<span data-ttu-id="42014-120">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="42014-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="42014-121">P-256</span><span class="sxs-lookup"><span data-stu-id="42014-121">P-256</span></span>
- <span data-ttu-id="42014-122">P-384</span><span class="sxs-lookup"><span data-stu-id="42014-122">P-384</span></span>
- <span data-ttu-id="42014-123">P-521</span><span class="sxs-lookup"><span data-stu-id="42014-123">P-521</span></span>
- <span data-ttu-id="42014-124">P-256K</span><span class="sxs-lookup"><span data-stu-id="42014-124">P-256K</span></span>
- <span data-ttu-id="42014-125">SECP256K1</span><span class="sxs-lookup"><span data-stu-id="42014-125">SECP256K1</span></span>

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

### <span data-ttu-id="42014-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42014-126">-DefaultProfile</span></span>
<span data-ttu-id="42014-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="42014-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="42014-128">-Wyłączone</span><span class="sxs-lookup"><span data-stu-id="42014-128">-Disabled</span></span>
<span data-ttu-id="42014-129">Wskazuje, że zasada certyfikatu jest wyłączona.</span><span class="sxs-lookup"><span data-stu-id="42014-129">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="42014-130">-DnsName</span><span class="sxs-lookup"><span data-stu-id="42014-130">-DnsName</span></span>
<span data-ttu-id="42014-131">Określa nazwę podmiotu certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="42014-131">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="42014-132">-Ekus</span><span class="sxs-lookup"><span data-stu-id="42014-132">-Ekus</span></span>
<span data-ttu-id="42014-133">Określa ulepszone użycie klucza (EKUs) w certyfikacie.</span><span class="sxs-lookup"><span data-stu-id="42014-133">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="42014-134">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="42014-134">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="42014-135">Określa liczbę dni, po upływie których należy zacząć automatyczne odnawianie.</span><span class="sxs-lookup"><span data-stu-id="42014-135">Specifies the number of days before expiration when automatic renewal should start.</span></span>

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

### <span data-ttu-id="42014-136">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="42014-136">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="42014-137">Określa wartość procentową okresu istnienia, po upływie którego rozpocznie się proces automatycznego powiadomienia.</span><span class="sxs-lookup"><span data-stu-id="42014-137">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="42014-138">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="42014-138">-InputObject</span></span>
<span data-ttu-id="42014-139">Określa zasady certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="42014-139">Specifies the certificate policy.</span></span>

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

### <span data-ttu-id="42014-140">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="42014-140">-IssuerName</span></span>
<span data-ttu-id="42014-141">Określa nazwę wystawcy dla tego certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="42014-141">Specifies the name of the issuer for this certificate.</span></span>

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

### <span data-ttu-id="42014-142">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="42014-142">-KeyNotExportable</span></span>
<span data-ttu-id="42014-143">Wskazuje, że nie można eksportować klucza.</span><span class="sxs-lookup"><span data-stu-id="42014-143">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="42014-144">-Rozmiar czcionki</span><span class="sxs-lookup"><span data-stu-id="42014-144">-KeySize</span></span>
<span data-ttu-id="42014-145">Określa kluczowy rozmiar certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="42014-145">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="42014-146">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="42014-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="42014-147">2048</span><span class="sxs-lookup"><span data-stu-id="42014-147">2048</span></span>
- <span data-ttu-id="42014-148">3072</span><span class="sxs-lookup"><span data-stu-id="42014-148">3072</span></span>
- <span data-ttu-id="42014-149">4096</span><span class="sxs-lookup"><span data-stu-id="42014-149">4096</span></span>
- <span data-ttu-id="42014-150">256</span><span class="sxs-lookup"><span data-stu-id="42014-150">256</span></span>
- <span data-ttu-id="42014-151">384</span><span class="sxs-lookup"><span data-stu-id="42014-151">384</span></span>
- <span data-ttu-id="42014-152">521</span><span class="sxs-lookup"><span data-stu-id="42014-152">521</span></span>

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

### <span data-ttu-id="42014-153">-KeyType</span><span class="sxs-lookup"><span data-stu-id="42014-153">-KeyType</span></span>
<span data-ttu-id="42014-154">Określa typ klucza klucza, który wykonuje kopię zapasową certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="42014-154">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="42014-155">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="42014-155">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="42014-156">ALGORYTM</span><span class="sxs-lookup"><span data-stu-id="42014-156">RSA</span></span>
- <span data-ttu-id="42014-157">RSA — HSM</span><span class="sxs-lookup"><span data-stu-id="42014-157">RSA-HSM</span></span>
- <span data-ttu-id="42014-158">Wspólnoty</span><span class="sxs-lookup"><span data-stu-id="42014-158">EC</span></span>
- <span data-ttu-id="42014-159">EC — HSM</span><span class="sxs-lookup"><span data-stu-id="42014-159">EC-HSM</span></span>

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

### <span data-ttu-id="42014-160">-Użycie</span><span class="sxs-lookup"><span data-stu-id="42014-160">-KeyUsage</span></span>
<span data-ttu-id="42014-161">Określa użycie klucza w certyfikacie.</span><span class="sxs-lookup"><span data-stu-id="42014-161">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="42014-162">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="42014-162">-Name</span></span>
<span data-ttu-id="42014-163">Określa nazwę certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="42014-163">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="42014-164">-PassThru</span><span class="sxs-lookup"><span data-stu-id="42014-164">-PassThru</span></span>
<span data-ttu-id="42014-165">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="42014-165">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="42014-166">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="42014-166">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="42014-167">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="42014-167">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="42014-168">Określa liczbę dni przed wygaśnięciem, po upływie której rozpocznie się proces automatycznego odnawiania certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="42014-168">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="42014-169">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="42014-169">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="42014-170">Określa wartość procentową okresu istnienia, po upływie którego rozpocznie się proces automatycznego odnawiania certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="42014-170">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="42014-171">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="42014-171">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="42014-172">Wskazuje, że certyfikat jest ponownie używany podczas odnawiania klucza.</span><span class="sxs-lookup"><span data-stu-id="42014-172">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="42014-173">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="42014-173">-SecretContentType</span></span>
<span data-ttu-id="42014-174">Określa typ zawartości nowego klucza tajnego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="42014-174">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="42014-175">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="42014-175">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="42014-176">application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="42014-176">application/x-pkcs12</span></span>
- <span data-ttu-id="42014-177">application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="42014-177">application/x-pem-file</span></span>

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

### <span data-ttu-id="42014-178">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="42014-178">-SubjectName</span></span>
<span data-ttu-id="42014-179">Określa nazwę podmiotu certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="42014-179">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="42014-180">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="42014-180">-ValidityInMonths</span></span>
<span data-ttu-id="42014-181">Określa liczbę miesięcy ważności certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="42014-181">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="42014-182">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="42014-182">-VaultName</span></span>
<span data-ttu-id="42014-183">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="42014-183">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="42014-184">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="42014-184">-Confirm</span></span>
<span data-ttu-id="42014-185">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42014-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42014-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42014-186">-WhatIf</span></span>
<span data-ttu-id="42014-187">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42014-187">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42014-188">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="42014-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42014-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42014-189">CommonParameters</span></span>
<span data-ttu-id="42014-190">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42014-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42014-191">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="42014-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42014-192">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="42014-192">INPUTS</span></span>

### <span data-ttu-id="42014-193">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="42014-193">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="42014-194">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="42014-194">OUTPUTS</span></span>

### <span data-ttu-id="42014-195">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="42014-195">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="42014-196">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="42014-196">NOTES</span></span>

## <span data-ttu-id="42014-197">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="42014-197">RELATED LINKS</span></span>

[<span data-ttu-id="42014-198">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="42014-198">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="42014-199">Nowe — AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="42014-199">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

