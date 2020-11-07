---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7d6bd071f4e1d61fdf2d682459dbe8baa57b5276
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93889842"
---
# <span data-ttu-id="32e69-101">Get-AzsQueueService</span><span class="sxs-lookup"><span data-stu-id="32e69-101">Get-AzsQueueService</span></span>

## <span data-ttu-id="32e69-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="32e69-102">SYNOPSIS</span></span>
<span data-ttu-id="32e69-103">Zwraca usługę kolejek.</span><span class="sxs-lookup"><span data-stu-id="32e69-103">Returns the queue service.</span></span>

## <span data-ttu-id="32e69-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="32e69-104">SYNTAX</span></span>

```
Get-AzsQueueService [-FarmName] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

## <span data-ttu-id="32e69-105">Opis</span><span class="sxs-lookup"><span data-stu-id="32e69-105">DESCRIPTION</span></span>
<span data-ttu-id="32e69-106">Zwraca usługę kolejek.</span><span class="sxs-lookup"><span data-stu-id="32e69-106">Returns the queue service.</span></span>

## <span data-ttu-id="32e69-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="32e69-107">EXAMPLES</span></span>

### <span data-ttu-id="32e69-108">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="32e69-108">EXAMPLE 1</span></span>
```
Get-AzsQueueService -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="32e69-109">Pobierz usługę kolejkowania.</span><span class="sxs-lookup"><span data-stu-id="32e69-109">Get the queue service.</span></span>

## <span data-ttu-id="32e69-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="32e69-110">PARAMETERS</span></span>

### <span data-ttu-id="32e69-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="32e69-111">-FarmName</span></span>
<span data-ttu-id="32e69-112">Identyfikator farmy.</span><span class="sxs-lookup"><span data-stu-id="32e69-112">Farm Id.</span></span>

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

### <span data-ttu-id="32e69-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32e69-113">-ResourceGroupName</span></span>
<span data-ttu-id="32e69-114">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="32e69-114">Resource group name.</span></span>

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

### <span data-ttu-id="32e69-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32e69-115">CommonParameters</span></span>
<span data-ttu-id="32e69-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32e69-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32e69-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32e69-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32e69-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="32e69-118">INPUTS</span></span>

## <span data-ttu-id="32e69-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="32e69-119">OUTPUTS</span></span>

### <span data-ttu-id="32e69-120">Microsoft. AzureStack. Management. Storage. admin. models. QueueService</span><span class="sxs-lookup"><span data-stu-id="32e69-120">Microsoft.AzureStack.Management.Storage.Admin.Models.QueueService</span></span>

## <span data-ttu-id="32e69-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="32e69-121">NOTES</span></span>

## <span data-ttu-id="32e69-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="32e69-122">RELATED LINKS</span></span>
