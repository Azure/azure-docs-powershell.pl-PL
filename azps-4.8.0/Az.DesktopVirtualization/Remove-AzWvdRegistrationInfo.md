---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdRegistrationInfo.md
ms.openlocfilehash: bdef7b776d8da82a357d535ff91298a2f49e9e4c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221226"
---
# <span data-ttu-id="00def-101">Remove-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="00def-101">Remove-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="00def-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="00def-102">SYNOPSIS</span></span>
<span data-ttu-id="00def-103">Usuń informacje rejestracyjne na pulpicie wirtualnym systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="00def-103">Remove the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="00def-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="00def-104">SYNTAX</span></span>

```
Remove-AzWvdRegistrationInfo -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="00def-105">Opis</span><span class="sxs-lookup"><span data-stu-id="00def-105">DESCRIPTION</span></span>
<span data-ttu-id="00def-106">Usuń informacje rejestracyjne na pulpicie wirtualnym systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="00def-106">Remove the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="00def-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="00def-107">EXAMPLES</span></span>

### <span data-ttu-id="00def-108">Przykład 1: usuwanie tokenu rejestracji wirtualnego pulpitu systemu Windows</span><span class="sxs-lookup"><span data-stu-id="00def-108">Example 1: Delete a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> Remove-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName
```

<span data-ttu-id="00def-109">To polecenie usuwa token rejestracji wirtualnego pulpitu systemu Windows w puli hostów.</span><span class="sxs-lookup"><span data-stu-id="00def-109">This command deletes a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="00def-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="00def-110">PARAMETERS</span></span>

### <span data-ttu-id="00def-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00def-111">-DefaultProfile</span></span>
<span data-ttu-id="00def-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="00def-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00def-113">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="00def-113">-HostPoolName</span></span>
<span data-ttu-id="00def-114">Nazwa puli hostów</span><span class="sxs-lookup"><span data-stu-id="00def-114">Host Pool Name</span></span>

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

### <span data-ttu-id="00def-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00def-115">-ResourceGroupName</span></span>
<span data-ttu-id="00def-116">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="00def-116">Resource Group Name</span></span>

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

### <span data-ttu-id="00def-117">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="00def-117">-SubscriptionId</span></span>
<span data-ttu-id="00def-118">Pomóż foo 1</span><span class="sxs-lookup"><span data-stu-id="00def-118">help foo 1</span></span>

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

### <span data-ttu-id="00def-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="00def-119">-Confirm</span></span>
<span data-ttu-id="00def-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00def-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00def-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00def-121">-WhatIf</span></span>
<span data-ttu-id="00def-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00def-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00def-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="00def-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00def-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00def-124">CommonParameters</span></span>
<span data-ttu-id="00def-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00def-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00def-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="00def-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00def-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="00def-127">INPUTS</span></span>

## <span data-ttu-id="00def-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="00def-128">OUTPUTS</span></span>

## <span data-ttu-id="00def-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="00def-129">NOTES</span></span>

<span data-ttu-id="00def-130">PISUJE</span><span class="sxs-lookup"><span data-stu-id="00def-130">ALIASES</span></span>

## <span data-ttu-id="00def-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="00def-131">RELATED LINKS</span></span>

