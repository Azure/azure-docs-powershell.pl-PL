---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: e960aa211b53c79087e67e2bd86504e597a718d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553667"
---
# <span data-ttu-id="82ecc-101">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="82ecc-101">Set-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="82ecc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="82ecc-102">SYNOPSIS</span></span>
<span data-ttu-id="82ecc-103">Tworzy lub aktualizuje zasady dotyczące certyfikatu w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="82ecc-103">Creates or updates the policy for a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82ecc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="82ecc-104">SYNTAX</span></span>

### <span data-ttu-id="82ecc-105">ExpandedRenewPercentage (domyślny)</span><span class="sxs-lookup"><span data-stu-id="82ecc-105">ExpandedRenewPercentage (Default)</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> [-RenewAtPercentageLifetime <Int32>]
 [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82ecc-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="82ecc-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-InputObject] <PSKeyVaultCertificatePolicy> [-EmailAtNumberOfDaysBeforeExpiry <Int32>]
 [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82ecc-107">ExpandedRenewNumber</span><span class="sxs-lookup"><span data-stu-id="82ecc-107">ExpandedRenewNumber</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 -RenewAtNumberOfDaysBeforeExpiry <Int32> [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>]
 [-Disabled] [-SubjectName <String>] [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82ecc-108">Opis</span><span class="sxs-lookup"><span data-stu-id="82ecc-108">DESCRIPTION</span></span>
<span data-ttu-id="82ecc-109">Polecenie cmdlet **Set-AzureKeyVaultCertificatePolicy** służy do tworzenia lub aktualizowania zasad certyfikatu w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="82ecc-109">The **Set-AzureKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="82ecc-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="82ecc-110">EXAMPLES</span></span>

### <span data-ttu-id="82ecc-111">Przykład 1: Ustawianie zasad certyfikatów</span><span class="sxs-lookup"><span data-stu-id="82ecc-111">Example 1: Set a certificate policy</span></span>
```
PS C:\>Set-AzureKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01" -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal $True
```

<span data-ttu-id="82ecc-112">To polecenie ustawia zasady dla certyfikatu TestCert01 w magazynie kluczy ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="82ecc-112">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="82ecc-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="82ecc-113">PARAMETERS</span></span>

### <span data-ttu-id="82ecc-114">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="82ecc-114">-CertificateType</span></span>
<span data-ttu-id="82ecc-115">Określa typ certyfikatu dla emitenta.</span><span class="sxs-lookup"><span data-stu-id="82ecc-115">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82ecc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82ecc-116">-DefaultProfile</span></span>
<span data-ttu-id="82ecc-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="82ecc-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="82ecc-118">-Wyłączone</span><span class="sxs-lookup"><span data-stu-id="82ecc-118">-Disabled</span></span>
<span data-ttu-id="82ecc-119">Wskazuje, że zasada certyfikatu jest wyłączona.</span><span class="sxs-lookup"><span data-stu-id="82ecc-119">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82ecc-120">-DnsName</span><span class="sxs-lookup"><span data-stu-id="82ecc-120">-DnsName</span></span>
<span data-ttu-id="82ecc-121">Określa nazwę podmiotu certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="82ecc-121">Specifies the subject name of the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases: DnsNames

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82ecc-122">-Ekus</span><span class="sxs-lookup"><span data-stu-id="82ecc-122">-Ekus</span></span>
<span data-ttu-id="82ecc-123">Określa ulepszone użycie klucza (EKUs) w certyfikacie.</span><span class="sxs-lookup"><span data-stu-id="82ecc-123">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82ecc-124">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="82ecc-124">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="82ecc-125">Określa liczbę dni, po upływie których należy zacząć automatyczne odnawianie.</span><span class="sxs-lookup"><span data-stu-id="82ecc-125">Specifies the number of days before expiration when automatic renewal should start.</span></span>

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

### <span data-ttu-id="82ecc-126">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="82ecc-126">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="82ecc-127">Określa wartość procentową okresu istnienia, po upływie którego rozpocznie się proces automatycznego powiadomienia.</span><span class="sxs-lookup"><span data-stu-id="82ecc-127">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="82ecc-128">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="82ecc-128">-InputObject</span></span>
<span data-ttu-id="82ecc-129">Określa zasady certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="82ecc-129">Specifies the certificate policy.</span></span>

```yaml
Type: PSKeyVaultCertificatePolicy
Parameter Sets: ByValue
Aliases: CertificatePolicy

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82ecc-130">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="82ecc-130">-IssuerName</span></span>
<span data-ttu-id="82ecc-131">Określa nazwę wystawcy dla tego certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="82ecc-131">Specifies the name of the issuer for this certificate.</span></span>

```yaml
Type: String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82ecc-132">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="82ecc-132">-KeyNotExportable</span></span>
<span data-ttu-id="82ecc-133">Wskazuje, że nie można eksportować klucza.</span><span class="sxs-lookup"><span data-stu-id="82ecc-133">Indicates that the key is not exportable.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82ecc-134">-KeyType</span><span class="sxs-lookup"><span data-stu-id="82ecc-134">-KeyType</span></span>
<span data-ttu-id="82ecc-135">Określa typ klucza klucza, który wykonuje kopię zapasową certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="82ecc-135">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="82ecc-136">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="82ecc-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="82ecc-137">ALGORYTM</span><span class="sxs-lookup"><span data-stu-id="82ecc-137">RSA</span></span>
- <span data-ttu-id="82ecc-138">RSA — HSM</span><span class="sxs-lookup"><span data-stu-id="82ecc-138">RSA-HSM</span></span>

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

### <span data-ttu-id="82ecc-139">-Użycie</span><span class="sxs-lookup"><span data-stu-id="82ecc-139">-KeyUsage</span></span>
<span data-ttu-id="82ecc-140">Określa użycie klucza w certyfikacie.</span><span class="sxs-lookup"><span data-stu-id="82ecc-140">Specifies the key usages in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82ecc-141">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="82ecc-141">-Name</span></span>
<span data-ttu-id="82ecc-142">Określa nazwę certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="82ecc-142">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="82ecc-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="82ecc-143">-PassThru</span></span>
<span data-ttu-id="82ecc-144">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="82ecc-144">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="82ecc-145">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="82ecc-145">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="82ecc-146">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="82ecc-146">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="82ecc-147">Określa liczbę dni przed wygaśnięciem, po upływie której rozpocznie się proces automatycznego odnawiania certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="82ecc-147">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: Int32
Parameter Sets: ExpandedRenewNumber
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82ecc-148">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="82ecc-148">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="82ecc-149">Określa wartość procentową okresu istnienia, po upływie którego rozpocznie się proces automatycznego odnawiania certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="82ecc-149">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: Int32
Parameter Sets: ExpandedRenewPercentage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82ecc-150">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="82ecc-150">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="82ecc-151">Wskazuje, że certyfikat jest ponownie używany podczas odnawiania klucza.</span><span class="sxs-lookup"><span data-stu-id="82ecc-151">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: Boolean
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82ecc-152">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="82ecc-152">-SecretContentType</span></span>
<span data-ttu-id="82ecc-153">Określa typ zawartości nowego klucza tajnego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="82ecc-153">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="82ecc-154">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="82ecc-154">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="82ecc-155">application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="82ecc-155">application/x-pkcs12</span></span>
- <span data-ttu-id="82ecc-156">application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="82ecc-156">application/x-pem-file</span></span>

```yaml
Type: String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82ecc-157">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="82ecc-157">-SubjectName</span></span>
<span data-ttu-id="82ecc-158">Określa nazwę podmiotu certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="82ecc-158">Specifies the subject name of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82ecc-159">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="82ecc-159">-ValidityInMonths</span></span>
<span data-ttu-id="82ecc-160">Określa liczbę miesięcy ważności certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="82ecc-160">Specifies the number of months the certificate is valid.</span></span>

```yaml
Type: Int32
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82ecc-161">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="82ecc-161">-VaultName</span></span>
<span data-ttu-id="82ecc-162">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="82ecc-162">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="82ecc-163">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="82ecc-163">-Confirm</span></span>
<span data-ttu-id="82ecc-164">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82ecc-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82ecc-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82ecc-165">-WhatIf</span></span>
<span data-ttu-id="82ecc-166">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82ecc-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82ecc-167">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="82ecc-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82ecc-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82ecc-168">CommonParameters</span></span>
<span data-ttu-id="82ecc-169">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82ecc-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82ecc-170">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82ecc-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82ecc-171">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="82ecc-171">INPUTS</span></span>

### <span data-ttu-id="82ecc-172">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="82ecc-172">None</span></span>
<span data-ttu-id="82ecc-173">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="82ecc-173">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="82ecc-174">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="82ecc-174">OUTPUTS</span></span>

### <span data-ttu-id="82ecc-175">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="82ecc-175">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="82ecc-176">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="82ecc-176">NOTES</span></span>

## <span data-ttu-id="82ecc-177">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="82ecc-177">RELATED LINKS</span></span>

[<span data-ttu-id="82ecc-178">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="82ecc-178">Get-AzureKeyVaultCertificatePolicy</span></span>](./Get-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="82ecc-179">Nowe — AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="82ecc-179">New-AzureKeyVaultCertificatePolicy</span></span>](./New-AzureKeyVaultCertificatePolicy.md)

