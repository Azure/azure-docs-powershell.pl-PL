---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/remove-azdatafactoryv2triggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2TriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2TriggerSubscription.md
ms.openlocfilehash: 1ab801c9eca278d5d117ddca881867371882980c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996808"
---
# <span data-ttu-id="78f8e-101">Remove-AzDataFactoryV2TriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="78f8e-101">Remove-AzDataFactoryV2TriggerSubscription</span></span>

## <span data-ttu-id="78f8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78f8e-102">SYNOPSIS</span></span>
<span data-ttu-id="78f8e-103">Anulowanie anulowania wyzwalacza zdarzenia w usłudze zewnętrznej.</span><span class="sxs-lookup"><span data-stu-id="78f8e-103">Unsubscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="78f8e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="78f8e-104">SYNTAX</span></span>

### <span data-ttu-id="78f8e-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="78f8e-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-Name] <String> [-PassThru] [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="78f8e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="78f8e-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-InputObject] <PSTrigger> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78f8e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="78f8e-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-PassThru] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78f8e-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="78f8e-108">DESCRIPTION</span></span>
<span data-ttu-id="78f8e-109">To polecenie anuluje subskrypcję wyzwalacza zdarzenia dla określonych zdarzeń usługi zewnętrznej z zdefiniowania wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="78f8e-109">This command unsubscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="78f8e-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="78f8e-110">EXAMPLES</span></span>

### <span data-ttu-id="78f8e-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="78f8e-111">Example 1</span></span>
```
PS C:\> Remove-AzDataFactoryV2TriggerSubscription -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1
```

<span data-ttu-id="78f8e-112">To polecenie anuluje subskrypcję wyzwalacza BlobEnetTrigger1 dla określonych zdarzeń w definicji wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="78f8e-112">This command will unsubscribe BlobEnetTrigger1 trigger to the specified events from the trigger defintion.</span></span>

## <span data-ttu-id="78f8e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="78f8e-113">PARAMETERS</span></span>

### <span data-ttu-id="78f8e-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="78f8e-114">-DataFactoryName</span></span>
<span data-ttu-id="78f8e-115">Nazwa fabryczna danych.</span><span class="sxs-lookup"><span data-stu-id="78f8e-115">The data factory name.</span></span>

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

### <span data-ttu-id="78f8e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78f8e-116">-DefaultProfile</span></span>
<span data-ttu-id="78f8e-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="78f8e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78f8e-118">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="78f8e-118">-Force</span></span>
<span data-ttu-id="78f8e-119">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="78f8e-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="78f8e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78f8e-120">-InputObject</span></span>
<span data-ttu-id="78f8e-121">Obiekt wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="78f8e-121">The trigger object.</span></span>

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

### <span data-ttu-id="78f8e-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="78f8e-122">-Name</span></span>
<span data-ttu-id="78f8e-123">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="78f8e-123">The trigger name.</span></span>

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

### <span data-ttu-id="78f8e-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="78f8e-124">-PassThru</span></span>
<span data-ttu-id="78f8e-125">Jeśli zostanie określone, polecenie cmdlet zwróci wartość True (Prawda) po pomyślnym usunięciu.</span><span class="sxs-lookup"><span data-stu-id="78f8e-125">If specified, cmdlet will return return true on successful delete.</span></span>

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

### <span data-ttu-id="78f8e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78f8e-126">-ResourceGroupName</span></span>
<span data-ttu-id="78f8e-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="78f8e-127">The resource group name.</span></span>

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

### <span data-ttu-id="78f8e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78f8e-128">-ResourceId</span></span>
<span data-ttu-id="78f8e-129">Identyfikator zasobu Azure.</span><span class="sxs-lookup"><span data-stu-id="78f8e-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="78f8e-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="78f8e-130">-Confirm</span></span>
<span data-ttu-id="78f8e-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="78f8e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78f8e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78f8e-132">-WhatIf</span></span>
<span data-ttu-id="78f8e-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78f8e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78f8e-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="78f8e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78f8e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78f8e-135">CommonParameters</span></span>
<span data-ttu-id="78f8e-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78f8e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78f8e-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78f8e-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78f8e-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="78f8e-138">INPUTS</span></span>

### <span data-ttu-id="78f8e-139">System.String</span><span class="sxs-lookup"><span data-stu-id="78f8e-139">System.String</span></span>
<span data-ttu-id="78f8e-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="78f8e-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="78f8e-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="78f8e-141">OUTPUTS</span></span>

### <span data-ttu-id="78f8e-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="78f8e-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="78f8e-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="78f8e-143">NOTES</span></span>

## <span data-ttu-id="78f8e-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="78f8e-144">RELATED LINKS</span></span>

