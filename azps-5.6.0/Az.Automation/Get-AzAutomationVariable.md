---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 8FB78A4A-8392-44EE-A907-10FDF756071B
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationVariable.md
ms.openlocfilehash: c30e78b21c8f0dbc59e12c0fbecad14cfc93781a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014129"
---
# <span data-ttu-id="9a144-101">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="9a144-101">Get-AzAutomationVariable</span></span>

## <span data-ttu-id="9a144-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a144-102">SYNOPSIS</span></span>
<span data-ttu-id="9a144-103">Pobiera zmienną automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="9a144-103">Gets an Automation variable.</span></span>

## <span data-ttu-id="9a144-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9a144-104">SYNTAX</span></span>

### <span data-ttu-id="9a144-105">ByAll (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="9a144-105">ByAll (Default)</span></span>
```
Get-AzAutomationVariable [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a144-106">ByName</span><span class="sxs-lookup"><span data-stu-id="9a144-106">ByName</span></span>
```
Get-AzAutomationVariable [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a144-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="9a144-107">DESCRIPTION</span></span>
<span data-ttu-id="9a144-108">Polecenie **cmdlet Get-AzAutomationVariable** pobiera jedną lub więcej zmiennych automatyzacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9a144-108">The **Get-AzAutomationVariable** cmdlet gets one or more Azure Automation variables.</span></span>
<span data-ttu-id="9a144-109">Aby uzyskać określoną zmienną, określ jej nazwę.</span><span class="sxs-lookup"><span data-stu-id="9a144-109">To get a specific variable, specify its name.</span></span>

## <span data-ttu-id="9a144-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9a144-110">EXAMPLES</span></span>

### <span data-ttu-id="9a144-111">Przykład 1. Uzyskiwanie zmiennej</span><span class="sxs-lookup"><span data-stu-id="9a144-111">Example 1: Get a variable</span></span>
```
PS C:\>$Variable = Get-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "Variable06" -ResourceGroupName "ResourceGroup01"
PS C:\> $Value = $Variable.value
```

<span data-ttu-id="9a144-112">Pierwsze polecenie pobiera zmienną automatyzacji o nazwie Variable06 na koncie o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="9a144-112">The first command gets an Automation variable named Variable06 in the account named Contoso17.</span></span>
<span data-ttu-id="9a144-113">Polecenie przechowuje ten obiekt w $Variable zmienną.</span><span class="sxs-lookup"><span data-stu-id="9a144-113">The command stores that object in the $Variable variable.</span></span>
<span data-ttu-id="9a144-114">Drugie polecenie używa standardowej notacji kropki w celu odwołania się do **właściwości wartości** $Variable.</span><span class="sxs-lookup"><span data-stu-id="9a144-114">The second command uses standard dot notation to refer to the **value** property of $Variable.</span></span>
<span data-ttu-id="9a144-115">Polecenie przechowuje wartość w $value zmienną.</span><span class="sxs-lookup"><span data-stu-id="9a144-115">The command stores the value in the $value variable.</span></span>

## <span data-ttu-id="9a144-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9a144-116">PARAMETERS</span></span>

### <span data-ttu-id="9a144-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9a144-117">-AutomationAccountName</span></span>
<span data-ttu-id="9a144-118">Określa nazwę konta automatyzacji zawierającego zmienne, które otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a144-118">Specifies the name of the Automation account that contains the variables that this cmdlet gets.</span></span>

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

### <span data-ttu-id="9a144-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a144-119">-DefaultProfile</span></span>
<span data-ttu-id="9a144-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="9a144-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9a144-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9a144-121">-Name</span></span>
<span data-ttu-id="9a144-122">Określa nazwę zmiennej, która pobiera to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a144-122">Specifies the name of a variable that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a144-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a144-123">-ResourceGroupName</span></span>
<span data-ttu-id="9a144-124">Określa grupę zasobów, dla której to polecenie cmdlet pobiera zmienne.</span><span class="sxs-lookup"><span data-stu-id="9a144-124">Specifies the resource group for which this cmdlet gets variables.</span></span>

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

### <span data-ttu-id="9a144-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a144-125">CommonParameters</span></span>
<span data-ttu-id="9a144-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a144-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a144-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a144-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a144-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9a144-128">INPUTS</span></span>

### <span data-ttu-id="9a144-129">System.String</span><span class="sxs-lookup"><span data-stu-id="9a144-129">System.String</span></span>

## <span data-ttu-id="9a144-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9a144-130">OUTPUTS</span></span>

### <span data-ttu-id="9a144-131">Microsoft.Azure.Commands.Automation.Model.Variable</span><span class="sxs-lookup"><span data-stu-id="9a144-131">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="9a144-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9a144-132">NOTES</span></span>

## <span data-ttu-id="9a144-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9a144-133">RELATED LINKS</span></span>

[<span data-ttu-id="9a144-134">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="9a144-134">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="9a144-135">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="9a144-135">Remove-AzAutomationVariable</span></span>](./Remove-AzAutomationVariable.md)

[<span data-ttu-id="9a144-136">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="9a144-136">Set-AzAutomationVariable</span></span>](./Set-AzAutomationVariable.md)


