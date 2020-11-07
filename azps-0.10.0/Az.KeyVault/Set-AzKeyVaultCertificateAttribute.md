---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 3BD243C7-A40E-4061-93FF-DDE7DECAD0A7
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/set-AzKeyvaultcertificateattribute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateAttribute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateAttribute.md
ms.openlocfilehash: 9297e523e623542c19df1915d3da29d9e39cec40
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893010"
---
# <span data-ttu-id="85687-101">Set-AzKeyVaultCertificateAttribute</span><span class="sxs-lookup"><span data-stu-id="85687-101">Set-AzKeyVaultCertificateAttribute</span></span>

## <span data-ttu-id="85687-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="85687-102">SYNOPSIS</span></span>
<span data-ttu-id="85687-103">Modyfikowanie atrybutów edytowalnych certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="85687-103">Modifies editable attributes of a certificate.</span></span>

## <span data-ttu-id="85687-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="85687-104">SYNTAX</span></span>

```
Set-AzKeyVaultCertificateAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-Enable <Boolean>] [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85687-105">Opis</span><span class="sxs-lookup"><span data-stu-id="85687-105">DESCRIPTION</span></span>
<span data-ttu-id="85687-106">Polecenie cmdlet **Set-AzKeyVaultCertificateAttribute** modyfikuje atrybuty edytowalne certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="85687-106">The **Set-AzKeyVaultCertificateAttribute** cmdlet modifies the editable attributes of a certificate.</span></span>

## <span data-ttu-id="85687-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="85687-107">EXAMPLES</span></span>

### <span data-ttu-id="85687-108">Przykład 1. Modyfikowanie tagów skojarzonych z certyfikatem</span><span class="sxs-lookup"><span data-stu-id="85687-108">Example 1: Modify the tags associated with a certificate</span></span>
```
PS C:\>$Tags = @{ "Team" = "Azure" ; "Role" = "Engg" }
PS C:\> Set-AzKeyVaultCertificateAttribute -VaultName "ContosoKV01" -Name "TestCert01" -Tag $Tags
PS C:\> Get-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
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

<span data-ttu-id="85687-109">Pierwsze polecenie powoduje przypisanie tablicy par klucz/wartość do zmiennej $Tags.</span><span class="sxs-lookup"><span data-stu-id="85687-109">The first command assigns an array of key/value pairs to the $Tags variable.</span></span>

<span data-ttu-id="85687-110">Drugie polecenie ustawia wartość znacznika certyfikatu o nazwie TestCert01 na $Tags.</span><span class="sxs-lookup"><span data-stu-id="85687-110">The second command sets the tags value of the certificate named TestCert01 to be $Tags.</span></span>

<span data-ttu-id="85687-111">W poleceniu Final (ostatnie) jest wyświetlany certyfikat TestCert01, za pomocą polecenia cmdlet Get-AzKeyVaultCertificate w celu weryfikacji operacji.</span><span class="sxs-lookup"><span data-stu-id="85687-111">The final command displays the TestCert01 certificate by using the Get-AzKeyVaultCertificate cmdlet to verify the operation.</span></span>

## <span data-ttu-id="85687-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="85687-112">PARAMETERS</span></span>

### <span data-ttu-id="85687-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85687-113">-DefaultProfile</span></span>
<span data-ttu-id="85687-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="85687-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85687-115">-Enable</span><span class="sxs-lookup"><span data-stu-id="85687-115">-Enable</span></span>
<span data-ttu-id="85687-116">Wskazuje, czy włączyć, czy wyłączyć certyfikat.</span><span class="sxs-lookup"><span data-stu-id="85687-116">Indicates whether to enable or disable a certificate.</span></span>
<span data-ttu-id="85687-117">Określ $True, aby włączyć lub $False wyłączyć.</span><span class="sxs-lookup"><span data-stu-id="85687-117">Specify $True to enable or $False to disable.</span></span>

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

### <span data-ttu-id="85687-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="85687-118">-Name</span></span>
<span data-ttu-id="85687-119">Określa nazwę certyfikatu do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="85687-119">Specifies the name of the certificate to modify.</span></span> <span data-ttu-id="85687-120">To polecenie cmdlet konstruuje nazwę FQDN certyfikatu na podstawie nazwy magazynu kluczy, obecnie wybranego środowiska, nazwy certyfikatu i wersji certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="85687-120">This cmdlet constructs the FQDN of a certificate based on the key vault name, your currently selected environment, the certificate name, and the certificate version.</span></span>

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

### <span data-ttu-id="85687-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="85687-121">-PassThru</span></span>
<span data-ttu-id="85687-122">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="85687-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="85687-123">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="85687-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="85687-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="85687-124">-Tag</span></span>
<span data-ttu-id="85687-125">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="85687-125">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="85687-126">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="85687-126">For example:</span></span>

<span data-ttu-id="85687-127">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="85687-127">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="85687-128">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="85687-128">-VaultName</span></span>
<span data-ttu-id="85687-129">Określa nazwę magazynu kluczy, w którym to polecenie cmdlet modyfikuje certyfikat.</span><span class="sxs-lookup"><span data-stu-id="85687-129">Specifies the key vault name in which this cmdlet modifies a certificate.</span></span>
<span data-ttu-id="85687-130">To polecenie cmdlet konstruuje nazwę FQDN magazynu kluczy na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="85687-130">This cmdlet constructs the FQDN of a key vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="85687-131">-Version</span><span class="sxs-lookup"><span data-stu-id="85687-131">-Version</span></span>
<span data-ttu-id="85687-132">Określa wersję certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="85687-132">Specifies the version of a certificate.</span></span>
<span data-ttu-id="85687-133">To polecenie cmdlet konstruuje nazwę FQDN certyfikatu na podstawie nazwy magazynu kluczy, obecnie wybranego środowiska, nazwy certyfikatu i wersji certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="85687-133">This cmdlet constructs the FQDN of a certificate based on the key vault name, your currently selected environment, the certificate name, and the certificate version.</span></span>

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

### <span data-ttu-id="85687-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="85687-134">-Confirm</span></span>
<span data-ttu-id="85687-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85687-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85687-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85687-136">-WhatIf</span></span>
<span data-ttu-id="85687-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85687-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85687-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="85687-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85687-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85687-139">CommonParameters</span></span>
<span data-ttu-id="85687-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85687-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85687-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85687-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85687-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="85687-142">INPUTS</span></span>

### <span data-ttu-id="85687-143">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="85687-143">None</span></span>
<span data-ttu-id="85687-144">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="85687-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="85687-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="85687-145">OUTPUTS</span></span>

### <span data-ttu-id="85687-146">Microsoft. Azure. Commands. platforming. models. KeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="85687-146">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificate</span></span>

## <span data-ttu-id="85687-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="85687-147">NOTES</span></span>

## <span data-ttu-id="85687-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="85687-148">RELATED LINKS</span></span>

[<span data-ttu-id="85687-149">Dodaj-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="85687-149">Add-AzKeyVaultCertificate</span></span>](./Add-AzKeyVaultCertificate.md)
