---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityContact.md
ms.openlocfilehash: c6351fb39158f7389c0f491a813890373df82cc1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052738"
---
# <span data-ttu-id="cbd2c-101">Set-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="cbd2c-101">Set-AzSecurityContact</span></span>

## <span data-ttu-id="cbd2c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cbd2c-102">SYNOPSIS</span></span>
<span data-ttu-id="cbd2c-103">Umożliwia zaktualizowanie kontaktu z zabezpieczeniami dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="cbd2c-103">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="cbd2c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cbd2c-104">SYNTAX</span></span>

```
Set-AzSecurityContact -Name <String> -Email <String> [-Phone <String>] [-AlertAdmin] [-NotifyOnAlert]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cbd2c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cbd2c-105">DESCRIPTION</span></span>
<span data-ttu-id="cbd2c-106">Umożliwia zaktualizowanie kontaktu z zabezpieczeniami dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="cbd2c-106">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="cbd2c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cbd2c-107">EXAMPLES</span></span>

### <span data-ttu-id="cbd2c-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cbd2c-108">Example 1</span></span>
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

<span data-ttu-id="cbd2c-109">Umożliwia zaktualizowanie kontaktu z zabezpieczeniami dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="cbd2c-109">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="cbd2c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cbd2c-110">PARAMETERS</span></span>

### <span data-ttu-id="cbd2c-111">-AlertAdmin</span><span class="sxs-lookup"><span data-stu-id="cbd2c-111">-AlertAdmin</span></span>
<span data-ttu-id="cbd2c-112">Alerty dla administratorów.</span><span class="sxs-lookup"><span data-stu-id="cbd2c-112">Alerts To Administrators.</span></span>

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

### <span data-ttu-id="cbd2c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbd2c-113">-DefaultProfile</span></span>
<span data-ttu-id="cbd2c-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cbd2c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbd2c-115">-Mail</span><span class="sxs-lookup"><span data-stu-id="cbd2c-115">-Email</span></span>
<span data-ttu-id="cbd2c-116">Wysłać.</span><span class="sxs-lookup"><span data-stu-id="cbd2c-116">E-Mail.</span></span>

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

### <span data-ttu-id="cbd2c-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cbd2c-117">-Name</span></span>
<span data-ttu-id="cbd2c-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="cbd2c-118">Resource name.</span></span>

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

### <span data-ttu-id="cbd2c-119">-NotifyOnAlert</span><span class="sxs-lookup"><span data-stu-id="cbd2c-119">-NotifyOnAlert</span></span>
<span data-ttu-id="cbd2c-120">Powiadomienia o alertach.</span><span class="sxs-lookup"><span data-stu-id="cbd2c-120">Alert Notifications.</span></span>

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

### <span data-ttu-id="cbd2c-121">-Phone</span><span class="sxs-lookup"><span data-stu-id="cbd2c-121">-Phone</span></span>
<span data-ttu-id="cbd2c-122">Służb.</span><span class="sxs-lookup"><span data-stu-id="cbd2c-122">Phone.</span></span>

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

### <span data-ttu-id="cbd2c-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cbd2c-123">-Confirm</span></span>
<span data-ttu-id="cbd2c-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cbd2c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbd2c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbd2c-125">-WhatIf</span></span>
<span data-ttu-id="cbd2c-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cbd2c-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cbd2c-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cbd2c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbd2c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbd2c-128">CommonParameters</span></span>
<span data-ttu-id="cbd2c-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbd2c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbd2c-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbd2c-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbd2c-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cbd2c-131">INPUTS</span></span>

### <span data-ttu-id="cbd2c-132">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="cbd2c-132">None</span></span>

## <span data-ttu-id="cbd2c-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cbd2c-133">OUTPUTS</span></span>

### <span data-ttu-id="cbd2c-134">Microsoft. Azure. Commands. Security. models. SecurityContacts. PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="cbd2c-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="cbd2c-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cbd2c-135">NOTES</span></span>

## <span data-ttu-id="cbd2c-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cbd2c-136">RELATED LINKS</span></span>
