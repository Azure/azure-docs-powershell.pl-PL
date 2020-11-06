---
external help file: Microsoft.Azure.Commands.SignalR.dll-Help.xml
Module Name: AzureRM.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.signalr/new-azurermsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Remove-AzureRmSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Remove-AzureRmSignalR.md
ms.openlocfilehash: 5fcf62e592ed1e842c3dc6f4be21462170c4f83b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546431"
---
# <span data-ttu-id="66fbb-101">Remove-AzureRmSignalR</span><span class="sxs-lookup"><span data-stu-id="66fbb-101">Remove-AzureRmSignalR</span></span>

## <span data-ttu-id="66fbb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="66fbb-102">SYNOPSIS</span></span>
<span data-ttu-id="66fbb-103">Usuń usługę sygnalizującą.</span><span class="sxs-lookup"><span data-stu-id="66fbb-103">Remove a SignalR service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66fbb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="66fbb-104">SYNTAX</span></span>

### <span data-ttu-id="66fbb-105">ResourceGroupParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="66fbb-105">ResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66fbb-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="66fbb-106">ResourceIdParameterSet</span></span>
```
Remove-AzureRmSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66fbb-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="66fbb-107">InputObjectParameterSet</span></span>
```
Remove-AzureRmSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66fbb-108">Opis</span><span class="sxs-lookup"><span data-stu-id="66fbb-108">DESCRIPTION</span></span>
<span data-ttu-id="66fbb-109">Usuń usługę sygnalizującą.</span><span class="sxs-lookup"><span data-stu-id="66fbb-109">Remove a SignalR service.</span></span>

## <span data-ttu-id="66fbb-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="66fbb-110">EXAMPLES</span></span>

### <span data-ttu-id="66fbb-111">Usuwanie usługi sygnalizującej</span><span class="sxs-lookup"><span data-stu-id="66fbb-111">Remove a SignalR service</span></span>
```powershell
PS C:\> Remove-AzureRmSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

### <span data-ttu-id="66fbb-112">Usuwanie wszystkich usług sygnalizacji z potoku</span><span class="sxs-lookup"><span data-stu-id="66fbb-112">Remove all SignalR service from pipe</span></span>
```powershell
PS C:\> Get-AzureRmSignalR -ResourceGroupName myResourceGroup | Remove-AzureRmSignalR
```

## <span data-ttu-id="66fbb-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="66fbb-113">PARAMETERS</span></span>

### <span data-ttu-id="66fbb-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="66fbb-114">-AsJob</span></span>
<span data-ttu-id="66fbb-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="66fbb-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="66fbb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66fbb-116">-DefaultProfile</span></span>
<span data-ttu-id="66fbb-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="66fbb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66fbb-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="66fbb-118">-InputObject</span></span>
<span data-ttu-id="66fbb-119">Obiekt zasobu sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="66fbb-119">The SignalR resource object.</span></span>

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

### <span data-ttu-id="66fbb-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="66fbb-120">-Name</span></span>
<span data-ttu-id="66fbb-121">Nazwa usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="66fbb-121">SignalR service name.</span></span>

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

### <span data-ttu-id="66fbb-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="66fbb-122">-PassThru</span></span>
<span data-ttu-id="66fbb-123">Zwraca wartość PRAWDA, Jeśli usunięcie zostało pomyślnie zrealizowane.</span><span class="sxs-lookup"><span data-stu-id="66fbb-123">Returns true if the removal was completed successfully.</span></span>

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

### <span data-ttu-id="66fbb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66fbb-124">-ResourceGroupName</span></span>
<span data-ttu-id="66fbb-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="66fbb-125">Resource group name.</span></span>

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

### <span data-ttu-id="66fbb-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="66fbb-126">-ResourceId</span></span>
<span data-ttu-id="66fbb-127">Identyfikator zasobu usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="66fbb-127">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="66fbb-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="66fbb-128">-Confirm</span></span>
<span data-ttu-id="66fbb-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66fbb-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66fbb-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66fbb-130">-WhatIf</span></span>
<span data-ttu-id="66fbb-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66fbb-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66fbb-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="66fbb-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66fbb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66fbb-133">CommonParameters</span></span>
<span data-ttu-id="66fbb-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66fbb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66fbb-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66fbb-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66fbb-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="66fbb-136">INPUTS</span></span>

### <span data-ttu-id="66fbb-137">System. String</span><span class="sxs-lookup"><span data-stu-id="66fbb-137">System.String</span></span>
<span data-ttu-id="66fbb-138">Parametry: ResourceId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="66fbb-138">Parameters: ResourceId (ByValue)</span></span>

### <span data-ttu-id="66fbb-139">Microsoft. Azure. Commands. Signals. modele. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="66fbb-139">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
<span data-ttu-id="66fbb-140">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="66fbb-140">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="66fbb-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="66fbb-141">OUTPUTS</span></span>

### <span data-ttu-id="66fbb-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="66fbb-142">System.Boolean</span></span>

## <span data-ttu-id="66fbb-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="66fbb-143">NOTES</span></span>

## <span data-ttu-id="66fbb-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="66fbb-144">RELATED LINKS</span></span>
