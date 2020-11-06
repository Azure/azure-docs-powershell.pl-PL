---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 268a306597fe3760e8abc7e31f980da078bf2bc2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523862"
---
# <span data-ttu-id="98777-101">Get-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="98777-101">Get-AzsUpdateRun</span></span>

## <span data-ttu-id="98777-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="98777-102">SYNOPSIS</span></span>
<span data-ttu-id="98777-103">Pobierz listę przebiegów aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="98777-103">Get the list of update runs.</span></span>

## <span data-ttu-id="98777-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="98777-104">SYNTAX</span></span>

### <span data-ttu-id="98777-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="98777-105">List (Default)</span></span>
```
Get-AzsUpdateRun -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="98777-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="98777-106">Get</span></span>
```
Get-AzsUpdateRun -Name <String> -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="98777-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="98777-107">ResourceId</span></span>
```
Get-AzsUpdateRun -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="98777-108">Opis</span><span class="sxs-lookup"><span data-stu-id="98777-108">DESCRIPTION</span></span>
<span data-ttu-id="98777-109">Pobierz listę przebiegów aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="98777-109">Get the list of update runs.</span></span> <span data-ttu-id="98777-110">Po odpowiednim przypadku wystąpienia zwróconych obiektów UpdateRun można popotokować w celu ponownego uruchomienia-AzsUpdateRun.</span><span class="sxs-lookup"><span data-stu-id="98777-110">Instances of the UpdateRun objects returned can be piped to Restart-AzsUpdateRun, when applicable.</span></span>

## <span data-ttu-id="98777-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="98777-111">EXAMPLES</span></span>

### <span data-ttu-id="98777-112">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="98777-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUpdateRun -UpdateName Microsoft1.0.180302.1
```

<span data-ttu-id="98777-113">Zapoznaj się z listą wszystkich prób zastosowania określonej aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="98777-113">Get a list of all attempts to apply a specific update.</span></span>

## <span data-ttu-id="98777-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="98777-114">PARAMETERS</span></span>

### <span data-ttu-id="98777-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="98777-115">-Location</span></span>
<span data-ttu-id="98777-116">Nazwa lokalizacji aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="98777-116">The name of the update location.</span></span>

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

### <span data-ttu-id="98777-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="98777-117">-Name</span></span>
<span data-ttu-id="98777-118">Identyfikator uruchomienia aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="98777-118">Update run identifier.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98777-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98777-119">-ResourceGroupName</span></span>
<span data-ttu-id="98777-120">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="98777-120">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="98777-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98777-121">-ResourceId</span></span>
<span data-ttu-id="98777-122">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="98777-122">The resource id.</span></span>

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

### <span data-ttu-id="98777-123">-Skip</span><span class="sxs-lookup"><span data-stu-id="98777-123">-Skip</span></span>
<span data-ttu-id="98777-124">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="98777-124">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="98777-125">-Początek</span><span class="sxs-lookup"><span data-stu-id="98777-125">-Top</span></span>
<span data-ttu-id="98777-126">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="98777-126">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="98777-127">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="98777-127">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="98777-128">-Updatename</span><span class="sxs-lookup"><span data-stu-id="98777-128">-UpdateName</span></span>
<span data-ttu-id="98777-129">Nazwa aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="98777-129">Name of the update.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98777-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98777-130">CommonParameters</span></span>
<span data-ttu-id="98777-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98777-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98777-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98777-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98777-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="98777-133">INPUTS</span></span>

## <span data-ttu-id="98777-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="98777-134">OUTPUTS</span></span>

### <span data-ttu-id="98777-135">Microsoft. AzureStack. Management. Update. admin. models. UpdateRun</span><span class="sxs-lookup"><span data-stu-id="98777-135">Microsoft.AzureStack.Management.Update.Admin.Models.UpdateRun</span></span>

## <span data-ttu-id="98777-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="98777-136">NOTES</span></span>

## <span data-ttu-id="98777-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="98777-137">RELATED LINKS</span></span>

