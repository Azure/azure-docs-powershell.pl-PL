---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D788B84-0179-4A35-AC35-27C6F5FECB39
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 7b5f37cb42d128cbf44294520419c8f4d09124fa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871260"
---
# <span data-ttu-id="4fef0-101">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4fef0-101">Remove-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="4fef0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4fef0-102">SYNOPSIS</span></span>
<span data-ttu-id="4fef0-103">Usuwa certyfikat SSL z bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4fef0-103">Removes an SSL certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="4fef0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4fef0-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4fef0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4fef0-105">DESCRIPTION</span></span>
<span data-ttu-id="4fef0-106">Polecenie cmdlet **Remove-AzApplicationGatewaySslCertificate** usuwa certyfikat SSL (Secure Sockets Layer) z bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4fef0-106">The **Remove-AzApplicationGatewaySslCertificate** cmdlet removes a Secure Sockets Layer (SSL) certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="4fef0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4fef0-107">EXAMPLES</span></span>

### <span data-ttu-id="4fef0-108">Przykład 1: Usuwanie certyfikatu SSL z bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="4fef0-108">Example 1: Remove an SSL certificate from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert02"
```

<span data-ttu-id="4fef0-109">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 i zapisuje wynik w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="4fef0-109">The first command gets the application gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="4fef0-110">Drugie polecenie usuwa certyfikat SSL o nazwie Cert02 z bramy aplikacji przechowywanej w zmiennej $AppGW.</span><span class="sxs-lookup"><span data-stu-id="4fef0-110">The second command removes the SSL certificate named Cert02 from the application gateway stored in the $AppGW variable.</span></span>

## <span data-ttu-id="4fef0-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4fef0-111">PARAMETERS</span></span>

### <span data-ttu-id="4fef0-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4fef0-112">-ApplicationGateway</span></span>
<span data-ttu-id="4fef0-113">Określa bramę aplikacji, z której to polecenie cmdlet usuwa certyfikat SSL.</span><span class="sxs-lookup"><span data-stu-id="4fef0-113">Specifies the application gateway from which this cmdlet removes an SSL certificate.</span></span>

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

### <span data-ttu-id="4fef0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fef0-114">-DefaultProfile</span></span>
<span data-ttu-id="4fef0-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4fef0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4fef0-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4fef0-116">-Name</span></span>
<span data-ttu-id="4fef0-117">Określa nazwę certyfikatu SSL, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4fef0-117">Specifies the name of an SSL certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4fef0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fef0-118">CommonParameters</span></span>
<span data-ttu-id="4fef0-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fef0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fef0-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fef0-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fef0-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4fef0-121">INPUTS</span></span>

### <span data-ttu-id="4fef0-122">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4fef0-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4fef0-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4fef0-123">OUTPUTS</span></span>

### <span data-ttu-id="4fef0-124">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4fef0-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4fef0-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4fef0-125">NOTES</span></span>

## <span data-ttu-id="4fef0-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4fef0-126">RELATED LINKS</span></span>

[<span data-ttu-id="4fef0-127">Dodaj-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4fef0-127">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="4fef0-128">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4fef0-128">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="4fef0-129">Nowe — AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4fef0-129">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="4fef0-130">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4fef0-130">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


