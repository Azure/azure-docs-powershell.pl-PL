---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Set-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityContact.md
ms.openlocfilehash: 8cd5adee5e8b992cf709b76996a70760f3fd90a5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986511"
---
# <span data-ttu-id="315fe-101">Set-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="315fe-101">Set-AzSecurityContact</span></span>

## <span data-ttu-id="315fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="315fe-102">SYNOPSIS</span></span>
<span data-ttu-id="315fe-103">Aktualizuje kontakt zabezpieczeń dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="315fe-103">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="315fe-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="315fe-104">SYNTAX</span></span>

```
Set-AzSecurityContact -Name <String> -Email <String> [-Phone <String>] [-AlertAdmin] [-NotifyOnAlert]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="315fe-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="315fe-105">DESCRIPTION</span></span>
<span data-ttu-id="315fe-106">Aktualizuje kontakt zabezpieczeń dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="315fe-106">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="315fe-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="315fe-107">EXAMPLES</span></span>

### <span data-ttu-id="315fe-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="315fe-108">Example 1</span></span>
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

<span data-ttu-id="315fe-109">Aktualizuje kontakt zabezpieczeń dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="315fe-109">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="315fe-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="315fe-110">PARAMETERS</span></span>

### <span data-ttu-id="315fe-111">-AlertAdmin</span><span class="sxs-lookup"><span data-stu-id="315fe-111">-AlertAdmin</span></span>
<span data-ttu-id="315fe-112">Alerty dla administratorów.</span><span class="sxs-lookup"><span data-stu-id="315fe-112">Alerts To Administrators.</span></span>

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

### <span data-ttu-id="315fe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="315fe-113">-DefaultProfile</span></span>
<span data-ttu-id="315fe-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="315fe-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="315fe-115">— Poczta e-mail</span><span class="sxs-lookup"><span data-stu-id="315fe-115">-Email</span></span>
<span data-ttu-id="315fe-116">Poczta e-mail.</span><span class="sxs-lookup"><span data-stu-id="315fe-116">E-Mail.</span></span>

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

### <span data-ttu-id="315fe-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="315fe-117">-Name</span></span>
<span data-ttu-id="315fe-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="315fe-118">Resource name.</span></span>

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

### <span data-ttu-id="315fe-119">-NotifyOnAlert</span><span class="sxs-lookup"><span data-stu-id="315fe-119">-NotifyOnAlert</span></span>
<span data-ttu-id="315fe-120">Powiadomienia alertów.</span><span class="sxs-lookup"><span data-stu-id="315fe-120">Alert Notifications.</span></span>

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

### <span data-ttu-id="315fe-121">— Telefon</span><span class="sxs-lookup"><span data-stu-id="315fe-121">-Phone</span></span>
<span data-ttu-id="315fe-122">Telefon.</span><span class="sxs-lookup"><span data-stu-id="315fe-122">Phone.</span></span>

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

### <span data-ttu-id="315fe-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="315fe-123">-Confirm</span></span>
<span data-ttu-id="315fe-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="315fe-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="315fe-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="315fe-125">-WhatIf</span></span>
<span data-ttu-id="315fe-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="315fe-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="315fe-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="315fe-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="315fe-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="315fe-128">CommonParameters</span></span>
<span data-ttu-id="315fe-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="315fe-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="315fe-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="315fe-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="315fe-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="315fe-131">INPUTS</span></span>

### <span data-ttu-id="315fe-132">Brak</span><span class="sxs-lookup"><span data-stu-id="315fe-132">None</span></span>

## <span data-ttu-id="315fe-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="315fe-133">OUTPUTS</span></span>

### <span data-ttu-id="315fe-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="315fe-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="315fe-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="315fe-135">NOTES</span></span>

## <span data-ttu-id="315fe-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="315fe-136">RELATED LINKS</span></span>
