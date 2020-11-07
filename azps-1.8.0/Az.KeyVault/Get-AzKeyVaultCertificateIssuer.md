---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: dc1ee6f168a417c612e01d02c93d8729cc2563af
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867992"
---
# <span data-ttu-id="13ae1-101">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="13ae1-101">Get-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="13ae1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="13ae1-102">SYNOPSIS</span></span>
<span data-ttu-id="13ae1-103">Pobiera wystawcę certyfikatu dla magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="13ae1-103">Gets a certificate issuer for a key vault.</span></span>

## <span data-ttu-id="13ae1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="13ae1-104">SYNTAX</span></span>

### <span data-ttu-id="13ae1-105">ByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="13ae1-105">ByName (Default)</span></span>
```
Get-AzKeyVaultCertificateIssuer [-VaultName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13ae1-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="13ae1-106">ByInputObject</span></span>
```
Get-AzKeyVaultCertificateIssuer [-InputObject] <PSKeyVault> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13ae1-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="13ae1-107">ByResourceId</span></span>
```
Get-AzKeyVaultCertificateIssuer [-ResourceId] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13ae1-108">Opis</span><span class="sxs-lookup"><span data-stu-id="13ae1-108">DESCRIPTION</span></span>
<span data-ttu-id="13ae1-109">Polecenie cmdlet **Get-AzKeyVaultCertificateIssuer** pobiera określonego wystawcy certyfikatu lub wystawców certyfikatów dla magazynu kluczy w magazynie kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="13ae1-109">The **Get-AzKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="13ae1-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="13ae1-110">EXAMPLES</span></span>

### <span data-ttu-id="13ae1-111">Przykład 1: uzyskiwanie wystawcy certyfikatu</span><span class="sxs-lookup"><span data-stu-id="13ae1-111">Example 1: Get a certificate issuer</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="13ae1-112">To polecenie pobiera wystawcę certyfikatu o nazwie TestIssuer01.</span><span class="sxs-lookup"><span data-stu-id="13ae1-112">This command gets the certificate issuer named TestIssuer01.</span></span>

### <span data-ttu-id="13ae1-113">Przykład 2: wyświetlanie wystawców certyfikatów przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="13ae1-113">Example 2: List certificate issuers using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "test*"

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer02
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="13ae1-114">To polecenie otrzymuje wystawców certyfikatów rozpoczynających się od "test".</span><span class="sxs-lookup"><span data-stu-id="13ae1-114">This command gets the certificate issuers that start with "test".</span></span>

## <span data-ttu-id="13ae1-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="13ae1-115">PARAMETERS</span></span>

### <span data-ttu-id="13ae1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13ae1-116">-DefaultProfile</span></span>
<span data-ttu-id="13ae1-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="13ae1-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13ae1-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="13ae1-118">-InputObject</span></span>
<span data-ttu-id="13ae1-119">Obiekt magazynu.</span><span class="sxs-lookup"><span data-stu-id="13ae1-119">KeyVault object.</span></span>

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

### <span data-ttu-id="13ae1-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="13ae1-120">-Name</span></span>
<span data-ttu-id="13ae1-121">Określa nazwę wystawcy certyfikatu do pobrania.</span><span class="sxs-lookup"><span data-stu-id="13ae1-121">Specifies the name of the certificate issuer to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IssuerName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="13ae1-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13ae1-122">-ResourceId</span></span>
<span data-ttu-id="13ae1-123">Identyfikator zasobu magazynu.</span><span class="sxs-lookup"><span data-stu-id="13ae1-123">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="13ae1-124">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="13ae1-124">-VaultName</span></span>
<span data-ttu-id="13ae1-125">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="13ae1-125">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="13ae1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13ae1-126">CommonParameters</span></span>
<span data-ttu-id="13ae1-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13ae1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13ae1-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="13ae1-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13ae1-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13ae1-129">INPUTS</span></span>

### <span data-ttu-id="13ae1-130">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="13ae1-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="13ae1-131">System. String</span><span class="sxs-lookup"><span data-stu-id="13ae1-131">System.String</span></span>

## <span data-ttu-id="13ae1-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="13ae1-132">OUTPUTS</span></span>

### <span data-ttu-id="13ae1-133">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="13ae1-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

### <span data-ttu-id="13ae1-134">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="13ae1-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="13ae1-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="13ae1-135">NOTES</span></span>

## <span data-ttu-id="13ae1-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="13ae1-136">RELATED LINKS</span></span>

[<span data-ttu-id="13ae1-137">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="13ae1-137">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="13ae1-138">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="13ae1-138">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)


