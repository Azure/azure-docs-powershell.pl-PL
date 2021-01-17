---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3C046A0A-A2B6-413C-8D3B-8991A1FC4926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: dc5a0fb99ca3ce41447cc95ebb42490b88379f83
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385553"
---
# <span data-ttu-id="21e67-101">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="21e67-101">New-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="21e67-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="21e67-102">SYNOPSIS</span></span>
<span data-ttu-id="21e67-103">Tworzy port frontonu dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="21e67-103">Creates a front-end port for an application gateway.</span></span>

## <span data-ttu-id="21e67-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="21e67-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFrontendPort -Name <String> -Port <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="21e67-105">Opis</span><span class="sxs-lookup"><span data-stu-id="21e67-105">DESCRIPTION</span></span>
<span data-ttu-id="21e67-106">Polecenie cmdlet **New-AzApplicationGatewayFrontendPort** tworzy port frontonu dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="21e67-106">The **New-AzApplicationGatewayFrontendPort** cmdlet creates a front-end port for an Azure application gateway.</span></span>

## <span data-ttu-id="21e67-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="21e67-107">EXAMPLES</span></span>

### <span data-ttu-id="21e67-108">Przykład 1: example1: Tworzenie portu frontonu</span><span class="sxs-lookup"><span data-stu-id="21e67-108">Example 1: Example1: Create a front-end port</span></span>
```powershell
PS C:\>$FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="21e67-109">To polecenie tworzy port frontonu o nazwie FrontEndPort01 na porcie 80 i zapisuje wynik w zmiennej o nazwie $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="21e67-109">This command creates a front-end port named FrontEndPort01 on port 80 and stores the result in the variable named $FrontEndPort.</span></span>

## <span data-ttu-id="21e67-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="21e67-110">PARAMETERS</span></span>

### <span data-ttu-id="21e67-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21e67-111">-DefaultProfile</span></span>
<span data-ttu-id="21e67-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="21e67-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21e67-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="21e67-113">-Name</span></span>
<span data-ttu-id="21e67-114">Określa nazwę portu frontonu tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21e67-114">Specifies the name of the front-end port that this cmdlet creates.</span></span>

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

### <span data-ttu-id="21e67-115">-Port</span><span class="sxs-lookup"><span data-stu-id="21e67-115">-Port</span></span>
<span data-ttu-id="21e67-116">Określa numer portu na porcie frontonu.</span><span class="sxs-lookup"><span data-stu-id="21e67-116">Specifies the port number of the front-end port.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21e67-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21e67-117">CommonParameters</span></span>
<span data-ttu-id="21e67-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21e67-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21e67-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21e67-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21e67-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="21e67-120">INPUTS</span></span>

### <span data-ttu-id="21e67-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="21e67-121">None</span></span>

## <span data-ttu-id="21e67-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="21e67-122">OUTPUTS</span></span>

### <span data-ttu-id="21e67-123">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="21e67-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="21e67-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="21e67-124">NOTES</span></span>

## <span data-ttu-id="21e67-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="21e67-125">RELATED LINKS</span></span>

[<span data-ttu-id="21e67-126">Dodaj-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="21e67-126">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="21e67-127">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="21e67-127">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="21e67-128">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="21e67-128">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="21e67-129">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="21e67-129">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


