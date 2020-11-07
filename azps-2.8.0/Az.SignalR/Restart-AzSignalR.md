---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/restart-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Restart-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Restart-AzSignalR.md
ms.openlocfilehash: 1812a51492b834df4152d492960444c12d2bccc8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873015"
---
# <span data-ttu-id="d44f3-101">Restart-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="d44f3-101">Restart-AzSignalR</span></span>

## <span data-ttu-id="d44f3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d44f3-102">SYNOPSIS</span></span>
<span data-ttu-id="d44f3-103">Uruchom ponownie usługę sygnalizującą.</span><span class="sxs-lookup"><span data-stu-id="d44f3-103">Restart a SignalR service.</span></span>

## <span data-ttu-id="d44f3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d44f3-104">SYNTAX</span></span>

### <span data-ttu-id="d44f3-105">ResourceGroupParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d44f3-105">ResourceGroupParameterSet (Default)</span></span>
```
Restart-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d44f3-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d44f3-106">ResourceIdParameterSet</span></span>
```
Restart-AzSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d44f3-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d44f3-107">InputObjectParameterSet</span></span>
```
Restart-AzSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d44f3-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d44f3-108">DESCRIPTION</span></span>
<span data-ttu-id="d44f3-109">Uruchom ponownie usługę sygnalizującą.</span><span class="sxs-lookup"><span data-stu-id="d44f3-109">Restart a SignalR service.</span></span>

## <span data-ttu-id="d44f3-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d44f3-110">EXAMPLES</span></span>

### <span data-ttu-id="d44f3-111">Ponowne uruchamianie konkretnej usługi sygnalizującego</span><span class="sxs-lookup"><span data-stu-id="d44f3-111">Restart a specific SignalR service</span></span>
```powershell
PS C:\> Restart-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

<span data-ttu-id="d44f3-112">Domyślną grupę zasobów można ustawić przez \` Set-AzDefault-ResourceGroupName moja zasobów \` .</span><span class="sxs-lookup"><span data-stu-id="d44f3-112">The default resource group can be set by \`Set-AzDefault -ResourceGroupName myResourceGroup\`.</span></span>

## <span data-ttu-id="d44f3-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d44f3-113">PARAMETERS</span></span>

### <span data-ttu-id="d44f3-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d44f3-114">-AsJob</span></span>
<span data-ttu-id="d44f3-115">Uruchom polecenie cmdlet w zadaniu w tle.</span><span class="sxs-lookup"><span data-stu-id="d44f3-115">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="d44f3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d44f3-116">-DefaultProfile</span></span>
<span data-ttu-id="d44f3-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d44f3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d44f3-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d44f3-118">-InputObject</span></span>
<span data-ttu-id="d44f3-119">Obiekt zasobu sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="d44f3-119">The SignalR resource object.</span></span>

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

### <span data-ttu-id="d44f3-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d44f3-120">-Name</span></span>
<span data-ttu-id="d44f3-121">Nazwa usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="d44f3-121">The SignalR service name.</span></span>

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

### <span data-ttu-id="d44f3-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d44f3-122">-PassThru</span></span>
<span data-ttu-id="d44f3-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="d44f3-123">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="d44f3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d44f3-124">-ResourceGroupName</span></span>
<span data-ttu-id="d44f3-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d44f3-125">The resource group name.</span></span>
<span data-ttu-id="d44f3-126">Jeśli nie podano, zostanie użyte ustawienie domyślne.</span><span class="sxs-lookup"><span data-stu-id="d44f3-126">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="d44f3-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d44f3-127">-ResourceId</span></span>
<span data-ttu-id="d44f3-128">Identyfikator zasobu usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="d44f3-128">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="d44f3-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d44f3-129">-Confirm</span></span>
<span data-ttu-id="d44f3-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d44f3-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d44f3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d44f3-131">-WhatIf</span></span>
<span data-ttu-id="d44f3-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d44f3-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d44f3-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d44f3-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d44f3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d44f3-134">CommonParameters</span></span>
<span data-ttu-id="d44f3-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d44f3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d44f3-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d44f3-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d44f3-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d44f3-137">INPUTS</span></span>

### <span data-ttu-id="d44f3-138">System. String</span><span class="sxs-lookup"><span data-stu-id="d44f3-138">System.String</span></span>

### <span data-ttu-id="d44f3-139">Microsoft. Azure. Commands. Signals. modele. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="d44f3-139">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="d44f3-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d44f3-140">OUTPUTS</span></span>

### <span data-ttu-id="d44f3-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d44f3-141">System.Boolean</span></span>

## <span data-ttu-id="d44f3-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d44f3-142">NOTES</span></span>

## <span data-ttu-id="d44f3-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d44f3-143">RELATED LINKS</span></span>
