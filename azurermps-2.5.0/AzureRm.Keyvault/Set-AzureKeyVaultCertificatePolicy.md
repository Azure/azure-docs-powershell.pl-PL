---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultcertificatepolicy
schema: 2.0.0
ms.openlocfilehash: 7a9356952f2ea8b4113f5df0fe364e9647e2c733
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898741"
---
# <span data-ttu-id="1b554-101">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="1b554-101">Set-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="1b554-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1b554-102">SYNOPSIS</span></span>
<span data-ttu-id="1b554-103">Tworzy lub aktualizuje zasady dotyczące certyfikatu w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="1b554-103">Creates or updates the policy for a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b554-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1b554-104">SYNTAX</span></span>

### <span data-ttu-id="1b554-105">Rozwinięty (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1b554-105">Expanded (Default)</span></span>
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

### <span data-ttu-id="1b554-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="1b554-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [[-CertificatePolicy] <KeyVaultCertificatePolicy>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b554-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1b554-107">DESCRIPTION</span></span>
<span data-ttu-id="1b554-108">Polecenie cmdlet **Set-AzureKeyVaultCertificatePolicy** służy do tworzenia lub aktualizowania zasad certyfikatu w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="1b554-108">The **Set-AzureKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="1b554-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1b554-109">EXAMPLES</span></span>

### <span data-ttu-id="1b554-110">Przykład 1: Ustawianie zasad certyfikatów</span><span class="sxs-lookup"><span data-stu-id="1b554-110">Example 1: Set a certificate policy</span></span>
```
PS C:\>Set-AzureKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01" -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal $True
```

<span data-ttu-id="1b554-111">To polecenie ustawia zasady dla certyfikatu TestCert01 w magazynie kluczy ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="1b554-111">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="1b554-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1b554-112">PARAMETERS</span></span>

### <span data-ttu-id="1b554-113">-CertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="1b554-113">-CertificatePolicy</span></span>
<span data-ttu-id="1b554-114">Określa zasady certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="1b554-114">Specifies the certificate policy.</span></span>

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

### <span data-ttu-id="1b554-115">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="1b554-115">-CertificateType</span></span>
<span data-ttu-id="1b554-116">Określa typ certyfikatu dla emitenta.</span><span class="sxs-lookup"><span data-stu-id="1b554-116">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="1b554-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b554-117">-DefaultProfile</span></span>
<span data-ttu-id="1b554-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="1b554-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b554-119">-Wyłączone</span><span class="sxs-lookup"><span data-stu-id="1b554-119">-Disabled</span></span>
<span data-ttu-id="1b554-120">Wskazuje, że zasada certyfikatu jest wyłączona.</span><span class="sxs-lookup"><span data-stu-id="1b554-120">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="1b554-121">-DnsNames</span><span class="sxs-lookup"><span data-stu-id="1b554-121">-DnsNames</span></span>
<span data-ttu-id="1b554-122">Określa nazwy DNS w certyfikacie.</span><span class="sxs-lookup"><span data-stu-id="1b554-122">Specifies the DNS names in the certificate.</span></span>

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

### <span data-ttu-id="1b554-123">-Ekus</span><span class="sxs-lookup"><span data-stu-id="1b554-123">-Ekus</span></span>
<span data-ttu-id="1b554-124">Określa ulepszone użycie klucza (EKUs) w certyfikacie.</span><span class="sxs-lookup"><span data-stu-id="1b554-124">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="1b554-125">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="1b554-125">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="1b554-126">Określa, ile dni przed wygaśnięciem rozpocznie się proces powiadomień automatycznych.</span><span class="sxs-lookup"><span data-stu-id="1b554-126">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="1b554-127">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="1b554-127">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="1b554-128">Określa wartość procentową okresu istnienia, po upływie którego rozpocznie się proces automatycznego powiadomienia.</span><span class="sxs-lookup"><span data-stu-id="1b554-128">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="1b554-129">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="1b554-129">-IssuerName</span></span>
<span data-ttu-id="1b554-130">Określa nazwę wystawcy dla tego certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="1b554-130">Specifies the name of the issuer for this certificate.</span></span>

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

### <span data-ttu-id="1b554-131">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="1b554-131">-KeyNotExportable</span></span>
<span data-ttu-id="1b554-132">Wskazuje, że nie można eksportować klucza.</span><span class="sxs-lookup"><span data-stu-id="1b554-132">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="1b554-133">-KeyType</span><span class="sxs-lookup"><span data-stu-id="1b554-133">-KeyType</span></span>
<span data-ttu-id="1b554-134">Określa typ klucza klucza, który wykonuje kopię zapasową certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="1b554-134">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="1b554-135">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="1b554-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1b554-136">ALGORYTM</span><span class="sxs-lookup"><span data-stu-id="1b554-136">RSA</span></span>
- <span data-ttu-id="1b554-137">RSA — HSM</span><span class="sxs-lookup"><span data-stu-id="1b554-137">RSA-HSM</span></span>

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

### <span data-ttu-id="1b554-138">-Użycie</span><span class="sxs-lookup"><span data-stu-id="1b554-138">-KeyUsage</span></span>
<span data-ttu-id="1b554-139">Określa użycie klucza w certyfikacie.</span><span class="sxs-lookup"><span data-stu-id="1b554-139">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="1b554-140">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1b554-140">-Name</span></span>
<span data-ttu-id="1b554-141">Określa nazwę certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="1b554-141">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="1b554-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1b554-142">-PassThru</span></span>
<span data-ttu-id="1b554-143">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="1b554-143">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1b554-144">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="1b554-144">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1b554-145">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="1b554-145">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="1b554-146">Określa liczbę dni przed wygaśnięciem, po upływie której rozpocznie się proces automatycznego odnawiania certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="1b554-146">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="1b554-147">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="1b554-147">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="1b554-148">Określa wartość procentową okresu istnienia, po upływie którego rozpocznie się proces automatycznego odnawiania certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="1b554-148">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="1b554-149">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="1b554-149">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="1b554-150">Wskazuje, że certyfikat jest ponownie używany podczas odnawiania klucza.</span><span class="sxs-lookup"><span data-stu-id="1b554-150">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="1b554-151">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="1b554-151">-SecretContentType</span></span>
<span data-ttu-id="1b554-152">Określa typ zawartości nowego klucza tajnego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="1b554-152">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="1b554-153">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="1b554-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1b554-154">application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="1b554-154">application/x-pkcs12</span></span>
- <span data-ttu-id="1b554-155">application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="1b554-155">application/x-pem-file</span></span>

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

### <span data-ttu-id="1b554-156">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="1b554-156">-SubjectName</span></span>
<span data-ttu-id="1b554-157">Określa nazwę podmiotu certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="1b554-157">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="1b554-158">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="1b554-158">-ValidityInMonths</span></span>
<span data-ttu-id="1b554-159">Określa liczbę miesięcy ważności certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="1b554-159">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="1b554-160">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="1b554-160">-VaultName</span></span>
<span data-ttu-id="1b554-161">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="1b554-161">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="1b554-162">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1b554-162">-Confirm</span></span>
<span data-ttu-id="1b554-163">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b554-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b554-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b554-164">-WhatIf</span></span>
<span data-ttu-id="1b554-165">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b554-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b554-166">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1b554-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b554-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b554-167">CommonParameters</span></span>
<span data-ttu-id="1b554-168">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b554-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b554-169">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b554-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b554-170">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1b554-170">INPUTS</span></span>

## <span data-ttu-id="1b554-171">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1b554-171">OUTPUTS</span></span>

### <span data-ttu-id="1b554-172">Microsoft. Azure. Commands. platforming. models. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="1b554-172">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="1b554-173">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1b554-173">NOTES</span></span>

## <span data-ttu-id="1b554-174">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1b554-174">RELATED LINKS</span></span>

[<span data-ttu-id="1b554-175">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="1b554-175">Get-AzureKeyVaultCertificatePolicy</span></span>](./Get-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="1b554-176">Nowe — AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="1b554-176">New-AzureKeyVaultCertificatePolicy</span></span>](./New-AzureKeyVaultCertificatePolicy.md)

