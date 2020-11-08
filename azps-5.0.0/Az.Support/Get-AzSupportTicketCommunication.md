---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/get-azsupportticketcommunication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicketCommunication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicketCommunication.md
ms.openlocfilehash: 07a8747f94f9c1fb93bbff06ce855363088a67a0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224132"
---
# <span data-ttu-id="96608-101">Get-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="96608-101">Get-AzSupportTicketCommunication</span></span>

## <span data-ttu-id="96608-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="96608-102">SYNOPSIS</span></span>
<span data-ttu-id="96608-103">Uzyskaj pomoc na temat przekazu biletów pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="96608-103">Get support ticket communications.</span></span>

## <span data-ttu-id="96608-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="96608-104">SYNTAX</span></span>

### <span data-ttu-id="96608-105">GetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="96608-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSupportTicketCommunication -SupportTicketName <String> [-Name <String>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

### <span data-ttu-id="96608-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="96608-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSupportTicketCommunication [-Name <String>] -SupportTicketObject <PSSupportTicket> [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

## <span data-ttu-id="96608-107">Opis</span><span class="sxs-lookup"><span data-stu-id="96608-107">DESCRIPTION</span></span>
<span data-ttu-id="96608-108">Pobiera komunikat o pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="96608-108">Gets communications for a support ticket.</span></span> <span data-ttu-id="96608-109">Jeśli nie określisz żadnych innych parametrów, otrzymasz całą wiadomość dla biletu.</span><span class="sxs-lookup"><span data-stu-id="96608-109">It will retrieve all the communications for a ticket if you do not specify any other parameters.</span></span> <span data-ttu-id="96608-110">Możesz również filtrować komunikację według polach CreatedDate lub Communicationtype przy użyciu parametru Filter.</span><span class="sxs-lookup"><span data-stu-id="96608-110">You can also filter the communications by CreatedDate or CommunicationType using the Filter parameter.</span></span> <span data-ttu-id="96608-111">Poniżej przedstawiono kilka przykładów wartości filtru, które można określić.</span><span class="sxs-lookup"><span data-stu-id="96608-111">Here are some examples of filter values that you can specify.</span></span>


| <span data-ttu-id="96608-112">Scenariusz</span><span class="sxs-lookup"><span data-stu-id="96608-112">Scenario</span></span>                                                        | <span data-ttu-id="96608-113">Filtru</span><span class="sxs-lookup"><span data-stu-id="96608-113">Filter</span></span>                                                     |
|-----------------------------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="96608-114">Uzyskiwanie komunikacji w sieci Web</span><span class="sxs-lookup"><span data-stu-id="96608-114">Get Web communications</span></span>                                          | <span data-ttu-id="96608-115">"Internettype EQ" "</span><span class="sxs-lookup"><span data-stu-id="96608-115">"CommunicationType eq 'Web'"</span></span>                               |
| <span data-ttu-id="96608-116">Uzyskiwanie komunikacji telefonicznej</span><span class="sxs-lookup"><span data-stu-id="96608-116">Get Phone communications</span></span>                                        | <span data-ttu-id="96608-117">"Telefon komunikacyjny" EQ "</span><span class="sxs-lookup"><span data-stu-id="96608-117">"CommunicationType eq 'Phone'"</span></span>                             |
| <span data-ttu-id="96608-118">Uzyskiwanie wiadomości utworzonych w dniu 20 grudnia 2019 lub później</span><span class="sxs-lookup"><span data-stu-id="96608-118">Get communications that were created on or after 20th Dec, 2019</span></span> | <span data-ttu-id="96608-119">"Polach CreatedDate GE 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="96608-119">"CreatedDate ge 2019-12-20"</span></span>                                |
| <span data-ttu-id="96608-120">Pobierz komunikację utworzoną po 20 grudnia 2019 r.</span><span class="sxs-lookup"><span data-stu-id="96608-120">Get communications that were created after 20th Dec, 2019</span></span>       | <span data-ttu-id="96608-121">"Polach CreatedDate gt 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="96608-121">"CreatedDate gt 2019-12-20"</span></span>                                |
| <span data-ttu-id="96608-122">Pobiera wiadomości internetowe utworzone po 20 grudnia 2019 r.</span><span class="sxs-lookup"><span data-stu-id="96608-122">Gets Web communications created after 20th Dec, 2019</span></span>            | <span data-ttu-id="96608-123">"Polach CreatedDate gt 2019-12-20 and Communicationtype EQ" Web ' "</span><span class="sxs-lookup"><span data-stu-id="96608-123">"CreatedDate gt 2019-12-20 and CommunicationType eq 'Web'"</span></span> |


<span data-ttu-id="96608-124">To polecenie cmdlet obsługuje stronicowanie za pomocą pierwszych i pomijanych parametrów.</span><span class="sxs-lookup"><span data-stu-id="96608-124">This cmdlet supports paging via First and Skip parameters.</span></span>

<span data-ttu-id="96608-125">Możesz również pobrać pojedynczą komunikację biletów pomocy technicznej, podając nazwę komunikacji.</span><span class="sxs-lookup"><span data-stu-id="96608-125">You can also retrieve a single support ticket communication by specifying the communication name.</span></span> 

## <span data-ttu-id="96608-126">Przykłady</span><span class="sxs-lookup"><span data-stu-id="96608-126">EXAMPLES</span></span>

### <span data-ttu-id="96608-127">Przykład 1: pobieranie całej komunikacji za pomocą biletu pomocy technicznej</span><span class="sxs-lookup"><span data-stu-id="96608-127">Example 1: Retrieve all communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
testmessage1 user@contoso.com     test message   2/4/2020 9:35:42 PM
```

### <span data-ttu-id="96608-128">Przykład 2: pobieranie pojedynczej komunikacji za pomocą nazwy dla biletu pomocy technicznej</span><span class="sxs-lookup"><span data-stu-id="96608-128">Example 2: Retrieve a single communication by it's name for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Name "testmessage1"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage1 user@contoso.com     test message   2/4/2020 9:38:14 PM
```

### <span data-ttu-id="96608-129">Przykład 3: pobieranie pierwszych 2 wiadomości na bilet pomocy technicznej</span><span class="sxs-lookup"><span data-stu-id="96608-129">Example 3: Retrieve first 2 communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -First 2

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="96608-130">Przykład 4: pobieranie następnej 2 wiadomości po pominięciu pierwszych 2 wiadomości w przypadku biletu pomocy technicznej</span><span class="sxs-lookup"><span data-stu-id="96608-130">Example 4: Retrieve next 2 communications after skipping first 2 communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Skip 2 -First 2

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage4 user@contoso.com     test message4  2/4/2020 9:38:14 PM
testmessage5 user@contoso.com     test message5  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="96608-131">Przykład 5: pobieranie wszystkich wiadomości w sieci Web dla biletu pomocy technicznej</span><span class="sxs-lookup"><span data-stu-id="96608-131">Example 5: Retrieve all Web communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CommunicationType eq 'Web'"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="96608-132">Przykład 6: pobieranie wszystkich wiadomości utworzonych w dniu lub po 20 grudnia 2019 dla biletu pomocy technicznej</span><span class="sxs-lookup"><span data-stu-id="96608-132">Example 6: Retrieve all communications created on or after Dec 20th, 2019 for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CreatedDate ge 2019-12-20"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="96608-133">Przykład 7: pobieranie całej komunikacji w sieci Web utworzonej w dniu lub po 20 grudnia 2019 r. na bilet pomocy technicznej</span><span class="sxs-lookup"><span data-stu-id="96608-133">Example 7: Retrieve all Web communications created on or after Dec 20th, 2019 for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CommunicationType eq 'Web' and CreatedDate ge 2019-12-20"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="96608-134">Przykład 8: pobieranie całej komunikacji dla biletu pomocy technicznej przez obiekt biletu pomocy technicznej dla połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="96608-134">Example 8: Retrieve all communications for a support ticket by piping support ticket object</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Get-AzSupportTicketCommunication

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
testmessage1 user@contoso.com     test message   2/4/2020 9:35:42 PM
```

## <span data-ttu-id="96608-135">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="96608-135">PARAMETERS</span></span>

### <span data-ttu-id="96608-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96608-136">-DefaultProfile</span></span>
<span data-ttu-id="96608-137">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="96608-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96608-138">-Filter</span><span class="sxs-lookup"><span data-stu-id="96608-138">-Filter</span></span>
<span data-ttu-id="96608-139">Filtr, który ma zostać zastosowany do wyników tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96608-139">Filter to be applied to the results of this cmdlet.</span></span>

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

### <span data-ttu-id="96608-140">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="96608-140">-Name</span></span>
<span data-ttu-id="96608-141">Nazwa komunikacji.</span><span class="sxs-lookup"><span data-stu-id="96608-141">Communication name.</span></span>

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

### <span data-ttu-id="96608-142">-SupportTicketName</span><span class="sxs-lookup"><span data-stu-id="96608-142">-SupportTicketName</span></span>
<span data-ttu-id="96608-143">Nazwa biletu pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="96608-143">Support ticket name.</span></span>

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

### <span data-ttu-id="96608-144">-SupportTicketObject</span><span class="sxs-lookup"><span data-stu-id="96608-144">-SupportTicketObject</span></span>
<span data-ttu-id="96608-145">Obiekt biletu pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="96608-145">Support ticket object.</span></span>

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

### <span data-ttu-id="96608-146">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="96608-146">-IncludeTotalCount</span></span>
<span data-ttu-id="96608-147">Wyświetla całkowitą liczbę obiektów w zbiorze danych (liczba całkowita), a następnie zaznaczone obiekty.</span><span class="sxs-lookup"><span data-stu-id="96608-147">Reports the total number of objects in the data set (an integer) followed by the selected objects.</span></span>
<span data-ttu-id="96608-148">Jeśli polecenie cmdlet nie może ustalić całkowitej liczby, zostanie wyświetlona "Łączna liczba nieznanych".</span><span class="sxs-lookup"><span data-stu-id="96608-148">If the cmdlet cannot determine the total count, it displays "Unknown total count."</span></span> <span data-ttu-id="96608-149">Liczba całkowita ma właściwość dokładność wskazującą wiarygodność całkowitej wartości licznika.</span><span class="sxs-lookup"><span data-stu-id="96608-149">The integer has an Accuracy property that indicates the reliability of the total count value.</span></span>
<span data-ttu-id="96608-150">Wartość zakresu dokładności od 0,0 do 1,0 w przypadku, gdy 0,0 oznacza, że nie można zliczyć obiektów przez polecenie cmdlet, 1,0 oznacza, że liczba jest dokładna, a wartość między 0,0 a 1,0 wskazuje coraz bardziej niezawodny szacunek.</span><span class="sxs-lookup"><span data-stu-id="96608-150">The value of Accuracy ranges from 0.0 to 1.0 where 0.0 means that the cmdlet could not count the objects, 1.0 means that the count is exact, and a value between 0.0 and 1.0 indicates an increasingly reliable estimate.</span></span>

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

### <span data-ttu-id="96608-151">-Skip</span><span class="sxs-lookup"><span data-stu-id="96608-151">-Skip</span></span>
<span data-ttu-id="96608-152">Ignoruje określoną liczbę obiektów, a następnie pobiera pozostałe obiekty.</span><span class="sxs-lookup"><span data-stu-id="96608-152">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="96608-153">Wprowadź liczbę obiektów, które mają zostać pominięte.</span><span class="sxs-lookup"><span data-stu-id="96608-153">Enter the number of objects to skip.</span></span>

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

### <span data-ttu-id="96608-154">-First</span><span class="sxs-lookup"><span data-stu-id="96608-154">-First</span></span>
<span data-ttu-id="96608-155">Pobiera tylko określoną liczbę obiektów.</span><span class="sxs-lookup"><span data-stu-id="96608-155">Gets only the specified number of objects.</span></span>
<span data-ttu-id="96608-156">Wprowadź liczbę obiektów do pobrania.</span><span class="sxs-lookup"><span data-stu-id="96608-156">Enter the number of objects to get.</span></span>

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

### <span data-ttu-id="96608-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96608-157">CommonParameters</span></span>
<span data-ttu-id="96608-158">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96608-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96608-159">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="96608-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96608-160">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="96608-160">INPUTS</span></span>

### <span data-ttu-id="96608-161">Microsoft. Azure. Commands. support. models. PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="96608-161">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="96608-162">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="96608-162">OUTPUTS</span></span>

### <span data-ttu-id="96608-163">Microsoft. Azure. Commands. support. models. PSSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="96608-163">Microsoft.Azure.Commands.Support.Models.PSSupportTicketCommunication</span></span>

## <span data-ttu-id="96608-164">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="96608-164">NOTES</span></span>

## <span data-ttu-id="96608-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="96608-165">RELATED LINKS</span></span>
