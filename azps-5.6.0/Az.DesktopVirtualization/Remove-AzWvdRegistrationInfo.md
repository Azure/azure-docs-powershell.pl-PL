---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/remove-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdRegistrationInfo.md
ms.openlocfilehash: 548e7d19e2d5285ed4063bc9c14202980c02028d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980529"
---
# <span data-ttu-id="0c901-101">Remove-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="0c901-101">Remove-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="0c901-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c901-102">SYNOPSIS</span></span>
<span data-ttu-id="0c901-103">Usuń informacje dotyczące rejestracji pulpitu wirtualnego systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="0c901-103">Remove the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="0c901-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0c901-104">SYNTAX</span></span>

```
Remove-AzWvdRegistrationInfo -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0c901-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="0c901-105">DESCRIPTION</span></span>
<span data-ttu-id="0c901-106">Usuń informacje dotyczące rejestracji pulpitu wirtualnego systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="0c901-106">Remove the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="0c901-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0c901-107">EXAMPLES</span></span>

### <span data-ttu-id="0c901-108">Przykład 1. Usuwanie tokenu rejestracji pulpitu wirtualnego systemu Windows</span><span class="sxs-lookup"><span data-stu-id="0c901-108">Example 1: Delete a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> Remove-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName
```

<span data-ttu-id="0c901-109">To polecenie usuwa token rejestracji pulpitu wirtualnego systemu Windows w puli hostów.</span><span class="sxs-lookup"><span data-stu-id="0c901-109">This command deletes a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="0c901-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c901-110">PARAMETERS</span></span>

### <span data-ttu-id="0c901-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c901-111">-DefaultProfile</span></span>
<span data-ttu-id="0c901-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0c901-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c901-113">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="0c901-113">-HostPoolName</span></span>
<span data-ttu-id="0c901-114">Nazwa puli hosta</span><span class="sxs-lookup"><span data-stu-id="0c901-114">Host Pool Name</span></span>

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

### <span data-ttu-id="0c901-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c901-115">-ResourceGroupName</span></span>
<span data-ttu-id="0c901-116">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="0c901-116">Resource Group Name</span></span>

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

### <span data-ttu-id="0c901-117">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0c901-117">-SubscriptionId</span></span>
<span data-ttu-id="0c901-118">pomoc foo 1</span><span class="sxs-lookup"><span data-stu-id="0c901-118">help foo 1</span></span>

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

### <span data-ttu-id="0c901-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0c901-119">-Confirm</span></span>
<span data-ttu-id="0c901-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0c901-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c901-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c901-121">-WhatIf</span></span>
<span data-ttu-id="0c901-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c901-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c901-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0c901-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c901-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c901-124">CommonParameters</span></span>
<span data-ttu-id="0c901-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c901-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c901-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0c901-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c901-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0c901-127">INPUTS</span></span>

## <span data-ttu-id="0c901-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0c901-128">OUTPUTS</span></span>

## <span data-ttu-id="0c901-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0c901-129">NOTES</span></span>

<span data-ttu-id="0c901-130">ALIASY</span><span class="sxs-lookup"><span data-stu-id="0c901-130">ALIASES</span></span>

## <span data-ttu-id="0c901-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0c901-131">RELATED LINKS</span></span>

