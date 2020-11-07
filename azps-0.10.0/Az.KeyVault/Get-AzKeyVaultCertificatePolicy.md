---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0729687C-3104-4136-A80D-16BAEBD6B76C
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: d525a47dde9551e5d48c7c316cf6844323b75e81
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891297"
---
# <span data-ttu-id="fd027-101">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="fd027-101">Get-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="fd027-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fd027-102">SYNOPSIS</span></span>
<span data-ttu-id="fd027-103">Pobiera zasady dotyczące certyfikatu w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="fd027-103">Gets the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="fd027-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fd027-104">SYNTAX</span></span>

```
Get-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd027-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fd027-105">DESCRIPTION</span></span>
<span data-ttu-id="fd027-106">Polecenie cmdlet **Get-AzKeyVaultCertificatePolicy** pobiera zasady dotyczące certyfikatu w magazynie kluczy w magazynie kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fd027-106">The **Get-AzKeyVaultCertificatePolicy** cmdlet gets the policy for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="fd027-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fd027-107">EXAMPLES</span></span>

### <span data-ttu-id="fd027-108">Przykład 1: uzyskiwanie zasad certyfikatów</span><span class="sxs-lookup"><span data-stu-id="fd027-108">Example 1: Get a certificate policy</span></span>
```
PS C:\>Get-AzKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01"
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

<span data-ttu-id="fd027-109">To polecenie pobiera zasady certyfikatu dla certyfikatu TestCert01 w magazynie kluczy ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="fd027-109">This command gets the certificate policy for TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="fd027-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fd027-110">PARAMETERS</span></span>

### <span data-ttu-id="fd027-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd027-111">-DefaultProfile</span></span>
<span data-ttu-id="fd027-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="fd027-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fd027-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fd027-113">-Name</span></span>
<span data-ttu-id="fd027-114">Określa nazwę certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="fd027-114">Specifies the name of a certificate.</span></span>

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

### <span data-ttu-id="fd027-115">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="fd027-115">-VaultName</span></span>
<span data-ttu-id="fd027-116">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="fd027-116">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="fd027-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd027-117">CommonParameters</span></span>
<span data-ttu-id="fd027-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd027-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd027-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd027-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd027-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fd027-120">INPUTS</span></span>

### <span data-ttu-id="fd027-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="fd027-121">None</span></span>
<span data-ttu-id="fd027-122">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="fd027-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fd027-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fd027-123">OUTPUTS</span></span>

### <span data-ttu-id="fd027-124">Microsoft. Azure. Commands. platforming. models. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="fd027-124">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="fd027-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fd027-125">NOTES</span></span>

## <span data-ttu-id="fd027-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fd027-126">RELATED LINKS</span></span>

[<span data-ttu-id="fd027-127">Nowe — AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="fd027-127">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="fd027-128">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="fd027-128">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

