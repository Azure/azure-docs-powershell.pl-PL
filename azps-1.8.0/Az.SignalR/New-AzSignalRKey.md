---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/new-azsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalRKey.md
ms.openlocfilehash: 3feb052875cdf9afa7a32d4e7fc8066517b16dd8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708056"
---
# <span data-ttu-id="107f8-101">New-AzSignalRKey</span><span class="sxs-lookup"><span data-stu-id="107f8-101">New-AzSignalRKey</span></span>

## <span data-ttu-id="107f8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="107f8-102">SYNOPSIS</span></span>
<span data-ttu-id="107f8-103">Ponowne generowanie klucza dostępu do usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="107f8-103">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="107f8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="107f8-104">SYNTAX</span></span>

### <span data-ttu-id="107f8-105">ResourceGroupParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="107f8-105">ResourceGroupParameterSet (Default)</span></span>
```
New-AzSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="107f8-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="107f8-106">ResourceIdParameterSet</span></span>
```
New-AzSignalRKey -ResourceId <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="107f8-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="107f8-107">InputObjectParameterSet</span></span>
```
New-AzSignalRKey -InputObject <PSSignalRResource> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="107f8-108">Opis</span><span class="sxs-lookup"><span data-stu-id="107f8-108">DESCRIPTION</span></span>
<span data-ttu-id="107f8-109">Ponowne generowanie klucza dostępu do usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="107f8-109">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="107f8-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="107f8-110">EXAMPLES</span></span>

### <span data-ttu-id="107f8-111">Ponowne generowanie klucza podstawowego</span><span class="sxs-lookup"><span data-stu-id="107f8-111">Regenerate the primary key</span></span>
```powershell
PS C:\> New-AzSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1 -KeyType Primary -PassThru

True
```

## <span data-ttu-id="107f8-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="107f8-112">PARAMETERS</span></span>

### <span data-ttu-id="107f8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="107f8-113">-DefaultProfile</span></span>
<span data-ttu-id="107f8-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="107f8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="107f8-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="107f8-115">-InputObject</span></span>
<span data-ttu-id="107f8-116">Obiekt zasobu sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="107f8-116">The SignalR resource object.</span></span>

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

### <span data-ttu-id="107f8-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="107f8-117">-KeyType</span></span>
<span data-ttu-id="107f8-118">Typ klucza: podstawowy lub pomocniczy.</span><span class="sxs-lookup"><span data-stu-id="107f8-118">The key type, either Primary or Secondary.</span></span>

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

### <span data-ttu-id="107f8-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="107f8-119">-Name</span></span>
<span data-ttu-id="107f8-120">Nazwa usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="107f8-120">SignalR service name.</span></span>

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

### <span data-ttu-id="107f8-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="107f8-121">-PassThru</span></span>
<span data-ttu-id="107f8-122">Zwraca wartość PRAWDA, jeśli ponowne generowanie zostało zakończone pomyślnie.</span><span class="sxs-lookup"><span data-stu-id="107f8-122">Returns true if the regeneration was completed successfully.</span></span>

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

### <span data-ttu-id="107f8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="107f8-123">-ResourceGroupName</span></span>
<span data-ttu-id="107f8-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="107f8-124">Resource group name.</span></span>

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

### <span data-ttu-id="107f8-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="107f8-125">-ResourceId</span></span>
<span data-ttu-id="107f8-126">Identyfikator zasobu usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="107f8-126">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="107f8-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="107f8-127">-Confirm</span></span>
<span data-ttu-id="107f8-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="107f8-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="107f8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="107f8-129">-WhatIf</span></span>
<span data-ttu-id="107f8-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="107f8-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="107f8-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="107f8-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="107f8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="107f8-132">CommonParameters</span></span>
<span data-ttu-id="107f8-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="107f8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="107f8-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="107f8-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="107f8-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="107f8-135">INPUTS</span></span>

### <span data-ttu-id="107f8-136">System. String</span><span class="sxs-lookup"><span data-stu-id="107f8-136">System.String</span></span>

### <span data-ttu-id="107f8-137">Microsoft. Azure. Commands. Signals. modele. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="107f8-137">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="107f8-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="107f8-138">OUTPUTS</span></span>

### <span data-ttu-id="107f8-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="107f8-139">System.Boolean</span></span>

## <span data-ttu-id="107f8-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="107f8-140">NOTES</span></span>

## <span data-ttu-id="107f8-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="107f8-141">RELATED LINKS</span></span>