---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 919B3755-81D4-43FB-AE8C-B071329A61D9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaysslcertificate
schema: 2.0.0
ms.openlocfilehash: 6e2dceadf11323eb1798435df426c063f4d58858
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899285"
---
# <span data-ttu-id="b9959-101">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b9959-101">Get-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="b9959-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b9959-102">SYNOPSIS</span></span>
<span data-ttu-id="b9959-103">Pobiera certyfikat SSL dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="b9959-103">Gets an SSL certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9959-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b9959-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySslCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9959-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b9959-105">DESCRIPTION</span></span>
<span data-ttu-id="b9959-106">Polecenie cmdlet **Get-AzureRmApplicationGatewaySslCertificate** pobiera certyfikat SSL dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="b9959-106">The **Get-AzureRmApplicationGatewaySslCertificate** cmdlet gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="b9959-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b9959-107">EXAMPLES</span></span>

### <span data-ttu-id="b9959-108">Przykład 1: uzyskiwanie określonego certyfikatu SSL</span><span class="sxs-lookup"><span data-stu-id="b9959-108">Example 1: Get a specific SSL certificate</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Cert = Get-AzureRmApplicationGatewaySslCertificate -Name "Cert01" -ApplicationGateway $AppGW
```

<span data-ttu-id="b9959-109">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 i zapisuje wynik w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="b9959-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="b9959-110">Drugie polecenie pobiera certyfikat SSL o nazwie Cert01 z bramy aplikacji przechowywanej w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="b9959-110">The second command gets the SSL certificate named Cert01 from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="b9959-111">Polecenie zapisuje certyfikat w zmiennej o nazwie $Cert.</span><span class="sxs-lookup"><span data-stu-id="b9959-111">The command stores the certificate in the variable named $Cert.</span></span>

### <span data-ttu-id="b9959-112">Przykład 2: uzyskiwanie listy certyfikatów SSL</span><span class="sxs-lookup"><span data-stu-id="b9959-112">Example 2: Get a list of SSL certificates</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Certs = Get-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW
```

<span data-ttu-id="b9959-113">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 i zapisuje wynik w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="b9959-113">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="b9959-114">W tym drugim poleceniu jest pobierana Lista certyfikatów SSL z bramy aplikacji przechowywanej w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="b9959-114">This second command gets a list of SSL certificates from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="b9959-115">Polecenie zapisuje wyniki w zmiennej o nazwie $Certs.</span><span class="sxs-lookup"><span data-stu-id="b9959-115">The command then stores the results in the variable named $Certs.</span></span>

## <span data-ttu-id="b9959-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b9959-116">PARAMETERS</span></span>

### <span data-ttu-id="b9959-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9959-117">-ApplicationGateway</span></span>
<span data-ttu-id="b9959-118">Określa obiekt bramy aplikacji, który zawiera certyfikat SSL.</span><span class="sxs-lookup"><span data-stu-id="b9959-118">Specifies the application gateway object that contains the SSL certificate.</span></span>

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

### <span data-ttu-id="b9959-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9959-119">-DefaultProfile</span></span>
<span data-ttu-id="b9959-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b9959-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9959-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b9959-121">-Name</span></span>
<span data-ttu-id="b9959-122">Określa nazwę puli certyfikatów SSL, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9959-122">Specifies the name of SSL certificate pool that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9959-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9959-123">CommonParameters</span></span>
<span data-ttu-id="b9959-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9959-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9959-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9959-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9959-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b9959-126">INPUTS</span></span>

### <span data-ttu-id="b9959-127">System. String</span><span class="sxs-lookup"><span data-stu-id="b9959-127">System.String</span></span>

## <span data-ttu-id="b9959-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b9959-128">OUTPUTS</span></span>

### <span data-ttu-id="b9959-129">Microsoft. Azure. Commands. Network. models. PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b9959-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="b9959-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b9959-130">NOTES</span></span>

## <span data-ttu-id="b9959-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b9959-131">RELATED LINKS</span></span>

[<span data-ttu-id="b9959-132">Dodaj-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b9959-132">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="b9959-133">Nowe — AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b9959-133">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="b9959-134">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b9959-134">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="b9959-135">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b9959-135">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)


