---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 09391f521a2b75663b25731c6cc20ef78a658d5f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710652"
---
# <span data-ttu-id="eceda-101">Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="eceda-101">Add-AzsScaleUnitNode</span></span>

## <span data-ttu-id="eceda-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eceda-102">SYNOPSIS</span></span>
<span data-ttu-id="eceda-103">Skaluj na jednostkę skali.</span><span class="sxs-lookup"><span data-stu-id="eceda-103">Scale out a scale unit.</span></span>

## <span data-ttu-id="eceda-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eceda-104">SYNTAX</span></span>

```
Add-AzsScaleUnitNode [-NodeList] <ScaleOutScaleUnitParameters[]> [[-ResourceGroupName] <String>]
 [-ScaleUnit] <String> [[-Location] <String>] [-AwaitStorageConvergence] [-AsJob] [<CommonParameters>]
```

## <span data-ttu-id="eceda-105">Opis</span><span class="sxs-lookup"><span data-stu-id="eceda-105">DESCRIPTION</span></span>
<span data-ttu-id="eceda-106">Dodaj nowy węzeł jednostka skali do klastra jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="eceda-106">Add a new scale unit node to your scale unit cluster.</span></span>

## <span data-ttu-id="eceda-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eceda-107">EXAMPLES</span></span>

### <span data-ttu-id="eceda-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="eceda-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsScaleUnitNode -NodeList $Nodes -ScaleUnit $ScaleUnitName
```

<span data-ttu-id="eceda-109">Dodaje listę węzłów do jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="eceda-109">Adds a list of nodes to the scale unit.</span></span>

## <span data-ttu-id="eceda-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eceda-110">PARAMETERS</span></span>

### <span data-ttu-id="eceda-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eceda-111">-AsJob</span></span>
<span data-ttu-id="eceda-112">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="eceda-112">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eceda-113">-AwaitStorageConvergence</span><span class="sxs-lookup"><span data-stu-id="eceda-113">-AwaitStorageConvergence</span></span>
<span data-ttu-id="eceda-114">Przed zwróceniem sukcesu poczekaj na ukończenie replikacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="eceda-114">Wait for storage replication to complete before returning success.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eceda-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="eceda-115">-Location</span></span>
<span data-ttu-id="eceda-116">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="eceda-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eceda-117">-NodeList</span><span class="sxs-lookup"><span data-stu-id="eceda-117">-NodeList</span></span>
<span data-ttu-id="eceda-118">Lista danych wejściowych umożliwiających dodanie zestawu węzłów jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="eceda-118">A list of input data that allows for adding a set of scale unit nodes.</span></span>

```yaml
Type: ScaleOutScaleUnitParameters[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eceda-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eceda-119">-ResourceGroupName</span></span>
<span data-ttu-id="eceda-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="eceda-120">Name of the resource group.</span></span>

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

### <span data-ttu-id="eceda-121">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="eceda-121">-ScaleUnit</span></span>
<span data-ttu-id="eceda-122">Nazwa jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="eceda-122">Name of the scale units.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eceda-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eceda-123">CommonParameters</span></span>
<span data-ttu-id="eceda-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eceda-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eceda-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eceda-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eceda-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eceda-126">INPUTS</span></span>

## <span data-ttu-id="eceda-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eceda-127">OUTPUTS</span></span>

## <span data-ttu-id="eceda-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eceda-128">NOTES</span></span>

## <span data-ttu-id="eceda-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eceda-129">RELATED LINKS</span></span>

