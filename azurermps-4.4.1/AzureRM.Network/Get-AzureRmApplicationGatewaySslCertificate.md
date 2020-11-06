---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 919B3755-81D4-43FB-AE8C-B071329A61D9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslCertificate.md
ms.openlocfilehash: da831810461e763acc51319ea4d6662c45a1c3ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544711"
---
# <span data-ttu-id="bf5c8-101">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="bf5c8-101">Get-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="bf5c8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bf5c8-102">SYNOPSIS</span></span>
<span data-ttu-id="bf5c8-103">Pobiera certyfikat SSL dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="bf5c8-103">Gets an SSL certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf5c8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bf5c8-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySslCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf5c8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bf5c8-105">DESCRIPTION</span></span>
<span data-ttu-id="bf5c8-106">Polecenie cmdlet **Get-AzureRmApplicationGatewaySslCertificate** pobiera certyfikat SSL dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="bf5c8-106">The **Get-AzureRmApplicationGatewaySslCertificate** cmdlet gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="bf5c8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bf5c8-107">EXAMPLES</span></span>

### <span data-ttu-id="bf5c8-108">Przykład 1: uzyskiwanie określonego certyfikatu SSL</span><span class="sxs-lookup"><span data-stu-id="bf5c8-108">Example 1: Get a specific SSL certificate</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Cert = Get-AzureRmApplicationGatewaySslCertificate -Name "Cert01" -ApplicationGateway $AppGW
```

<span data-ttu-id="bf5c8-109">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 i zapisuje wynik w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="bf5c8-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="bf5c8-110">Drugie polecenie pobiera certyfikat SSL o nazwie Cert01 z bramy aplikacji przechowywanej w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="bf5c8-110">The second command gets the SSL certificate named Cert01 from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="bf5c8-111">Polecenie zapisuje certyfikat w zmiennej o nazwie $Cert.</span><span class="sxs-lookup"><span data-stu-id="bf5c8-111">The command stores the certificate in the variable named $Cert.</span></span>

### <span data-ttu-id="bf5c8-112">Przykład 2: uzyskiwanie listy certyfikatów SSL</span><span class="sxs-lookup"><span data-stu-id="bf5c8-112">Example 2: Get a list of SSL certificates</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Certs = Get-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW
```

<span data-ttu-id="bf5c8-113">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 i zapisuje wynik w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="bf5c8-113">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="bf5c8-114">W tym drugim poleceniu jest pobierana Lista certyfikatów SSL z bramy aplikacji przechowywanej w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="bf5c8-114">This second command gets a list of SSL certificates from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="bf5c8-115">Polecenie zapisuje wyniki w zmiennej o nazwie $Certs.</span><span class="sxs-lookup"><span data-stu-id="bf5c8-115">The command then stores the results in the variable named $Certs.</span></span>

## <span data-ttu-id="bf5c8-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bf5c8-116">PARAMETERS</span></span>

### <span data-ttu-id="bf5c8-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bf5c8-117">-ApplicationGateway</span></span>
<span data-ttu-id="bf5c8-118">Określa obiekt bramy aplikacji, który zawiera certyfikat SSL.</span><span class="sxs-lookup"><span data-stu-id="bf5c8-118">Specifies the application gateway object that contains the SSL certificate.</span></span>

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

### <span data-ttu-id="bf5c8-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bf5c8-119">-Name</span></span>
<span data-ttu-id="bf5c8-120">Określa nazwę puli certyfikatów SSL, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf5c8-120">Specifies the name of SSL certificate pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="bf5c8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf5c8-121">-DefaultProfile</span></span>
<span data-ttu-id="bf5c8-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bf5c8-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf5c8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf5c8-123">CommonParameters</span></span>
<span data-ttu-id="bf5c8-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf5c8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf5c8-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf5c8-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf5c8-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bf5c8-126">INPUTS</span></span>

### <span data-ttu-id="bf5c8-127">System. String</span><span class="sxs-lookup"><span data-stu-id="bf5c8-127">System.String</span></span>

## <span data-ttu-id="bf5c8-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bf5c8-128">OUTPUTS</span></span>

### <span data-ttu-id="bf5c8-129">Microsoft. Azure. Commands. Network. models. PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="bf5c8-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="bf5c8-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bf5c8-130">NOTES</span></span>

## <span data-ttu-id="bf5c8-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bf5c8-131">RELATED LINKS</span></span>

[<span data-ttu-id="bf5c8-132">Dodaj-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="bf5c8-132">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="bf5c8-133">Nowe — AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="bf5c8-133">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="bf5c8-134">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="bf5c8-134">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="bf5c8-135">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="bf5c8-135">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)


