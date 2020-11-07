---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2cf36bf232ae48891b28562313fa2063e14a2be8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93887557"
---
# <span data-ttu-id="36d25-101">Get-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="36d25-101">Get-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="36d25-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="36d25-102">SYNOPSIS</span></span>
<span data-ttu-id="36d25-103">Zwraca listę zadań dotyczących migracji dysków zarządzanych.</span><span class="sxs-lookup"><span data-stu-id="36d25-103">Returns the list of managed disk migration jobs.</span></span>

## <span data-ttu-id="36d25-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="36d25-104">SYNTAX</span></span>

### <span data-ttu-id="36d25-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="36d25-105">List (Default)</span></span>
```
Get-AzsDiskMigrationJob [-Status <String>] [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="36d25-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="36d25-106">ResourceId</span></span>
```
Get-AzsDiskMigrationJob -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="36d25-107">Pobierz</span><span class="sxs-lookup"><span data-stu-id="36d25-107">Get</span></span>
```
Get-AzsDiskMigrationJob [-Location <String>] -Name <String> [<CommonParameters>]
```

## <span data-ttu-id="36d25-108">Opis</span><span class="sxs-lookup"><span data-stu-id="36d25-108">DESCRIPTION</span></span>
<span data-ttu-id="36d25-109">Zwraca listę zadań migracji dysków.</span><span class="sxs-lookup"><span data-stu-id="36d25-109">Returns a list of disk migration jobs.</span></span>

## <span data-ttu-id="36d25-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="36d25-110">EXAMPLES</span></span>

### <span data-ttu-id="36d25-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="36d25-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
$migration = Get-AzsDiskMigrationJob -location local -Name "mymigrationName"
```

<span data-ttu-id="36d25-112">Uzyskiwanie określonego zadania dotyczącego migracji dysków zarządzanych.</span><span class="sxs-lookup"><span data-stu-id="36d25-112">Get a specific managed disk migration job.</span></span>

### <span data-ttu-id="36d25-113">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="36d25-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
$migration = Get-AzsDiskMigrationJob -location local
```

<span data-ttu-id="36d25-114">Zwraca listę zadań zarządzanych migracji dysków w lokalizacji lokalnej.</span><span class="sxs-lookup"><span data-stu-id="36d25-114">Returns a list of managed disk migration jobs at the location local.</span></span>

## <span data-ttu-id="36d25-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="36d25-115">PARAMETERS</span></span>

### <span data-ttu-id="36d25-116">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="36d25-116">-Location</span></span>
<span data-ttu-id="36d25-117">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="36d25-117">Location of the resource.</span></span>

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

### <span data-ttu-id="36d25-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="36d25-118">-Name</span></span>
<span data-ttu-id="36d25-119">Nazwa GUID zadania migracji.</span><span class="sxs-lookup"><span data-stu-id="36d25-119">The migration job guid name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: MigrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36d25-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="36d25-120">-ResourceId</span></span>
<span data-ttu-id="36d25-121">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="36d25-121">The resource id.</span></span>

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

### <span data-ttu-id="36d25-122">-Status</span><span class="sxs-lookup"><span data-stu-id="36d25-122">-Status</span></span>
<span data-ttu-id="36d25-123">Parametry stanu zadania migracji dysków.</span><span class="sxs-lookup"><span data-stu-id="36d25-123">The parameters of disk migration job status.</span></span>

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

### <span data-ttu-id="36d25-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36d25-124">CommonParameters</span></span>
<span data-ttu-id="36d25-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36d25-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36d25-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36d25-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36d25-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="36d25-127">INPUTS</span></span>

## <span data-ttu-id="36d25-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="36d25-128">OUTPUTS</span></span>

### <span data-ttu-id="36d25-129">Microsoft. AzureStack. Management. COMPUTE. admin. models. DiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="36d25-129">Microsoft.AzureStack.Management.Compute.Admin.Models.DiskMigrationJob</span></span>

## <span data-ttu-id="36d25-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="36d25-130">NOTES</span></span>

## <span data-ttu-id="36d25-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="36d25-131">RELATED LINKS</span></span>

