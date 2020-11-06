---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 77CDEE77-FD5D-4C2D-B027-FF1F6FF6618E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGateway.md
ms.openlocfilehash: e8a395306c7df773792390c71aa7a8b9d894f77b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546495"
---
# <span data-ttu-id="df1f2-101">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="df1f2-101">Get-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="df1f2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="df1f2-102">SYNOPSIS</span></span>
<span data-ttu-id="df1f2-103">Pobiera bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="df1f2-103">Gets an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df1f2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="df1f2-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGateway [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df1f2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="df1f2-105">DESCRIPTION</span></span>
<span data-ttu-id="df1f2-106">Polecenie cmdlet **Get-AzureRmApplicationGateway** pobiera bramę Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="df1f2-106">The **Get-AzureRmApplicationGateway** cmdlet gets an application gateway.</span></span>

## <span data-ttu-id="df1f2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="df1f2-107">EXAMPLES</span></span>

### <span data-ttu-id="df1f2-108">Przykład 1: uzyskiwanie określonej bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="df1f2-108">Example 1: Get a specified application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="df1f2-109">To polecenie pobiera bramkę Application Gateway o nazwie ApplicationGateway01 należącej do grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="df1f2-109">This command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

### <span data-ttu-id="df1f2-110">Przykład 2: uzyskiwanie listy bram aplikacji w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="df1f2-110">Example 2: Get a list of application gateways in a resource group</span></span>
```
PS C:\>$AppGwList = Get-AzureRmApplicationGateway -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="df1f2-111">To polecenie powoduje wyświetlenie listy wszystkich bram aplikacji w grupie zasób o nazwie ResourceGroup01 i zapisanie jej w zmiennej $AppGwList.</span><span class="sxs-lookup"><span data-stu-id="df1f2-111">This command gets a list of all the application gateways in the resource group named ResourceGroup01 and stores it in the $AppGwList variable.</span></span>

### <span data-ttu-id="df1f2-112">Przykład 3: uzyskiwanie listy bram aplikacji w subskrypcji</span><span class="sxs-lookup"><span data-stu-id="df1f2-112">Example 3: Get a list of application gateways in a subscription</span></span>
```
PS C:\>$AppGwList = Get-AzureRmApplicationGateway
```

<span data-ttu-id="df1f2-113">To polecenie powoduje wyświetlenie listy wszystkich bram aplikacji w subskrypcji i zapisanie jej w zmiennej $AppGwList.</span><span class="sxs-lookup"><span data-stu-id="df1f2-113">This command gets a list of all the application gateways in the subscription and stores it in the $AppGwList variable.</span></span>

## <span data-ttu-id="df1f2-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="df1f2-114">PARAMETERS</span></span>

### <span data-ttu-id="df1f2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df1f2-115">-DefaultProfile</span></span>
<span data-ttu-id="df1f2-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="df1f2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df1f2-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="df1f2-117">-Name</span></span>
<span data-ttu-id="df1f2-118">Określa nazwę bramy aplikacji, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df1f2-118">Specifies the name of the application gateway that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df1f2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df1f2-119">-ResourceGroupName</span></span>
<span data-ttu-id="df1f2-120">Określa nazwę grupy zasobów zawierającej bramkę Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="df1f2-120">Specifies the name of the resource group that contains the application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df1f2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df1f2-121">CommonParameters</span></span>
<span data-ttu-id="df1f2-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df1f2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df1f2-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df1f2-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df1f2-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="df1f2-124">INPUTS</span></span>

### <span data-ttu-id="df1f2-125">System. String</span><span class="sxs-lookup"><span data-stu-id="df1f2-125">System.String</span></span>

## <span data-ttu-id="df1f2-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="df1f2-126">OUTPUTS</span></span>

### <span data-ttu-id="df1f2-127">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="df1f2-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="df1f2-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="df1f2-128">NOTES</span></span>

## <span data-ttu-id="df1f2-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="df1f2-129">RELATED LINKS</span></span>

[<span data-ttu-id="df1f2-130">Zatrzymaj — AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="df1f2-130">Stop-AzureRmApplicationGateway</span></span>](./Stop-AzureRmApplicationGateway.md)


