---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/new-azsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalRKey.md
ms.openlocfilehash: 9c27342a073f33a52881376037fc8d3a5d7e8bb1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499902"
---
# <span data-ttu-id="cea08-101">New-AzSignalRKey</span><span class="sxs-lookup"><span data-stu-id="cea08-101">New-AzSignalRKey</span></span>

## <span data-ttu-id="cea08-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cea08-102">SYNOPSIS</span></span>
<span data-ttu-id="cea08-103">Ponowne generowanie klucza dostępu do usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="cea08-103">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="cea08-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cea08-104">SYNTAX</span></span>

### <span data-ttu-id="cea08-105">ResourceGroupParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cea08-105">ResourceGroupParameterSet (Default)</span></span>
```
New-AzSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cea08-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cea08-106">ResourceIdParameterSet</span></span>
```
New-AzSignalRKey -ResourceId <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cea08-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cea08-107">InputObjectParameterSet</span></span>
```
New-AzSignalRKey -InputObject <PSSignalRResource> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cea08-108">Opis</span><span class="sxs-lookup"><span data-stu-id="cea08-108">DESCRIPTION</span></span>
<span data-ttu-id="cea08-109">Ponowne generowanie klucza dostępu do usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="cea08-109">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="cea08-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cea08-110">EXAMPLES</span></span>

### <span data-ttu-id="cea08-111">Ponowne generowanie klucza podstawowego</span><span class="sxs-lookup"><span data-stu-id="cea08-111">Regenerate the primary key</span></span>
```powershell
PS C:\> New-AzSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1 -KeyType Primary -PassThru

True
```

## <span data-ttu-id="cea08-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cea08-112">PARAMETERS</span></span>

### <span data-ttu-id="cea08-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cea08-113">-DefaultProfile</span></span>
<span data-ttu-id="cea08-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cea08-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cea08-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="cea08-115">-InputObject</span></span>
<span data-ttu-id="cea08-116">Obiekt zasobu sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="cea08-116">The SignalR resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cea08-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="cea08-117">-KeyType</span></span>
<span data-ttu-id="cea08-118">Typ klucza: podstawowy lub pomocniczy.</span><span class="sxs-lookup"><span data-stu-id="cea08-118">The key type, either Primary or Secondary.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cea08-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cea08-119">-Name</span></span>
<span data-ttu-id="cea08-120">Nazwa usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="cea08-120">SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cea08-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cea08-121">-PassThru</span></span>
<span data-ttu-id="cea08-122">Zwraca wartość PRAWDA, jeśli ponowne generowanie zostało zakończone pomyślnie.</span><span class="sxs-lookup"><span data-stu-id="cea08-122">Returns true if the regeneration was completed successfully.</span></span>

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

### <span data-ttu-id="cea08-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cea08-123">-ResourceGroupName</span></span>
<span data-ttu-id="cea08-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cea08-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cea08-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cea08-125">-ResourceId</span></span>
<span data-ttu-id="cea08-126">Identyfikator zasobu usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="cea08-126">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cea08-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cea08-127">-Confirm</span></span>
<span data-ttu-id="cea08-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cea08-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cea08-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cea08-129">-WhatIf</span></span>
<span data-ttu-id="cea08-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cea08-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cea08-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cea08-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cea08-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cea08-132">CommonParameters</span></span>
<span data-ttu-id="cea08-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cea08-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cea08-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cea08-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cea08-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cea08-135">INPUTS</span></span>

### <span data-ttu-id="cea08-136">System. String</span><span class="sxs-lookup"><span data-stu-id="cea08-136">System.String</span></span>
### <span data-ttu-id="cea08-137">Microsoft. Azure. Commands. Signals. modele. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="cea08-137">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="cea08-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cea08-138">OUTPUTS</span></span>

### <span data-ttu-id="cea08-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cea08-139">System.Boolean</span></span>
## <span data-ttu-id="cea08-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cea08-140">NOTES</span></span>

## <span data-ttu-id="cea08-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cea08-141">RELATED LINKS</span></span>
