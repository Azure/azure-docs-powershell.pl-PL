---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 363FA51E-D075-4800-A4BE-BFF63FD25C90
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificate.md
ms.openlocfilehash: 87b030229eb2a1f4bb91122aaec8a119134d27fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542572"
---
# <span data-ttu-id="4bd33-101">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="4bd33-101">Get-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="4bd33-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4bd33-102">SYNOPSIS</span></span>
<span data-ttu-id="4bd33-103">Pobiera certyfikat z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="4bd33-103">Gets a certificate from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4bd33-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4bd33-104">SYNTAX</span></span>

### <span data-ttu-id="4bd33-105">ByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4bd33-105">ByName (Default)</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bd33-106">ByCertificateNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="4bd33-106">ByCertificateNameAndVersion</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bd33-107">ByCertificateAllVersions</span><span class="sxs-lookup"><span data-stu-id="4bd33-107">ByCertificateAllVersions</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bd33-108">ByNameInputObject</span><span class="sxs-lookup"><span data-stu-id="4bd33-108">ByNameInputObject</span></span>
```
Get-AzureKeyVaultCertificate [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bd33-109">ByCertificateNameAndVersionInputObject</span><span class="sxs-lookup"><span data-stu-id="4bd33-109">ByCertificateNameAndVersionInputObject</span></span>
```
Get-AzureKeyVaultCertificate [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bd33-110">ByCertificateAllVersionsInputObject</span><span class="sxs-lookup"><span data-stu-id="4bd33-110">ByCertificateAllVersionsInputObject</span></span>
```
Get-AzureKeyVaultCertificate [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4bd33-111">Opis</span><span class="sxs-lookup"><span data-stu-id="4bd33-111">DESCRIPTION</span></span>
<span data-ttu-id="4bd33-112">Polecenie cmdlet **Get-AzureKeyVaultCertificate** Pobiera określony certyfikat lub wersje certyfikatu z magazynu kluczy w magazynie kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4bd33-112">The **Get-AzureKeyVaultCertificate** cmdlet gets the specified certificate or the versions of a certificate from a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="4bd33-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4bd33-113">EXAMPLES</span></span>

### <span data-ttu-id="4bd33-114">Przykład 1: uzyskiwanie certyfikatu</span><span class="sxs-lookup"><span data-stu-id="4bd33-114">Example 1: Get a certificate</span></span>
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
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

<span data-ttu-id="4bd33-115">To polecenie pobiera certyfikat o nazwie TestCert01 z magazynu kluczy o nazwie ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="4bd33-115">This command gets the certificate named TestCert01 from the key vault named ContosoKV01.</span></span>

### <span data-ttu-id="4bd33-116">Przykład 2: Uzyskaj wszystkie certyfikaty, które zostały usunięte, ale nie zostały przeczyszczone dla tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="4bd33-116">Example 2: Get all the certificates that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="4bd33-117">To polecenie pobiera wszystkie certyfikaty, które zostały wcześniej usunięte, ale nie są usuwane, w magazynie kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="4bd33-117">This command gets all the certificates that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="4bd33-118">Przykład 3: pobiera certyfikat servicecert, który został usunięty, ale nie został odczyszczony dla tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="4bd33-118">Example 3: Gets the certificate MyCert that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="4bd33-119">To polecenie pobiera certyfikat o nazwie "Moje CERT", który został wcześniej usunięty, ale nie został przeczyszczony w magazynie kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="4bd33-119">This command gets the certificate named 'MyCert' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="4bd33-120">To polecenie zwróci metadane, takie jak Data usunięcia, oraz zaplanowaną datę przeczyszczania tego usuniętego certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="4bd33-120">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted certificate.</span></span>

## <span data-ttu-id="4bd33-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4bd33-121">PARAMETERS</span></span>

### <span data-ttu-id="4bd33-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bd33-122">-DefaultProfile</span></span>
<span data-ttu-id="4bd33-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="4bd33-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4bd33-124">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="4bd33-124">-IncludeVersions</span></span>
<span data-ttu-id="4bd33-125">Wskazuje, że ta operacja pobiera wszystkie wersje certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="4bd33-125">Indicates that this operation gets all versions of the certificate.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByCertificateAllVersions, ByCertificateAllVersionsInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bd33-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4bd33-126">-InputObject</span></span>
<span data-ttu-id="4bd33-127">Obiekt magazynu.</span><span class="sxs-lookup"><span data-stu-id="4bd33-127">KeyVault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByNameInputObject, ByCertificateNameAndVersionInputObject, ByCertificateAllVersionsInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4bd33-128">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="4bd33-128">-InRemovedState</span></span>
<span data-ttu-id="4bd33-129">Określa, czy w danych wyjściowych mają być uwzględniane uprzednio usunięte certyfikaty.</span><span class="sxs-lookup"><span data-stu-id="4bd33-129">Specifies whether to include previously deleted certificates in the output</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByName, ByNameInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bd33-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4bd33-130">-Name</span></span>
<span data-ttu-id="4bd33-131">Określa nazwę certyfikatu do pobrania.</span><span class="sxs-lookup"><span data-stu-id="4bd33-131">Specifies the name of the certificate to get.</span></span>

```yaml
Type: String
Parameter Sets: ByName, ByNameInputObject
Aliases: CertificateName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByCertificateNameAndVersion, ByCertificateAllVersions, ByCertificateNameAndVersionInputObject, ByCertificateAllVersionsInputObject
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bd33-132">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="4bd33-132">-VaultName</span></span>
<span data-ttu-id="4bd33-133">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="4bd33-133">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: ByName, ByCertificateNameAndVersion, ByCertificateAllVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bd33-134">-Version</span><span class="sxs-lookup"><span data-stu-id="4bd33-134">-Version</span></span>
<span data-ttu-id="4bd33-135">Określa wersję certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="4bd33-135">Specifies the version of a certificate.</span></span>

```yaml
Type: String
Parameter Sets: ByCertificateNameAndVersion, ByCertificateNameAndVersionInputObject
Aliases: CertificateVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bd33-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bd33-136">CommonParameters</span></span>
<span data-ttu-id="4bd33-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bd33-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bd33-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bd33-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bd33-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4bd33-139">INPUTS</span></span>

### <span data-ttu-id="4bd33-140">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="4bd33-140">None</span></span>
<span data-ttu-id="4bd33-141">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="4bd33-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4bd33-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4bd33-142">OUTPUTS</span></span>

### <span data-ttu-id="4bd33-143">System. Collections. Generic. list "1 [Microsoft. Azure. Commands. platforming. modele. PSKeyVaultCertificateIdentityItem]</span><span class="sxs-lookup"><span data-stu-id="4bd33-143">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem]</span></span>

### <span data-ttu-id="4bd33-144">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="4bd33-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="4bd33-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4bd33-145">NOTES</span></span>

## <span data-ttu-id="4bd33-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4bd33-146">RELATED LINKS</span></span>

[<span data-ttu-id="4bd33-147">Dodaj-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="4bd33-147">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)

[<span data-ttu-id="4bd33-148">Import — AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="4bd33-148">Import-AzureKeyVaultCertificate</span></span>](./Import-AzureKeyVaultCertificate.md)

[<span data-ttu-id="4bd33-149">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="4bd33-149">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)

[<span data-ttu-id="4bd33-150">Cofanie — AzureKeyVaultSecretCertificate</span><span class="sxs-lookup"><span data-stu-id="4bd33-150">Undo-AzureKeyVaultSecretCertificate</span></span>](./Undo-AzureKeyVaultSecretCertificate.md)
