---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/add-azdatafactoryv2triggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2TriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2TriggerSubscription.md
ms.openlocfilehash: 6e38f98f9dd3ebfaa2ad4747016556aecd9998e9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053387"
---
# <span data-ttu-id="3ad98-101">Add-AzDataFactoryV2TriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="3ad98-101">Add-AzDataFactoryV2TriggerSubscription</span></span>

## <span data-ttu-id="3ad98-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3ad98-102">SYNOPSIS</span></span>
<span data-ttu-id="3ad98-103">Zasubskrybuj wyzwalacz zdarzeń na zdarzenia usługi zewnętrznej.</span><span class="sxs-lookup"><span data-stu-id="3ad98-103">Subscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="3ad98-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3ad98-104">SYNTAX</span></span>

### <span data-ttu-id="3ad98-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3ad98-105">ByFactoryName (Default)</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3ad98-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3ad98-106">ByInputObject</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-InputObject] <PSTrigger> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ad98-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3ad98-107">ByResourceId</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ad98-108">Opis</span><span class="sxs-lookup"><span data-stu-id="3ad98-108">DESCRIPTION</span></span>
<span data-ttu-id="3ad98-109">To polecenie umożliwia zasubskrybowanie wyzwalacza zdarzeń do określonych zdarzeń usług zewnętrznych z poziomu wyzwalacza defintion.</span><span class="sxs-lookup"><span data-stu-id="3ad98-109">This command subscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="3ad98-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3ad98-110">EXAMPLES</span></span>

### <span data-ttu-id="3ad98-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3ad98-111">Example 1</span></span>
```
PS C:\> Add-AzDataFactoryV2TriggerSubscription -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1

TriggerName Status
----------- ------
Trigger1    Provisioning
```

<span data-ttu-id="3ad98-112">To polecenie spowoduje zasubskrybowanie wyzwalacza BlobEnetTrigger1 do określonych zdarzeń z poziomu wyzwalacza defintion.</span><span class="sxs-lookup"><span data-stu-id="3ad98-112">This command will subscribe BlobEnetTrigger1 trigger to the specified events from the trigger defintion.</span></span>

## <span data-ttu-id="3ad98-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3ad98-113">PARAMETERS</span></span>

### <span data-ttu-id="3ad98-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="3ad98-114">-DataFactoryName</span></span>
<span data-ttu-id="3ad98-115">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="3ad98-115">The data factory name.</span></span>

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

### <span data-ttu-id="3ad98-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ad98-116">-DefaultProfile</span></span>
<span data-ttu-id="3ad98-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3ad98-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ad98-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3ad98-118">-InputObject</span></span>
<span data-ttu-id="3ad98-119">Obiekt Trigger.</span><span class="sxs-lookup"><span data-stu-id="3ad98-119">The trigger object.</span></span>

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

### <span data-ttu-id="3ad98-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3ad98-120">-Name</span></span>
<span data-ttu-id="3ad98-121">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="3ad98-121">The trigger name.</span></span>

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

### <span data-ttu-id="3ad98-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ad98-122">-ResourceGroupName</span></span>
<span data-ttu-id="3ad98-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3ad98-123">The resource group name.</span></span>

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

### <span data-ttu-id="3ad98-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ad98-124">-ResourceId</span></span>
<span data-ttu-id="3ad98-125">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3ad98-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="3ad98-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3ad98-126">-Confirm</span></span>
<span data-ttu-id="3ad98-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ad98-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ad98-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ad98-128">-WhatIf</span></span>
<span data-ttu-id="3ad98-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ad98-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ad98-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3ad98-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ad98-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ad98-131">CommonParameters</span></span>
<span data-ttu-id="3ad98-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ad98-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ad98-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ad98-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ad98-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3ad98-134">INPUTS</span></span>

### <span data-ttu-id="3ad98-135">System. String</span><span class="sxs-lookup"><span data-stu-id="3ad98-135">System.String</span></span>
<span data-ttu-id="3ad98-136">Microsoft. Azure. Commands. DataFactoryV2. models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="3ad98-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="3ad98-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3ad98-137">OUTPUTS</span></span>

### <span data-ttu-id="3ad98-138">Microsoft. Azure. Commands. DataFactoryV2. models. PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="3ad98-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="3ad98-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3ad98-139">NOTES</span></span>

## <span data-ttu-id="3ad98-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3ad98-140">RELATED LINKS</span></span>

