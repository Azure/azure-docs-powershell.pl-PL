---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c5fe6e28ff87cfd3f365441d0e09f09ef21dc454
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93888978"
---
# <span data-ttu-id="75347-101">Get-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="75347-101">Get-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="75347-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="75347-102">SYNOPSIS</span></span>
<span data-ttu-id="75347-103">Zwraca listę wszystkich wystąpień ról infrastruktury w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="75347-103">Returns a list of all infrastructure role instances at a location.</span></span>

## <span data-ttu-id="75347-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="75347-104">SYNTAX</span></span>

### <span data-ttu-id="75347-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="75347-105">List (Default)</span></span>
```
Get-AzsInfrastructureRoleInstance [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>]
 [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="75347-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="75347-106">Get</span></span>
```
Get-AzsInfrastructureRoleInstance [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="75347-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="75347-107">ResourceId</span></span>
```
Get-AzsInfrastructureRoleInstance -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="75347-108">Opis</span><span class="sxs-lookup"><span data-stu-id="75347-108">DESCRIPTION</span></span>
<span data-ttu-id="75347-109">Zwraca listę wszystkich wystąpień ról infrastruktury w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="75347-109">Returns a list of all infrastructure role instances at a location.</span></span>

## <span data-ttu-id="75347-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="75347-110">EXAMPLES</span></span>

### <span data-ttu-id="75347-111">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="75347-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureRoleInstance
```

<span data-ttu-id="75347-112">Zwraca listę wszystkich wystąpień ról infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="75347-112">Return a list of all infrastructure role instances.</span></span>

### <span data-ttu-id="75347-113">PRZYKŁAD 2</span><span class="sxs-lookup"><span data-stu-id="75347-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="75347-114">Zwracanie pojedynczego wystąpienia roli infrastruktury na podstawie nazwy.</span><span class="sxs-lookup"><span data-stu-id="75347-114">Return a single infrastructure role instance based on name.</span></span>

## <span data-ttu-id="75347-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="75347-115">PARAMETERS</span></span>

### <span data-ttu-id="75347-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="75347-116">-Name</span></span>
<span data-ttu-id="75347-117">Nazwa wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="75347-117">Name of an infrastructure role instance.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75347-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="75347-118">-Location</span></span>
<span data-ttu-id="75347-119">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="75347-119">Location of the resource.</span></span>

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

### <span data-ttu-id="75347-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75347-120">-ResourceGroupName</span></span>
<span data-ttu-id="75347-121">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="75347-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="75347-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75347-122">-ResourceId</span></span>
<span data-ttu-id="75347-123">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="75347-123">The resource id.</span></span>

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

### <span data-ttu-id="75347-124">-Filter</span><span class="sxs-lookup"><span data-stu-id="75347-124">-Filter</span></span>
<span data-ttu-id="75347-125">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="75347-125">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75347-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="75347-126">-Skip</span></span>
<span data-ttu-id="75347-127">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="75347-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="75347-128">-Początek</span><span class="sxs-lookup"><span data-stu-id="75347-128">-Top</span></span>
<span data-ttu-id="75347-129">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="75347-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="75347-130">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="75347-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="75347-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75347-131">CommonParameters</span></span>
<span data-ttu-id="75347-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75347-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75347-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75347-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75347-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="75347-134">INPUTS</span></span>

## <span data-ttu-id="75347-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="75347-135">OUTPUTS</span></span>

### <span data-ttu-id="75347-136">Microsoft. AzureStack. Management. Fabric. admin. models. InfraRoleInstance</span><span class="sxs-lookup"><span data-stu-id="75347-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.InfraRoleInstance</span></span>

## <span data-ttu-id="75347-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="75347-137">NOTES</span></span>

## <span data-ttu-id="75347-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="75347-138">RELATED LINKS</span></span>
