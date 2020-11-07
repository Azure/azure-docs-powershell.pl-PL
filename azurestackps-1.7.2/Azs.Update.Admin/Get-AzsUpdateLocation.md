---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a9234cb73b1f9c3652827293ae2813f78d7ce336
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704597"
---
# <span data-ttu-id="2dbcb-101">Get-AzsUpdateLocation</span><span class="sxs-lookup"><span data-stu-id="2dbcb-101">Get-AzsUpdateLocation</span></span>

## <span data-ttu-id="2dbcb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2dbcb-102">SYNOPSIS</span></span>
<span data-ttu-id="2dbcb-103">Pobierz listę lokalizacji aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="2dbcb-103">Get the list of update locations.</span></span>

## <span data-ttu-id="2dbcb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2dbcb-104">SYNTAX</span></span>

### <span data-ttu-id="2dbcb-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="2dbcb-105">List (Default)</span></span>
```
Get-AzsUpdateLocation [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="2dbcb-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="2dbcb-106">Get</span></span>
```
Get-AzsUpdateLocation [-Name <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="2dbcb-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="2dbcb-107">ResourceId</span></span>
```
Get-AzsUpdateLocation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="2dbcb-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2dbcb-108">DESCRIPTION</span></span>
<span data-ttu-id="2dbcb-109">Pobierz listę lokalizacji aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="2dbcb-109">Get the list of update locations.</span></span> <span data-ttu-id="2dbcb-110">Zwracane lokalizacje mogą być używane do uzyskiwania dostępnych aktualizacji w określonej lokalizacji za pomocą polecenia Get-AzsUpdate.</span><span class="sxs-lookup"><span data-stu-id="2dbcb-110">The locations returned can be used to get available updates at a particular location using Get-AzsUpdate.</span></span>

## <span data-ttu-id="2dbcb-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2dbcb-111">EXAMPLES</span></span>

### <span data-ttu-id="2dbcb-112">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2dbcb-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUpdateLocation
```

<span data-ttu-id="2dbcb-113">Pobierz listę lokalizacji aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="2dbcb-113">Get the list of update locations.</span></span>

## <span data-ttu-id="2dbcb-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2dbcb-114">PARAMETERS</span></span>

### <span data-ttu-id="2dbcb-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2dbcb-115">-Name</span></span>
<span data-ttu-id="2dbcb-116">Nazwa lokalizacji aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="2dbcb-116">The name of the update location.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: Location

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dbcb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dbcb-117">-ResourceGroupName</span></span>
<span data-ttu-id="2dbcb-118">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="2dbcb-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="2dbcb-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2dbcb-119">-ResourceId</span></span>
<span data-ttu-id="2dbcb-120">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="2dbcb-120">The resource id.</span></span>

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

### <span data-ttu-id="2dbcb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dbcb-121">CommonParameters</span></span>
<span data-ttu-id="2dbcb-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2dbcb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dbcb-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2dbcb-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dbcb-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2dbcb-124">INPUTS</span></span>

## <span data-ttu-id="2dbcb-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2dbcb-125">OUTPUTS</span></span>

### <span data-ttu-id="2dbcb-126">Microsoft. AzureStack. Management. Update. admin. models. UpdateLocation</span><span class="sxs-lookup"><span data-stu-id="2dbcb-126">Microsoft.AzureStack.Management.Update.Admin.Models.UpdateLocation</span></span>

## <span data-ttu-id="2dbcb-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2dbcb-127">NOTES</span></span>

## <span data-ttu-id="2dbcb-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2dbcb-128">RELATED LINKS</span></span>

