---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: eff689d36268f7eaec045c05c00d4fd18e91a026
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93889589"
---
# <span data-ttu-id="76618-101">Get-AzsDirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="76618-101">Get-AzsDirectoryTenant</span></span>

## <span data-ttu-id="76618-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="76618-102">SYNOPSIS</span></span>
<span data-ttu-id="76618-103">Wyświetla listę wszystkich dzierżawców w katalogu w ramach bieżącego abonamentu i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="76618-103">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="76618-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="76618-104">SYNTAX</span></span>

### <span data-ttu-id="76618-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="76618-105">List (Default)</span></span>
```
Get-AzsDirectoryTenant [-ResourceGroupName <String>] [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="76618-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="76618-106">Get</span></span>
```
Get-AzsDirectoryTenant -Name <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="76618-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="76618-107">ResourceId</span></span>
```
Get-AzsDirectoryTenant -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="76618-108">Opis</span><span class="sxs-lookup"><span data-stu-id="76618-108">DESCRIPTION</span></span>
<span data-ttu-id="76618-109">Wyświetla listę wszystkich dzierżawców w katalogu w ramach bieżącego abonamentu i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="76618-109">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="76618-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="76618-110">EXAMPLES</span></span>

### <span data-ttu-id="76618-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="76618-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDirectoryTenant -ResourceGroupName "System.Local"
```

<span data-ttu-id="76618-112">Wyświetla listę wszystkich dzierżawców w katalogu w ramach bieżącego abonamentu i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="76618-112">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="76618-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="76618-113">PARAMETERS</span></span>

### <span data-ttu-id="76618-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="76618-114">-Name</span></span>
<span data-ttu-id="76618-115">Nazwa dzierżawy katalogu.</span><span class="sxs-lookup"><span data-stu-id="76618-115">Directory tenant name.</span></span>

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

### <span data-ttu-id="76618-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76618-116">-ResourceGroupName</span></span>
<span data-ttu-id="76618-117">{{Fill ResourceGroupName Description}}</span><span class="sxs-lookup"><span data-stu-id="76618-117">{{Fill ResourceGroupName Description}}</span></span>

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

### <span data-ttu-id="76618-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="76618-118">-ResourceId</span></span>
<span data-ttu-id="76618-119">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="76618-119">The resource id.</span></span>

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

### <span data-ttu-id="76618-120">-Skip</span><span class="sxs-lookup"><span data-stu-id="76618-120">-Skip</span></span>
<span data-ttu-id="76618-121">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="76618-121">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="76618-122">-Początek</span><span class="sxs-lookup"><span data-stu-id="76618-122">-Top</span></span>
<span data-ttu-id="76618-123">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="76618-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="76618-124">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="76618-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="76618-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76618-125">CommonParameters</span></span>
<span data-ttu-id="76618-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76618-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76618-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76618-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76618-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="76618-128">INPUTS</span></span>

## <span data-ttu-id="76618-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="76618-129">OUTPUTS</span></span>

### <span data-ttu-id="76618-130">Microsoft. AzureStack. Management. Subscriptions. admin. models. DirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="76618-130">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.DirectoryTenant</span></span>

## <span data-ttu-id="76618-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="76618-131">NOTES</span></span>

## <span data-ttu-id="76618-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="76618-132">RELATED LINKS</span></span>

