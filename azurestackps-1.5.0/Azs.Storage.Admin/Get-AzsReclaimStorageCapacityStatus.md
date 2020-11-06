---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: dbd8de47397e86f2aed9f774b555a587cf69976a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523497"
---
# <span data-ttu-id="7a152-101">Get-AzsReclaimStorageCapacityStatus</span><span class="sxs-lookup"><span data-stu-id="7a152-101">Get-AzsReclaimStorageCapacityStatus</span></span>

## <span data-ttu-id="7a152-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7a152-102">SYNOPSIS</span></span>
<span data-ttu-id="7a152-103">Zwraca stan zadania zbierania elementów bezużytecznych.</span><span class="sxs-lookup"><span data-stu-id="7a152-103">Returns the state of the garbage collection job.</span></span>

## <span data-ttu-id="7a152-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7a152-104">SYNTAX</span></span>

```
Get-AzsReclaimStorageCapacityStatus [-FarmName] <String> [-JobId] <String> [[-ResourceGroupName] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="7a152-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7a152-105">DESCRIPTION</span></span>
<span data-ttu-id="7a152-106">Zwraca stan zadania zbierania elementów bezużytecznych.</span><span class="sxs-lookup"><span data-stu-id="7a152-106">Returns the state of the garbage collection job.</span></span>

## <span data-ttu-id="7a152-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7a152-107">EXAMPLES</span></span>

### <span data-ttu-id="7a152-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7a152-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsReclaimStorageCapacityStatus -FarmName "6ddbfe6e-8781-4a3d-b370-4a8b20a494d8" -JobId "92360f29-cd21-429d-a20b-9b11ab5902a0"
```

<span data-ttu-id="7a152-109">Zwracają informacje o stanie wyrzucania elementów bezużytecznych.</span><span class="sxs-lookup"><span data-stu-id="7a152-109">Return information about the status of garbage collection.</span></span>

## <span data-ttu-id="7a152-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7a152-110">PARAMETERS</span></span>

### <span data-ttu-id="7a152-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="7a152-111">-FarmName</span></span>
<span data-ttu-id="7a152-112">Identyfikator farmy.</span><span class="sxs-lookup"><span data-stu-id="7a152-112">Farm Id.</span></span>

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

### <span data-ttu-id="7a152-113">-JobId</span><span class="sxs-lookup"><span data-stu-id="7a152-113">-JobId</span></span>
<span data-ttu-id="7a152-114">Identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="7a152-114">Operation Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a152-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a152-115">-ResourceGroupName</span></span>
<span data-ttu-id="7a152-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7a152-116">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a152-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a152-117">CommonParameters</span></span>
<span data-ttu-id="7a152-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a152-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a152-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a152-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a152-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7a152-120">INPUTS</span></span>

## <span data-ttu-id="7a152-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7a152-121">OUTPUTS</span></span>

## <span data-ttu-id="7a152-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7a152-122">NOTES</span></span>

## <span data-ttu-id="7a152-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7a152-123">RELATED LINKS</span></span>

