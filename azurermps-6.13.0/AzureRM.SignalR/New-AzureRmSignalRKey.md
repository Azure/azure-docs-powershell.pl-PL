---
external help file: Microsoft.Azure.Commands.SignalR.dll-Help.xml
Module Name: AzureRM.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.signalr/new-azurermsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/New-AzureRmSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/New-AzureRmSignalRKey.md
ms.openlocfilehash: 4b4f3a416ece999641570a33101a3e7ab201ca3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546435"
---
# <span data-ttu-id="294ad-101">New-AzureRmSignalRKey</span><span class="sxs-lookup"><span data-stu-id="294ad-101">New-AzureRmSignalRKey</span></span>

## <span data-ttu-id="294ad-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="294ad-102">SYNOPSIS</span></span>
<span data-ttu-id="294ad-103">Ponowne generowanie klucza dostępu do usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="294ad-103">Regenerate an access key for a SignalR service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="294ad-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="294ad-104">SYNTAX</span></span>

### <span data-ttu-id="294ad-105">ResourceGroupParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="294ad-105">ResourceGroupParameterSet (Default)</span></span>
```
New-AzureRmSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="294ad-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="294ad-106">ResourceIdParameterSet</span></span>
```
New-AzureRmSignalRKey -ResourceId <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="294ad-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="294ad-107">InputObjectParameterSet</span></span>
```
New-AzureRmSignalRKey -InputObject <PSSignalRResource> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="294ad-108">Opis</span><span class="sxs-lookup"><span data-stu-id="294ad-108">DESCRIPTION</span></span>
<span data-ttu-id="294ad-109">Ponowne generowanie klucza dostępu do usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="294ad-109">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="294ad-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="294ad-110">EXAMPLES</span></span>

### <span data-ttu-id="294ad-111">Ponowne generowanie klucza podstawowego</span><span class="sxs-lookup"><span data-stu-id="294ad-111">Regenerate the primary key</span></span>
```powershell
PS C:\> New-AzureRmSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1 -KeyType Primary -PassThru

True
```

## <span data-ttu-id="294ad-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="294ad-112">PARAMETERS</span></span>

### <span data-ttu-id="294ad-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="294ad-113">-DefaultProfile</span></span>
<span data-ttu-id="294ad-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="294ad-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="294ad-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="294ad-115">-InputObject</span></span>
<span data-ttu-id="294ad-116">Obiekt zasobu sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="294ad-116">The SignalR resource object.</span></span>

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

### <span data-ttu-id="294ad-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="294ad-117">-KeyType</span></span>
<span data-ttu-id="294ad-118">Typ klucza: podstawowy lub pomocniczy.</span><span class="sxs-lookup"><span data-stu-id="294ad-118">The key type, either Primary or Secondary.</span></span>

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

### <span data-ttu-id="294ad-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="294ad-119">-Name</span></span>
<span data-ttu-id="294ad-120">Nazwa usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="294ad-120">SignalR service name.</span></span>

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

### <span data-ttu-id="294ad-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="294ad-121">-PassThru</span></span>
<span data-ttu-id="294ad-122">Zwraca wartość PRAWDA, jeśli ponowne generowanie zostało zakończone pomyślnie.</span><span class="sxs-lookup"><span data-stu-id="294ad-122">Returns true if the regeneration was completed successfully.</span></span>

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

### <span data-ttu-id="294ad-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="294ad-123">-ResourceGroupName</span></span>
<span data-ttu-id="294ad-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="294ad-124">Resource group name.</span></span>

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

### <span data-ttu-id="294ad-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="294ad-125">-ResourceId</span></span>
<span data-ttu-id="294ad-126">Identyfikator zasobu usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="294ad-126">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="294ad-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="294ad-127">-Confirm</span></span>
<span data-ttu-id="294ad-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="294ad-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="294ad-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="294ad-129">-WhatIf</span></span>
<span data-ttu-id="294ad-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="294ad-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="294ad-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="294ad-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="294ad-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="294ad-132">CommonParameters</span></span>
<span data-ttu-id="294ad-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="294ad-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="294ad-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="294ad-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="294ad-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="294ad-135">INPUTS</span></span>

### <span data-ttu-id="294ad-136">System. String</span><span class="sxs-lookup"><span data-stu-id="294ad-136">System.String</span></span>
<span data-ttu-id="294ad-137">Parametry: ResourceId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="294ad-137">Parameters: ResourceId (ByValue)</span></span>

### <span data-ttu-id="294ad-138">Microsoft. Azure. Commands. Signals. modele. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="294ad-138">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
<span data-ttu-id="294ad-139">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="294ad-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="294ad-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="294ad-140">OUTPUTS</span></span>

### <span data-ttu-id="294ad-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="294ad-141">System.Boolean</span></span>

## <span data-ttu-id="294ad-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="294ad-142">NOTES</span></span>

## <span data-ttu-id="294ad-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="294ad-143">RELATED LINKS</span></span>
