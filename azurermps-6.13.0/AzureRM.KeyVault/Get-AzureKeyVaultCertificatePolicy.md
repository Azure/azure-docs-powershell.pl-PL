---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 0729687C-3104-4136-A80D-16BAEBD6B76C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: 8d03d93a374f2184a995d9cbcdb83050aa98a8ef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718318"
---
# <span data-ttu-id="db5b7-101">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="db5b7-101">Get-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="db5b7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="db5b7-102">SYNOPSIS</span></span>
<span data-ttu-id="db5b7-103">Pobiera zasady dotyczące certyfikatu w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="db5b7-103">Gets the policy for a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db5b7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="db5b7-104">SYNTAX</span></span>

### <span data-ttu-id="db5b7-105">VaultAndCertName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="db5b7-105">VaultAndCertName (Default)</span></span>
```
Get-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db5b7-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="db5b7-106">InputObject</span></span>
```
Get-AzureKeyVaultCertificatePolicy [-InputObject] <PSKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db5b7-107">Opis</span><span class="sxs-lookup"><span data-stu-id="db5b7-107">DESCRIPTION</span></span>
<span data-ttu-id="db5b7-108">Polecenie cmdlet **Get-AzureKeyVaultCertificatePolicy** pobiera zasady dotyczące certyfikatu w magazynie kluczy w magazynie kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="db5b7-108">The **Get-AzureKeyVaultCertificatePolicy** cmdlet gets the policy for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="db5b7-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="db5b7-109">EXAMPLES</span></span>

### <span data-ttu-id="db5b7-110">Przykład 1: uzyskiwanie zasad certyfikatów</span><span class="sxs-lookup"><span data-stu-id="db5b7-110">Example 1: Get a certificate policy</span></span>
```powershell
PS C:\ >Get-AzureKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01"

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

<span data-ttu-id="db5b7-111">To polecenie pobiera zasady certyfikatu dla certyfikatu TestCert01 w magazynie kluczy ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="db5b7-111">This command gets the certificate policy for TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="db5b7-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="db5b7-112">PARAMETERS</span></span>

### <span data-ttu-id="db5b7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db5b7-113">-DefaultProfile</span></span>
<span data-ttu-id="db5b7-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="db5b7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="db5b7-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="db5b7-115">-InputObject</span></span>
<span data-ttu-id="db5b7-116">Obiekt Certificate (certyfikat).</span><span class="sxs-lookup"><span data-stu-id="db5b7-116">Certificate Object.</span></span>

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

### <span data-ttu-id="db5b7-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="db5b7-117">-Name</span></span>
<span data-ttu-id="db5b7-118">Określa nazwę certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="db5b7-118">Specifies the name of a certificate.</span></span>

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

### <span data-ttu-id="db5b7-119">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="db5b7-119">-VaultName</span></span>
<span data-ttu-id="db5b7-120">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="db5b7-120">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="db5b7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db5b7-121">CommonParameters</span></span>
<span data-ttu-id="db5b7-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db5b7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db5b7-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db5b7-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db5b7-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="db5b7-124">INPUTS</span></span>

### <span data-ttu-id="db5b7-125">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="db5b7-125">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>
<span data-ttu-id="db5b7-126">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="db5b7-126">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="db5b7-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="db5b7-127">OUTPUTS</span></span>

### <span data-ttu-id="db5b7-128">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="db5b7-128">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="db5b7-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="db5b7-129">NOTES</span></span>

## <span data-ttu-id="db5b7-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="db5b7-130">RELATED LINKS</span></span>

[<span data-ttu-id="db5b7-131">Nowe — AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="db5b7-131">New-AzureKeyVaultCertificatePolicy</span></span>](./New-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="db5b7-132">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="db5b7-132">Set-AzureKeyVaultCertificatePolicy</span></span>](./Set-AzureKeyVaultCertificatePolicy.md)

