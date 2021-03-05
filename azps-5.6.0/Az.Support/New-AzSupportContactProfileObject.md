---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/powershell/module/az.support/new-azsupportcontactprofileobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportContactProfileObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportContactProfileObject.md
ms.openlocfilehash: 5b2dfbc472b128a12f108aafc92aa9d30b661255
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002161"
---
# <span data-ttu-id="b323a-101">New-AzSupportContactProfileObject</span><span class="sxs-lookup"><span data-stu-id="b323a-101">New-AzSupportContactProfileObject</span></span>

## <span data-ttu-id="b323a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b323a-102">SYNOPSIS</span></span>
<span data-ttu-id="b323a-103">Tworzy obiekt profilu kontaktu pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="b323a-103">Creates a support contact profile object.</span></span>

## <span data-ttu-id="b323a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b323a-104">SYNTAX</span></span>

```
New-AzSupportContactProfileObject -FirstName <String> -LastName <String>
 -PreferredContactMethod <ContactMethod> -PrimaryEmailAddress <String> [-AdditionalEmailAddress <String[]>]
 [-PhoneNumber <String>] -PreferredTimeZone <String> -Country <String> -PreferredSupportLanguage <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b323a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b323a-105">DESCRIPTION</span></span>
<span data-ttu-id="b323a-106">Jest to polecenie cmdlet pomocy, za pomocą których można utworzyć obiekt profilu kontaktu pomocy technicznej podczas tworzenia lub aktualizowania biletu pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="b323a-106">This is a helper cmdlet that you can use to create a support contact profile object when creating or updating a support ticket.</span></span> <span data-ttu-id="b323a-107">Aby utworzyć zgłoszenie do pomocy technicznej, musisz określić następujące parametry, które są obowiązkowe:</span><span class="sxs-lookup"><span data-stu-id="b323a-107">You must specify the following parameters which are mandatory for creating a support ticket:</span></span> 

    • FirstName
    • LastName
    • PrimaryEmailAddress
    • PreferredContactMethod
    • Country
    • PreferredSupportLanguage
    • PreferredTimeZone

## <span data-ttu-id="b323a-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b323a-108">EXAMPLES</span></span>

### <span data-ttu-id="b323a-109">Przykład 1. Tworzenie obiektu kontaktu</span><span class="sxs-lookup"><span data-stu-id="b323a-109">Example 1: Create a contact object</span></span>
```powershell
PS C:\> New-AzSupportContactProfileObject -FirstName "First" -LastName "Last" -PreferredContactMethod "Email" -PrimaryEmailAddress "user@contoso.com" -PreferredTimeZone "Pacific Standard Time" -PreferredSupportLanguage "en-US" -Country "USA"             

FirstName LastName PreferredContactMethod PrimaryEmailAddress  PhoneNumber PreferredTimeZone     Country PreferredSupportLanguage
--------- -------- ---------------------- -------------------  ----------- -----------------     ------- ------------------------
First     Last     Email                  user@contoso.com                 Pacific Standard Time USA     en-US
```

## <span data-ttu-id="b323a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b323a-110">PARAMETERS</span></span>

### <span data-ttu-id="b323a-111">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="b323a-111">-AdditionalEmailAddress</span></span>
<span data-ttu-id="b323a-112">Wymienione tutaj adresy e-mail zostaną skopiowane w przypadku każdej korespondencji dotyczącej zgłoszenia do pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="b323a-112">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b323a-113">— Kraj</span><span class="sxs-lookup"><span data-stu-id="b323a-113">-Country</span></span>
<span data-ttu-id="b323a-114">Kraj klienta.</span><span class="sxs-lookup"><span data-stu-id="b323a-114">Customer country.</span></span>
<span data-ttu-id="b323a-115">Ten kod musi być prawidłowym kodem iso Alfa-3 (ISO 3166).</span><span class="sxs-lookup"><span data-stu-id="b323a-115">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b323a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b323a-116">-DefaultProfile</span></span>
<span data-ttu-id="b323a-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b323a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b323a-118">-FirstName</span><span class="sxs-lookup"><span data-stu-id="b323a-118">-FirstName</span></span>
<span data-ttu-id="b323a-119">Imię klienta.</span><span class="sxs-lookup"><span data-stu-id="b323a-119">Customer first name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b323a-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="b323a-120">-LastName</span></span>
<span data-ttu-id="b323a-121">Nazwisko klienta.</span><span class="sxs-lookup"><span data-stu-id="b323a-121">Customer last name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b323a-122">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="b323a-122">-PhoneNumber</span></span>
<span data-ttu-id="b323a-123">Numer telefonu klienta.</span><span class="sxs-lookup"><span data-stu-id="b323a-123">Customer phone number.</span></span>
<span data-ttu-id="b323a-124">Jest to wymagane, jeśli preferowaną metodą kontaktu jest telefon.</span><span class="sxs-lookup"><span data-stu-id="b323a-124">This is required if preferred contact method is phone.</span></span>

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

### <span data-ttu-id="b323a-125">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="b323a-125">-PreferredContactMethod</span></span>
<span data-ttu-id="b323a-126">Preferowana metoda kontaktu.</span><span class="sxs-lookup"><span data-stu-id="b323a-126">Preferred contact method.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.ContactMethod
Parameter Sets: (All)
Aliases:
Accepted values: Email, Phone

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b323a-127">-PreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="b323a-127">-PreferredSupportLanguage</span></span>
<span data-ttu-id="b323a-128">Preferowany język pomocy technicznej klienta.</span><span class="sxs-lookup"><span data-stu-id="b323a-128">Customer preferred support language.</span></span>
<span data-ttu-id="b323a-129">Ten kod musi być prawidłowym kodem języka dla jednego z obsługiwanych języków wymienionych https://azure.microsoft.com/support/faq/ tutaj.</span><span class="sxs-lookup"><span data-stu-id="b323a-129">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/support/faq/.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b323a-130">-PreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="b323a-130">-PreferredTimeZone</span></span>
<span data-ttu-id="b323a-131">Preferowana strefa czasowa klienta.</span><span class="sxs-lookup"><span data-stu-id="b323a-131">Customer preferred time zone.</span></span>
<span data-ttu-id="b323a-132">Musi to być prawidłowa System.TimeZoneInfo.Id wartości.</span><span class="sxs-lookup"><span data-stu-id="b323a-132">This must be a valid System.TimeZoneInfo.Id value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b323a-133">-PrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="b323a-133">-PrimaryEmailAddress</span></span>
<span data-ttu-id="b323a-134">Podstawowy adres e-mail klienta.</span><span class="sxs-lookup"><span data-stu-id="b323a-134">Customer primary email address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b323a-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b323a-135">-Confirm</span></span>
<span data-ttu-id="b323a-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b323a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b323a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b323a-137">-WhatIf</span></span>
<span data-ttu-id="b323a-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b323a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b323a-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b323a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b323a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b323a-140">CommonParameters</span></span>
<span data-ttu-id="b323a-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b323a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b323a-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b323a-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b323a-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b323a-143">INPUTS</span></span>

### <span data-ttu-id="b323a-144">Brak</span><span class="sxs-lookup"><span data-stu-id="b323a-144">None</span></span>

## <span data-ttu-id="b323a-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b323a-145">OUTPUTS</span></span>

### <span data-ttu-id="b323a-146">Microsoft.Azure.Commands.Support.Models.PSContactProfile</span><span class="sxs-lookup"><span data-stu-id="b323a-146">Microsoft.Azure.Commands.Support.Models.PSContactProfile</span></span>

## <span data-ttu-id="b323a-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b323a-147">NOTES</span></span>

## <span data-ttu-id="b323a-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b323a-148">RELATED LINKS</span></span>
