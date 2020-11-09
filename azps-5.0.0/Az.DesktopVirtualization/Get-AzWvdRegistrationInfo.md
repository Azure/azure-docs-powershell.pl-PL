---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdRegistrationInfo.md
ms.openlocfilehash: 0f82c80e9f06abd5a2189bbee665de58ee6a3528
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304819"
---
# <span data-ttu-id="818e7-101">Get-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="818e7-101">Get-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="818e7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="818e7-102">SYNOPSIS</span></span>
<span data-ttu-id="818e7-103">Uzyskaj informacje o rejestracji na pulpicie wirtualnym systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="818e7-103">Get the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="818e7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="818e7-104">SYNTAX</span></span>

```
Get-AzWvdRegistrationInfo -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="818e7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="818e7-105">DESCRIPTION</span></span>
<span data-ttu-id="818e7-106">Uzyskaj informacje o rejestracji na pulpicie wirtualnym systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="818e7-106">Get the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="818e7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="818e7-107">EXAMPLES</span></span>

### <span data-ttu-id="818e7-108">Przykład 1: uzyskiwanie tokenu rejestracji wirtualnego pulpitu systemu Windows</span><span class="sxs-lookup"><span data-stu-id="818e7-108">Example 1: Get a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> Get-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

ExpirationTime       RegistrationTokenOperation Token
--------------       -------------------------- -----
4/1/2020 10:19:33 PM None                       eyJhbGciOiJSUzI1NiIsImtpZCI6IkMyRjU1RUYxNzg0MEFCNzkzMDk2RUYzRjdEMkNBRDk0NThGNDhEOTQiLCJ0eXAiOiJKV1QifQ.eyJSZWdpc3RyYXRpb25JZCI6IjU5NGJjZWUwLTk5MjQtNDg3ZC1iOW...
```

<span data-ttu-id="818e7-109">To polecenie pobiera token rejestracji pulpitu wirtualnego systemu Windows w puli hostów.</span><span class="sxs-lookup"><span data-stu-id="818e7-109">This command gets a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="818e7-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="818e7-110">PARAMETERS</span></span>

### <span data-ttu-id="818e7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="818e7-111">-DefaultProfile</span></span>
<span data-ttu-id="818e7-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="818e7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="818e7-113">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="818e7-113">-HostPoolName</span></span>
<span data-ttu-id="818e7-114">Nazwa puli hostów</span><span class="sxs-lookup"><span data-stu-id="818e7-114">Host Pool Name</span></span>

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

### <span data-ttu-id="818e7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="818e7-115">-ResourceGroupName</span></span>
<span data-ttu-id="818e7-116">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="818e7-116">Resource Group Name</span></span>

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

### <span data-ttu-id="818e7-117">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="818e7-117">-SubscriptionId</span></span>
<span data-ttu-id="818e7-118">Identyfikator subskrypcji</span><span class="sxs-lookup"><span data-stu-id="818e7-118">Subscription Id</span></span>

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

### <span data-ttu-id="818e7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="818e7-119">CommonParameters</span></span>
<span data-ttu-id="818e7-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="818e7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="818e7-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="818e7-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="818e7-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="818e7-122">INPUTS</span></span>

## <span data-ttu-id="818e7-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="818e7-123">OUTPUTS</span></span>

### <span data-ttu-id="818e7-124">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. Api20191210Preview. RegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="818e7-124">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.RegistrationInfo</span></span>

## <span data-ttu-id="818e7-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="818e7-125">NOTES</span></span>

<span data-ttu-id="818e7-126">PISUJE</span><span class="sxs-lookup"><span data-stu-id="818e7-126">ALIASES</span></span>

## <span data-ttu-id="818e7-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="818e7-127">RELATED LINKS</span></span>

