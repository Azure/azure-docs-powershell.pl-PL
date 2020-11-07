---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 0729687C-3104-4136-A80D-16BAEBD6B76C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificatepolicy
schema: 2.0.0
ms.openlocfilehash: 692c639ac42d0a8f2dc2bf121321dfc116ebce1b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898754"
---
# <span data-ttu-id="1b008-101">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="1b008-101">Get-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="1b008-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1b008-102">SYNOPSIS</span></span>
<span data-ttu-id="1b008-103">Pobiera zasady dotyczące certyfikatu w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="1b008-103">Gets the policy for a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b008-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1b008-104">SYNTAX</span></span>

```
Get-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b008-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1b008-105">DESCRIPTION</span></span>
<span data-ttu-id="1b008-106">Polecenie cmdlet **Get-AzureKeyVaultCertificatePolicy** pobiera zasady dotyczące certyfikatu w magazynie kluczy w magazynie kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1b008-106">The **Get-AzureKeyVaultCertificatePolicy** cmdlet gets the policy for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="1b008-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1b008-107">EXAMPLES</span></span>

### <span data-ttu-id="1b008-108">Przykład 1: uzyskiwanie zasad certyfikatów</span><span class="sxs-lookup"><span data-stu-id="1b008-108">Example 1: Get a certificate policy</span></span>
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

<span data-ttu-id="1b008-109">To polecenie pobiera zasady certyfikatu dla certyfikatu TestCert01 w magazynie kluczy ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="1b008-109">This command gets the certificate policy for TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="1b008-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1b008-110">PARAMETERS</span></span>

### <span data-ttu-id="1b008-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b008-111">-DefaultProfile</span></span>
<span data-ttu-id="1b008-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="1b008-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1b008-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1b008-113">-Name</span></span>
<span data-ttu-id="1b008-114">Określa nazwę certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="1b008-114">Specifies the name of a certificate.</span></span>

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

### <span data-ttu-id="1b008-115">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="1b008-115">-VaultName</span></span>
<span data-ttu-id="1b008-116">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="1b008-116">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="1b008-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b008-117">CommonParameters</span></span>
<span data-ttu-id="1b008-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b008-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b008-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b008-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b008-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1b008-120">INPUTS</span></span>

## <span data-ttu-id="1b008-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1b008-121">OUTPUTS</span></span>

### <span data-ttu-id="1b008-122">Microsoft. Azure. Commands. platforming. models. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="1b008-122">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="1b008-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1b008-123">NOTES</span></span>

## <span data-ttu-id="1b008-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1b008-124">RELATED LINKS</span></span>

[<span data-ttu-id="1b008-125">Nowe — AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="1b008-125">New-AzureKeyVaultCertificatePolicy</span></span>](./New-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="1b008-126">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="1b008-126">Set-AzureKeyVaultCertificatePolicy</span></span>](./Set-AzureKeyVaultCertificatePolicy.md)

