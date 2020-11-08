---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalrusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
ms.openlocfilehash: 91910bc8a8c5135672e311bd1bb1c6367ccd14f3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049753"
---
# <span data-ttu-id="41585-101">Get-AzSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="41585-101">Get-AzSignalRUsage</span></span>

## <span data-ttu-id="41585-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="41585-102">SYNOPSIS</span></span>
<span data-ttu-id="41585-103">Uzyskaj przydział użycia subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="41585-103">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="41585-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="41585-104">SYNTAX</span></span>

```
Get-AzSignalRUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41585-105">Opis</span><span class="sxs-lookup"><span data-stu-id="41585-105">DESCRIPTION</span></span>
<span data-ttu-id="41585-106">Uzyskaj przydział użycia subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="41585-106">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="41585-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="41585-107">EXAMPLES</span></span>

### <span data-ttu-id="41585-108">Uzyskiwanie przydziału użycia przez umieszczenie lokalizacji</span><span class="sxs-lookup"><span data-stu-id="41585-108">Get the usage quota by inputting the location</span></span>
```powershell
PS C:\> Get-AzSignalRUsage eastus

Name                 CurrentValue Limit
----                 ------------ -----
FreeTierInstances    2            5
SignalRTotalUnits    3            300
```

## <span data-ttu-id="41585-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="41585-109">PARAMETERS</span></span>

### <span data-ttu-id="41585-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41585-110">-DefaultProfile</span></span>
<span data-ttu-id="41585-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="41585-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41585-112">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="41585-112">-Location</span></span>
<span data-ttu-id="41585-113">Lokalizacja usługi sygnalizacji.</span><span class="sxs-lookup"><span data-stu-id="41585-113">The SignalR service location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41585-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41585-114">CommonParameters</span></span>
<span data-ttu-id="41585-115">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41585-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41585-116">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="41585-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41585-117">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="41585-117">INPUTS</span></span>

### <span data-ttu-id="41585-118">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="41585-118">None</span></span>

## <span data-ttu-id="41585-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="41585-119">OUTPUTS</span></span>

### <span data-ttu-id="41585-120">Microsoft. Azure. Commands. Signals. modele. PSSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="41585-120">Microsoft.Azure.Commands.SignalR.Models.PSSignalRUsage</span></span>

## <span data-ttu-id="41585-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="41585-121">NOTES</span></span>

## <span data-ttu-id="41585-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="41585-122">RELATED LINKS</span></span>
