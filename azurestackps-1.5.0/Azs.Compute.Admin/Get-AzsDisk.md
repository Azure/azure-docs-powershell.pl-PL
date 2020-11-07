---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e4c464d2d0e822b745acc2a7c6daecf329449105
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523169"
---
# <span data-ttu-id="2638b-101">Get-AzsDisk</span><span class="sxs-lookup"><span data-stu-id="2638b-101">Get-AzsDisk</span></span>

## <span data-ttu-id="2638b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2638b-102">SYNOPSIS</span></span>
<span data-ttu-id="2638b-103">Zwraca listę zarządzanych dysków, które można migrować w określonym udziale.</span><span class="sxs-lookup"><span data-stu-id="2638b-103">Returns the list of managed disks which can be migrated in the specified share.</span></span>

## <span data-ttu-id="2638b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2638b-104">SYNTAX</span></span>

### <span data-ttu-id="2638b-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="2638b-105">List (Default)</span></span>
```
Get-AzsDisk [-Location <String>] [-Start <Int32>] [-SharePath <String>] [-Count <Int32>]
 [-UserSubscriptionId <String>] [-Status <String>] [<CommonParameters>]
```

### <span data-ttu-id="2638b-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="2638b-106">ResourceId</span></span>
```
Get-AzsDisk -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="2638b-107">Pobierz</span><span class="sxs-lookup"><span data-stu-id="2638b-107">Get</span></span>
```
Get-AzsDisk [-Location <String>] -Name <String> [<CommonParameters>]
```

## <span data-ttu-id="2638b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2638b-108">DESCRIPTION</span></span>
<span data-ttu-id="2638b-109">Zwraca listę dysków.</span><span class="sxs-lookup"><span data-stu-id="2638b-109">Returns a list of disks.</span></span>

## <span data-ttu-id="2638b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2638b-110">EXAMPLES</span></span>

### <span data-ttu-id="2638b-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2638b-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
$disks = Get-AzsDisk -location local
```

<span data-ttu-id="2638b-112">Zwraca listę dysków zarządzanych w lokalizacji lokalnej.</span><span class="sxs-lookup"><span data-stu-id="2638b-112">Returns a list of managed disks at the location local.</span></span>
<span data-ttu-id="2638b-113">Domyślnie będzie to pierwsze 100 dysków</span><span class="sxs-lookup"><span data-stu-id="2638b-113">By default, it will the first 100 disks</span></span>

### <span data-ttu-id="2638b-114">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="2638b-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
$disk = Get-AzsDisk -location local -name $DiskId
```

<span data-ttu-id="2638b-115">Uzyskiwanie określonego zarządzanego dysku.</span><span class="sxs-lookup"><span data-stu-id="2638b-115">Get a specific managed disk.</span></span>

## <span data-ttu-id="2638b-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2638b-116">PARAMETERS</span></span>

### <span data-ttu-id="2638b-117">-Count</span><span class="sxs-lookup"><span data-stu-id="2638b-117">-Count</span></span>
<span data-ttu-id="2638b-118">Maksymalna liczba dysków, które mają zostać zwrócone.</span><span class="sxs-lookup"><span data-stu-id="2638b-118">The maximum number of disks to return.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2638b-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="2638b-119">-Location</span></span>
<span data-ttu-id="2638b-120">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="2638b-120">Location of the resource.</span></span>

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

### <span data-ttu-id="2638b-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2638b-121">-Name</span></span>
<span data-ttu-id="2638b-122">Identyfikator GUID dysku jako tożsamość.</span><span class="sxs-lookup"><span data-stu-id="2638b-122">The disk guid as identity.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: DiskId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2638b-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2638b-123">-ResourceId</span></span>
<span data-ttu-id="2638b-124">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="2638b-124">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2638b-125">-SharePath</span><span class="sxs-lookup"><span data-stu-id="2638b-125">-SharePath</span></span>
<span data-ttu-id="2638b-126">Udział źródłowy, do którego należy zasób.</span><span class="sxs-lookup"><span data-stu-id="2638b-126">The source share which the resource belongs to.</span></span>

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

### <span data-ttu-id="2638b-127">-Start</span><span class="sxs-lookup"><span data-stu-id="2638b-127">-Start</span></span>
<span data-ttu-id="2638b-128">Indeks początkowy dysków w zapytaniu.</span><span class="sxs-lookup"><span data-stu-id="2638b-128">The start index of disks in query.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2638b-129">-Status</span><span class="sxs-lookup"><span data-stu-id="2638b-129">-Status</span></span>
<span data-ttu-id="2638b-130">Parametry stanu dysku.</span><span class="sxs-lookup"><span data-stu-id="2638b-130">The parameters of disk state.</span></span>

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

### <span data-ttu-id="2638b-131">-UserSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2638b-131">-UserSubscriptionId</span></span>
<span data-ttu-id="2638b-132">Identyfikator subskrypcji dzierżawy, do której należy zasób.</span><span class="sxs-lookup"><span data-stu-id="2638b-132">Tenant Subscription Id which the resource belongs to.</span></span>

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

### <span data-ttu-id="2638b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2638b-133">CommonParameters</span></span>
<span data-ttu-id="2638b-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2638b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2638b-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2638b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2638b-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2638b-136">INPUTS</span></span>

## <span data-ttu-id="2638b-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2638b-137">OUTPUTS</span></span>

### <span data-ttu-id="2638b-138">Microsoft. AzureStack. Management. COMPUTE. admin. modele. dysk</span><span class="sxs-lookup"><span data-stu-id="2638b-138">Microsoft.AzureStack.Management.Compute.Admin.Models.Disk</span></span>

## <span data-ttu-id="2638b-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2638b-139">NOTES</span></span>

## <span data-ttu-id="2638b-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2638b-140">RELATED LINKS</span></span>
