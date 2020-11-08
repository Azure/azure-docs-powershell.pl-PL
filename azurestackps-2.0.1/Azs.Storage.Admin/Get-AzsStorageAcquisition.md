---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/get-azsstorageacquisition
schema: 2.0.0
ms.openlocfilehash: 098c268d3894d85efe0e17618b5d7ec46b82b0f2
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/24/2020
ms.locfileid: "94054227"
---
# <span data-ttu-id="991c9-101">Get-AzsStorageAcquisition</span><span class="sxs-lookup"><span data-stu-id="991c9-101">Get-AzsStorageAcquisition</span></span>

## <span data-ttu-id="991c9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="991c9-102">SYNOPSIS</span></span>
<span data-ttu-id="991c9-103">Zwraca listę operacji nabycia obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="991c9-103">Returns a list of BLOB acquisitions.</span></span>

## <span data-ttu-id="991c9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="991c9-104">SYNTAX</span></span>

```
Get-AzsStorageAcquisition [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="991c9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="991c9-105">DESCRIPTION</span></span>
<span data-ttu-id="991c9-106">Zwraca listę operacji nabycia obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="991c9-106">Returns a list of BLOB acquisitions.</span></span>

## <span data-ttu-id="991c9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="991c9-107">EXAMPLES</span></span>

### <span data-ttu-id="991c9-108">Przykład 1:</span><span class="sxs-lookup"><span data-stu-id="991c9-108">Example 1:</span></span>
```powershell
PS C:\> Get-AzsStorageAcquisition
```

<span data-ttu-id="991c9-109">Pobierz listę obiektów BLOB acquistions.</span><span class="sxs-lookup"><span data-stu-id="991c9-109">Get the list of blob acquistions.</span></span>

## <span data-ttu-id="991c9-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="991c9-110">PARAMETERS</span></span>

### <span data-ttu-id="991c9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="991c9-111">-DefaultProfile</span></span>
<span data-ttu-id="991c9-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="991c9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="991c9-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="991c9-113">-Location</span></span>
<span data-ttu-id="991c9-114">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="991c9-114">Resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="991c9-115">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="991c9-115">-SubscriptionId</span></span>
<span data-ttu-id="991c9-116">Identyfikator abonamentu.</span><span class="sxs-lookup"><span data-stu-id="991c9-116">Subscription Id.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="991c9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="991c9-117">CommonParameters</span></span>
<span data-ttu-id="991c9-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="991c9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="991c9-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="991c9-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="991c9-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="991c9-120">INPUTS</span></span>

## <span data-ttu-id="991c9-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="991c9-121">OUTPUTS</span></span>

### <span data-ttu-id="991c9-122">Microsoft. Azure. PowerShell. polecenia. StorageAdmin. models. Api201908Preview. IAcquisition</span><span class="sxs-lookup"><span data-stu-id="991c9-122">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IAcquisition</span></span>



## <span data-ttu-id="991c9-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="991c9-123">NOTES</span></span>

## <span data-ttu-id="991c9-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="991c9-124">RELATED LINKS</span></span>

