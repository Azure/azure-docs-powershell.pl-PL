---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Start-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Start-AzApplicationGateway.md
ms.openlocfilehash: 8c37ed72659c8b5ab00d54a7ecbe9622cb9f553b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892689"
---
# <span data-ttu-id="f41c7-101">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f41c7-101">Start-AzApplicationGateway</span></span>

## <span data-ttu-id="f41c7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f41c7-102">SYNOPSIS</span></span>
<span data-ttu-id="f41c7-103">Uruchamia bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f41c7-103">Starts an application gateway.</span></span>

## <span data-ttu-id="f41c7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f41c7-104">SYNTAX</span></span>

```
Start-AzApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f41c7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f41c7-105">DESCRIPTION</span></span>
<span data-ttu-id="f41c7-106">Polecenie cmdlet **Start-AzApplicationGateway** uruchamia bramę aplikacji platformy Azure</span><span class="sxs-lookup"><span data-stu-id="f41c7-106">The **Start-AzApplicationGateway** cmdlet starts an Azure application gateway</span></span>

## <span data-ttu-id="f41c7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f41c7-107">EXAMPLES</span></span>

### <span data-ttu-id="f41c7-108">Example1: uruchamianie bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="f41c7-108">Example1: Start an application gateway</span></span>
```
PS C:\>$AppGw = Start-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="f41c7-109">To polecenie uruchamia bramkę aplikacji przechowywaną w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="f41c7-109">This command starts the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="f41c7-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f41c7-110">PARAMETERS</span></span>

### <span data-ttu-id="f41c7-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f41c7-111">-ApplicationGateway</span></span>
<span data-ttu-id="f41c7-112">Określa bramę aplikacji, która jest uruchamiana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f41c7-112">Specifies the application gateway that this cmdlet starts.</span></span>

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

### <span data-ttu-id="f41c7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f41c7-113">-DefaultProfile</span></span>
<span data-ttu-id="f41c7-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f41c7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f41c7-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f41c7-115">CommonParameters</span></span>
<span data-ttu-id="f41c7-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f41c7-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f41c7-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f41c7-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f41c7-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f41c7-118">INPUTS</span></span>

### <span data-ttu-id="f41c7-119">System. String</span><span class="sxs-lookup"><span data-stu-id="f41c7-119">System.String</span></span>

## <span data-ttu-id="f41c7-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f41c7-120">OUTPUTS</span></span>

### <span data-ttu-id="f41c7-121">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f41c7-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f41c7-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f41c7-122">NOTES</span></span>

## <span data-ttu-id="f41c7-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f41c7-123">RELATED LINKS</span></span>

[<span data-ttu-id="f41c7-124">Zatrzymaj — AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f41c7-124">Stop-AzApplicationGateway</span></span>](./Stop-AzApplicationGateway.md)


