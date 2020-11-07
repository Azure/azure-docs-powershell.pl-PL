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
ms.locfileid: "93523785"
---
# <span data-ttu-id="c4f38-101">Get-AzsUpdateLocation</span><span class="sxs-lookup"><span data-stu-id="c4f38-101">Get-AzsUpdateLocation</span></span>

## <span data-ttu-id="c4f38-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c4f38-102">SYNOPSIS</span></span>
<span data-ttu-id="c4f38-103">Pobierz listę lokalizacji aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="c4f38-103">Get the list of update locations.</span></span>

## <span data-ttu-id="c4f38-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c4f38-104">SYNTAX</span></span>

### <span data-ttu-id="c4f38-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="c4f38-105">List (Default)</span></span>
```
Get-AzsUpdateLocation [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="c4f38-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="c4f38-106">Get</span></span>
```
Get-AzsUpdateLocation [-Name <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="c4f38-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="c4f38-107">ResourceId</span></span>
```
Get-AzsUpdateLocation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="c4f38-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c4f38-108">DESCRIPTION</span></span>
<span data-ttu-id="c4f38-109">Pobierz listę lokalizacji aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="c4f38-109">Get the list of update locations.</span></span> <span data-ttu-id="c4f38-110">Zwracane lokalizacje mogą być używane do uzyskiwania dostępnych aktualizacji w określonej lokalizacji za pomocą polecenia Get-AzsUpdate.</span><span class="sxs-lookup"><span data-stu-id="c4f38-110">The locations returned can be used to get available updates at a particular location using Get-AzsUpdate.</span></span>

## <span data-ttu-id="c4f38-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c4f38-111">EXAMPLES</span></span>

### <span data-ttu-id="c4f38-112">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c4f38-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUpdateLocation
```

<span data-ttu-id="c4f38-113">Pobierz listę lokalizacji aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="c4f38-113">Get the list of update locations.</span></span>

## <span data-ttu-id="c4f38-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c4f38-114">PARAMETERS</span></span>

### <span data-ttu-id="c4f38-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c4f38-115">-Name</span></span>
<span data-ttu-id="c4f38-116">Nazwa lokalizacji aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="c4f38-116">The name of the update location.</span></span>

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

### <span data-ttu-id="c4f38-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4f38-117">-ResourceGroupName</span></span>
<span data-ttu-id="c4f38-118">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="c4f38-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="c4f38-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4f38-119">-ResourceId</span></span>
<span data-ttu-id="c4f38-120">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="c4f38-120">The resource id.</span></span>

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

### <span data-ttu-id="c4f38-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4f38-121">CommonParameters</span></span>
<span data-ttu-id="c4f38-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4f38-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4f38-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4f38-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4f38-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c4f38-124">INPUTS</span></span>

## <span data-ttu-id="c4f38-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c4f38-125">OUTPUTS</span></span>

### <span data-ttu-id="c4f38-126">Microsoft. AzureStack. Management. Update. admin. models. UpdateLocation</span><span class="sxs-lookup"><span data-stu-id="c4f38-126">Microsoft.AzureStack.Management.Update.Admin.Models.UpdateLocation</span></span>

## <span data-ttu-id="c4f38-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c4f38-127">NOTES</span></span>

## <span data-ttu-id="c4f38-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c4f38-128">RELATED LINKS</span></span>
