---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: CA25260C-D0BF-4F9C-A846-9D9B6C48CE8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationconnectionfieldvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationConnectionFieldValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationConnectionFieldValue.md
ms.openlocfilehash: 2df58153b2617a8ad62b0e46544128fa47a462b5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502263"
---
# <span data-ttu-id="a65ba-101">Set-AzAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="a65ba-101">Set-AzAutomationConnectionFieldValue</span></span>

## <span data-ttu-id="a65ba-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a65ba-102">SYNOPSIS</span></span>
<span data-ttu-id="a65ba-103">Modyfikuje wartość pola w połączeniu automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="a65ba-103">Modifies the value of a field in an Automation connection.</span></span>

## <span data-ttu-id="a65ba-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a65ba-104">SYNTAX</span></span>

```
Set-AzAutomationConnectionFieldValue [-Name] <String> -ConnectionFieldName <String> -Value <Object>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a65ba-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a65ba-105">DESCRIPTION</span></span>
<span data-ttu-id="a65ba-106">Polecenie cmdlet **Set-AzAutomationConnectionFieldValue** modyfikuje wartość pola w połączeniu w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="a65ba-106">The **Set-AzAutomationConnectionFieldValue** cmdlet modifies the value of a field in a connection in Azure Automation.</span></span>

## <span data-ttu-id="a65ba-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a65ba-107">EXAMPLES</span></span>

### <span data-ttu-id="a65ba-108">Przykład 1. Zmienianie wartości pola w połączeniu</span><span class="sxs-lookup"><span data-stu-id="a65ba-108">Example 1: Change a field value in a connection</span></span>
```
PS C:\>Set-AzAutomationConnectionFieldValue -Name "ContosoConnection" -ConnectionFieldName "SubscriptionID" -Value "b53ec456-3494-4847-8f2b-180901c51050" -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="a65ba-109">To polecenie zmienia Identyfikator subskrypcji dla połączenia platformy Azure o nazwie ContosoConnection na koncie usługi Automation o nazwie AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="a65ba-109">This command changes the subscription ID for the Azure connection named ContosoConnection in the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="a65ba-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a65ba-110">PARAMETERS</span></span>

### <span data-ttu-id="a65ba-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a65ba-111">-AutomationAccountName</span></span>
<span data-ttu-id="a65ba-112">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet modyfikuje pole w połączeniu.</span><span class="sxs-lookup"><span data-stu-id="a65ba-112">Specifies the name of the Automation account for which this cmdlet modifies a field in a connection.</span></span>

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

### <span data-ttu-id="a65ba-113">-ConnectionFieldName</span><span class="sxs-lookup"><span data-stu-id="a65ba-113">-ConnectionFieldName</span></span>
<span data-ttu-id="a65ba-114">Określa nazwę pola, które zostanie zmodyfikowane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a65ba-114">Specifies a name for the field that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="a65ba-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a65ba-115">-DefaultProfile</span></span>
<span data-ttu-id="a65ba-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a65ba-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a65ba-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a65ba-117">-Name</span></span>
<span data-ttu-id="a65ba-118">Określa nazwę połączenia, dla którego to polecenie cmdlet modyfikuje pole.</span><span class="sxs-lookup"><span data-stu-id="a65ba-118">Specifies a name for the connection for which this cmdlet modifies a field.</span></span>

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

### <span data-ttu-id="a65ba-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a65ba-119">-ResourceGroupName</span></span>
<span data-ttu-id="a65ba-120">Określa nazwę grupy zasobów, dla której to polecenie cmdlet modyfikuje pole w połączeniu.</span><span class="sxs-lookup"><span data-stu-id="a65ba-120">Specifies the name of the resource group for which this cmdlet modifies a field in a connection.</span></span>

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

### <span data-ttu-id="a65ba-121">-Value</span><span class="sxs-lookup"><span data-stu-id="a65ba-121">-Value</span></span>
<span data-ttu-id="a65ba-122">Określa wartość do zmodyfikowania w polu połączenie.</span><span class="sxs-lookup"><span data-stu-id="a65ba-122">Specifies a value to modify in the connection field.</span></span>

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

### <span data-ttu-id="a65ba-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a65ba-123">CommonParameters</span></span>
<span data-ttu-id="a65ba-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a65ba-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a65ba-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a65ba-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a65ba-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a65ba-126">INPUTS</span></span>

### <span data-ttu-id="a65ba-127">System. String</span><span class="sxs-lookup"><span data-stu-id="a65ba-127">System.String</span></span>

### <span data-ttu-id="a65ba-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="a65ba-128">System.Object</span></span>

## <span data-ttu-id="a65ba-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a65ba-129">OUTPUTS</span></span>

### <span data-ttu-id="a65ba-130">Microsoft. Azure. Commands. Automation. model. Connection</span><span class="sxs-lookup"><span data-stu-id="a65ba-130">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="a65ba-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a65ba-131">NOTES</span></span>

## <span data-ttu-id="a65ba-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a65ba-132">RELATED LINKS</span></span>

[<span data-ttu-id="a65ba-133">Nowe — AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="a65ba-133">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)


