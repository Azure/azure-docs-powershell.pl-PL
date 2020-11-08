---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ee1a9ae5a4d5ef7545ee9a3e071fcc06475034f4
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055745"
---
# <span data-ttu-id="0639c-101">Stop-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="0639c-101">Stop-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="0639c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0639c-102">SYNOPSIS</span></span>
<span data-ttu-id="0639c-103">Anulowanie zadania zarządzanego migracji dysków.</span><span class="sxs-lookup"><span data-stu-id="0639c-103">Cancel a managed disk migration job.</span></span>

## <span data-ttu-id="0639c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0639c-104">SYNTAX</span></span>

```
Stop-AzsDiskMigrationJob [[-Location] <String>] [[-Name] <String>] [<CommonParameters>]
```

## <span data-ttu-id="0639c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0639c-105">DESCRIPTION</span></span>
<span data-ttu-id="0639c-106">Anulowanie zadania migracji dysku.</span><span class="sxs-lookup"><span data-stu-id="0639c-106">Cancel a disk migration job.</span></span>

## <span data-ttu-id="0639c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0639c-107">EXAMPLES</span></span>

### <span data-ttu-id="0639c-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0639c-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Stop-AzsDiskMigrationJob -Location local -MigrationId $migration.MigrationId
```

<span data-ttu-id="0639c-109">Anulowanie zadania zarządzanego migracji dysków.</span><span class="sxs-lookup"><span data-stu-id="0639c-109">Cancel a managed disk migration job.</span></span>

## <span data-ttu-id="0639c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0639c-110">PARAMETERS</span></span>

### <span data-ttu-id="0639c-111">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="0639c-111">-Location</span></span>
<span data-ttu-id="0639c-112">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="0639c-112">Location of the resource.</span></span>

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

### <span data-ttu-id="0639c-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0639c-113">-Name</span></span>
<span data-ttu-id="0639c-114">Nazwa GUID zadania migracji.</span><span class="sxs-lookup"><span data-stu-id="0639c-114">The migration job guid name.</span></span>

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

### <span data-ttu-id="0639c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0639c-115">CommonParameters</span></span>
<span data-ttu-id="0639c-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0639c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0639c-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0639c-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0639c-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0639c-118">INPUTS</span></span>

## <span data-ttu-id="0639c-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0639c-119">OUTPUTS</span></span>

### <span data-ttu-id="0639c-120">Microsoft. AzureStack. Management. COMPUTE. admin. models. DiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="0639c-120">Microsoft.AzureStack.Management.Compute.Admin.Models.DiskMigrationJob</span></span>

## <span data-ttu-id="0639c-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0639c-121">NOTES</span></span>

## <span data-ttu-id="0639c-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0639c-122">RELATED LINKS</span></span>

