---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/new-azurekeyvaultcertificatepolicy
schema: 2.0.0
ms.openlocfilehash: b10dd0e034db53af35c930ce1c4588dee2576c75
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898001"
---
# <span data-ttu-id="f6aef-101">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="f6aef-101">New-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="f6aef-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f6aef-102">SYNOPSIS</span></span>
<span data-ttu-id="f6aef-103">Tworzy obiekt zasad certyfikatu w pamięci.</span><span class="sxs-lookup"><span data-stu-id="f6aef-103">Creates an in-memory certificate policy object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6aef-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f6aef-104">SYNTAX</span></span>

```
New-AzureKeyVaultCertificatePolicy [-SecretContentType <String>] [-ReuseKeyOnRenewal] [-Disabled]
 [-SubjectName <String>] [-DnsNames <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] -IssuerName <String>
 [-CertificateType <String>] [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>]
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6aef-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f6aef-105">DESCRIPTION</span></span>
<span data-ttu-id="f6aef-106">Polecenie cmdlet **New-AzureKeyVaultCertificatePolicy** umożliwia utworzenie obiektu zasad certyfikatu w pamięci dla magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f6aef-106">The **New-AzureKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="f6aef-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f6aef-107">EXAMPLES</span></span>

### <span data-ttu-id="f6aef-108">Przykład 1: Tworzenie zasad certyfikatów</span><span class="sxs-lookup"><span data-stu-id="f6aef-108">Example 1: Create a certificate policy</span></span>
```
PS C:\>New-AzureKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal
```

<span data-ttu-id="f6aef-109">To polecenie tworzy zasady certyfikatów, które są ważne przez sześć miesięcy i odnowią certyfikat za pomocą klucza.</span><span class="sxs-lookup"><span data-stu-id="f6aef-109">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

## <span data-ttu-id="f6aef-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f6aef-110">PARAMETERS</span></span>

### <span data-ttu-id="f6aef-111">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="f6aef-111">-CertificateType</span></span>
<span data-ttu-id="f6aef-112">Określa typ certyfikatu dla emitenta.</span><span class="sxs-lookup"><span data-stu-id="f6aef-112">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="f6aef-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6aef-113">-DefaultProfile</span></span>
<span data-ttu-id="f6aef-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f6aef-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f6aef-115">-Wyłączone</span><span class="sxs-lookup"><span data-stu-id="f6aef-115">-Disabled</span></span>
<span data-ttu-id="f6aef-116">Wskazuje, że zasada certyfikatu jest wyłączona.</span><span class="sxs-lookup"><span data-stu-id="f6aef-116">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="f6aef-117">-DnsNames</span><span class="sxs-lookup"><span data-stu-id="f6aef-117">-DnsNames</span></span>
<span data-ttu-id="f6aef-118">Określa nazwy DNS w certyfikacie.</span><span class="sxs-lookup"><span data-stu-id="f6aef-118">Specifies the DNS names in the certificate.</span></span>

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

### <span data-ttu-id="f6aef-119">-Ekus</span><span class="sxs-lookup"><span data-stu-id="f6aef-119">-Ekus</span></span>
<span data-ttu-id="f6aef-120">Określa ulepszone użycie klucza (EKUs) w certyfikacie.</span><span class="sxs-lookup"><span data-stu-id="f6aef-120">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="f6aef-121">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="f6aef-121">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="f6aef-122">Określa, ile dni przed wygaśnięciem rozpocznie się proces powiadomień automatycznych.</span><span class="sxs-lookup"><span data-stu-id="f6aef-122">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="f6aef-123">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="f6aef-123">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="f6aef-124">Określa wartość procentową okresu istnienia, po upływie którego rozpocznie się proces automatycznego powiadomienia.</span><span class="sxs-lookup"><span data-stu-id="f6aef-124">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="f6aef-125">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="f6aef-125">-IssuerName</span></span>
<span data-ttu-id="f6aef-126">Określa nazwę wystawcy certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="f6aef-126">Specifies the name of the issuer for the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6aef-127">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="f6aef-127">-KeyNotExportable</span></span>
<span data-ttu-id="f6aef-128">Wskazuje, że nie można eksportować klucza.</span><span class="sxs-lookup"><span data-stu-id="f6aef-128">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="f6aef-129">-KeyType</span><span class="sxs-lookup"><span data-stu-id="f6aef-129">-KeyType</span></span>
<span data-ttu-id="f6aef-130">Określa typ klucza klucza, który wykonuje kopię zapasową certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="f6aef-130">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="f6aef-131">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="f6aef-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f6aef-132">ALGORYTM</span><span class="sxs-lookup"><span data-stu-id="f6aef-132">RSA</span></span>
- <span data-ttu-id="f6aef-133">RSA — HSM</span><span class="sxs-lookup"><span data-stu-id="f6aef-133">RSA-HSM</span></span>

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

### <span data-ttu-id="f6aef-134">-Użycie</span><span class="sxs-lookup"><span data-stu-id="f6aef-134">-KeyUsage</span></span>
<span data-ttu-id="f6aef-135">Określa użycie klucza w certyfikacie.</span><span class="sxs-lookup"><span data-stu-id="f6aef-135">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="f6aef-136">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="f6aef-136">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="f6aef-137">Określa liczbę dni przed wygaśnięciem, po upływie której rozpocznie się proces automatycznego odnawiania certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="f6aef-137">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="f6aef-138">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="f6aef-138">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="f6aef-139">Określa wartość procentową okresu istnienia, po upływie którego rozpocznie się proces automatycznego odnawiania certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="f6aef-139">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="f6aef-140">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="f6aef-140">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="f6aef-141">Wskazuje, że certyfikat jest ponownie używany podczas odnawiania klucza.</span><span class="sxs-lookup"><span data-stu-id="f6aef-141">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="f6aef-142">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="f6aef-142">-SecretContentType</span></span>
<span data-ttu-id="f6aef-143">Określa typ zawartości nowego klucza tajnego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="f6aef-143">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="f6aef-144">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="f6aef-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f6aef-145">application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="f6aef-145">application/x-pkcs12</span></span>
- <span data-ttu-id="f6aef-146">application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="f6aef-146">application/x-pem-file</span></span>

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

### <span data-ttu-id="f6aef-147">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="f6aef-147">-SubjectName</span></span>
<span data-ttu-id="f6aef-148">Określa nazwę podmiotu certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="f6aef-148">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="f6aef-149">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="f6aef-149">-ValidityInMonths</span></span>
<span data-ttu-id="f6aef-150">Określa liczbę miesięcy ważności certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="f6aef-150">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="f6aef-151">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f6aef-151">-Confirm</span></span>
<span data-ttu-id="f6aef-152">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6aef-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6aef-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6aef-153">-WhatIf</span></span>
<span data-ttu-id="f6aef-154">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6aef-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6aef-155">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f6aef-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6aef-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6aef-156">CommonParameters</span></span>
<span data-ttu-id="f6aef-157">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6aef-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6aef-158">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6aef-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6aef-159">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f6aef-159">INPUTS</span></span>

## <span data-ttu-id="f6aef-160">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f6aef-160">OUTPUTS</span></span>

### <span data-ttu-id="f6aef-161">Microsoft. Azure. Commands. platforming. models. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="f6aef-161">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="f6aef-162">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f6aef-162">NOTES</span></span>

## <span data-ttu-id="f6aef-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f6aef-163">RELATED LINKS</span></span>

[<span data-ttu-id="f6aef-164">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="f6aef-164">Get-AzureKeyVaultCertificatePolicy</span></span>](./Get-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="f6aef-165">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="f6aef-165">Set-AzureKeyVaultCertificatePolicy</span></span>](./Set-AzureKeyVaultCertificatePolicy.md)

