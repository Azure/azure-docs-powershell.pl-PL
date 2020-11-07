---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 87bab7bc266a77d9459bb0a3166d09f2b7d6c7de
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93889785"
---
# <span data-ttu-id="71621-101">Get-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="71621-101">Get-AzsUpdate</span></span>

## <span data-ttu-id="71621-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="71621-102">SYNOPSIS</span></span>
<span data-ttu-id="71621-103">Pobierz listę dostępnych aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="71621-103">Get the list of available updates.</span></span>

## <span data-ttu-id="71621-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="71621-104">SYNTAX</span></span>

### <span data-ttu-id="71621-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="71621-105">List (Default)</span></span>
```
Get-AzsUpdate [-Location <String>] [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="71621-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="71621-106">Get</span></span>
```
Get-AzsUpdate [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="71621-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="71621-107">ResourceId</span></span>
```
Get-AzsUpdate -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="71621-108">Opis</span><span class="sxs-lookup"><span data-stu-id="71621-108">DESCRIPTION</span></span>
<span data-ttu-id="71621-109">Pobierz listę dostępnych aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="71621-109">Get the list of available updates.</span></span> <span data-ttu-id="71621-110">Aktualizacje zwrócone w tym module mogą być potokami "Install-AzsUpdate", jeśli ma to zastosowanie.</span><span class="sxs-lookup"><span data-stu-id="71621-110">Updates returned from this module may be piped to 'Install-AzsUpdate', if applicable.</span></span>

## <span data-ttu-id="71621-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="71621-111">EXAMPLES</span></span>

### <span data-ttu-id="71621-112">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="71621-112">EXAMPLE 1</span></span>
```
Get-AzsUpdate | ft
```

<span data-ttu-id="71621-113">Pobierz listę dostępnych aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="71621-113">Get the list of available updates.</span></span>

### <span data-ttu-id="71621-114">PRZYKŁAD 2</span><span class="sxs-lookup"><span data-stu-id="71621-114">EXAMPLE 2</span></span>
```
Get-AzsUpdate -Name Microsoft1.0.180305.1
```

<span data-ttu-id="71621-115">Pobierz określoną aktualizację.</span><span class="sxs-lookup"><span data-stu-id="71621-115">Get the specific update.</span></span>

## <span data-ttu-id="71621-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="71621-116">PARAMETERS</span></span>

### <span data-ttu-id="71621-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="71621-117">-Name</span></span>
<span data-ttu-id="71621-118">Nazwa aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="71621-118">Name of the update.</span></span>

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

### <span data-ttu-id="71621-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="71621-119">-Location</span></span>
<span data-ttu-id="71621-120">Nazwa lokalizacji aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="71621-120">The name of the update location.</span></span>

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

### <span data-ttu-id="71621-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71621-121">-ResourceGroupName</span></span>
<span data-ttu-id="71621-122">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="71621-122">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="71621-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="71621-123">-ResourceId</span></span>
<span data-ttu-id="71621-124">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="71621-124">The resource id.</span></span>

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

### <span data-ttu-id="71621-125">-Skip</span><span class="sxs-lookup"><span data-stu-id="71621-125">-Skip</span></span>
<span data-ttu-id="71621-126">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="71621-126">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="71621-127">-Początek</span><span class="sxs-lookup"><span data-stu-id="71621-127">-Top</span></span>
<span data-ttu-id="71621-128">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="71621-128">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="71621-129">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="71621-129">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="71621-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71621-130">CommonParameters</span></span>
<span data-ttu-id="71621-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71621-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71621-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71621-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71621-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="71621-133">INPUTS</span></span>

## <span data-ttu-id="71621-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="71621-134">OUTPUTS</span></span>

### <span data-ttu-id="71621-135">Microsoft. AzureStack. Management. Update. admin. models. Update</span><span class="sxs-lookup"><span data-stu-id="71621-135">Microsoft.AzureStack.Management.Update.Admin.Models.Update</span></span>

## <span data-ttu-id="71621-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="71621-136">NOTES</span></span>

## <span data-ttu-id="71621-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="71621-137">RELATED LINKS</span></span>
