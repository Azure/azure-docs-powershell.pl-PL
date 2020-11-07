---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 89299823-3382-402D-9458-519466748051
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificate.md
ms.openlocfilehash: dd51ca4bc6d238d2aac1e4dccea4ad3a89bc8d35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552792"
---
# <span data-ttu-id="19c41-101">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="19c41-101">Add-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="19c41-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="19c41-102">SYNOPSIS</span></span>
<span data-ttu-id="19c41-103">Dodaje certyfikat do magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="19c41-103">Adds a certificate to a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19c41-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="19c41-104">SYNTAX</span></span>

```
Add-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String>
 [-CertificatePolicy] <PSKeyVaultCertificatePolicy> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19c41-105">Opis</span><span class="sxs-lookup"><span data-stu-id="19c41-105">DESCRIPTION</span></span>
<span data-ttu-id="19c41-106">Polecenie cmdlet **Add-AzureKeyVaultCertificate** uruchamia proces rejestrowania certyfikatu w magazynie kluczy usługi Azure Key.</span><span class="sxs-lookup"><span data-stu-id="19c41-106">The **Add-AzureKeyVaultCertificate** cmdlet starts the process of enrolling for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="19c41-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="19c41-107">EXAMPLES</span></span>

### <span data-ttu-id="19c41-108">Przykład 1. Dodaj certyfikat</span><span class="sxs-lookup"><span data-stu-id="19c41-108">Example 1: Add a certificate</span></span>
```powershell
PS C:\> $Policy = New-AzureKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal
PS C:\> Add-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01" -CertificatePolicy $Policy

Status                    : inProgress
CancellationRequested     : False
CertificateSigningRequest : MIICpjCCAY4CAQAwFjEUMBIGA1UEAxMLY29udG9zby5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC73w3VRBOlgJ5Od1PjDh+2ytngNZp+ZP4fkuX8K1Ti5LA6Ih7eWx1fgAN/iTb6l
                            5K6LvAIJvsTNVePMNxfSdaEIJ70Inm45wVU4A/kf+UxQWAYVMsBrLtDFWxnVhzf6n7RGYke6HLBj3j5ASb9g+olSs6eON25ibF0t+u6JC+sIR0LmVGar9Q0eZys1rdfzJBIKq+laOM7z2pJijb5ANqve9
                            i7rH5mnhQk4V8WsRstOhYR9jgLqSSxokDoeaBClIOidSBYqVc1yNv4ASe1UWUCR7ZK6OQXiecNWSWPmgWEyawu6AR9eb1YotCr2ScheMOCxlm3103luitxrd8A7kMjAgMBAAGgSzBJBgkqhkiG9w0BCQ4
                            xPDA6MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAQEAIHhsDJV37PKi8hor5eQf7+Tct1preIvSwqV0NF6Uo7O6
                            YnC9Py7Wp7CHfKzuqeptUk2Tsu7B5dHB+o9Ypeeqw8fWhTN0GFGRKO7WjZQlDqL+lRNcjlFSaP022oIP0kmvVhBcmZqRQlALXccAaxEclFA/3y/aNj2gwWeKpH/pwAkZ39zMEzpQCaRfnQk7e3l4MV8cf
                            eC2HPYdRWkXxAeDcNPxBuVmKy49AzYvly+APNVDU3v66gxl3fIKrGRsKi2Cp/nO5rBxG2h8t+0Za4l/HJ7ZWR9wKbd/xg7JhdZZFVBxMHYzw8KQ0ys13x8HY+PXU92Y7yD3uC2Rcj+zbAf+Kg==
ErrorCode                 :
ErrorMessage              : 

PS C:\> Get-AzureKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01"
Status                    : completed
CancellationRequested     : False
CertificateSigningRequest : MIICpjCCAY4CAQAwFjEUMBIGA1UEAxMLY29udG9zby5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC73w3VRBOlgJ5Od1PjDh+2ytngNZp+ZP4fkuX8K1Ti5LA6Ih7eWx1fgAN/iTb6l
                            5K6LvAIJvsTNVePMNxfSdaEIJ70Inm45wVU4A/kf+UxQWAYVMsBrLtDFWxnVhzf6n7RGYke6HLBj3j5ASb9g+olSs6eON25ibF0t+u6JC+sIR0LmVGar9Q0eZys1rdfzJBIKq+laOM7z2pJijb5ANqve9
                            i7rH5mnhQk4V8WsRstOhYR9jgLqSSxokDoeaBClIOidSBYqVc1yNv4ASe1UWUCR7ZK6OQXiecNWSWPmgWEyawu6AR9eb1YotCr2ScheMOCxlm3103luitxrd8A7kMjAgMBAAGgSzBJBgkqhkiG9w0BCQ4
                            xPDA6MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAQEAIHhsDJV37PKi8hor5eQf7+Tct1preIvSwqV0NF6Uo7O6
                            YnC9Py7Wp7CHfKzuqeptUk2Tsu7B5dHB+o9Ypeeqw8fWhTN0GFGRKO7WjZQlDqL+lRNcjlFSaP022oIP0kmvVhBcmZqRQlALXccAaxEclFA/3y/aNj2gwWeKpH/pwAkZ39zMEzpQCaRfnQk7e3l4MV8cf
                            eC2HPYdRWkXxAeDcNPxBuVmKy49AzYvly+APNVDU3v66gxl3fIKrGRsKi2Cp/nO5rBxG2h8t+0Za4l/HJ7ZWR9wKbd/xg7JhdZZFVBxMHYzw8KQ0ys13x8HY+PXU92Y7yD3uC2Rcj+zbAf+Kg==
ErrorCode                 :
ErrorMessage              : 

PS C:\> Get-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"

Name        : testCert01
Certificate : [Subject]
                CN=contoso.com

              [Issuer]
                CN=contoso.com

              [Serial Number]
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

              [Not Before]
                2/8/2016 3:11:45 PM

              [Not After]
                8/8/2016 4:21:45 PM

              [Thumbprint]
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

Thumbprint  : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
Tags        :
Enabled     : True
Created     : 2/8/2016 11:21:45 PM
Updated     : 2/8/2016 11:21:45 PM
```

<span data-ttu-id="19c41-109">W pierwszym poleceniu jest używane polecenie cmdlet New-AzureKeyVaultCertificatePolicy w celu utworzenia zasad certyfikatu, a następnie zapisanie go w zmiennej $Policy.</span><span class="sxs-lookup"><span data-stu-id="19c41-109">The first command uses the New-AzureKeyVaultCertificatePolicy cmdlet to create a certificate policy, and then stores it in the $Policy variable.</span></span>
<span data-ttu-id="19c41-110">Drugie polecenie używa polecenia **Add-AzureKeyVaultCertificate** , aby rozpocząć proces tworzenia certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="19c41-110">The second command uses **Add-AzureKeyVaultCertificate** to start the process to create a certificate.</span></span>
<span data-ttu-id="19c41-111">W trzecim poleceniu użyto polecenia cmdlet Get-AzureKeyVaultCertificateOperation do sondowania operacji w celu sprawdzenia, czy jest ona kompletna.</span><span class="sxs-lookup"><span data-stu-id="19c41-111">The third command uses the Get-AzureKeyVaultCertificateOperation cmdlet to poll the operation to verify that it's complete.</span></span>
<span data-ttu-id="19c41-112">Polecenie ostatnie używa polecenia cmdlet Get-AzureKeyVaultCertificate, aby uzyskać certyfikat.</span><span class="sxs-lookup"><span data-stu-id="19c41-112">The final command uses the Get-AzureKeyVaultCertificate cmdlet to get the certificate.</span></span>

## <span data-ttu-id="19c41-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="19c41-113">PARAMETERS</span></span>

### <span data-ttu-id="19c41-114">-CertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="19c41-114">-CertificatePolicy</span></span>
<span data-ttu-id="19c41-115">Określa obiekt **KeyVaultCertificatePolicy** .</span><span class="sxs-lookup"><span data-stu-id="19c41-115">Specifies a **KeyVaultCertificatePolicy** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19c41-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19c41-116">-DefaultProfile</span></span>
<span data-ttu-id="19c41-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="19c41-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="19c41-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="19c41-118">-Name</span></span>
<span data-ttu-id="19c41-119">Określa nazwę certyfikatu, który ma zostać dodany.</span><span class="sxs-lookup"><span data-stu-id="19c41-119">Specifies the name of the certificate to add.</span></span>

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

### <span data-ttu-id="19c41-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="19c41-120">-Tag</span></span>
<span data-ttu-id="19c41-121">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="19c41-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="19c41-122">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="19c41-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c41-123">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="19c41-123">-VaultName</span></span>
<span data-ttu-id="19c41-124">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="19c41-124">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="19c41-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="19c41-125">-Confirm</span></span>
<span data-ttu-id="19c41-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19c41-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19c41-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19c41-127">-WhatIf</span></span>
<span data-ttu-id="19c41-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19c41-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19c41-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="19c41-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19c41-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19c41-130">CommonParameters</span></span>
<span data-ttu-id="19c41-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19c41-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19c41-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19c41-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19c41-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="19c41-133">INPUTS</span></span>

### <span data-ttu-id="19c41-134">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="19c41-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>
<span data-ttu-id="19c41-135">Parametry: CertificatePolicy (ByValue)</span><span class="sxs-lookup"><span data-stu-id="19c41-135">Parameters: CertificatePolicy (ByValue)</span></span>

## <span data-ttu-id="19c41-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="19c41-136">OUTPUTS</span></span>

### <span data-ttu-id="19c41-137">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="19c41-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="19c41-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="19c41-138">NOTES</span></span>

## <span data-ttu-id="19c41-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="19c41-139">RELATED LINKS</span></span>

[<span data-ttu-id="19c41-140">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="19c41-140">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)

[<span data-ttu-id="19c41-141">Import — AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="19c41-141">Import-AzureKeyVaultCertificate</span></span>](./Import-AzureKeyVaultCertificate.md)

[<span data-ttu-id="19c41-142">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="19c41-142">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)