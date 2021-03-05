---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: CA25260C-D0BF-4F9C-A846-9D9B6C48CE8A
online version: https://docs.microsoft.com/powershell/module/az.automation/set-azautomationconnectionfieldvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationConnectionFieldValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationConnectionFieldValue.md
ms.openlocfilehash: d11b99352d3a3f75c24e47cabfe06e816958fb82
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004737"
---
# <span data-ttu-id="19352-101">Set-AzAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="19352-101">Set-AzAutomationConnectionFieldValue</span></span>

## <span data-ttu-id="19352-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19352-102">SYNOPSIS</span></span>
<span data-ttu-id="19352-103">Modyfikuje wartość pola w połączeniu automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="19352-103">Modifies the value of a field in an Automation connection.</span></span>

## <span data-ttu-id="19352-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="19352-104">SYNTAX</span></span>

```
Set-AzAutomationConnectionFieldValue [-Name] <String> -ConnectionFieldName <String> -Value <Object>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="19352-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="19352-105">DESCRIPTION</span></span>
<span data-ttu-id="19352-106">Polecenie **cmdlet Set-AzAutomationConnectionFieldValue** modyfikuje wartość pola w połączeniu w automatyzacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="19352-106">The **Set-AzAutomationConnectionFieldValue** cmdlet modifies the value of a field in a connection in Azure Automation.</span></span>

## <span data-ttu-id="19352-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="19352-107">EXAMPLES</span></span>

### <span data-ttu-id="19352-108">Przykład 1. Zmienianie wartości pola w połączeniu</span><span class="sxs-lookup"><span data-stu-id="19352-108">Example 1: Change a field value in a connection</span></span>
```
PS C:\>Set-AzAutomationConnectionFieldValue -Name "ContosoConnection" -ConnectionFieldName "SubscriptionID" -Value "b53ec456-3494-4847-8f2b-180901c51050" -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="19352-109">To polecenie zmienia identyfikator subskrypcji dla połączenia platformy Azure o nazwie ContosoConnection na koncie automatyzacji o nazwie AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="19352-109">This command changes the subscription ID for the Azure connection named ContosoConnection in the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="19352-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19352-110">PARAMETERS</span></span>

### <span data-ttu-id="19352-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="19352-111">-AutomationAccountName</span></span>
<span data-ttu-id="19352-112">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet modyfikuje pole w połączeniu.</span><span class="sxs-lookup"><span data-stu-id="19352-112">Specifies the name of the Automation account for which this cmdlet modifies a field in a connection.</span></span>

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

### <span data-ttu-id="19352-113">-ConnectionFieldName</span><span class="sxs-lookup"><span data-stu-id="19352-113">-ConnectionFieldName</span></span>
<span data-ttu-id="19352-114">Określa nazwę pola, które to polecenie cmdlet modyfikuje.</span><span class="sxs-lookup"><span data-stu-id="19352-114">Specifies a name for the field that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="19352-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19352-115">-DefaultProfile</span></span>
<span data-ttu-id="19352-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="19352-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="19352-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="19352-117">-Name</span></span>
<span data-ttu-id="19352-118">Określa nazwę połączenia, dla którego to polecenie cmdlet modyfikuje pole.</span><span class="sxs-lookup"><span data-stu-id="19352-118">Specifies a name for the connection for which this cmdlet modifies a field.</span></span>

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

### <span data-ttu-id="19352-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19352-119">-ResourceGroupName</span></span>
<span data-ttu-id="19352-120">Określa nazwę grupy zasobów, dla której to polecenie cmdlet modyfikuje pole w połączeniu.</span><span class="sxs-lookup"><span data-stu-id="19352-120">Specifies the name of the resource group for which this cmdlet modifies a field in a connection.</span></span>

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

### <span data-ttu-id="19352-121">— Wartość</span><span class="sxs-lookup"><span data-stu-id="19352-121">-Value</span></span>
<span data-ttu-id="19352-122">Określa wartość do zmodyfikowania w polu połączenia.</span><span class="sxs-lookup"><span data-stu-id="19352-122">Specifies a value to modify in the connection field.</span></span>

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

### <span data-ttu-id="19352-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19352-123">CommonParameters</span></span>
<span data-ttu-id="19352-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19352-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19352-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19352-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19352-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="19352-126">INPUTS</span></span>

### <span data-ttu-id="19352-127">System.String</span><span class="sxs-lookup"><span data-stu-id="19352-127">System.String</span></span>

### <span data-ttu-id="19352-128">System.Object</span><span class="sxs-lookup"><span data-stu-id="19352-128">System.Object</span></span>

## <span data-ttu-id="19352-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="19352-129">OUTPUTS</span></span>

### <span data-ttu-id="19352-130">Microsoft.Azure.Commands.Automation.Model.Connection</span><span class="sxs-lookup"><span data-stu-id="19352-130">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="19352-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="19352-131">NOTES</span></span>

## <span data-ttu-id="19352-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="19352-132">RELATED LINKS</span></span>

[<span data-ttu-id="19352-133">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="19352-133">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)


