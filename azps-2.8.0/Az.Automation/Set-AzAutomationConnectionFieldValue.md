---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: CA25260C-D0BF-4F9C-A846-9D9B6C48CE8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationconnectionfieldvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationConnectionFieldValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationConnectionFieldValue.md
ms.openlocfilehash: 71f044dcce4944960d10fe2946b48c04354b8256
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706709"
---
# <span data-ttu-id="c0d30-101">Set-AzAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="c0d30-101">Set-AzAutomationConnectionFieldValue</span></span>

## <span data-ttu-id="c0d30-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c0d30-102">SYNOPSIS</span></span>
<span data-ttu-id="c0d30-103">Modyfikuje wartość pola w połączeniu automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="c0d30-103">Modifies the value of a field in an Automation connection.</span></span>

## <span data-ttu-id="c0d30-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c0d30-104">SYNTAX</span></span>

```
Set-AzAutomationConnectionFieldValue [-Name] <String> -ConnectionFieldName <String> -Value <Object>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c0d30-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c0d30-105">DESCRIPTION</span></span>
<span data-ttu-id="c0d30-106">Polecenie cmdlet **Set-AzAutomationConnectionFieldValue** modyfikuje wartość pola w połączeniu w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="c0d30-106">The **Set-AzAutomationConnectionFieldValue** cmdlet modifies the value of a field in a connection in Azure Automation.</span></span>

## <span data-ttu-id="c0d30-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c0d30-107">EXAMPLES</span></span>

### <span data-ttu-id="c0d30-108">Przykład 1. Zmienianie wartości pola w połączeniu</span><span class="sxs-lookup"><span data-stu-id="c0d30-108">Example 1: Change a field value in a connection</span></span>
```
PS C:\>Set-AzAutomationConnectionFieldValue -Name "ContosoConnection" -ConnectionFieldName "SubscriptionID" -Value "b53ec456-3494-4847-8f2b-180901c51050" -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="c0d30-109">To polecenie zmienia Identyfikator subskrypcji dla połączenia platformy Azure o nazwie ContosoConnection na koncie usługi Automation o nazwie AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="c0d30-109">This command changes the subscription ID for the Azure connection named ContosoConnection in the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="c0d30-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c0d30-110">PARAMETERS</span></span>

### <span data-ttu-id="c0d30-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c0d30-111">-AutomationAccountName</span></span>
<span data-ttu-id="c0d30-112">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet modyfikuje pole w połączeniu.</span><span class="sxs-lookup"><span data-stu-id="c0d30-112">Specifies the name of the Automation account for which this cmdlet modifies a field in a connection.</span></span>

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

### <span data-ttu-id="c0d30-113">-ConnectionFieldName</span><span class="sxs-lookup"><span data-stu-id="c0d30-113">-ConnectionFieldName</span></span>
<span data-ttu-id="c0d30-114">Określa nazwę pola, które zostanie zmodyfikowane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0d30-114">Specifies a name for the field that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="c0d30-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0d30-115">-DefaultProfile</span></span>
<span data-ttu-id="c0d30-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c0d30-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0d30-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c0d30-117">-Name</span></span>
<span data-ttu-id="c0d30-118">Określa nazwę połączenia, dla którego to polecenie cmdlet modyfikuje pole.</span><span class="sxs-lookup"><span data-stu-id="c0d30-118">Specifies a name for the connection for which this cmdlet modifies a field.</span></span>

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

### <span data-ttu-id="c0d30-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0d30-119">-ResourceGroupName</span></span>
<span data-ttu-id="c0d30-120">Określa nazwę grupy zasobów, dla której to polecenie cmdlet modyfikuje pole w połączeniu.</span><span class="sxs-lookup"><span data-stu-id="c0d30-120">Specifies the name of the resource group for which this cmdlet modifies a field in a connection.</span></span>

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

### <span data-ttu-id="c0d30-121">-Value</span><span class="sxs-lookup"><span data-stu-id="c0d30-121">-Value</span></span>
<span data-ttu-id="c0d30-122">Określa wartość do zmodyfikowania w polu połączenie.</span><span class="sxs-lookup"><span data-stu-id="c0d30-122">Specifies a value to modify in the connection field.</span></span>

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

### <span data-ttu-id="c0d30-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0d30-123">CommonParameters</span></span>
<span data-ttu-id="c0d30-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0d30-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0d30-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0d30-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0d30-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0d30-126">INPUTS</span></span>

### <span data-ttu-id="c0d30-127">System. String</span><span class="sxs-lookup"><span data-stu-id="c0d30-127">System.String</span></span>

### <span data-ttu-id="c0d30-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="c0d30-128">System.Object</span></span>

## <span data-ttu-id="c0d30-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c0d30-129">OUTPUTS</span></span>

### <span data-ttu-id="c0d30-130">Microsoft. Azure. Commands. Automation. model. Connection</span><span class="sxs-lookup"><span data-stu-id="c0d30-130">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="c0d30-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c0d30-131">NOTES</span></span>

## <span data-ttu-id="c0d30-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c0d30-132">RELATED LINKS</span></span>

[<span data-ttu-id="c0d30-133">Nowe — AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="c0d30-133">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)

