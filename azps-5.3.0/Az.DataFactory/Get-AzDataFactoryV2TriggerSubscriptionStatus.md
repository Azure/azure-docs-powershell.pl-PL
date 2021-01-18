---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2triggersubscriptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerSubscriptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerSubscriptionStatus.md
ms.openlocfilehash: 62418f0840e2bbeef016d53c3136f155c4de055f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503677"
---
# <span data-ttu-id="1a62a-101">Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="1a62a-101">Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>

## <span data-ttu-id="1a62a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1a62a-102">SYNOPSIS</span></span>
<span data-ttu-id="1a62a-103">Uzyskaj stan subskrypcji wyzwalacza zdarzeń na określone zdarzenia usługi zewnętrznej.</span><span class="sxs-lookup"><span data-stu-id="1a62a-103">Get the status of the subscription for the event trigger to the specified external service events.</span></span>

## <span data-ttu-id="1a62a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1a62a-104">SYNTAX</span></span>

### <span data-ttu-id="1a62a-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1a62a-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a62a-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1a62a-106">ByInputObject</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-InputObject] <PSTrigger>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a62a-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1a62a-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1a62a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="1a62a-108">DESCRIPTION</span></span>
<span data-ttu-id="1a62a-109">To polecenie pobiera stan subskrypcji wyzwalacza zdarzeń do określonych zdarzeń usługi zewnętrznej.</span><span class="sxs-lookup"><span data-stu-id="1a62a-109">This command gets the status of the subscription for the event trigger to the specified external service events.</span></span> <span data-ttu-id="1a62a-110">Nie można uruchomić wyzwalacza, dopóki nie zostanie zwrócony stan "włączony".</span><span class="sxs-lookup"><span data-stu-id="1a62a-110">The trigger can't be started until the returned status is "Enabled".</span></span>

## <span data-ttu-id="1a62a-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1a62a-111">EXAMPLES</span></span>

### <span data-ttu-id="1a62a-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1a62a-112">Example 1</span></span>
```
PS C:\> Get-AzDataFactoryV2TriggerSubscriptionStatus -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1

TriggerName Status
----------- ------
Trigger1    Enabled
```

<span data-ttu-id="1a62a-113">To polecenie spowoduje wyświetlenie stanu wyzwalacza subscribtion dla BlobEnetTrigger1 na zdarzenia usługi zewnętrznej.</span><span class="sxs-lookup"><span data-stu-id="1a62a-113">This command will get the status of the subscribtion for BlobEnetTrigger1 trigger to the external service events.</span></span>

## <span data-ttu-id="1a62a-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1a62a-114">PARAMETERS</span></span>

### <span data-ttu-id="1a62a-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="1a62a-115">-DataFactoryName</span></span>
<span data-ttu-id="1a62a-116">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="1a62a-116">The data factory name.</span></span>

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

### <span data-ttu-id="1a62a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a62a-117">-DefaultProfile</span></span>
<span data-ttu-id="1a62a-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1a62a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a62a-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1a62a-119">-InputObject</span></span>
<span data-ttu-id="1a62a-120">Obiekt Trigger.</span><span class="sxs-lookup"><span data-stu-id="1a62a-120">The trigger object.</span></span>

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

### <span data-ttu-id="1a62a-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1a62a-121">-Name</span></span>
<span data-ttu-id="1a62a-122">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="1a62a-122">The trigger name.</span></span>

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

### <span data-ttu-id="1a62a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a62a-123">-ResourceGroupName</span></span>
<span data-ttu-id="1a62a-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1a62a-124">The resource group name.</span></span>

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

### <span data-ttu-id="1a62a-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1a62a-125">-ResourceId</span></span>
<span data-ttu-id="1a62a-126">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1a62a-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="1a62a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a62a-127">CommonParameters</span></span>
<span data-ttu-id="1a62a-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a62a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a62a-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a62a-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a62a-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1a62a-130">INPUTS</span></span>

### <span data-ttu-id="1a62a-131">System. String</span><span class="sxs-lookup"><span data-stu-id="1a62a-131">System.String</span></span>
<span data-ttu-id="1a62a-132">Microsoft. Azure. Commands. DataFactoryV2. models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="1a62a-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="1a62a-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1a62a-133">OUTPUTS</span></span>

### <span data-ttu-id="1a62a-134">Microsoft. Azure. Commands. DataFactoryV2. models. PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="1a62a-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="1a62a-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1a62a-135">NOTES</span></span>

## <span data-ttu-id="1a62a-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1a62a-136">RELATED LINKS</span></span>

