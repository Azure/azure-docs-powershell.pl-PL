---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a2b639a09789960393ac26d035a80157069dbaaa
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93889062"
---
# <span data-ttu-id="29e07-101">Get-AzsDisk</span><span class="sxs-lookup"><span data-stu-id="29e07-101">Get-AzsDisk</span></span>

## <span data-ttu-id="29e07-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="29e07-102">SYNOPSIS</span></span>
<span data-ttu-id="29e07-103">Zwraca listę zarządzanych dysków, które można migrować w określonym udziale.</span><span class="sxs-lookup"><span data-stu-id="29e07-103">Returns the list of managed disks which can be migrated in the specified share.</span></span>

## <span data-ttu-id="29e07-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="29e07-104">SYNTAX</span></span>

### <span data-ttu-id="29e07-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="29e07-105">List (Default)</span></span>
```
Get-AzsDisk [-Location <String>] [-Start <Int32>] [-SharePath <String>] [-Count <Int32>]
 [-UserSubscriptionId <String>] [-Status <String>] [<CommonParameters>]
```

### <span data-ttu-id="29e07-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="29e07-106">ResourceId</span></span>
```
Get-AzsDisk -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="29e07-107">Pobierz</span><span class="sxs-lookup"><span data-stu-id="29e07-107">Get</span></span>
```
Get-AzsDisk [-Location <String>] -Name <String> [<CommonParameters>]
```

## <span data-ttu-id="29e07-108">Opis</span><span class="sxs-lookup"><span data-stu-id="29e07-108">DESCRIPTION</span></span>
<span data-ttu-id="29e07-109">Zwraca listę dysków.</span><span class="sxs-lookup"><span data-stu-id="29e07-109">Returns a list of disks.</span></span>

## <span data-ttu-id="29e07-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="29e07-110">EXAMPLES</span></span>

### <span data-ttu-id="29e07-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="29e07-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
$disks = Get-AzsDisk -location local
```

<span data-ttu-id="29e07-112">Zwraca listę dysków zarządzanych w lokalizacji lokalnej.</span><span class="sxs-lookup"><span data-stu-id="29e07-112">Returns a list of managed disks at the location local.</span></span>
<span data-ttu-id="29e07-113">Domyślnie będzie to pierwsze 100 dysków</span><span class="sxs-lookup"><span data-stu-id="29e07-113">By default, it will the first 100 disks</span></span>

### <span data-ttu-id="29e07-114">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="29e07-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
$disk = Get-AzsDisk -location local -name $DiskId
```

<span data-ttu-id="29e07-115">Uzyskiwanie określonego zarządzanego dysku.</span><span class="sxs-lookup"><span data-stu-id="29e07-115">Get a specific managed disk.</span></span>

## <span data-ttu-id="29e07-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="29e07-116">PARAMETERS</span></span>

### <span data-ttu-id="29e07-117">-Count</span><span class="sxs-lookup"><span data-stu-id="29e07-117">-Count</span></span>
<span data-ttu-id="29e07-118">Maksymalna liczba dysków, które mają zostać zwrócone.</span><span class="sxs-lookup"><span data-stu-id="29e07-118">The maximum number of disks to return.</span></span>

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

### <span data-ttu-id="29e07-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="29e07-119">-Location</span></span>
<span data-ttu-id="29e07-120">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="29e07-120">Location of the resource.</span></span>

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

### <span data-ttu-id="29e07-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="29e07-121">-Name</span></span>
<span data-ttu-id="29e07-122">Identyfikator GUID dysku jako tożsamość.</span><span class="sxs-lookup"><span data-stu-id="29e07-122">The disk guid as identity.</span></span>

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

### <span data-ttu-id="29e07-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="29e07-123">-ResourceId</span></span>
<span data-ttu-id="29e07-124">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="29e07-124">The resource id.</span></span>

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

### <span data-ttu-id="29e07-125">-SharePath</span><span class="sxs-lookup"><span data-stu-id="29e07-125">-SharePath</span></span>
<span data-ttu-id="29e07-126">Udział źródłowy, do którego należy zasób.</span><span class="sxs-lookup"><span data-stu-id="29e07-126">The source share which the resource belongs to.</span></span>

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

### <span data-ttu-id="29e07-127">-Start</span><span class="sxs-lookup"><span data-stu-id="29e07-127">-Start</span></span>
<span data-ttu-id="29e07-128">Indeks początkowy dysków w zapytaniu.</span><span class="sxs-lookup"><span data-stu-id="29e07-128">The start index of disks in query.</span></span>

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

### <span data-ttu-id="29e07-129">-Status</span><span class="sxs-lookup"><span data-stu-id="29e07-129">-Status</span></span>
<span data-ttu-id="29e07-130">Parametry stanu dysku.</span><span class="sxs-lookup"><span data-stu-id="29e07-130">The parameters of disk state.</span></span>

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

### <span data-ttu-id="29e07-131">-UserSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="29e07-131">-UserSubscriptionId</span></span>
<span data-ttu-id="29e07-132">Identyfikator subskrypcji dzierżawy, do której należy zasób.</span><span class="sxs-lookup"><span data-stu-id="29e07-132">Tenant Subscription Id which the resource belongs to.</span></span>

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

### <span data-ttu-id="29e07-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29e07-133">CommonParameters</span></span>
<span data-ttu-id="29e07-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29e07-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29e07-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29e07-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29e07-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="29e07-136">INPUTS</span></span>

## <span data-ttu-id="29e07-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="29e07-137">OUTPUTS</span></span>

### <span data-ttu-id="29e07-138">Microsoft. AzureStack. Management. COMPUTE. admin. modele. dysk</span><span class="sxs-lookup"><span data-stu-id="29e07-138">Microsoft.AzureStack.Management.Compute.Admin.Models.Disk</span></span>

## <span data-ttu-id="29e07-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="29e07-139">NOTES</span></span>

## <span data-ttu-id="29e07-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="29e07-140">RELATED LINKS</span></span>

