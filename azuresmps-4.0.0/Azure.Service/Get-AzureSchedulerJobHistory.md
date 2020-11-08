---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 2BF5BDF8-3743-46FC-8E04-1A4EA920A2AF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 77b4d184ffbdb1d054f3d14aa3c51c8d2afc928b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055276"
---
# <span data-ttu-id="9e9f5-101">Get-AzureSchedulerJobHistory</span><span class="sxs-lookup"><span data-stu-id="9e9f5-101">Get-AzureSchedulerJobHistory</span></span>

## <span data-ttu-id="9e9f5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9e9f5-102">SYNOPSIS</span></span>
<span data-ttu-id="9e9f5-103">Pobiera historię zadania harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="9e9f5-103">Gets history for a scheduler job.</span></span>

## <span data-ttu-id="9e9f5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9e9f5-104">SYNTAX</span></span>

```
Get-AzureSchedulerJobHistory -Location <String> -JobCollectionName <String> -JobName <String>
 [-JobStatus <String>] [-Profile <AzureSMProfile>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

## <span data-ttu-id="9e9f5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9e9f5-105">DESCRIPTION</span></span>
<span data-ttu-id="9e9f5-106">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9e9f5-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="9e9f5-107">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="9e9f5-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="9e9f5-108">Polecenie cmdlet **Get-AzureSchedulerJobHistory** pobiera historię zadania harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="9e9f5-108">The **Get-AzureSchedulerJobHistory** cmdlet gets the history for a scheduler job.</span></span>

## <span data-ttu-id="9e9f5-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9e9f5-109">EXAMPLES</span></span>

### <span data-ttu-id="9e9f5-110">Przykład 1: uzyskiwanie historii zadania przy użyciu jego nazwy</span><span class="sxs-lookup"><span data-stu-id="9e9f5-110">Example 1: Get history for a job by using its name</span></span>
```
PS C:\> Get-AzureSchedulerJobHistory -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job01"
```

<span data-ttu-id="9e9f5-111">To polecenie pobiera historię zadania o nazwie Job01.</span><span class="sxs-lookup"><span data-stu-id="9e9f5-111">This command gets the history of the job named Job01.</span></span>
<span data-ttu-id="9e9f5-112">To zadanie należy do kolekcji zadań o nazwie JobCollection01 w określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="9e9f5-112">That job belongs to the job collection named JobCollection01 in the specified location.</span></span>

### <span data-ttu-id="9e9f5-113">Przykład 2: Pobieranie historii zadania zakończonego niepowodzeniem przy użyciu jego nazwy</span><span class="sxs-lookup"><span data-stu-id="9e9f5-113">Example 2: Get history for a failed job by using its name</span></span>
```
PS C:\> Get-AzureSchedulerJobHistory -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job12" -JobStatus "Failed"
```

<span data-ttu-id="9e9f5-114">To polecenie pobiera historię zadania o nazwie Job12 o stanie Niepowodzenie.</span><span class="sxs-lookup"><span data-stu-id="9e9f5-114">This command gets the history of the job named Job12 that has a status of Failed.</span></span>
<span data-ttu-id="9e9f5-115">To zadanie należy do kolekcji zadań o nazwie JobCollection01 w określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="9e9f5-115">That job belongs to the job collection named JobCollection01 in the specified location.</span></span>

## <span data-ttu-id="9e9f5-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9e9f5-116">PARAMETERS</span></span>

### <span data-ttu-id="9e9f5-117">-First</span><span class="sxs-lookup"><span data-stu-id="9e9f5-117">-First</span></span>
<span data-ttu-id="9e9f5-118">Pobiera tylko określoną liczbę obiektów.</span><span class="sxs-lookup"><span data-stu-id="9e9f5-118">Gets only the specified number of objects.</span></span>
<span data-ttu-id="9e9f5-119">Wprowadź liczbę obiektów do pobrania.</span><span class="sxs-lookup"><span data-stu-id="9e9f5-119">Enter the number of objects to get.</span></span>

```yaml
Type: UInt64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e9f5-120">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="9e9f5-120">-IncludeTotalCount</span></span>
<span data-ttu-id="9e9f5-121">Wyświetla całkowitą liczbę obiektów w zbiorze danych (liczba całkowita), a następnie zaznaczone obiekty.</span><span class="sxs-lookup"><span data-stu-id="9e9f5-121">Reports the total number of objects in the data set (an integer) followed by the selected objects.</span></span>
<span data-ttu-id="9e9f5-122">Jeśli polecenie cmdlet nie może ustalić całkowitej liczby, zostanie wyświetlona "Łączna liczba nieznanych".</span><span class="sxs-lookup"><span data-stu-id="9e9f5-122">If the cmdlet cannot determine the total count, it displays "Unknown total count."</span></span> <span data-ttu-id="9e9f5-123">Liczba całkowita ma właściwość dokładność wskazującą wiarygodność całkowitej wartości licznika.</span><span class="sxs-lookup"><span data-stu-id="9e9f5-123">The integer has an Accuracy property that indicates the reliability of the total count value.</span></span>
<span data-ttu-id="9e9f5-124">Wartość zakresu dokładności od 0,0 do 1,0 w przypadku, gdy 0,0 oznacza, że nie można zliczyć obiektów przez polecenie cmdlet, 1,0 oznacza, że liczba jest dokładna, a wartość między 0,0 a 1,0 wskazuje coraz bardziej niezawodny szacunek.</span><span class="sxs-lookup"><span data-stu-id="9e9f5-124">The value of Accuracy ranges from 0.0 to 1.0 where 0.0 means that the cmdlet could not count the objects, 1.0 means that the count is exact, and a value between 0.0 and 1.0 indicates an increasingly reliable estimate.</span></span>

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

### <span data-ttu-id="9e9f5-125">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="9e9f5-125">-JobCollectionName</span></span>
<span data-ttu-id="9e9f5-126">Określa nazwę kolekcji zadań harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="9e9f5-126">Specifies the name of a scheduler job collection.</span></span>
<span data-ttu-id="9e9f5-127">To polecenie cmdlet pobiera historię zadania należącego do kolekcji, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="9e9f5-127">This cmdlet gets the history for a job that belongs to the collection that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e9f5-128">-JobName</span><span class="sxs-lookup"><span data-stu-id="9e9f5-128">-JobName</span></span>
<span data-ttu-id="9e9f5-129">Określa nazwę zadania harmonogramu, dla którego ma zostać wykorzystana historia.</span><span class="sxs-lookup"><span data-stu-id="9e9f5-129">Specifies the name of a scheduler job for which to get the history.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e9f5-130">-JobStatus</span><span class="sxs-lookup"><span data-stu-id="9e9f5-130">-JobStatus</span></span>
<span data-ttu-id="9e9f5-131">Określa stan zadania harmonogramu, dla którego ma zostać wykorzystana historia.</span><span class="sxs-lookup"><span data-stu-id="9e9f5-131">Specifies the status of scheduler job for which to get the history.</span></span>
<span data-ttu-id="9e9f5-132">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="9e9f5-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9e9f5-133">Zakończyć</span><span class="sxs-lookup"><span data-stu-id="9e9f5-133">Completed</span></span>
- <span data-ttu-id="9e9f5-134">Nie powiodło się</span><span class="sxs-lookup"><span data-stu-id="9e9f5-134">Failed</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e9f5-135">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="9e9f5-135">-Location</span></span>
<span data-ttu-id="9e9f5-136">Określa nazwę lokalizacji, w której znajduje się usługa chmury.</span><span class="sxs-lookup"><span data-stu-id="9e9f5-136">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="9e9f5-137">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="9e9f5-137">Valid values are:</span></span> 

- <span data-ttu-id="9e9f5-138">W dowolnym miejscu w Azji</span><span class="sxs-lookup"><span data-stu-id="9e9f5-138">Anywhere Asia</span></span>
- <span data-ttu-id="9e9f5-139">Dowolne miejsce w Europie</span><span class="sxs-lookup"><span data-stu-id="9e9f5-139">Anywhere Europe</span></span>
- <span data-ttu-id="9e9f5-140">Dowolne miejsce w USA</span><span class="sxs-lookup"><span data-stu-id="9e9f5-140">Anywhere US</span></span>
- <span data-ttu-id="9e9f5-141">Azja Wschodnia</span><span class="sxs-lookup"><span data-stu-id="9e9f5-141">East Asia</span></span>
- <span data-ttu-id="9e9f5-142">Wschodnie USA</span><span class="sxs-lookup"><span data-stu-id="9e9f5-142">East US</span></span>
- <span data-ttu-id="9e9f5-143">Północno-środkowe USA</span><span class="sxs-lookup"><span data-stu-id="9e9f5-143">North Central US</span></span>
- <span data-ttu-id="9e9f5-144">Europa Północna</span><span class="sxs-lookup"><span data-stu-id="9e9f5-144">North Europe</span></span>
- <span data-ttu-id="9e9f5-145">Południowa Centrala amerykańska</span><span class="sxs-lookup"><span data-stu-id="9e9f5-145">South Central US</span></span>
- <span data-ttu-id="9e9f5-146">Azja Południowo-Wschodnia</span><span class="sxs-lookup"><span data-stu-id="9e9f5-146">Southeast Asia</span></span>
- <span data-ttu-id="9e9f5-147">Europa Zachodnia</span><span class="sxs-lookup"><span data-stu-id="9e9f5-147">West Europe</span></span>
- <span data-ttu-id="9e9f5-148">Zachodnie USA</span><span class="sxs-lookup"><span data-stu-id="9e9f5-148">West US</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e9f5-149">-Profile</span><span class="sxs-lookup"><span data-stu-id="9e9f5-149">-Profile</span></span>
<span data-ttu-id="9e9f5-150">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e9f5-150">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9e9f5-151">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="9e9f5-151">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e9f5-152">-Skip</span><span class="sxs-lookup"><span data-stu-id="9e9f5-152">-Skip</span></span>
<span data-ttu-id="9e9f5-153">Ignoruje określoną liczbę obiektów, a następnie pobiera pozostałe obiekty.</span><span class="sxs-lookup"><span data-stu-id="9e9f5-153">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="9e9f5-154">Wprowadź liczbę obiektów, które mają zostać pominięte.</span><span class="sxs-lookup"><span data-stu-id="9e9f5-154">Enter the number of objects to skip.</span></span>

```yaml
Type: UInt64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e9f5-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e9f5-155">CommonParameters</span></span>
<span data-ttu-id="9e9f5-156">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e9f5-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e9f5-157">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e9f5-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e9f5-158">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9e9f5-158">INPUTS</span></span>

## <span data-ttu-id="9e9f5-159">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9e9f5-159">OUTPUTS</span></span>

## <span data-ttu-id="9e9f5-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9e9f5-160">NOTES</span></span>

## <span data-ttu-id="9e9f5-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9e9f5-161">RELATED LINKS</span></span>

[<span data-ttu-id="9e9f5-162">Get-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="9e9f5-162">Get-AzureSchedulerJob</span></span>](./Get-AzureSchedulerJob.md)

[<span data-ttu-id="9e9f5-163">Get-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="9e9f5-163">Get-AzureSchedulerJobCollection</span></span>](./Get-AzureSchedulerJobCollection.md)


