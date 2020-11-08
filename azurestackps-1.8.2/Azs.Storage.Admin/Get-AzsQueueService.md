---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7d6bd071f4e1d61fdf2d682459dbe8baa57b5276
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055864"
---
# <span data-ttu-id="a9737-101">Get-AzsQueueService</span><span class="sxs-lookup"><span data-stu-id="a9737-101">Get-AzsQueueService</span></span>

## <span data-ttu-id="a9737-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a9737-102">SYNOPSIS</span></span>
<span data-ttu-id="a9737-103">Zwraca usługę kolejek.</span><span class="sxs-lookup"><span data-stu-id="a9737-103">Returns the queue service.</span></span>

## <span data-ttu-id="a9737-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a9737-104">SYNTAX</span></span>

```
Get-AzsQueueService [-FarmName] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

## <span data-ttu-id="a9737-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a9737-105">DESCRIPTION</span></span>
<span data-ttu-id="a9737-106">Zwraca usługę kolejek.</span><span class="sxs-lookup"><span data-stu-id="a9737-106">Returns the queue service.</span></span>

## <span data-ttu-id="a9737-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a9737-107">EXAMPLES</span></span>

### <span data-ttu-id="a9737-108">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="a9737-108">EXAMPLE 1</span></span>
```
Get-AzsQueueService -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="a9737-109">Pobierz usługę kolejkowania.</span><span class="sxs-lookup"><span data-stu-id="a9737-109">Get the queue service.</span></span>

## <span data-ttu-id="a9737-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a9737-110">PARAMETERS</span></span>

### <span data-ttu-id="a9737-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="a9737-111">-FarmName</span></span>
<span data-ttu-id="a9737-112">Identyfikator farmy.</span><span class="sxs-lookup"><span data-stu-id="a9737-112">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9737-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9737-113">-ResourceGroupName</span></span>
<span data-ttu-id="a9737-114">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a9737-114">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9737-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9737-115">CommonParameters</span></span>
<span data-ttu-id="a9737-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9737-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9737-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9737-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9737-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a9737-118">INPUTS</span></span>

## <span data-ttu-id="a9737-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a9737-119">OUTPUTS</span></span>

### <span data-ttu-id="a9737-120">Microsoft. AzureStack. Management. Storage. admin. models. QueueService</span><span class="sxs-lookup"><span data-stu-id="a9737-120">Microsoft.AzureStack.Management.Storage.Admin.Models.QueueService</span></span>

## <span data-ttu-id="a9737-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a9737-121">NOTES</span></span>

## <span data-ttu-id="a9737-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a9737-122">RELATED LINKS</span></span>
