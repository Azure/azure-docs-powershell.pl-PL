---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3C046A0A-A2B6-413C-8D3B-8991A1FC4926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: ddfe8b1736ef6c037522815dc81019fadc5b6c1f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890569"
---
# <span data-ttu-id="f0d06-101">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="f0d06-101">New-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="f0d06-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f0d06-102">SYNOPSIS</span></span>
<span data-ttu-id="f0d06-103">Tworzy port frontonu dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f0d06-103">Creates a front-end port for an application gateway.</span></span>

## <span data-ttu-id="f0d06-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f0d06-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFrontendPort -Name <String> -Port <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0d06-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f0d06-105">DESCRIPTION</span></span>
<span data-ttu-id="f0d06-106">Polecenie cmdlet **New-AzApplicationGatewayFrontendPort** tworzy port frontonu dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f0d06-106">The **New-AzApplicationGatewayFrontendPort** cmdlet creates a front-end port for an Azure application gateway.</span></span>

## <span data-ttu-id="f0d06-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f0d06-107">EXAMPLES</span></span>

### <span data-ttu-id="f0d06-108">Example1: Tworzenie portu frontonu</span><span class="sxs-lookup"><span data-stu-id="f0d06-108">Example1: Create a front-end port</span></span>
```
PS C:\>$FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="f0d06-109">To polecenie tworzy port frontonu o nazwie FrontEndPort01 na porcie 80 i zapisuje wynik w zmiennej o nazwie $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="f0d06-109">This command creates a front-end port named FrontEndPort01 on port 80 and stores the result in the variable named $FrontEndPort.</span></span>

## <span data-ttu-id="f0d06-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f0d06-110">PARAMETERS</span></span>

### <span data-ttu-id="f0d06-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0d06-111">-DefaultProfile</span></span>
<span data-ttu-id="f0d06-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f0d06-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0d06-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f0d06-113">-Name</span></span>
<span data-ttu-id="f0d06-114">Określa nazwę portu frontonu tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0d06-114">Specifies the name of the front-end port that this cmdlet creates.</span></span>

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

### <span data-ttu-id="f0d06-115">-Port</span><span class="sxs-lookup"><span data-stu-id="f0d06-115">-Port</span></span>
<span data-ttu-id="f0d06-116">Określa numer portu na porcie frontonu.</span><span class="sxs-lookup"><span data-stu-id="f0d06-116">Specifies the port number of the front-end port.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0d06-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0d06-117">CommonParameters</span></span>
<span data-ttu-id="f0d06-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0d06-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0d06-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0d06-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0d06-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f0d06-120">INPUTS</span></span>

### <span data-ttu-id="f0d06-121">System. String</span><span class="sxs-lookup"><span data-stu-id="f0d06-121">System.String</span></span>

## <span data-ttu-id="f0d06-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f0d06-122">OUTPUTS</span></span>

### <span data-ttu-id="f0d06-123">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="f0d06-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="f0d06-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f0d06-124">NOTES</span></span>

## <span data-ttu-id="f0d06-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f0d06-125">RELATED LINKS</span></span>

[<span data-ttu-id="f0d06-126">Dodaj-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="f0d06-126">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="f0d06-127">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="f0d06-127">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="f0d06-128">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="f0d06-128">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="f0d06-129">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="f0d06-129">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


