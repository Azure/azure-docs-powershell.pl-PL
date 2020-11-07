---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportslocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
ms.openlocfilehash: 196cc354ddac7f317400b7baa665b8975dcc9df9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709536"
---
# <span data-ttu-id="82ba0-101">Get-AzExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="82ba0-101">Get-AzExpressRoutePortsLocation</span></span>

## <span data-ttu-id="82ba0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="82ba0-102">SYNOPSIS</span></span>
<span data-ttu-id="82ba0-103">Pobiera lokalizacje, w których ExpressRoutePort są dostępne zasoby.</span><span class="sxs-lookup"><span data-stu-id="82ba0-103">Gets the locations at which ExpressRoutePort resources are available.</span></span>

## <span data-ttu-id="82ba0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="82ba0-104">SYNTAX</span></span>

```
Get-AzExpressRoutePortsLocation [-LocationName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="82ba0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="82ba0-105">DESCRIPTION</span></span>
<span data-ttu-id="82ba0-106">Polecenie cmdlet **Get-AzExpressRoutePortsLocation** służy do pobierania lokalizacji, w których zasoby ExpressRoutePort są dostępne.</span><span class="sxs-lookup"><span data-stu-id="82ba0-106">The **Get-AzExpressRoutePortsLocation** cmdlet is used to retrieve the locations at which ExpressRoutePort resources are available.</span></span> <span data-ttu-id="82ba0-107">W przypadku konkretnych lokalizacji jako danych wejściowych polecenie cmdlet wyświetla szczegóły tej lokalizacji, czyli listę dostępnych przepustowości w tej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="82ba0-107">Given a specific location as input, the cmdlet displays the details of that location i.e., list of available bandwidths at that location.</span></span>

## <span data-ttu-id="82ba0-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="82ba0-108">EXAMPLES</span></span>

### <span data-ttu-id="82ba0-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="82ba0-109">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortsLocation
```

<span data-ttu-id="82ba0-110">Wyświetla listę lokalizacji, w których ExpressRoutePort są dostępne zasoby.</span><span class="sxs-lookup"><span data-stu-id="82ba0-110">Lists the locations at which ExpressRoutePort resources are available.</span></span>

### <span data-ttu-id="82ba0-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="82ba0-111">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortsLocation -LocationName $loc
```

<span data-ttu-id="82ba0-112">Wyświetla listę dostępnych ExpressRoutePortych przepustowości w lokalizacji $loc.</span><span class="sxs-lookup"><span data-stu-id="82ba0-112">Lists the ExpressRoutePort bandwidths available at location $loc.</span></span>

## <span data-ttu-id="82ba0-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="82ba0-113">PARAMETERS</span></span>

### <span data-ttu-id="82ba0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82ba0-114">-DefaultProfile</span></span>
<span data-ttu-id="82ba0-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="82ba0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82ba0-116">-LocationName</span><span class="sxs-lookup"><span data-stu-id="82ba0-116">-LocationName</span></span>
<span data-ttu-id="82ba0-117">Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="82ba0-117">The name of the location.</span></span>

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

### <span data-ttu-id="82ba0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82ba0-118">CommonParameters</span></span>
<span data-ttu-id="82ba0-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82ba0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82ba0-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="82ba0-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82ba0-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="82ba0-121">INPUTS</span></span>

### <span data-ttu-id="82ba0-122">System. String</span><span class="sxs-lookup"><span data-stu-id="82ba0-122">System.String</span></span>

## <span data-ttu-id="82ba0-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="82ba0-123">OUTPUTS</span></span>

### <span data-ttu-id="82ba0-124">Microsoft. Azure. Commands. Network. models. PSExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="82ba0-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePortsLocation</span></span>

## <span data-ttu-id="82ba0-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="82ba0-125">NOTES</span></span>

## <span data-ttu-id="82ba0-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="82ba0-126">RELATED LINKS</span></span>