---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: f19fa119bf307724fb318e0a1d9a390190523bd1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542571"
---
# <span data-ttu-id="fb7fc-101">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="fb7fc-101">Get-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="fb7fc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fb7fc-102">SYNOPSIS</span></span>
<span data-ttu-id="fb7fc-103">Pobiera wystawcę certyfikatu dla magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="fb7fc-103">Gets a certificate issuer for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb7fc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fb7fc-104">SYNTAX</span></span>

### <span data-ttu-id="fb7fc-105">ByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="fb7fc-105">ByName (Default)</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb7fc-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fb7fc-106">ByInputObject</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-InputObject] <PSKeyVault> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb7fc-107">Opis</span><span class="sxs-lookup"><span data-stu-id="fb7fc-107">DESCRIPTION</span></span>
<span data-ttu-id="fb7fc-108">Polecenie cmdlet **Get-AzureKeyVaultCertificateIssuer** pobiera określonego wystawcy certyfikatu lub wystawców certyfikatów dla magazynu kluczy w magazynie kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fb7fc-108">The **Get-AzureKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="fb7fc-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fb7fc-109">EXAMPLES</span></span>

### <span data-ttu-id="fb7fc-110">Przykład 1: uzyskiwanie wystawcy certyfikatu</span><span class="sxs-lookup"><span data-stu-id="fb7fc-110">Example 1: Get a certificate issuer</span></span>
```
PS C:\>Get-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"
Name                : TestIssuer01
IssuerProvider      : Test
AccountId           : 555
ApiKey              : 
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails
```

<span data-ttu-id="fb7fc-111">To polecenie pobiera wystawcę certyfikatu o nazwie TestIssuer01.</span><span class="sxs-lookup"><span data-stu-id="fb7fc-111">This command gets the certificate issuer named TestIssuer01.</span></span>

## <span data-ttu-id="fb7fc-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fb7fc-112">PARAMETERS</span></span>

### <span data-ttu-id="fb7fc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb7fc-113">-DefaultProfile</span></span>
<span data-ttu-id="fb7fc-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="fb7fc-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb7fc-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fb7fc-115">-InputObject</span></span>
<span data-ttu-id="fb7fc-116">Obiekt magazynu.</span><span class="sxs-lookup"><span data-stu-id="fb7fc-116">KeyVault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb7fc-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fb7fc-117">-Name</span></span>
<span data-ttu-id="fb7fc-118">Określa nazwę wystawcy certyfikatu do pobrania.</span><span class="sxs-lookup"><span data-stu-id="fb7fc-118">Specifies the name of the certificate issuer to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IssuerName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb7fc-119">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="fb7fc-119">-VaultName</span></span>
<span data-ttu-id="fb7fc-120">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="fb7fc-120">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="fb7fc-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb7fc-121">CommonParameters</span></span>
<span data-ttu-id="fb7fc-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb7fc-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb7fc-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb7fc-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb7fc-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fb7fc-124">INPUTS</span></span>

### <span data-ttu-id="fb7fc-125">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="fb7fc-125">None</span></span>
<span data-ttu-id="fb7fc-126">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="fb7fc-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fb7fc-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fb7fc-127">OUTPUTS</span></span>

### <span data-ttu-id="fb7fc-128">Lista<Microsoft. Azure. Commands.. modele. PSKeyVaultCertificateIssuerIdentityItem>, Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="fb7fc-128">List<Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="fb7fc-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fb7fc-129">NOTES</span></span>

## <span data-ttu-id="fb7fc-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fb7fc-130">RELATED LINKS</span></span>

[<span data-ttu-id="fb7fc-131">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="fb7fc-131">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="fb7fc-132">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="fb7fc-132">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


