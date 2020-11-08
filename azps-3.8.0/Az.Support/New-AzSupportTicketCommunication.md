---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/new-azsupportticketcommunication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicketCommunication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicketCommunication.md
ms.openlocfilehash: 3a0191e1df223427ec7d60dfd92f7607e2c171b0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050626"
---
# <span data-ttu-id="5d9df-101">New-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="5d9df-101">New-AzSupportTicketCommunication</span></span>

## <span data-ttu-id="5d9df-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5d9df-102">SYNOPSIS</span></span>
<span data-ttu-id="5d9df-103">Tworzy nową komunikację biletów pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="5d9df-103">Creates a new support ticket communication.</span></span>

## <span data-ttu-id="5d9df-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5d9df-104">SYNTAX</span></span>

### <span data-ttu-id="5d9df-105">CreateByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5d9df-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSupportTicketCommunication -SupportTicketName <String> -Name <String> -Subject <String> -Body <String>
 [-Sender <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5d9df-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d9df-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSupportTicketCommunication -SupportTicketObject <PSSupportTicket> -Name <String> -Subject <String>
 -Body <String> [-Sender <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5d9df-107">Opis</span><span class="sxs-lookup"><span data-stu-id="5d9df-107">DESCRIPTION</span></span>
<span data-ttu-id="5d9df-108">Dodaje nową komunikację z klientem do biletu pomocy technicznej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5d9df-108">Adds a new customer communication to an Azure support ticket.</span></span>

## <span data-ttu-id="5d9df-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5d9df-109">EXAMPLES</span></span>

### <span data-ttu-id="5d9df-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5d9df-110">Example 1</span></span>
```powershell
PS C:\> New-AzSupportTicketCommunication -Name "testmessage" -SupportTicketName "testticket" -Subject "test subject" -Body "test body" -Sender "user@contoso.com"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage  user@contoso.com     test subject   2/4/2020 9:38:14 PM
```

## <span data-ttu-id="5d9df-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5d9df-111">PARAMETERS</span></span>

### <span data-ttu-id="5d9df-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5d9df-112">-AsJob</span></span>
<span data-ttu-id="5d9df-113">Uruchom polecenie cmdlet w tle.</span><span class="sxs-lookup"><span data-stu-id="5d9df-113">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="5d9df-114">-Body</span><span class="sxs-lookup"><span data-stu-id="5d9df-114">-Body</span></span>
<span data-ttu-id="5d9df-115">Treść komunikatu.</span><span class="sxs-lookup"><span data-stu-id="5d9df-115">Body of the communication.</span></span>

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

### <span data-ttu-id="5d9df-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d9df-116">-DefaultProfile</span></span>
<span data-ttu-id="5d9df-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5d9df-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d9df-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5d9df-118">-Name</span></span>
<span data-ttu-id="5d9df-119">Nazwa zasobu komunikacyjnego.</span><span class="sxs-lookup"><span data-stu-id="5d9df-119">Name of the communication resource.</span></span>

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

### <span data-ttu-id="5d9df-120">-Nadawca</span><span class="sxs-lookup"><span data-stu-id="5d9df-120">-Sender</span></span>
<span data-ttu-id="5d9df-121">Adres e-mail nadawcy.</span><span class="sxs-lookup"><span data-stu-id="5d9df-121">Email address of the sender.</span></span>

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

### <span data-ttu-id="5d9df-122">— Temat</span><span class="sxs-lookup"><span data-stu-id="5d9df-122">-Subject</span></span>
<span data-ttu-id="5d9df-123">Temat komunikacji.</span><span class="sxs-lookup"><span data-stu-id="5d9df-123">Subject of the communication.</span></span>

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

### <span data-ttu-id="5d9df-124">-SupportTicketName</span><span class="sxs-lookup"><span data-stu-id="5d9df-124">-SupportTicketName</span></span>
<span data-ttu-id="5d9df-125">Nazwa biletu pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="5d9df-125">Support ticket name.</span></span>

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

### <span data-ttu-id="5d9df-126">-SupportTicketObject</span><span class="sxs-lookup"><span data-stu-id="5d9df-126">-SupportTicketObject</span></span>
<span data-ttu-id="5d9df-127">Obiekt biletu pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="5d9df-127">Support ticket object.</span></span>

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

### <span data-ttu-id="5d9df-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5d9df-128">-Confirm</span></span>
<span data-ttu-id="5d9df-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d9df-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d9df-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d9df-130">-WhatIf</span></span>
<span data-ttu-id="5d9df-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d9df-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d9df-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5d9df-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d9df-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d9df-133">CommonParameters</span></span>
<span data-ttu-id="5d9df-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d9df-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d9df-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5d9df-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d9df-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5d9df-136">INPUTS</span></span>

### <span data-ttu-id="5d9df-137">Microsoft. Azure. Commands. support. models. PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="5d9df-137">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="5d9df-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5d9df-138">OUTPUTS</span></span>

### <span data-ttu-id="5d9df-139">Microsoft. Azure. Commands. support. models. PSSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="5d9df-139">Microsoft.Azure.Commands.Support.Models.PSSupportTicketCommunication</span></span>

## <span data-ttu-id="5d9df-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5d9df-140">NOTES</span></span>

## <span data-ttu-id="5d9df-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5d9df-141">RELATED LINKS</span></span>
