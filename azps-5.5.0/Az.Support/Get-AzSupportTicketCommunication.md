---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/get-azsupportticketcommunication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicketCommunication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicketCommunication.md
ms.openlocfilehash: 07a8747f94f9c1fb93bbff06ce855363088a67a0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190658"
---
# <span data-ttu-id="e495f-101">Get-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="e495f-101">Get-AzSupportTicketCommunication</span></span>

## <span data-ttu-id="e495f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e495f-102">SYNOPSIS</span></span>
<span data-ttu-id="e495f-103">Uzyskaj informacje o biletach pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="e495f-103">Get support ticket communications.</span></span>

## <span data-ttu-id="e495f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e495f-104">SYNTAX</span></span>

### <span data-ttu-id="e495f-105">GetByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="e495f-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSupportTicketCommunication -SupportTicketName <String> [-Name <String>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

### <span data-ttu-id="e495f-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e495f-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSupportTicketCommunication [-Name <String>] -SupportTicketObject <PSSupportTicket> [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

## <span data-ttu-id="e495f-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="e495f-107">DESCRIPTION</span></span>
<span data-ttu-id="e495f-108">Pobiera informacje na zgłoszenie do pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="e495f-108">Gets communications for a support ticket.</span></span> <span data-ttu-id="e495f-109">Jeśli nie określisz żadnych innych parametrów, zostanie pobrana cała komunikacja z biletem.</span><span class="sxs-lookup"><span data-stu-id="e495f-109">It will retrieve all the communications for a ticket if you do not specify any other parameters.</span></span> <span data-ttu-id="e495f-110">Możesz również filtrować komunikację według wartości CreatedDate lub CommunicationType, używając parametru Filter.</span><span class="sxs-lookup"><span data-stu-id="e495f-110">You can also filter the communications by CreatedDate or CommunicationType using the Filter parameter.</span></span> <span data-ttu-id="e495f-111">Poniżej przedstawiono kilka przykładów wartości filtru, które można określić.</span><span class="sxs-lookup"><span data-stu-id="e495f-111">Here are some examples of filter values that you can specify.</span></span>


| <span data-ttu-id="e495f-112">Scenariusz</span><span class="sxs-lookup"><span data-stu-id="e495f-112">Scenario</span></span>                                                        | <span data-ttu-id="e495f-113">Filtr</span><span class="sxs-lookup"><span data-stu-id="e495f-113">Filter</span></span>                                                     |
|-----------------------------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="e495f-114">Uzyskiwanie komunikacji za pomocą sieci Web</span><span class="sxs-lookup"><span data-stu-id="e495f-114">Get Web communications</span></span>                                          | <span data-ttu-id="e495f-115">"CommunicationType eq 'Web'"</span><span class="sxs-lookup"><span data-stu-id="e495f-115">"CommunicationType eq 'Web'"</span></span>                               |
| <span data-ttu-id="e495f-116">Uzyskiwanie komunikacji za pomocą telefonu</span><span class="sxs-lookup"><span data-stu-id="e495f-116">Get Phone communications</span></span>                                        | <span data-ttu-id="e495f-117">"CommunicationType eq 'Phone'"</span><span class="sxs-lookup"><span data-stu-id="e495f-117">"CommunicationType eq 'Phone'"</span></span>                             |
| <span data-ttu-id="e495f-118">Uzyskiwanie informacji utworzonych 20 grudnia 2019 r. lub później</span><span class="sxs-lookup"><span data-stu-id="e495f-118">Get communications that were created on or after 20th Dec, 2019</span></span> | <span data-ttu-id="e495f-119">"CreatedDate ge 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="e495f-119">"CreatedDate ge 2019-12-20"</span></span>                                |
| <span data-ttu-id="e495f-120">Uzyskiwanie komunikacji utworzonej po 20 grudnia 2019 r.</span><span class="sxs-lookup"><span data-stu-id="e495f-120">Get communications that were created after 20th Dec, 2019</span></span>       | <span data-ttu-id="e495f-121">"CreatedDate gt 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="e495f-121">"CreatedDate gt 2019-12-20"</span></span>                                |
| <span data-ttu-id="e495f-122">Pobiera informacje z sieci Web utworzone po 20 grudnia 2019 r.</span><span class="sxs-lookup"><span data-stu-id="e495f-122">Gets Web communications created after 20th Dec, 2019</span></span>            | <span data-ttu-id="e495f-123">"CreatedDate gt 2019-12-20 and CommunicationType eq 'Web'"</span><span class="sxs-lookup"><span data-stu-id="e495f-123">"CreatedDate gt 2019-12-20 and CommunicationType eq 'Web'"</span></span> |


<span data-ttu-id="e495f-124">To polecenie cmdlet obsługuje stronicowanie za pomocą parametrów First (Pierwszy) i Skip (Pomiń).</span><span class="sxs-lookup"><span data-stu-id="e495f-124">This cmdlet supports paging via First and Skip parameters.</span></span>

<span data-ttu-id="e495f-125">Możesz również pobrać komunikację z biletem pomocy technicznej, określając nazwę komunikacji.</span><span class="sxs-lookup"><span data-stu-id="e495f-125">You can also retrieve a single support ticket communication by specifying the communication name.</span></span> 

## <span data-ttu-id="e495f-126">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e495f-126">EXAMPLES</span></span>

### <span data-ttu-id="e495f-127">Przykład 1. Pobieranie całej komunikacji dla biletu pomocy technicznej</span><span class="sxs-lookup"><span data-stu-id="e495f-127">Example 1: Retrieve all communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
testmessage1 user@contoso.com     test message   2/4/2020 9:35:42 PM
```

### <span data-ttu-id="e495f-128">Przykład 2. Pobieranie pojedynczej komunikacji według jej nazwy dla biletu pomocy technicznej</span><span class="sxs-lookup"><span data-stu-id="e495f-128">Example 2: Retrieve a single communication by it's name for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Name "testmessage1"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage1 user@contoso.com     test message   2/4/2020 9:38:14 PM
```

### <span data-ttu-id="e495f-129">Przykład 3. Pobieranie pierwszej 2 komunikacji dla zgłoszenia do pomocy technicznej</span><span class="sxs-lookup"><span data-stu-id="e495f-129">Example 3: Retrieve first 2 communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -First 2

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="e495f-130">Przykład 4. Pobieranie następnej 2 komunikacji po pominięciem pierwszej 2 komunikacji dla zgłoszenia do pomocy technicznej</span><span class="sxs-lookup"><span data-stu-id="e495f-130">Example 4: Retrieve next 2 communications after skipping first 2 communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Skip 2 -First 2

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage4 user@contoso.com     test message4  2/4/2020 9:38:14 PM
testmessage5 user@contoso.com     test message5  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="e495f-131">Przykład 5. Pobieranie całej komunikacji w sieci Web dla biletu pomocy technicznej</span><span class="sxs-lookup"><span data-stu-id="e495f-131">Example 5: Retrieve all Web communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CommunicationType eq 'Web'"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="e495f-132">Przykład 6. Pobieranie całej komunikacji utworzonej 20 grudnia 2019 r. w sprawie zgłoszenia do pomocy technicznej</span><span class="sxs-lookup"><span data-stu-id="e495f-132">Example 6: Retrieve all communications created on or after Dec 20th, 2019 for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CreatedDate ge 2019-12-20"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="e495f-133">Przykład 7. Pobieranie całej komunikacji w sieci Web utworzonej 20 grudnia 2019 r. w celu zgłoszenia do pomocy technicznej</span><span class="sxs-lookup"><span data-stu-id="e495f-133">Example 7: Retrieve all Web communications created on or after Dec 20th, 2019 for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CommunicationType eq 'Web' and CreatedDate ge 2019-12-20"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="e495f-134">Przykład 8. Pobieranie całej komunikacji dla biletu pomocy technicznej przez obiekt biletu pomocy technicznej dla usługi pipingu</span><span class="sxs-lookup"><span data-stu-id="e495f-134">Example 8: Retrieve all communications for a support ticket by piping support ticket object</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Get-AzSupportTicketCommunication

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
testmessage1 user@contoso.com     test message   2/4/2020 9:35:42 PM
```

## <span data-ttu-id="e495f-135">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e495f-135">PARAMETERS</span></span>

### <span data-ttu-id="e495f-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e495f-136">-DefaultProfile</span></span>
<span data-ttu-id="e495f-137">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e495f-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e495f-138">— Filtr</span><span class="sxs-lookup"><span data-stu-id="e495f-138">-Filter</span></span>
<span data-ttu-id="e495f-139">Filtr, który ma zostać zastosowany do wyników tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e495f-139">Filter to be applied to the results of this cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e495f-140">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e495f-140">-Name</span></span>
<span data-ttu-id="e495f-141">Nazwa komunikacji.</span><span class="sxs-lookup"><span data-stu-id="e495f-141">Communication name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e495f-142">-SupportTicketName</span><span class="sxs-lookup"><span data-stu-id="e495f-142">-SupportTicketName</span></span>
<span data-ttu-id="e495f-143">Nazwa biletu pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="e495f-143">Support ticket name.</span></span>

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

### <span data-ttu-id="e495f-144">-SupportTicketObject</span><span class="sxs-lookup"><span data-stu-id="e495f-144">-SupportTicketObject</span></span>
<span data-ttu-id="e495f-145">Obiekt bilet pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="e495f-145">Support ticket object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSSupportTicket
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e495f-146">- IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="e495f-146">-IncludeTotalCount</span></span>
<span data-ttu-id="e495f-147">Raportuje całkowitą liczbę obiektów w zestawie danych (liczbę całkowitą), a po niej zaznaczone obiekty.</span><span class="sxs-lookup"><span data-stu-id="e495f-147">Reports the total number of objects in the data set (an integer) followed by the selected objects.</span></span>
<span data-ttu-id="e495f-148">Jeśli polecenie cmdlet nie może ustalić łącznej liczby, wyświetla komunikat "Nieznana liczba sum".</span><span class="sxs-lookup"><span data-stu-id="e495f-148">If the cmdlet cannot determine the total count, it displays "Unknown total count."</span></span> <span data-ttu-id="e495f-149">Liczba całkowita ma właściwość Dokładność, która wskazuje niezawodność wartości łącznej liczby.</span><span class="sxs-lookup"><span data-stu-id="e495f-149">The integer has an Accuracy property that indicates the reliability of the total count value.</span></span>
<span data-ttu-id="e495f-150">Wartość zakresu dokładności z zakresu od 0,0 do 1,0, gdzie 0,0 oznacza, że polecenie cmdlet nie może zliczyć obiektów, 1,0 oznacza, że liczba jest dokładna, a wartość z przedziału od 0,0 do 1,0 oznacza coraz bardziej niezawodną oszacowanie.</span><span class="sxs-lookup"><span data-stu-id="e495f-150">The value of Accuracy ranges from 0.0 to 1.0 where 0.0 means that the cmdlet could not count the objects, 1.0 means that the count is exact, and a value between 0.0 and 1.0 indicates an increasingly reliable estimate.</span></span>

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

### <span data-ttu-id="e495f-151">— Pomiń</span><span class="sxs-lookup"><span data-stu-id="e495f-151">-Skip</span></span>
<span data-ttu-id="e495f-152">Ignoruje określoną liczbę obiektów, a następnie pobiera pozostałe obiekty.</span><span class="sxs-lookup"><span data-stu-id="e495f-152">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="e495f-153">Wprowadź liczbę obiektów, które mają być pomijane.</span><span class="sxs-lookup"><span data-stu-id="e495f-153">Enter the number of objects to skip.</span></span>

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

### <span data-ttu-id="e495f-154">— najpierw</span><span class="sxs-lookup"><span data-stu-id="e495f-154">-First</span></span>
<span data-ttu-id="e495f-155">Pobiera tylko określoną liczbę obiektów.</span><span class="sxs-lookup"><span data-stu-id="e495f-155">Gets only the specified number of objects.</span></span>
<span data-ttu-id="e495f-156">Wprowadź liczbę obiektów do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="e495f-156">Enter the number of objects to get.</span></span>

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

### <span data-ttu-id="e495f-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e495f-157">CommonParameters</span></span>
<span data-ttu-id="e495f-158">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e495f-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e495f-159">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e495f-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e495f-160">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e495f-160">INPUTS</span></span>

### <span data-ttu-id="e495f-161">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="e495f-161">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="e495f-162">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e495f-162">OUTPUTS</span></span>

### <span data-ttu-id="e495f-163">Microsoft.Azure.Commands.Support.Models.PSSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="e495f-163">Microsoft.Azure.Commands.Support.Models.PSSupportTicketCommunication</span></span>

## <span data-ttu-id="e495f-164">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e495f-164">NOTES</span></span>

## <span data-ttu-id="e495f-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e495f-165">RELATED LINKS</span></span>
