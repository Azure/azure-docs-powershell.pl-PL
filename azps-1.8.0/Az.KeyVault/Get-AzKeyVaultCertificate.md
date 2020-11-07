---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 363FA51E-D075-4800-A4BE-BFF63FD25C90
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
ms.openlocfilehash: 5935706c341fac5f0b26d3e4965f226342c3dfc8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868004"
---
# <span data-ttu-id="bfeda-101">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="bfeda-101">Get-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="bfeda-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bfeda-102">SYNOPSIS</span></span>
<span data-ttu-id="bfeda-103">Pobiera certyfikat z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="bfeda-103">Gets a certificate from a key vault.</span></span>

## <span data-ttu-id="bfeda-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bfeda-104">SYNTAX</span></span>

### <span data-ttu-id="bfeda-105">ByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bfeda-105">ByName (Default)</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [[-Name] <String>] [-InRemovedState] [-IncludePending]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bfeda-106">ByCertificateNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="bfeda-106">ByCertificateNameAndVersion</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bfeda-107">ByCertificateAllVersions</span><span class="sxs-lookup"><span data-stu-id="bfeda-107">ByCertificateAllVersions</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bfeda-108">ByNameInputObject</span><span class="sxs-lookup"><span data-stu-id="bfeda-108">ByNameInputObject</span></span>
```
Get-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState] [-IncludePending]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bfeda-109">ByCertificateNameAndVersionInputObject</span><span class="sxs-lookup"><span data-stu-id="bfeda-109">ByCertificateNameAndVersionInputObject</span></span>
```
Get-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bfeda-110">ByCertificateAllVersionsInputObject</span><span class="sxs-lookup"><span data-stu-id="bfeda-110">ByCertificateAllVersionsInputObject</span></span>
```
Get-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bfeda-111">ByNameResourceId</span><span class="sxs-lookup"><span data-stu-id="bfeda-111">ByNameResourceId</span></span>
```
Get-AzKeyVaultCertificate [-ResourceId] <String> [[-Name] <String>] [-InRemovedState] [-IncludePending]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bfeda-112">ByCertificateNameAndVersionResourceId</span><span class="sxs-lookup"><span data-stu-id="bfeda-112">ByCertificateNameAndVersionResourceId</span></span>
```
Get-AzKeyVaultCertificate [-ResourceId] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bfeda-113">ByCertificateAllVersionsResourceId</span><span class="sxs-lookup"><span data-stu-id="bfeda-113">ByCertificateAllVersionsResourceId</span></span>
```
Get-AzKeyVaultCertificate [-ResourceId] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bfeda-114">Opis</span><span class="sxs-lookup"><span data-stu-id="bfeda-114">DESCRIPTION</span></span>
<span data-ttu-id="bfeda-115">Polecenie cmdlet **Get-AzKeyVaultCertificate** Pobiera określony certyfikat lub wersje certyfikatu z magazynu kluczy w magazynie kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bfeda-115">The **Get-AzKeyVaultCertificate** cmdlet gets the specified certificate or the versions of a certificate from a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="bfeda-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bfeda-116">EXAMPLES</span></span>

### <span data-ttu-id="bfeda-117">Przykład 1: uzyskiwanie certyfikatu</span><span class="sxs-lookup"><span data-stu-id="bfeda-117">Example 1: Get a certificate</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
Name        : testCert01
Certificate : [Subject] 
                CN=contoso.com

              [Issuer] 
                CN=contoso.com

              [Serial Number] 
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

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

<span data-ttu-id="bfeda-118">To polecenie pobiera certyfikat o nazwie TestCert01 z magazynu kluczy o nazwie ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="bfeda-118">This command gets the certificate named TestCert01 from the key vault named ContosoKV01.</span></span>

### <span data-ttu-id="bfeda-119">Przykład 2: Uzyskaj wszystkie certyfikaty, które zostały usunięte, ale nie zostały przeczyszczone dla tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="bfeda-119">Example 2: Get all the certificates that have been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificate -VaultName 'contoso' -InRemovedState

DeletedDate        : 5/24/2018 6:08:32 PM
Enabled            : True
Expires            : 11/24/2018 6:08:13 PM
NotBefore          : 5/24/2018 5:58:13 PM
Created            : 5/24/2018 6:08:13 PM
Updated            : 5/24/2018 6:08:13 PM
Tags               :
VaultName          : contoso
Name               : test1
Version            :
Id                 : https://contoso.vault.azure.net:443/certificates/test1

ScheduledPurgeDate : 8/22/2018 6:10:47 PM
DeletedDate        : 5/24/2018 6:10:47 PM
Enabled            : True
Expires            : 11/24/2018 6:09:44 PM
NotBefore          : 5/24/2018 5:59:44 PM
Created            : 5/24/2018 6:09:44 PM
Updated            : 5/24/2018 6:09:44 PM
Tags               :
VaultName          : contoso
Name               : test2
Version            :
Id                 : https://contoso.vault.azure.net:443/certificates/test2
```

<span data-ttu-id="bfeda-120">To polecenie pobiera wszystkie certyfikaty, które zostały wcześniej usunięte, ale nie są usuwane, w magazynie kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="bfeda-120">This command gets all the certificates that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="bfeda-121">Przykład 3: pobiera certyfikat servicecert, który został usunięty, ale nie został odczyszczony dla tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="bfeda-121">Example 3: Gets the certificate MyCert that has been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificate -VaultName 'contoso' -Name 'test1' -InRemovedState

Certificate        : [Subject]
                       CN=contoso.com

                     [Issuer]
                       CN=contoso.com

                     [Serial Number]
                       XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

                     [Not Before]
                       5/24/2018 10:58:13 AM

                     [Not After]
                       11/24/2018 10:08:13 AM

                     [Thumbprint]
                       XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

KeyId              : https://contoso.vault.azure.net:443/keys/test1/7fe415d5518240c1a6fce89986b8d334
SecretId           : https://contoso.vault.azure.net:443/secrets/test1/7fe415d5518240c1a6fce89986b8d334
Thumbprint         : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
RecoveryLevel      : Recoverable+Purgeable
ScheduledPurgeDate : 8/22/2018 6:08:32 PM
DeletedDate        : 5/24/2018 6:08:32 PM
Enabled            : True
Expires            : 11/24/2018 6:08:13 PM
NotBefore          : 5/24/2018 5:58:13 PM
Created            : 5/24/2018 6:08:13 PM
Updated            : 5/24/2018 6:08:13 PM
Tags               :
VaultName          : contoso
Name               : test1
Version            : 7fe415d5518240c1a6fce89986b8d334
Id                 : https://contoso.vault.azure.net:443/certificates/test1/7fe415d5518240c1a6fce89986b8d334
```

<span data-ttu-id="bfeda-122">To polecenie pobiera certyfikat o nazwie "Moje CERT", który został wcześniej usunięty, ale nie został przeczyszczony w magazynie kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="bfeda-122">This command gets the certificate named 'MyCert' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="bfeda-123">To polecenie zwróci metadane, takie jak Data usunięcia, oraz zaplanowaną datę przeczyszczania tego usuniętego certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="bfeda-123">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted certificate.</span></span>

### <span data-ttu-id="bfeda-124">Przykład 4: Wyświetlanie listy certyfikatów przy użyciu funkcji filtrowania</span><span class="sxs-lookup"><span data-stu-id="bfeda-124">Example 4: List certificates using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "test*"

Enabled   : True
Expires   : 8/5/2019 2:39:25 AM
NotBefore : 2/5/2019 2:29:25 AM
Created   : 2/5/2019 2:39:25 AM
Updated   : 2/5/2019 2:39:25 AM
Tags      :
VaultName : ContosoKV01
Name      : test1
Version   :
Id        : https://ContosoKV01.vault.azure.net:443/certificates/test1

Enabled   : True
Expires   : 8/5/2019 2:39:25 AM
NotBefore : 2/5/2019 2:29:25 AM
Created   : 2/5/2019 2:39:25 AM
Updated   : 2/5/2019 2:39:25 AM
Tags      :
VaultName : ContosoKV01
Name      : test2
Version   :
Id        : https://ContosoKV01.vault.azure.net:443/certificates/test2

This command gets all certificates starting with "test" from the key vault named ContosoKV01.
```

## <span data-ttu-id="bfeda-125">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bfeda-125">PARAMETERS</span></span>

### <span data-ttu-id="bfeda-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfeda-126">-DefaultProfile</span></span>
<span data-ttu-id="bfeda-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="bfeda-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bfeda-128">-IncludePending</span><span class="sxs-lookup"><span data-stu-id="bfeda-128">-IncludePending</span></span>
<span data-ttu-id="bfeda-129">Określa, czy mają być uwzględniane oczekujące certyfikaty w danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="bfeda-129">Specifies whether to include pending certificates in the output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByName, ByNameInputObject, ByNameResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfeda-130">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="bfeda-130">-IncludeVersions</span></span>
<span data-ttu-id="bfeda-131">Wskazuje, że ta operacja pobiera wszystkie wersje certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="bfeda-131">Indicates that this operation gets all versions of the certificate.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByCertificateAllVersions, ByCertificateAllVersionsInputObject, ByCertificateAllVersionsResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfeda-132">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bfeda-132">-InputObject</span></span>
<span data-ttu-id="bfeda-133">Obiekt magazynu.</span><span class="sxs-lookup"><span data-stu-id="bfeda-133">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByNameInputObject, ByCertificateNameAndVersionInputObject, ByCertificateAllVersionsInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bfeda-134">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="bfeda-134">-InRemovedState</span></span>
<span data-ttu-id="bfeda-135">Określa, czy w danych wyjściowych mają być uwzględniane uprzednio usunięte certyfikaty.</span><span class="sxs-lookup"><span data-stu-id="bfeda-135">Specifies whether to include previously deleted certificates in the output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByName, ByNameInputObject, ByNameResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfeda-136">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bfeda-136">-Name</span></span>
<span data-ttu-id="bfeda-137">Określa nazwę certyfikatu do pobrania.</span><span class="sxs-lookup"><span data-stu-id="bfeda-137">Specifies the name of the certificate to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName, ByNameInputObject, ByNameResourceId
Aliases: CertificateName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ByCertificateNameAndVersion, ByCertificateAllVersions, ByCertificateNameAndVersionInputObject, ByCertificateAllVersionsInputObject, ByCertificateNameAndVersionResourceId, ByCertificateAllVersionsResourceId
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="bfeda-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bfeda-138">-ResourceId</span></span>
<span data-ttu-id="bfeda-139">Identyfikator zasobu magazynu.</span><span class="sxs-lookup"><span data-stu-id="bfeda-139">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameResourceId, ByCertificateNameAndVersionResourceId, ByCertificateAllVersionsResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfeda-140">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="bfeda-140">-VaultName</span></span>
<span data-ttu-id="bfeda-141">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="bfeda-141">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName, ByCertificateNameAndVersion, ByCertificateAllVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfeda-142">-Version</span><span class="sxs-lookup"><span data-stu-id="bfeda-142">-Version</span></span>
<span data-ttu-id="bfeda-143">Określa wersję certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="bfeda-143">Specifies the version of a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ByCertificateNameAndVersion, ByCertificateNameAndVersionInputObject, ByCertificateNameAndVersionResourceId
Aliases: CertificateVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfeda-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfeda-144">CommonParameters</span></span>
<span data-ttu-id="bfeda-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfeda-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfeda-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bfeda-146">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfeda-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bfeda-147">INPUTS</span></span>

### <span data-ttu-id="bfeda-148">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="bfeda-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="bfeda-149">System. String</span><span class="sxs-lookup"><span data-stu-id="bfeda-149">System.String</span></span>

## <span data-ttu-id="bfeda-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bfeda-150">OUTPUTS</span></span>

### <span data-ttu-id="bfeda-151">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="bfeda-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

### <span data-ttu-id="bfeda-152">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="bfeda-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

### <span data-ttu-id="bfeda-153">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="bfeda-153">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span></span>

### <span data-ttu-id="bfeda-154">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="bfeda-154">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="bfeda-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bfeda-155">NOTES</span></span>

## <span data-ttu-id="bfeda-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bfeda-156">RELATED LINKS</span></span>

[<span data-ttu-id="bfeda-157">Dodaj-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="bfeda-157">Add-AzKeyVaultCertificate</span></span>](./Add-AzKeyVaultCertificate.md)

[<span data-ttu-id="bfeda-158">Import — AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="bfeda-158">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="bfeda-159">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="bfeda-159">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

[<span data-ttu-id="bfeda-160">Cofanie — AzKeyVaultSecretCertificate</span><span class="sxs-lookup"><span data-stu-id="bfeda-160">Undo-AzKeyVaultSecretCertificate</span></span>](./Undo-AzKeyVaultSecretCertificate.md)
