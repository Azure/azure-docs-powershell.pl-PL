---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 919B3755-81D4-43FB-AE8C-B071329A61D9
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: aa6dbacb85263d8f0169f913c07e56a9dbd1c7ba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994057"
---
# <span data-ttu-id="b0d90-101">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b0d90-101">Get-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="b0d90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0d90-102">SYNOPSIS</span></span>
<span data-ttu-id="b0d90-103">Otrzymuje certyfikat SSL dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="b0d90-103">Gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="b0d90-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b0d90-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0d90-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b0d90-105">DESCRIPTION</span></span>
<span data-ttu-id="b0d90-106">Polecenie **cmdlet Get-AzApplicationGatewaySslCertificate** otrzymuje certyfikat SSL dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="b0d90-106">The **Get-AzApplicationGatewaySslCertificate** cmdlet gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="b0d90-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b0d90-107">EXAMPLES</span></span>

### <span data-ttu-id="b0d90-108">Przykład 1. Uzyskiwanie określonego certyfikatu SSL</span><span class="sxs-lookup"><span data-stu-id="b0d90-108">Example 1: Get a specific SSL certificate</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Cert = Get-AzApplicationGatewaySslCertificate -Name "Cert01" -ApplicationGateway $AppGW
```

<span data-ttu-id="b0d90-109">Pierwsze polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01 i przechowuje wynik w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="b0d90-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="b0d90-110">Drugie polecenie pobiera certyfikat SSL o nazwie Cert01 z bramy aplikacji przechowywanej w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="b0d90-110">The second command gets the SSL certificate named Cert01 from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="b0d90-111">Polecenie przechowuje certyfikat w zmiennej o nazwie $Cert.</span><span class="sxs-lookup"><span data-stu-id="b0d90-111">The command stores the certificate in the variable named $Cert.</span></span>

### <span data-ttu-id="b0d90-112">Przykład 2. Uzyskiwanie listy certyfikatów SSL</span><span class="sxs-lookup"><span data-stu-id="b0d90-112">Example 2: Get a list of SSL certificates</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Certs = Get-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW
```

<span data-ttu-id="b0d90-113">Pierwsze polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01 i przechowuje wynik w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="b0d90-113">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="b0d90-114">Drugie polecenie pobiera listę certyfikatów SSL z bramy aplikacji przechowywaną w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="b0d90-114">This second command gets a list of SSL certificates from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="b0d90-115">Następnie polecenie przechowuje wyniki w zmiennej o nazwie $Certs.</span><span class="sxs-lookup"><span data-stu-id="b0d90-115">The command then stores the results in the variable named $Certs.</span></span>

## <span data-ttu-id="b0d90-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0d90-116">PARAMETERS</span></span>

### <span data-ttu-id="b0d90-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b0d90-117">-ApplicationGateway</span></span>
<span data-ttu-id="b0d90-118">Określa obiekt bramy aplikacji zawierający certyfikat SSL.</span><span class="sxs-lookup"><span data-stu-id="b0d90-118">Specifies the application gateway object that contains the SSL certificate.</span></span>

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

### <span data-ttu-id="b0d90-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0d90-119">-DefaultProfile</span></span>
<span data-ttu-id="b0d90-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b0d90-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0d90-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b0d90-121">-Name</span></span>
<span data-ttu-id="b0d90-122">Określa nazwę puli certyfikatów SSL, która otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0d90-122">Specifies the name of SSL certificate pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b0d90-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0d90-123">CommonParameters</span></span>
<span data-ttu-id="b0d90-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0d90-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0d90-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b0d90-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0d90-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b0d90-126">INPUTS</span></span>

### <span data-ttu-id="b0d90-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b0d90-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b0d90-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b0d90-128">OUTPUTS</span></span>

### <span data-ttu-id="b0d90-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b0d90-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="b0d90-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b0d90-130">NOTES</span></span>

## <span data-ttu-id="b0d90-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b0d90-131">RELATED LINKS</span></span>

[<span data-ttu-id="b0d90-132">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b0d90-132">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="b0d90-133">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b0d90-133">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="b0d90-134">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b0d90-134">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="b0d90-135">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b0d90-135">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


