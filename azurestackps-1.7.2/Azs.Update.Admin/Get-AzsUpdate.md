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
ms.locfileid: "93888765"
---
# <span data-ttu-id="147b3-101">Get-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="147b3-101">Get-AzsUpdate</span></span>

## <span data-ttu-id="147b3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="147b3-102">SYNOPSIS</span></span>
<span data-ttu-id="147b3-103">Pobierz listę dostępnych aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="147b3-103">Get the list of available updates.</span></span>

## <span data-ttu-id="147b3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="147b3-104">SYNTAX</span></span>

### <span data-ttu-id="147b3-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="147b3-105">List (Default)</span></span>
```
Get-AzsUpdate [-Location <String>] [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="147b3-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="147b3-106">Get</span></span>
```
Get-AzsUpdate [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="147b3-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="147b3-107">ResourceId</span></span>
```
Get-AzsUpdate -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="147b3-108">Opis</span><span class="sxs-lookup"><span data-stu-id="147b3-108">DESCRIPTION</span></span>
<span data-ttu-id="147b3-109">Pobierz listę dostępnych aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="147b3-109">Get the list of available updates.</span></span> <span data-ttu-id="147b3-110">Aktualizacje zwrócone w tym module mogą być potokami "Install-AzsUpdate", jeśli ma to zastosowanie.</span><span class="sxs-lookup"><span data-stu-id="147b3-110">Updates returned from this module may be piped to 'Install-AzsUpdate', if applicable.</span></span>

## <span data-ttu-id="147b3-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="147b3-111">EXAMPLES</span></span>

### <span data-ttu-id="147b3-112">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="147b3-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUpdate | ft
```

<span data-ttu-id="147b3-113">Pobierz listę dostępnych aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="147b3-113">Get the list of available updates.</span></span>

### <span data-ttu-id="147b3-114">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="147b3-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsUpdate -Name Microsoft1.0.180305.1
```

<span data-ttu-id="147b3-115">Pobierz określoną aktualizację.</span><span class="sxs-lookup"><span data-stu-id="147b3-115">Get the specific update.</span></span>

## <span data-ttu-id="147b3-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="147b3-116">PARAMETERS</span></span>

### <span data-ttu-id="147b3-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="147b3-117">-Location</span></span>
<span data-ttu-id="147b3-118">Nazwa lokalizacji aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="147b3-118">The name of the update location.</span></span>

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

### <span data-ttu-id="147b3-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="147b3-119">-Name</span></span>
<span data-ttu-id="147b3-120">Nazwa aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="147b3-120">Name of the update.</span></span>

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

### <span data-ttu-id="147b3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="147b3-121">-ResourceGroupName</span></span>
<span data-ttu-id="147b3-122">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="147b3-122">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="147b3-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="147b3-123">-ResourceId</span></span>
<span data-ttu-id="147b3-124">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="147b3-124">The resource id.</span></span>

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

### <span data-ttu-id="147b3-125">-Skip</span><span class="sxs-lookup"><span data-stu-id="147b3-125">-Skip</span></span>
<span data-ttu-id="147b3-126">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="147b3-126">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="147b3-127">-Początek</span><span class="sxs-lookup"><span data-stu-id="147b3-127">-Top</span></span>
<span data-ttu-id="147b3-128">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="147b3-128">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="147b3-129">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="147b3-129">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="147b3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="147b3-130">CommonParameters</span></span>
<span data-ttu-id="147b3-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="147b3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="147b3-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="147b3-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="147b3-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="147b3-133">INPUTS</span></span>

## <span data-ttu-id="147b3-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="147b3-134">OUTPUTS</span></span>

### <span data-ttu-id="147b3-135">Microsoft. AzureStack. Management. Update. admin. models. Update</span><span class="sxs-lookup"><span data-stu-id="147b3-135">Microsoft.AzureStack.Management.Update.Admin.Models.Update</span></span>

## <span data-ttu-id="147b3-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="147b3-136">NOTES</span></span>

## <span data-ttu-id="147b3-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="147b3-137">RELATED LINKS</span></span>

