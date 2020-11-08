---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/new-azsupportcontactprofileobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportContactProfileObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportContactProfileObject.md
ms.openlocfilehash: 312fa24c8805664867d86bdaf38a01d287a3c499
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224131"
---
# <span data-ttu-id="1d4e6-101">New-AzSupportContactProfileObject</span><span class="sxs-lookup"><span data-stu-id="1d4e6-101">New-AzSupportContactProfileObject</span></span>

## <span data-ttu-id="1d4e6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1d4e6-102">SYNOPSIS</span></span>
<span data-ttu-id="1d4e6-103">Tworzy obiekt profilu kontaktu pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="1d4e6-103">Creates a support contact profile object.</span></span>

## <span data-ttu-id="1d4e6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1d4e6-104">SYNTAX</span></span>

```
New-AzSupportContactProfileObject -FirstName <String> -LastName <String>
 -PreferredContactMethod <ContactMethod> -PrimaryEmailAddress <String> [-AdditionalEmailAddress <String[]>]
 [-PhoneNumber <String>] -PreferredTimeZone <String> -Country <String> -PreferredSupportLanguage <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d4e6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1d4e6-105">DESCRIPTION</span></span>
<span data-ttu-id="1d4e6-106">To jest polecenie cmdlet pomocnika, którego można użyć do utworzenia obiektu profilu kontaktu pomocy technicznej podczas tworzenia lub aktualizowania biletu pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="1d4e6-106">This is a helper cmdlet that you can use to create a support contact profile object when creating or updating a support ticket.</span></span> <span data-ttu-id="1d4e6-107">Musisz określić następujące parametry, które są wymagane do utworzenia biletu pomocy technicznej:</span><span class="sxs-lookup"><span data-stu-id="1d4e6-107">You must specify the following parameters which are mandatory for creating a support ticket:</span></span> 

    • FirstName
    • LastName
    • PrimaryEmailAddress
    • PreferredContactMethod
    • Country
    • PreferredSupportLanguage
    • PreferredTimeZone

## <span data-ttu-id="1d4e6-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1d4e6-108">EXAMPLES</span></span>

### <span data-ttu-id="1d4e6-109">Przykład 1. Tworzenie obiektu Contact</span><span class="sxs-lookup"><span data-stu-id="1d4e6-109">Example 1: Create a contact object</span></span>
```powershell
PS C:\> New-AzSupportContactProfileObject -FirstName "First" -LastName "Last" -PreferredContactMethod "Email" -PrimaryEmailAddress "user@contoso.com" -PreferredTimeZone "Pacific Standard Time" -PreferredSupportLanguage "en-US" -Country "USA"             

FirstName LastName PreferredContactMethod PrimaryEmailAddress  PhoneNumber PreferredTimeZone     Country PreferredSupportLanguage
--------- -------- ---------------------- -------------------  ----------- -----------------     ------- ------------------------
First     Last     Email                  user@contoso.com                 Pacific Standard Time USA     en-US
```

## <span data-ttu-id="1d4e6-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1d4e6-110">PARAMETERS</span></span>

### <span data-ttu-id="1d4e6-111">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="1d4e6-111">-AdditionalEmailAddress</span></span>
<span data-ttu-id="1d4e6-112">Adresy e-mail wymienione tutaj zostaną skopiowane w dowolnej korespondencji na temat biletu pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="1d4e6-112">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

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

### <span data-ttu-id="1d4e6-113">-Country</span><span class="sxs-lookup"><span data-stu-id="1d4e6-113">-Country</span></span>
<span data-ttu-id="1d4e6-114">Kraj klienta.</span><span class="sxs-lookup"><span data-stu-id="1d4e6-114">Customer country.</span></span>
<span data-ttu-id="1d4e6-115">Musi to być prawidłowy kod kraju ISO alfa-3 (ISO 3166).</span><span class="sxs-lookup"><span data-stu-id="1d4e6-115">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

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

### <span data-ttu-id="1d4e6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d4e6-116">-DefaultProfile</span></span>
<span data-ttu-id="1d4e6-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1d4e6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d4e6-118">-FirstName</span><span class="sxs-lookup"><span data-stu-id="1d4e6-118">-FirstName</span></span>
<span data-ttu-id="1d4e6-119">Imię i nazwisko klienta.</span><span class="sxs-lookup"><span data-stu-id="1d4e6-119">Customer first name.</span></span>

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

### <span data-ttu-id="1d4e6-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="1d4e6-120">-LastName</span></span>
<span data-ttu-id="1d4e6-121">Nazwisko klienta.</span><span class="sxs-lookup"><span data-stu-id="1d4e6-121">Customer last name.</span></span>

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

### <span data-ttu-id="1d4e6-122">-Rachunek</span><span class="sxs-lookup"><span data-stu-id="1d4e6-122">-PhoneNumber</span></span>
<span data-ttu-id="1d4e6-123">Numer telefonu klienta.</span><span class="sxs-lookup"><span data-stu-id="1d4e6-123">Customer phone number.</span></span>
<span data-ttu-id="1d4e6-124">Jest to wymagane, jeśli preferowaną metodą kontaktu jest telefon.</span><span class="sxs-lookup"><span data-stu-id="1d4e6-124">This is required if preferred contact method is phone.</span></span>

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

### <span data-ttu-id="1d4e6-125">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="1d4e6-125">-PreferredContactMethod</span></span>
<span data-ttu-id="1d4e6-126">Preferowana metoda kontaktu.</span><span class="sxs-lookup"><span data-stu-id="1d4e6-126">Preferred contact method.</span></span>

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

### <span data-ttu-id="1d4e6-127">-PreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="1d4e6-127">-PreferredSupportLanguage</span></span>
<span data-ttu-id="1d4e6-128">Preferowany język obsługi klienta.</span><span class="sxs-lookup"><span data-stu-id="1d4e6-128">Customer preferred support language.</span></span>
<span data-ttu-id="1d4e6-129">Musi to być prawidłowy kod językowy dla jednego z obsługiwanych języków z listy https://azure.microsoft.com/support/faq/ .</span><span class="sxs-lookup"><span data-stu-id="1d4e6-129">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/support/faq/.</span></span>

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

### <span data-ttu-id="1d4e6-130">-PreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="1d4e6-130">-PreferredTimeZone</span></span>
<span data-ttu-id="1d4e6-131">Preferowana strefa czasowa klienta.</span><span class="sxs-lookup"><span data-stu-id="1d4e6-131">Customer preferred time zone.</span></span>
<span data-ttu-id="1d4e6-132">Ta wartość musi być prawidłową wartością System.TimeZoneInfo.Id.</span><span class="sxs-lookup"><span data-stu-id="1d4e6-132">This must be a valid System.TimeZoneInfo.Id value.</span></span>

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

### <span data-ttu-id="1d4e6-133">-PrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="1d4e6-133">-PrimaryEmailAddress</span></span>
<span data-ttu-id="1d4e6-134">Podstawowy adres e-mail klienta.</span><span class="sxs-lookup"><span data-stu-id="1d4e6-134">Customer primary email address.</span></span>

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

### <span data-ttu-id="1d4e6-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1d4e6-135">-Confirm</span></span>
<span data-ttu-id="1d4e6-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d4e6-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d4e6-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d4e6-137">-WhatIf</span></span>
<span data-ttu-id="1d4e6-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d4e6-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d4e6-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1d4e6-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d4e6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d4e6-140">CommonParameters</span></span>
<span data-ttu-id="1d4e6-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d4e6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d4e6-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1d4e6-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d4e6-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1d4e6-143">INPUTS</span></span>

### <span data-ttu-id="1d4e6-144">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="1d4e6-144">None</span></span>

## <span data-ttu-id="1d4e6-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1d4e6-145">OUTPUTS</span></span>

### <span data-ttu-id="1d4e6-146">Microsoft. Azure. Commands. support. models. PSContactProfile</span><span class="sxs-lookup"><span data-stu-id="1d4e6-146">Microsoft.Azure.Commands.Support.Models.PSContactProfile</span></span>

## <span data-ttu-id="1d4e6-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1d4e6-147">NOTES</span></span>

## <span data-ttu-id="1d4e6-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1d4e6-148">RELATED LINKS</span></span>
