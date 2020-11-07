---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: b9188e1bb4d5de4896bf0ca3b2844c7718593ca2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891309"
---
# <span data-ttu-id="f4672-101">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="f4672-101">Get-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="f4672-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f4672-102">SYNOPSIS</span></span>
<span data-ttu-id="f4672-103">Pobiera wystawcę certyfikatu dla magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="f4672-103">Gets a certificate issuer for a key vault.</span></span>

## <span data-ttu-id="f4672-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f4672-104">SYNTAX</span></span>

### <span data-ttu-id="f4672-105">ByVaultName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f4672-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultCertificateIssuer [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f4672-106">ByName</span><span class="sxs-lookup"><span data-stu-id="f4672-106">ByName</span></span>
```
Get-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4672-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f4672-107">DESCRIPTION</span></span>
<span data-ttu-id="f4672-108">Polecenie cmdlet **Get-AzKeyVaultCertificateIssuer** pobiera określonego wystawcy certyfikatu lub wystawców certyfikatów dla magazynu kluczy w magazynie kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f4672-108">The **Get-AzKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="f4672-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f4672-109">EXAMPLES</span></span>

### <span data-ttu-id="f4672-110">Przykład 1: uzyskiwanie wystawcy certyfikatu</span><span class="sxs-lookup"><span data-stu-id="f4672-110">Example 1: Get a certificate issuer</span></span>
```
PS C:\>Get-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"
Name                : TestIssuer01
IssuerProvider      : Test
AccountId           : 555
ApiKey              : 
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails
```

<span data-ttu-id="f4672-111">To polecenie pobiera wystawcę certyfikatu o nazwie TestIssuer01.</span><span class="sxs-lookup"><span data-stu-id="f4672-111">This command gets the certificate issuer named TestIssuer01.</span></span>

## <span data-ttu-id="f4672-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f4672-112">PARAMETERS</span></span>

### <span data-ttu-id="f4672-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4672-113">-DefaultProfile</span></span>
<span data-ttu-id="f4672-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f4672-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f4672-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f4672-115">-Name</span></span>
<span data-ttu-id="f4672-116">Określa nazwę wystawcy certyfikatu do pobrania.</span><span class="sxs-lookup"><span data-stu-id="f4672-116">Specifies the name of the certificate issuer to get.</span></span>

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

### <span data-ttu-id="f4672-117">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="f4672-117">-VaultName</span></span>
<span data-ttu-id="f4672-118">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="f4672-118">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="f4672-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4672-119">CommonParameters</span></span>
<span data-ttu-id="f4672-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4672-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4672-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4672-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4672-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f4672-122">INPUTS</span></span>

### <span data-ttu-id="f4672-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f4672-123">None</span></span>
<span data-ttu-id="f4672-124">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="f4672-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f4672-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f4672-125">OUTPUTS</span></span>

### <span data-ttu-id="f4672-126">Lista<Microsoft. Azure. Commands.. modele. CertificateIssuerIdentityItem>, Microsoft. Azure. Commands. platforming. models. KeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="f4672-126">List<Microsoft.Azure.Commands.KeyVault.Models.CertificateIssuerIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="f4672-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f4672-127">NOTES</span></span>

## <span data-ttu-id="f4672-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f4672-128">RELATED LINKS</span></span>

[<span data-ttu-id="f4672-129">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="f4672-129">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="f4672-130">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="f4672-130">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)


