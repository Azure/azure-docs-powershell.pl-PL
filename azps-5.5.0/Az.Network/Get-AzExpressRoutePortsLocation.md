---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportslocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
ms.openlocfilehash: 918ef18717cb09bad28ee10b91f635181dd5b3cb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189786"
---
# <span data-ttu-id="cc364-101">Get-AzExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="cc364-101">Get-AzExpressRoutePortsLocation</span></span>

## <span data-ttu-id="cc364-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc364-102">SYNOPSIS</span></span>
<span data-ttu-id="cc364-103">Pobiera lokalizacje, w których są dostępne zasoby usługi ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="cc364-103">Gets the locations at which ExpressRoutePort resources are available.</span></span>

## <span data-ttu-id="cc364-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cc364-104">SYNTAX</span></span>

```
Get-AzExpressRoutePortsLocation [-LocationName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cc364-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="cc364-105">DESCRIPTION</span></span>
<span data-ttu-id="cc364-106">Polecenie **cmdlet Get-AzExpressRoutePortsLocation** służy do pobierania lokalizacji, w których są dostępne zasoby usługi ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="cc364-106">The **Get-AzExpressRoutePortsLocation** cmdlet is used to retrieve the locations at which ExpressRoutePort resources are available.</span></span> <span data-ttu-id="cc364-107">Gdy jako dane wejściowe jest podana konkletna lokalizacja, polecenie cmdlet wyświetla szczegóły tej lokalizacji, czyli listę dostępnych przepustowości w tej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="cc364-107">Given a specific location as input, the cmdlet displays the details of that location i.e., list of available bandwidths at that location.</span></span>

## <span data-ttu-id="cc364-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cc364-108">EXAMPLES</span></span>

### <span data-ttu-id="cc364-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cc364-109">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortsLocation
```

<span data-ttu-id="cc364-110">Lista lokalizacji, w których są dostępne zasoby usługi ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="cc364-110">Lists the locations at which ExpressRoutePort resources are available.</span></span>

### <span data-ttu-id="cc364-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="cc364-111">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortsLocation -LocationName $loc
```

<span data-ttu-id="cc364-112">Zawiera informacje o przepustowości usługi ExpressRoutePort dostępnej w lokalizacji $loc.</span><span class="sxs-lookup"><span data-stu-id="cc364-112">Lists the ExpressRoutePort bandwidths available at location $loc.</span></span>

## <span data-ttu-id="cc364-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cc364-113">PARAMETERS</span></span>

### <span data-ttu-id="cc364-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc364-114">-DefaultProfile</span></span>
<span data-ttu-id="cc364-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="cc364-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc364-116">-LocationName</span><span class="sxs-lookup"><span data-stu-id="cc364-116">-LocationName</span></span>
<span data-ttu-id="cc364-117">Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="cc364-117">The name of the location.</span></span>

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

### <span data-ttu-id="cc364-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc364-118">CommonParameters</span></span>
<span data-ttu-id="cc364-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc364-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc364-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cc364-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc364-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cc364-121">INPUTS</span></span>

### <span data-ttu-id="cc364-122">System.String</span><span class="sxs-lookup"><span data-stu-id="cc364-122">System.String</span></span>

## <span data-ttu-id="cc364-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cc364-123">OUTPUTS</span></span>

### <span data-ttu-id="cc364-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="cc364-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePortsLocation</span></span>

## <span data-ttu-id="cc364-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cc364-125">NOTES</span></span>

## <span data-ttu-id="cc364-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cc364-126">RELATED LINKS</span></span>
