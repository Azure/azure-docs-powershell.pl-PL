---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5D788B84-0179-4A35-AC35-27C6F5FECB39
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaysslcertificate
schema: 2.0.0
ms.openlocfilehash: eeab1f5699af5de737bc1e0390c35d387acfdd98
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897894"
---
# <span data-ttu-id="06043-101">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="06043-101">Remove-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="06043-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="06043-102">SYNOPSIS</span></span>
<span data-ttu-id="06043-103">Usuwa certyfikat SSL z bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="06043-103">Removes an SSL certificate from an Azure application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06043-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="06043-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewaySslCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06043-105">Opis</span><span class="sxs-lookup"><span data-stu-id="06043-105">DESCRIPTION</span></span>
<span data-ttu-id="06043-106">Polecenie cmdlet **Remove-AzureRmApplicationGatewaySslCertificate** usuwa certyfikat SSL (Secure Sockets Layer) z bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="06043-106">The **Remove-AzureRmApplicationGatewaySslCertificate** cmdlet removes a Secure Sockets Layer (SSL) certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="06043-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="06043-107">EXAMPLES</span></span>

### <span data-ttu-id="06043-108">Przykład 1: Usuwanie certyfikatu SSL z bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="06043-108">Example 1: Remove an SSL certificate from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert02"
```

<span data-ttu-id="06043-109">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 i zapisuje wynik w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="06043-109">The first command gets the application gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>

<span data-ttu-id="06043-110">Drugie polecenie usuwa certyfikat SSL o nazwie Cert02 z bramy aplikacji przechowywanej w zmiennej $AppGW.</span><span class="sxs-lookup"><span data-stu-id="06043-110">The second command removes the SSL certificate named Cert02 from the application gateway stored in the $AppGW variable.</span></span>

## <span data-ttu-id="06043-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="06043-111">PARAMETERS</span></span>

### <span data-ttu-id="06043-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="06043-112">-ApplicationGateway</span></span>
<span data-ttu-id="06043-113">Określa bramę aplikacji, z której to polecenie cmdlet usuwa certyfikat SSL.</span><span class="sxs-lookup"><span data-stu-id="06043-113">Specifies the application gateway from which this cmdlet removes an SSL certificate.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06043-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06043-114">-DefaultProfile</span></span>
<span data-ttu-id="06043-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="06043-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06043-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="06043-116">-Name</span></span>
<span data-ttu-id="06043-117">Określa nazwę certyfikatu SSL, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06043-117">Specifies the name of an SSL certificate that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06043-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06043-118">CommonParameters</span></span>
<span data-ttu-id="06043-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06043-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06043-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06043-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06043-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="06043-121">INPUTS</span></span>

### <span data-ttu-id="06043-122">System. String</span><span class="sxs-lookup"><span data-stu-id="06043-122">System.String</span></span>

## <span data-ttu-id="06043-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="06043-123">OUTPUTS</span></span>

### <span data-ttu-id="06043-124">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="06043-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="06043-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="06043-125">NOTES</span></span>

## <span data-ttu-id="06043-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="06043-126">RELATED LINKS</span></span>

[<span data-ttu-id="06043-127">Dodaj-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="06043-127">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="06043-128">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="06043-128">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="06043-129">Nowe — AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="06043-129">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="06043-130">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="06043-130">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)


