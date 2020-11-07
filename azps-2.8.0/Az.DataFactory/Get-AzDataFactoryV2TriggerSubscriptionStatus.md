---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2triggersubscriptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerSubscriptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerSubscriptionStatus.md
ms.openlocfilehash: fedb3db8ae8d7cd64ab4309da65f9dea998826e4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706009"
---
# <span data-ttu-id="e5f7d-101">Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="e5f7d-101">Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>

## <span data-ttu-id="e5f7d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e5f7d-102">SYNOPSIS</span></span>
<span data-ttu-id="e5f7d-103">Uzyskaj stan subskrypcji wyzwalacza zdarzeń na określone zdarzenia usługi zewnętrznej.</span><span class="sxs-lookup"><span data-stu-id="e5f7d-103">Get the status of the subscription for the event trigger to the specified external service events.</span></span>

## <span data-ttu-id="e5f7d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e5f7d-104">SYNTAX</span></span>

### <span data-ttu-id="e5f7d-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e5f7d-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5f7d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e5f7d-106">ByInputObject</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-InputObject] <PSTrigger>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5f7d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e5f7d-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e5f7d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e5f7d-108">DESCRIPTION</span></span>
<span data-ttu-id="e5f7d-109">To polecenie pobiera stan subskrypcji wyzwalacza zdarzeń do określonych zdarzeń usługi zewnętrznej.</span><span class="sxs-lookup"><span data-stu-id="e5f7d-109">This command gets the status of the subscription for the event trigger to the specified external service events.</span></span> <span data-ttu-id="e5f7d-110">Nie można uruchomić wyzwalacza, dopóki nie zostanie zwrócony stan "włączony".</span><span class="sxs-lookup"><span data-stu-id="e5f7d-110">The trigger can't be started until the returned status is "Enabled".</span></span>

## <span data-ttu-id="e5f7d-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e5f7d-111">EXAMPLES</span></span>

### <span data-ttu-id="e5f7d-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e5f7d-112">Example 1</span></span>
```
PS C:\> Get-AzDataFactoryV2TriggerSubscriptionStatus -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1

TriggerName Status
----------- ------
Trigger1    Enabled
```

<span data-ttu-id="e5f7d-113">To polecenie spowoduje wyświetlenie stanu wyzwalacza subscribtion dla BlobEnetTrigger1 na zdarzenia usługi zewnętrznej.</span><span class="sxs-lookup"><span data-stu-id="e5f7d-113">This command will get the status of the subscribtion for BlobEnetTrigger1 trigger to the external service events.</span></span>

## <span data-ttu-id="e5f7d-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e5f7d-114">PARAMETERS</span></span>

### <span data-ttu-id="e5f7d-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="e5f7d-115">-DataFactoryName</span></span>
<span data-ttu-id="e5f7d-116">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="e5f7d-116">The data factory name.</span></span>

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

### <span data-ttu-id="e5f7d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5f7d-117">-DefaultProfile</span></span>
<span data-ttu-id="e5f7d-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e5f7d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5f7d-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e5f7d-119">-InputObject</span></span>
<span data-ttu-id="e5f7d-120">Obiekt Trigger.</span><span class="sxs-lookup"><span data-stu-id="e5f7d-120">The trigger object.</span></span>

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

### <span data-ttu-id="e5f7d-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e5f7d-121">-Name</span></span>
<span data-ttu-id="e5f7d-122">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="e5f7d-122">The trigger name.</span></span>

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

### <span data-ttu-id="e5f7d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5f7d-123">-ResourceGroupName</span></span>
<span data-ttu-id="e5f7d-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e5f7d-124">The resource group name.</span></span>

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

### <span data-ttu-id="e5f7d-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5f7d-125">-ResourceId</span></span>
<span data-ttu-id="e5f7d-126">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e5f7d-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="e5f7d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5f7d-127">CommonParameters</span></span>
<span data-ttu-id="e5f7d-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5f7d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5f7d-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5f7d-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5f7d-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e5f7d-130">INPUTS</span></span>

### <span data-ttu-id="e5f7d-131">System. String</span><span class="sxs-lookup"><span data-stu-id="e5f7d-131">System.String</span></span>
<span data-ttu-id="e5f7d-132">Microsoft. Azure. Commands. DataFactoryV2. models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="e5f7d-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="e5f7d-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e5f7d-133">OUTPUTS</span></span>

### <span data-ttu-id="e5f7d-134">Microsoft. Azure. Commands. DataFactoryV2. models. PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="e5f7d-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="e5f7d-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e5f7d-135">NOTES</span></span>

## <span data-ttu-id="e5f7d-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e5f7d-136">RELATED LINKS</span></span>

