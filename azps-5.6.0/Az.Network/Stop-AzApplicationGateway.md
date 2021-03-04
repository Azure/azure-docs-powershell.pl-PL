---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C9609E8-0D8B-471B-9F0E-672BF55C3A0E
online version: https://docs.microsoft.com/powershell/module/az.network/stop-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzApplicationGateway.md
ms.openlocfilehash: 0cf179bf02c8590bd5c5e30277c7299c7b13b06b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951866"
---
# <span data-ttu-id="d6f4b-101">Stop-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d6f4b-101">Stop-AzApplicationGateway</span></span>

## <span data-ttu-id="d6f4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6f4b-102">SYNOPSIS</span></span>
<span data-ttu-id="d6f4b-103">Zatrzymuje bramę aplikacji</span><span class="sxs-lookup"><span data-stu-id="d6f4b-103">Stops an application gateway</span></span>

## <span data-ttu-id="d6f4b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d6f4b-104">SYNTAX</span></span>

```
Stop-AzApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6f4b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d6f4b-105">DESCRIPTION</span></span>
<span data-ttu-id="d6f4b-106">Polecenie **cmdlet Stop-AzApplicationGateway** zatrzymuje bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d6f4b-106">The **Stop-AzApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="d6f4b-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d6f4b-107">EXAMPLES</span></span>

### <span data-ttu-id="d6f4b-108">Przykład 1. Zatrzymywanie bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="d6f4b-108">Example 1: Stop an application gateway</span></span>
```
PS C:\>Stop-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="d6f4b-109">To polecenie zatrzymuje bramę aplikacji przechowywaną w $AppGw zmienną.</span><span class="sxs-lookup"><span data-stu-id="d6f4b-109">This command stops the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="d6f4b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d6f4b-110">PARAMETERS</span></span>

### <span data-ttu-id="d6f4b-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d6f4b-111">-ApplicationGateway</span></span>
<span data-ttu-id="d6f4b-112">Określa bramę aplikacji, która ma być zatrzymana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6f4b-112">Specifies the application gateway that this cmdlet stops.</span></span>

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

### <span data-ttu-id="d6f4b-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="d6f4b-113">-AsJob</span></span>
<span data-ttu-id="d6f4b-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d6f4b-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6f4b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6f4b-115">-DefaultProfile</span></span>
<span data-ttu-id="d6f4b-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d6f4b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6f4b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6f4b-117">CommonParameters</span></span>
<span data-ttu-id="d6f4b-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6f4b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6f4b-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6f4b-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6f4b-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d6f4b-120">INPUTS</span></span>

### <span data-ttu-id="d6f4b-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d6f4b-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d6f4b-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d6f4b-122">OUTPUTS</span></span>

### <span data-ttu-id="d6f4b-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d6f4b-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d6f4b-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d6f4b-124">NOTES</span></span>

## <span data-ttu-id="d6f4b-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d6f4b-125">RELATED LINKS</span></span>

[<span data-ttu-id="d6f4b-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d6f4b-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="d6f4b-127">New-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d6f4b-127">New-AzApplicationGateway</span></span>](./New-AzApplicationGateway.md)

[<span data-ttu-id="d6f4b-128">Remove-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d6f4b-128">Remove-AzApplicationGateway</span></span>](./Remove-AzApplicationGateway.md)

[<span data-ttu-id="d6f4b-129">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d6f4b-129">Set-AzApplicationGateway</span></span>](./Set-AzApplicationGateway.md)

[<span data-ttu-id="d6f4b-130">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d6f4b-130">Start-AzApplicationGateway</span></span>](./Start-AzApplicationGateway.md)


