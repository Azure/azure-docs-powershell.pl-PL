---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: 94f8b6e136925956faf4402b583d80f6a675cca3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553260"
---
# <span data-ttu-id="11eb8-101">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="11eb8-101">Set-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="11eb8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="11eb8-102">SYNOPSIS</span></span>
<span data-ttu-id="11eb8-103">Tworzy lub aktualizuje zasady dotyczące certyfikatu w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="11eb8-103">Creates or updates the policy for a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11eb8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="11eb8-104">SYNTAX</span></span>

### <span data-ttu-id="11eb8-105">Rozwinięty (domyślny)</span><span class="sxs-lookup"><span data-stu-id="11eb8-105">Expanded (Default)</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> [-SecretContentType <String>]
 [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsNames <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>]
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [-KeyNotExportable] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="11eb8-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="11eb8-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [[-CertificatePolicy] <KeyVaultCertificatePolicy>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11eb8-107">Opis</span><span class="sxs-lookup"><span data-stu-id="11eb8-107">DESCRIPTION</span></span>
<span data-ttu-id="11eb8-108">Polecenie cmdlet **Set-AzureKeyVaultCertificatePolicy** służy do tworzenia lub aktualizowania zasad certyfikatu w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="11eb8-108">The **Set-AzureKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="11eb8-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="11eb8-109">EXAMPLES</span></span>

### <span data-ttu-id="11eb8-110">Przykład 1: Ustawianie zasad certyfikatów</span><span class="sxs-lookup"><span data-stu-id="11eb8-110">Example 1: Set a certificate policy</span></span>
```
PS C:\>Set-AzureKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01" -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal $True
```

<span data-ttu-id="11eb8-111">To polecenie ustawia zasady dla certyfikatu TestCert01 w magazynie kluczy ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="11eb8-111">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="11eb8-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="11eb8-112">PARAMETERS</span></span>

### <span data-ttu-id="11eb8-113">-CertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="11eb8-113">-CertificatePolicy</span></span>
<span data-ttu-id="11eb8-114">Określa zasady certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="11eb8-114">Specifies the certificate policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy
Parameter Sets: ByValue
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11eb8-115">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="11eb8-115">-CertificateType</span></span>
<span data-ttu-id="11eb8-116">Określa typ certyfikatu dla emitenta.</span><span class="sxs-lookup"><span data-stu-id="11eb8-116">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11eb8-117">-Wyłączone</span><span class="sxs-lookup"><span data-stu-id="11eb8-117">-Disabled</span></span>
<span data-ttu-id="11eb8-118">Wskazuje, że zasada certyfikatu jest wyłączona.</span><span class="sxs-lookup"><span data-stu-id="11eb8-118">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11eb8-119">-DnsNames</span><span class="sxs-lookup"><span data-stu-id="11eb8-119">-DnsNames</span></span>
<span data-ttu-id="11eb8-120">Określa nazwy DNS w certyfikacie.</span><span class="sxs-lookup"><span data-stu-id="11eb8-120">Specifies the DNS names in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11eb8-121">-Ekus</span><span class="sxs-lookup"><span data-stu-id="11eb8-121">-Ekus</span></span>
<span data-ttu-id="11eb8-122">Określa ulepszone użycie klucza (EKUs) w certyfikacie.</span><span class="sxs-lookup"><span data-stu-id="11eb8-122">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11eb8-123">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="11eb8-123">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="11eb8-124">Określa, ile dni przed wygaśnięciem rozpocznie się proces powiadomień automatycznych.</span><span class="sxs-lookup"><span data-stu-id="11eb8-124">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="11eb8-125">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="11eb8-125">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="11eb8-126">Określa wartość procentową okresu istnienia, po upływie którego rozpocznie się proces automatycznego powiadomienia.</span><span class="sxs-lookup"><span data-stu-id="11eb8-126">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="11eb8-127">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="11eb8-127">-IssuerName</span></span>
<span data-ttu-id="11eb8-128">Określa nazwę wystawcy dla tego certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="11eb8-128">Specifies the name of the issuer for this certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11eb8-129">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="11eb8-129">-KeyNotExportable</span></span>
<span data-ttu-id="11eb8-130">Wskazuje, że nie można eksportować klucza.</span><span class="sxs-lookup"><span data-stu-id="11eb8-130">Indicates that the key is not exportable.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11eb8-131">-KeyType</span><span class="sxs-lookup"><span data-stu-id="11eb8-131">-KeyType</span></span>
<span data-ttu-id="11eb8-132">Określa typ klucza klucza, który wykonuje kopię zapasową certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="11eb8-132">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="11eb8-133">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="11eb8-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="11eb8-134">ALGORYTM</span><span class="sxs-lookup"><span data-stu-id="11eb8-134">RSA</span></span>
- <span data-ttu-id="11eb8-135">RSA — HSM</span><span class="sxs-lookup"><span data-stu-id="11eb8-135">RSA-HSM</span></span>

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

### <span data-ttu-id="11eb8-136">-Użycie</span><span class="sxs-lookup"><span data-stu-id="11eb8-136">-KeyUsage</span></span>
<span data-ttu-id="11eb8-137">Określa użycie klucza w certyfikacie.</span><span class="sxs-lookup"><span data-stu-id="11eb8-137">Specifies the key usages in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11eb8-138">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="11eb8-138">-Name</span></span>
<span data-ttu-id="11eb8-139">Określa nazwę certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="11eb8-139">Specifies the name of the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11eb8-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="11eb8-140">-PassThru</span></span>
<span data-ttu-id="11eb8-141">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="11eb8-141">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="11eb8-142">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="11eb8-142">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="11eb8-143">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="11eb8-143">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="11eb8-144">Określa liczbę dni przed wygaśnięciem, po upływie której rozpocznie się proces automatycznego odnawiania certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="11eb8-144">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11eb8-145">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="11eb8-145">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="11eb8-146">Określa wartość procentową okresu istnienia, po upływie którego rozpocznie się proces automatycznego odnawiania certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="11eb8-146">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11eb8-147">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="11eb8-147">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="11eb8-148">Wskazuje, że certyfikat jest ponownie używany podczas odnawiania klucza.</span><span class="sxs-lookup"><span data-stu-id="11eb8-148">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11eb8-149">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="11eb8-149">-SecretContentType</span></span>
<span data-ttu-id="11eb8-150">Określa typ zawartości nowego klucza tajnego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="11eb8-150">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="11eb8-151">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="11eb8-151">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="11eb8-152">application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="11eb8-152">application/x-pkcs12</span></span>
- <span data-ttu-id="11eb8-153">application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="11eb8-153">application/x-pem-file</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases: 
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11eb8-154">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="11eb8-154">-SubjectName</span></span>
<span data-ttu-id="11eb8-155">Określa nazwę podmiotu certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="11eb8-155">Specifies the subject name of the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11eb8-156">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="11eb8-156">-ValidityInMonths</span></span>
<span data-ttu-id="11eb8-157">Określa liczbę miesięcy ważności certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="11eb8-157">Specifies the number of months the certificate is valid.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11eb8-158">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="11eb8-158">-VaultName</span></span>
<span data-ttu-id="11eb8-159">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="11eb8-159">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11eb8-160">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="11eb8-160">-Confirm</span></span>
<span data-ttu-id="11eb8-161">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11eb8-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11eb8-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11eb8-162">-WhatIf</span></span>
<span data-ttu-id="11eb8-163">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11eb8-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11eb8-164">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="11eb8-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11eb8-165">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11eb8-165">-DefaultProfile</span></span>
<span data-ttu-id="11eb8-166">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="11eb8-166">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11eb8-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11eb8-167">CommonParameters</span></span>
<span data-ttu-id="11eb8-168">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11eb8-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11eb8-169">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11eb8-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11eb8-170">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11eb8-170">INPUTS</span></span>

## <span data-ttu-id="11eb8-171">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="11eb8-171">OUTPUTS</span></span>

### <span data-ttu-id="11eb8-172">Microsoft. Azure. Commands. platforming. models. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="11eb8-172">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="11eb8-173">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="11eb8-173">NOTES</span></span>

## <span data-ttu-id="11eb8-174">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="11eb8-174">RELATED LINKS</span></span>

[<span data-ttu-id="11eb8-175">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="11eb8-175">Get-AzureKeyVaultCertificatePolicy</span></span>](./Get-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="11eb8-176">Nowe — AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="11eb8-176">New-AzureKeyVaultCertificatePolicy</span></span>](./New-AzureKeyVaultCertificatePolicy.md)

