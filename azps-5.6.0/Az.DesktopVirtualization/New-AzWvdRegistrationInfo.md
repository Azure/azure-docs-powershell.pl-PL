---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/new-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdRegistrationInfo.md
ms.openlocfilehash: 7e633d2ba607132de6dbdfc262642659cc5e4c35
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966106"
---
# <span data-ttu-id="c5b26-101">New-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="c5b26-101">New-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="c5b26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5b26-102">SYNOPSIS</span></span>
<span data-ttu-id="c5b26-103">Utwórz informacje dotyczące rejestracji pulpitu wirtualnego systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="c5b26-103">Create Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="c5b26-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c5b26-104">SYNTAX</span></span>

```
New-AzWvdRegistrationInfo -ExpirationTime <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c5b26-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="c5b26-105">DESCRIPTION</span></span>
<span data-ttu-id="c5b26-106">Utwórz informacje dotyczące rejestracji pulpitu wirtualnego systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="c5b26-106">Create Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="c5b26-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c5b26-107">EXAMPLES</span></span>

### <span data-ttu-id="c5b26-108">Przykład 1. Tworzenie tokenu rejestracji pulpitu wirtualnego systemu Windows</span><span class="sxs-lookup"><span data-stu-id="c5b26-108">Example 1: Create a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> New-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -ExpirationTime $((get-date).ToUniversalTime().AddDays(1).ToString('yyyy-MM-ddTHH:mm:ss.fffffffZ'))

ExpirationTime       RegistrationTokenOperation Token
--------------       -------------------------- -----
4/1/2020 10:19:33 PM Update                       eyJhbGciOiJSUzI1NiIsImtpZCI6IkMyRjU1RUYxNzg0MEFCNzkzMDk2RUYzRjdEMkNBRDk0NThGNDhEOTQiLCJ0eXAiOiJKV1QifQ.eyJSZWdpc3RyYXRpb25JZCI6IjU5NGJjZWUwLTk5MjQtNDg3ZC1iOW...
```

<span data-ttu-id="c5b26-109">To polecenie tworzy token rejestracji pulpitu wirtualnego systemu Windows w puli hostów.</span><span class="sxs-lookup"><span data-stu-id="c5b26-109">This command creates a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="c5b26-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5b26-110">PARAMETERS</span></span>

### <span data-ttu-id="c5b26-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5b26-111">-DefaultProfile</span></span>
<span data-ttu-id="c5b26-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c5b26-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5b26-113">-ExpirationTime</span><span class="sxs-lookup"><span data-stu-id="c5b26-113">-ExpirationTime</span></span>
<span data-ttu-id="c5b26-114">Czas wygaśnięcia</span><span class="sxs-lookup"><span data-stu-id="c5b26-114">Expiration Time</span></span>

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

### <span data-ttu-id="c5b26-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="c5b26-115">-HostPoolName</span></span>
<span data-ttu-id="c5b26-116">Nazwa puli hosta</span><span class="sxs-lookup"><span data-stu-id="c5b26-116">Host Pool Name</span></span>

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

### <span data-ttu-id="c5b26-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5b26-117">-ResourceGroupName</span></span>
<span data-ttu-id="c5b26-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="c5b26-118">Resource Group Name</span></span>

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

### <span data-ttu-id="c5b26-119">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c5b26-119">-SubscriptionId</span></span>
<span data-ttu-id="c5b26-120">Identyfikator subskrypcji</span><span class="sxs-lookup"><span data-stu-id="c5b26-120">Subscription Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5b26-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c5b26-121">-Confirm</span></span>
<span data-ttu-id="c5b26-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c5b26-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5b26-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5b26-123">-WhatIf</span></span>
<span data-ttu-id="c5b26-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5b26-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5b26-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c5b26-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5b26-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5b26-126">CommonParameters</span></span>
<span data-ttu-id="c5b26-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5b26-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5b26-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c5b26-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5b26-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c5b26-129">INPUTS</span></span>

## <span data-ttu-id="c5b26-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c5b26-130">OUTPUTS</span></span>

### <span data-ttu-id="c5b26-131">Microsoft.Azure.PowerShell.cmdlet.DesktopVirtualization.Models.Api20201102Preview.IRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="c5b26-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IRegistrationInfo</span></span>

## <span data-ttu-id="c5b26-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c5b26-132">NOTES</span></span>

<span data-ttu-id="c5b26-133">ALIASY</span><span class="sxs-lookup"><span data-stu-id="c5b26-133">ALIASES</span></span>

## <span data-ttu-id="c5b26-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c5b26-134">RELATED LINKS</span></span>

