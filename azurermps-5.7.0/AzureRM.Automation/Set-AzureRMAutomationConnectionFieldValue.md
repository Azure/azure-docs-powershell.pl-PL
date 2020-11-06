---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: CA25260C-D0BF-4F9C-A846-9D9B6C48CE8A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationconnectionfieldvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationConnectionFieldValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationConnectionFieldValue.md
ms.openlocfilehash: 84da08588838982353bc8c39354452bec1a17a78
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550708"
---
# <span data-ttu-id="47634-101">Set-AzureRmAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="47634-101">Set-AzureRmAutomationConnectionFieldValue</span></span>

## <span data-ttu-id="47634-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="47634-102">SYNOPSIS</span></span>
<span data-ttu-id="47634-103">Modyfikuje wartość pola w połączeniu automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="47634-103">Modifies the value of a field in an Automation connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47634-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="47634-104">SYNTAX</span></span>

```
Set-AzureRmAutomationConnectionFieldValue [-Name] <String> -ConnectionFieldName <String> -Value <Object>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="47634-105">Opis</span><span class="sxs-lookup"><span data-stu-id="47634-105">DESCRIPTION</span></span>
<span data-ttu-id="47634-106">Polecenie cmdlet **Set-AzureRmAutomationConnectionFieldValue** modyfikuje wartość pola w połączeniu w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="47634-106">The **Set-AzureRmAutomationConnectionFieldValue** cmdlet modifies the value of a field in a connection in Azure Automation.</span></span>

## <span data-ttu-id="47634-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="47634-107">EXAMPLES</span></span>

### <span data-ttu-id="47634-108">Przykład 1. Zmienianie wartości pola w połączeniu</span><span class="sxs-lookup"><span data-stu-id="47634-108">Example 1: Change a field value in a connection</span></span>
```
PS C:\>Set-AzureRmAutomationConnectionFieldValue -Name "ContosoConnection" -ConnectionFieldName "SubscriptionID" -Value "b53ec456-3494-4847-8f2b-180901c51050" -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="47634-109">To polecenie zmienia Identyfikator subskrypcji dla połączenia platformy Azure o nazwie ContosoConnection na koncie usługi Automation o nazwie AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="47634-109">This command changes the subscription ID for the Azure connection named ContosoConnection in the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="47634-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="47634-110">PARAMETERS</span></span>

### <span data-ttu-id="47634-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="47634-111">-AutomationAccountName</span></span>
<span data-ttu-id="47634-112">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet modyfikuje pole w połączeniu.</span><span class="sxs-lookup"><span data-stu-id="47634-112">Specifies the name of the Automation account for which this cmdlet modifies a field in a connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47634-113">-ConnectionFieldName</span><span class="sxs-lookup"><span data-stu-id="47634-113">-ConnectionFieldName</span></span>
<span data-ttu-id="47634-114">Określa nazwę pola, które zostanie zmodyfikowane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47634-114">Specifies a name for the field that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47634-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47634-115">-DefaultProfile</span></span>
<span data-ttu-id="47634-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="47634-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47634-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="47634-117">-Name</span></span>
<span data-ttu-id="47634-118">Określa nazwę połączenia, dla którego to polecenie cmdlet modyfikuje pole.</span><span class="sxs-lookup"><span data-stu-id="47634-118">Specifies a name for the connection for which this cmdlet modifies a field.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47634-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47634-119">-ResourceGroupName</span></span>
<span data-ttu-id="47634-120">Określa nazwę grupy zasobów, dla której to polecenie cmdlet modyfikuje pole w połączeniu.</span><span class="sxs-lookup"><span data-stu-id="47634-120">Specifies the name of the resource group for which this cmdlet modifies a field in a connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47634-121">-Value</span><span class="sxs-lookup"><span data-stu-id="47634-121">-Value</span></span>
<span data-ttu-id="47634-122">Określa wartość do zmodyfikowania w polu połączenie.</span><span class="sxs-lookup"><span data-stu-id="47634-122">Specifies a value to modify in the connection field.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47634-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47634-123">CommonParameters</span></span>
<span data-ttu-id="47634-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47634-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47634-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47634-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47634-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="47634-126">INPUTS</span></span>

### <span data-ttu-id="47634-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="47634-127">None</span></span>
<span data-ttu-id="47634-128">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="47634-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="47634-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="47634-129">OUTPUTS</span></span>

### <span data-ttu-id="47634-130">Microsoft. Azure. Commands. Automation. model. Connection</span><span class="sxs-lookup"><span data-stu-id="47634-130">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="47634-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="47634-131">NOTES</span></span>

## <span data-ttu-id="47634-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="47634-132">RELATED LINKS</span></span>

[<span data-ttu-id="47634-133">Nowe — AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="47634-133">New-AzureRmAutomationConnection</span></span>](./New-AzureRMAutomationConnection.md)


