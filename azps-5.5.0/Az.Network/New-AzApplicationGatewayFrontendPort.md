---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3C046A0A-A2B6-413C-8D3B-8991A1FC4926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: dc5a0fb99ca3ce41447cc95ebb42490b88379f83
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202942"
---
# <span data-ttu-id="06daa-101">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="06daa-101">New-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="06daa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06daa-102">SYNOPSIS</span></span>
<span data-ttu-id="06daa-103">Tworzy port frontoronowy dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="06daa-103">Creates a front-end port for an application gateway.</span></span>

## <span data-ttu-id="06daa-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="06daa-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFrontendPort -Name <String> -Port <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="06daa-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="06daa-105">DESCRIPTION</span></span>
<span data-ttu-id="06daa-106">Polecenie **cmdlet New-AzApplicationGatewayFrontendPort** tworzy port front end dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="06daa-106">The **New-AzApplicationGatewayFrontendPort** cmdlet creates a front-end port for an Azure application gateway.</span></span>

## <span data-ttu-id="06daa-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="06daa-107">EXAMPLES</span></span>

### <span data-ttu-id="06daa-108">Przykład 1. Przykład1. Tworzenie portu frontoronu</span><span class="sxs-lookup"><span data-stu-id="06daa-108">Example 1: Example1: Create a front-end port</span></span>
```powershell
PS C:\>$FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="06daa-109">To polecenie tworzy port frontonu o nazwie FrontEndPort01 na porcie 80 i zapisuje wynik w zmiennej o nazwie $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="06daa-109">This command creates a front-end port named FrontEndPort01 on port 80 and stores the result in the variable named $FrontEndPort.</span></span>

## <span data-ttu-id="06daa-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06daa-110">PARAMETERS</span></span>

### <span data-ttu-id="06daa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06daa-111">-DefaultProfile</span></span>
<span data-ttu-id="06daa-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="06daa-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06daa-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="06daa-113">-Name</span></span>
<span data-ttu-id="06daa-114">Określa nazwę portu frontoronu, który tworzy to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06daa-114">Specifies the name of the front-end port that this cmdlet creates.</span></span>

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

### <span data-ttu-id="06daa-115">— Port</span><span class="sxs-lookup"><span data-stu-id="06daa-115">-Port</span></span>
<span data-ttu-id="06daa-116">Określa numer portu frontoronu.</span><span class="sxs-lookup"><span data-stu-id="06daa-116">Specifies the port number of the front-end port.</span></span>

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

### <span data-ttu-id="06daa-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06daa-117">CommonParameters</span></span>
<span data-ttu-id="06daa-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06daa-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06daa-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06daa-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06daa-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="06daa-120">INPUTS</span></span>

### <span data-ttu-id="06daa-121">Brak</span><span class="sxs-lookup"><span data-stu-id="06daa-121">None</span></span>

## <span data-ttu-id="06daa-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="06daa-122">OUTPUTS</span></span>

### <span data-ttu-id="06daa-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="06daa-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="06daa-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="06daa-124">NOTES</span></span>

## <span data-ttu-id="06daa-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="06daa-125">RELATED LINKS</span></span>

[<span data-ttu-id="06daa-126">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="06daa-126">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="06daa-127">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="06daa-127">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="06daa-128">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="06daa-128">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="06daa-129">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="06daa-129">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


