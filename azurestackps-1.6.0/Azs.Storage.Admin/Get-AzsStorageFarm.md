---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 419bddaaa121e052b486bf4bb5408fcae6160fd4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523517"
---
# <span data-ttu-id="7941f-101">Get-AzsStorageFarm</span><span class="sxs-lookup"><span data-stu-id="7941f-101">Get-AzsStorageFarm</span></span>

## <span data-ttu-id="7941f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7941f-102">SYNOPSIS</span></span>
<span data-ttu-id="7941f-103">Zwraca listę wszystkich Farm przestrzeni dyskowej.</span><span class="sxs-lookup"><span data-stu-id="7941f-103">Returns a list of all storage farms.</span></span>

## <span data-ttu-id="7941f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7941f-104">SYNTAX</span></span>

### <span data-ttu-id="7941f-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="7941f-105">List (Default)</span></span>
```
Get-AzsStorageFarm [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="7941f-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="7941f-106">Get</span></span>
```
Get-AzsStorageFarm [-Name] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="7941f-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="7941f-107">ResourceId</span></span>
```
Get-AzsStorageFarm -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="7941f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="7941f-108">DESCRIPTION</span></span>
<span data-ttu-id="7941f-109">Zwraca listę wszystkich Farm przestrzeni dyskowej.</span><span class="sxs-lookup"><span data-stu-id="7941f-109">Returns a list of all storage farms.</span></span>

## <span data-ttu-id="7941f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7941f-110">EXAMPLES</span></span>

### <span data-ttu-id="7941f-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7941f-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageFarm
```

<span data-ttu-id="7941f-112">Pobierz listę wszystkich Farm magazynowania.</span><span class="sxs-lookup"><span data-stu-id="7941f-112">Get the list of all storage farms.</span></span>

## <span data-ttu-id="7941f-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7941f-113">PARAMETERS</span></span>

### <span data-ttu-id="7941f-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7941f-114">-Name</span></span>
<span data-ttu-id="7941f-115">Identyfikator farmy.</span><span class="sxs-lookup"><span data-stu-id="7941f-115">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7941f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7941f-116">-ResourceGroupName</span></span>
<span data-ttu-id="7941f-117">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7941f-117">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7941f-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7941f-118">-ResourceId</span></span>
<span data-ttu-id="7941f-119">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="7941f-119">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7941f-120">-Skip</span><span class="sxs-lookup"><span data-stu-id="7941f-120">-Skip</span></span>
<span data-ttu-id="7941f-121">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="7941f-121">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7941f-122">-Początek</span><span class="sxs-lookup"><span data-stu-id="7941f-122">-Top</span></span>
<span data-ttu-id="7941f-123">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="7941f-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="7941f-124">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="7941f-124">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7941f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7941f-125">CommonParameters</span></span>
<span data-ttu-id="7941f-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7941f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7941f-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7941f-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7941f-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7941f-128">INPUTS</span></span>

## <span data-ttu-id="7941f-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7941f-129">OUTPUTS</span></span>

### <span data-ttu-id="7941f-130">Microsoft. AzureStack. Management. Storage. admin. modele. farma</span><span class="sxs-lookup"><span data-stu-id="7941f-130">Microsoft.AzureStack.Management.Storage.Admin.Models.Farm</span></span>

## <span data-ttu-id="7941f-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7941f-131">NOTES</span></span>

## <span data-ttu-id="7941f-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7941f-132">RELATED LINKS</span></span>

