---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/update-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Update-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Update-AzSupportTicket.md
ms.openlocfilehash: 160d6b4d4a8505c99d5bfcb4c535ec7bbb3b6dd3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94231620"
---
# <span data-ttu-id="8d5f7-101">Update-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="8d5f7-101">Update-AzSupportTicket</span></span>

## <span data-ttu-id="8d5f7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8d5f7-102">SYNOPSIS</span></span>
<span data-ttu-id="8d5f7-103">Umożliwia aktualizowanie biletu pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-103">Updates support ticket.</span></span>

## <span data-ttu-id="8d5f7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8d5f7-104">SYNTAX</span></span>

### <span data-ttu-id="8d5f7-105">UpdateByNameWithContactDetailParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8d5f7-105">UpdateByNameWithContactDetailParameterSet (Default)</span></span>
```
Update-AzSupportTicket -Name <String> [-Severity <Severity>] [-Status <Status>] [-CustomerFirstName <String>]
 [-CustomerLastName <String>] [-PreferredContactMethod <ContactMethod>] [-CustomerPrimaryEmailAddress <String>]
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] [-CustomerPreferredTimeZone <String>]
 [-CustomerCountry <String>] [-CustomerPreferredSupportLanguage <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d5f7-106">UpdateByNameWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d5f7-106">UpdateByNameWithContactObjectParameterSet</span></span>
```
Update-AzSupportTicket -Name <String> [-Severity <Severity>] [-Status <Status>] -CustomerContactDetail <PSContactProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d5f7-107">UpdateByInputObjectWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d5f7-107">UpdateByInputObjectWithContactDetailParameterSet</span></span>
```
Update-AzSupportTicket -InputObject <PSSupportTicket> [-Severity <Severity>] [-Status <Status>] [-CustomerFirstName <String>]
 [-CustomerLastName <String>] [-PreferredContactMethod <ContactMethod>] [-CustomerPrimaryEmailAddress <String>]
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] [-CustomerPreferredTimeZone <String>]
 [-CustomerCountry <String>] [-CustomerPreferredSupportLanguage <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d5f7-108">UpdateByInputObjectWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d5f7-108">UpdateByInputObjectWithContactObjectParameterSet</span></span>
```
Update-AzSupportTicket -InputObject <PSSupportTicket> [-Severity <Severity>] [-Status <Status>]
 -CustomerContactDetail <PSContactProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8d5f7-109">Opis</span><span class="sxs-lookup"><span data-stu-id="8d5f7-109">DESCRIPTION</span></span>
<span data-ttu-id="8d5f7-110">Za pomocą tego polecenia cmdlet można zaktualizować poziom ważności biletu pomocy technicznej, status lub dane kontaktowe klienta.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-110">Use this cmdlet to update a support ticket's severity level, status or customer contact details.</span></span> <span data-ttu-id="8d5f7-111">Zwróć uwagę, że zaktualizowanie poziomu ważności biletu pomocy technicznej lub statusu nie jest dozwolone, gdy bilet jest przypisany do inżyniera pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-111">Note that updating a support ticket's severity level or status is not allowed when the ticket is assigned to a support engineer.</span></span> <span data-ttu-id="8d5f7-112">Jeśli chcesz zaktualizować poziom ważności lub status po przypisaniu biletu, skontaktuj się z pracownikiem pomocy technicznej, wysyłając wiadomość na bilet.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-112">If you wish to update the severity level or status after ticket assignment, contact the support engineer by sending a communication on the ticket.</span></span>

## <span data-ttu-id="8d5f7-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8d5f7-113">EXAMPLES</span></span>

### <span data-ttu-id="8d5f7-114">Przykład 1: Aktualizacja ważność biletu pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-114">Example 1: Update severity of support ticket.</span></span>
```powershell
PS C:\> Update-AzSupportTicket -Name "test1" -Severity "moderate"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="8d5f7-115">Przykład 2: zaktualizowanie statusu biletu pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-115">Example 2: Update status of support ticket.</span></span>
```powershell
PS C:\> Update-AzSupportTicket -Name "test1" -Status "Closed"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Closed   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="8d5f7-116">Przykład 3: aktualizowanie danych kontaktu dotyczących biletu pomocy technicznej przez określenie obiektu kontaktu.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-116">Example 3: Update contact details of support ticket by specify contact object.</span></span>
```powershell
PS C:\> $contactDetail = new-object Microsoft.Azure.Commands.Support.Models.PSContactProfile
PS C:\> $contactDetail.FirstName = "first name updated"
PS C:\> $contactDetail.LastName = "last name updated"
PS C:\> Update-AzSupportTicket -Name "test1" -CustomerContactDetail $contactDetail 

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="8d5f7-117">Przykład 4: Aktualizacja ważność biletu pomocy technicznej dzięki obiektowi biletu pomocy technicznej dla połączeń rurowych.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-117">Example 4: Update severity of support ticket by piping support ticket object.</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Update-AzSupportTicket -Severity "moderate"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="8d5f7-118">Przykład 5: aktualizowanie danych kontaktowych dotyczących biletu pomocy technicznej przez określenie indywidualnych parametrów kontaktu.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-118">Example 5: Update contact details of support ticket by specifying individual contact parameters.</span></span>
```powershell
PS C:\> Update-AzSupportTicket -Name "test1" -CustomerFirstName "first name updated" -CustomerLastName "last name updated" -AdditionalEmailAddress @("user2@contoso.com") 

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="8d5f7-119">Przykład 6: aktualizowanie stanu biletu pomocy technicznej przez obiekt biletu pomocy technicznej dla połączeń rurowych.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-119">Example 6: Update status of support ticket by piping support ticket object.</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Update-AzSupportTicket -Status "Closed"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Closed   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="8d5f7-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8d5f7-120">PARAMETERS</span></span>

### <span data-ttu-id="8d5f7-121">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="8d5f7-121">-AdditionalEmailAddress</span></span>
<span data-ttu-id="8d5f7-122">Dodatkowe adresy e-mail.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-122">Additional email addresses.</span></span>
<span data-ttu-id="8d5f7-123">Adresy e-mail wymienione tutaj zostaną skopiowane w dowolnej korespondencji na temat biletu pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-123">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

```yaml
Type: System.String[]
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d5f7-124">-CustomerContactDetail</span><span class="sxs-lookup"><span data-stu-id="8d5f7-124">-CustomerContactDetail</span></span>
<span data-ttu-id="8d5f7-125">Zaktualizuj szczegółowe dane kontaktowe w witrynie SupportTicket.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-125">Update Contact details on SupportTicket.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSContactProfile
Parameter Sets: UpdateByNameWithContactObjectParameterSet, UpdateByInputObjectWithContactObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d5f7-126">-CustomerCountry</span><span class="sxs-lookup"><span data-stu-id="8d5f7-126">-CustomerCountry</span></span>
<span data-ttu-id="8d5f7-127">Kraj klienta.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-127">Customer country.</span></span>
<span data-ttu-id="8d5f7-128">Musi to być prawidłowy kod kraju ISO alfa-3 (ISO 3166).</span><span class="sxs-lookup"><span data-stu-id="8d5f7-128">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d5f7-129">-CustomerFirstName</span><span class="sxs-lookup"><span data-stu-id="8d5f7-129">-CustomerFirstName</span></span>
<span data-ttu-id="8d5f7-130">Imię i nazwisko klienta.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-130">Customer first name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d5f7-131">-CustomerLastName</span><span class="sxs-lookup"><span data-stu-id="8d5f7-131">-CustomerLastName</span></span>
<span data-ttu-id="8d5f7-132">Nazwisko klienta.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-132">Customer last name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d5f7-133">-CustomerPhoneNumber</span><span class="sxs-lookup"><span data-stu-id="8d5f7-133">-CustomerPhoneNumber</span></span>
<span data-ttu-id="8d5f7-134">Numer telefonu klienta.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-134">Customer phone number.</span></span>
<span data-ttu-id="8d5f7-135">Jest to wymagane, jeśli preferowaną metodą kontaktu jest telefon.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-135">This is required if preferred contact method is phone.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d5f7-136">-CustomerPreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="8d5f7-136">-CustomerPreferredSupportLanguage</span></span>
<span data-ttu-id="8d5f7-137">Preferowany język obsługi klienta.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-137">Customer preferred support language.</span></span>
<span data-ttu-id="8d5f7-138">Musi to być prawidłowy kod językowy dla jednego z obsługiwanych języków z listy https://azure.microsoft.com/support/faq/ .</span><span class="sxs-lookup"><span data-stu-id="8d5f7-138">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/support/faq/.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d5f7-139">-CustomerPreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="8d5f7-139">-CustomerPreferredTimeZone</span></span>
<span data-ttu-id="8d5f7-140">Preferowana strefa czasowa klienta.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-140">Customer preferred time zone.</span></span>
<span data-ttu-id="8d5f7-141">Ta wartość musi być prawidłową wartością System.TimeZoneInfo.Id.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-141">This must be a valid System.TimeZoneInfo.Id value.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d5f7-142">-CustomerPrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="8d5f7-142">-CustomerPrimaryEmailAddress</span></span>
<span data-ttu-id="8d5f7-143">Podstawowy adres e-mail klienta.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-143">Customer primary email address.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d5f7-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d5f7-144">-DefaultProfile</span></span>
<span data-ttu-id="8d5f7-145">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-145">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d5f7-146">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8d5f7-146">-InputObject</span></span>
<span data-ttu-id="8d5f7-147">Obiekt zasobu SupportTicket, który jest aktualizowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-147">SupportTicket resource object that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSSupportTicket
Parameter Sets: UpdateByInputObjectWithContactDetailParameterSet, UpdateByInputObjectWithContactObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d5f7-148">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8d5f7-148">-Name</span></span>
<span data-ttu-id="8d5f7-149">Nazwa zasobu SupportTicket, który jest aktualizowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-149">Name of SupportTicket resource that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByNameWithContactObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d5f7-150">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="8d5f7-150">-PreferredContactMethod</span></span>
<span data-ttu-id="8d5f7-151">Preferowana metoda kontaktu.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-151">Preferred contact method.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.ContactMethod
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:
Accepted values: Email, Phone

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d5f7-152">— Ważność</span><span class="sxs-lookup"><span data-stu-id="8d5f7-152">-Severity</span></span>
<span data-ttu-id="8d5f7-153">Aktualizuj ważność SupportTicket.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-153">Update Severity of SupportTicket.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.Severity
Parameter Sets: (All)
Aliases:
Accepted values: Minimal, Moderate, Critical, HighestCriticalImpact

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d5f7-154">-Status</span><span class="sxs-lookup"><span data-stu-id="8d5f7-154">-Status</span></span>
<span data-ttu-id="8d5f7-155">Zaktualizuj stan SupportTicket.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-155">Update Status of SupportTicket.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.Status
Parameter Sets: (All)
Aliases:
Accepted values: Open, Closed

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d5f7-156">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8d5f7-156">-Confirm</span></span>
<span data-ttu-id="8d5f7-157">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-157">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d5f7-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d5f7-158">-WhatIf</span></span>
<span data-ttu-id="8d5f7-159">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d5f7-160">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-160">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d5f7-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d5f7-161">CommonParameters</span></span>
<span data-ttu-id="8d5f7-162">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d5f7-163">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8d5f7-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d5f7-164">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8d5f7-164">INPUTS</span></span>

### <span data-ttu-id="8d5f7-165">Microsoft. Azure. Commands. support. models. PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="8d5f7-165">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="8d5f7-166">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8d5f7-166">OUTPUTS</span></span>

### <span data-ttu-id="8d5f7-167">Microsoft. Azure. Commands. support. models. PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="8d5f7-167">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="8d5f7-168">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8d5f7-168">NOTES</span></span>

## <span data-ttu-id="8d5f7-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8d5f7-169">RELATED LINKS</span></span>
