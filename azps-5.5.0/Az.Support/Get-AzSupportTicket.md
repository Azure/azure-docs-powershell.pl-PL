---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/get-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicket.md
ms.openlocfilehash: 368ae4ad814c9414ea211ea6e44c2d3fbda005f7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182835"
---
# <span data-ttu-id="4f700-101">Get-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="4f700-101">Get-AzSupportTicket</span></span>

## <span data-ttu-id="4f700-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f700-102">SYNOPSIS</span></span>
<span data-ttu-id="4f700-103">Uzyskaj bilety pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="4f700-103">Get support tickets.</span></span>

## <span data-ttu-id="4f700-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4f700-104">SYNTAX</span></span>

### <span data-ttu-id="4f700-105">ListParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="4f700-105">ListParameterSet (Default)</span></span>
```
Get-AzSupportTicket [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="4f700-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f700-106">GetByNameParameterSet</span></span>
```
Get-AzSupportTicket -Name <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="4f700-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="4f700-107">DESCRIPTION</span></span>
<span data-ttu-id="4f700-108">Pobiera listę biletów pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="4f700-108">Gets the list of support tickets.</span></span> <span data-ttu-id="4f700-109">Jeśli nie określisz żadnych parametrów, zostaną pobrane wszystkie bilety pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="4f700-109">It will retrieve all the support tickets if you do not specify any parameters.</span></span> <span data-ttu-id="4f700-110">Możesz również filtrować bilety pomocy technicznej według stanu lub wartości CreatedDate, używając parametru Filtruj.</span><span class="sxs-lookup"><span data-stu-id="4f700-110">You can also filter the support tickets by Status or CreatedDate using the Filter parameter.</span></span> <span data-ttu-id="4f700-111">Poniżej przedstawiono kilka przykładów wartości filtru, które można określić.</span><span class="sxs-lookup"><span data-stu-id="4f700-111">Here are some examples of filter values that you can specify.</span></span>

| <span data-ttu-id="4f700-112">Scenariusz</span><span class="sxs-lookup"><span data-stu-id="4f700-112">Scenario</span></span>                                                         | <span data-ttu-id="4f700-113">Filtr</span><span class="sxs-lookup"><span data-stu-id="4f700-113">Filter</span></span>                                           |
|------------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="4f700-114">Uzyskaj bilety, które są w stanie otwartym</span><span class="sxs-lookup"><span data-stu-id="4f700-114">Get tickets that are in open state</span></span>                               | <span data-ttu-id="4f700-115">"Status eq 'Open'"</span><span class="sxs-lookup"><span data-stu-id="4f700-115">"Status eq 'Open'"</span></span>                               |
| <span data-ttu-id="4f700-116">Uzyskaj bilety, które są w stanie zamkniętym</span><span class="sxs-lookup"><span data-stu-id="4f700-116">Get tickets that are in closed state</span></span>                             | <span data-ttu-id="4f700-117">"Status eq 'Closed'"</span><span class="sxs-lookup"><span data-stu-id="4f700-117">"Status eq 'Closed'"</span></span>                             |
| <span data-ttu-id="4f700-118">Uzyskaj bilety utworzone 20 grudnia 2019 r. lub później</span><span class="sxs-lookup"><span data-stu-id="4f700-118">Get tickets that were created on or after 20th Dec, 2019</span></span>         | <span data-ttu-id="4f700-119">"CreatedDate ge 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="4f700-119">"CreatedDate ge 2019-12-20"</span></span>                      |
| <span data-ttu-id="4f700-120">Uzyskaj bilety utworzone po 20 grudnia 2019 r.</span><span class="sxs-lookup"><span data-stu-id="4f700-120">Get tickets that were created after 20th Dec, 2019</span></span>               | <span data-ttu-id="4f700-121">"CreatedDate gt 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="4f700-121">"CreatedDate gt 2019-12-20"</span></span>                      |
| <span data-ttu-id="4f700-122">Pobiera bilety utworzone po 20 grudnia 2019 r. w stanie otwartym</span><span class="sxs-lookup"><span data-stu-id="4f700-122">Gets tickets created after 20th Dec, 2019 that are in open state</span></span> | <span data-ttu-id="4f700-123">"CreatedDate gt 2019-12-20 and Status eq 'Open'"</span><span class="sxs-lookup"><span data-stu-id="4f700-123">"CreatedDate gt 2019-12-20 and Status eq 'Open'"</span></span> |


<span data-ttu-id="4f700-124">To polecenie cmdlet obsługuje stronicowanie za pomocą parametrów First (Pierwszy) i Skip (Pomiń).</span><span class="sxs-lookup"><span data-stu-id="4f700-124">This cmdlet supports paging via First and Skip parameters.</span></span>

<span data-ttu-id="4f700-125">Możesz również pobrać pojedynczy bilet pomocy technicznej, określając nazwę biletu.</span><span class="sxs-lookup"><span data-stu-id="4f700-125">You can also retrieve a single support ticket by specifying the ticket name.</span></span> 

## <span data-ttu-id="4f700-126">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4f700-126">EXAMPLES</span></span>

### <span data-ttu-id="4f700-127">Przykład 1. Uzyskaj pierwsze 2 bilety</span><span class="sxs-lookup"><span data-stu-id="4f700-127">Example 1: Get first 2 tickets</span></span>
```powershell
PS C:\> Get-AzSupportTicket -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="4f700-128">Przykład 2. Uzyskiwanie pierwszych 2 biletów po pominięciem pierwszych 2 biletów</span><span class="sxs-lookup"><span data-stu-id="4f700-128">Example 2: Get first 2 tickets after skipping the first 2</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Skip 2 -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test3 test title3                  150010521000314 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test4 test title4                  150010521000315 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="4f700-129">Przykład 3. Uzyskiwanie zgłoszenia do pomocy technicznej według nazwy</span><span class="sxs-lookup"><span data-stu-id="4f700-129">Example 3: Get a support ticket by name</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="4f700-130">Przykład 4. Uzyskaj pierwsze 2 bilety pomocy technicznej filtrowane według stanu</span><span class="sxs-lookup"><span data-stu-id="4f700-130">Example 4: Get first 2 support tickets filtered by status</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Closed'" -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="4f700-131">Przykład 5. Uzyskaj wszystkie bilety pomocy technicznej, które znajdują się w stanie otwartym i zostały utworzone po 20 grudnia 2019 r.</span><span class="sxs-lookup"><span data-stu-id="4f700-131">Example 5: Get all support tickets that are in Open state and created after Dec 20th, 2019</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Open' and CreatedDate gt 2019-12-20"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test6 test title6                  150010521000311 Minimal  Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
test7 test title7                  150010521000312 Minimal  Billing                       Open   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="4f700-132">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f700-132">PARAMETERS</span></span>

### <span data-ttu-id="4f700-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f700-133">-DefaultProfile</span></span>
<span data-ttu-id="4f700-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4f700-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f700-135">— Filtr</span><span class="sxs-lookup"><span data-stu-id="4f700-135">-Filter</span></span>
<span data-ttu-id="4f700-136">Filtr, który ma zostać zastosowany do wyników tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f700-136">Filter to be applied to the results of this cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f700-137">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4f700-137">-Name</span></span>
<span data-ttu-id="4f700-138">Nazwa biletu pomocy technicznej, które otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f700-138">Name of support ticket that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f700-139">- IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="4f700-139">-IncludeTotalCount</span></span>
<span data-ttu-id="4f700-140">Raportuje całkowitą liczbę obiektów w zestawie danych (liczbę całkowitą), a po niej zaznaczone obiekty.</span><span class="sxs-lookup"><span data-stu-id="4f700-140">Reports the total number of objects in the data set (an integer) followed by the selected objects.</span></span>
<span data-ttu-id="4f700-141">Jeśli polecenie cmdlet nie może ustalić łącznej liczby, wyświetla komunikat "Nieznana liczba sum".</span><span class="sxs-lookup"><span data-stu-id="4f700-141">If the cmdlet cannot determine the total count, it displays "Unknown total count."</span></span> <span data-ttu-id="4f700-142">Liczba całkowita ma właściwość Dokładność, która wskazuje niezawodność wartości łącznej liczby.</span><span class="sxs-lookup"><span data-stu-id="4f700-142">The integer has an Accuracy property that indicates the reliability of the total count value.</span></span>
<span data-ttu-id="4f700-143">Wartość zakresu dokładności wynosi od 0,0 do 1,0, gdzie 0,0 oznacza, że nie można zliczyć obiektów za pomocą polecenia cmdlet, wartość 1,0 oznacza, że liczba jest dokładna, a wartość z przedziału od 0,0 do 1,0 oznacza coraz bardziej niezawodne oszacowanie.</span><span class="sxs-lookup"><span data-stu-id="4f700-143">The value of Accuracy ranges from 0.0 to 1.0 where 0.0 means that the cmdlet could not count the objects, 1.0 means that the count is exact, and a value between 0.0 and 1.0 indicates an increasingly reliable estimate.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f700-144">— Pomiń</span><span class="sxs-lookup"><span data-stu-id="4f700-144">-Skip</span></span>
<span data-ttu-id="4f700-145">Ignoruje określoną liczbę obiektów, a następnie pobiera pozostałe obiekty.</span><span class="sxs-lookup"><span data-stu-id="4f700-145">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="4f700-146">Wprowadź liczbę obiektów do pominięcia.</span><span class="sxs-lookup"><span data-stu-id="4f700-146">Enter the number of objects to skip.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f700-147">— najpierw</span><span class="sxs-lookup"><span data-stu-id="4f700-147">-First</span></span>
<span data-ttu-id="4f700-148">Pobiera tylko określoną liczbę obiektów.</span><span class="sxs-lookup"><span data-stu-id="4f700-148">Gets only the specified number of objects.</span></span>
<span data-ttu-id="4f700-149">Wprowadź liczbę obiektów do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="4f700-149">Enter the number of objects to get.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f700-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f700-150">CommonParameters</span></span>
<span data-ttu-id="4f700-151">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f700-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f700-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4f700-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f700-153">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4f700-153">INPUTS</span></span>

### <span data-ttu-id="4f700-154">Brak</span><span class="sxs-lookup"><span data-stu-id="4f700-154">None</span></span>

## <span data-ttu-id="4f700-155">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4f700-155">OUTPUTS</span></span>

### <span data-ttu-id="4f700-156">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="4f700-156">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="4f700-157">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4f700-157">NOTES</span></span>

## <span data-ttu-id="4f700-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4f700-158">RELATED LINKS</span></span>
