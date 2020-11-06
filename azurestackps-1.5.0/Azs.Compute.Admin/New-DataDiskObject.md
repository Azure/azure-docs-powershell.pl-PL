---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b30ae24d384667aa8d399f03c76ab886b2faa1c9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523282"
---
# <span data-ttu-id="eba6c-101">New-DataDiskObject</span><span class="sxs-lookup"><span data-stu-id="eba6c-101">New-DataDiskObject</span></span>

## <span data-ttu-id="eba6c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eba6c-102">SYNOPSIS</span></span>
<span data-ttu-id="eba6c-103">Tworzy dysk danych, który służy do tworzenia nowego obrazu platformy maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="eba6c-103">Creates a data disk which is used to create a new virtual machine platform image.</span></span>

## <span data-ttu-id="eba6c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eba6c-104">SYNTAX</span></span>

```
New-DataDiskObject [[-Lun] <Int32>] [[-Uri] <String>] [<CommonParameters>]
```

## <span data-ttu-id="eba6c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="eba6c-105">DESCRIPTION</span></span>
<span data-ttu-id="eba6c-106">Tworzy obiekt przechowujący informacje o dysku danych.</span><span class="sxs-lookup"><span data-stu-id="eba6c-106">Creates an object holding information about a data disk.</span></span>

## <span data-ttu-id="eba6c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eba6c-107">EXAMPLES</span></span>

### <span data-ttu-id="eba6c-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="eba6c-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-DataDiskObject -Lun 5 -URI test.blob.windows.net/disks/datadisk5.vhd
```

<span data-ttu-id="eba6c-109">Utwórz nowy obiekt dysku danych.</span><span class="sxs-lookup"><span data-stu-id="eba6c-109">Create a new data disk object.</span></span>

## <span data-ttu-id="eba6c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eba6c-110">PARAMETERS</span></span>

### <span data-ttu-id="eba6c-111">-LUN</span><span class="sxs-lookup"><span data-stu-id="eba6c-111">-Lun</span></span>
<span data-ttu-id="eba6c-112">Numer jednostki logicznej.</span><span class="sxs-lookup"><span data-stu-id="eba6c-112">Logical unit number.</span></span>

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

### <span data-ttu-id="eba6c-113">-URI</span><span class="sxs-lookup"><span data-stu-id="eba6c-113">-Uri</span></span>
<span data-ttu-id="eba6c-114">Lokalizacja szablonu dysku.</span><span class="sxs-lookup"><span data-stu-id="eba6c-114">Location of the disk template.</span></span>

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

### <span data-ttu-id="eba6c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eba6c-115">CommonParameters</span></span>
<span data-ttu-id="eba6c-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eba6c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eba6c-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eba6c-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eba6c-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eba6c-118">INPUTS</span></span>

## <span data-ttu-id="eba6c-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eba6c-119">OUTPUTS</span></span>

## <span data-ttu-id="eba6c-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eba6c-120">NOTES</span></span>

## <span data-ttu-id="eba6c-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eba6c-121">RELATED LINKS</span></span>

