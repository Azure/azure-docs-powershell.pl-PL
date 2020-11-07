---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: c37c55539f983b490c917e1fe062f14b252ee477
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717921"
---
# <span data-ttu-id="c8d2e-101">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="c8d2e-101">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="c8d2e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c8d2e-102">SYNOPSIS</span></span>
<span data-ttu-id="c8d2e-103">Pobiera zaufany certyfikat główny z określoną nazwą z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c8d2e-103">Gets the Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8d2e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c8d2e-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayTrustedRootCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8d2e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c8d2e-105">DESCRIPTION</span></span>
<span data-ttu-id="c8d2e-106">Polecenie cmdlet **Get-AzureRmApplicationGatewayTrustedRootCertificate** pobiera zaufany certyfikat główny z określoną nazwą z bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="c8d2e-106">The **Get-AzureRmApplicationGatewayTrustedRootCertificate** cmdlet gets Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="c8d2e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c8d2e-107">EXAMPLES</span></span>

### <span data-ttu-id="c8d2e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c8d2e-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedRootCert = Get-AzureRmApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCA.cer"
```

<span data-ttu-id="c8d2e-109">Pierwsze polecenie uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $gw.</span><span class="sxs-lookup"><span data-stu-id="c8d2e-109">The first command gets the Application Gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="c8d2e-110">Drugie polecenie pobiera zaufany certyfikat główny o określonej nazwie z bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="c8d2e-110">The second command gets the Trusted Root Certificate with a specified name from the Application Gateway.</span></span>

## <span data-ttu-id="c8d2e-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c8d2e-111">PARAMETERS</span></span>

### <span data-ttu-id="c8d2e-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c8d2e-112">-ApplicationGateway</span></span>
<span data-ttu-id="c8d2e-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c8d2e-113">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8d2e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8d2e-114">-DefaultProfile</span></span>
<span data-ttu-id="c8d2e-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c8d2e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8d2e-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c8d2e-116">-Name</span></span>
<span data-ttu-id="c8d2e-117">Nazwa certyfikatu TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="c8d2e-117">The name of the TrustedRoot certificate</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8d2e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8d2e-118">CommonParameters</span></span>
<span data-ttu-id="c8d2e-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8d2e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8d2e-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8d2e-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8d2e-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c8d2e-121">INPUTS</span></span>

### <span data-ttu-id="c8d2e-122">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c8d2e-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c8d2e-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c8d2e-123">OUTPUTS</span></span>

### <span data-ttu-id="c8d2e-124">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="c8d2e-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="c8d2e-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c8d2e-125">NOTES</span></span>

## <span data-ttu-id="c8d2e-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c8d2e-126">RELATED LINKS</span></span>
