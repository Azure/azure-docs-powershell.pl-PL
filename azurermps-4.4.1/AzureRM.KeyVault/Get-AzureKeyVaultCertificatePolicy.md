---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 0729687C-3104-4136-A80D-16BAEBD6B76C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: a6b8b4f07d4ac589a0bb700e6303c384e38966fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719023"
---
# <span data-ttu-id="6cd76-101">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="6cd76-101">Get-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="6cd76-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6cd76-102">SYNOPSIS</span></span>
<span data-ttu-id="6cd76-103">Pobiera zasady dotyczące certyfikatu w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="6cd76-103">Gets the policy for a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6cd76-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6cd76-104">SYNTAX</span></span>

```
Get-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6cd76-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6cd76-105">DESCRIPTION</span></span>
<span data-ttu-id="6cd76-106">Polecenie cmdlet **Get-AzureKeyVaultCertificatePolicy** pobiera zasady dotyczące certyfikatu w magazynie kluczy w magazynie kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6cd76-106">The **Get-AzureKeyVaultCertificatePolicy** cmdlet gets the policy for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="6cd76-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6cd76-107">EXAMPLES</span></span>

### <span data-ttu-id="6cd76-108">Przykład 1: uzyskiwanie zasad certyfikatów</span><span class="sxs-lookup"><span data-stu-id="6cd76-108">Example 1: Get a certificate policy</span></span>
```
PS C:\>Get-AzureKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01"
SecretContentType               : application/x-pkcs12
Kty                             : RSA
KeySize                         : 2048
Exportable                      : True
ReuseKeyOnRenewal               : True
SubjectName                     : CN=contoso.com
DnsNames                        : 
Ekus                            : {1.3.6.1.5.5.7.3.1, 1.3.6.1.5.5.7.3.2}
ValidityInMonths                : 6
IssuerName                      : Self
RenewAtNumberOfDaysBeforeExpiry : 
RenewAtPercentageLifetime       : 80
EmailOnly                       : False
Enabled                         : True
Created                         : 2/8/2016 11:10:29 PM
Updated                         : 2/8/2016 11:10:29 PM
```

<span data-ttu-id="6cd76-109">To polecenie pobiera zasady certyfikatu dla certyfikatu TestCert01 w magazynie kluczy ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="6cd76-109">This command gets the certificate policy for TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="6cd76-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6cd76-110">PARAMETERS</span></span>

### <span data-ttu-id="6cd76-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6cd76-111">-Name</span></span>
<span data-ttu-id="6cd76-112">Określa nazwę certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="6cd76-112">Specifies the name of a certificate.</span></span>

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

### <span data-ttu-id="6cd76-113">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="6cd76-113">-VaultName</span></span>
<span data-ttu-id="6cd76-114">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="6cd76-114">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="6cd76-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cd76-115">-DefaultProfile</span></span>
<span data-ttu-id="6cd76-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6cd76-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6cd76-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cd76-117">CommonParameters</span></span>
<span data-ttu-id="6cd76-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cd76-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cd76-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cd76-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cd76-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6cd76-120">INPUTS</span></span>

## <span data-ttu-id="6cd76-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6cd76-121">OUTPUTS</span></span>

### <span data-ttu-id="6cd76-122">Microsoft. Azure. Commands. platforming. models. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="6cd76-122">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="6cd76-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6cd76-123">NOTES</span></span>

## <span data-ttu-id="6cd76-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6cd76-124">RELATED LINKS</span></span>

[<span data-ttu-id="6cd76-125">Nowe — AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="6cd76-125">New-AzureKeyVaultCertificatePolicy</span></span>](./New-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="6cd76-126">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="6cd76-126">Set-AzureKeyVaultCertificatePolicy</span></span>](./Set-AzureKeyVaultCertificatePolicy.md)

