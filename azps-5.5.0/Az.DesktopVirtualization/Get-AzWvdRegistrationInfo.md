---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdRegistrationInfo.md
ms.openlocfilehash: 52b2d636e9ab4dbde9cbafc69da3122828a91477
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200506"
---
# <span data-ttu-id="aa891-101">Get-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="aa891-101">Get-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="aa891-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa891-102">SYNOPSIS</span></span>
<span data-ttu-id="aa891-103">Uzyskaj informacje dotyczące rejestracji pulpitu wirtualnego systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="aa891-103">Get the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="aa891-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="aa891-104">SYNTAX</span></span>

```
Get-AzWvdRegistrationInfo -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="aa891-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="aa891-105">DESCRIPTION</span></span>
<span data-ttu-id="aa891-106">Uzyskaj informacje dotyczące rejestracji pulpitu wirtualnego systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="aa891-106">Get the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="aa891-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="aa891-107">EXAMPLES</span></span>

### <span data-ttu-id="aa891-108">Przykład 1. Uzyskiwanie tokenu rejestracji pulpitu wirtualnego systemu Windows</span><span class="sxs-lookup"><span data-stu-id="aa891-108">Example 1: Get a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> Get-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

ExpirationTime       RegistrationTokenOperation Token
--------------       -------------------------- -----
4/1/2020 10:19:33 PM None                       eyJhbGciOiJSUzI1NiIsImtpZCI6IkMyRjU1RUYxNzg0MEFCNzkzMDk2RUYzRjdEMkNBRDk0NThGNDhEOTQiLCJ0eXAiOiJKV1QifQ.eyJSZWdpc3RyYXRpb25JZCI6IjU5NGJjZWUwLTk5MjQtNDg3ZC1iOW...
```

<span data-ttu-id="aa891-109">To polecenie otrzymuje token rejestracji pulpitu wirtualnego systemu Windows w puli hostów.</span><span class="sxs-lookup"><span data-stu-id="aa891-109">This command gets a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="aa891-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aa891-110">PARAMETERS</span></span>

### <span data-ttu-id="aa891-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa891-111">-DefaultProfile</span></span>
<span data-ttu-id="aa891-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="aa891-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa891-113">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="aa891-113">-HostPoolName</span></span>
<span data-ttu-id="aa891-114">Nazwa puli hosta</span><span class="sxs-lookup"><span data-stu-id="aa891-114">Host Pool Name</span></span>

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

### <span data-ttu-id="aa891-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa891-115">-ResourceGroupName</span></span>
<span data-ttu-id="aa891-116">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="aa891-116">Resource Group Name</span></span>

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

### <span data-ttu-id="aa891-117">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aa891-117">-SubscriptionId</span></span>
<span data-ttu-id="aa891-118">Identyfikator subskrypcji</span><span class="sxs-lookup"><span data-stu-id="aa891-118">Subscription Id</span></span>

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

### <span data-ttu-id="aa891-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa891-119">CommonParameters</span></span>
<span data-ttu-id="aa891-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa891-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa891-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aa891-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa891-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aa891-122">INPUTS</span></span>

## <span data-ttu-id="aa891-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="aa891-123">OUTPUTS</span></span>

### <span data-ttu-id="aa891-124">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.Api20201102Preview.RegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="aa891-124">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.RegistrationInfo</span></span>

## <span data-ttu-id="aa891-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="aa891-125">NOTES</span></span>

<span data-ttu-id="aa891-126">ALIASY</span><span class="sxs-lookup"><span data-stu-id="aa891-126">ALIASES</span></span>

## <span data-ttu-id="aa891-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aa891-127">RELATED LINKS</span></span>

