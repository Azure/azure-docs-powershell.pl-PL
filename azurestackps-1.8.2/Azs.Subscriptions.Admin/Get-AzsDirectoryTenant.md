---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: eff689d36268f7eaec045c05c00d4fd18e91a026
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055939"
---
# <span data-ttu-id="25a71-101">Get-AzsDirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="25a71-101">Get-AzsDirectoryTenant</span></span>

## <span data-ttu-id="25a71-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="25a71-102">SYNOPSIS</span></span>
<span data-ttu-id="25a71-103">Wyświetla listę wszystkich dzierżawców w katalogu w ramach bieżącego abonamentu i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="25a71-103">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="25a71-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="25a71-104">SYNTAX</span></span>

### <span data-ttu-id="25a71-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="25a71-105">List (Default)</span></span>
```
Get-AzsDirectoryTenant [-ResourceGroupName <String>] [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="25a71-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="25a71-106">Get</span></span>
```
Get-AzsDirectoryTenant -Name <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="25a71-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="25a71-107">ResourceId</span></span>
```
Get-AzsDirectoryTenant -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="25a71-108">Opis</span><span class="sxs-lookup"><span data-stu-id="25a71-108">DESCRIPTION</span></span>
<span data-ttu-id="25a71-109">Wyświetla listę wszystkich dzierżawców w katalogu w ramach bieżącego abonamentu i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="25a71-109">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="25a71-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="25a71-110">EXAMPLES</span></span>

### <span data-ttu-id="25a71-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="25a71-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDirectoryTenant -ResourceGroupName "System.Local"
```

<span data-ttu-id="25a71-112">Wyświetla listę wszystkich dzierżawców w katalogu w ramach bieżącego abonamentu i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="25a71-112">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="25a71-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="25a71-113">PARAMETERS</span></span>

### <span data-ttu-id="25a71-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="25a71-114">-Name</span></span>
<span data-ttu-id="25a71-115">Nazwa dzierżawy katalogu.</span><span class="sxs-lookup"><span data-stu-id="25a71-115">Directory tenant name.</span></span>

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

### <span data-ttu-id="25a71-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25a71-116">-ResourceGroupName</span></span>
<span data-ttu-id="25a71-117">{{Fill ResourceGroupName Description}}</span><span class="sxs-lookup"><span data-stu-id="25a71-117">{{Fill ResourceGroupName Description}}</span></span>

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

### <span data-ttu-id="25a71-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25a71-118">-ResourceId</span></span>
<span data-ttu-id="25a71-119">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="25a71-119">The resource id.</span></span>

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

### <span data-ttu-id="25a71-120">-Skip</span><span class="sxs-lookup"><span data-stu-id="25a71-120">-Skip</span></span>
<span data-ttu-id="25a71-121">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="25a71-121">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="25a71-122">-Początek</span><span class="sxs-lookup"><span data-stu-id="25a71-122">-Top</span></span>
<span data-ttu-id="25a71-123">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="25a71-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="25a71-124">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="25a71-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="25a71-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25a71-125">CommonParameters</span></span>
<span data-ttu-id="25a71-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25a71-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25a71-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25a71-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25a71-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="25a71-128">INPUTS</span></span>

## <span data-ttu-id="25a71-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="25a71-129">OUTPUTS</span></span>

### <span data-ttu-id="25a71-130">Microsoft. AzureStack. Management. Subscriptions. admin. models. DirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="25a71-130">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.DirectoryTenant</span></span>

## <span data-ttu-id="25a71-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="25a71-131">NOTES</span></span>

## <span data-ttu-id="25a71-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="25a71-132">RELATED LINKS</span></span>

