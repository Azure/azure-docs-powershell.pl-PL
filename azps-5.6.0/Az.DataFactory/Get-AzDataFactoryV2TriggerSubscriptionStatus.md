---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2triggersubscriptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerSubscriptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerSubscriptionStatus.md
ms.openlocfilehash: a83028b47d487f4bbb2732497d7e9eefd01882ce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975114"
---
# <span data-ttu-id="fd176-101">Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="fd176-101">Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>

## <span data-ttu-id="fd176-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd176-102">SYNOPSIS</span></span>
<span data-ttu-id="fd176-103">Uzyskiwanie stanu subskrypcji wyzwalacza zdarzenia dla określonych zdarzeń usługi zewnętrznej.</span><span class="sxs-lookup"><span data-stu-id="fd176-103">Get the status of the subscription for the event trigger to the specified external service events.</span></span>

## <span data-ttu-id="fd176-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fd176-104">SYNTAX</span></span>

### <span data-ttu-id="fd176-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="fd176-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd176-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fd176-106">ByInputObject</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-InputObject] <PSTrigger>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd176-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fd176-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fd176-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="fd176-108">DESCRIPTION</span></span>
<span data-ttu-id="fd176-109">To polecenie otrzymuje stan subskrypcji wyzwalacza zdarzenia dla określonych zdarzeń usługi zewnętrznej.</span><span class="sxs-lookup"><span data-stu-id="fd176-109">This command gets the status of the subscription for the event trigger to the specified external service events.</span></span> <span data-ttu-id="fd176-110">Wyzwalacza nie można uruchomić, dopóki nie zostanie zwrócony stan "Włączony".</span><span class="sxs-lookup"><span data-stu-id="fd176-110">The trigger can't be started until the returned status is "Enabled".</span></span>

## <span data-ttu-id="fd176-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fd176-111">EXAMPLES</span></span>

### <span data-ttu-id="fd176-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fd176-112">Example 1</span></span>
```
PS C:\> Get-AzDataFactoryV2TriggerSubscriptionStatus -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1

TriggerName Status
----------- ------
Trigger1    Enabled
```

<span data-ttu-id="fd176-113">To polecenie pobierze stan subscribtion wyzwalacza BlobEnetTrigger1 do zdarzeń usługi zewnętrznej.</span><span class="sxs-lookup"><span data-stu-id="fd176-113">This command will get the status of the subscribtion for BlobEnetTrigger1 trigger to the external service events.</span></span>

## <span data-ttu-id="fd176-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd176-114">PARAMETERS</span></span>

### <span data-ttu-id="fd176-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="fd176-115">-DataFactoryName</span></span>
<span data-ttu-id="fd176-116">Nazwa fabryczna danych.</span><span class="sxs-lookup"><span data-stu-id="fd176-116">The data factory name.</span></span>

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

### <span data-ttu-id="fd176-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd176-117">-DefaultProfile</span></span>
<span data-ttu-id="fd176-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fd176-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd176-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd176-119">-InputObject</span></span>
<span data-ttu-id="fd176-120">Obiekt wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="fd176-120">The trigger object.</span></span>

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

### <span data-ttu-id="fd176-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="fd176-121">-Name</span></span>
<span data-ttu-id="fd176-122">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="fd176-122">The trigger name.</span></span>

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

### <span data-ttu-id="fd176-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd176-123">-ResourceGroupName</span></span>
<span data-ttu-id="fd176-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fd176-124">The resource group name.</span></span>

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

### <span data-ttu-id="fd176-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd176-125">-ResourceId</span></span>
<span data-ttu-id="fd176-126">Identyfikator zasobu Azure.</span><span class="sxs-lookup"><span data-stu-id="fd176-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="fd176-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd176-127">CommonParameters</span></span>
<span data-ttu-id="fd176-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd176-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd176-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd176-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd176-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fd176-130">INPUTS</span></span>

### <span data-ttu-id="fd176-131">System.String</span><span class="sxs-lookup"><span data-stu-id="fd176-131">System.String</span></span>
<span data-ttu-id="fd176-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="fd176-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="fd176-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fd176-133">OUTPUTS</span></span>

### <span data-ttu-id="fd176-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="fd176-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="fd176-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fd176-135">NOTES</span></span>

## <span data-ttu-id="fd176-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fd176-136">RELATED LINKS</span></span>

