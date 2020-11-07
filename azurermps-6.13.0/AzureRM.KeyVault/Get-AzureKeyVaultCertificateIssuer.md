---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: 83e81e479807c3eada25456d53521dfcecd81f40
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718322"
---
# <span data-ttu-id="6697e-101">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="6697e-101">Get-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="6697e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6697e-102">SYNOPSIS</span></span>
<span data-ttu-id="6697e-103">Pobiera wystawcę certyfikatu dla magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="6697e-103">Gets a certificate issuer for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6697e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6697e-104">SYNTAX</span></span>

### <span data-ttu-id="6697e-105">ByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6697e-105">ByName (Default)</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6697e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="6697e-106">ByInputObject</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-InputObject] <PSKeyVault> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6697e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6697e-107">ByResourceId</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-ResourceId] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6697e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6697e-108">DESCRIPTION</span></span>
<span data-ttu-id="6697e-109">Polecenie cmdlet **Get-AzureKeyVaultCertificateIssuer** pobiera określonego wystawcy certyfikatu lub wystawców certyfikatów dla magazynu kluczy w magazynie kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6697e-109">The **Get-AzureKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="6697e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6697e-110">EXAMPLES</span></span>

### <span data-ttu-id="6697e-111">Przykład 1: uzyskiwanie wystawcy certyfikatu</span><span class="sxs-lookup"><span data-stu-id="6697e-111">Example 1: Get a certificate issuer</span></span>
```powershell
PS C:\> Get-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="6697e-112">To polecenie pobiera wystawcę certyfikatu o nazwie TestIssuer01.</span><span class="sxs-lookup"><span data-stu-id="6697e-112">This command gets the certificate issuer named TestIssuer01.</span></span>

## <span data-ttu-id="6697e-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6697e-113">PARAMETERS</span></span>

### <span data-ttu-id="6697e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6697e-114">-DefaultProfile</span></span>
<span data-ttu-id="6697e-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="6697e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6697e-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6697e-116">-InputObject</span></span>
<span data-ttu-id="6697e-117">Obiekt magazynu.</span><span class="sxs-lookup"><span data-stu-id="6697e-117">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6697e-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6697e-118">-Name</span></span>
<span data-ttu-id="6697e-119">Określa nazwę wystawcy certyfikatu do pobrania.</span><span class="sxs-lookup"><span data-stu-id="6697e-119">Specifies the name of the certificate issuer to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IssuerName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6697e-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6697e-120">-ResourceId</span></span>
<span data-ttu-id="6697e-121">Identyfikator zasobu magazynu.</span><span class="sxs-lookup"><span data-stu-id="6697e-121">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6697e-122">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="6697e-122">-VaultName</span></span>
<span data-ttu-id="6697e-123">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="6697e-123">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="6697e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6697e-124">CommonParameters</span></span>
<span data-ttu-id="6697e-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6697e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6697e-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6697e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6697e-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6697e-127">INPUTS</span></span>

### <span data-ttu-id="6697e-128">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="6697e-128">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="6697e-129">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6697e-129">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="6697e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="6697e-130">System.String</span></span>

## <span data-ttu-id="6697e-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6697e-131">OUTPUTS</span></span>

### <span data-ttu-id="6697e-132">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="6697e-132">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

### <span data-ttu-id="6697e-133">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="6697e-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="6697e-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6697e-134">NOTES</span></span>

## <span data-ttu-id="6697e-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6697e-135">RELATED LINKS</span></span>

[<span data-ttu-id="6697e-136">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="6697e-136">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="6697e-137">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="6697e-137">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


