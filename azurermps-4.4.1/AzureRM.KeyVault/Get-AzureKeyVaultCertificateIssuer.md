---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: 66c5e949cca8a6f53fdbac89e2745ac7697e14ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551876"
---
# <span data-ttu-id="e8ab3-101">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="e8ab3-101">Get-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="e8ab3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e8ab3-102">SYNOPSIS</span></span>
<span data-ttu-id="e8ab3-103">Pobiera wystawcę certyfikatu dla magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="e8ab3-103">Gets a certificate issuer for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8ab3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e8ab3-104">SYNTAX</span></span>

### <span data-ttu-id="e8ab3-105">ByVaultName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e8ab3-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e8ab3-106">ByName</span><span class="sxs-lookup"><span data-stu-id="e8ab3-106">ByName</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8ab3-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e8ab3-107">DESCRIPTION</span></span>
<span data-ttu-id="e8ab3-108">Polecenie cmdlet **Get-AzureKeyVaultCertificateIssuer** pobiera określonego wystawcy certyfikatu lub wystawców certyfikatów dla magazynu kluczy w magazynie kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e8ab3-108">The **Get-AzureKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="e8ab3-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e8ab3-109">EXAMPLES</span></span>

### <span data-ttu-id="e8ab3-110">Przykład 1: uzyskiwanie wystawcy certyfikatu</span><span class="sxs-lookup"><span data-stu-id="e8ab3-110">Example 1: Get a certificate issuer</span></span>
```
PS C:\>Get-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"
Name                : TestIssuer01
IssuerProvider      : Test
AccountId           : 555
ApiKey              : 
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails
```

<span data-ttu-id="e8ab3-111">To polecenie pobiera wystawcę certyfikatu o nazwie TestIssuer01.</span><span class="sxs-lookup"><span data-stu-id="e8ab3-111">This command gets the certificate issuer named TestIssuer01.</span></span>

## <span data-ttu-id="e8ab3-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e8ab3-112">PARAMETERS</span></span>

### <span data-ttu-id="e8ab3-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e8ab3-113">-Name</span></span>
<span data-ttu-id="e8ab3-114">Określa nazwę wystawcy certyfikatu do pobrania.</span><span class="sxs-lookup"><span data-stu-id="e8ab3-114">Specifies the name of the certificate issuer to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: IssuerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8ab3-115">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="e8ab3-115">-VaultName</span></span>
<span data-ttu-id="e8ab3-116">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="e8ab3-116">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="e8ab3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8ab3-117">-DefaultProfile</span></span>
<span data-ttu-id="e8ab3-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e8ab3-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8ab3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8ab3-119">CommonParameters</span></span>
<span data-ttu-id="e8ab3-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8ab3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8ab3-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8ab3-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8ab3-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e8ab3-122">INPUTS</span></span>

## <span data-ttu-id="e8ab3-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e8ab3-123">OUTPUTS</span></span>

### <span data-ttu-id="e8ab3-124">Lista<Microsoft. Azure. Commands.. modele. CertificateIssuerIdentityItem>, Microsoft. Azure. Commands. platforming. models. KeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="e8ab3-124">List<Microsoft.Azure.Commands.KeyVault.Models.CertificateIssuerIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="e8ab3-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e8ab3-125">NOTES</span></span>

## <span data-ttu-id="e8ab3-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e8ab3-126">RELATED LINKS</span></span>

[<span data-ttu-id="e8ab3-127">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="e8ab3-127">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="e8ab3-128">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="e8ab3-128">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


