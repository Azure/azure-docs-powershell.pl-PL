---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 77CDEE77-FD5D-4C2D-B027-FF1F6FF6618E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgateway
schema: 2.0.0
ms.openlocfilehash: 2b6373944f8b7bbc741557629fad7c9f717e979e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899300"
---
# <span data-ttu-id="7ed54-101">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7ed54-101">Get-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="7ed54-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7ed54-102">SYNOPSIS</span></span>
<span data-ttu-id="7ed54-103">Pobiera bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="7ed54-103">Gets an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ed54-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7ed54-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGateway [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ed54-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7ed54-105">DESCRIPTION</span></span>
<span data-ttu-id="7ed54-106">Polecenie cmdlet **Get-AzureRmApplicationGateway** pobiera bramę Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="7ed54-106">The **Get-AzureRmApplicationGateway** cmdlet gets an application gateway.</span></span>

## <span data-ttu-id="7ed54-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7ed54-107">EXAMPLES</span></span>

### <span data-ttu-id="7ed54-108">Przykład 1: uzyskiwanie określonej bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="7ed54-108">Example 1: Get a specified application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="7ed54-109">To polecenie pobiera bramkę Application Gateway o nazwie ApplicationGateway01 należącej do grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="7ed54-109">This command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

### <span data-ttu-id="7ed54-110">Przykład 2: uzyskiwanie listy bram aplikacji w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="7ed54-110">Example 2: Get a list of application gateways in a resource group</span></span>
```
PS C:\>$AppGwList = Get-AzureRmApplicationGateway -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="7ed54-111">To polecenie powoduje wyświetlenie listy wszystkich bram aplikacji w grupie zasób o nazwie ResourceGroup01 i zapisanie jej w zmiennej $AppGwList.</span><span class="sxs-lookup"><span data-stu-id="7ed54-111">This command gets a list of all the application gateways in the resource group named ResourceGroup01 and stores it in the $AppGwList variable.</span></span>

### <span data-ttu-id="7ed54-112">Przykład 3: uzyskiwanie listy bram aplikacji w subskrypcji</span><span class="sxs-lookup"><span data-stu-id="7ed54-112">Example 3: Get a list of application gateways in a subscription</span></span>
```
PS C:\>$AppGwList = Get-AzureRmApplicationGateway
```

<span data-ttu-id="7ed54-113">To polecenie powoduje wyświetlenie listy wszystkich bram aplikacji w subskrypcji i zapisanie jej w zmiennej $AppGwList.</span><span class="sxs-lookup"><span data-stu-id="7ed54-113">This command gets a list of all the application gateways in the subscription and stores it in the $AppGwList variable.</span></span>

## <span data-ttu-id="7ed54-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7ed54-114">PARAMETERS</span></span>

### <span data-ttu-id="7ed54-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ed54-115">-DefaultProfile</span></span>
<span data-ttu-id="7ed54-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7ed54-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ed54-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7ed54-117">-Name</span></span>
<span data-ttu-id="7ed54-118">Określa nazwę bramy aplikacji, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ed54-118">Specifies the name of the application gateway that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ed54-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ed54-119">-ResourceGroupName</span></span>
<span data-ttu-id="7ed54-120">Określa nazwę grupy zasobów zawierającej bramkę Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="7ed54-120">Specifies the name of the resource group that contains the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ed54-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ed54-121">CommonParameters</span></span>
<span data-ttu-id="7ed54-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ed54-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ed54-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ed54-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ed54-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7ed54-124">INPUTS</span></span>

### <span data-ttu-id="7ed54-125">System. String</span><span class="sxs-lookup"><span data-stu-id="7ed54-125">System.String</span></span>

## <span data-ttu-id="7ed54-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7ed54-126">OUTPUTS</span></span>

### <span data-ttu-id="7ed54-127">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7ed54-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7ed54-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7ed54-128">NOTES</span></span>

## <span data-ttu-id="7ed54-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7ed54-129">RELATED LINKS</span></span>

[<span data-ttu-id="7ed54-130">Zatrzymaj — AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7ed54-130">Stop-AzureRmApplicationGateway</span></span>](./Stop-AzureRmApplicationGateway.md)


