---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayavailablessloption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
ms.openlocfilehash: 8d2022f79dff5263f07737d525169dad3566fcda
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003642"
---
# <span data-ttu-id="1188e-101">Get-AzApplicationGatewayAvailableSslOption</span><span class="sxs-lookup"><span data-stu-id="1188e-101">Get-AzApplicationGatewayAvailableSslOption</span></span>

## <span data-ttu-id="1188e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1188e-102">SYNOPSIS</span></span>
<span data-ttu-id="1188e-103">Pobiera wszystkie dostępne opcje ssl dla zasad SSL dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1188e-103">Gets all available ssl options for ssl policy for Application Gateway.</span></span>

## <span data-ttu-id="1188e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1188e-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableSslOption [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1188e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="1188e-105">DESCRIPTION</span></span>
<span data-ttu-id="1188e-106">Polecenie **cmdlet Get-AzApplicationGatewayAvailableSslOption** pobiera wszystkie dostępne opcje ssl dla zasad ssl</span><span class="sxs-lookup"><span data-stu-id="1188e-106">The **Get-AzApplicationGatewayAvailableSslOption** cmdlet gets all available ssl options for ssl policy</span></span>

## <span data-ttu-id="1188e-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1188e-107">EXAMPLES</span></span>

### <span data-ttu-id="1188e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1188e-108">Example 1</span></span>
```
PS C:\>$sslOptions = Get-AzApplicationGatewayAvailableSslOption
```

<span data-ttu-id="1188e-109">Te polecenia zwracają wszystkie dostępne opcje ssl dla zasad SSL.</span><span class="sxs-lookup"><span data-stu-id="1188e-109">This commands returns all available ssl options for ssl policy.</span></span>

## <span data-ttu-id="1188e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1188e-110">PARAMETERS</span></span>

### <span data-ttu-id="1188e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1188e-111">-DefaultProfile</span></span>
<span data-ttu-id="1188e-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1188e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1188e-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1188e-113">CommonParameters</span></span>
<span data-ttu-id="1188e-114">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1188e-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1188e-115">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1188e-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1188e-116">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1188e-116">INPUTS</span></span>

### <span data-ttu-id="1188e-117">Brak</span><span class="sxs-lookup"><span data-stu-id="1188e-117">None</span></span>

## <span data-ttu-id="1188e-118">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1188e-118">OUTPUTS</span></span>

### <span data-ttu-id="1188e-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="1188e-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="1188e-120">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1188e-120">NOTES</span></span>

## <span data-ttu-id="1188e-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1188e-121">RELATED LINKS</span></span>
