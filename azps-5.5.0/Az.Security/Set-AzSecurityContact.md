---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityContact.md
ms.openlocfilehash: 504f07092a0a8e246e778421748f1cd807b04a77
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242275"
---
# <span data-ttu-id="7bf2e-101">Set-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="7bf2e-101">Set-AzSecurityContact</span></span>

## <span data-ttu-id="7bf2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7bf2e-102">SYNOPSIS</span></span>
<span data-ttu-id="7bf2e-103">Aktualizuje kontakt zabezpieczeń dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-103">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="7bf2e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7bf2e-104">SYNTAX</span></span>

```
Set-AzSecurityContact -Name <String> -Email <String> [-Phone <String>] [-AlertAdmin] [-NotifyOnAlert]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bf2e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="7bf2e-105">DESCRIPTION</span></span>
<span data-ttu-id="7bf2e-106">Aktualizuje kontakt zabezpieczeń dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-106">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="7bf2e-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7bf2e-107">EXAMPLES</span></span>

### <span data-ttu-id="7bf2e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7bf2e-108">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityContact -Name "default1" -Email "john@contoso.com" -Phone "214275-4038" -AlertAdmin -NotifyOnAlert

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/securityContacts/
                     default1
Name               : default1
Email              : john@contoso.com
Phone              : 214275-4038
AlertNotifications : On
AlertsToAdmins     : On
```

<span data-ttu-id="7bf2e-109">Aktualizuje kontakt zabezpieczeń dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-109">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="7bf2e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7bf2e-110">PARAMETERS</span></span>

### <span data-ttu-id="7bf2e-111">-AlertAdmin</span><span class="sxs-lookup"><span data-stu-id="7bf2e-111">-AlertAdmin</span></span>
<span data-ttu-id="7bf2e-112">Alerty dla administratorów.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-112">Alerts To Administrators.</span></span>

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

### <span data-ttu-id="7bf2e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bf2e-113">-DefaultProfile</span></span>
<span data-ttu-id="7bf2e-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7bf2e-115">— Poczta e-mail</span><span class="sxs-lookup"><span data-stu-id="7bf2e-115">-Email</span></span>
<span data-ttu-id="7bf2e-116">Poczta e-mail.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-116">E-Mail.</span></span>

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

### <span data-ttu-id="7bf2e-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7bf2e-117">-Name</span></span>
<span data-ttu-id="7bf2e-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-118">Resource name.</span></span>

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

### <span data-ttu-id="7bf2e-119">-NotifyOnAlert</span><span class="sxs-lookup"><span data-stu-id="7bf2e-119">-NotifyOnAlert</span></span>
<span data-ttu-id="7bf2e-120">Powiadomienia alertów.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-120">Alert Notifications.</span></span>

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

### <span data-ttu-id="7bf2e-121">— Telefon</span><span class="sxs-lookup"><span data-stu-id="7bf2e-121">-Phone</span></span>
<span data-ttu-id="7bf2e-122">Telefon.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-122">Phone.</span></span>

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

### <span data-ttu-id="7bf2e-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7bf2e-123">-Confirm</span></span>
<span data-ttu-id="7bf2e-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bf2e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bf2e-125">-WhatIf</span></span>
<span data-ttu-id="7bf2e-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7bf2e-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bf2e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bf2e-128">CommonParameters</span></span>
<span data-ttu-id="7bf2e-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bf2e-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7bf2e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bf2e-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7bf2e-131">INPUTS</span></span>

### <span data-ttu-id="7bf2e-132">Brak</span><span class="sxs-lookup"><span data-stu-id="7bf2e-132">None</span></span>

## <span data-ttu-id="7bf2e-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7bf2e-133">OUTPUTS</span></span>

### <span data-ttu-id="7bf2e-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="7bf2e-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="7bf2e-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7bf2e-135">NOTES</span></span>

## <span data-ttu-id="7bf2e-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7bf2e-136">RELATED LINKS</span></span>
