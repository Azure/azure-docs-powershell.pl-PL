---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: db6eff0b0b0e0698c42dd7905cd3e5f7879345e1
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055754"
---
# <span data-ttu-id="ca70f-101">New-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="ca70f-101">New-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="ca70f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ca70f-102">SYNOPSIS</span></span>
<span data-ttu-id="ca70f-103">Rozpoczyna zadanie migracji dysków zarządzanych w celu migrowania zarządzanych dysków do określonego udziału docelowego.</span><span class="sxs-lookup"><span data-stu-id="ca70f-103">Starts a managed disk migration job to migrate managed disks to the specified destination share.</span></span>

## <span data-ttu-id="ca70f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ca70f-104">SYNTAX</span></span>

```
New-AzsDiskMigrationJob [-Disks] <Disk[]> [-TargetShare] <String> [[-Location] <String>] [-Name] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="ca70f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ca70f-105">DESCRIPTION</span></span>
<span data-ttu-id="ca70f-106">Tworzenie zadania migracji dysku.</span><span class="sxs-lookup"><span data-stu-id="ca70f-106">Create a disk migration job.</span></span>

## <span data-ttu-id="ca70f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ca70f-107">EXAMPLES</span></span>

### <span data-ttu-id="ca70f-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ca70f-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsDiskMigrationJob -Name "MyMigrationJob" -Disks $disks -location local -TargetShare "\\SU1FileServer.azurestack.local\SU1_ObjStore"
```

<span data-ttu-id="ca70f-109">Rozpoczynanie zadania migracji dysków zarządzanych dla pierwszych 20 dysków</span><span class="sxs-lookup"><span data-stu-id="ca70f-109">Start a managed disk migration job for the first 20 disks</span></span>

## <span data-ttu-id="ca70f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ca70f-110">PARAMETERS</span></span>

### <span data-ttu-id="ca70f-111">-Dyski</span><span class="sxs-lookup"><span data-stu-id="ca70f-111">-Disks</span></span>
<span data-ttu-id="ca70f-112">Parametry listy dysków.</span><span class="sxs-lookup"><span data-stu-id="ca70f-112">The parameters of disk list.</span></span>

```yaml
Type: Disk[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca70f-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ca70f-113">-Location</span></span>
<span data-ttu-id="ca70f-114">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="ca70f-114">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca70f-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ca70f-115">-Name</span></span>
<span data-ttu-id="ca70f-116">Nazwa GUID zadania migracji.</span><span class="sxs-lookup"><span data-stu-id="ca70f-116">The migration job guid name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: MigrationId

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca70f-117">-TargetShare</span><span class="sxs-lookup"><span data-stu-id="ca70f-117">-TargetShare</span></span>
<span data-ttu-id="ca70f-118">Nazwa udziału docelowego.</span><span class="sxs-lookup"><span data-stu-id="ca70f-118">The target share name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca70f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca70f-119">CommonParameters</span></span>
<span data-ttu-id="ca70f-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca70f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca70f-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca70f-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca70f-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ca70f-122">INPUTS</span></span>

## <span data-ttu-id="ca70f-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ca70f-123">OUTPUTS</span></span>

### <span data-ttu-id="ca70f-124">Microsoft. AzureStack. Management. COMPUTE. admin. models. DiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="ca70f-124">Microsoft.AzureStack.Management.Compute.Admin.Models.DiskMigrationJob</span></span>

## <span data-ttu-id="ca70f-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ca70f-125">NOTES</span></span>

## <span data-ttu-id="ca70f-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ca70f-126">RELATED LINKS</span></span>

