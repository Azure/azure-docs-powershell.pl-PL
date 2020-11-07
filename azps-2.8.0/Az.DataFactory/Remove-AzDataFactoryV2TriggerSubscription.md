---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2triggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2TriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2TriggerSubscription.md
ms.openlocfilehash: c1e7fab8eb4e8afe22bdebc5930c8599c2dadceb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705951"
---
# <span data-ttu-id="5cf73-101">Remove-AzDataFactoryV2TriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="5cf73-101">Remove-AzDataFactoryV2TriggerSubscription</span></span>

## <span data-ttu-id="5cf73-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5cf73-102">SYNOPSIS</span></span>
<span data-ttu-id="5cf73-103">Anulowanie subskrypcji wyzwalacza zdarzeń na zdarzenia usługi zewnętrznej.</span><span class="sxs-lookup"><span data-stu-id="5cf73-103">Unsubscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="5cf73-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5cf73-104">SYNTAX</span></span>

### <span data-ttu-id="5cf73-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5cf73-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-Name] <String> [-PassThru] [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5cf73-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5cf73-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-InputObject] <PSTrigger> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cf73-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5cf73-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-PassThru] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5cf73-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5cf73-108">DESCRIPTION</span></span>
<span data-ttu-id="5cf73-109">To polecenie spowoduje anulowanie subskrypcji wyzwalacza zdarzeń do określonych zdarzeń usług zewnętrznych z poziomu wyzwalacza defintion.</span><span class="sxs-lookup"><span data-stu-id="5cf73-109">This command unsubscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="5cf73-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5cf73-110">EXAMPLES</span></span>

### <span data-ttu-id="5cf73-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5cf73-111">Example 1</span></span>
```
PS C:\> Remove-AzDataFactoryV2TriggerSubscription -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1
```

<span data-ttu-id="5cf73-112">To polecenie spowoduje anulowanie subskrypcji wyzwalacza BlobEnetTrigger1 z określonymi zdarzeniami z wyzwalacza defintion.</span><span class="sxs-lookup"><span data-stu-id="5cf73-112">This command will unsubscribe BlobEnetTrigger1 trigger to the specified events from the trigger defintion.</span></span>

## <span data-ttu-id="5cf73-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5cf73-113">PARAMETERS</span></span>

### <span data-ttu-id="5cf73-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="5cf73-114">-DataFactoryName</span></span>
<span data-ttu-id="5cf73-115">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="5cf73-115">The data factory name.</span></span>

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

### <span data-ttu-id="5cf73-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cf73-116">-DefaultProfile</span></span>
<span data-ttu-id="5cf73-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5cf73-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5cf73-118">-Force</span><span class="sxs-lookup"><span data-stu-id="5cf73-118">-Force</span></span>
<span data-ttu-id="5cf73-119">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5cf73-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="5cf73-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5cf73-120">-InputObject</span></span>
<span data-ttu-id="5cf73-121">Obiekt Trigger.</span><span class="sxs-lookup"><span data-stu-id="5cf73-121">The trigger object.</span></span>

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

### <span data-ttu-id="5cf73-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5cf73-122">-Name</span></span>
<span data-ttu-id="5cf73-123">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="5cf73-123">The trigger name.</span></span>

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

### <span data-ttu-id="5cf73-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5cf73-124">-PassThru</span></span>
<span data-ttu-id="5cf73-125">Jeśli ta właściwość jest określona, polecenie cmdlet zwraca wartość prawda w przypadku udanego usunięcia.</span><span class="sxs-lookup"><span data-stu-id="5cf73-125">If specified, cmdlet will return return true on successful delete.</span></span>

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

### <span data-ttu-id="5cf73-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cf73-126">-ResourceGroupName</span></span>
<span data-ttu-id="5cf73-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5cf73-127">The resource group name.</span></span>

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

### <span data-ttu-id="5cf73-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5cf73-128">-ResourceId</span></span>
<span data-ttu-id="5cf73-129">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5cf73-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="5cf73-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5cf73-130">-Confirm</span></span>
<span data-ttu-id="5cf73-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5cf73-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cf73-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cf73-132">-WhatIf</span></span>
<span data-ttu-id="5cf73-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5cf73-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cf73-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5cf73-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cf73-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cf73-135">CommonParameters</span></span>
<span data-ttu-id="5cf73-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cf73-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cf73-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cf73-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cf73-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5cf73-138">INPUTS</span></span>

### <span data-ttu-id="5cf73-139">System. String</span><span class="sxs-lookup"><span data-stu-id="5cf73-139">System.String</span></span>
<span data-ttu-id="5cf73-140">Microsoft. Azure. Commands. DataFactoryV2. models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="5cf73-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="5cf73-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5cf73-141">OUTPUTS</span></span>

### <span data-ttu-id="5cf73-142">Microsoft. Azure. Commands. DataFactoryV2. models. PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="5cf73-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="5cf73-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5cf73-143">NOTES</span></span>

## <span data-ttu-id="5cf73-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5cf73-144">RELATED LINKS</span></span>

