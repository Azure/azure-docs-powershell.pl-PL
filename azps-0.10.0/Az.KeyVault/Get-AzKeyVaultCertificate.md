---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 363FA51E-D075-4800-A4BE-BFF63FD25C90
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
ms.openlocfilehash: 40514bdd6ed8d37679d3002f80146e622a0614e9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891314"
---
# <span data-ttu-id="d0518-101">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="d0518-101">Get-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="d0518-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d0518-102">SYNOPSIS</span></span>
<span data-ttu-id="d0518-103">Pobiera certyfikat z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="d0518-103">Gets a certificate from a key vault.</span></span>

## <span data-ttu-id="d0518-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d0518-104">SYNTAX</span></span>

### <span data-ttu-id="d0518-105">ByVaultName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d0518-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d0518-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="d0518-106">ByCertificateName</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0518-107">ByCertificateVersions</span><span class="sxs-lookup"><span data-stu-id="d0518-107">ByCertificateVersions</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0518-108">ByDeletedCertificates</span><span class="sxs-lookup"><span data-stu-id="d0518-108">ByDeletedCertificates</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0518-109">Opis</span><span class="sxs-lookup"><span data-stu-id="d0518-109">DESCRIPTION</span></span>
<span data-ttu-id="d0518-110">Polecenie cmdlet **Get-AzKeyVaultCertificate** Pobiera określony certyfikat lub wersje certyfikatu z magazynu kluczy w magazynie kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d0518-110">The **Get-AzKeyVaultCertificate** cmdlet gets the specified certificate or the versions of a certificate from a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="d0518-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d0518-111">EXAMPLES</span></span>

### <span data-ttu-id="d0518-112">Przykład 1: uzyskiwanie certyfikatu</span><span class="sxs-lookup"><span data-stu-id="d0518-112">Example 1: Get a certificate</span></span>
```
PS C:\>Get-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
Name        : testCert01
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
Created     : 2/8/2016 11:21:45 PM
Updated     : 2/8/2016 11:21:45 PM
```

<span data-ttu-id="d0518-113">To polecenie pobiera certyfikat o nazwie TestCert01 z magazynu kluczy o nazwie ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="d0518-113">This command gets the certificate named TestCert01 from the key vault named ContosoKV01.</span></span>

### <span data-ttu-id="d0518-114">Przykład 2: Uzyskaj wszystkie certyfikaty, które zostały usunięte, ale nie zostały przeczyszczone dla tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="d0518-114">Example 2: Get all the certificates that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzKeyVaultCertificate -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="d0518-115">To polecenie pobiera wszystkie certyfikaty, które zostały wcześniej usunięte, ale nie są usuwane, w magazynie kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="d0518-115">This command gets all the certificates that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="d0518-116">Przykład 3: pobiera certyfikat servicecert, który został usunięty, ale nie został odczyszczony dla tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="d0518-116">Example 3: Gets the certificate MyCert that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="d0518-117">To polecenie pobiera certyfikat o nazwie "Moje CERT", który został wcześniej usunięty, ale nie został przeczyszczony w magazynie kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="d0518-117">This command gets the certificate named 'MyCert' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="d0518-118">To polecenie zwróci metadane, takie jak Data usunięcia, oraz zaplanowaną datę przeczyszczania tego usuniętego certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="d0518-118">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted certificate.</span></span>

## <span data-ttu-id="d0518-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d0518-119">PARAMETERS</span></span>

### <span data-ttu-id="d0518-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0518-120">-DefaultProfile</span></span>
<span data-ttu-id="d0518-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d0518-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d0518-122">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="d0518-122">-IncludeVersions</span></span>
<span data-ttu-id="d0518-123">Wskazuje, że ta operacja pobiera wszystkie wersje certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="d0518-123">Indicates that this operation gets all versions of the certificate.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByCertificateVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0518-124">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="d0518-124">-InRemovedState</span></span>
<span data-ttu-id="d0518-125">Określa, czy w danych wyjściowych mają być uwzględniane uprzednio usunięte certyfikaty.</span><span class="sxs-lookup"><span data-stu-id="d0518-125">Specifies whether to include previously deleted certificates in the output</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedCertificates
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0518-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d0518-126">-Name</span></span>
<span data-ttu-id="d0518-127">Określa nazwę certyfikatu do pobrania.</span><span class="sxs-lookup"><span data-stu-id="d0518-127">Specifies the name of the certificate to get.</span></span>

```yaml
Type: String
Parameter Sets: ByCertificateName, ByCertificateVersions
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedCertificates
Aliases: CertificateName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0518-128">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="d0518-128">-VaultName</span></span>
<span data-ttu-id="d0518-129">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="d0518-129">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="d0518-130">-Version</span><span class="sxs-lookup"><span data-stu-id="d0518-130">-Version</span></span>
<span data-ttu-id="d0518-131">Określa wersję certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="d0518-131">Specifies the version of a certificate.</span></span>

```yaml
Type: String
Parameter Sets: ByCertificateName
Aliases: CertificateVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0518-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0518-132">CommonParameters</span></span>
<span data-ttu-id="d0518-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0518-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0518-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0518-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0518-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d0518-135">INPUTS</span></span>

### <span data-ttu-id="d0518-136">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d0518-136">None</span></span>
<span data-ttu-id="d0518-137">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="d0518-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d0518-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d0518-138">OUTPUTS</span></span>

### <span data-ttu-id="d0518-139">System. Collections. Generic. list "1 [Microsoft. Azure. Commands. platforming. modele. CertificateIdentityItem]</span><span class="sxs-lookup"><span data-stu-id="d0518-139">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.CertificateIdentityItem]</span></span>

### <span data-ttu-id="d0518-140">Microsoft. Azure. Commands. platforming. models. KeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="d0518-140">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificate</span></span>

## <span data-ttu-id="d0518-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d0518-141">NOTES</span></span>

## <span data-ttu-id="d0518-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d0518-142">RELATED LINKS</span></span>

[<span data-ttu-id="d0518-143">Dodaj-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="d0518-143">Add-AzKeyVaultCertificate</span></span>](./Add-AzKeyVaultCertificate.md)

[<span data-ttu-id="d0518-144">Import — AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="d0518-144">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="d0518-145">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="d0518-145">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

[<span data-ttu-id="d0518-146">Cofanie — AzKeyVaultSecretCertificate</span><span class="sxs-lookup"><span data-stu-id="d0518-146">Undo-AzKeyVaultSecretCertificate</span></span>](./Undo-AzKeyVaultSecretCertificate.md)
