---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailablessloption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
ms.openlocfilehash: f2175583aaaf3af04120e22e32db79d7b20f1e30
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189882"
---
# <span data-ttu-id="09b95-101">Get-AzApplicationGatewayAvailableSslOption</span><span class="sxs-lookup"><span data-stu-id="09b95-101">Get-AzApplicationGatewayAvailableSslOption</span></span>

## <span data-ttu-id="09b95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09b95-102">SYNOPSIS</span></span>
<span data-ttu-id="09b95-103">Pobiera wszystkie dostępne opcje ssl dla zasad SSL dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="09b95-103">Gets all available ssl options for ssl policy for Application Gateway.</span></span>

## <span data-ttu-id="09b95-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="09b95-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableSslOption [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09b95-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="09b95-105">DESCRIPTION</span></span>
<span data-ttu-id="09b95-106">Polecenie **cmdlet Get-AzApplicationGatewayAvailableSslOption** pobiera wszystkie dostępne opcje ssl dla zasad ssl</span><span class="sxs-lookup"><span data-stu-id="09b95-106">The **Get-AzApplicationGatewayAvailableSslOption** cmdlet gets all available ssl options for ssl policy</span></span>

## <span data-ttu-id="09b95-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="09b95-107">EXAMPLES</span></span>

### <span data-ttu-id="09b95-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="09b95-108">Example 1</span></span>
```
PS C:\>$sslOptions = Get-AzApplicationGatewayAvailableSslOption
```

<span data-ttu-id="09b95-109">Te polecenia zwracają wszystkie dostępne opcje ssl dla zasad ssl.</span><span class="sxs-lookup"><span data-stu-id="09b95-109">This commands returns all available ssl options for ssl policy.</span></span>

## <span data-ttu-id="09b95-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="09b95-110">PARAMETERS</span></span>

### <span data-ttu-id="09b95-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09b95-111">-DefaultProfile</span></span>
<span data-ttu-id="09b95-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="09b95-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09b95-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09b95-113">CommonParameters</span></span>
<span data-ttu-id="09b95-114">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09b95-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09b95-115">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="09b95-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09b95-116">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="09b95-116">INPUTS</span></span>

### <span data-ttu-id="09b95-117">Brak</span><span class="sxs-lookup"><span data-stu-id="09b95-117">None</span></span>

## <span data-ttu-id="09b95-118">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="09b95-118">OUTPUTS</span></span>

### <span data-ttu-id="09b95-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="09b95-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="09b95-120">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="09b95-120">NOTES</span></span>

## <span data-ttu-id="09b95-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="09b95-121">RELATED LINKS</span></span>
