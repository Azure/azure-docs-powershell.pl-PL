---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b37d41ae2ec772cc755436bc01c3c4009c9c30f5
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93889038"
---
# <span data-ttu-id="4ed11-101">New-DataDiskObject</span><span class="sxs-lookup"><span data-stu-id="4ed11-101">New-DataDiskObject</span></span>

## <span data-ttu-id="4ed11-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4ed11-102">SYNOPSIS</span></span>
<span data-ttu-id="4ed11-103">Tworzy dysk danych, który służy do tworzenia nowego obrazu platformy maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4ed11-103">Creates a data disk which is used to create a new virtual machine platform image.</span></span>

## <span data-ttu-id="4ed11-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4ed11-104">SYNTAX</span></span>

```
New-DataDiskObject [[-Lun] <Int32>] [[-Uri] <String>] [<CommonParameters>]
```

## <span data-ttu-id="4ed11-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4ed11-105">DESCRIPTION</span></span>
<span data-ttu-id="4ed11-106">Tworzy obiekt przechowujący informacje o dysku danych.</span><span class="sxs-lookup"><span data-stu-id="4ed11-106">Creates an object holding information about a data disk.</span></span>

## <span data-ttu-id="4ed11-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4ed11-107">EXAMPLES</span></span>

### <span data-ttu-id="4ed11-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="4ed11-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-DataDiskObject -Lun 5 -URI test.blob.windows.net/disks/datadisk5.vhd
```

<span data-ttu-id="4ed11-109">Utwórz nowy obiekt dysku danych.</span><span class="sxs-lookup"><span data-stu-id="4ed11-109">Create a new data disk object.</span></span>

## <span data-ttu-id="4ed11-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4ed11-110">PARAMETERS</span></span>

### <span data-ttu-id="4ed11-111">-LUN</span><span class="sxs-lookup"><span data-stu-id="4ed11-111">-Lun</span></span>
<span data-ttu-id="4ed11-112">Numer jednostki logicznej.</span><span class="sxs-lookup"><span data-stu-id="4ed11-112">Logical unit number.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ed11-113">-URI</span><span class="sxs-lookup"><span data-stu-id="4ed11-113">-Uri</span></span>
<span data-ttu-id="4ed11-114">Lokalizacja szablonu dysku.</span><span class="sxs-lookup"><span data-stu-id="4ed11-114">Location of the disk template.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ed11-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ed11-115">CommonParameters</span></span>
<span data-ttu-id="4ed11-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ed11-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ed11-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ed11-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ed11-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4ed11-118">INPUTS</span></span>

## <span data-ttu-id="4ed11-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4ed11-119">OUTPUTS</span></span>

## <span data-ttu-id="4ed11-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4ed11-120">NOTES</span></span>

## <span data-ttu-id="4ed11-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4ed11-121">RELATED LINKS</span></span>

