---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/new-azurekeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: caa0961c1b7aebd5fd2f9883831d733a0fa69f1b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551723"
---
# <span data-ttu-id="80da1-101">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="80da1-101">New-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="80da1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="80da1-102">SYNOPSIS</span></span>
<span data-ttu-id="80da1-103">Tworzy obiekt zasad certyfikatu w pamięci.</span><span class="sxs-lookup"><span data-stu-id="80da1-103">Creates an in-memory certificate policy object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80da1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="80da1-104">SYNTAX</span></span>

### <span data-ttu-id="80da1-105">SubjectName (wartość domyślna)</span><span class="sxs-lookup"><span data-stu-id="80da1-105">SubjectName (Default)</span></span>
```
New-AzureKeyVaultCertificatePolicy [-IssuerName] <String> [-SubjectName] <String>
 [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>]
 [-ReuseKeyOnRenewal] [-Disabled] [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="80da1-106">DNSNames</span><span class="sxs-lookup"><span data-stu-id="80da1-106">DNSNames</span></span>
```
New-AzureKeyVaultCertificatePolicy [-IssuerName] <String> [[-SubjectName] <String>]
 [-DnsName] <System.Collections.Generic.List`1[System.String]> [-RenewAtNumberOfDaysBeforeExpiry <Int32>]
 [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>] [-ReuseKeyOnRenewal] [-Disabled]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="80da1-107">Opis</span><span class="sxs-lookup"><span data-stu-id="80da1-107">DESCRIPTION</span></span>
<span data-ttu-id="80da1-108">Polecenie cmdlet **New-AzureKeyVaultCertificatePolicy** umożliwia utworzenie obiektu zasad certyfikatu w pamięci dla magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="80da1-108">The **New-AzureKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="80da1-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="80da1-109">EXAMPLES</span></span>

### <span data-ttu-id="80da1-110">Przykład 1: Tworzenie zasad certyfikatów</span><span class="sxs-lookup"><span data-stu-id="80da1-110">Example 1: Create a certificate policy</span></span>
```
PS C:\>New-AzureKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal
```

<span data-ttu-id="80da1-111">To polecenie tworzy zasady certyfikatów, które są ważne przez sześć miesięcy i odnowią certyfikat za pomocą klucza.</span><span class="sxs-lookup"><span data-stu-id="80da1-111">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

## <span data-ttu-id="80da1-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="80da1-112">PARAMETERS</span></span>

### <span data-ttu-id="80da1-113">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="80da1-113">-CertificateType</span></span>
<span data-ttu-id="80da1-114">Określa typ certyfikatu dla emitenta.</span><span class="sxs-lookup"><span data-stu-id="80da1-114">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80da1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80da1-115">-DefaultProfile</span></span>
<span data-ttu-id="80da1-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="80da1-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="80da1-117">-Wyłączone</span><span class="sxs-lookup"><span data-stu-id="80da1-117">-Disabled</span></span>
<span data-ttu-id="80da1-118">Wskazuje, że zasada certyfikatu jest wyłączona.</span><span class="sxs-lookup"><span data-stu-id="80da1-118">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80da1-119">-DnsName</span><span class="sxs-lookup"><span data-stu-id="80da1-119">-DnsName</span></span>
<span data-ttu-id="80da1-120">Określa nazwy DNS w certyfikacie.</span><span class="sxs-lookup"><span data-stu-id="80da1-120">Specifies the DNS names in the certificate.</span></span>

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

### <span data-ttu-id="80da1-121">-Ekus</span><span class="sxs-lookup"><span data-stu-id="80da1-121">-Ekus</span></span>
<span data-ttu-id="80da1-122">Określa ulepszone użycie klucza (EKUs) w certyfikacie.</span><span class="sxs-lookup"><span data-stu-id="80da1-122">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="80da1-123">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="80da1-123">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="80da1-124">Określa, ile dni przed wygaśnięciem rozpocznie się proces powiadomień automatycznych.</span><span class="sxs-lookup"><span data-stu-id="80da1-124">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="80da1-125">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="80da1-125">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="80da1-126">Określa wartość procentową okresu istnienia, po upływie którego rozpocznie się proces automatycznego powiadomienia.</span><span class="sxs-lookup"><span data-stu-id="80da1-126">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="80da1-127">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="80da1-127">-IssuerName</span></span>
<span data-ttu-id="80da1-128">Określa nazwę wystawcy certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="80da1-128">Specifies the name of the issuer for the certificate.</span></span>

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

### <span data-ttu-id="80da1-129">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="80da1-129">-KeyNotExportable</span></span>
<span data-ttu-id="80da1-130">Wskazuje, że nie można eksportować klucza.</span><span class="sxs-lookup"><span data-stu-id="80da1-130">Indicates that the key is not exportable.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80da1-131">-KeyType</span><span class="sxs-lookup"><span data-stu-id="80da1-131">-KeyType</span></span>
<span data-ttu-id="80da1-132">Określa typ klucza klucza, który wykonuje kopię zapasową certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="80da1-132">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="80da1-133">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="80da1-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="80da1-134">ALGORYTM</span><span class="sxs-lookup"><span data-stu-id="80da1-134">RSA</span></span>
- <span data-ttu-id="80da1-135">RSA — HSM</span><span class="sxs-lookup"><span data-stu-id="80da1-135">RSA-HSM</span></span>

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

### <span data-ttu-id="80da1-136">-Użycie</span><span class="sxs-lookup"><span data-stu-id="80da1-136">-KeyUsage</span></span>
<span data-ttu-id="80da1-137">Określa użycie klucza w certyfikacie.</span><span class="sxs-lookup"><span data-stu-id="80da1-137">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="80da1-138">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="80da1-138">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="80da1-139">Określa liczbę dni przed wygaśnięciem, po upływie której rozpocznie się proces automatycznego odnawiania certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="80da1-139">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="80da1-140">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="80da1-140">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="80da1-141">Określa wartość procentową okresu istnienia, po upływie którego rozpocznie się proces automatycznego odnawiania certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="80da1-141">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="80da1-142">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="80da1-142">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="80da1-143">Wskazuje, że certyfikat jest ponownie używany podczas odnawiania klucza.</span><span class="sxs-lookup"><span data-stu-id="80da1-143">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80da1-144">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="80da1-144">-SecretContentType</span></span>
<span data-ttu-id="80da1-145">Określa typ zawartości nowego klucza tajnego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="80da1-145">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="80da1-146">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="80da1-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="80da1-147">application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="80da1-147">application/x-pkcs12</span></span>
- <span data-ttu-id="80da1-148">application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="80da1-148">application/x-pem-file</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80da1-149">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="80da1-149">-SubjectName</span></span>
<span data-ttu-id="80da1-150">Określa nazwę podmiotu certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="80da1-150">Specifies the subject name of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: SubjectName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: DNSNames
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80da1-151">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="80da1-151">-ValidityInMonths</span></span>
<span data-ttu-id="80da1-152">Określa liczbę miesięcy ważności certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="80da1-152">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="80da1-153">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="80da1-153">-Confirm</span></span>
<span data-ttu-id="80da1-154">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80da1-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80da1-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80da1-155">-WhatIf</span></span>
<span data-ttu-id="80da1-156">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80da1-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80da1-157">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="80da1-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80da1-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80da1-158">CommonParameters</span></span>
<span data-ttu-id="80da1-159">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80da1-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80da1-160">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80da1-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80da1-161">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="80da1-161">INPUTS</span></span>

### <span data-ttu-id="80da1-162">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="80da1-162">None</span></span>
<span data-ttu-id="80da1-163">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="80da1-163">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="80da1-164">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="80da1-164">OUTPUTS</span></span>

### <span data-ttu-id="80da1-165">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="80da1-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="80da1-166">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="80da1-166">NOTES</span></span>

## <span data-ttu-id="80da1-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="80da1-167">RELATED LINKS</span></span>

[<span data-ttu-id="80da1-168">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="80da1-168">Get-AzureKeyVaultCertificatePolicy</span></span>](./Get-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="80da1-169">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="80da1-169">Set-AzureKeyVaultCertificatePolicy</span></span>](./Set-AzureKeyVaultCertificatePolicy.md)

