---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0729687C-3104-4136-A80D-16BAEBD6B76C
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: d6e2225cc7441d4c370d990aa45c9b2c2bb40457
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98500940"
---
# <span data-ttu-id="13afd-101">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="13afd-101">Get-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="13afd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="13afd-102">SYNOPSIS</span></span>
<span data-ttu-id="13afd-103">Pobiera zasady dotyczące certyfikatu w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="13afd-103">Gets the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="13afd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="13afd-104">SYNTAX</span></span>

### <span data-ttu-id="13afd-105">VaultAndCertName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="13afd-105">VaultAndCertName (Default)</span></span>
```
Get-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13afd-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="13afd-106">InputObject</span></span>
```
Get-AzKeyVaultCertificatePolicy [-InputObject] <PSKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13afd-107">Opis</span><span class="sxs-lookup"><span data-stu-id="13afd-107">DESCRIPTION</span></span>
<span data-ttu-id="13afd-108">Polecenie cmdlet **Get-AzKeyVaultCertificatePolicy** pobiera zasady dotyczące certyfikatu w magazynie kluczy w magazynie kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="13afd-108">The **Get-AzKeyVaultCertificatePolicy** cmdlet gets the policy for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="13afd-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="13afd-109">EXAMPLES</span></span>

### <span data-ttu-id="13afd-110">Przykład 1: uzyskiwanie zasad certyfikatów</span><span class="sxs-lookup"><span data-stu-id="13afd-110">Example 1: Get a certificate policy</span></span>
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

<span data-ttu-id="13afd-111">To polecenie pobiera zasady certyfikatu dla certyfikatu TestCert01 w magazynie kluczy ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="13afd-111">This command gets the certificate policy for TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="13afd-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="13afd-112">PARAMETERS</span></span>

### <span data-ttu-id="13afd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13afd-113">-DefaultProfile</span></span>
<span data-ttu-id="13afd-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="13afd-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="13afd-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="13afd-115">-InputObject</span></span>
<span data-ttu-id="13afd-116">Obiekt Certificate (certyfikat).</span><span class="sxs-lookup"><span data-stu-id="13afd-116">Certificate Object.</span></span>

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

### <span data-ttu-id="13afd-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="13afd-117">-Name</span></span>
<span data-ttu-id="13afd-118">Określa nazwę certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="13afd-118">Specifies the name of a certificate.</span></span>

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

### <span data-ttu-id="13afd-119">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="13afd-119">-VaultName</span></span>
<span data-ttu-id="13afd-120">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="13afd-120">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="13afd-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13afd-121">CommonParameters</span></span>
<span data-ttu-id="13afd-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13afd-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13afd-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="13afd-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13afd-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13afd-124">INPUTS</span></span>

### <span data-ttu-id="13afd-125">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="13afd-125">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="13afd-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="13afd-126">OUTPUTS</span></span>

### <span data-ttu-id="13afd-127">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="13afd-127">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="13afd-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="13afd-128">NOTES</span></span>

## <span data-ttu-id="13afd-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="13afd-129">RELATED LINKS</span></span>

[<span data-ttu-id="13afd-130">Nowe — AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="13afd-130">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="13afd-131">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="13afd-131">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

