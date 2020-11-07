---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/set-AzKeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: 160c98b141dbde36786404b58c694772dc86d323
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893014"
---
# <span data-ttu-id="47a5c-101">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="47a5c-101">Set-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="47a5c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="47a5c-102">SYNOPSIS</span></span>
<span data-ttu-id="47a5c-103">Tworzy lub aktualizuje zasady dotyczące certyfikatu w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="47a5c-103">Creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="47a5c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="47a5c-104">SYNTAX</span></span>

### <span data-ttu-id="47a5c-105">Rozwinięty (domyślny)</span><span class="sxs-lookup"><span data-stu-id="47a5c-105">Expanded (Default)</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> [-SecretContentType <String>]
 [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsNames <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>]
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [-KeyNotExportable] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="47a5c-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="47a5c-106">ByValue</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [[-CertificatePolicy] <KeyVaultCertificatePolicy>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47a5c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="47a5c-107">DESCRIPTION</span></span>
<span data-ttu-id="47a5c-108">Polecenie cmdlet **Set-AzKeyVaultCertificatePolicy** służy do tworzenia lub aktualizowania zasad certyfikatu w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="47a5c-108">The **Set-AzKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="47a5c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="47a5c-109">EXAMPLES</span></span>

### <span data-ttu-id="47a5c-110">Przykład 1: Ustawianie zasad certyfikatów</span><span class="sxs-lookup"><span data-stu-id="47a5c-110">Example 1: Set a certificate policy</span></span>
```
PS C:\>Set-AzKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01" -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal $True
```

<span data-ttu-id="47a5c-111">To polecenie ustawia zasady dla certyfikatu TestCert01 w magazynie kluczy ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="47a5c-111">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="47a5c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="47a5c-112">PARAMETERS</span></span>

### <span data-ttu-id="47a5c-113">-CertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="47a5c-113">-CertificatePolicy</span></span>
<span data-ttu-id="47a5c-114">Określa zasady certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="47a5c-114">Specifies the certificate policy.</span></span>

```yaml
Type: KeyVaultCertificatePolicy
Parameter Sets: ByValue
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47a5c-115">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="47a5c-115">-CertificateType</span></span>
<span data-ttu-id="47a5c-116">Określa typ certyfikatu dla emitenta.</span><span class="sxs-lookup"><span data-stu-id="47a5c-116">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47a5c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47a5c-117">-DefaultProfile</span></span>
<span data-ttu-id="47a5c-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="47a5c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47a5c-119">-Wyłączone</span><span class="sxs-lookup"><span data-stu-id="47a5c-119">-Disabled</span></span>
<span data-ttu-id="47a5c-120">Wskazuje, że zasada certyfikatu jest wyłączona.</span><span class="sxs-lookup"><span data-stu-id="47a5c-120">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47a5c-121">-DnsNames</span><span class="sxs-lookup"><span data-stu-id="47a5c-121">-DnsNames</span></span>
<span data-ttu-id="47a5c-122">Określa nazwy DNS w certyfikacie.</span><span class="sxs-lookup"><span data-stu-id="47a5c-122">Specifies the DNS names in the certificate.</span></span>

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

### <span data-ttu-id="47a5c-123">-Ekus</span><span class="sxs-lookup"><span data-stu-id="47a5c-123">-Ekus</span></span>
<span data-ttu-id="47a5c-124">Określa ulepszone użycie klucza (EKUs) w certyfikacie.</span><span class="sxs-lookup"><span data-stu-id="47a5c-124">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="47a5c-125">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="47a5c-125">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="47a5c-126">Określa, ile dni przed wygaśnięciem rozpocznie się proces powiadomień automatycznych.</span><span class="sxs-lookup"><span data-stu-id="47a5c-126">Specifies how many days before expiry the automatic notification process begins.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47a5c-127">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="47a5c-127">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="47a5c-128">Określa wartość procentową okresu istnienia, po upływie którego rozpocznie się proces automatycznego powiadomienia.</span><span class="sxs-lookup"><span data-stu-id="47a5c-128">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47a5c-129">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="47a5c-129">-IssuerName</span></span>
<span data-ttu-id="47a5c-130">Określa nazwę wystawcy dla tego certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="47a5c-130">Specifies the name of the issuer for this certificate.</span></span>

```yaml
Type: String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47a5c-131">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="47a5c-131">-KeyNotExportable</span></span>
<span data-ttu-id="47a5c-132">Wskazuje, że nie można eksportować klucza.</span><span class="sxs-lookup"><span data-stu-id="47a5c-132">Indicates that the key is not exportable.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47a5c-133">-KeyType</span><span class="sxs-lookup"><span data-stu-id="47a5c-133">-KeyType</span></span>
<span data-ttu-id="47a5c-134">Określa typ klucza klucza, który wykonuje kopię zapasową certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="47a5c-134">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="47a5c-135">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="47a5c-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="47a5c-136">ALGORYTM</span><span class="sxs-lookup"><span data-stu-id="47a5c-136">RSA</span></span>
- <span data-ttu-id="47a5c-137">RSA — HSM</span><span class="sxs-lookup"><span data-stu-id="47a5c-137">RSA-HSM</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: RSA, RSA-HSM

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47a5c-138">-Użycie</span><span class="sxs-lookup"><span data-stu-id="47a5c-138">-KeyUsage</span></span>
<span data-ttu-id="47a5c-139">Określa użycie klucza w certyfikacie.</span><span class="sxs-lookup"><span data-stu-id="47a5c-139">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="47a5c-140">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="47a5c-140">-Name</span></span>
<span data-ttu-id="47a5c-141">Określa nazwę certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="47a5c-141">Specifies the name of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47a5c-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="47a5c-142">-PassThru</span></span>
<span data-ttu-id="47a5c-143">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="47a5c-143">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="47a5c-144">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="47a5c-144">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47a5c-145">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="47a5c-145">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="47a5c-146">Określa liczbę dni przed wygaśnięciem, po upływie której rozpocznie się proces automatycznego odnawiania certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="47a5c-146">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: Int32
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47a5c-147">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="47a5c-147">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="47a5c-148">Określa wartość procentową okresu istnienia, po upływie którego rozpocznie się proces automatycznego odnawiania certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="47a5c-148">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: Int32
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47a5c-149">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="47a5c-149">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="47a5c-150">Wskazuje, że certyfikat jest ponownie używany podczas odnawiania klucza.</span><span class="sxs-lookup"><span data-stu-id="47a5c-150">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: Boolean
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47a5c-151">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="47a5c-151">-SecretContentType</span></span>
<span data-ttu-id="47a5c-152">Określa typ zawartości nowego klucza tajnego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="47a5c-152">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="47a5c-153">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="47a5c-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="47a5c-154">application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="47a5c-154">application/x-pkcs12</span></span>
- <span data-ttu-id="47a5c-155">application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="47a5c-155">application/x-pem-file</span></span>

```yaml
Type: String
Parameter Sets: Expanded
Aliases: 
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47a5c-156">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="47a5c-156">-SubjectName</span></span>
<span data-ttu-id="47a5c-157">Określa nazwę podmiotu certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="47a5c-157">Specifies the subject name of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47a5c-158">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="47a5c-158">-ValidityInMonths</span></span>
<span data-ttu-id="47a5c-159">Określa liczbę miesięcy ważności certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="47a5c-159">Specifies the number of months the certificate is valid.</span></span>

```yaml
Type: Int32
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47a5c-160">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="47a5c-160">-VaultName</span></span>
<span data-ttu-id="47a5c-161">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="47a5c-161">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47a5c-162">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="47a5c-162">-Confirm</span></span>
<span data-ttu-id="47a5c-163">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47a5c-163">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47a5c-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47a5c-164">-WhatIf</span></span>
<span data-ttu-id="47a5c-165">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47a5c-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47a5c-166">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="47a5c-166">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47a5c-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47a5c-167">CommonParameters</span></span>
<span data-ttu-id="47a5c-168">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47a5c-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47a5c-169">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47a5c-169">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47a5c-170">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="47a5c-170">INPUTS</span></span>

### <span data-ttu-id="47a5c-171">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="47a5c-171">None</span></span>
<span data-ttu-id="47a5c-172">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="47a5c-172">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="47a5c-173">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="47a5c-173">OUTPUTS</span></span>

### <span data-ttu-id="47a5c-174">Microsoft. Azure. Commands. platforming. models. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="47a5c-174">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="47a5c-175">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="47a5c-175">NOTES</span></span>

## <span data-ttu-id="47a5c-176">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="47a5c-176">RELATED LINKS</span></span>

[<span data-ttu-id="47a5c-177">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="47a5c-177">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="47a5c-178">Nowe — AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="47a5c-178">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

