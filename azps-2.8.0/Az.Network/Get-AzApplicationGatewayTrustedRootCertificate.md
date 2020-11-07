---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 1e617ef1283937116bd97c24a968f247fa7552de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870763"
---
# <span data-ttu-id="94a08-101">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="94a08-101">Get-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="94a08-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="94a08-102">SYNOPSIS</span></span>
<span data-ttu-id="94a08-103">Pobiera zaufany certyfikat główny z określoną nazwą z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="94a08-103">Gets the Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="94a08-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="94a08-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayTrustedRootCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94a08-105">Opis</span><span class="sxs-lookup"><span data-stu-id="94a08-105">DESCRIPTION</span></span>
<span data-ttu-id="94a08-106">Polecenie cmdlet **Get-AzApplicationGatewayTrustedRootCertificate** pobiera zaufany certyfikat główny z określoną nazwą z bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="94a08-106">The **Get-AzApplicationGatewayTrustedRootCertificate** cmdlet gets Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="94a08-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="94a08-107">EXAMPLES</span></span>

### <span data-ttu-id="94a08-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="94a08-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedRootCert = Get-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCA.cer"
```

<span data-ttu-id="94a08-109">Pierwsze polecenie uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $gw.</span><span class="sxs-lookup"><span data-stu-id="94a08-109">The first command gets the Application Gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="94a08-110">Drugie polecenie pobiera zaufany certyfikat główny o określonej nazwie z bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="94a08-110">The second command gets the Trusted Root Certificate with a specified name from the Application Gateway.</span></span>

## <span data-ttu-id="94a08-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="94a08-111">PARAMETERS</span></span>

### <span data-ttu-id="94a08-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="94a08-112">-ApplicationGateway</span></span>
<span data-ttu-id="94a08-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="94a08-113">The applicationGateway</span></span>

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

### <span data-ttu-id="94a08-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94a08-114">-DefaultProfile</span></span>
<span data-ttu-id="94a08-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="94a08-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94a08-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="94a08-116">-Name</span></span>
<span data-ttu-id="94a08-117">Nazwa certyfikatu TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="94a08-117">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="94a08-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94a08-118">CommonParameters</span></span>
<span data-ttu-id="94a08-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94a08-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94a08-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="94a08-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94a08-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="94a08-121">INPUTS</span></span>

### <span data-ttu-id="94a08-122">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="94a08-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="94a08-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="94a08-123">OUTPUTS</span></span>

### <span data-ttu-id="94a08-124">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="94a08-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="94a08-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="94a08-125">NOTES</span></span>

## <span data-ttu-id="94a08-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="94a08-126">RELATED LINKS</span></span>

[<span data-ttu-id="94a08-127">Dodaj-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="94a08-127">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="94a08-128">Nowe — AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="94a08-128">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="94a08-129">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="94a08-129">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="94a08-130">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="94a08-130">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
