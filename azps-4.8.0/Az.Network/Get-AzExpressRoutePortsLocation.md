---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportslocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
ms.openlocfilehash: 918ef18717cb09bad28ee10b91f635181dd5b3cb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223117"
---
# <span data-ttu-id="88670-101">Get-AzExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="88670-101">Get-AzExpressRoutePortsLocation</span></span>

## <span data-ttu-id="88670-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="88670-102">SYNOPSIS</span></span>
<span data-ttu-id="88670-103">Pobiera lokalizacje, w których ExpressRoutePort są dostępne zasoby.</span><span class="sxs-lookup"><span data-stu-id="88670-103">Gets the locations at which ExpressRoutePort resources are available.</span></span>

## <span data-ttu-id="88670-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="88670-104">SYNTAX</span></span>

```
Get-AzExpressRoutePortsLocation [-LocationName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="88670-105">Opis</span><span class="sxs-lookup"><span data-stu-id="88670-105">DESCRIPTION</span></span>
<span data-ttu-id="88670-106">Polecenie cmdlet **Get-AzExpressRoutePortsLocation** służy do pobierania lokalizacji, w których zasoby ExpressRoutePort są dostępne.</span><span class="sxs-lookup"><span data-stu-id="88670-106">The **Get-AzExpressRoutePortsLocation** cmdlet is used to retrieve the locations at which ExpressRoutePort resources are available.</span></span> <span data-ttu-id="88670-107">W przypadku konkretnych lokalizacji jako danych wejściowych polecenie cmdlet wyświetla szczegóły tej lokalizacji, czyli listę dostępnych przepustowości w tej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="88670-107">Given a specific location as input, the cmdlet displays the details of that location i.e., list of available bandwidths at that location.</span></span>

## <span data-ttu-id="88670-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="88670-108">EXAMPLES</span></span>

### <span data-ttu-id="88670-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="88670-109">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortsLocation
```

<span data-ttu-id="88670-110">Wyświetla listę lokalizacji, w których ExpressRoutePort są dostępne zasoby.</span><span class="sxs-lookup"><span data-stu-id="88670-110">Lists the locations at which ExpressRoutePort resources are available.</span></span>

### <span data-ttu-id="88670-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="88670-111">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortsLocation -LocationName $loc
```

<span data-ttu-id="88670-112">Wyświetla listę dostępnych ExpressRoutePortych przepustowości w lokalizacji $loc.</span><span class="sxs-lookup"><span data-stu-id="88670-112">Lists the ExpressRoutePort bandwidths available at location $loc.</span></span>

## <span data-ttu-id="88670-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="88670-113">PARAMETERS</span></span>

### <span data-ttu-id="88670-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88670-114">-DefaultProfile</span></span>
<span data-ttu-id="88670-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="88670-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88670-116">-LocationName</span><span class="sxs-lookup"><span data-stu-id="88670-116">-LocationName</span></span>
<span data-ttu-id="88670-117">Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="88670-117">The name of the location.</span></span>

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

### <span data-ttu-id="88670-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88670-118">CommonParameters</span></span>
<span data-ttu-id="88670-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88670-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88670-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88670-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88670-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="88670-121">INPUTS</span></span>

### <span data-ttu-id="88670-122">System. String</span><span class="sxs-lookup"><span data-stu-id="88670-122">System.String</span></span>

## <span data-ttu-id="88670-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="88670-123">OUTPUTS</span></span>

### <span data-ttu-id="88670-124">Microsoft. Azure. Commands. Network. models. PSExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="88670-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePortsLocation</span></span>

## <span data-ttu-id="88670-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="88670-125">NOTES</span></span>

## <span data-ttu-id="88670-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="88670-126">RELATED LINKS</span></span>
