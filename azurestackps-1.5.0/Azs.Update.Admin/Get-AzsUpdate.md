---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: dc16e5ecb0a70c20f9cd8b77b16208a09ac0a023
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523786"
---
# <span data-ttu-id="887c5-101">Get-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="887c5-101">Get-AzsUpdate</span></span>

## <span data-ttu-id="887c5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="887c5-102">SYNOPSIS</span></span>
<span data-ttu-id="887c5-103">Pobierz listę dostępnych aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="887c5-103">Get the list of available updates.</span></span>

## <span data-ttu-id="887c5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="887c5-104">SYNTAX</span></span>

### <span data-ttu-id="887c5-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="887c5-105">List (Default)</span></span>
```
Get-AzsUpdate [-Location <String>] [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="887c5-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="887c5-106">Get</span></span>
```
Get-AzsUpdate [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="887c5-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="887c5-107">ResourceId</span></span>
```
Get-AzsUpdate -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="887c5-108">Opis</span><span class="sxs-lookup"><span data-stu-id="887c5-108">DESCRIPTION</span></span>
<span data-ttu-id="887c5-109">Pobierz listę dostępnych aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="887c5-109">Get the list of available updates.</span></span> <span data-ttu-id="887c5-110">Aktualizacje zwrócone w tym module mogą być potokami "Install-AzsUpdate", jeśli ma to zastosowanie.</span><span class="sxs-lookup"><span data-stu-id="887c5-110">Updates returned from this module may be piped to 'Install-AzsUpdate', if applicable.</span></span>

## <span data-ttu-id="887c5-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="887c5-111">EXAMPLES</span></span>

### <span data-ttu-id="887c5-112">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="887c5-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUpdate | ft
```

<span data-ttu-id="887c5-113">Pobierz listę dostępnych aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="887c5-113">Get the list of available updates.</span></span>

### <span data-ttu-id="887c5-114">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="887c5-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsUpdate -Name Microsoft1.0.180305.1
```

<span data-ttu-id="887c5-115">Pobierz określoną aktualizację.</span><span class="sxs-lookup"><span data-stu-id="887c5-115">Get the specific update.</span></span>

## <span data-ttu-id="887c5-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="887c5-116">PARAMETERS</span></span>

### <span data-ttu-id="887c5-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="887c5-117">-Location</span></span>
<span data-ttu-id="887c5-118">Nazwa lokalizacji aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="887c5-118">The name of the update location.</span></span>

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

### <span data-ttu-id="887c5-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="887c5-119">-Name</span></span>
<span data-ttu-id="887c5-120">Nazwa aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="887c5-120">Name of the update.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: Update

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="887c5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="887c5-121">-ResourceGroupName</span></span>
<span data-ttu-id="887c5-122">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="887c5-122">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="887c5-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="887c5-123">-ResourceId</span></span>
<span data-ttu-id="887c5-124">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="887c5-124">The resource id.</span></span>

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

### <span data-ttu-id="887c5-125">-Skip</span><span class="sxs-lookup"><span data-stu-id="887c5-125">-Skip</span></span>
<span data-ttu-id="887c5-126">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="887c5-126">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="887c5-127">-Początek</span><span class="sxs-lookup"><span data-stu-id="887c5-127">-Top</span></span>
<span data-ttu-id="887c5-128">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="887c5-128">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="887c5-129">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="887c5-129">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="887c5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="887c5-130">CommonParameters</span></span>
<span data-ttu-id="887c5-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="887c5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="887c5-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="887c5-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="887c5-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="887c5-133">INPUTS</span></span>

## <span data-ttu-id="887c5-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="887c5-134">OUTPUTS</span></span>

### <span data-ttu-id="887c5-135">Microsoft. AzureStack. Management. Update. admin. models. Update</span><span class="sxs-lookup"><span data-stu-id="887c5-135">Microsoft.AzureStack.Management.Update.Admin.Models.Update</span></span>

## <span data-ttu-id="887c5-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="887c5-136">NOTES</span></span>

## <span data-ttu-id="887c5-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="887c5-137">RELATED LINKS</span></span>
