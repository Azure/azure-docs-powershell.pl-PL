---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: D4188DC6-A8AB-4B45-9781-94B74C338C63
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Import-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Import-AzureKeyVaultCertificate.md
ms.openlocfilehash: b97dc509ad6508c2cbec79d6ba1db27508f94c34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527545"
---
# <span data-ttu-id="15798-101">Import-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="15798-101">Import-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="15798-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="15798-102">SYNOPSIS</span></span>
<span data-ttu-id="15798-103">Importuje certyfikat do magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="15798-103">Imports a certificate to a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15798-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="15798-104">SYNTAX</span></span>

### <span data-ttu-id="15798-105">ImportCertificateFromFile (domyślny)</span><span class="sxs-lookup"><span data-stu-id="15798-105">ImportCertificateFromFile (Default)</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> -FilePath <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15798-106">ImportWithPrivateKeyFromFile</span><span class="sxs-lookup"><span data-stu-id="15798-106">ImportWithPrivateKeyFromFile</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> -FilePath <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="15798-107">ImportWithPrivateKeyFromString</span><span class="sxs-lookup"><span data-stu-id="15798-107">ImportWithPrivateKeyFromString</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> -CertificateString <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="15798-108">ImportWithPrivateKeyFromCollection</span><span class="sxs-lookup"><span data-stu-id="15798-108">ImportWithPrivateKeyFromCollection</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String>
 -CertificateCollection <X509Certificate2Collection> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15798-109">Opis</span><span class="sxs-lookup"><span data-stu-id="15798-109">DESCRIPTION</span></span>
<span data-ttu-id="15798-110">Polecenie cmdlet **Import-AzureKeyVaultCertificate** importuje certyfikat do magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="15798-110">The **Import-AzureKeyVaultCertificate** cmdlet imports a certificate into a key vault.</span></span>

<span data-ttu-id="15798-111">Możesz utworzyć certyfikat do zaimportowania, korzystając z jednej z następujących metod:</span><span class="sxs-lookup"><span data-stu-id="15798-111">You can create the certificate to import by using one of the following methods:</span></span>

- <span data-ttu-id="15798-112">Użyj polecenia cmdlet New-AzureKeyVaultCertificateSigningRequest, aby utworzyć żądanie podpisania certyfikatu i przesłać je do urzędu certyfikacji.</span><span class="sxs-lookup"><span data-stu-id="15798-112">Use the New-AzureKeyVaultCertificateSigningRequest cmdlet to create a certificate signing request and submit it to a certificate authority.</span></span>
- <span data-ttu-id="15798-113">Użyj istniejącego pliku pakietu certyfikatów, takiego jak plik PFX lub P12, zawierający zarówno certyfikat, jak i klucz prywatny.</span><span class="sxs-lookup"><span data-stu-id="15798-113">Use an existing certificate package file, such as a .pfx or .p12 file, which contains both the certificate and private key.</span></span>

## <span data-ttu-id="15798-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="15798-114">EXAMPLES</span></span>

### <span data-ttu-id="15798-115">Przykład 1: Importowanie certyfikatu magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="15798-115">Example 1: Import a key vault certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS C:\> Import-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "ImportCert01" -FilePath "C:\Users\contosoUser\Desktop\import.pfx" -Password $Password
Name        : importCert01
Certificate : [Subject]
                CN=contoso.com

              [Issuer]
                CN=contoso.com

              [Serial Number]
                05979C5A2F0741D5A3B6F97673E8A118

              [Not Before]
                2/8/2016 3:11:45 PM

              [Not After]
                8/8/2016 4:21:45 PM

              [Thumbprint]
                3E9B6848AD1834284157D68B060F748037F663C8

Thumbprint  : 3E9B6848AD1834284157D68B060F748037F663C8
Tags        :
Enabled     : True
Created     : 2/8/2016 11:50:43 PM
Updated     : 2/8/2016 11:50:43 PM
```

<span data-ttu-id="15798-116">W pierwszym poleceniu użyto polecenia cmdlet ConvertTo-SecureString, aby utworzyć bezpieczne hasło, a następnie przechowywać je w zmiennej $Password.</span><span class="sxs-lookup"><span data-stu-id="15798-116">The first command uses the ConvertTo-SecureString cmdlet to create a secure password, and then stores it in the $Password variable.</span></span>

<span data-ttu-id="15798-117">Drugie polecenie importuje certyfikat o nazwie ImportCert01 do magazynu kluczy CosotosoKV01.</span><span class="sxs-lookup"><span data-stu-id="15798-117">The second command imports the certificate named ImportCert01 into the CosotosoKV01 key vault.</span></span>

## <span data-ttu-id="15798-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="15798-118">PARAMETERS</span></span>

### <span data-ttu-id="15798-119">-CertificateCollection</span><span class="sxs-lookup"><span data-stu-id="15798-119">-CertificateCollection</span></span>
<span data-ttu-id="15798-120">Określa kolekcję certyfikatów, którą należy dodać do magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="15798-120">Specifies the certificate collection to add to a key vault.</span></span>

```yaml
Type: System.Security.Cryptography.X509Certificates.X509Certificate2Collection
Parameter Sets: ImportWithPrivateKeyFromCollection
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15798-121">-CertificateString</span><span class="sxs-lookup"><span data-stu-id="15798-121">-CertificateString</span></span>
<span data-ttu-id="15798-122">Określa ciąg certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="15798-122">Specifies a certificate string.</span></span>

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

### <span data-ttu-id="15798-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="15798-123">-Confirm</span></span>
<span data-ttu-id="15798-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15798-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15798-125">-FilePath</span><span class="sxs-lookup"><span data-stu-id="15798-125">-FilePath</span></span>
<span data-ttu-id="15798-126">Określa ścieżkę pliku certyfikatu, który został zaimportowany za pomocą tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15798-126">Specifies the path of the certificate file that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportCertificateFromFile, ImportWithPrivateKeyFromFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15798-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="15798-127">-Name</span></span>
<span data-ttu-id="15798-128">Określa nazwę certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="15798-128">Specifies the certificate name.</span></span> <span data-ttu-id="15798-129">To polecenie cmdlet konstruuje w pełni kwalifikowaną nazwę domeny (FQDN) certyfikatu z nazwy magazynu kluczy, obecnie wybranego środowiska i nazwy certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="15798-129">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate from key vault name, currently selected environment, and certificate name.</span></span>

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

### <span data-ttu-id="15798-130">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="15798-130">-Password</span></span>
<span data-ttu-id="15798-131">Określa hasło do pliku certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="15798-131">Specifies the password for a certificate file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ImportWithPrivateKeyFromFile, ImportWithPrivateKeyFromString
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15798-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="15798-132">-Tag</span></span>
<span data-ttu-id="15798-133">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="15798-133">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="15798-134">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="15798-134">For example:</span></span>

<span data-ttu-id="15798-135">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="15798-135">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="15798-136">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="15798-136">-VaultName</span></span>
<span data-ttu-id="15798-137">Określa nazwę magazynu kluczy, do którego to polecenie cmdlet importuje certyfikaty.</span><span class="sxs-lookup"><span data-stu-id="15798-137">Specifies the key vault name into which this cmdlet imports certificates.</span></span>
<span data-ttu-id="15798-138">To polecenie cmdlet tworzy w pełni kwalifikowaną nazwę domeny (FQDN) magazynu kluczy na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="15798-138">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="15798-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15798-139">-WhatIf</span></span>
<span data-ttu-id="15798-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15798-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15798-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="15798-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15798-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15798-142">-DefaultProfile</span></span>
<span data-ttu-id="15798-143">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="15798-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15798-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15798-144">CommonParameters</span></span>
<span data-ttu-id="15798-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15798-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15798-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15798-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15798-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="15798-147">INPUTS</span></span>

## <span data-ttu-id="15798-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="15798-148">OUTPUTS</span></span>

### <span data-ttu-id="15798-149">Microsoft. Azure. Commands. platforming. models. CertificateBundle</span><span class="sxs-lookup"><span data-stu-id="15798-149">Microsoft.Azure.Commands.KeyVault.Models.CertificateBundle</span></span>

## <span data-ttu-id="15798-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="15798-150">NOTES</span></span>

## <span data-ttu-id="15798-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="15798-151">RELATED LINKS</span></span>

[<span data-ttu-id="15798-152">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="15798-152">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)
