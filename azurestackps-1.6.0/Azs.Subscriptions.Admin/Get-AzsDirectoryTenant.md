---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3ae30d06970d9533c32c96f33a1917fa8d2a6e41
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523033"
---
# <span data-ttu-id="70b76-101">Get-AzsDirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="70b76-101">Get-AzsDirectoryTenant</span></span>

## <span data-ttu-id="70b76-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="70b76-102">SYNOPSIS</span></span>
<span data-ttu-id="70b76-103">Wyświetla listę wszystkich dzierżawców w katalogu w ramach bieżącego abonamentu i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="70b76-103">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="70b76-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="70b76-104">SYNTAX</span></span>

### <span data-ttu-id="70b76-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="70b76-105">List (Default)</span></span>
```
Get-AzsDirectoryTenant [-ResourceGroupName <String>] [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="70b76-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="70b76-106">Get</span></span>
```
Get-AzsDirectoryTenant -Name <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="70b76-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="70b76-107">ResourceId</span></span>
```
Get-AzsDirectoryTenant -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="70b76-108">Opis</span><span class="sxs-lookup"><span data-stu-id="70b76-108">DESCRIPTION</span></span>
<span data-ttu-id="70b76-109">Wyświetla listę wszystkich dzierżawców w katalogu w ramach bieżącego abonamentu i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="70b76-109">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="70b76-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="70b76-110">EXAMPLES</span></span>

### <span data-ttu-id="70b76-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="70b76-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDirectoryTenant -ResourceGroupName "System.Local"
```

<span data-ttu-id="70b76-112">Wyświetla listę wszystkich dzierżawców w katalogu w ramach bieżącego abonamentu i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="70b76-112">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="70b76-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="70b76-113">PARAMETERS</span></span>

### <span data-ttu-id="70b76-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="70b76-114">-Name</span></span>
<span data-ttu-id="70b76-115">Nazwa dzierżawy katalogu.</span><span class="sxs-lookup"><span data-stu-id="70b76-115">Directory tenant name.</span></span>

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

### <span data-ttu-id="70b76-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70b76-116">-ResourceGroupName</span></span>
<span data-ttu-id="70b76-117">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="70b76-117">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="70b76-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="70b76-118">-ResourceId</span></span>
<span data-ttu-id="70b76-119">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="70b76-119">The resource id.</span></span>

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

### <span data-ttu-id="70b76-120">-Skip</span><span class="sxs-lookup"><span data-stu-id="70b76-120">-Skip</span></span>
<span data-ttu-id="70b76-121">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="70b76-121">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="70b76-122">-Początek</span><span class="sxs-lookup"><span data-stu-id="70b76-122">-Top</span></span>
<span data-ttu-id="70b76-123">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="70b76-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="70b76-124">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="70b76-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="70b76-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70b76-125">CommonParameters</span></span>
<span data-ttu-id="70b76-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70b76-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70b76-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70b76-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70b76-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="70b76-128">INPUTS</span></span>

## <span data-ttu-id="70b76-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="70b76-129">OUTPUTS</span></span>

### <span data-ttu-id="70b76-130">Microsoft. AzureStack. Management. Subscriptions. admin. models. DirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="70b76-130">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.DirectoryTenant</span></span>

## <span data-ttu-id="70b76-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="70b76-131">NOTES</span></span>

## <span data-ttu-id="70b76-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="70b76-132">RELATED LINKS</span></span>

