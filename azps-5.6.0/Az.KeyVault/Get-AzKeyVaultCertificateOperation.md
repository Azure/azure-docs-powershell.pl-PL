---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0743C43D-2A1F-4950-B0F3-1FED4014EEC5
online version: https://docs.microsoft.com/powershell/module/az.keyvault/get-azkeyvaultcertificateoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateOperation.md
ms.openlocfilehash: 522496e8b754f8f979fdf6fd4bdb5f8fb4fb3eb4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004001"
---
# <span data-ttu-id="303ba-101">Get-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="303ba-101">Get-AzKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="303ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="303ba-102">SYNOPSIS</span></span>
<span data-ttu-id="303ba-103">Pobiera stan operacji certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="303ba-103">Gets the status of a certificate operation.</span></span>

## <span data-ttu-id="303ba-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="303ba-104">SYNTAX</span></span>

### <span data-ttu-id="303ba-105">ByName (Default)</span><span class="sxs-lookup"><span data-stu-id="303ba-105">ByName (Default)</span></span>
```
Get-AzKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="303ba-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="303ba-106">ByInputObject</span></span>
```
Get-AzKeyVaultCertificateOperation [-InputObject] <PSKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="303ba-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="303ba-107">DESCRIPTION</span></span>
<span data-ttu-id="303ba-108">Polecenie **cmdlet Get-AzKeyVaultCertificateOperation** pobiera stan operacji certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="303ba-108">The **Get-AzKeyVaultCertificateOperation** cmdlet gets the status of a certificate operation.</span></span>

## <span data-ttu-id="303ba-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="303ba-109">EXAMPLES</span></span>

### <span data-ttu-id="303ba-110">Przykład 1. Uzyskiwanie stanu operacji certyfikatu</span><span class="sxs-lookup"><span data-stu-id="303ba-110">Example 1: Get the status of a certificate operation</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificateOperation -VaultName "contosoKV01" -Name "TestCert01"

Id                        : https://contosoKV01.vault.azure.net/certificates/TestCert01/pending
Status                    : inProgress
StatusDetails             : Pending certificate created. Certificate request is in progress. This may take some time
                            based on the issuer provider. Please check again later.
RequestId                 : 32a63e80568442a2892dafb9f7cf366t
Target                    :
Issuer                    : Self
CancellationRequested     : False
CertificateSigningRequest : MIICpjCCAY4CAQAwFjEUMBIGA1UEAxMLY29udG9zby5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC73w3VRBOlgJ5Od1PjDh+2ytngNZp+ZP4fkuX8K1Ti5LA6Ih7eWx1fgAN/iTb6l
                            5K6LvAIJvsTNVePMNxfSdaEIJ70Inm45wVU4A/kf+UxQWAYVMsBrLtDFWxnVhzf6n7RGYke6HLBj3j5ASb9g+olSs6eON25ibF0t+u6JC+sIR0LmVGar9Q0eZys1rdfzJBIKq+laOM7z2pJijb5ANqve9
                            i7rH5mnhQk4V8WsRstOhYR9jgLqSSxokDoeaBClIOidSBYqVc1yNv4ASe1UWUCR7ZK6OQXiecNWSWPmgWEyawu6AR9eb1YotCr2ScheMOCxlm3103luitxrd8A7kMjAgMBAAGgSzBJBgkqhkiG9w0BCQ4
                            xPDA6MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAQEAIHhsDJV37PKi8hor5eQf7+Tct1preIvSwqV0NF6Uo7O6
                            YnC9Py7Wp7CHfKzuqeptUk2Tsu7B5dHB+o9Ypeeqw8fWhTN0GFGRKO7WjZQlDqL+lRNcjlFSaP022oIP0kmvVhBcmZqRQlALXccAaxEclFA/3y/aNj2gwWeKpH/pwAkZ39zMEzpQCaRfnQk7e3l4MV8cf
                            eC2HPYdRWkXxAeDcNPxBuVmKy49AzYvly+APNVDU3v66gxl3fIKrGRsKi2Cp/nO5rBxG2h8t+0Za4l/HJ7ZWR9wKbd/xg7JhdZZFVBxMHYzw8KQ0ys13x8HY+PXU92Y7yD3uC2Rcj+zbAf+Kg==
ErrorCode                 :
ErrorMessage              :
Name                      :
VaultName                 :
```

<span data-ttu-id="303ba-111">To polecenie otrzymuje stan operacji certyfikatu dla certyfikatu TestCert01 w magazynie kluczy ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="303ba-111">This command gets the status of the certificate operation for TestCert01 on the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="303ba-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="303ba-112">PARAMETERS</span></span>

### <span data-ttu-id="303ba-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="303ba-113">-DefaultProfile</span></span>
<span data-ttu-id="303ba-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="303ba-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="303ba-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="303ba-115">-InputObject</span></span>
<span data-ttu-id="303ba-116">Obiekt Certificate.</span><span class="sxs-lookup"><span data-stu-id="303ba-116">Certificate Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="303ba-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="303ba-117">-Name</span></span>
<span data-ttu-id="303ba-118">Określa nazwę certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="303ba-118">Specifies the name of a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="303ba-119">-VaultName</span><span class="sxs-lookup"><span data-stu-id="303ba-119">-VaultName</span></span>
<span data-ttu-id="303ba-120">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="303ba-120">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="303ba-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="303ba-121">CommonParameters</span></span>
<span data-ttu-id="303ba-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="303ba-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="303ba-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="303ba-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="303ba-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="303ba-124">INPUTS</span></span>

### <span data-ttu-id="303ba-125">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="303ba-125">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="303ba-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="303ba-126">OUTPUTS</span></span>

### <span data-ttu-id="303ba-127">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="303ba-127">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="303ba-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="303ba-128">NOTES</span></span>

## <span data-ttu-id="303ba-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="303ba-129">RELATED LINKS</span></span>

[<span data-ttu-id="303ba-130">Remove-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="303ba-130">Remove-AzKeyVaultCertificateOperation</span></span>](./Remove-AzKeyVaultCertificateOperation.md)

[<span data-ttu-id="303ba-131">Stop-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="303ba-131">Stop-AzKeyVaultCertificateOperation</span></span>](./Stop-AzKeyVaultCertificateOperation.md)

