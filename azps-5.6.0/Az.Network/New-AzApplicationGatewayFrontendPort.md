---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3C046A0A-A2B6-413C-8D3B-8991A1FC4926
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: bcc7335076a0f74c89cede8c6fed66f55d88ec9d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953946"
---
# <span data-ttu-id="380aa-101">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="380aa-101">New-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="380aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="380aa-102">SYNOPSIS</span></span>
<span data-ttu-id="380aa-103">Tworzy port frontoronowy dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="380aa-103">Creates a front-end port for an application gateway.</span></span>

## <span data-ttu-id="380aa-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="380aa-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFrontendPort -Name <String> -Port <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="380aa-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="380aa-105">DESCRIPTION</span></span>
<span data-ttu-id="380aa-106">Polecenie **cmdlet New-AzApplicationGatewayFrontendPort** tworzy port front end dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="380aa-106">The **New-AzApplicationGatewayFrontendPort** cmdlet creates a front-end port for an Azure application gateway.</span></span>

## <span data-ttu-id="380aa-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="380aa-107">EXAMPLES</span></span>

### <span data-ttu-id="380aa-108">Przykład 1. Przykład1. Tworzenie portu frontoronu</span><span class="sxs-lookup"><span data-stu-id="380aa-108">Example 1: Example1: Create a front-end port</span></span>
```powershell
PS C:\>$FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="380aa-109">To polecenie tworzy port frontonu o nazwie FrontEndPort01 na porcie 80 i zapisuje wynik w zmiennej o nazwie $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="380aa-109">This command creates a front-end port named FrontEndPort01 on port 80 and stores the result in the variable named $FrontEndPort.</span></span>

## <span data-ttu-id="380aa-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="380aa-110">PARAMETERS</span></span>

### <span data-ttu-id="380aa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="380aa-111">-DefaultProfile</span></span>
<span data-ttu-id="380aa-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="380aa-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="380aa-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="380aa-113">-Name</span></span>
<span data-ttu-id="380aa-114">Określa nazwę portu frontoronu, który tworzy to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="380aa-114">Specifies the name of the front-end port that this cmdlet creates.</span></span>

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

### <span data-ttu-id="380aa-115">— Port</span><span class="sxs-lookup"><span data-stu-id="380aa-115">-Port</span></span>
<span data-ttu-id="380aa-116">Określa numer portu frontoronu.</span><span class="sxs-lookup"><span data-stu-id="380aa-116">Specifies the port number of the front-end port.</span></span>

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

### <span data-ttu-id="380aa-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="380aa-117">CommonParameters</span></span>
<span data-ttu-id="380aa-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="380aa-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="380aa-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="380aa-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="380aa-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="380aa-120">INPUTS</span></span>

### <span data-ttu-id="380aa-121">Brak</span><span class="sxs-lookup"><span data-stu-id="380aa-121">None</span></span>

## <span data-ttu-id="380aa-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="380aa-122">OUTPUTS</span></span>

### <span data-ttu-id="380aa-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="380aa-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="380aa-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="380aa-124">NOTES</span></span>

## <span data-ttu-id="380aa-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="380aa-125">RELATED LINKS</span></span>

[<span data-ttu-id="380aa-126">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="380aa-126">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="380aa-127">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="380aa-127">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="380aa-128">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="380aa-128">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="380aa-129">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="380aa-129">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


