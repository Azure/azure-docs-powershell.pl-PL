---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 3BD243C7-A40E-4061-93FF-DDE7DECAD0A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultcertificateattribute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateAttribute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateAttribute.md
ms.openlocfilehash: 4aac9e7079451eebda0c77ae663666fbd55dc9e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525090"
---
# <span data-ttu-id="1f30d-101">Set-AzureKeyVaultCertificateAttribute</span><span class="sxs-lookup"><span data-stu-id="1f30d-101">Set-AzureKeyVaultCertificateAttribute</span></span>

## <span data-ttu-id="1f30d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1f30d-102">SYNOPSIS</span></span>
<span data-ttu-id="1f30d-103">Modyfikowanie atrybutów edytowalnych certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="1f30d-103">Modifies editable attributes of a certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f30d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1f30d-104">SYNTAX</span></span>

### <span data-ttu-id="1f30d-105">ByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1f30d-105">ByName (Default)</span></span>
```
Set-AzureKeyVaultCertificateAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-Enable <Boolean>] [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f30d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1f30d-106">ByInputObject</span></span>
```
Set-AzureKeyVaultCertificateAttribute [-InputObject] <PSKeyVaultCertificateIdentityItem> [[-Version] <String>]
 [-Enable <Boolean>] [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f30d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1f30d-107">DESCRIPTION</span></span>
<span data-ttu-id="1f30d-108">Polecenie cmdlet **Set-AzureKeyVaultCertificateAttribute** modyfikuje atrybuty edytowalne certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="1f30d-108">The **Set-AzureKeyVaultCertificateAttribute** cmdlet modifies the editable attributes of a certificate.</span></span>

## <span data-ttu-id="1f30d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1f30d-109">EXAMPLES</span></span>

### <span data-ttu-id="1f30d-110">Przykład 1. Modyfikowanie tagów skojarzonych z certyfikatem</span><span class="sxs-lookup"><span data-stu-id="1f30d-110">Example 1: Modify the tags associated with a certificate</span></span>
```
PS C:\>$Tags = @{ "Team" = "Azure" ; "Role" = "Engg" }
PS C:\> Set-AzureKeyVaultCertificateAttribute -VaultName "ContosoKV01" -Name "TestCert01" -Tag $Tags
PS C:\> Get-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
Name        : "TestCert01"
Certificate : [Subject]
                CN=AZURE

              [Issuer]
                CN=AZURE

              [Serial Number]
                5A2EF60501F241D6A4336841B36FEA41

              [Not Before]
                7/27/2016 6:50:01 PM

              [Not After]
                7/27/2018 7:00:01 PM

              [Thumbprint]
                A565D568082FEE2BE33B356ECC3703C2E9886555

Id          : https://ContosoKV01.vault.azure.net:443/certificates/tt02
KeyId       : https://ContosoKV01.vault.azure.net:443/keys/tt02
SecretId    : https://ContosoKV01.vault.azure.net:443/secrets/tt02
Thumbprint  : A565D568082FEE2BE33B356ECC3703C2E9886555
Tags        : {[Role, Engg], [Team, Azure]}
Enabled     : True
Created     : 7/28/2016 2:00:01 AM
Updated     : 8/1/2016 5:37:48 PM
```

<span data-ttu-id="1f30d-111">Pierwsze polecenie powoduje przypisanie tablicy par klucz/wartość do zmiennej $Tags.</span><span class="sxs-lookup"><span data-stu-id="1f30d-111">The first command assigns an array of key/value pairs to the $Tags variable.</span></span>

<span data-ttu-id="1f30d-112">Drugie polecenie ustawia wartość znacznika certyfikatu o nazwie TestCert01 na $Tags.</span><span class="sxs-lookup"><span data-stu-id="1f30d-112">The second command sets the tags value of the certificate named TestCert01 to be $Tags.</span></span>

<span data-ttu-id="1f30d-113">W poleceniu Final (ostatnie) jest wyświetlany certyfikat TestCert01, za pomocą polecenia cmdlet Get-AzureKeyVaultCertificate w celu weryfikacji operacji.</span><span class="sxs-lookup"><span data-stu-id="1f30d-113">The final command displays the TestCert01 certificate by using the Get-AzureKeyVaultCertificate cmdlet to verify the operation.</span></span>

## <span data-ttu-id="1f30d-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1f30d-114">PARAMETERS</span></span>

### <span data-ttu-id="1f30d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f30d-115">-DefaultProfile</span></span>
<span data-ttu-id="1f30d-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="1f30d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f30d-117">-Enable</span><span class="sxs-lookup"><span data-stu-id="1f30d-117">-Enable</span></span>
<span data-ttu-id="1f30d-118">Wskazuje, czy włączyć, czy wyłączyć certyfikat.</span><span class="sxs-lookup"><span data-stu-id="1f30d-118">Indicates whether to enable or disable a certificate.</span></span>
<span data-ttu-id="1f30d-119">Określ $True, aby włączyć lub $False wyłączyć.</span><span class="sxs-lookup"><span data-stu-id="1f30d-119">Specify $True to enable or $False to disable.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f30d-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1f30d-120">-InputObject</span></span>
<span data-ttu-id="1f30d-121">Obiekt Certificate</span><span class="sxs-lookup"><span data-stu-id="1f30d-121">Certificate object</span></span>

```yaml
Type: PSKeyVaultCertificateIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f30d-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1f30d-122">-Name</span></span>
<span data-ttu-id="1f30d-123">Określa nazwę certyfikatu do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="1f30d-123">Specifies the name of the certificate to modify.</span></span> <span data-ttu-id="1f30d-124">To polecenie cmdlet konstruuje nazwę FQDN certyfikatu na podstawie nazwy magazynu kluczy, obecnie wybranego środowiska, nazwy certyfikatu i wersji certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="1f30d-124">This cmdlet constructs the FQDN of a certificate based on the key vault name, your currently selected environment, the certificate name, and the certificate version.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f30d-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f30d-125">-PassThru</span></span>
<span data-ttu-id="1f30d-126">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="1f30d-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1f30d-127">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="1f30d-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1f30d-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="1f30d-128">-Tag</span></span>
<span data-ttu-id="1f30d-129">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="1f30d-129">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1f30d-130">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="1f30d-130">For example:</span></span>

<span data-ttu-id="1f30d-131">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="1f30d-131">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="1f30d-132">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="1f30d-132">-VaultName</span></span>
<span data-ttu-id="1f30d-133">Określa nazwę magazynu kluczy, w którym to polecenie cmdlet modyfikuje certyfikat.</span><span class="sxs-lookup"><span data-stu-id="1f30d-133">Specifies the key vault name in which this cmdlet modifies a certificate.</span></span>
<span data-ttu-id="1f30d-134">To polecenie cmdlet konstruuje nazwę FQDN magazynu kluczy na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="1f30d-134">This cmdlet constructs the FQDN of a key vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f30d-135">-Version</span><span class="sxs-lookup"><span data-stu-id="1f30d-135">-Version</span></span>
<span data-ttu-id="1f30d-136">Określa wersję certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="1f30d-136">Specifies the version of a certificate.</span></span>
<span data-ttu-id="1f30d-137">To polecenie cmdlet konstruuje nazwę FQDN certyfikatu na podstawie nazwy magazynu kluczy, obecnie wybranego środowiska, nazwy certyfikatu i wersji certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="1f30d-137">This cmdlet constructs the FQDN of a certificate based on the key vault name, your currently selected environment, the certificate name, and the certificate version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f30d-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1f30d-138">-Confirm</span></span>
<span data-ttu-id="1f30d-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f30d-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f30d-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f30d-140">-WhatIf</span></span>
<span data-ttu-id="1f30d-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f30d-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f30d-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1f30d-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f30d-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f30d-143">CommonParameters</span></span>
<span data-ttu-id="1f30d-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f30d-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f30d-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f30d-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f30d-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1f30d-146">INPUTS</span></span>

### <span data-ttu-id="1f30d-147">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="1f30d-147">None</span></span>
<span data-ttu-id="1f30d-148">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="1f30d-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1f30d-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1f30d-149">OUTPUTS</span></span>

### <span data-ttu-id="1f30d-150">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="1f30d-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="1f30d-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1f30d-151">NOTES</span></span>

## <span data-ttu-id="1f30d-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1f30d-152">RELATED LINKS</span></span>

[<span data-ttu-id="1f30d-153">Dodaj-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="1f30d-153">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)
