---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: D4188DC6-A8AB-4B45-9781-94B74C338C63
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/import-azurekeyvaultcertificate
schema: 2.0.0
ms.openlocfilehash: 2903aa294830b8f9a39578374c1c108fe91c36e4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898917"
---
# <span data-ttu-id="24160-101">Import-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="24160-101">Import-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="24160-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="24160-102">SYNOPSIS</span></span>
<span data-ttu-id="24160-103">Importuje certyfikat do magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="24160-103">Imports a certificate to a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24160-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="24160-104">SYNTAX</span></span>

### <span data-ttu-id="24160-105">ImportCertificateFromFile (domyślny)</span><span class="sxs-lookup"><span data-stu-id="24160-105">ImportCertificateFromFile (Default)</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> -FilePath <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24160-106">ImportWithPrivateKeyFromFile</span><span class="sxs-lookup"><span data-stu-id="24160-106">ImportWithPrivateKeyFromFile</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> -FilePath <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="24160-107">ImportWithPrivateKeyFromString</span><span class="sxs-lookup"><span data-stu-id="24160-107">ImportWithPrivateKeyFromString</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> -CertificateString <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="24160-108">ImportWithPrivateKeyFromCollection</span><span class="sxs-lookup"><span data-stu-id="24160-108">ImportWithPrivateKeyFromCollection</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String>
 -CertificateCollection <X509Certificate2Collection> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24160-109">Opis</span><span class="sxs-lookup"><span data-stu-id="24160-109">DESCRIPTION</span></span>
<span data-ttu-id="24160-110">Polecenie cmdlet **Import-AzureKeyVaultCertificate** importuje certyfikat do magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="24160-110">The **Import-AzureKeyVaultCertificate** cmdlet imports a certificate into a key vault.</span></span>

<span data-ttu-id="24160-111">Możesz utworzyć certyfikat do zaimportowania, korzystając z jednej z następujących metod:</span><span class="sxs-lookup"><span data-stu-id="24160-111">You can create the certificate to import by using one of the following methods:</span></span>

- <span data-ttu-id="24160-112">Użyj polecenia cmdlet New-AzureKeyVaultCertificateSigningRequest, aby utworzyć żądanie podpisania certyfikatu i przesłać je do urzędu certyfikacji.</span><span class="sxs-lookup"><span data-stu-id="24160-112">Use the New-AzureKeyVaultCertificateSigningRequest cmdlet to create a certificate signing request and submit it to a certificate authority.</span></span>
- <span data-ttu-id="24160-113">Użyj istniejącego pliku pakietu certyfikatów, takiego jak plik PFX lub P12, zawierający zarówno certyfikat, jak i klucz prywatny.</span><span class="sxs-lookup"><span data-stu-id="24160-113">Use an existing certificate package file, such as a .pfx or .p12 file, which contains both the certificate and private key.</span></span>

## <span data-ttu-id="24160-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="24160-114">EXAMPLES</span></span>

### <span data-ttu-id="24160-115">Przykład 1: Importowanie certyfikatu magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="24160-115">Example 1: Import a key vault certificate</span></span>
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

<span data-ttu-id="24160-116">W pierwszym poleceniu użyto polecenia cmdlet ConvertTo-SecureString, aby utworzyć bezpieczne hasło, a następnie przechowywać je w zmiennej $Password.</span><span class="sxs-lookup"><span data-stu-id="24160-116">The first command uses the ConvertTo-SecureString cmdlet to create a secure password, and then stores it in the $Password variable.</span></span>

<span data-ttu-id="24160-117">Drugie polecenie importuje certyfikat o nazwie ImportCert01 do magazynu kluczy CosotosoKV01.</span><span class="sxs-lookup"><span data-stu-id="24160-117">The second command imports the certificate named ImportCert01 into the CosotosoKV01 key vault.</span></span>

## <span data-ttu-id="24160-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="24160-118">PARAMETERS</span></span>

### <span data-ttu-id="24160-119">-CertificateCollection</span><span class="sxs-lookup"><span data-stu-id="24160-119">-CertificateCollection</span></span>
<span data-ttu-id="24160-120">Określa kolekcję certyfikatów, którą należy dodać do magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="24160-120">Specifies the certificate collection to add to a key vault.</span></span>

```yaml
Type: X509Certificate2Collection
Parameter Sets: ImportWithPrivateKeyFromCollection
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24160-121">-CertificateString</span><span class="sxs-lookup"><span data-stu-id="24160-121">-CertificateString</span></span>
<span data-ttu-id="24160-122">Określa ciąg certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="24160-122">Specifies a certificate string.</span></span>

```yaml
Type: String
Parameter Sets: ImportWithPrivateKeyFromString
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24160-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24160-123">-DefaultProfile</span></span>
<span data-ttu-id="24160-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="24160-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="24160-125">-FilePath</span><span class="sxs-lookup"><span data-stu-id="24160-125">-FilePath</span></span>
<span data-ttu-id="24160-126">Określa ścieżkę pliku certyfikatu, który został zaimportowany za pomocą tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24160-126">Specifies the path of the certificate file that this cmdlet imports.</span></span>

```yaml
Type: String
Parameter Sets: ImportCertificateFromFile, ImportWithPrivateKeyFromFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24160-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="24160-127">-Name</span></span>
<span data-ttu-id="24160-128">Określa nazwę certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="24160-128">Specifies the certificate name.</span></span> <span data-ttu-id="24160-129">To polecenie cmdlet konstruuje w pełni kwalifikowaną nazwę domeny (FQDN) certyfikatu z nazwy magazynu kluczy, obecnie wybranego środowiska i nazwy certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="24160-129">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate from key vault name, currently selected environment, and certificate name.</span></span>

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

### <span data-ttu-id="24160-130">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="24160-130">-Password</span></span>
<span data-ttu-id="24160-131">Określa hasło do pliku certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="24160-131">Specifies the password for a certificate file.</span></span>

```yaml
Type: SecureString
Parameter Sets: ImportWithPrivateKeyFromFile, ImportWithPrivateKeyFromString
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24160-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="24160-132">-Tag</span></span>
<span data-ttu-id="24160-133">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="24160-133">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="24160-134">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="24160-134">For example:</span></span>

<span data-ttu-id="24160-135">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="24160-135">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24160-136">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="24160-136">-VaultName</span></span>
<span data-ttu-id="24160-137">Określa nazwę magazynu kluczy, do którego to polecenie cmdlet importuje certyfikaty.</span><span class="sxs-lookup"><span data-stu-id="24160-137">Specifies the key vault name into which this cmdlet imports certificates.</span></span>
<span data-ttu-id="24160-138">To polecenie cmdlet tworzy w pełni kwalifikowaną nazwę domeny (FQDN) magazynu kluczy na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="24160-138">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="24160-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="24160-139">-Confirm</span></span>
<span data-ttu-id="24160-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24160-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24160-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24160-141">-WhatIf</span></span>
<span data-ttu-id="24160-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24160-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24160-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="24160-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24160-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24160-144">CommonParameters</span></span>
<span data-ttu-id="24160-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24160-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24160-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24160-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24160-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="24160-147">INPUTS</span></span>

## <span data-ttu-id="24160-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="24160-148">OUTPUTS</span></span>

### <span data-ttu-id="24160-149">Microsoft. Azure. Commands. platforming. models. CertificateBundle</span><span class="sxs-lookup"><span data-stu-id="24160-149">Microsoft.Azure.Commands.KeyVault.Models.CertificateBundle</span></span>

## <span data-ttu-id="24160-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="24160-150">NOTES</span></span>

## <span data-ttu-id="24160-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="24160-151">RELATED LINKS</span></span>

[<span data-ttu-id="24160-152">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="24160-152">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)
