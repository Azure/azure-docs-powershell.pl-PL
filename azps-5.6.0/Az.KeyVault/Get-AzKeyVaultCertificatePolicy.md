---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0729687C-3104-4136-A80D-16BAEBD6B76C
online version: https://docs.microsoft.com/powershell/module/az.keyvault/get-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: cace261f300dc63b9568413fb8a709c323349531
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991138"
---
# <span data-ttu-id="d5097-101">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="d5097-101">Get-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="d5097-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5097-102">SYNOPSIS</span></span>
<span data-ttu-id="d5097-103">Pobiera zasady dla certyfikatu w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="d5097-103">Gets the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="d5097-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d5097-104">SYNTAX</span></span>

### <span data-ttu-id="d5097-105">VaultAndCertName (domyślne)</span><span class="sxs-lookup"><span data-stu-id="d5097-105">VaultAndCertName (Default)</span></span>
```
Get-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5097-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="d5097-106">InputObject</span></span>
```
Get-AzKeyVaultCertificatePolicy [-InputObject] <PSKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5097-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="d5097-107">DESCRIPTION</span></span>
<span data-ttu-id="d5097-108">Polecenie **cmdlet Get-AzKeyVaultCertificatePolicy** pobiera zasady dla certyfikatu w magazynie kluczy w magazynie kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d5097-108">The **Get-AzKeyVaultCertificatePolicy** cmdlet gets the policy for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="d5097-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d5097-109">EXAMPLES</span></span>

### <span data-ttu-id="d5097-110">Przykład 1. Uzyskiwanie zasad certyfikatu</span><span class="sxs-lookup"><span data-stu-id="d5097-110">Example 1: Get a certificate policy</span></span>
```powershell
PS C:\ >Get-AzKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01"

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
CertificateType                 :
RenewAtNumberOfDaysBeforeExpiry : 
RenewAtPercentageLifetime       : 80
EmailAtNumberOfDaysBeforeExpiry :
EmailAtPercentageLifetime       :
Enabled                         : True
Created                         : 2/8/2016 11:10:29 PM
Updated                         : 2/8/2016 11:10:29 PM
```

<span data-ttu-id="d5097-111">To polecenie pobiera zasady certyfikatu TestCert01 w magazynie kluczy ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="d5097-111">This command gets the certificate policy for TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="d5097-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5097-112">PARAMETERS</span></span>

### <span data-ttu-id="d5097-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5097-113">-DefaultProfile</span></span>
<span data-ttu-id="d5097-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="d5097-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d5097-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d5097-115">-InputObject</span></span>
<span data-ttu-id="d5097-116">Obiekt Certificate.</span><span class="sxs-lookup"><span data-stu-id="d5097-116">Certificate Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5097-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d5097-117">-Name</span></span>
<span data-ttu-id="d5097-118">Określa nazwę certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="d5097-118">Specifies the name of a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: VaultAndCertName
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5097-119">-VaultName</span><span class="sxs-lookup"><span data-stu-id="d5097-119">-VaultName</span></span>
<span data-ttu-id="d5097-120">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="d5097-120">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: VaultAndCertName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5097-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5097-121">CommonParameters</span></span>
<span data-ttu-id="d5097-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5097-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5097-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d5097-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5097-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d5097-124">INPUTS</span></span>

### <span data-ttu-id="d5097-125">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="d5097-125">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="d5097-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d5097-126">OUTPUTS</span></span>

### <span data-ttu-id="d5097-127">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="d5097-127">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="d5097-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d5097-128">NOTES</span></span>

## <span data-ttu-id="d5097-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d5097-129">RELATED LINKS</span></span>

[<span data-ttu-id="d5097-130">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="d5097-130">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="d5097-131">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="d5097-131">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

