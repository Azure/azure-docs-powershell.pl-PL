---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 47ac85406955592cba566df505900e6c42befb7a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523518"
---
# <span data-ttu-id="ec06b-101">Get-AzsStorageDestinationShare</span><span class="sxs-lookup"><span data-stu-id="ec06b-101">Get-AzsStorageDestinationShare</span></span>

## <span data-ttu-id="ec06b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ec06b-102">SYNOPSIS</span></span>
<span data-ttu-id="ec06b-103">Zwraca listę udziałów docelowych, które system traktuje jako najlepszą liczbę kandydatów do migracji.</span><span class="sxs-lookup"><span data-stu-id="ec06b-103">Returns a list of destination shares that the system considers as best candidates for migration.</span></span>

## <span data-ttu-id="ec06b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ec06b-104">SYNTAX</span></span>

```
Get-AzsStorageDestinationShare [-SourceShareName] <String> [-FarmName] <String> [[-ResourceGroupName] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="ec06b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ec06b-105">DESCRIPTION</span></span>
<span data-ttu-id="ec06b-106">Zwraca listę udziałów docelowych, które system traktuje jako najlepszą liczbę kandydatów do migracji.</span><span class="sxs-lookup"><span data-stu-id="ec06b-106">Returns a list of destination shares that the system considers as best candidates for migration.</span></span>

## <span data-ttu-id="ec06b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ec06b-107">EXAMPLES</span></span>

### <span data-ttu-id="ec06b-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ec06b-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageDestinationShare -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -SourceShareName "||SU1FileServer.azurestack.local|SU1_ObjStore"
```

<span data-ttu-id="ec06b-109">Uzyskaj listę udziałów docelowych, które system traktuje jako najlepszego kandydatów do migracji.</span><span class="sxs-lookup"><span data-stu-id="ec06b-109">Get a list of destination shares that the system considers as best candidates for migration.</span></span>

## <span data-ttu-id="ec06b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ec06b-110">PARAMETERS</span></span>

### <span data-ttu-id="ec06b-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="ec06b-111">-FarmName</span></span>
<span data-ttu-id="ec06b-112">Identyfikator farmy.</span><span class="sxs-lookup"><span data-stu-id="ec06b-112">Farm Id.</span></span>

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

### <span data-ttu-id="ec06b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec06b-113">-ResourceGroupName</span></span>
<span data-ttu-id="ec06b-114">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ec06b-114">Resource group name.</span></span>

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

### <span data-ttu-id="ec06b-115">-SourceShareName</span><span class="sxs-lookup"><span data-stu-id="ec06b-115">-SourceShareName</span></span>
<span data-ttu-id="ec06b-116">Nazwa udziału, który przechowuje migrację kontenerów.</span><span class="sxs-lookup"><span data-stu-id="ec06b-116">Name of the share which holds containers to be migrated.</span></span>

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

### <span data-ttu-id="ec06b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec06b-117">CommonParameters</span></span>
<span data-ttu-id="ec06b-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec06b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec06b-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec06b-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec06b-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ec06b-120">INPUTS</span></span>

## <span data-ttu-id="ec06b-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ec06b-121">OUTPUTS</span></span>

## <span data-ttu-id="ec06b-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ec06b-122">NOTES</span></span>

## <span data-ttu-id="ec06b-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ec06b-123">RELATED LINKS</span></span>

