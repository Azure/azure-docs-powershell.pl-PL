---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalrusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
ms.openlocfilehash: 91910bc8a8c5135672e311bd1bb1c6367ccd14f3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499905"
---
# <span data-ttu-id="bb65a-101">Get-AzSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="bb65a-101">Get-AzSignalRUsage</span></span>

## <span data-ttu-id="bb65a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bb65a-102">SYNOPSIS</span></span>
<span data-ttu-id="bb65a-103">Uzyskaj przydział użycia subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="bb65a-103">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="bb65a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bb65a-104">SYNTAX</span></span>

```
Get-AzSignalRUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb65a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bb65a-105">DESCRIPTION</span></span>
<span data-ttu-id="bb65a-106">Uzyskaj przydział użycia subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="bb65a-106">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="bb65a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bb65a-107">EXAMPLES</span></span>

### <span data-ttu-id="bb65a-108">Uzyskiwanie przydziału użycia przez umieszczenie lokalizacji</span><span class="sxs-lookup"><span data-stu-id="bb65a-108">Get the usage quota by inputting the location</span></span>
```powershell
PS C:\> Get-AzSignalRUsage eastus

Name                 CurrentValue Limit
----                 ------------ -----
FreeTierInstances    2            5
SignalRTotalUnits    3            300
```

## <span data-ttu-id="bb65a-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bb65a-109">PARAMETERS</span></span>

### <span data-ttu-id="bb65a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb65a-110">-DefaultProfile</span></span>
<span data-ttu-id="bb65a-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bb65a-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb65a-112">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="bb65a-112">-Location</span></span>
<span data-ttu-id="bb65a-113">Lokalizacja usługi sygnalizacji.</span><span class="sxs-lookup"><span data-stu-id="bb65a-113">The SignalR service location.</span></span>

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

### <span data-ttu-id="bb65a-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb65a-114">CommonParameters</span></span>
<span data-ttu-id="bb65a-115">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb65a-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb65a-116">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bb65a-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb65a-117">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bb65a-117">INPUTS</span></span>

### <span data-ttu-id="bb65a-118">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="bb65a-118">None</span></span>

## <span data-ttu-id="bb65a-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bb65a-119">OUTPUTS</span></span>

### <span data-ttu-id="bb65a-120">Microsoft. Azure. Commands. Signals. modele. PSSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="bb65a-120">Microsoft.Azure.Commands.SignalR.Models.PSSignalRUsage</span></span>

## <span data-ttu-id="bb65a-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bb65a-121">NOTES</span></span>

## <span data-ttu-id="bb65a-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bb65a-122">RELATED LINKS</span></span>
