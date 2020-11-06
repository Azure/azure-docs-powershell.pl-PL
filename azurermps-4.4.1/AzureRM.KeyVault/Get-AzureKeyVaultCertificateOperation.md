---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 0743C43D-2A1F-4950-B0F3-1FED4014EEC5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateOperation.md
ms.openlocfilehash: dd9260fa833a09736aaba4b63f56f5b5c894662d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527557"
---
# <span data-ttu-id="fa99b-101">Get-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="fa99b-101">Get-AzureKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="fa99b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fa99b-102">SYNOPSIS</span></span>
<span data-ttu-id="fa99b-103">Pobiera stan operacji certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="fa99b-103">Gets the status of a certificate operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa99b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fa99b-104">SYNTAX</span></span>

```
Get-AzureKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa99b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fa99b-105">DESCRIPTION</span></span>
<span data-ttu-id="fa99b-106">Polecenie cmdlet **Get-AzureKeyVaultCertificateOperation** Pobiera stan operacji certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="fa99b-106">The **Get-AzureKeyVaultCertificateOperation** cmdlet gets the status of a certificate operation.</span></span>

## <span data-ttu-id="fa99b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fa99b-107">EXAMPLES</span></span>

### <span data-ttu-id="fa99b-108">Przykład 1: uzyskiwanie stanu operacji na certyfikacie</span><span class="sxs-lookup"><span data-stu-id="fa99b-108">Example 1: Get the status of a certificate operation</span></span>
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

<span data-ttu-id="fa99b-109">To polecenie uzyskuje stan operacji certyfikatu dla TestCert01 w magazynie kluczy ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="fa99b-109">This command gets the status of the certificate operation for TestCert01 on the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="fa99b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fa99b-110">PARAMETERS</span></span>

### <span data-ttu-id="fa99b-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fa99b-111">-Name</span></span>
<span data-ttu-id="fa99b-112">Określa nazwę certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="fa99b-112">Specifies the name of a certificate.</span></span>

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

### <span data-ttu-id="fa99b-113">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="fa99b-113">-VaultName</span></span>
<span data-ttu-id="fa99b-114">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="fa99b-114">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="fa99b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa99b-115">-DefaultProfile</span></span>
<span data-ttu-id="fa99b-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fa99b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa99b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa99b-117">CommonParameters</span></span>
<span data-ttu-id="fa99b-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa99b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa99b-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa99b-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa99b-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fa99b-120">INPUTS</span></span>

## <span data-ttu-id="fa99b-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fa99b-121">OUTPUTS</span></span>

### <span data-ttu-id="fa99b-122">Microsoft. Azure. Commands. platforming. models. KeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="fa99b-122">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOperation</span></span>

## <span data-ttu-id="fa99b-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fa99b-123">NOTES</span></span>

## <span data-ttu-id="fa99b-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fa99b-124">RELATED LINKS</span></span>

[<span data-ttu-id="fa99b-125">Remove-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="fa99b-125">Remove-AzureKeyVaultCertificateOperation</span></span>](./Remove-AzureKeyVaultCertificateOperation.md)

[<span data-ttu-id="fa99b-126">Zatrzymaj — AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="fa99b-126">Stop-AzureKeyVaultCertificateOperation</span></span>](./Stop-AzureKeyVaultCertificateOperation.md)

