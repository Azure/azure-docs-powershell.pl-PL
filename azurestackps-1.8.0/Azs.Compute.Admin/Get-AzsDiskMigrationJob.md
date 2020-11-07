---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 06f2d231754fc422115cf800ef66189378e0cd4d
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93889054"
---
# <span data-ttu-id="aeb89-101">Get-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="aeb89-101">Get-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="aeb89-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aeb89-102">SYNOPSIS</span></span>
<span data-ttu-id="aeb89-103">Zwraca listę zadań dotyczących migracji dysków zarządzanych.</span><span class="sxs-lookup"><span data-stu-id="aeb89-103">Returns the list of managed disk migration jobs.</span></span>

## <span data-ttu-id="aeb89-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aeb89-104">SYNTAX</span></span>

### <span data-ttu-id="aeb89-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="aeb89-105">List (Default)</span></span>
```
Get-AzsDiskMigrationJob [-Status <String>] [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="aeb89-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="aeb89-106">ResourceId</span></span>
```
Get-AzsDiskMigrationJob -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="aeb89-107">Pobierz</span><span class="sxs-lookup"><span data-stu-id="aeb89-107">Get</span></span>
```
Get-AzsDiskMigrationJob [-Location <String>] -Name <String> [<CommonParameters>]
```

## <span data-ttu-id="aeb89-108">Opis</span><span class="sxs-lookup"><span data-stu-id="aeb89-108">DESCRIPTION</span></span>
<span data-ttu-id="aeb89-109">Zwraca listę zadań migracji dysków.</span><span class="sxs-lookup"><span data-stu-id="aeb89-109">Returns a list of disk migration jobs.</span></span>

## <span data-ttu-id="aeb89-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aeb89-110">EXAMPLES</span></span>

### <span data-ttu-id="aeb89-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="aeb89-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
$migration = Get-AzsDiskMigrationJob -location local -Name "mymigrationName"
```

<span data-ttu-id="aeb89-112">Uzyskiwanie określonego zadania dotyczącego migracji dysków zarządzanych.</span><span class="sxs-lookup"><span data-stu-id="aeb89-112">Get a specific managed disk migration job.</span></span>

### <span data-ttu-id="aeb89-113">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="aeb89-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
$migration = Get-AzsDiskMigrationJob -location local
```

<span data-ttu-id="aeb89-114">Zwraca listę zadań zarządzanych migracji dysków w lokalizacji lokalnej.</span><span class="sxs-lookup"><span data-stu-id="aeb89-114">Returns a list of managed disk migration jobs at the location local.</span></span>

## <span data-ttu-id="aeb89-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aeb89-115">PARAMETERS</span></span>

### <span data-ttu-id="aeb89-116">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="aeb89-116">-Location</span></span>
<span data-ttu-id="aeb89-117">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="aeb89-117">Location of the resource.</span></span>

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

### <span data-ttu-id="aeb89-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="aeb89-118">-Name</span></span>
<span data-ttu-id="aeb89-119">Nazwa GUID zadania migracji.</span><span class="sxs-lookup"><span data-stu-id="aeb89-119">The migration job guid name.</span></span>

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

### <span data-ttu-id="aeb89-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aeb89-120">-ResourceId</span></span>
<span data-ttu-id="aeb89-121">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="aeb89-121">The resource id.</span></span>

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

### <span data-ttu-id="aeb89-122">-Status</span><span class="sxs-lookup"><span data-stu-id="aeb89-122">-Status</span></span>
<span data-ttu-id="aeb89-123">Parametry stanu zadania migracji dysków.</span><span class="sxs-lookup"><span data-stu-id="aeb89-123">The parameters of disk migration job status.</span></span>

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

### <span data-ttu-id="aeb89-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aeb89-124">CommonParameters</span></span>
<span data-ttu-id="aeb89-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aeb89-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aeb89-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aeb89-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aeb89-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aeb89-127">INPUTS</span></span>

## <span data-ttu-id="aeb89-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aeb89-128">OUTPUTS</span></span>

### <span data-ttu-id="aeb89-129">Microsoft. AzureStack. Management. COMPUTE. admin. models. DiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="aeb89-129">Microsoft.AzureStack.Management.Compute.Admin.Models.DiskMigrationJob</span></span>

## <span data-ttu-id="aeb89-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aeb89-130">NOTES</span></span>

## <span data-ttu-id="aeb89-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aeb89-131">RELATED LINKS</span></span>

