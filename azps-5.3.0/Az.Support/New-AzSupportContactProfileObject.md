---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/new-azsupportcontactprofileobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportContactProfileObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportContactProfileObject.md
ms.openlocfilehash: 312fa24c8805664867d86bdaf38a01d287a3c499
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491138"
---
# <span data-ttu-id="bbf1d-101">New-AzSupportContactProfileObject</span><span class="sxs-lookup"><span data-stu-id="bbf1d-101">New-AzSupportContactProfileObject</span></span>

## <span data-ttu-id="bbf1d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bbf1d-102">SYNOPSIS</span></span>
<span data-ttu-id="bbf1d-103">Tworzy obiekt profilu kontaktu pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-103">Creates a support contact profile object.</span></span>

## <span data-ttu-id="bbf1d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bbf1d-104">SYNTAX</span></span>

```
New-AzSupportContactProfileObject -FirstName <String> -LastName <String>
 -PreferredContactMethod <ContactMethod> -PrimaryEmailAddress <String> [-AdditionalEmailAddress <String[]>]
 [-PhoneNumber <String>] -PreferredTimeZone <String> -Country <String> -PreferredSupportLanguage <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbf1d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bbf1d-105">DESCRIPTION</span></span>
<span data-ttu-id="bbf1d-106">To jest polecenie cmdlet pomocnika, którego można użyć do utworzenia obiektu profilu kontaktu pomocy technicznej podczas tworzenia lub aktualizowania biletu pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-106">This is a helper cmdlet that you can use to create a support contact profile object when creating or updating a support ticket.</span></span> <span data-ttu-id="bbf1d-107">Musisz określić następujące parametry, które są wymagane do utworzenia biletu pomocy technicznej:</span><span class="sxs-lookup"><span data-stu-id="bbf1d-107">You must specify the following parameters which are mandatory for creating a support ticket:</span></span> 

    • FirstName
    • LastName
    • PrimaryEmailAddress
    • PreferredContactMethod
    • Country
    • PreferredSupportLanguage
    • PreferredTimeZone

## <span data-ttu-id="bbf1d-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bbf1d-108">EXAMPLES</span></span>

### <span data-ttu-id="bbf1d-109">Przykład 1. Tworzenie obiektu Contact</span><span class="sxs-lookup"><span data-stu-id="bbf1d-109">Example 1: Create a contact object</span></span>
```powershell
PS C:\> New-AzSupportContactProfileObject -FirstName "First" -LastName "Last" -PreferredContactMethod "Email" -PrimaryEmailAddress "user@contoso.com" -PreferredTimeZone "Pacific Standard Time" -PreferredSupportLanguage "en-US" -Country "USA"             

FirstName LastName PreferredContactMethod PrimaryEmailAddress  PhoneNumber PreferredTimeZone     Country PreferredSupportLanguage
--------- -------- ---------------------- -------------------  ----------- -----------------     ------- ------------------------
First     Last     Email                  user@contoso.com                 Pacific Standard Time USA     en-US
```

## <span data-ttu-id="bbf1d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bbf1d-110">PARAMETERS</span></span>

### <span data-ttu-id="bbf1d-111">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="bbf1d-111">-AdditionalEmailAddress</span></span>
<span data-ttu-id="bbf1d-112">Adresy e-mail wymienione tutaj zostaną skopiowane w dowolnej korespondencji na temat biletu pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-112">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

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

### <span data-ttu-id="bbf1d-113">-Country</span><span class="sxs-lookup"><span data-stu-id="bbf1d-113">-Country</span></span>
<span data-ttu-id="bbf1d-114">Kraj klienta.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-114">Customer country.</span></span>
<span data-ttu-id="bbf1d-115">Musi to być prawidłowy kod kraju ISO alfa-3 (ISO 3166).</span><span class="sxs-lookup"><span data-stu-id="bbf1d-115">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

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

### <span data-ttu-id="bbf1d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbf1d-116">-DefaultProfile</span></span>
<span data-ttu-id="bbf1d-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbf1d-118">-FirstName</span><span class="sxs-lookup"><span data-stu-id="bbf1d-118">-FirstName</span></span>
<span data-ttu-id="bbf1d-119">Imię i nazwisko klienta.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-119">Customer first name.</span></span>

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

### <span data-ttu-id="bbf1d-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="bbf1d-120">-LastName</span></span>
<span data-ttu-id="bbf1d-121">Nazwisko klienta.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-121">Customer last name.</span></span>

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

### <span data-ttu-id="bbf1d-122">-Rachunek</span><span class="sxs-lookup"><span data-stu-id="bbf1d-122">-PhoneNumber</span></span>
<span data-ttu-id="bbf1d-123">Numer telefonu klienta.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-123">Customer phone number.</span></span>
<span data-ttu-id="bbf1d-124">Jest to wymagane, jeśli preferowaną metodą kontaktu jest telefon.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-124">This is required if preferred contact method is phone.</span></span>

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

### <span data-ttu-id="bbf1d-125">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="bbf1d-125">-PreferredContactMethod</span></span>
<span data-ttu-id="bbf1d-126">Preferowana metoda kontaktu.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-126">Preferred contact method.</span></span>

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

### <span data-ttu-id="bbf1d-127">-PreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="bbf1d-127">-PreferredSupportLanguage</span></span>
<span data-ttu-id="bbf1d-128">Preferowany język obsługi klienta.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-128">Customer preferred support language.</span></span>
<span data-ttu-id="bbf1d-129">Musi to być prawidłowy kod językowy dla jednego z obsługiwanych języków z listy https://azure.microsoft.com/support/faq/ .</span><span class="sxs-lookup"><span data-stu-id="bbf1d-129">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/support/faq/.</span></span>

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

### <span data-ttu-id="bbf1d-130">-PreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="bbf1d-130">-PreferredTimeZone</span></span>
<span data-ttu-id="bbf1d-131">Preferowana strefa czasowa klienta.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-131">Customer preferred time zone.</span></span>
<span data-ttu-id="bbf1d-132">Ta wartość musi być prawidłową wartością System.TimeZoneInfo.Id.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-132">This must be a valid System.TimeZoneInfo.Id value.</span></span>

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

### <span data-ttu-id="bbf1d-133">-PrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="bbf1d-133">-PrimaryEmailAddress</span></span>
<span data-ttu-id="bbf1d-134">Podstawowy adres e-mail klienta.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-134">Customer primary email address.</span></span>

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

### <span data-ttu-id="bbf1d-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bbf1d-135">-Confirm</span></span>
<span data-ttu-id="bbf1d-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbf1d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbf1d-137">-WhatIf</span></span>
<span data-ttu-id="bbf1d-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbf1d-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbf1d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbf1d-140">CommonParameters</span></span>
<span data-ttu-id="bbf1d-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbf1d-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bbf1d-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbf1d-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bbf1d-143">INPUTS</span></span>

### <span data-ttu-id="bbf1d-144">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="bbf1d-144">None</span></span>

## <span data-ttu-id="bbf1d-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bbf1d-145">OUTPUTS</span></span>

### <span data-ttu-id="bbf1d-146">Microsoft. Azure. Commands. support. models. PSContactProfile</span><span class="sxs-lookup"><span data-stu-id="bbf1d-146">Microsoft.Azure.Commands.Support.Models.PSContactProfile</span></span>

## <span data-ttu-id="bbf1d-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bbf1d-147">NOTES</span></span>

## <span data-ttu-id="bbf1d-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bbf1d-148">RELATED LINKS</span></span>
