---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2triggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2TriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2TriggerSubscription.md
ms.openlocfilehash: 89fb4591af19db46aa536ebd15f3746cf6691244
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242778"
---
# <span data-ttu-id="4afbd-101">Remove-AzDataFactoryV2TriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="4afbd-101">Remove-AzDataFactoryV2TriggerSubscription</span></span>

## <span data-ttu-id="4afbd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4afbd-102">SYNOPSIS</span></span>
<span data-ttu-id="4afbd-103">Anulowanie anulowania wyzwalacza zdarzenia w usłudze zewnętrznej.</span><span class="sxs-lookup"><span data-stu-id="4afbd-103">Unsubscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="4afbd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4afbd-104">SYNTAX</span></span>

### <span data-ttu-id="4afbd-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="4afbd-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-Name] <String> [-PassThru] [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4afbd-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4afbd-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-InputObject] <PSTrigger> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4afbd-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4afbd-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-PassThru] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4afbd-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="4afbd-108">DESCRIPTION</span></span>
<span data-ttu-id="4afbd-109">To polecenie anuluje subskrypcję wyzwalacza zdarzenia dla określonych zdarzeń usługi zewnętrznej z zdefiniowania wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="4afbd-109">This command unsubscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="4afbd-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4afbd-110">EXAMPLES</span></span>

### <span data-ttu-id="4afbd-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4afbd-111">Example 1</span></span>
```
PS C:\> Remove-AzDataFactoryV2TriggerSubscription -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1
```

<span data-ttu-id="4afbd-112">To polecenie anuluje subskrypcję wyzwalacza BlobEnetTrigger1 dla określonych zdarzeń w definicji wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="4afbd-112">This command will unsubscribe BlobEnetTrigger1 trigger to the specified events from the trigger defintion.</span></span>

## <span data-ttu-id="4afbd-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4afbd-113">PARAMETERS</span></span>

### <span data-ttu-id="4afbd-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="4afbd-114">-DataFactoryName</span></span>
<span data-ttu-id="4afbd-115">Nazwa fabryczna danych.</span><span class="sxs-lookup"><span data-stu-id="4afbd-115">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4afbd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4afbd-116">-DefaultProfile</span></span>
<span data-ttu-id="4afbd-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4afbd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4afbd-118">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="4afbd-118">-Force</span></span>
<span data-ttu-id="4afbd-119">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4afbd-119">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4afbd-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4afbd-120">-InputObject</span></span>
<span data-ttu-id="4afbd-121">Obiekt wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="4afbd-121">The trigger object.</span></span>

```yaml
Type: PSTrigger
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4afbd-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4afbd-122">-Name</span></span>
<span data-ttu-id="4afbd-123">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="4afbd-123">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4afbd-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4afbd-124">-PassThru</span></span>
<span data-ttu-id="4afbd-125">Jeśli zostanie określone, polecenie cmdlet zwróci wartość True (Prawda) po pomyślnym usunięciu.</span><span class="sxs-lookup"><span data-stu-id="4afbd-125">If specified, cmdlet will return return true on successful delete.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4afbd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4afbd-126">-ResourceGroupName</span></span>
<span data-ttu-id="4afbd-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4afbd-127">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4afbd-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4afbd-128">-ResourceId</span></span>
<span data-ttu-id="4afbd-129">Identyfikator zasobu Azure.</span><span class="sxs-lookup"><span data-stu-id="4afbd-129">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4afbd-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4afbd-130">-Confirm</span></span>
<span data-ttu-id="4afbd-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4afbd-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4afbd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4afbd-132">-WhatIf</span></span>
<span data-ttu-id="4afbd-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4afbd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4afbd-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4afbd-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4afbd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4afbd-135">CommonParameters</span></span>
<span data-ttu-id="4afbd-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4afbd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4afbd-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4afbd-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4afbd-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4afbd-138">INPUTS</span></span>

### <span data-ttu-id="4afbd-139">System.String</span><span class="sxs-lookup"><span data-stu-id="4afbd-139">System.String</span></span>
<span data-ttu-id="4afbd-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="4afbd-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="4afbd-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4afbd-141">OUTPUTS</span></span>

### <span data-ttu-id="4afbd-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="4afbd-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="4afbd-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4afbd-143">NOTES</span></span>

## <span data-ttu-id="4afbd-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4afbd-144">RELATED LINKS</span></span>

