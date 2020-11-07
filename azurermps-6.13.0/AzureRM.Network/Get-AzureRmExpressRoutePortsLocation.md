---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressrouteportslocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePortsLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePortsLocation.md
ms.openlocfilehash: 5d077991e42da0709019df1dccdd83f03659ca49
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719092"
---
# <span data-ttu-id="f1f40-101">Get-AzureRmExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="f1f40-101">Get-AzureRmExpressRoutePortsLocation</span></span>

## <span data-ttu-id="f1f40-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f1f40-102">SYNOPSIS</span></span>
<span data-ttu-id="f1f40-103">Pobiera lokalizacje, w których ExpressRoutePort są dostępne zasoby.</span><span class="sxs-lookup"><span data-stu-id="f1f40-103">Gets the locations at which ExpressRoutePort resources are available.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1f40-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f1f40-104">SYNTAX</span></span>

```
Get-AzureRmExpressRoutePortsLocation [-LocationName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f1f40-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f1f40-105">DESCRIPTION</span></span>
<span data-ttu-id="f1f40-106">Polecenie cmdlet **Get-AzureRmExpressRoutePortsLocation** służy do pobierania lokalizacji, w których zasoby ExpressRoutePort są dostępne.</span><span class="sxs-lookup"><span data-stu-id="f1f40-106">The **Get-AzureRmExpressRoutePortsLocation** cmdlet is used to retrieve the locations at which ExpressRoutePort resources are available.</span></span> <span data-ttu-id="f1f40-107">W przypadku konkretnych lokalizacji jako danych wejściowych polecenie cmdlet wyświetla szczegóły tej lokalizacji, czyli listę dostępnych przepustowości w tej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="f1f40-107">Given a specific location as input, the cmdlet displays the details of that location i.e., list of available bandwidths at that location.</span></span>


## <span data-ttu-id="f1f40-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f1f40-108">EXAMPLES</span></span>

### <span data-ttu-id="f1f40-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f1f40-109">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmExpressRoutePortsLocation
```

<span data-ttu-id="f1f40-110">Wyświetla listę lokalizacji, w których ExpressRoutePort są dostępne zasoby.</span><span class="sxs-lookup"><span data-stu-id="f1f40-110">Lists the locations at which ExpressRoutePort resources are available.</span></span>

### <span data-ttu-id="f1f40-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f1f40-111">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmExpressRoutePortsLocation -LocationName $loc
```

<span data-ttu-id="f1f40-112">Wyświetla listę dostępnych ExpressRoutePortych przepustowości w lokalizacji $loc.</span><span class="sxs-lookup"><span data-stu-id="f1f40-112">Lists the ExpressRoutePort bandwidths available at location $loc.</span></span>

## <span data-ttu-id="f1f40-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f1f40-113">PARAMETERS</span></span>

### <span data-ttu-id="f1f40-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1f40-114">-DefaultProfile</span></span>
<span data-ttu-id="f1f40-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f1f40-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1f40-116">-LocationName</span><span class="sxs-lookup"><span data-stu-id="f1f40-116">-LocationName</span></span>
<span data-ttu-id="f1f40-117">Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="f1f40-117">The name of the location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1f40-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1f40-118">CommonParameters</span></span>
<span data-ttu-id="f1f40-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1f40-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1f40-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1f40-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1f40-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f1f40-121">INPUTS</span></span>

### <span data-ttu-id="f1f40-122">System. String</span><span class="sxs-lookup"><span data-stu-id="f1f40-122">System.String</span></span>

## <span data-ttu-id="f1f40-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f1f40-123">OUTPUTS</span></span>

### <span data-ttu-id="f1f40-124">Microsoft. Azure. Commands. Network. models. PSExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="f1f40-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePortsLocation</span></span>

## <span data-ttu-id="f1f40-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f1f40-125">NOTES</span></span>

## <span data-ttu-id="f1f40-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f1f40-126">RELATED LINKS</span></span>
