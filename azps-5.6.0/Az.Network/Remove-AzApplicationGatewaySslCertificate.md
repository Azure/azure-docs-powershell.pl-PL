---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D788B84-0179-4A35-AC35-27C6F5FECB39
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: b8e74c8630dc7f5ba0cd3633314b416ca9a3e39e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986728"
---
# <span data-ttu-id="dfe14-101">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="dfe14-101">Remove-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="dfe14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfe14-102">SYNOPSIS</span></span>
<span data-ttu-id="dfe14-103">Usuwa certyfikat SSL z bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="dfe14-103">Removes an SSL certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="dfe14-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="dfe14-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dfe14-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="dfe14-105">DESCRIPTION</span></span>
<span data-ttu-id="dfe14-106">Polecenie cmdlet **Remove-AzApplicationGatewaySslCertificate** usuwa certyfikat Secure Sockets Layer (SSL) z bramy aplikacji azure.</span><span class="sxs-lookup"><span data-stu-id="dfe14-106">The **Remove-AzApplicationGatewaySslCertificate** cmdlet removes a Secure Sockets Layer (SSL) certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="dfe14-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="dfe14-107">EXAMPLES</span></span>

### <span data-ttu-id="dfe14-108">Przykład 1. Usuwanie certyfikatu SSL z bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="dfe14-108">Example 1: Remove an SSL certificate from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert02"
```

<span data-ttu-id="dfe14-109">Pierwsze polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01 i przechowuje wynik w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="dfe14-109">The first command gets the application gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="dfe14-110">Drugie polecenie usuwa certyfikat SSL o nazwie Cert02 z bramy aplikacji przechowywanej w $AppGW danych.</span><span class="sxs-lookup"><span data-stu-id="dfe14-110">The second command removes the SSL certificate named Cert02 from the application gateway stored in the $AppGW variable.</span></span>

## <span data-ttu-id="dfe14-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dfe14-111">PARAMETERS</span></span>

### <span data-ttu-id="dfe14-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dfe14-112">-ApplicationGateway</span></span>
<span data-ttu-id="dfe14-113">Określa bramę aplikacji, z której to polecenie cmdlet usuwa certyfikat SSL.</span><span class="sxs-lookup"><span data-stu-id="dfe14-113">Specifies the application gateway from which this cmdlet removes an SSL certificate.</span></span>

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

### <span data-ttu-id="dfe14-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfe14-114">-DefaultProfile</span></span>
<span data-ttu-id="dfe14-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="dfe14-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dfe14-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="dfe14-116">-Name</span></span>
<span data-ttu-id="dfe14-117">Określa nazwę certyfikatu SSL, który zostanie usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dfe14-117">Specifies the name of an SSL certificate that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfe14-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfe14-118">CommonParameters</span></span>
<span data-ttu-id="dfe14-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfe14-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfe14-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfe14-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfe14-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dfe14-121">INPUTS</span></span>

### <span data-ttu-id="dfe14-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dfe14-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="dfe14-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dfe14-123">OUTPUTS</span></span>

### <span data-ttu-id="dfe14-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dfe14-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="dfe14-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="dfe14-125">NOTES</span></span>

## <span data-ttu-id="dfe14-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dfe14-126">RELATED LINKS</span></span>

[<span data-ttu-id="dfe14-127">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="dfe14-127">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="dfe14-128">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="dfe14-128">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="dfe14-129">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="dfe14-129">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="dfe14-130">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="dfe14-130">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


