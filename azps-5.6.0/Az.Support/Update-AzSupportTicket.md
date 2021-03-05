---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/powershell/module/az.support/update-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Update-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Update-AzSupportTicket.md
ms.openlocfilehash: 5fac9eac7225364af7c884ab64a80d4299939ec0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005025"
---
# <span data-ttu-id="0d04c-101">Update-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="0d04c-101">Update-AzSupportTicket</span></span>

## <span data-ttu-id="0d04c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d04c-102">SYNOPSIS</span></span>
<span data-ttu-id="0d04c-103">Bilet pomocy technicznej aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="0d04c-103">Updates support ticket.</span></span>

## <span data-ttu-id="0d04c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0d04c-104">SYNTAX</span></span>

### <span data-ttu-id="0d04c-105">UpdateByNameWithContactDetailParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="0d04c-105">UpdateByNameWithContactDetailParameterSet (Default)</span></span>
```
Update-AzSupportTicket -Name <String> [-Severity <Severity>] [-Status <Status>] [-CustomerFirstName <String>]
 [-CustomerLastName <String>] [-PreferredContactMethod <ContactMethod>] [-CustomerPrimaryEmailAddress <String>]
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] [-CustomerPreferredTimeZone <String>]
 [-CustomerCountry <String>] [-CustomerPreferredSupportLanguage <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d04c-106">UpdateByNameWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d04c-106">UpdateByNameWithContactObjectParameterSet</span></span>
```
Update-AzSupportTicket -Name <String> [-Severity <Severity>] [-Status <Status>] -CustomerContactDetail <PSContactProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d04c-107">UpdateByInputObjectWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d04c-107">UpdateByInputObjectWithContactDetailParameterSet</span></span>
```
Update-AzSupportTicket -InputObject <PSSupportTicket> [-Severity <Severity>] [-Status <Status>] [-CustomerFirstName <String>]
 [-CustomerLastName <String>] [-PreferredContactMethod <ContactMethod>] [-CustomerPrimaryEmailAddress <String>]
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] [-CustomerPreferredTimeZone <String>]
 [-CustomerCountry <String>] [-CustomerPreferredSupportLanguage <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d04c-108">UpdateByInputObjectWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d04c-108">UpdateByInputObjectWithContactObjectParameterSet</span></span>
```
Update-AzSupportTicket -InputObject <PSSupportTicket> [-Severity <Severity>] [-Status <Status>]
 -CustomerContactDetail <PSContactProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0d04c-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="0d04c-109">DESCRIPTION</span></span>
<span data-ttu-id="0d04c-110">Użyj tego polecenia cmdlet, aby zaktualizować poziom ważności biletu pomocy technicznej, stan lub szczegóły kontaktowe klienta.</span><span class="sxs-lookup"><span data-stu-id="0d04c-110">Use this cmdlet to update a support ticket's severity level, status or customer contact details.</span></span> <span data-ttu-id="0d04c-111">Pamiętaj, że zaktualizowanie poziomu ważności lub stanu biletu pomocy technicznej nie jest dozwolone, gdy bilet jest przypisany do inżyniera pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="0d04c-111">Note that updating a support ticket's severity level or status is not allowed when the ticket is assigned to a support engineer.</span></span> <span data-ttu-id="0d04c-112">Jeśli chcesz zaktualizować poziom ważności lub stan po przypisaniu biletu, skontaktuj się z inżynierem pomocy technicznej, wysyłając komunikat w sprawie biletu.</span><span class="sxs-lookup"><span data-stu-id="0d04c-112">If you wish to update the severity level or status after ticket assignment, contact the support engineer by sending a communication on the ticket.</span></span>

## <span data-ttu-id="0d04c-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0d04c-113">EXAMPLES</span></span>

### <span data-ttu-id="0d04c-114">Przykład 1. Zaktualizuj ważność biletu pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="0d04c-114">Example 1: Update severity of support ticket.</span></span>
```powershell
PS C:\> Update-AzSupportTicket -Name "test1" -Severity "moderate"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="0d04c-115">Przykład 2. Aktualizowanie stanu zgłoszenia do pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="0d04c-115">Example 2: Update status of support ticket.</span></span>
```powershell
PS C:\> Update-AzSupportTicket -Name "test1" -Status "Closed"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Closed   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="0d04c-116">Przykład 3. Aktualizowanie szczegółów kontaktu biletu pomocy technicznej przez określenie obiektu kontaktu.</span><span class="sxs-lookup"><span data-stu-id="0d04c-116">Example 3: Update contact details of support ticket by specify contact object.</span></span>
```powershell
PS C:\> $contactDetail = new-object Microsoft.Azure.Commands.Support.Models.PSContactProfile
PS C:\> $contactDetail.FirstName = "first name updated"
PS C:\> $contactDetail.LastName = "last name updated"
PS C:\> Update-AzSupportTicket -Name "test1" -CustomerContactDetail $contactDetail 

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="0d04c-117">Przykład 4. Aktualizowanie ważności biletu pomocy technicznej przez obiekt biletu pomocy technicznej dla funkcji rurowych.</span><span class="sxs-lookup"><span data-stu-id="0d04c-117">Example 4: Update severity of support ticket by piping support ticket object.</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Update-AzSupportTicket -Severity "moderate"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="0d04c-118">Przykład 5. Zaktualizuj dane kontaktowe biletu pomocy technicznej, określając poszczególne parametry kontaktu.</span><span class="sxs-lookup"><span data-stu-id="0d04c-118">Example 5: Update contact details of support ticket by specifying individual contact parameters.</span></span>
```powershell
PS C:\> Update-AzSupportTicket -Name "test1" -CustomerFirstName "first name updated" -CustomerLastName "last name updated" -AdditionalEmailAddress @("user2@contoso.com") 

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="0d04c-119">Przykład 6. Aktualizowanie stanu biletu pomocy technicznej przez obiekt biletu pomocy technicznej dla połączenia rurowego.</span><span class="sxs-lookup"><span data-stu-id="0d04c-119">Example 6: Update status of support ticket by piping support ticket object.</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Update-AzSupportTicket -Status "Closed"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Closed   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="0d04c-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0d04c-120">PARAMETERS</span></span>

### <span data-ttu-id="0d04c-121">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="0d04c-121">-AdditionalEmailAddress</span></span>
<span data-ttu-id="0d04c-122">Dodatkowe adresy e-mail.</span><span class="sxs-lookup"><span data-stu-id="0d04c-122">Additional email addresses.</span></span>
<span data-ttu-id="0d04c-123">Wymienione tutaj adresy e-mail zostaną skopiowane w przypadku każdej korespondencji dotyczącej zgłoszenia do pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="0d04c-123">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

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

### <span data-ttu-id="0d04c-124">-CustomerContactDetail</span><span class="sxs-lookup"><span data-stu-id="0d04c-124">-CustomerContactDetail</span></span>
<span data-ttu-id="0d04c-125">Zaktualizuj dane kontaktowe w ketcie pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="0d04c-125">Update Contact details on SupportTicket.</span></span>

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

### <span data-ttu-id="0d04c-126">-CustomerCountry</span><span class="sxs-lookup"><span data-stu-id="0d04c-126">-CustomerCountry</span></span>
<span data-ttu-id="0d04c-127">Kraj klienta.</span><span class="sxs-lookup"><span data-stu-id="0d04c-127">Customer country.</span></span>
<span data-ttu-id="0d04c-128">Ten kod musi być prawidłowym kodem iso Alfa-3 (ISO 3166).</span><span class="sxs-lookup"><span data-stu-id="0d04c-128">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

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

### <span data-ttu-id="0d04c-129">-CustomerFirstName</span><span class="sxs-lookup"><span data-stu-id="0d04c-129">-CustomerFirstName</span></span>
<span data-ttu-id="0d04c-130">Imię klienta.</span><span class="sxs-lookup"><span data-stu-id="0d04c-130">Customer first name.</span></span>

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

### <span data-ttu-id="0d04c-131">-CustomerLastName</span><span class="sxs-lookup"><span data-stu-id="0d04c-131">-CustomerLastName</span></span>
<span data-ttu-id="0d04c-132">Nazwisko klienta.</span><span class="sxs-lookup"><span data-stu-id="0d04c-132">Customer last name.</span></span>

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

### <span data-ttu-id="0d04c-133">-CustomerPhoneNumber</span><span class="sxs-lookup"><span data-stu-id="0d04c-133">-CustomerPhoneNumber</span></span>
<span data-ttu-id="0d04c-134">Numer telefonu klienta.</span><span class="sxs-lookup"><span data-stu-id="0d04c-134">Customer phone number.</span></span>
<span data-ttu-id="0d04c-135">Jest to wymagane, jeśli preferowaną metodą kontaktu jest telefon.</span><span class="sxs-lookup"><span data-stu-id="0d04c-135">This is required if preferred contact method is phone.</span></span>

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

### <span data-ttu-id="0d04c-136">-CustomerPreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="0d04c-136">-CustomerPreferredSupportLanguage</span></span>
<span data-ttu-id="0d04c-137">Preferowany język pomocy technicznej klienta.</span><span class="sxs-lookup"><span data-stu-id="0d04c-137">Customer preferred support language.</span></span>
<span data-ttu-id="0d04c-138">Ten kod musi być prawidłowym kodem języka dla jednego z obsługiwanych języków wymienionych https://azure.microsoft.com/support/faq/ tutaj.</span><span class="sxs-lookup"><span data-stu-id="0d04c-138">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/support/faq/.</span></span>

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

### <span data-ttu-id="0d04c-139">-CustomerPreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="0d04c-139">-CustomerPreferredTimeZone</span></span>
<span data-ttu-id="0d04c-140">Preferowana strefa czasowa klienta.</span><span class="sxs-lookup"><span data-stu-id="0d04c-140">Customer preferred time zone.</span></span>
<span data-ttu-id="0d04c-141">Musi to być prawidłowa System.TimeZoneInfo.Id wartości.</span><span class="sxs-lookup"><span data-stu-id="0d04c-141">This must be a valid System.TimeZoneInfo.Id value.</span></span>

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

### <span data-ttu-id="0d04c-142">-CustomerPrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="0d04c-142">-CustomerPrimaryEmailAddress</span></span>
<span data-ttu-id="0d04c-143">Podstawowy adres e-mail klienta.</span><span class="sxs-lookup"><span data-stu-id="0d04c-143">Customer primary email address.</span></span>

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

### <span data-ttu-id="0d04c-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d04c-144">-DefaultProfile</span></span>
<span data-ttu-id="0d04c-145">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0d04c-145">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d04c-146">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0d04c-146">-InputObject</span></span>
<span data-ttu-id="0d04c-147">Obiekt zasobu SupportTicket aktualizowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d04c-147">SupportTicket resource object that this cmdlet updates.</span></span>

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

### <span data-ttu-id="0d04c-148">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0d04c-148">-Name</span></span>
<span data-ttu-id="0d04c-149">Nazwa zasobu SupportTicket, który aktualizuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d04c-149">Name of SupportTicket resource that this cmdlet updates.</span></span>

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

### <span data-ttu-id="0d04c-150">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="0d04c-150">-PreferredContactMethod</span></span>
<span data-ttu-id="0d04c-151">Preferowana metoda kontaktu.</span><span class="sxs-lookup"><span data-stu-id="0d04c-151">Preferred contact method.</span></span>

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

### <span data-ttu-id="0d04c-152">— Ważność</span><span class="sxs-lookup"><span data-stu-id="0d04c-152">-Severity</span></span>
<span data-ttu-id="0d04c-153">Ważność aktualizacji supportTicket.</span><span class="sxs-lookup"><span data-stu-id="0d04c-153">Update Severity of SupportTicket.</span></span>

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

### <span data-ttu-id="0d04c-154">— Status</span><span class="sxs-lookup"><span data-stu-id="0d04c-154">-Status</span></span>
<span data-ttu-id="0d04c-155">Zaktualizuj stan supportTicket.</span><span class="sxs-lookup"><span data-stu-id="0d04c-155">Update Status of SupportTicket.</span></span>

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

### <span data-ttu-id="0d04c-156">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0d04c-156">-Confirm</span></span>
<span data-ttu-id="0d04c-157">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0d04c-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d04c-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d04c-158">-WhatIf</span></span>
<span data-ttu-id="0d04c-159">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d04c-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d04c-160">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0d04c-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d04c-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d04c-161">CommonParameters</span></span>
<span data-ttu-id="0d04c-162">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d04c-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d04c-163">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0d04c-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d04c-164">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0d04c-164">INPUTS</span></span>

### <span data-ttu-id="0d04c-165">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="0d04c-165">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="0d04c-166">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0d04c-166">OUTPUTS</span></span>

### <span data-ttu-id="0d04c-167">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="0d04c-167">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="0d04c-168">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0d04c-168">NOTES</span></span>

## <span data-ttu-id="0d04c-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0d04c-169">RELATED LINKS</span></span>
