---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 57A6DB40-43EC-402C-9784-06817ECD99B8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: d82a6801c9307bac5220df2e021eb1a8c4ba0bb3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717043"
---
# <span data-ttu-id="fcfdb-101">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="fcfdb-101">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="fcfdb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fcfdb-102">SYNOPSIS</span></span>
<span data-ttu-id="fcfdb-103">Pobiera regułę routingu żądań bramy Application.</span><span class="sxs-lookup"><span data-stu-id="fcfdb-103">Gets the request routing rule of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fcfdb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fcfdb-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayRequestRoutingRule [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fcfdb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fcfdb-105">DESCRIPTION</span></span>
<span data-ttu-id="fcfdb-106">Polecenie cmdlet **Get-AzureRmApplicationGatewayRequestRoutingRule** pobiera regułę rozsyłania żądań bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="fcfdb-106">The **Get-AzureRmApplicationGatewayRequestRoutingRule** cmdlet gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="fcfdb-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fcfdb-107">EXAMPLES</span></span>

### <span data-ttu-id="fcfdb-108">Przykład 1: uzyskiwanie określonej reguły routingu żądań</span><span class="sxs-lookup"><span data-stu-id="fcfdb-108">Example 1: Get a specific request routing rule</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzureRmApplicationGatewayRequestRoutingRule -"Rule01" -ApplicationGateway $AppGW
```

<span data-ttu-id="fcfdb-109">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 i zapisuje wynik w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="fcfdb-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="fcfdb-110">Drugie polecenie pobiera regułę rozsyłania żądań o nazwie Rule01 od bramy aplikacji zapisanej w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="fcfdb-110">The second command gets the request routing rule named Rule01 from the Application Gateway stored in the variable named $AppGW.</span></span>

### <span data-ttu-id="fcfdb-111">Przykład 2: uzyskiwanie listy reguł rozsyłania żądań</span><span class="sxs-lookup"><span data-stu-id="fcfdb-111">Example 2: Get a list of request routing rules</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rules = Get-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGW
```

<span data-ttu-id="fcfdb-112">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 i zapisuje wynik w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="fcfdb-112">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="fcfdb-113">Drugie polecenie pobiera listę reguł rozsyłania żądań od bramy aplikacji zapisanej w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="fcfdb-113">The second command gets a list of request routing rules from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="fcfdb-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fcfdb-114">PARAMETERS</span></span>

### <span data-ttu-id="fcfdb-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fcfdb-115">-ApplicationGateway</span></span>
<span data-ttu-id="fcfdb-116">Określa obiekt bramy aplikacji, który zawiera regułę routingu żądań.</span><span class="sxs-lookup"><span data-stu-id="fcfdb-116">Specifies the application gateway object that contains request routing rule.</span></span>

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

### <span data-ttu-id="fcfdb-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fcfdb-117">-Name</span></span>
<span data-ttu-id="fcfdb-118">Określa nazwę reguły rozsyłania żądań, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fcfdb-118">Specifies the name of the request routing rule which this cmdlet gets.</span></span>

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

### <span data-ttu-id="fcfdb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcfdb-119">-DefaultProfile</span></span>
<span data-ttu-id="fcfdb-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fcfdb-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fcfdb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcfdb-121">CommonParameters</span></span>
<span data-ttu-id="fcfdb-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcfdb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcfdb-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcfdb-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcfdb-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fcfdb-124">INPUTS</span></span>

### <span data-ttu-id="fcfdb-125">System. String</span><span class="sxs-lookup"><span data-stu-id="fcfdb-125">System.String</span></span>

## <span data-ttu-id="fcfdb-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fcfdb-126">OUTPUTS</span></span>

### <span data-ttu-id="fcfdb-127">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="fcfdb-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="fcfdb-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fcfdb-128">NOTES</span></span>

## <span data-ttu-id="fcfdb-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fcfdb-129">RELATED LINKS</span></span>

[<span data-ttu-id="fcfdb-130">Dodaj-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="fcfdb-130">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Add-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="fcfdb-131">Nowe — AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="fcfdb-131">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="fcfdb-132">Remove-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="fcfdb-132">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="fcfdb-133">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="fcfdb-133">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Set-AzureRmApplicationGatewayRequestRoutingRule.md)


