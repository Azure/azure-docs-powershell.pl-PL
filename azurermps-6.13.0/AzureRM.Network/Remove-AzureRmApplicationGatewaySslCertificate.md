---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5D788B84-0179-4A35-AC35-27C6F5FECB39
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewaySslCertificate.md
ms.openlocfilehash: 865b9a576219cbaf7d938094baf923c497436e07
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543656"
---
# <span data-ttu-id="34548-101">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="34548-101">Remove-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="34548-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="34548-102">SYNOPSIS</span></span>
<span data-ttu-id="34548-103">Usuwa certyfikat SSL z bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="34548-103">Removes an SSL certificate from an Azure application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34548-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="34548-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewaySslCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34548-105">Opis</span><span class="sxs-lookup"><span data-stu-id="34548-105">DESCRIPTION</span></span>
<span data-ttu-id="34548-106">Polecenie cmdlet **Remove-AzureRmApplicationGatewaySslCertificate** usuwa certyfikat SSL (Secure Sockets Layer) z bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="34548-106">The **Remove-AzureRmApplicationGatewaySslCertificate** cmdlet removes a Secure Sockets Layer (SSL) certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="34548-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="34548-107">EXAMPLES</span></span>

### <span data-ttu-id="34548-108">Przykład 1: Usuwanie certyfikatu SSL z bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="34548-108">Example 1: Remove an SSL certificate from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert02"
```

<span data-ttu-id="34548-109">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 i zapisuje wynik w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="34548-109">The first command gets the application gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="34548-110">Drugie polecenie usuwa certyfikat SSL o nazwie Cert02 z bramy aplikacji przechowywanej w zmiennej $AppGW.</span><span class="sxs-lookup"><span data-stu-id="34548-110">The second command removes the SSL certificate named Cert02 from the application gateway stored in the $AppGW variable.</span></span>

## <span data-ttu-id="34548-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="34548-111">PARAMETERS</span></span>

### <span data-ttu-id="34548-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="34548-112">-ApplicationGateway</span></span>
<span data-ttu-id="34548-113">Określa bramę aplikacji, z której to polecenie cmdlet usuwa certyfikat SSL.</span><span class="sxs-lookup"><span data-stu-id="34548-113">Specifies the application gateway from which this cmdlet removes an SSL certificate.</span></span>

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

### <span data-ttu-id="34548-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34548-114">-DefaultProfile</span></span>
<span data-ttu-id="34548-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="34548-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34548-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="34548-116">-Name</span></span>
<span data-ttu-id="34548-117">Określa nazwę certyfikatu SSL, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34548-117">Specifies the name of an SSL certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="34548-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34548-118">CommonParameters</span></span>
<span data-ttu-id="34548-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34548-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34548-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34548-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34548-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34548-121">INPUTS</span></span>

### <span data-ttu-id="34548-122">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="34548-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="34548-123">Parametry: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="34548-123">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="34548-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="34548-124">OUTPUTS</span></span>

### <span data-ttu-id="34548-125">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="34548-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="34548-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="34548-126">NOTES</span></span>

## <span data-ttu-id="34548-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="34548-127">RELATED LINKS</span></span>

[<span data-ttu-id="34548-128">Dodaj-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="34548-128">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="34548-129">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="34548-129">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="34548-130">Nowe — AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="34548-130">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="34548-131">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="34548-131">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)


