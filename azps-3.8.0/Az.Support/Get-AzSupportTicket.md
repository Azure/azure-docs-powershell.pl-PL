---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/get-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicket.md
ms.openlocfilehash: 625d5e375a8a0e7ad2af5256fc344d80a240d37d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93895318"
---
# <span data-ttu-id="85d3e-101">Get-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="85d3e-101">Get-AzSupportTicket</span></span>

## <span data-ttu-id="85d3e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="85d3e-102">SYNOPSIS</span></span>
<span data-ttu-id="85d3e-103">Uzyskaj bilety na pomoc techniczną.</span><span class="sxs-lookup"><span data-stu-id="85d3e-103">Get support tickets.</span></span>

## <span data-ttu-id="85d3e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="85d3e-104">SYNTAX</span></span>

### <span data-ttu-id="85d3e-105">ListParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="85d3e-105">ListParameterSet (Default)</span></span>
```
Get-AzSupportTicket [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="85d3e-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="85d3e-106">GetByNameParameterSet</span></span>
```
Get-AzSupportTicket -Name <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="85d3e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="85d3e-107">DESCRIPTION</span></span>
<span data-ttu-id="85d3e-108">Pobiera listę biletów pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="85d3e-108">Gets the list of support tickets.</span></span> <span data-ttu-id="85d3e-109">Jeśli nie określisz żadnych parametrów, wszystkie bilety pomocy technicznej zostaną pobrane.</span><span class="sxs-lookup"><span data-stu-id="85d3e-109">It will retrieve all the support tickets if you do not specify any parameters.</span></span> <span data-ttu-id="85d3e-110">Możesz również filtrować bilety obsługi według statusu lub polach CreatedDate za pomocą parametru Filter.</span><span class="sxs-lookup"><span data-stu-id="85d3e-110">You can also filter the support tickets by Status or CreatedDate using the Filter parameter.</span></span> <span data-ttu-id="85d3e-111">Poniżej przedstawiono kilka przykładów wartości filtru, które można określić.</span><span class="sxs-lookup"><span data-stu-id="85d3e-111">Here are some examples of filter values that you can specify.</span></span>

| <span data-ttu-id="85d3e-112">Scenariusz</span><span class="sxs-lookup"><span data-stu-id="85d3e-112">Scenario</span></span>                                                         | <span data-ttu-id="85d3e-113">Filtru</span><span class="sxs-lookup"><span data-stu-id="85d3e-113">Filter</span></span>                                           |
|------------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="85d3e-114">Uzyskiwanie biletów z otwartym stanem</span><span class="sxs-lookup"><span data-stu-id="85d3e-114">Get tickets that are in open state</span></span>                               | <span data-ttu-id="85d3e-115">"Status eq" Otwórz ""</span><span class="sxs-lookup"><span data-stu-id="85d3e-115">"Status eq 'Open'"</span></span>                               |
| <span data-ttu-id="85d3e-116">Uzyskiwanie biletów w stanie zamkniętym</span><span class="sxs-lookup"><span data-stu-id="85d3e-116">Get tickets that are in closed state</span></span>                             | <span data-ttu-id="85d3e-117">"Stan EQ" zamknięty "</span><span class="sxs-lookup"><span data-stu-id="85d3e-117">"Status eq 'Closed'"</span></span>                             |
| <span data-ttu-id="85d3e-118">Pobierz bilety utworzone w dniu 20 grudnia 2019 lub później</span><span class="sxs-lookup"><span data-stu-id="85d3e-118">Get tickets that were created on or after 20th Dec, 2019</span></span>         | <span data-ttu-id="85d3e-119">"Polach CreatedDate GE 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="85d3e-119">"CreatedDate ge 2019-12-20"</span></span>                      |
| <span data-ttu-id="85d3e-120">Pobierz bilety utworzone po 20 grudnia 2019 r.</span><span class="sxs-lookup"><span data-stu-id="85d3e-120">Get tickets that were created after 20th Dec, 2019</span></span>               | <span data-ttu-id="85d3e-121">"Polach CreatedDate gt 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="85d3e-121">"CreatedDate gt 2019-12-20"</span></span>                      |
| <span data-ttu-id="85d3e-122">Pobiera bilety utworzone po 20 grudnia 2019ch w stanie Open (Otwórz).</span><span class="sxs-lookup"><span data-stu-id="85d3e-122">Gets tickets created after 20th Dec, 2019 that are in open state</span></span> | <span data-ttu-id="85d3e-123">"Polach CreatedDate gt 2019-12-20 and status eq" "Open"</span><span class="sxs-lookup"><span data-stu-id="85d3e-123">"CreatedDate gt 2019-12-20 and Status eq 'Open'"</span></span> |


<span data-ttu-id="85d3e-124">To polecenie cmdlet obsługuje stronicowanie za pomocą pierwszych i pomijanych parametrów.</span><span class="sxs-lookup"><span data-stu-id="85d3e-124">This cmdlet supports paging via First and Skip parameters.</span></span>

<span data-ttu-id="85d3e-125">Możesz również pobrać jeden bilet pomocy technicznej, podając nazwę biletu.</span><span class="sxs-lookup"><span data-stu-id="85d3e-125">You can also retrieve a single support ticket by specifying the ticket name.</span></span> 

## <span data-ttu-id="85d3e-126">Przykłady</span><span class="sxs-lookup"><span data-stu-id="85d3e-126">EXAMPLES</span></span>

### <span data-ttu-id="85d3e-127">Przykład 1: Uzyskaj pierwszych 2 bilety</span><span class="sxs-lookup"><span data-stu-id="85d3e-127">Example 1: Get first 2 tickets</span></span>
```powershell
PS C:\> Get-AzSupportTicket -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="85d3e-128">Przykład 2: Uzyskaj pierwsze 2 bilety po pominięciu pierwszego 2.</span><span class="sxs-lookup"><span data-stu-id="85d3e-128">Example 2: Get first 2 tickets after skipping the first 2</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Skip 2 -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test3 test title3                  150010521000314 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test4 test title4                  150010521000315 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="85d3e-129">Przykład 3: uzyskiwanie biletu pomocy technicznej według nazwy</span><span class="sxs-lookup"><span data-stu-id="85d3e-129">Example 3: Get a support ticket by name</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="85d3e-130">Przykład 3: Uzyskaj pierwszych 2 bilety pomocy technicznej filtrowane według statusu</span><span class="sxs-lookup"><span data-stu-id="85d3e-130">Example 3: Get first 2 support tickets filtered by status</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Closed'" -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="85d3e-131">Przykład 3: Uzyskaj wszystkie bilety pomocy technicznej, które są w stanie otwartym, i utworzono po 20 grudnia 2019 r.</span><span class="sxs-lookup"><span data-stu-id="85d3e-131">Example 3: Get all support tickets that are in Open state and created after Dec 20th, 2019</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Open' and CreatedDate gt 2019-12-20"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test6 test title6                  150010521000311 Minimal  Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
test7 test title7                  150010521000312 Minimal  Billing                       Open   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="85d3e-132">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="85d3e-132">PARAMETERS</span></span>

### <span data-ttu-id="85d3e-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85d3e-133">-DefaultProfile</span></span>
<span data-ttu-id="85d3e-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="85d3e-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85d3e-135">-Filter</span><span class="sxs-lookup"><span data-stu-id="85d3e-135">-Filter</span></span>
<span data-ttu-id="85d3e-136">Filtr, który ma zostać zastosowany do wyników tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85d3e-136">Filter to be applied to the results of this cmdlet.</span></span>

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

### <span data-ttu-id="85d3e-137">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="85d3e-137">-Name</span></span>
<span data-ttu-id="85d3e-138">Nazwa biletu pomocy technicznej, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85d3e-138">Name of support ticket that this cmdlet gets.</span></span>

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

### <span data-ttu-id="85d3e-139">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="85d3e-139">-IncludeTotalCount</span></span>
<span data-ttu-id="85d3e-140">Wyświetla całkowitą liczbę obiektów w zbiorze danych (liczba całkowita), a następnie zaznaczone obiekty.</span><span class="sxs-lookup"><span data-stu-id="85d3e-140">Reports the total number of objects in the data set (an integer) followed by the selected objects.</span></span>
<span data-ttu-id="85d3e-141">Jeśli polecenie cmdlet nie może ustalić całkowitej liczby, zostanie wyświetlona "Łączna liczba nieznanych".</span><span class="sxs-lookup"><span data-stu-id="85d3e-141">If the cmdlet cannot determine the total count, it displays "Unknown total count."</span></span> <span data-ttu-id="85d3e-142">Liczba całkowita ma właściwość dokładność wskazującą wiarygodność całkowitej wartości licznika.</span><span class="sxs-lookup"><span data-stu-id="85d3e-142">The integer has an Accuracy property that indicates the reliability of the total count value.</span></span>
<span data-ttu-id="85d3e-143">Wartość zakresu dokładności od 0,0 do 1,0 w przypadku, gdy 0,0 oznacza, że nie można zliczyć obiektów przez polecenie cmdlet, 1,0 oznacza, że liczba jest dokładna, a wartość między 0,0 a 1,0 wskazuje coraz bardziej niezawodny szacunek.</span><span class="sxs-lookup"><span data-stu-id="85d3e-143">The value of Accuracy ranges from 0.0 to 1.0 where 0.0 means that the cmdlet could not count the objects, 1.0 means that the count is exact, and a value between 0.0 and 1.0 indicates an increasingly reliable estimate.</span></span>

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

### <span data-ttu-id="85d3e-144">-Skip</span><span class="sxs-lookup"><span data-stu-id="85d3e-144">-Skip</span></span>
<span data-ttu-id="85d3e-145">Ignoruje określoną liczbę obiektów, a następnie pobiera pozostałe obiekty.</span><span class="sxs-lookup"><span data-stu-id="85d3e-145">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="85d3e-146">Wprowadź liczbę obiektów, które mają zostać pominięte.</span><span class="sxs-lookup"><span data-stu-id="85d3e-146">Enter the number of objects to skip.</span></span>

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

### <span data-ttu-id="85d3e-147">-First</span><span class="sxs-lookup"><span data-stu-id="85d3e-147">-First</span></span>
<span data-ttu-id="85d3e-148">Pobiera tylko określoną liczbę obiektów.</span><span class="sxs-lookup"><span data-stu-id="85d3e-148">Gets only the specified number of objects.</span></span>
<span data-ttu-id="85d3e-149">Wprowadź liczbę obiektów do pobrania.</span><span class="sxs-lookup"><span data-stu-id="85d3e-149">Enter the number of objects to get.</span></span>

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

### <span data-ttu-id="85d3e-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85d3e-150">CommonParameters</span></span>
<span data-ttu-id="85d3e-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85d3e-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85d3e-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="85d3e-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85d3e-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="85d3e-153">INPUTS</span></span>

### <span data-ttu-id="85d3e-154">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="85d3e-154">None</span></span>

## <span data-ttu-id="85d3e-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="85d3e-155">OUTPUTS</span></span>

### <span data-ttu-id="85d3e-156">Microsoft. Azure. Commands. support. models. PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="85d3e-156">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="85d3e-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="85d3e-157">NOTES</span></span>

## <span data-ttu-id="85d3e-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="85d3e-158">RELATED LINKS</span></span>
