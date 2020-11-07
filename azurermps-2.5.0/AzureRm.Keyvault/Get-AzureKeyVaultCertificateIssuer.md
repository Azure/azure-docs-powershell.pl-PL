---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificateissuer
schema: 2.0.0
ms.openlocfilehash: fcbb19936bb9924f95aa3a20fa026a9c8c723033
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898756"
---
# <span data-ttu-id="4743f-101">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="4743f-101">Get-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="4743f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4743f-102">SYNOPSIS</span></span>
<span data-ttu-id="4743f-103">Pobiera wystawcę certyfikatu dla magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="4743f-103">Gets a certificate issuer for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4743f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4743f-104">SYNTAX</span></span>

### <span data-ttu-id="4743f-105">ByVaultName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4743f-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4743f-106">ByName</span><span class="sxs-lookup"><span data-stu-id="4743f-106">ByName</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4743f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="4743f-107">DESCRIPTION</span></span>
<span data-ttu-id="4743f-108">Polecenie cmdlet **Get-AzureKeyVaultCertificateIssuer** pobiera określonego wystawcy certyfikatu lub wystawców certyfikatów dla magazynu kluczy w magazynie kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4743f-108">The **Get-AzureKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="4743f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4743f-109">EXAMPLES</span></span>

### <span data-ttu-id="4743f-110">Przykład 1: uzyskiwanie wystawcy certyfikatu</span><span class="sxs-lookup"><span data-stu-id="4743f-110">Example 1: Get a certificate issuer</span></span>
```
PS C:\>Get-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"
Name                : TestIssuer01
IssuerProvider      : Test
AccountId           : 555
ApiKey              : 
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails
```

<span data-ttu-id="4743f-111">To polecenie pobiera wystawcę certyfikatu o nazwie TestIssuer01.</span><span class="sxs-lookup"><span data-stu-id="4743f-111">This command gets the certificate issuer named TestIssuer01.</span></span>

## <span data-ttu-id="4743f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4743f-112">PARAMETERS</span></span>

### <span data-ttu-id="4743f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4743f-113">-DefaultProfile</span></span>
<span data-ttu-id="4743f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="4743f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4743f-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4743f-115">-Name</span></span>
<span data-ttu-id="4743f-116">Określa nazwę wystawcy certyfikatu do pobrania.</span><span class="sxs-lookup"><span data-stu-id="4743f-116">Specifies the name of the certificate issuer to get.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4743f-117">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="4743f-117">-VaultName</span></span>
<span data-ttu-id="4743f-118">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="4743f-118">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="4743f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4743f-119">CommonParameters</span></span>
<span data-ttu-id="4743f-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4743f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4743f-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4743f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4743f-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4743f-122">INPUTS</span></span>

## <span data-ttu-id="4743f-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4743f-123">OUTPUTS</span></span>

### <span data-ttu-id="4743f-124">Lista<Microsoft. Azure. Commands.. modele. CertificateIssuerIdentityItem>, Microsoft. Azure. Commands. platforming. models. KeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="4743f-124">List<Microsoft.Azure.Commands.KeyVault.Models.CertificateIssuerIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="4743f-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4743f-125">NOTES</span></span>

## <span data-ttu-id="4743f-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4743f-126">RELATED LINKS</span></span>

[<span data-ttu-id="4743f-127">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="4743f-127">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="4743f-128">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="4743f-128">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


