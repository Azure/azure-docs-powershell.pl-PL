---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdRegistrationInfo.md
ms.openlocfilehash: 3e4553fa3d11c8084f103f6e5c6b3f0c57cdb50c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186066"
---
# <span data-ttu-id="39ad3-101">New-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="39ad3-101">New-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="39ad3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39ad3-102">SYNOPSIS</span></span>
<span data-ttu-id="39ad3-103">Utwórz informacje dotyczące rejestracji pulpitu wirtualnego systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="39ad3-103">Create Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="39ad3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="39ad3-104">SYNTAX</span></span>

```
New-AzWvdRegistrationInfo -ExpirationTime <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="39ad3-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="39ad3-105">DESCRIPTION</span></span>
<span data-ttu-id="39ad3-106">Utwórz informacje dotyczące rejestracji pulpitu wirtualnego systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="39ad3-106">Create Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="39ad3-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="39ad3-107">EXAMPLES</span></span>

### <span data-ttu-id="39ad3-108">Przykład 1. Tworzenie tokenu rejestracji pulpitu wirtualnego systemu Windows</span><span class="sxs-lookup"><span data-stu-id="39ad3-108">Example 1: Create a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> New-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -ExpirationTime $((get-date).ToUniversalTime().AddDays(1).ToString('yyyy-MM-ddTHH:mm:ss.fffffffZ'))

ExpirationTime       RegistrationTokenOperation Token
--------------       -------------------------- -----
4/1/2020 10:19:33 PM Update                       eyJhbGciOiJSUzI1NiIsImtpZCI6IkMyRjU1RUYxNzg0MEFCNzkzMDk2RUYzRjdEMkNBRDk0NThGNDhEOTQiLCJ0eXAiOiJKV1QifQ.eyJSZWdpc3RyYXRpb25JZCI6IjU5NGJjZWUwLTk5MjQtNDg3ZC1iOW...
```

<span data-ttu-id="39ad3-109">To polecenie tworzy token rejestracji pulpitu wirtualnego systemu Windows w puli hostów.</span><span class="sxs-lookup"><span data-stu-id="39ad3-109">This command creates a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="39ad3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39ad3-110">PARAMETERS</span></span>

### <span data-ttu-id="39ad3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39ad3-111">-DefaultProfile</span></span>
<span data-ttu-id="39ad3-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="39ad3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39ad3-113">-ExpirationTime</span><span class="sxs-lookup"><span data-stu-id="39ad3-113">-ExpirationTime</span></span>
<span data-ttu-id="39ad3-114">Czas wygaśnięcia</span><span class="sxs-lookup"><span data-stu-id="39ad3-114">Expiration Time</span></span>

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

### <span data-ttu-id="39ad3-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="39ad3-115">-HostPoolName</span></span>
<span data-ttu-id="39ad3-116">Nazwa puli hosta</span><span class="sxs-lookup"><span data-stu-id="39ad3-116">Host Pool Name</span></span>

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

### <span data-ttu-id="39ad3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39ad3-117">-ResourceGroupName</span></span>
<span data-ttu-id="39ad3-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="39ad3-118">Resource Group Name</span></span>

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

### <span data-ttu-id="39ad3-119">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="39ad3-119">-SubscriptionId</span></span>
<span data-ttu-id="39ad3-120">Identyfikator subskrypcji</span><span class="sxs-lookup"><span data-stu-id="39ad3-120">Subscription Id</span></span>

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

### <span data-ttu-id="39ad3-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="39ad3-121">-Confirm</span></span>
<span data-ttu-id="39ad3-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="39ad3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39ad3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39ad3-123">-WhatIf</span></span>
<span data-ttu-id="39ad3-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39ad3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39ad3-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="39ad3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39ad3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39ad3-126">CommonParameters</span></span>
<span data-ttu-id="39ad3-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39ad3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39ad3-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="39ad3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39ad3-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="39ad3-129">INPUTS</span></span>

## <span data-ttu-id="39ad3-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="39ad3-130">OUTPUTS</span></span>

### <span data-ttu-id="39ad3-131">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.Api20201102Preview.IRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="39ad3-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IRegistrationInfo</span></span>

## <span data-ttu-id="39ad3-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="39ad3-132">NOTES</span></span>

<span data-ttu-id="39ad3-133">ALIASY</span><span class="sxs-lookup"><span data-stu-id="39ad3-133">ALIASES</span></span>

## <span data-ttu-id="39ad3-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="39ad3-134">RELATED LINKS</span></span>

