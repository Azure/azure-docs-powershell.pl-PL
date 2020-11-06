---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: CA25260C-D0BF-4F9C-A846-9D9B6C48CE8A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationConnectionFieldValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationConnectionFieldValue.md
ms.openlocfilehash: c3f889f45a90b127287821afb789eab2908faffa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552435"
---
# <span data-ttu-id="32994-101">Set-AzureRmAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="32994-101">Set-AzureRmAutomationConnectionFieldValue</span></span>

## <span data-ttu-id="32994-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="32994-102">SYNOPSIS</span></span>
<span data-ttu-id="32994-103">Modyfikuje wartość pola w połączeniu automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="32994-103">Modifies the value of a field in an Automation connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32994-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="32994-104">SYNTAX</span></span>

```
Set-AzureRmAutomationConnectionFieldValue [-Name] <String> -ConnectionFieldName <String> -Value <Object>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="32994-105">Opis</span><span class="sxs-lookup"><span data-stu-id="32994-105">DESCRIPTION</span></span>
<span data-ttu-id="32994-106">Polecenie cmdlet **Set-AzureRmAutomationConnectionFieldValue** modyfikuje wartość pola w połączeniu w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="32994-106">The **Set-AzureRmAutomationConnectionFieldValue** cmdlet modifies the value of a field in a connection in Azure Automation.</span></span>

## <span data-ttu-id="32994-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="32994-107">EXAMPLES</span></span>

### <span data-ttu-id="32994-108">Przykład 1. Zmienianie wartości pola w połączeniu</span><span class="sxs-lookup"><span data-stu-id="32994-108">Example 1: Change a field value in a connection</span></span>
```
PS C:\>Set-AzureRmAutomationConnectionFieldValue -Name "ContosoConnection" -ConnectionFieldName "SubscriptionID" -Value "b53ec456-3494-4847-8f2b-180901c51050" -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="32994-109">To polecenie zmienia Identyfikator subskrypcji dla połączenia platformy Azure o nazwie ContosoConnection na koncie usługi Automation o nazwie AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="32994-109">This command changes the subscription ID for the Azure connection named ContosoConnection in the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="32994-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="32994-110">PARAMETERS</span></span>

### <span data-ttu-id="32994-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="32994-111">-AutomationAccountName</span></span>
<span data-ttu-id="32994-112">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet modyfikuje pole w połączeniu.</span><span class="sxs-lookup"><span data-stu-id="32994-112">Specifies the name of the Automation account for which this cmdlet modifies a field in a connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32994-113">-ConnectionFieldName</span><span class="sxs-lookup"><span data-stu-id="32994-113">-ConnectionFieldName</span></span>
<span data-ttu-id="32994-114">Określa nazwę pola, które zostanie zmodyfikowane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32994-114">Specifies a name for the field that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32994-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="32994-115">-Name</span></span>
<span data-ttu-id="32994-116">Określa nazwę połączenia, dla którego to polecenie cmdlet modyfikuje pole.</span><span class="sxs-lookup"><span data-stu-id="32994-116">Specifies a name for the connection for which this cmdlet modifies a field.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32994-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32994-117">-ResourceGroupName</span></span>
<span data-ttu-id="32994-118">Określa nazwę grupy zasobów, dla której to polecenie cmdlet modyfikuje pole w połączeniu.</span><span class="sxs-lookup"><span data-stu-id="32994-118">Specifies the name of the resource group for which this cmdlet modifies a field in a connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32994-119">-Value</span><span class="sxs-lookup"><span data-stu-id="32994-119">-Value</span></span>
<span data-ttu-id="32994-120">Określa wartość do zmodyfikowania w polu połączenie.</span><span class="sxs-lookup"><span data-stu-id="32994-120">Specifies a value to modify in the connection field.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32994-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32994-121">-DefaultProfile</span></span>
<span data-ttu-id="32994-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="32994-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32994-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32994-123">CommonParameters</span></span>
<span data-ttu-id="32994-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32994-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32994-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32994-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32994-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="32994-126">INPUTS</span></span>

## <span data-ttu-id="32994-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="32994-127">OUTPUTS</span></span>

### <span data-ttu-id="32994-128">Microsoft. Azure. Commands. Automation. model. Connection</span><span class="sxs-lookup"><span data-stu-id="32994-128">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="32994-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="32994-129">NOTES</span></span>

## <span data-ttu-id="32994-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="32994-130">RELATED LINKS</span></span>

[<span data-ttu-id="32994-131">Nowe — AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="32994-131">New-AzureRmAutomationConnection</span></span>](./New-AzureRMAutomationConnection.md)


