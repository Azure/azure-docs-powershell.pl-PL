---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: 381ce302a8404c0bb643db0fc82e392fe53d956a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527529"
---
# <span data-ttu-id="31703-101">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="31703-101">New-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="31703-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="31703-102">SYNOPSIS</span></span>
<span data-ttu-id="31703-103">Tworzy obiekt zasad certyfikatu w pamięci.</span><span class="sxs-lookup"><span data-stu-id="31703-103">Creates an in-memory certificate policy object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31703-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="31703-104">SYNTAX</span></span>

```
New-AzureKeyVaultCertificatePolicy [-SecretContentType <String>] [-ReuseKeyOnRenewal] [-Disabled]
 [-SubjectName <String>] [-DnsNames <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] -IssuerName <String>
 [-CertificateType <String>] [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>]
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31703-105">Opis</span><span class="sxs-lookup"><span data-stu-id="31703-105">DESCRIPTION</span></span>
<span data-ttu-id="31703-106">Polecenie cmdlet **New-AzureKeyVaultCertificatePolicy** umożliwia utworzenie obiektu zasad certyfikatu w pamięci dla magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="31703-106">The **New-AzureKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="31703-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="31703-107">EXAMPLES</span></span>

### <span data-ttu-id="31703-108">Przykład 1: Tworzenie zasad certyfikatów</span><span class="sxs-lookup"><span data-stu-id="31703-108">Example 1: Create a certificate policy</span></span>
```
PS C:\>New-AzureKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal
```

<span data-ttu-id="31703-109">To polecenie tworzy zasady certyfikatów, które są ważne przez sześć miesięcy i odnowią certyfikat za pomocą klucza.</span><span class="sxs-lookup"><span data-stu-id="31703-109">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

## <span data-ttu-id="31703-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="31703-110">PARAMETERS</span></span>

### <span data-ttu-id="31703-111">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="31703-111">-CertificateType</span></span>
<span data-ttu-id="31703-112">Określa typ certyfikatu dla emitenta.</span><span class="sxs-lookup"><span data-stu-id="31703-112">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="31703-113">-Wyłączone</span><span class="sxs-lookup"><span data-stu-id="31703-113">-Disabled</span></span>
<span data-ttu-id="31703-114">Wskazuje, że zasada certyfikatu jest wyłączona.</span><span class="sxs-lookup"><span data-stu-id="31703-114">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="31703-115">-DnsNames</span><span class="sxs-lookup"><span data-stu-id="31703-115">-DnsNames</span></span>
<span data-ttu-id="31703-116">Określa nazwy DNS w certyfikacie.</span><span class="sxs-lookup"><span data-stu-id="31703-116">Specifies the DNS names in the certificate.</span></span>

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

### <span data-ttu-id="31703-117">-Ekus</span><span class="sxs-lookup"><span data-stu-id="31703-117">-Ekus</span></span>
<span data-ttu-id="31703-118">Określa ulepszone użycie klucza (EKUs) w certyfikacie.</span><span class="sxs-lookup"><span data-stu-id="31703-118">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="31703-119">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="31703-119">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="31703-120">Określa, ile dni przed wygaśnięciem rozpocznie się proces powiadomień automatycznych.</span><span class="sxs-lookup"><span data-stu-id="31703-120">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="31703-121">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="31703-121">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="31703-122">Określa wartość procentową okresu istnienia, po upływie którego rozpocznie się proces automatycznego powiadomienia.</span><span class="sxs-lookup"><span data-stu-id="31703-122">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="31703-123">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="31703-123">-IssuerName</span></span>
<span data-ttu-id="31703-124">Określa nazwę wystawcy certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="31703-124">Specifies the name of the issuer for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31703-125">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="31703-125">-KeyNotExportable</span></span>
<span data-ttu-id="31703-126">Wskazuje, że nie można eksportować klucza.</span><span class="sxs-lookup"><span data-stu-id="31703-126">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="31703-127">-KeyType</span><span class="sxs-lookup"><span data-stu-id="31703-127">-KeyType</span></span>
<span data-ttu-id="31703-128">Określa typ klucza klucza, który wykonuje kopię zapasową certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="31703-128">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="31703-129">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="31703-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="31703-130">ALGORYTM</span><span class="sxs-lookup"><span data-stu-id="31703-130">RSA</span></span>
- <span data-ttu-id="31703-131">RSA — HSM</span><span class="sxs-lookup"><span data-stu-id="31703-131">RSA-HSM</span></span>

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

### <span data-ttu-id="31703-132">-Użycie</span><span class="sxs-lookup"><span data-stu-id="31703-132">-KeyUsage</span></span>
<span data-ttu-id="31703-133">Określa użycie klucza w certyfikacie.</span><span class="sxs-lookup"><span data-stu-id="31703-133">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="31703-134">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="31703-134">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="31703-135">Określa liczbę dni przed wygaśnięciem, po upływie której rozpocznie się proces automatycznego odnawiania certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="31703-135">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="31703-136">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="31703-136">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="31703-137">Określa wartość procentową okresu istnienia, po upływie którego rozpocznie się proces automatycznego odnawiania certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="31703-137">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="31703-138">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="31703-138">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="31703-139">Wskazuje, że certyfikat jest ponownie używany podczas odnawiania klucza.</span><span class="sxs-lookup"><span data-stu-id="31703-139">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="31703-140">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="31703-140">-SecretContentType</span></span>
<span data-ttu-id="31703-141">Określa typ zawartości nowego klucza tajnego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="31703-141">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="31703-142">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="31703-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="31703-143">application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="31703-143">application/x-pkcs12</span></span>
- <span data-ttu-id="31703-144">application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="31703-144">application/x-pem-file</span></span>

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

### <span data-ttu-id="31703-145">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="31703-145">-SubjectName</span></span>
<span data-ttu-id="31703-146">Określa nazwę podmiotu certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="31703-146">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="31703-147">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="31703-147">-ValidityInMonths</span></span>
<span data-ttu-id="31703-148">Określa liczbę miesięcy ważności certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="31703-148">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="31703-149">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="31703-149">-Confirm</span></span>
<span data-ttu-id="31703-150">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31703-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31703-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31703-151">-WhatIf</span></span>
<span data-ttu-id="31703-152">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31703-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31703-153">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="31703-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31703-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31703-154">-DefaultProfile</span></span>
<span data-ttu-id="31703-155">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="31703-155">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31703-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31703-156">CommonParameters</span></span>
<span data-ttu-id="31703-157">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31703-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31703-158">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31703-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31703-159">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="31703-159">INPUTS</span></span>

## <span data-ttu-id="31703-160">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="31703-160">OUTPUTS</span></span>

### <span data-ttu-id="31703-161">Microsoft. Azure. Commands. platforming. models. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="31703-161">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="31703-162">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="31703-162">NOTES</span></span>

## <span data-ttu-id="31703-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="31703-163">RELATED LINKS</span></span>

[<span data-ttu-id="31703-164">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="31703-164">Get-AzureKeyVaultCertificatePolicy</span></span>](./Get-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="31703-165">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="31703-165">Set-AzureKeyVaultCertificatePolicy</span></span>](./Set-AzureKeyVaultCertificatePolicy.md)

