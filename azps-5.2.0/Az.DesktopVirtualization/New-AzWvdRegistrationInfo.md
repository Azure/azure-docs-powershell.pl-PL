---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdRegistrationInfo.md
ms.openlocfilehash: 2268135ebd1e1c504aae7462730d104e842f288f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332614"
---
# <span data-ttu-id="fd310-101">New-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="fd310-101">New-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="fd310-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fd310-102">SYNOPSIS</span></span>
<span data-ttu-id="fd310-103">Tworzenie informacji rejestracyjnych na pulpicie wirtualnym systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="fd310-103">Create Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="fd310-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fd310-104">SYNTAX</span></span>

```
New-AzWvdRegistrationInfo -ExpirationTime <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fd310-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fd310-105">DESCRIPTION</span></span>
<span data-ttu-id="fd310-106">Tworzenie informacji rejestracyjnych na pulpicie wirtualnym systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="fd310-106">Create Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="fd310-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fd310-107">EXAMPLES</span></span>

### <span data-ttu-id="fd310-108">Przykład 1: Tworzenie tokenu rejestracji wirtualnego pulpitu systemu Windows</span><span class="sxs-lookup"><span data-stu-id="fd310-108">Example 1: Create a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> New-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -ExpirationTime $((get-date).ToUniversalTime().AddDays(1).ToString('yyyy-MM-ddTHH:mm:ss.fffffffZ'))

ExpirationTime       RegistrationTokenOperation Token
--------------       -------------------------- -----
4/1/2020 10:19:33 PM Update                       eyJhbGciOiJSUzI1NiIsImtpZCI6IkMyRjU1RUYxNzg0MEFCNzkzMDk2RUYzRjdEMkNBRDk0NThGNDhEOTQiLCJ0eXAiOiJKV1QifQ.eyJSZWdpc3RyYXRpb25JZCI6IjU5NGJjZWUwLTk5MjQtNDg3ZC1iOW...
```

<span data-ttu-id="fd310-109">To polecenie tworzy token rejestracji na pulpicie wirtualnym systemu Windows w puli hostów.</span><span class="sxs-lookup"><span data-stu-id="fd310-109">This command creates a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="fd310-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fd310-110">PARAMETERS</span></span>

### <span data-ttu-id="fd310-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd310-111">-DefaultProfile</span></span>
<span data-ttu-id="fd310-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fd310-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd310-113">-ExpirationTime</span><span class="sxs-lookup"><span data-stu-id="fd310-113">-ExpirationTime</span></span>
<span data-ttu-id="fd310-114">Czas wygaśnięcia</span><span class="sxs-lookup"><span data-stu-id="fd310-114">Expiration Time</span></span>

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

### <span data-ttu-id="fd310-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="fd310-115">-HostPoolName</span></span>
<span data-ttu-id="fd310-116">Nazwa puli hostów</span><span class="sxs-lookup"><span data-stu-id="fd310-116">Host Pool Name</span></span>

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

### <span data-ttu-id="fd310-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd310-117">-ResourceGroupName</span></span>
<span data-ttu-id="fd310-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="fd310-118">Resource Group Name</span></span>

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

### <span data-ttu-id="fd310-119">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="fd310-119">-SubscriptionId</span></span>
<span data-ttu-id="fd310-120">Identyfikator subskrypcji</span><span class="sxs-lookup"><span data-stu-id="fd310-120">Subscription Id</span></span>

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

### <span data-ttu-id="fd310-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fd310-121">-Confirm</span></span>
<span data-ttu-id="fd310-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd310-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd310-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd310-123">-WhatIf</span></span>
<span data-ttu-id="fd310-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd310-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd310-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fd310-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd310-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd310-126">CommonParameters</span></span>
<span data-ttu-id="fd310-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd310-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd310-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fd310-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd310-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fd310-129">INPUTS</span></span>

## <span data-ttu-id="fd310-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fd310-130">OUTPUTS</span></span>

### <span data-ttu-id="fd310-131">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. Api20201019Preview. IRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="fd310-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IRegistrationInfo</span></span>

## <span data-ttu-id="fd310-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fd310-132">NOTES</span></span>

<span data-ttu-id="fd310-133">PISUJE</span><span class="sxs-lookup"><span data-stu-id="fd310-133">ALIASES</span></span>

## <span data-ttu-id="fd310-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fd310-134">RELATED LINKS</span></span>

