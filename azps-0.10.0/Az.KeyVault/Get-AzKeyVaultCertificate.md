---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 363FA51E-D075-4800-A4BE-BFF63FD25C90
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
ms.openlocfilehash: babd3d8a42ddbd740c8189a41de76c78170ecae5
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398822"
---
# <span data-ttu-id="fe012-101">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="fe012-101">Get-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="fe012-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe012-102">SYNOPSIS</span></span>
<span data-ttu-id="fe012-103">Pobiera certyfikat z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="fe012-103">Gets a certificate from a key vault.</span></span>

## <span data-ttu-id="fe012-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fe012-104">SYNTAX</span></span>

### <span data-ttu-id="fe012-105">ByVaultName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="fe012-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fe012-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="fe012-106">ByCertificateName</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe012-107">ByCertificateVersions</span><span class="sxs-lookup"><span data-stu-id="fe012-107">ByCertificateVersions</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe012-108">ByDeletedCertificates</span><span class="sxs-lookup"><span data-stu-id="fe012-108">ByDeletedCertificates</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe012-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="fe012-109">DESCRIPTION</span></span>
<span data-ttu-id="fe012-110">Polecenie **cmdlet Get-AzKeyVaultCertificate** pobiera określony certyfikat lub wersje certyfikatu z magazynu kluczy w magazynie kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fe012-110">The **Get-AzKeyVaultCertificate** cmdlet gets the specified certificate or the versions of a certificate from a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="fe012-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fe012-111">EXAMPLES</span></span>

### <span data-ttu-id="fe012-112">Przykład 1. Uzyskiwanie certyfikatu</span><span class="sxs-lookup"><span data-stu-id="fe012-112">Example 1: Get a certificate</span></span>
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

<span data-ttu-id="fe012-113">To polecenie pobiera certyfikat o nazwie TestCert01 z magazynu kluczy o nazwie ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="fe012-113">This command gets the certificate named TestCert01 from the key vault named ContosoKV01.</span></span>

### <span data-ttu-id="fe012-114">Przykład 2. Pobierz wszystkie certyfikaty, które zostały usunięte, ale nie są czyszone dla tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="fe012-114">Example 2: Get all the certificates that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzKeyVaultCertificate -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="fe012-115">To polecenie pobiera wszystkie certyfikaty, które zostały wcześniej usunięte, ale nie przeczyszono, w magazynie kluczy o nazwie Contoso.</span><span class="sxs-lookup"><span data-stu-id="fe012-115">This command gets all the certificates that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="fe012-116">Przykład 3. Pobiera certyfikat MyCert, który został usunięty, ale nie został przeczyszony dla tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="fe012-116">Example 3: Gets the certificate MyCert that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="fe012-117">To polecenie pobiera certyfikat o nazwie "MyCert", który został wcześniej usunięty, ale nie przeczyszczony, w magazynie kluczy o nazwie Contoso.</span><span class="sxs-lookup"><span data-stu-id="fe012-117">This command gets the certificate named 'MyCert' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="fe012-118">To polecenie zwróci metadane, takie jak data usunięcia i zaplanowana data usunięcia tego usuniętego certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="fe012-118">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted certificate.</span></span>

## <span data-ttu-id="fe012-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe012-119">PARAMETERS</span></span>

### <span data-ttu-id="fe012-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe012-120">-DefaultProfile</span></span>
<span data-ttu-id="fe012-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="fe012-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fe012-122">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="fe012-122">-IncludeVersions</span></span>
<span data-ttu-id="fe012-123">Wskazuje, że ta operacja pobiera wszystkie wersje certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="fe012-123">Indicates that this operation gets all versions of the certificate.</span></span>

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

### <span data-ttu-id="fe012-124">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="fe012-124">-InRemovedState</span></span>
<span data-ttu-id="fe012-125">Określa, czy do danych wyjściowych mają być dołączane usunięte wcześniej certyfikaty</span><span class="sxs-lookup"><span data-stu-id="fe012-125">Specifies whether to include previously deleted certificates in the output</span></span>

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

### <span data-ttu-id="fe012-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="fe012-126">-Name</span></span>
<span data-ttu-id="fe012-127">Określa nazwę certyfikatu do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="fe012-127">Specifies the name of the certificate to get.</span></span>

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

### <span data-ttu-id="fe012-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="fe012-128">-VaultName</span></span>
<span data-ttu-id="fe012-129">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="fe012-129">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="fe012-130">— Wersja</span><span class="sxs-lookup"><span data-stu-id="fe012-130">-Version</span></span>
<span data-ttu-id="fe012-131">Określa wersję certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="fe012-131">Specifies the version of a certificate.</span></span>

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

### <span data-ttu-id="fe012-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe012-132">CommonParameters</span></span>
<span data-ttu-id="fe012-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe012-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe012-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe012-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe012-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe012-135">INPUTS</span></span>

### <span data-ttu-id="fe012-136">Brak</span><span class="sxs-lookup"><span data-stu-id="fe012-136">None</span></span>
<span data-ttu-id="fe012-137">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="fe012-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fe012-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fe012-138">OUTPUTS</span></span>

### <span data-ttu-id="fe012-139">System.Collections.generic.List'1[Microsoft.Azure.Commands.KeyVault.Models.CertificateIdentityItem]</span><span class="sxs-lookup"><span data-stu-id="fe012-139">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.CertificateIdentityItem]</span></span>

### <span data-ttu-id="fe012-140">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="fe012-140">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificate</span></span>

## <span data-ttu-id="fe012-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fe012-141">NOTES</span></span>

## <span data-ttu-id="fe012-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fe012-142">RELATED LINKS</span></span>

[<span data-ttu-id="fe012-143">Add-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="fe012-143">Add-AzKeyVaultCertificate</span></span>](./Add-AzKeyVaultCertificate.md)

[<span data-ttu-id="fe012-144">Import-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="fe012-144">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="fe012-145">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="fe012-145">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

