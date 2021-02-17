---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/new-azsupportticketcommunication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicketCommunication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicketCommunication.md
ms.openlocfilehash: 3a0191e1df223427ec7d60dfd92f7607e2c171b0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182818"
---
# <span data-ttu-id="036f7-101">New-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="036f7-101">New-AzSupportTicketCommunication</span></span>

## <span data-ttu-id="036f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="036f7-102">SYNOPSIS</span></span>
<span data-ttu-id="036f7-103">Tworzy nowy bilet pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="036f7-103">Creates a new support ticket communication.</span></span>

## <span data-ttu-id="036f7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="036f7-104">SYNTAX</span></span>

### <span data-ttu-id="036f7-105">CreateByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="036f7-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSupportTicketCommunication -SupportTicketName <String> -Name <String> -Subject <String> -Body <String>
 [-Sender <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="036f7-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="036f7-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSupportTicketCommunication -SupportTicketObject <PSSupportTicket> -Name <String> -Subject <String>
 -Body <String> [-Sender <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="036f7-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="036f7-107">DESCRIPTION</span></span>
<span data-ttu-id="036f7-108">Dodaje nową komunikację z klientami do biletu pomocy technicznej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="036f7-108">Adds a new customer communication to an Azure support ticket.</span></span>

## <span data-ttu-id="036f7-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="036f7-109">EXAMPLES</span></span>

### <span data-ttu-id="036f7-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="036f7-110">Example 1</span></span>
```powershell
PS C:\> New-AzSupportTicketCommunication -Name "testmessage" -SupportTicketName "testticket" -Subject "test subject" -Body "test body" -Sender "user@contoso.com"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage  user@contoso.com     test subject   2/4/2020 9:38:14 PM
```

## <span data-ttu-id="036f7-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="036f7-111">PARAMETERS</span></span>

### <span data-ttu-id="036f7-112">— AsJob</span><span class="sxs-lookup"><span data-stu-id="036f7-112">-AsJob</span></span>
<span data-ttu-id="036f7-113">Uruchom polecenie cmdlet w tle.</span><span class="sxs-lookup"><span data-stu-id="036f7-113">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="036f7-114">— Treść</span><span class="sxs-lookup"><span data-stu-id="036f7-114">-Body</span></span>
<span data-ttu-id="036f7-115">Treść komunikacji.</span><span class="sxs-lookup"><span data-stu-id="036f7-115">Body of the communication.</span></span>

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

### <span data-ttu-id="036f7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="036f7-116">-DefaultProfile</span></span>
<span data-ttu-id="036f7-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="036f7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="036f7-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="036f7-118">-Name</span></span>
<span data-ttu-id="036f7-119">Nazwa zasobu komunikacji.</span><span class="sxs-lookup"><span data-stu-id="036f7-119">Name of the communication resource.</span></span>

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

### <span data-ttu-id="036f7-120">— Sender</span><span class="sxs-lookup"><span data-stu-id="036f7-120">-Sender</span></span>
<span data-ttu-id="036f7-121">Adres e-mail nadawcy.</span><span class="sxs-lookup"><span data-stu-id="036f7-121">Email address of the sender.</span></span>

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

### <span data-ttu-id="036f7-122">— Temat</span><span class="sxs-lookup"><span data-stu-id="036f7-122">-Subject</span></span>
<span data-ttu-id="036f7-123">Temat komunikacji.</span><span class="sxs-lookup"><span data-stu-id="036f7-123">Subject of the communication.</span></span>

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

### <span data-ttu-id="036f7-124">-SupportTicketName</span><span class="sxs-lookup"><span data-stu-id="036f7-124">-SupportTicketName</span></span>
<span data-ttu-id="036f7-125">Nazwa biletu pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="036f7-125">Support ticket name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="036f7-126">-SupportTicketObject</span><span class="sxs-lookup"><span data-stu-id="036f7-126">-SupportTicketObject</span></span>
<span data-ttu-id="036f7-127">Obiekt bilet pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="036f7-127">Support ticket object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSSupportTicket
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="036f7-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="036f7-128">-Confirm</span></span>
<span data-ttu-id="036f7-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="036f7-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="036f7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="036f7-130">-WhatIf</span></span>
<span data-ttu-id="036f7-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="036f7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="036f7-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="036f7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="036f7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="036f7-133">CommonParameters</span></span>
<span data-ttu-id="036f7-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="036f7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="036f7-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="036f7-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="036f7-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="036f7-136">INPUTS</span></span>

### <span data-ttu-id="036f7-137">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="036f7-137">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="036f7-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="036f7-138">OUTPUTS</span></span>

### <span data-ttu-id="036f7-139">Microsoft.Azure.Commands.Support.Models.PSSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="036f7-139">Microsoft.Azure.Commands.Support.Models.PSSupportTicketCommunication</span></span>

## <span data-ttu-id="036f7-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="036f7-140">NOTES</span></span>

## <span data-ttu-id="036f7-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="036f7-141">RELATED LINKS</span></span>
