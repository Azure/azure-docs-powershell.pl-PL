---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d38e4bd949a6118f55ce0096a8ca56d08137bb2a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523705"
---
# <span data-ttu-id="23802-101">Stop-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="23802-101">Stop-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="23802-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="23802-102">SYNOPSIS</span></span>
<span data-ttu-id="23802-103">Anulowanie zadania zarządzanego migracji dysków.</span><span class="sxs-lookup"><span data-stu-id="23802-103">Cancel a managed disk migration job.</span></span>

## <span data-ttu-id="23802-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="23802-104">SYNTAX</span></span>

```
Stop-AzsDiskMigrationJob [[-Location] <String>] [[-Name] <String>] [<CommonParameters>]
```

## <span data-ttu-id="23802-105">Opis</span><span class="sxs-lookup"><span data-stu-id="23802-105">DESCRIPTION</span></span>
<span data-ttu-id="23802-106">Anulowanie zadania migracji dysku.</span><span class="sxs-lookup"><span data-stu-id="23802-106">Cancel a disk migration job.</span></span>

## <span data-ttu-id="23802-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="23802-107">EXAMPLES</span></span>

### <span data-ttu-id="23802-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="23802-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Stop-AzsDiskMigrationJob -Location local -MigrationId $migration.MigrationId
```

<span data-ttu-id="23802-109">Anulowanie zadania zarządzanego migracji dysków.</span><span class="sxs-lookup"><span data-stu-id="23802-109">Cancel a managed disk migration job.</span></span>

## <span data-ttu-id="23802-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="23802-110">PARAMETERS</span></span>

### <span data-ttu-id="23802-111">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="23802-111">-Location</span></span>
<span data-ttu-id="23802-112">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="23802-112">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23802-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="23802-113">-Name</span></span>
<span data-ttu-id="23802-114">Nazwa GUID zadania migracji.</span><span class="sxs-lookup"><span data-stu-id="23802-114">The migration job guid name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: MigrationId

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23802-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23802-115">CommonParameters</span></span>
<span data-ttu-id="23802-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23802-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23802-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23802-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23802-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="23802-118">INPUTS</span></span>

## <span data-ttu-id="23802-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="23802-119">OUTPUTS</span></span>

### <span data-ttu-id="23802-120">Microsoft. AzureStack. Management. COMPUTE. admin. models. DiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="23802-120">Microsoft.AzureStack.Management.Compute.Admin.Models.DiskMigrationJob</span></span>

## <span data-ttu-id="23802-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="23802-121">NOTES</span></span>

## <span data-ttu-id="23802-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="23802-122">RELATED LINKS</span></span>

