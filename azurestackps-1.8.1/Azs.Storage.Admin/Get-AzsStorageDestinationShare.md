---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0a75fafa646839375bf9dc7f1a64b3084fd31ee4
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93889813"
---
# <span data-ttu-id="b31f9-101">Get-AzsStorageDestinationShare</span><span class="sxs-lookup"><span data-stu-id="b31f9-101">Get-AzsStorageDestinationShare</span></span>

## <span data-ttu-id="b31f9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b31f9-102">SYNOPSIS</span></span>
<span data-ttu-id="b31f9-103">Zwraca listę udziałów docelowych, które system traktuje jako najlepszą liczbę kandydatów do migracji.</span><span class="sxs-lookup"><span data-stu-id="b31f9-103">Returns a list of destination shares that the system considers as best candidates for migration.</span></span>

## <span data-ttu-id="b31f9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b31f9-104">SYNTAX</span></span>

```
Get-AzsStorageDestinationShare [-SourceShareName] <String> [-FarmName] <String> [[-ResourceGroupName] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="b31f9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b31f9-105">DESCRIPTION</span></span>
<span data-ttu-id="b31f9-106">Zwraca listę udziałów docelowych, które system traktuje jako najlepszą liczbę kandydatów do migracji.</span><span class="sxs-lookup"><span data-stu-id="b31f9-106">Returns a list of destination shares that the system considers as best candidates for migration.</span></span>

## <span data-ttu-id="b31f9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b31f9-107">EXAMPLES</span></span>

### <span data-ttu-id="b31f9-108">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="b31f9-108">EXAMPLE 1</span></span>
```
Get-AzsStorageDestinationShare -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -SourceShareName "||SU1FileServer.azurestack.local|SU1_ObjStore"
```

<span data-ttu-id="b31f9-109">Uzyskaj listę udziałów docelowych, które system traktuje jako najlepszego kandydatów do migracji.</span><span class="sxs-lookup"><span data-stu-id="b31f9-109">Get a list of destination shares that the system considers as best candidates for migration.</span></span>

## <span data-ttu-id="b31f9-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b31f9-110">PARAMETERS</span></span>

### <span data-ttu-id="b31f9-111">-SourceShareName</span><span class="sxs-lookup"><span data-stu-id="b31f9-111">-SourceShareName</span></span>
<span data-ttu-id="b31f9-112">Nazwa udziału, który przechowuje migrację kontenerów.</span><span class="sxs-lookup"><span data-stu-id="b31f9-112">Name of the share which holds containers to be migrated.</span></span>

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

### <span data-ttu-id="b31f9-113">-Farmname</span><span class="sxs-lookup"><span data-stu-id="b31f9-113">-FarmName</span></span>
<span data-ttu-id="b31f9-114">Identyfikator farmy.</span><span class="sxs-lookup"><span data-stu-id="b31f9-114">Farm Id.</span></span>

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

### <span data-ttu-id="b31f9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b31f9-115">-ResourceGroupName</span></span>
<span data-ttu-id="b31f9-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b31f9-116">Resource group name.</span></span>

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

### <span data-ttu-id="b31f9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b31f9-117">CommonParameters</span></span>
<span data-ttu-id="b31f9-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b31f9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b31f9-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b31f9-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b31f9-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b31f9-120">INPUTS</span></span>

## <span data-ttu-id="b31f9-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b31f9-121">OUTPUTS</span></span>

## <span data-ttu-id="b31f9-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b31f9-122">NOTES</span></span>

## <span data-ttu-id="b31f9-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b31f9-123">RELATED LINKS</span></span>
