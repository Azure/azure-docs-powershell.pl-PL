---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 0743C43D-2A1F-4950-B0F3-1FED4014EEC5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificateoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateOperation.md
ms.openlocfilehash: 1f61207afbdf4c6553f6db4050775577d72c5eba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542568"
---
# <span data-ttu-id="9bf02-101">Get-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="9bf02-101">Get-AzureKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="9bf02-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9bf02-102">SYNOPSIS</span></span>
<span data-ttu-id="9bf02-103">Pobiera stan operacji certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="9bf02-103">Gets the status of a certificate operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9bf02-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9bf02-104">SYNTAX</span></span>

### <span data-ttu-id="9bf02-105">ByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9bf02-105">ByName (Default)</span></span>
```
Get-AzureKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9bf02-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9bf02-106">ByInputObject</span></span>
```
Get-AzureKeyVaultCertificateOperation [-InputObject] <PSKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9bf02-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9bf02-107">DESCRIPTION</span></span>
<span data-ttu-id="9bf02-108">Polecenie cmdlet **Get-AzureKeyVaultCertificateOperation** Pobiera stan operacji certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="9bf02-108">The **Get-AzureKeyVaultCertificateOperation** cmdlet gets the status of a certificate operation.</span></span>

## <span data-ttu-id="9bf02-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9bf02-109">EXAMPLES</span></span>

### <span data-ttu-id="9bf02-110">Przykład 1: uzyskiwanie stanu operacji na certyfikacie</span><span class="sxs-lookup"><span data-stu-id="9bf02-110">Example 1: Get the status of a certificate operation</span></span>
```
PS C:\>Get-AzureKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01"
Status                    : inProgress
CancellationRequested     : False
CertificateSigningRequest : MIICpjCCAY4CAQAwFjEUMBIGA1UEAxMLY29udG9zby5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC73w3VRBOlgJ5Od1PjDh+2ytngNZp+ZP4fkuX8K1Ti5LA6Ih7eWx1fgAN/iTb6l
                            5K6LvAIJvsTNVePMNxfSdaEIJ70Inm45wVU4A/kf+UxQWAYVMsBrLtDFWxnVhzf6n7RGYke6HLBj3j5ASb9g+olSs6eON25ibF0t+u6JC+sIR0LmVGar9Q0eZys1rdfzJBIKq+laOM7z2pJijb5ANqve9
                            i7rH5mnhQk4V8WsRstOhYR9jgLqSSxokDoeaBClIOidSBYqVc1yNv4ASe1UWUCR7ZK6OQXiecNWSWPmgWEyawu6AR9eb1YotCr2ScheMOCxlm3103luitxrd8A7kMjAgMBAAGgSzBJBgkqhkiG9w0BCQ4
                            xPDA6MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAQEAIHhsDJV37PKi8hor5eQf7+Tct1preIvSwqV0NF6Uo7O6
                            YnC9Py7Wp7CHfKzuqeptUk2Tsu7B5dHB+o9Ypeeqw8fWhTN0GFGRKO7WjZQlDqL+lRNcjlFSaP022oIP0kmvVhBcmZqRQlALXccAaxEclFA/3y/aNj2gwWeKpH/pwAkZ39zMEzpQCaRfnQk7e3l4MV8cf
                            eC2HPYdRWkXxAeDcNPxBuVmKy49AzYvly+APNVDU3v66gxl3fIKrGRsKi2Cp/nO5rBxG2h8t+0Za4l/HJ7ZWR9wKbd/xg7JhdZZFVBxMHYzw8KQ0ys13x8HY+PXU92Y7yD3uC2Rcj+zbAf+Kg==
ErrorCode                 : 
ErrorMessage              :
```

<span data-ttu-id="9bf02-111">To polecenie uzyskuje stan operacji certyfikatu dla TestCert01 w magazynie kluczy ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="9bf02-111">This command gets the status of the certificate operation for TestCert01 on the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="9bf02-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9bf02-112">PARAMETERS</span></span>

### <span data-ttu-id="9bf02-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bf02-113">-DefaultProfile</span></span>
<span data-ttu-id="9bf02-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="9bf02-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9bf02-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9bf02-115">-InputObject</span></span>
<span data-ttu-id="9bf02-116">Obiekt Certificate (certyfikat).</span><span class="sxs-lookup"><span data-stu-id="9bf02-116">Certificate Object.</span></span>

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

### <span data-ttu-id="9bf02-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9bf02-117">-Name</span></span>
<span data-ttu-id="9bf02-118">Określa nazwę certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="9bf02-118">Specifies the name of a certificate.</span></span>

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

### <span data-ttu-id="9bf02-119">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="9bf02-119">-VaultName</span></span>
<span data-ttu-id="9bf02-120">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="9bf02-120">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="9bf02-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bf02-121">CommonParameters</span></span>
<span data-ttu-id="9bf02-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bf02-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bf02-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bf02-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bf02-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9bf02-124">INPUTS</span></span>

### <span data-ttu-id="9bf02-125">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9bf02-125">None</span></span>
<span data-ttu-id="9bf02-126">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="9bf02-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9bf02-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9bf02-127">OUTPUTS</span></span>

### <span data-ttu-id="9bf02-128">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="9bf02-128">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="9bf02-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9bf02-129">NOTES</span></span>

## <span data-ttu-id="9bf02-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9bf02-130">RELATED LINKS</span></span>

[<span data-ttu-id="9bf02-131">Remove-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="9bf02-131">Remove-AzureKeyVaultCertificateOperation</span></span>](./Remove-AzureKeyVaultCertificateOperation.md)

[<span data-ttu-id="9bf02-132">Zatrzymaj — AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="9bf02-132">Stop-AzureKeyVaultCertificateOperation</span></span>](./Stop-AzureKeyVaultCertificateOperation.md)

