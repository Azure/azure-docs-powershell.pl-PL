---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: D4188DC6-A8AB-4B45-9781-94B74C338C63
online version: https://docs.microsoft.com/powershell/module/az.keyvault/import-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultCertificate.md
ms.openlocfilehash: 507bcce6607566c733ee4cd52f72f7e7910ac90f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001409"
---
# <span data-ttu-id="d5af8-101">Import-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="d5af8-101">Import-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="d5af8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5af8-102">SYNOPSIS</span></span>
<span data-ttu-id="d5af8-103">Importuje certyfikat do magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="d5af8-103">Imports a certificate to a key vault.</span></span>

## <span data-ttu-id="d5af8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d5af8-104">SYNTAX</span></span>

### <span data-ttu-id="d5af8-105">ImportCertificateFromFile (domyślne)</span><span class="sxs-lookup"><span data-stu-id="d5af8-105">ImportCertificateFromFile (Default)</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> -FilePath <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d5af8-106">ImportWithPrivateKeyFromString</span><span class="sxs-lookup"><span data-stu-id="d5af8-106">ImportWithPrivateKeyFromString</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> -CertificateString <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d5af8-107">ImportWithPrivateKeyFromCollection</span><span class="sxs-lookup"><span data-stu-id="d5af8-107">ImportWithPrivateKeyFromCollection</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String>
 [-CertificateCollection] <X509Certificate2Collection> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5af8-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="d5af8-108">DESCRIPTION</span></span>
<span data-ttu-id="d5af8-109">Polecenie **cmdlet Import-AzKeyVaultCertificate** importuje certyfikat do magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="d5af8-109">The **Import-AzKeyVaultCertificate** cmdlet imports a certificate into a key vault.</span></span>
<span data-ttu-id="d5af8-110">Certyfikat można utworzyć do zaimportowania przy użyciu jednej z następujących metod:</span><span class="sxs-lookup"><span data-stu-id="d5af8-110">You can create the certificate to import by using one of the following methods:</span></span>
- <span data-ttu-id="d5af8-111">Umożliwia `Add-AzKeyVaultCertificate` utworzenie żądania podpisania certyfikatu i przesłanie go do urzędu certyfikacji.</span><span class="sxs-lookup"><span data-stu-id="d5af8-111">Use `Add-AzKeyVaultCertificate` to create a certificate signing request and submit it to a certificate authority.</span></span> <span data-ttu-id="d5af8-112">Zobacz https://docs.microsoft.com/azure/key-vault/certificates/create-certificate-signing-request</span><span class="sxs-lookup"><span data-stu-id="d5af8-112">See https://docs.microsoft.com/azure/key-vault/certificates/create-certificate-signing-request</span></span>
- <span data-ttu-id="d5af8-113">Użyj istniejącego pliku pakietu certyfikatu, takiego jak pfx lub p12, który zawiera zarówno certyfikat, jak i klucz prywatny.</span><span class="sxs-lookup"><span data-stu-id="d5af8-113">Use an existing certificate package file, such as a .pfx or .p12 file, which contains both the certificate and private key.</span></span>

## <span data-ttu-id="d5af8-114">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d5af8-114">EXAMPLES</span></span>

### <span data-ttu-id="d5af8-115">Przykład 1. Importowanie certyfikatu magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="d5af8-115">Example 1: Import a key vault certificate</span></span>
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

<span data-ttu-id="d5af8-116">Pierwsze polecenie tworzy bezpieczne ConvertTo-SecureString cmdlet, a następnie zapisuje je w $Password danych.</span><span class="sxs-lookup"><span data-stu-id="d5af8-116">The first command uses the ConvertTo-SecureString cmdlet to create a secure password, and then stores it in the $Password variable.</span></span>
<span data-ttu-id="d5af8-117">Drugie polecenie importuje certyfikat o nazwie ImportCert01 do magazynu kluczy cosotosoKV01.</span><span class="sxs-lookup"><span data-stu-id="d5af8-117">The second command imports the certificate named ImportCert01 into the CosotosoKV01 key vault.</span></span>

## <span data-ttu-id="d5af8-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5af8-118">PARAMETERS</span></span>

### <span data-ttu-id="d5af8-119">-CertificateCollection</span><span class="sxs-lookup"><span data-stu-id="d5af8-119">-CertificateCollection</span></span>
<span data-ttu-id="d5af8-120">Określa kolekcję certyfikatów do dodania do magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="d5af8-120">Specifies the certificate collection to add to a key vault.</span></span>

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

### <span data-ttu-id="d5af8-121">-CertificateString</span><span class="sxs-lookup"><span data-stu-id="d5af8-121">-CertificateString</span></span>
<span data-ttu-id="d5af8-122">Określa ciąg certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="d5af8-122">Specifies a certificate string.</span></span>

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

### <span data-ttu-id="d5af8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5af8-123">-DefaultProfile</span></span>
<span data-ttu-id="d5af8-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="d5af8-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d5af8-125">- FilePath</span><span class="sxs-lookup"><span data-stu-id="d5af8-125">-FilePath</span></span>
<span data-ttu-id="d5af8-126">Określa ścieżkę pliku certyfikatu, który zostanie importowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5af8-126">Specifies the path of the certificate file that this cmdlet imports.</span></span>

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

### <span data-ttu-id="d5af8-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d5af8-127">-Name</span></span>
<span data-ttu-id="d5af8-128">Określa nazwę certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="d5af8-128">Specifies the certificate name.</span></span> <span data-ttu-id="d5af8-129">To polecenie cmdlet konstruuje w pełni kwalifikowaną nazwę domeny (FQDN) certyfikatu z nazwy magazynu kluczy, obecnie wybranego środowiska i nazwy certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="d5af8-129">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate from key vault name, currently selected environment, and certificate name.</span></span>

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

### <span data-ttu-id="d5af8-130">— Hasło</span><span class="sxs-lookup"><span data-stu-id="d5af8-130">-Password</span></span>
<span data-ttu-id="d5af8-131">Określa hasło dla pliku certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="d5af8-131">Specifies the password for a certificate file.</span></span>

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

### <span data-ttu-id="d5af8-132">— Tag</span><span class="sxs-lookup"><span data-stu-id="d5af8-132">-Tag</span></span>
<span data-ttu-id="d5af8-133">Pary klucz-wartość w postaci tabeli skrótu.</span><span class="sxs-lookup"><span data-stu-id="d5af8-133">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d5af8-134">Na przykład: @{key0="value0";key1=$null;key2="wartość2"}</span><span class="sxs-lookup"><span data-stu-id="d5af8-134">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="d5af8-135">-VaultName</span><span class="sxs-lookup"><span data-stu-id="d5af8-135">-VaultName</span></span>
<span data-ttu-id="d5af8-136">Określa nazwę magazynu klucza, do którego to polecenie cmdlet importuje certyfikaty.</span><span class="sxs-lookup"><span data-stu-id="d5af8-136">Specifies the key vault name into which this cmdlet imports certificates.</span></span>
<span data-ttu-id="d5af8-137">To polecenie cmdlet konstruuje w pełni kwalifikowaną nazwę domeny (FQDN) magazynu kluczy na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="d5af8-137">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="d5af8-138">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d5af8-138">-Confirm</span></span>
<span data-ttu-id="d5af8-139">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d5af8-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5af8-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5af8-140">-WhatIf</span></span>
<span data-ttu-id="d5af8-141">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5af8-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5af8-142">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d5af8-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5af8-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5af8-143">CommonParameters</span></span>
<span data-ttu-id="d5af8-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5af8-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5af8-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d5af8-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5af8-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d5af8-146">INPUTS</span></span>

### <span data-ttu-id="d5af8-147">System.String</span><span class="sxs-lookup"><span data-stu-id="d5af8-147">System.String</span></span>

### <span data-ttu-id="d5af8-148">System.Security.Cryptography.X509Certificates.X509Certificate2Collection</span><span class="sxs-lookup"><span data-stu-id="d5af8-148">System.Security.Cryptography.X509Certificates.X509Certificate2Collection</span></span>

### <span data-ttu-id="d5af8-149">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="d5af8-149">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d5af8-150">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d5af8-150">OUTPUTS</span></span>

### <span data-ttu-id="d5af8-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="d5af8-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="d5af8-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d5af8-152">NOTES</span></span>

## <span data-ttu-id="d5af8-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d5af8-153">RELATED LINKS</span></span>

[<span data-ttu-id="d5af8-154">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="d5af8-154">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

[<span data-ttu-id="d5af8-155">Tworzenie i scalanie obsługi klienta w magazynie kluczy</span><span class="sxs-lookup"><span data-stu-id="d5af8-155">Creating and merging CSR in Key Vault</span></span>](https://docs.microsoft.com/azure/key-vault/certificates/create-certificate-signing-request)