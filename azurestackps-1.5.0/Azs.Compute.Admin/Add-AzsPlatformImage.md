---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 15ec1f3e70752a5386cd5dad78d867da68091b96
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523717"
---
# <span data-ttu-id="bc90c-101">Add-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="bc90c-101">Add-AzsPlatformImage</span></span>

## <span data-ttu-id="bc90c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bc90c-102">SYNOPSIS</span></span>
<span data-ttu-id="bc90c-103">Dodaj obraz platformy maszyny wirtualnej z danej konfiguracji obrazu.</span><span class="sxs-lookup"><span data-stu-id="bc90c-103">Add a virtual machine platform image from a given image configuration.</span></span>

## <span data-ttu-id="bc90c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bc90c-104">SYNTAX</span></span>

```
Add-AzsPlatformImage [-Publisher] <String> [-Offer] <String> [-Sku] <String> [-Version] <String>
 [-OsType] <Object> [-OsUri] <String> [[-BillingPartNumber] <String>] [[-DataDisks] <DataDisk[]>]
 [[-Location] <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc90c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bc90c-105">DESCRIPTION</span></span>
<span data-ttu-id="bc90c-106">Dodaj obraz platformy.</span><span class="sxs-lookup"><span data-stu-id="bc90c-106">Add a platform image.</span></span>

## <span data-ttu-id="bc90c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bc90c-107">EXAMPLES</span></span>

### <span data-ttu-id="bc90c-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="bc90c-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsPlatformImage -Publisher Test -Offer UbuntuServer -Sku 16.04-LTS -Version 1.0.0 -OsType "Linux" -OsUri "https://test.blob.local.azurestack.external/test/xenial-server-cloudimg-amd64-disk1.vhd"
```

<span data-ttu-id="bc90c-109">Dodaj nowy obraz platformy.</span><span class="sxs-lookup"><span data-stu-id="bc90c-109">Add a new platform image.</span></span>

## <span data-ttu-id="bc90c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bc90c-110">PARAMETERS</span></span>

### <span data-ttu-id="bc90c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bc90c-111">-AsJob</span></span>
<span data-ttu-id="bc90c-112">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="bc90c-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="bc90c-113">-BillingPartNumber</span><span class="sxs-lookup"><span data-stu-id="bc90c-113">-BillingPartNumber</span></span>
<span data-ttu-id="bc90c-114">Numer części jest wykorzystywany do naliczania kosztów oprogramowania.</span><span class="sxs-lookup"><span data-stu-id="bc90c-114">The part number is used to bill for software costs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc90c-115">-Datadyski</span><span class="sxs-lookup"><span data-stu-id="bc90c-115">-DataDisks</span></span>
<span data-ttu-id="bc90c-116">Dyski danych używane przez obraz platformy.</span><span class="sxs-lookup"><span data-stu-id="bc90c-116">Data disks used by the platform image.</span></span>

```yaml
Type: DataDisk[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc90c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="bc90c-117">-Force</span></span>
<span data-ttu-id="bc90c-118">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bc90c-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="bc90c-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="bc90c-119">-Location</span></span>
<span data-ttu-id="bc90c-120">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="bc90c-120">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc90c-121">-Offer</span><span class="sxs-lookup"><span data-stu-id="bc90c-121">-Offer</span></span>
<span data-ttu-id="bc90c-122">Imię i nazwisko oferty.</span><span class="sxs-lookup"><span data-stu-id="bc90c-122">Name of the offer.</span></span>

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

### <span data-ttu-id="bc90c-123">-OsType</span><span class="sxs-lookup"><span data-stu-id="bc90c-123">-OsType</span></span>
<span data-ttu-id="bc90c-124">Typ systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="bc90c-124">Operating system type.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc90c-125">-OsUri</span><span class="sxs-lookup"><span data-stu-id="bc90c-125">-OsUri</span></span>
<span data-ttu-id="bc90c-126">Lokalizacja dysku.</span><span class="sxs-lookup"><span data-stu-id="bc90c-126">Location of the disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc90c-127">— Wydawca</span><span class="sxs-lookup"><span data-stu-id="bc90c-127">-Publisher</span></span>
<span data-ttu-id="bc90c-128">Nazwa wydawcy.</span><span class="sxs-lookup"><span data-stu-id="bc90c-128">Name of the publisher.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc90c-129">-SKU</span><span class="sxs-lookup"><span data-stu-id="bc90c-129">-Sku</span></span>
<span data-ttu-id="bc90c-130">Nazwa jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="bc90c-130">Name of the SKU.</span></span>

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

### <span data-ttu-id="bc90c-131">-Version</span><span class="sxs-lookup"><span data-stu-id="bc90c-131">-Version</span></span>
<span data-ttu-id="bc90c-132">Wersja obrazu platformy maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bc90c-132">The version of the virtual machine platform image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc90c-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bc90c-133">-Confirm</span></span>
<span data-ttu-id="bc90c-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc90c-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc90c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc90c-135">-WhatIf</span></span>
<span data-ttu-id="bc90c-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc90c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc90c-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bc90c-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc90c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc90c-138">CommonParameters</span></span>
<span data-ttu-id="bc90c-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc90c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc90c-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc90c-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc90c-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bc90c-141">INPUTS</span></span>

## <span data-ttu-id="bc90c-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bc90c-142">OUTPUTS</span></span>

### <span data-ttu-id="bc90c-143">PlatformImageObject</span><span class="sxs-lookup"><span data-stu-id="bc90c-143">PlatformImageObject</span></span>

## <span data-ttu-id="bc90c-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bc90c-144">NOTES</span></span>

## <span data-ttu-id="bc90c-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bc90c-145">RELATED LINKS</span></span>

