---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/add-azdatafactoryv2triggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2TriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2TriggerSubscription.md
ms.openlocfilehash: c74eb60e698cff0d95a4361235c9282f1405dce0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992804"
---
# <span data-ttu-id="b3843-101">Add-AzDataFactoryV2TriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="b3843-101">Add-AzDataFactoryV2TriggerSubscription</span></span>

## <span data-ttu-id="b3843-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3843-102">SYNOPSIS</span></span>
<span data-ttu-id="b3843-103">Zasubskrybuj wyzwalacz zdarzenia zdarzenia w usłudze zewnętrznej.</span><span class="sxs-lookup"><span data-stu-id="b3843-103">Subscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="b3843-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b3843-104">SYNTAX</span></span>

### <span data-ttu-id="b3843-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="b3843-105">ByFactoryName (Default)</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b3843-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b3843-106">ByInputObject</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-InputObject] <PSTrigger> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3843-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b3843-107">ByResourceId</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3843-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="b3843-108">DESCRIPTION</span></span>
<span data-ttu-id="b3843-109">To polecenie subskrybuje wyzwalacz zdarzenia określonym zdarzeniami usługi zewnętrznej z definicji wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="b3843-109">This command subscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="b3843-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b3843-110">EXAMPLES</span></span>

### <span data-ttu-id="b3843-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b3843-111">Example 1</span></span>
```
PS C:\> Add-AzDataFactoryV2TriggerSubscription -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1

TriggerName Status
----------- ------
Trigger1    Provisioning
```

<span data-ttu-id="b3843-112">To polecenie subskrybuje wyzwalacz BlobEnetTrigger1 określonym zdarzeniam z definicji wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="b3843-112">This command will subscribe BlobEnetTrigger1 trigger to the specified events from the trigger defintion.</span></span>

## <span data-ttu-id="b3843-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3843-113">PARAMETERS</span></span>

### <span data-ttu-id="b3843-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b3843-114">-DataFactoryName</span></span>
<span data-ttu-id="b3843-115">Nazwa fabryczna danych.</span><span class="sxs-lookup"><span data-stu-id="b3843-115">The data factory name.</span></span>

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

### <span data-ttu-id="b3843-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3843-116">-DefaultProfile</span></span>
<span data-ttu-id="b3843-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b3843-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3843-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3843-118">-InputObject</span></span>
<span data-ttu-id="b3843-119">Obiekt wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="b3843-119">The trigger object.</span></span>

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

### <span data-ttu-id="b3843-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b3843-120">-Name</span></span>
<span data-ttu-id="b3843-121">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="b3843-121">The trigger name.</span></span>

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

### <span data-ttu-id="b3843-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3843-122">-ResourceGroupName</span></span>
<span data-ttu-id="b3843-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b3843-123">The resource group name.</span></span>

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

### <span data-ttu-id="b3843-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3843-124">-ResourceId</span></span>
<span data-ttu-id="b3843-125">Identyfikator zasobu Azure.</span><span class="sxs-lookup"><span data-stu-id="b3843-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="b3843-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b3843-126">-Confirm</span></span>
<span data-ttu-id="b3843-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b3843-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3843-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3843-128">-WhatIf</span></span>
<span data-ttu-id="b3843-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3843-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3843-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b3843-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3843-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3843-131">CommonParameters</span></span>
<span data-ttu-id="b3843-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3843-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3843-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3843-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3843-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b3843-134">INPUTS</span></span>

### <span data-ttu-id="b3843-135">System.String</span><span class="sxs-lookup"><span data-stu-id="b3843-135">System.String</span></span>
<span data-ttu-id="b3843-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="b3843-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="b3843-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b3843-137">OUTPUTS</span></span>

### <span data-ttu-id="b3843-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="b3843-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="b3843-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b3843-139">NOTES</span></span>

## <span data-ttu-id="b3843-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b3843-140">RELATED LINKS</span></span>

