---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 62c174a3aec5034b230954922f6aab5078fe4bac
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93889430"
---
# <span data-ttu-id="03810-101">Get-AzsQueueService</span><span class="sxs-lookup"><span data-stu-id="03810-101">Get-AzsQueueService</span></span>

## <span data-ttu-id="03810-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="03810-102">SYNOPSIS</span></span>
<span data-ttu-id="03810-103">Zwraca usługę kolejek.</span><span class="sxs-lookup"><span data-stu-id="03810-103">Returns the queue service.</span></span>

## <span data-ttu-id="03810-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="03810-104">SYNTAX</span></span>

```
Get-AzsQueueService [-FarmName] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

## <span data-ttu-id="03810-105">Opis</span><span class="sxs-lookup"><span data-stu-id="03810-105">DESCRIPTION</span></span>
<span data-ttu-id="03810-106">Zwraca usługę kolejek.</span><span class="sxs-lookup"><span data-stu-id="03810-106">Returns the queue service.</span></span>

## <span data-ttu-id="03810-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="03810-107">EXAMPLES</span></span>

### <span data-ttu-id="03810-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="03810-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsQueueService -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="03810-109">Pobierz usługę kolejkowania.</span><span class="sxs-lookup"><span data-stu-id="03810-109">Get the queue service.</span></span>

## <span data-ttu-id="03810-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="03810-110">PARAMETERS</span></span>

### <span data-ttu-id="03810-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="03810-111">-FarmName</span></span>
<span data-ttu-id="03810-112">Identyfikator farmy.</span><span class="sxs-lookup"><span data-stu-id="03810-112">Farm Id.</span></span>

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

### <span data-ttu-id="03810-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03810-113">-ResourceGroupName</span></span>
<span data-ttu-id="03810-114">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="03810-114">Resource group name.</span></span>

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

### <span data-ttu-id="03810-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03810-115">CommonParameters</span></span>
<span data-ttu-id="03810-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03810-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03810-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03810-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03810-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="03810-118">INPUTS</span></span>

## <span data-ttu-id="03810-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="03810-119">OUTPUTS</span></span>

### <span data-ttu-id="03810-120">Microsoft. AzureStack. Management. Storage. admin. models. QueueService</span><span class="sxs-lookup"><span data-stu-id="03810-120">Microsoft.AzureStack.Management.Storage.Admin.Models.QueueService</span></span>

## <span data-ttu-id="03810-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="03810-121">NOTES</span></span>

## <span data-ttu-id="03810-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="03810-122">RELATED LINKS</span></span>

