---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: e6ae1be8599869631698ddd886fa09184abfb867
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705114"
---
# <span data-ttu-id="b6658-101">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="b6658-101">Set-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="b6658-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b6658-102">SYNOPSIS</span></span>
<span data-ttu-id="b6658-103">Tworzy lub aktualizuje zasady dotyczące certyfikatu w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="b6658-103">Creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="b6658-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b6658-104">SYNTAX</span></span>

### <span data-ttu-id="b6658-105">ExpandedRenewPercentage (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b6658-105">ExpandedRenewPercentage (Default)</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> [-RenewAtPercentageLifetime <Int32>]
 [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeySize <Int32>] [-KeyType <String>] [-KeyNotExportable] [-CertificateTransparency <Boolean>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6658-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="b6658-106">ByValue</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-InputObject] <PSKeyVaultCertificatePolicy> [-EmailAtNumberOfDaysBeforeExpiry <Int32>]
 [-EmailAtPercentageLifetime <Int32>] [-KeySize <Int32>] [-KeyType <String>] [-CertificateTransparency <Boolean>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6658-107">ExpandedRenewNumber</span><span class="sxs-lookup"><span data-stu-id="b6658-107">ExpandedRenewNumber</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> -RenewAtNumberOfDaysBeforeExpiry <Int32>
 [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeySize <Int32>] [-KeyType <String>] [-KeyNotExportable] [-CertificateTransparency <Boolean>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6658-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b6658-108">DESCRIPTION</span></span>
<span data-ttu-id="b6658-109">Polecenie cmdlet **Set-AzKeyVaultCertificatePolicy** służy do tworzenia lub aktualizowania zasad certyfikatu w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="b6658-109">The **Set-AzKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="b6658-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b6658-110">EXAMPLES</span></span>

### <span data-ttu-id="b6658-111">Przykład 1: Ustawianie zasad certyfikatów</span><span class="sxs-lookup"><span data-stu-id="b6658-111">Example 1: Set a certificate policy</span></span>
```powershell
PS C:\> Set-AzKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01" -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal $True -PassThru

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

<span data-ttu-id="b6658-112">To polecenie ustawia zasady dla certyfikatu TestCert01 w magazynie kluczy ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="b6658-112">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="b6658-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b6658-113">PARAMETERS</span></span>

### <span data-ttu-id="b6658-114">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="b6658-114">-CertificateTransparency</span></span>
<span data-ttu-id="b6658-115">Wskazuje, czy dla tego certyfikatu/wystawcy jest włączone przezroczystość certyfikatu; Jeśli argument nie jest określony, wartością domyślną jest "prawda"</span><span class="sxs-lookup"><span data-stu-id="b6658-115">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'</span></span>

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

### <span data-ttu-id="b6658-116">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="b6658-116">-CertificateType</span></span>
<span data-ttu-id="b6658-117">Określa typ certyfikatu dla emitenta.</span><span class="sxs-lookup"><span data-stu-id="b6658-117">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="b6658-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6658-118">-DefaultProfile</span></span>
<span data-ttu-id="b6658-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b6658-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b6658-120">-Wyłączone</span><span class="sxs-lookup"><span data-stu-id="b6658-120">-Disabled</span></span>
<span data-ttu-id="b6658-121">Wskazuje, że zasada certyfikatu jest wyłączona.</span><span class="sxs-lookup"><span data-stu-id="b6658-121">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="b6658-122">-DnsName</span><span class="sxs-lookup"><span data-stu-id="b6658-122">-DnsName</span></span>
<span data-ttu-id="b6658-123">Określa nazwę podmiotu certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="b6658-123">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="b6658-124">-Ekus</span><span class="sxs-lookup"><span data-stu-id="b6658-124">-Ekus</span></span>
<span data-ttu-id="b6658-125">Określa ulepszone użycie klucza (EKUs) w certyfikacie.</span><span class="sxs-lookup"><span data-stu-id="b6658-125">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="b6658-126">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="b6658-126">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="b6658-127">Określa liczbę dni, po upływie których należy zacząć automatyczne odnawianie.</span><span class="sxs-lookup"><span data-stu-id="b6658-127">Specifies the number of days before expiration when automatic renewal should start.</span></span>

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

### <span data-ttu-id="b6658-128">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="b6658-128">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="b6658-129">Określa wartość procentową okresu istnienia, po upływie którego rozpocznie się proces automatycznego powiadomienia.</span><span class="sxs-lookup"><span data-stu-id="b6658-129">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="b6658-130">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b6658-130">-InputObject</span></span>
<span data-ttu-id="b6658-131">Określa zasady certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="b6658-131">Specifies the certificate policy.</span></span>

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

### <span data-ttu-id="b6658-132">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="b6658-132">-IssuerName</span></span>
<span data-ttu-id="b6658-133">Określa nazwę wystawcy dla tego certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="b6658-133">Specifies the name of the issuer for this certificate.</span></span>

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

### <span data-ttu-id="b6658-134">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="b6658-134">-KeyNotExportable</span></span>
<span data-ttu-id="b6658-135">Wskazuje, że nie można eksportować klucza.</span><span class="sxs-lookup"><span data-stu-id="b6658-135">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="b6658-136">-Rozmiar czcionki</span><span class="sxs-lookup"><span data-stu-id="b6658-136">-KeySize</span></span>
<span data-ttu-id="b6658-137">Określa kluczowy rozmiar certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="b6658-137">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="b6658-138">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="b6658-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b6658-139">2048</span><span class="sxs-lookup"><span data-stu-id="b6658-139">2048</span></span>
- <span data-ttu-id="b6658-140">3072</span><span class="sxs-lookup"><span data-stu-id="b6658-140">3072</span></span>
- <span data-ttu-id="b6658-141">4096</span><span class="sxs-lookup"><span data-stu-id="b6658-141">4096</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:
Accepted values: 2048, 3072, 4096

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6658-142">-KeyType</span><span class="sxs-lookup"><span data-stu-id="b6658-142">-KeyType</span></span>
<span data-ttu-id="b6658-143">Określa typ klucza klucza, który wykonuje kopię zapasową certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="b6658-143">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="b6658-144">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="b6658-144">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b6658-145">ALGORYTM</span><span class="sxs-lookup"><span data-stu-id="b6658-145">RSA</span></span>
- <span data-ttu-id="b6658-146">RSA — HSM</span><span class="sxs-lookup"><span data-stu-id="b6658-146">RSA-HSM</span></span>

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

### <span data-ttu-id="b6658-147">-Użycie</span><span class="sxs-lookup"><span data-stu-id="b6658-147">-KeyUsage</span></span>
<span data-ttu-id="b6658-148">Określa użycie klucza w certyfikacie.</span><span class="sxs-lookup"><span data-stu-id="b6658-148">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="b6658-149">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b6658-149">-Name</span></span>
<span data-ttu-id="b6658-150">Określa nazwę certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="b6658-150">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="b6658-151">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b6658-151">-PassThru</span></span>
<span data-ttu-id="b6658-152">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="b6658-152">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b6658-153">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="b6658-153">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b6658-154">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="b6658-154">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="b6658-155">Określa liczbę dni przed wygaśnięciem, po upływie której rozpocznie się proces automatycznego odnawiania certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="b6658-155">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="b6658-156">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="b6658-156">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="b6658-157">Określa wartość procentową okresu istnienia, po upływie którego rozpocznie się proces automatycznego odnawiania certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="b6658-157">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="b6658-158">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="b6658-158">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="b6658-159">Wskazuje, że certyfikat jest ponownie używany podczas odnawiania klucza.</span><span class="sxs-lookup"><span data-stu-id="b6658-159">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="b6658-160">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="b6658-160">-SecretContentType</span></span>
<span data-ttu-id="b6658-161">Określa typ zawartości nowego klucza tajnego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="b6658-161">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="b6658-162">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="b6658-162">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b6658-163">application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="b6658-163">application/x-pkcs12</span></span>
- <span data-ttu-id="b6658-164">application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="b6658-164">application/x-pem-file</span></span>

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

### <span data-ttu-id="b6658-165">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="b6658-165">-SubjectName</span></span>
<span data-ttu-id="b6658-166">Określa nazwę podmiotu certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="b6658-166">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="b6658-167">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="b6658-167">-ValidityInMonths</span></span>
<span data-ttu-id="b6658-168">Określa liczbę miesięcy ważności certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="b6658-168">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="b6658-169">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="b6658-169">-VaultName</span></span>
<span data-ttu-id="b6658-170">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="b6658-170">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="b6658-171">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b6658-171">-Confirm</span></span>
<span data-ttu-id="b6658-172">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6658-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6658-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6658-173">-WhatIf</span></span>
<span data-ttu-id="b6658-174">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6658-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6658-175">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b6658-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6658-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6658-176">CommonParameters</span></span>
<span data-ttu-id="b6658-177">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6658-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6658-178">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6658-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6658-179">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b6658-179">INPUTS</span></span>

### <span data-ttu-id="b6658-180">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="b6658-180">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="b6658-181">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b6658-181">OUTPUTS</span></span>

### <span data-ttu-id="b6658-182">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="b6658-182">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="b6658-183">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b6658-183">NOTES</span></span>

## <span data-ttu-id="b6658-184">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b6658-184">RELATED LINKS</span></span>

[<span data-ttu-id="b6658-185">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="b6658-185">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="b6658-186">Nowe — AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="b6658-186">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

