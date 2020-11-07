---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: D4188DC6-A8AB-4B45-9781-94B74C338C63
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/import-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultCertificate.md
ms.openlocfilehash: 6591b96257a1c94cd2da9d0bc6f2995dc2034a40
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867972"
---
# <span data-ttu-id="d10be-101">Import-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="d10be-101">Import-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="d10be-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d10be-102">SYNOPSIS</span></span>
<span data-ttu-id="d10be-103">Importuje certyfikat do magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="d10be-103">Imports a certificate to a key vault.</span></span>

## <span data-ttu-id="d10be-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d10be-104">SYNTAX</span></span>

### <span data-ttu-id="d10be-105">ImportCertificateFromFile (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d10be-105">ImportCertificateFromFile (Default)</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> -FilePath <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d10be-106">ImportWithPrivateKeyFromString</span><span class="sxs-lookup"><span data-stu-id="d10be-106">ImportWithPrivateKeyFromString</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> -CertificateString <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d10be-107">ImportWithPrivateKeyFromCollection</span><span class="sxs-lookup"><span data-stu-id="d10be-107">ImportWithPrivateKeyFromCollection</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String>
 [-CertificateCollection] <X509Certificate2Collection> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d10be-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d10be-108">DESCRIPTION</span></span>
<span data-ttu-id="d10be-109">Polecenie cmdlet **Import-AzKeyVaultCertificate** importuje certyfikat do magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="d10be-109">The **Import-AzKeyVaultCertificate** cmdlet imports a certificate into a key vault.</span></span>
<span data-ttu-id="d10be-110">Możesz utworzyć certyfikat do zaimportowania, korzystając z jednej z następujących metod:</span><span class="sxs-lookup"><span data-stu-id="d10be-110">You can create the certificate to import by using one of the following methods:</span></span>
- <span data-ttu-id="d10be-111">Użyj polecenia cmdlet New-AzKeyVaultCertificateSigningRequest, aby utworzyć żądanie podpisania certyfikatu i przesłać je do urzędu certyfikacji.</span><span class="sxs-lookup"><span data-stu-id="d10be-111">Use the New-AzKeyVaultCertificateSigningRequest cmdlet to create a certificate signing request and submit it to a certificate authority.</span></span>
- <span data-ttu-id="d10be-112">Użyj istniejącego pliku pakietu certyfikatów, takiego jak plik PFX lub P12, zawierający zarówno certyfikat, jak i klucz prywatny.</span><span class="sxs-lookup"><span data-stu-id="d10be-112">Use an existing certificate package file, such as a .pfx or .p12 file, which contains both the certificate and private key.</span></span>

## <span data-ttu-id="d10be-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d10be-113">EXAMPLES</span></span>

### <span data-ttu-id="d10be-114">Przykład 1: Importowanie certyfikatu magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="d10be-114">Example 1: Import a key vault certificate</span></span>
```powershell
PS C:\> $Password = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS C:\> Import-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "ImportCert01" -FilePath "C:\Users\contosoUser\Desktop\import.pfx" -Password $Password

Name        : importCert01
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
Created     : 2/8/2016 11:50:43 PM
Updated     : 2/8/2016 11:50:43 PM
```

<span data-ttu-id="d10be-115">W pierwszym poleceniu użyto polecenia cmdlet ConvertTo-SecureString, aby utworzyć bezpieczne hasło, a następnie przechowywać je w zmiennej $Password.</span><span class="sxs-lookup"><span data-stu-id="d10be-115">The first command uses the ConvertTo-SecureString cmdlet to create a secure password, and then stores it in the $Password variable.</span></span>
<span data-ttu-id="d10be-116">Drugie polecenie importuje certyfikat o nazwie ImportCert01 do magazynu kluczy CosotosoKV01.</span><span class="sxs-lookup"><span data-stu-id="d10be-116">The second command imports the certificate named ImportCert01 into the CosotosoKV01 key vault.</span></span>

## <span data-ttu-id="d10be-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d10be-117">PARAMETERS</span></span>

### <span data-ttu-id="d10be-118">-CertificateCollection</span><span class="sxs-lookup"><span data-stu-id="d10be-118">-CertificateCollection</span></span>
<span data-ttu-id="d10be-119">Określa kolekcję certyfikatów, którą należy dodać do magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="d10be-119">Specifies the certificate collection to add to a key vault.</span></span>

```yaml
Type: System.Security.Cryptography.X509Certificates.X509Certificate2Collection
Parameter Sets: ImportWithPrivateKeyFromCollection
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d10be-120">-CertificateString</span><span class="sxs-lookup"><span data-stu-id="d10be-120">-CertificateString</span></span>
<span data-ttu-id="d10be-121">Określa ciąg certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="d10be-121">Specifies a certificate string.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportWithPrivateKeyFromString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d10be-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d10be-122">-DefaultProfile</span></span>
<span data-ttu-id="d10be-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d10be-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d10be-124">-FilePath</span><span class="sxs-lookup"><span data-stu-id="d10be-124">-FilePath</span></span>
<span data-ttu-id="d10be-125">Określa ścieżkę pliku certyfikatu, który został zaimportowany za pomocą tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d10be-125">Specifies the path of the certificate file that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportCertificateFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d10be-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d10be-126">-Name</span></span>
<span data-ttu-id="d10be-127">Określa nazwę certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="d10be-127">Specifies the certificate name.</span></span> <span data-ttu-id="d10be-128">To polecenie cmdlet konstruuje w pełni kwalifikowaną nazwę domeny (FQDN) certyfikatu z nazwy magazynu kluczy, obecnie wybranego środowiska i nazwy certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="d10be-128">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate from key vault name, currently selected environment, and certificate name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d10be-129">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="d10be-129">-Password</span></span>
<span data-ttu-id="d10be-130">Określa hasło do pliku certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="d10be-130">Specifies the password for a certificate file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ImportCertificateFromFile, ImportWithPrivateKeyFromString
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d10be-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="d10be-131">-Tag</span></span>
<span data-ttu-id="d10be-132">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="d10be-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d10be-133">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="d10be-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d10be-134">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="d10be-134">-VaultName</span></span>
<span data-ttu-id="d10be-135">Określa nazwę magazynu kluczy, do którego to polecenie cmdlet importuje certyfikaty.</span><span class="sxs-lookup"><span data-stu-id="d10be-135">Specifies the key vault name into which this cmdlet imports certificates.</span></span>
<span data-ttu-id="d10be-136">To polecenie cmdlet tworzy w pełni kwalifikowaną nazwę domeny (FQDN) magazynu kluczy na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="d10be-136">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d10be-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d10be-137">-Confirm</span></span>
<span data-ttu-id="d10be-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d10be-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d10be-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d10be-139">-WhatIf</span></span>
<span data-ttu-id="d10be-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d10be-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d10be-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d10be-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d10be-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d10be-142">CommonParameters</span></span>
<span data-ttu-id="d10be-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d10be-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d10be-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d10be-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d10be-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d10be-145">INPUTS</span></span>

### <span data-ttu-id="d10be-146">System. String</span><span class="sxs-lookup"><span data-stu-id="d10be-146">System.String</span></span>

### <span data-ttu-id="d10be-147">System. Security. Cryptography. x509. X509Certificate2Collection</span><span class="sxs-lookup"><span data-stu-id="d10be-147">System.Security.Cryptography.X509Certificates.X509Certificate2Collection</span></span>

### <span data-ttu-id="d10be-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d10be-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d10be-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d10be-149">OUTPUTS</span></span>

### <span data-ttu-id="d10be-150">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="d10be-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="d10be-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d10be-151">NOTES</span></span>

## <span data-ttu-id="d10be-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d10be-152">RELATED LINKS</span></span>

[<span data-ttu-id="d10be-153">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="d10be-153">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)
