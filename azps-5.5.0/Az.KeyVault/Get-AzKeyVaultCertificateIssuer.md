---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: d089cf44e14e70be8b377de310ab4a332ae2d1a1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188179"
---
# <span data-ttu-id="22ffb-101">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="22ffb-101">Get-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="22ffb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22ffb-102">SYNOPSIS</span></span>
<span data-ttu-id="22ffb-103">Pobiera wystawcę certyfikatu dla magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="22ffb-103">Gets a certificate issuer for a key vault.</span></span>

## <span data-ttu-id="22ffb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="22ffb-104">SYNTAX</span></span>

### <span data-ttu-id="22ffb-105">ByName (Default)</span><span class="sxs-lookup"><span data-stu-id="22ffb-105">ByName (Default)</span></span>
```
Get-AzKeyVaultCertificateIssuer [-VaultName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22ffb-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="22ffb-106">ByInputObject</span></span>
```
Get-AzKeyVaultCertificateIssuer [-InputObject] <PSKeyVault> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22ffb-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="22ffb-107">ByResourceId</span></span>
```
Get-AzKeyVaultCertificateIssuer [-ResourceId] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22ffb-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="22ffb-108">DESCRIPTION</span></span>
<span data-ttu-id="22ffb-109">Polecenie **cmdlet Get-AzKeyVaultCertificateIssuer** pobiera określonego wystawcę certyfikatu lub wszystkich wystawców certyfikatów dla magazynu kluczy w magazynie kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="22ffb-109">The **Get-AzKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="22ffb-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="22ffb-110">EXAMPLES</span></span>

### <span data-ttu-id="22ffb-111">Przykład 1. Uzyskiwanie wystawcy certyfikatu</span><span class="sxs-lookup"><span data-stu-id="22ffb-111">Example 1: Get a certificate issuer</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="22ffb-112">To polecenie pobiera wystawcę certyfikatu o nazwie TestIssuer01.</span><span class="sxs-lookup"><span data-stu-id="22ffb-112">This command gets the certificate issuer named TestIssuer01.</span></span>

### <span data-ttu-id="22ffb-113">Przykład 2. Lista wystawców certyfikatów przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="22ffb-113">Example 2: List certificate issuers using filtering</span></span>
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

<span data-ttu-id="22ffb-114">To polecenie pobiera wystawców certyfikatów, których wystawcy zaczynają od "testu".</span><span class="sxs-lookup"><span data-stu-id="22ffb-114">This command gets the certificate issuers that start with "test".</span></span>

## <span data-ttu-id="22ffb-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22ffb-115">PARAMETERS</span></span>

### <span data-ttu-id="22ffb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22ffb-116">-DefaultProfile</span></span>
<span data-ttu-id="22ffb-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="22ffb-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="22ffb-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="22ffb-118">-InputObject</span></span>
<span data-ttu-id="22ffb-119">Obiekt KeyVault.</span><span class="sxs-lookup"><span data-stu-id="22ffb-119">KeyVault object.</span></span>

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

### <span data-ttu-id="22ffb-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="22ffb-120">-Name</span></span>
<span data-ttu-id="22ffb-121">Określa nazwę wystawcy certyfikatu do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="22ffb-121">Specifies the name of the certificate issuer to get.</span></span>

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

### <span data-ttu-id="22ffb-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="22ffb-122">-ResourceId</span></span>
<span data-ttu-id="22ffb-123">Identyfikator zasobu KeyVault.</span><span class="sxs-lookup"><span data-stu-id="22ffb-123">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="22ffb-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="22ffb-124">-VaultName</span></span>
<span data-ttu-id="22ffb-125">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="22ffb-125">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="22ffb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22ffb-126">CommonParameters</span></span>
<span data-ttu-id="22ffb-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22ffb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22ffb-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="22ffb-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22ffb-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="22ffb-129">INPUTS</span></span>

### <span data-ttu-id="22ffb-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="22ffb-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="22ffb-131">System.String</span><span class="sxs-lookup"><span data-stu-id="22ffb-131">System.String</span></span>

## <span data-ttu-id="22ffb-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="22ffb-132">OUTPUTS</span></span>

### <span data-ttu-id="22ffb-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="22ffb-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

### <span data-ttu-id="22ffb-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="22ffb-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="22ffb-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="22ffb-135">NOTES</span></span>

## <span data-ttu-id="22ffb-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="22ffb-136">RELATED LINKS</span></span>

[<span data-ttu-id="22ffb-137">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="22ffb-137">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="22ffb-138">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="22ffb-138">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)


