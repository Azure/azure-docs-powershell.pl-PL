---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5d94fdb44a5e37988853c95de794d67fcb26a515
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93889165"
---
# <span data-ttu-id="f8307-101">Get-AzsUpdateLocation</span><span class="sxs-lookup"><span data-stu-id="f8307-101">Get-AzsUpdateLocation</span></span>

## <span data-ttu-id="f8307-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f8307-102">SYNOPSIS</span></span>
<span data-ttu-id="f8307-103">Pobierz listę lokalizacji aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="f8307-103">Get the list of update locations.</span></span>

## <span data-ttu-id="f8307-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f8307-104">SYNTAX</span></span>

### <span data-ttu-id="f8307-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="f8307-105">List (Default)</span></span>
```
Get-AzsUpdateLocation [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="f8307-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="f8307-106">Get</span></span>
```
Get-AzsUpdateLocation [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="f8307-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="f8307-107">ResourceId</span></span>
```
Get-AzsUpdateLocation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="f8307-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f8307-108">DESCRIPTION</span></span>
<span data-ttu-id="f8307-109">Pobierz listę lokalizacji aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="f8307-109">Get the list of update locations.</span></span> <span data-ttu-id="f8307-110">Zwracane lokalizacje mogą być używane do uzyskiwania dostępnych aktualizacji w określonej lokalizacji za pomocą polecenia Get-AzsUpdate.</span><span class="sxs-lookup"><span data-stu-id="f8307-110">The locations returned can be used to get available updates at a particular location using Get-AzsUpdate.</span></span>

## <span data-ttu-id="f8307-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f8307-111">EXAMPLES</span></span>

### <span data-ttu-id="f8307-112">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="f8307-112">EXAMPLE 1</span></span>
```
Get-AzsUpdateLocation
```

<span data-ttu-id="f8307-113">Pobierz listę lokalizacji aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="f8307-113">Get the list of update locations.</span></span>

## <span data-ttu-id="f8307-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f8307-114">PARAMETERS</span></span>

### <span data-ttu-id="f8307-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f8307-115">-Location</span></span>
<span data-ttu-id="f8307-116">Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="f8307-116">Name of the Location.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8307-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8307-117">-ResourceGroupName</span></span>
<span data-ttu-id="f8307-118">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="f8307-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="f8307-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f8307-119">-ResourceId</span></span>
<span data-ttu-id="f8307-120">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="f8307-120">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8307-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8307-121">CommonParameters</span></span>
<span data-ttu-id="f8307-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8307-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8307-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8307-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8307-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f8307-124">INPUTS</span></span>

## <span data-ttu-id="f8307-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f8307-125">OUTPUTS</span></span>

### <span data-ttu-id="f8307-126">Microsoft. AzureStack. Management. Update. admin. models. UpdateLocation</span><span class="sxs-lookup"><span data-stu-id="f8307-126">Microsoft.AzureStack.Management.Update.Admin.Models.UpdateLocation</span></span>

## <span data-ttu-id="f8307-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f8307-127">NOTES</span></span>

## <span data-ttu-id="f8307-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f8307-128">RELATED LINKS</span></span>
